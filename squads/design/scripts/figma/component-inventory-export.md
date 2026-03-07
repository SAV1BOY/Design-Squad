# Component Inventory Export

## Title
Script de exportação do inventário de componentes do Figma para análise e tracking.

## Purpose

Gerar um inventário completo de todos os componentes publicados nas libraries do
Figma, incluindo: nome, variantes, uso por arquivo, última modificação e status
de documentação. Usado para audits de design system, tracking de adoption e
identificação de componentes candidatos a deprecation.

## Prerequisites

- **Node.js** >= 18.0
- **Figma API token** com acesso às libraries do time
- **jq** para processamento de JSON (opcional, para análise rápida)
- **Acesso de leitura** a todas as libraries do design system no Figma

Variáveis de ambiente:
```bash
export FIGMA_API_TOKEN="figd_xxxxxxxxxxxxx"
export DS_LIBRARY_FILE_ID="xxxxxxxxxxxxx"    # DS Core Library
export DS_ICONS_FILE_ID="xxxxxxxxxxxxx"      # DS Icons
export DS_ILLUSTRATIONS_FILE_ID="xxxxxxxxxxxxx"  # DS Illustrations
```

## Steps

### 1. Extrair componentes da library

```bash
# Extrair todos os componentes publicados
node scripts/figma-component-inventory.js \
  --files $DS_LIBRARY_FILE_ID,$DS_ICONS_FILE_ID,$DS_ILLUSTRATIONS_FILE_ID \
  --output inventory/raw/

# Output: inventory/raw/components.json
```

### 2. Enriquecer com dados de uso

```bash
# Buscar quantos arquivos usam cada componente (Figma Analytics API)
node scripts/figma-usage-stats.js \
  --components inventory/raw/components.json \
  --team-id $FIGMA_TEAM_ID \
  --output inventory/enriched/

# Output: inventory/enriched/components-with-usage.json
```

### 3. Gerar relatório

```bash
# Gerar relatório em múltiplos formatos
node scripts/generate-inventory-report.js \
  --input inventory/enriched/components-with-usage.json \
  --output-csv inventory/reports/inventory-$(date +%Y%m%d).csv \
  --output-md inventory/reports/inventory-$(date +%Y%m%d).md \
  --output-json inventory/reports/inventory-$(date +%Y%m%d).json
```

### 4. Analisar resultados

```bash
# Componentes mais usados (top 20)
jq '.components | sort_by(-.usageCount) | .[0:20] | .[] | {name, usageCount}' \
  inventory/enriched/components-with-usage.json

# Componentes sem uso (candidatos a deprecation)
jq '.components | map(select(.usageCount == 0)) | .[] | .name' \
  inventory/enriched/components-with-usage.json

# Componentes sem documentação
jq '.components | map(select(.hasDescription == false)) | length' \
  inventory/enriched/components-with-usage.json

# Variantes por componente (complexidade)
jq '.components | sort_by(-.variantCount) | .[0:10] | .[] | {name, variantCount}' \
  inventory/enriched/components-with-usage.json
```

### 5. Diff com inventário anterior

```bash
# Comparar com último inventário para identificar mudanças
node scripts/inventory-diff.js \
  --old inventory/reports/inventory-previous.json \
  --new inventory/reports/inventory-$(date +%Y%m%d).json \
  --output inventory/reports/diff-$(date +%Y%m%d).md
```

## Expected Output

Arquivo CSV com colunas:
```
component_name | library | variant_count | usage_count | last_modified | has_docs | status
Button/Primary | DS Core | 5 | 347 | 2026-02-28 | true | stable
Card/Product   | DS Core | 3 | 189 | 2026-03-01 | true | stable
Modal/Alert    | DS Core | 2 | 12  | 2025-11-15 | false | review
```

Relatório markdown com:
- Total de componentes: [N]
- Componentes com docs: [N] ([%])
- Componentes sem uso: [N] (candidatos a deprecation)
- Top 10 mais usados
- Top 10 com mais variantes
- Componentes modificados desde último report

## Automation Notes

- **Frequência:** Mensal (primeira segunda-feira do mês)
- **CI/CD:** GitHub Actions scheduled workflow
- **Storage:** Reports archivados no repositório em `/reports/inventory/`
- **Notificação:** Summary postado no #design-system mensalmente
- **Dashboard:** Dados alimentam o dashboard de DS health em [link]
- **Retention:** Manter últimos 12 reports para análise de tendência
