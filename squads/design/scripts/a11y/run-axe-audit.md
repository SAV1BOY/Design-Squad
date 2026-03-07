# Run Axe Audit

## Title
Script de audit automatizado de acessibilidade usando axe-core.

## Purpose

Executar varredura automatizada de acessibilidade em todas as páginas do produto
usando axe-core. Identifica violações de WCAG 2.2 AA programaticamente, gerando
relatório com severidade, localização e sugestão de correção. Cobre aproximadamente
30-40% dos issues possíveis — o restante requer revisão manual.

## Prerequisites

- **Node.js** >= 18.0
- **@axe-core/cli** — `npm install -g @axe-core/cli`
- **Puppeteer** ou **Playwright** para navegação automatizada
- **axe-core** >= 4.8
- **Produto rodando** em ambiente acessível (staging ou local)

Dependências:
```bash
npm install @axe-core/puppeteer puppeteer
# ou
npm install @axe-core/playwright @playwright/test
```

Variáveis:
```bash
export BASE_URL="https://staging.produto.com.br"
export AUDIT_OUTPUT_DIR="./audit-results"
```

## Steps

### 1. Definir páginas para audit

```bash
# Lista de URLs a auditar (todas as páginas core)
cat > audit-urls.json << 'EOF'
{
  "pages": [
    {"name": "Home", "url": "/"},
    {"name": "Login", "url": "/login"},
    {"name": "Cadastro", "url": "/cadastro"},
    {"name": "Dashboard", "url": "/dashboard"},
    {"name": "Checkout - Cart", "url": "/checkout/cart"},
    {"name": "Checkout - Payment", "url": "/checkout/payment"},
    {"name": "Checkout - Confirmation", "url": "/checkout/confirmation"},
    {"name": "Profile", "url": "/profile"},
    {"name": "Settings", "url": "/settings"},
    {"name": "Search Results", "url": "/search?q=test"}
  ]
}
EOF
```

### 2. Executar audit

```bash
# Audit completo com Puppeteer
node scripts/axe-audit.js \
  --urls audit-urls.json \
  --base-url $BASE_URL \
  --standard wcag22aa \
  --output $AUDIT_OUTPUT_DIR/audit-$(date +%Y%m%d).json \
  --screenshot true \
  --viewport "1440x900,375x812"

# Audit rápido via CLI (página única)
npx axe $BASE_URL/login --rules wcag22aa --save audit-login.json
```

### 3. Gerar relatório

```bash
# Relatório detalhado
node scripts/generate-a11y-report.js \
  --input $AUDIT_OUTPUT_DIR/audit-$(date +%Y%m%d).json \
  --format md \
  --output $AUDIT_OUTPUT_DIR/report-$(date +%Y%m%d).md

# Relatório executivo (resumo para stakeholders)
node scripts/generate-a11y-report.js \
  --input $AUDIT_OUTPUT_DIR/audit-$(date +%Y%m%d).json \
  --format executive \
  --output $AUDIT_OUTPUT_DIR/executive-$(date +%Y%m%d).md
```

### 4. Comparar com audit anterior

```bash
# Identificar novos issues e issues resolvidos
node scripts/a11y-diff.js \
  --old $AUDIT_OUTPUT_DIR/audit-previous.json \
  --new $AUDIT_OUTPUT_DIR/audit-$(date +%Y%m%d).json \
  --output $AUDIT_OUTPUT_DIR/diff-$(date +%Y%m%d).md
```

### 5. Criar tickets para violations

```bash
# Gerar tickets automaticamente para violations critical/serious
node scripts/create-a11y-tickets.js \
  --input $AUDIT_OUTPUT_DIR/audit-$(date +%Y%m%d).json \
  --severity critical,serious \
  --project DESIGN \
  --labels accessibility,automated
```

## Expected Output

```markdown
# Accessibility Audit Report — [Data]

## Score: 78/100

## Summary
| Severity | Count | Delta |
|----------|-------|-------|
| Critical | 2 | -1 |
| Serious  | 8 | -3 |
| Moderate | 15 | +2 |
| Minor    | 23 | -5 |

## Critical Issues
### 1. Images missing alt text (3 instances)
- **Rule:** image-alt
- **WCAG:** 1.1.1 Non-text Content (A)
- **Pages:** Home, Dashboard
- **Fix:** Adicionar alt text descritivo ou alt="" para decorativas

### 2. Form inputs without labels (2 instances)
- **Rule:** label
- **WCAG:** 1.3.1 Info and Relationships (A)
- **Pages:** Login, Cadastro
- **Fix:** Associar label via for/id ou aria-label

## Compliance by Page
| Page | Score | Critical | Serious |
|------|-------|----------|---------|
| Home | 82 | 1 | 2 |
| Login | 71 | 1 | 3 |
| Dashboard | 85 | 0 | 1 |
```

## Automation Notes

- **Frequência:** Semanal (domingo à noite) + on-demand pré-release
- **CI/CD:** GitHub Actions com Playwright, roda em staging após deploy
- **Threshold:** Build falha se violations critical > 0 em fluxos core
- **Notification:** Relatório postado no #design-squad toda segunda
- **Tracking:** Dados alimentam dashboard de a11y compliance em [link]
- **Limitação:** axe-core não detecta issues de lógica, semântica contextual
  ou usabilidade com assistive tech — complementar com revisão manual
