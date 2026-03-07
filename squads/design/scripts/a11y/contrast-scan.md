# Contrast Scan

## Title
Script de varredura automatizada de contraste de cores em interfaces.

## Purpose

Verificar automaticamente se todas as combinações de cor texto/fundo na interface
atendem aos requisitos mínimos de contraste WCAG 2.2. Identifica violações,
calcula contrast ratio exato e sugere cores alternativas que passam no critério.

## Prerequisites

- **Node.js** >= 18.0
- **Puppeteer** para captura de estilos computados
- **color** ou **chroma-js** para cálculos de contraste
- **Produto rodando** em ambiente acessível

Dependências:
```bash
npm install puppeteer chroma-js
```

## Steps

### 1. Capturar pares de cor da interface

```bash
# Extrair todos os pares texto/fundo de todas as páginas
node scripts/contrast-scan.js \
  --urls audit-urls.json \
  --base-url $BASE_URL \
  --output contrast/raw/pairs-$(date +%Y%m%d).json \
  --viewport "1440x900"

# O script navega cada página e extrai:
# - Cor do texto (computed color)
# - Cor do fundo (computed background-color, resolve gradients e overlays)
# - Tamanho da fonte (para determinar se é "large text")
# - Seletor CSS do elemento (para localização)
```

### 2. Calcular contrast ratios

```bash
# Calcular ratio para cada par e classificar
node scripts/calculate-contrast.js \
  --input contrast/raw/pairs-$(date +%Y%m%d).json \
  --standard wcag22aa \
  --output contrast/results/ratios-$(date +%Y%m%d).json

# Critérios WCAG 2.2 AA:
# - Texto normal (< 18pt ou < 14pt bold): mínimo 4.5:1
# - Texto grande (>= 18pt ou >= 14pt bold): mínimo 3:1
# - UI components e graphics: mínimo 3:1
```

### 3. Gerar sugestões de correção

```bash
# Para cada violação, sugerir cor alternativa mais próxima que passa
node scripts/suggest-contrast-fix.js \
  --input contrast/results/ratios-$(date +%Y%m%d).json \
  --strategy "darken-text" \
  --output contrast/results/suggestions-$(date +%Y%m%d).json

# Estratégias disponíveis:
# - darken-text: escurece o texto até passar
# - lighten-bg: clareia o fundo até passar
# - closest-palette: sugere cor mais próxima da palette do DS que passa
```

### 4. Mapear para tokens

```bash
# Identificar quais tokens estão causando violações
node scripts/map-contrast-to-tokens.js \
  --violations contrast/results/ratios-$(date +%Y%m%d).json \
  --tokens dist/web/tokens.json \
  --output contrast/results/token-violations-$(date +%Y%m%d).json

# Identifica: "color-text-secondary (#999) sobre color-surface-primary (#FFF)
# = 2.85:1, abaixo de 4.5:1. Fix no token: mudar color-text-secondary para #767676"
```

### 5. Gerar relatório visual

```bash
# Gerar relatório com swatches visuais
node scripts/generate-contrast-report.js \
  --input contrast/results/ratios-$(date +%Y%m%d).json \
  --suggestions contrast/results/suggestions-$(date +%Y%m%d).json \
  --format html \
  --output contrast/reports/contrast-report-$(date +%Y%m%d).html

# Formato markdown para docs
node scripts/generate-contrast-report.js \
  --input contrast/results/ratios-$(date +%Y%m%d).json \
  --format md \
  --output contrast/reports/contrast-report-$(date +%Y%m%d).md
```

## Expected Output

```markdown
# Contrast Scan Report — [Data]

## Summary
- Pares analisados: 487
- Passando: 451 (92.6%)
- Falhando: 36 (7.4%)
  - Texto normal: 28 violations
  - Texto grande: 5 violations
  - UI components: 3 violations

## Top Violations by Token

| Token | Valor | Contra | Ratio | Mínimo | Sugestão |
|-------|-------|--------|-------|--------|----------|
| color-text-secondary | #999 | #FFF | 2.85:1 | 4.5:1 | #767676 |
| color-text-tertiary | #BBB | #F5F5F5 | 1.65:1 | 4.5:1 | #767676 |
| color-text-disabled | #CCC | #FFF | 1.61:1 | 3:1 | #949494 |

## Violations by Page
| Page | Violations | Most common |
|------|-----------|-------------|
| Home | 8 | color-text-secondary |
| Dashboard | 12 | color-text-tertiary |
| Settings | 6 | color-text-disabled |
```

## Automation Notes

- **Frequência:** Semanal + após mudanças em color tokens
- **CI/CD:** Integrado ao pipeline de token build
- **Threshold:** 0 violations em tokens semânticos = blocking
- **Figma integration:** Resultados podem alimentar o Stark plugin config
- **Dark mode:** Executar scan separado com `--theme dark` para validar ambos
- **Edge case:** Gradients e imagens de fundo podem não ser detectados — manual review
