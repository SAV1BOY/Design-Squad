# Token Diff Report

## Title
Script de geração de relatório de diferenças entre versões de tokens.

## Purpose

Gerar um relatório detalhado das mudanças entre duas versões de design tokens —
tokens adicionados, removidos, renomeados e com valor alterado. Essencial para
comunicar breaking changes, gerar release notes do design system e planejar
migrações.

## Prerequisites

- **Node.js** >= 18.0
- **Duas versões de tokens** para comparar (JSON, CSS ou SCSS)
- **Git** para acessar versões históricas de tokens

Dependências:
```bash
npm install deep-diff chalk
```

## Steps

### 1. Obter versões para comparar

```bash
# Opção A: Comparar branches
git show main:dist/web/tokens.json > tokens-old.json
git show develop:dist/web/tokens.json > tokens-new.json

# Opção B: Comparar tags de release
git show v2.5.0:dist/web/tokens.json > tokens-old.json
git show v3.0.0:dist/web/tokens.json > tokens-new.json

# Opção C: Comparar com arquivo local atual
cp dist-previous/web/tokens.json tokens-old.json
cp dist/web/tokens.json tokens-new.json
```

### 2. Gerar diff

```bash
# Diff detalhado entre versões
node scripts/token-diff.js \
  --old tokens-old.json \
  --new tokens-new.json \
  --output diff/token-diff-$(date +%Y%m%d).json

# Com categorização por tipo de mudança
node scripts/token-diff.js \
  --old tokens-old.json \
  --new tokens-new.json \
  --categorize true \
  --detect-renames true \
  --output diff/token-diff-categorized-$(date +%Y%m%d).json
```

### 3. Classificar impacto

```bash
# Classificar cada mudança por impacto
node scripts/classify-token-changes.js \
  --input diff/token-diff-categorized-$(date +%Y%m%d).json \
  --output diff/classified-$(date +%Y%m%d).json

# Classificação:
# - breaking: Remoção ou rename sem alias
# - migration-needed: Mudança de valor que pode afetar visual
# - safe: Adição de novo token ou mudança sem impacto
```

### 4. Gerar relatório

```bash
# Relatório para release notes
node scripts/generate-diff-report.js \
  --input diff/classified-$(date +%Y%m%d).json \
  --format release-notes \
  --output diff/reports/release-notes-tokens.md

# Relatório para migration guide
node scripts/generate-diff-report.js \
  --input diff/classified-$(date +%Y%m%d).json \
  --format migration \
  --output diff/reports/migration-guide.md

# Relatório para Slack
node scripts/generate-diff-report.js \
  --input diff/classified-$(date +%Y%m%d).json \
  --format slack \
  --output diff/reports/slack-announcement.txt
```

### 5. Gerar codemod (se houver breaking changes)

```bash
# Gerar script de migração automática
node scripts/generate-token-codemod.js \
  --changes diff/classified-$(date +%Y%m%d).json \
  --filter "breaking,migration-needed" \
  --output diff/codemods/migrate-tokens.js

# Testar codemod
node diff/codemods/migrate-tokens.js --dry-run --dir src/
```

## Expected Output

```markdown
# Token Diff Report — v2.5.0 → v3.0.0

## Summary
- Added: 12 tokens
- Removed: 3 tokens
- Changed: 8 tokens
- Renamed: 2 tokens
- Total breaking changes: 5

## Breaking Changes

### Removed Tokens
| Token | Old Value | Migration |
|-------|-----------|-----------|
| color-primary | #1976D2 | Use color-action-primary |
| color-secondary | #388E3C | Use color-action-secondary |
| spacing-base | 8px | Use spacing-md |

### Renamed Tokens
| Old Name | New Name |
|----------|----------|
| color-bg-main | color-surface-primary |
| color-bg-card | color-surface-secondary |

## Value Changes

| Token | Old | New | Impact |
|-------|-----|-----|--------|
| color-action-primary | #1976D2 | #1A73E8 | Visual change |
| spacing-lg | 32px | 24px | Layout shift |
| radius-md | 6px | 8px | Visual change |

## New Tokens
| Token | Value | Purpose |
|-------|-------|---------|
| color-surface-tertiary | #FAFAFA | Fundo alternativo |
| shadow-xs | 0 1px 2px ... | Elevação sutil |

## Migration Guide
1. Run codemod: `node migrate-tokens.js --dir src/`
2. Review visual changes manually
3. Update snapshots: `UPDATE_SNAPSHOTS=true npm test`
```

## Automation Notes

- **Frequência:** A cada release do design system
- **CI/CD:** Gerado automaticamente quando tag de release é criada
- **Blocking:** Breaking changes sem migration guide bloqueiam release
- **Distribution:** Relatório enviado para #design-system e todos os squad leads
- **Codemod:** Testado automaticamente contra codebase de referência antes de publicar
