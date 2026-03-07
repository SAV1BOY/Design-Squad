# Token Sync Validator

## Title
Script de validação de sincronização entre tokens no Figma e tokens no código.

## Purpose

Verificar que os design tokens definidos no Figma estão sincronizados com os tokens
implementados no código. Detecta: tokens no Figma que não estão no code, tokens no
code que não estão no Figma, e tokens com valores divergentes. A sincronização é
crítica para garantir que designers e desenvolvedores trabalham com a mesma source of truth.

## Prerequisites

- **Node.js** >= 18.0
- **Figma API token** com acesso à library
- **Tokens extraídos do Figma** (via `export-tokens.md`)
- **Tokens buildados do código** (CSS custom properties ou JSON)

## Steps

### 1. Extrair tokens do Figma

```bash
# Extrair tokens atuais do Figma
node scripts/extract-figma-tokens.js \
  --file-id $DS_LIBRARY_FILE_ID \
  --output sync/figma-tokens-$(date +%Y%m%d).json

# Output: JSON com todos os tokens e valores do Figma
```

### 2. Extrair tokens do código

```bash
# Extrair tokens do build atual
node scripts/extract-code-tokens.js \
  --input dist/web/tokens.css \
  --output sync/code-tokens-$(date +%Y%m%d).json

# Para múltiplas plataformas:
node scripts/extract-code-tokens.js \
  --input dist/web/tokens.css,dist/ios/Tokens.swift,dist/android/tokens.xml \
  --output sync/code-tokens-all-$(date +%Y%m%d).json
```

### 3. Comparar tokens

```bash
# Executar comparação
node scripts/compare-tokens.js \
  --figma sync/figma-tokens-$(date +%Y%m%d).json \
  --code sync/code-tokens-$(date +%Y%m%d).json \
  --tolerance "color:0,spacing:0,opacity:0.01" \
  --output sync/comparison-$(date +%Y%m%d).json

# Tolerance: margem aceitável de diferença por tipo
# color: 0 (exato — hex deve ser idêntico)
# spacing: 0 (exato — px deve ser idêntico)
# opacity: 0.01 (permite arredondamento float)
```

### 4. Categorizar diferenças

```bash
# Classificar cada diferença por tipo e severidade
node scripts/categorize-sync-issues.js \
  --input sync/comparison-$(date +%Y%m%d).json \
  --output sync/categorized-$(date +%Y%m%d).json

# Categorias:
# - missing-in-code: Token existe no Figma mas não no código
# - missing-in-figma: Token existe no código mas não no Figma
# - value-mismatch: Token existe em ambos mas com valores diferentes
# - name-mismatch: Token existe mas com naming diferente (possível rename)
```

### 5. Gerar relatório

```bash
# Relatório detalhado
node scripts/generate-sync-report.js \
  --input sync/categorized-$(date +%Y%m%d).json \
  --format md \
  --output sync/reports/sync-report-$(date +%Y%m%d).md
```

## Expected Output

```markdown
# Token Sync Report — [Data]

## Summary
- Tokens no Figma: 234
- Tokens no código: 228
- Sincronizados: 220 (94.0%)
- Divergentes: 14 (6.0%)

## Missing in Code (6 tokens)
Tokens definidos no Figma que não existem no código:

| Token | Figma Value | Provável causa |
|-------|-------------|---------------|
| color-surface-tertiary | #FAFAFA | Novo — adicionado no Figma, não exportado |
| spacing-xxs | 2px | Novo — adicionado no Figma |
| shadow-xs | 0 1px 2px rgba(0,0,0,0.05) | Novo |

## Missing in Figma (2 tokens)
Tokens no código que não existem no Figma:

| Token | Code Value | Provável causa |
|-------|-----------|---------------|
| color-legacy-blue | #0066CC | Legacy — remover do código |
| spacing-custom-header | 76px | Custom — não deveria ser token |

## Value Mismatch (6 tokens)
Tokens que existem em ambos com valores diferentes:

| Token | Figma | Code | Delta |
|-------|-------|------|-------|
| color-action-primary | #1A73E8 | #1976D2 | Hex diferente |
| spacing-lg | 24px | 32px | 8px de diferença |
| radius-md | 8px | 6px | 2px de diferença |
| font-size-heading-lg | 28px | 24px | 4px de diferença |

## Action Items
- [ ] Exportar 6 tokens novos do Figma para código
- [ ] Remover 2 tokens legacy do código
- [ ] Resolver 6 conflitos de valor (Figma é source of truth)
```

## Automation Notes

- **Frequência:** Diária (overnight) — alerta se divergência > 5%
- **CI/CD:** Roda como check em PRs que tocam tokens
- **Blocking:** Divergência em tokens semânticos bloqueia release
- **Source of truth:** Figma é source of truth para valores de design
- **Alert:** Divergência > 10% envia alerta para #design-system
- **History:** Reports archivados para tracking de sync health
