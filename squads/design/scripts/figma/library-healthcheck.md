# Library Healthcheck

## Title
Script de verificação de saúde das libraries do design system no Figma.

## Purpose

Executar verificações automatizadas na library do Figma para identificar problemas
de qualidade: componentes sem descrição, naming inconsistente, layers desordenadas,
variantes incompletas e tokens desatualizados. É o "linting" do Figma.

## Prerequisites

- **Node.js** >= 18.0
- **Figma API token** com acesso de leitura às libraries
- **Regras de linting** configuradas em `figma-lint.config.json`
- **Figma file IDs** das libraries a verificar

Arquivo de configuração `figma-lint.config.json`:
```json
{
  "rules": {
    "component-has-description": "error",
    "component-naming-convention": "error",
    "no-unnamed-layers": "warning",
    "no-absolute-positioning": "warning",
    "auto-layout-preferred": "warning",
    "variant-naming-consistent": "error",
    "no-detached-instances": "error",
    "color-uses-style-or-variable": "error",
    "text-uses-style": "error",
    "spacing-uses-variable": "warning"
  }
}
```

## Steps

### 1. Fetch da estrutura do arquivo Figma

```bash
# Baixar a tree completa do arquivo Figma
node scripts/figma-fetch-tree.js \
  --file-id $DS_LIBRARY_FILE_ID \
  --depth 5 \
  --output healthcheck/raw/tree.json
```

### 2. Executar regras de linting

```bash
# Rodar todas as regras configuradas
node scripts/figma-lint.js \
  --config figma-lint.config.json \
  --input healthcheck/raw/tree.json \
  --output healthcheck/results/lint-$(date +%Y%m%d).json

# Rodar apenas uma categoria de regras
node scripts/figma-lint.js \
  --config figma-lint.config.json \
  --input healthcheck/raw/tree.json \
  --rules "component-*" \
  --output healthcheck/results/lint-components.json
```

### 3. Gerar relatório

```bash
# Relatório detalhado com todas as violations
node scripts/generate-lint-report.js \
  --input healthcheck/results/lint-$(date +%Y%m%d).json \
  --format md \
  --output healthcheck/reports/healthcheck-$(date +%Y%m%d).md

# Relatório resumido para Slack
node scripts/generate-lint-report.js \
  --input healthcheck/results/lint-$(date +%Y%m%d).json \
  --format slack \
  --output healthcheck/reports/healthcheck-slack.txt
```

### 4. Comparar com healthcheck anterior

```bash
# Trend de saúde ao longo do tempo
node scripts/healthcheck-trend.js \
  --reports-dir healthcheck/reports/ \
  --output healthcheck/reports/trend.json
```

## Expected Output

Relatório markdown:
```markdown
# Library Healthcheck — [Data]

## Score: 87/100 (up from 82)

## Summary
- Errors: 12 (down from 18)
- Warnings: 34 (down from 41)
- Components checked: 156
- Layers checked: 2,847

## Errors (must fix)
| Rule | Count | Components |
|------|-------|------------|
| component-has-description | 5 | Modal/Confirm, Tooltip/Info, ... |
| variant-naming-consistent | 4 | Card/*, Badge/* |
| color-uses-style-or-variable | 3 | Header, Footer, Sidebar |

## Warnings (should fix)
| Rule | Count | Components |
|------|-------|------------|
| no-unnamed-layers | 18 | Various |
| auto-layout-preferred | 12 | Various |
| spacing-uses-variable | 4 | Card/Product, List/Item |

## Trend (last 6 months)
Score: 71 → 75 → 79 → 82 → 85 → 87
```

## Automation Notes

- **Frequência:** Semanal (segunda-feira 8h, antes do design sync)
- **CI/CD:** GitHub Actions scheduled workflow
- **Threshold:** Score < 80 gera alerta no #design-system
- **Trend tracking:** Dados armazenados para gráfico de evolução mensal
- **Blocker:** Score < 70 bloqueia release de novas versões do DS
- **Ownership:** Violations são atribuídas ao último editor do componente
