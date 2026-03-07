# Focus Order Validator

## Title
Script de validação da ordem de foco (tab order) em interfaces.

## Purpose

Verificar automaticamente se a ordem de foco via teclado (Tab navigation) segue
uma sequência lógica e intuitiva em todas as páginas do produto. Identifica
elementos fora de ordem, elementos interativos não focáveis, e focus traps
(lugares onde o foco fica "preso").

Focus order incorreta é uma das violações de a11y mais comuns e mais impactantes
para usuários de teclado e screen reader.

## Prerequisites

- **Node.js** >= 18.0
- **Playwright** >= 1.40 (preferido sobre Puppeteer para testes de keyboard)
- **Produto rodando** em ambiente acessível
- **Focus order specs** do design (definidos no handoff)

Dependências:
```bash
npm install @playwright/test
npx playwright install chromium
```

## Steps

### 1. Definir expected focus order

```bash
# Arquivo de specs de focus order por página
cat > focus-specs/login.json << 'EOF'
{
  "page": "Login",
  "url": "/login",
  "expectedOrder": [
    {"role": "link", "name": "Logo - Voltar ao início"},
    {"role": "textbox", "name": "Email"},
    {"role": "textbox", "name": "Senha"},
    {"role": "link", "name": "Esqueceu a senha?"},
    {"role": "button", "name": "Entrar"},
    {"role": "link", "name": "Criar conta"}
  ]
}
EOF
```

### 2. Capturar focus order real

```bash
# Navegar pela página usando Tab e registrar ordem de foco
node scripts/capture-focus-order.js \
  --url "$BASE_URL/login" \
  --max-tabs 50 \
  --output focus/captured/login-$(date +%Y%m%d).json \
  --screenshot-each true

# O script:
# 1. Carrega a página
# 2. Pressiona Tab repetidamente
# 3. Para cada elemento focado, registra: tag, role, name, position, tabindex
# 4. Detecta ciclo (foco volta ao início) ou trap (foco não avança)
```

### 3. Comparar com expected order

```bash
# Comparar ordem capturada com ordem especificada
node scripts/validate-focus-order.js \
  --expected focus-specs/login.json \
  --captured focus/captured/login-$(date +%Y%m%d).json \
  --output focus/results/login-validation-$(date +%Y%m%d).json
```

### 4. Detectar problemas comuns

```bash
# Verificações adicionais além da ordem
node scripts/focus-issues-detector.js \
  --url "$BASE_URL/login" \
  --checks "trap,skip,invisible,no-indicator,tabindex-positive" \
  --output focus/results/issues-$(date +%Y%m%d).json

# Checks disponíveis:
# - trap: foco preso em região sem saída
# - skip: elementos interativos não recebem foco
# - invisible: elementos focáveis que não estão visíveis
# - no-indicator: foco sem indicador visual (focus ring)
# - tabindex-positive: uso de tabindex > 0 (anti-pattern)
# - modal-trap: modal sem focus trap (foco escapa para trás)
```

### 5. Gerar relatório

```bash
# Relatório consolidado de todas as páginas
node scripts/generate-focus-report.js \
  --results-dir focus/results/ \
  --format md \
  --output focus/reports/focus-report-$(date +%Y%m%d).md
```

## Expected Output

```markdown
# Focus Order Validation — [Data]

## Summary
- Páginas testadas: 10
- Páginas OK: 7
- Páginas com issues: 3

## Issues Found

### Login (/login)
- SKIP: Link "Termos de uso" no footer não recebe foco (tabindex="-1")
- ORDER: "Esqueceu a senha?" foca ANTES do campo "Senha" (esperado: depois)
- NO-INDICATOR: Campo "Email" sem focus ring visível em Chrome

### Checkout (/checkout/payment)
- TRAP: Dropdown de "País" prende o foco — Escape não fecha
- SKIP: Botão "Remover cupom" (ícone X) não é focável
- MODAL-TRAP: Modal de confirmação não implementa focus trap

### Dashboard (/dashboard)
- TABINDEX: 3 elementos com tabindex="5" — remover e usar DOM order
- ORDER: Sidebar foca antes do conteúdo principal (lógica visual: conteúdo primeiro)

## Focus Order Comparison — Login

| # | Expected | Actual | Match |
|---|----------|--------|-------|
| 1 | Logo link | Logo link | OK |
| 2 | Email input | Email input | OK |
| 3 | Senha input | Esqueceu senha link | MISMATCH |
| 4 | Esqueceu senha link | Senha input | MISMATCH |
| 5 | Entrar button | Entrar button | OK |
| 6 | Criar conta link | Criar conta link | OK |
```

## Automation Notes

- **Frequência:** Por sprint (antes de release) + on-demand para features novas
- **CI/CD:** Playwright test suite integrada ao pipeline de staging
- **Blocking:** Focus trap em modal ou focus skip em CTA = blocker para release
- **Specs:** Designers devem definir expected focus order no handoff (ver `handoff-standards.md`)
- **Limitation:** Não testa com screen reader real — complementar com teste manual
- **Dynamic content:** Conteúdo carregado assincronamente pode alterar focus order — testar após load
