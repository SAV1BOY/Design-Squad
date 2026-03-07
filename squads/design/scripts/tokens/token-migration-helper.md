# Token Migration Helper

## Title
Script auxiliar para migração de tokens entre versões do design system.

## Purpose

Facilitar a migração de tokens quando o design system lança breaking changes.
O script identifica todas as ocorrências de tokens antigos no codebase, sugere
o replacement correto, e pode aplicar as mudanças automaticamente (codemod).

Migrar tokens manualmente em um codebase grande é propenso a erro e consome dias.
Este helper reduz para minutos.

## Prerequisites

- **Node.js** >= 18.0
- **Migration map** gerado pelo `token-diff-report.md`
- **Git** limpo (sem mudanças uncommitted) — o script modifica arquivos
- **Acesso de escrita** ao repositório do produto

Dependências:
```bash
npm install glob jscodeshift postcss
```

## Steps

### 1. Gerar migration map

```bash
# O migration map define: token antigo → token novo
# Pode ser gerado automaticamente pelo token-diff ou manualmente

cat > migration-map.json << 'EOF'
{
  "version": "2.5.0 → 3.0.0",
  "date": "2026-03-07",
  "mappings": [
    {
      "old": "color-primary",
      "new": "color-action-primary",
      "type": "rename"
    },
    {
      "old": "color-bg-main",
      "new": "color-surface-primary",
      "type": "rename"
    },
    {
      "old": "spacing-base",
      "new": "spacing-md",
      "type": "rename",
      "note": "Valor mudou de 8px para 16px — verificar visualmente"
    },
    {
      "old": "color-secondary",
      "new": "color-action-secondary",
      "type": "rename"
    }
  ]
}
EOF
```

### 2. Scan do codebase

```bash
# Identificar todas as ocorrências de tokens antigos
node scripts/scan-token-usage.js \
  --migration-map migration-map.json \
  --dirs "src/,styles/,components/" \
  --extensions ".css,.scss,.tsx,.jsx,.ts,.js" \
  --output migration/scan-results-$(date +%Y%m%d).json

# Output: lista de arquivos e linhas que usam tokens antigos
```

### 3. Preview das mudanças

```bash
# Dry-run — mostra o que seria mudado sem aplicar
node scripts/migrate-tokens.js \
  --migration-map migration-map.json \
  --dirs "src/,styles/,components/" \
  --dry-run true \
  --output migration/preview-$(date +%Y%m%d).md
```

### 4. Aplicar migração

```bash
# Aplicar mudanças no codebase
node scripts/migrate-tokens.js \
  --migration-map migration-map.json \
  --dirs "src/,styles/,components/" \
  --dry-run false \
  --backup true \
  --output migration/applied-$(date +%Y%m%d).json

# O flag --backup cria cópias .bak dos arquivos modificados
```

### 5. Verificar migração

```bash
# Re-scan para verificar que nenhum token antigo permaneceu
node scripts/scan-token-usage.js \
  --migration-map migration-map.json \
  --dirs "src/,styles/,components/" \
  --output migration/post-migration-scan.json

# Verificar: deve retornar 0 ocorrências de tokens antigos

# Rodar testes existentes
npm test

# Rodar visual regression para detectar mudanças visuais
npx playwright test --config playwright.visual.config.ts
```

### 6. Commit e PR

```bash
# Commit com mensagem descritiva
git add -A
git commit -m "chore: migrate tokens from DS v2.5 to v3.0

Migration applied via token-migration-helper.
Changes:
- color-primary → color-action-primary (8 files)
- color-bg-main → color-surface-primary (12 files)
- spacing-base → spacing-md (23 files)
- color-secondary → color-action-secondary (5 files)

Migration map: migration-map.json
Visual regression: [link to test results]"

git push origin design/token-migration-v3
```

## Expected Output

Preview (dry-run):
```markdown
# Token Migration Preview — v2.5.0 → v3.0.0

## Files to modify: 48

## Changes by token

### color-primary → color-action-primary
- src/components/Button.tsx (line 15, 23)
- src/components/Link.tsx (line 8)
- styles/global.scss (line 42, 56, 78)
- styles/components/header.scss (line 12)
Total: 8 occurrences in 4 files

### color-bg-main → color-surface-primary
- src/layouts/MainLayout.tsx (line 3)
- styles/global.scss (line 5, 10)
- styles/components/card.scss (line 2, 8)
Total: 12 occurrences in 5 files

### spacing-base → spacing-md (VALUE CHANGED: 8px → 16px)
- [23 files — MANUAL REVIEW RECOMMENDED]
Total: 45 occurrences in 23 files

## Warnings
- spacing-base: valor mudou além do nome — verificar impacto visual
- 3 ocorrências em arquivos .min.css — estes são gerados, migrar source
```

## Automation Notes

- **Quando usar:** A cada major version do design system com breaking changes
- **Safety:** Sempre rodar dry-run primeiro e revisar output
- **Backup:** Flag --backup é habilitado por default
- **Testing:** Visual regression obrigatório após migração
- **Partial migration:** Suporte a migrar por diretório para PRs menores
- **Rollback:** `git checkout .` reverte todas as mudanças se necessário
