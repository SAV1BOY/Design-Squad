# Monthly DS Release Notes

## Title
Script de geração de release notes mensais do design system.

## Purpose

Consolidar todas as mudanças do design system no mês em um documento único de
release notes — novos componentes, atualizações, bug fixes, deprecations e
breaking changes. Comunicação clara de mudanças é essencial para manter a
confiança dos consumers no design system.

## Prerequisites

- **Node.js** >= 18.0
- **Git** com acesso ao repositório do design system
- **Figma API token** para extrair changelog de componentes
- **GitHub API token** para extrair PRs e commits

Variáveis:
```bash
export DS_REPO_PATH="/path/to/design-system"
export GITHUB_TOKEN="ghp_xxxxx"
export GITHUB_REPO="org/design-system"
export FIGMA_API_TOKEN="figd_xxxxx"
```

## Steps

### 1. Extrair dados do Git

```bash
# Listar commits do DS no mês
cd $DS_REPO_PATH
git log --since="$(date -d '1 month ago' +%Y-%m-%d)" \
  --until="$(date +%Y-%m-%d)" \
  --pretty=format:"%H|%s|%an|%ad" \
  --date=short > /tmp/ds-commits.txt

# Extrair PRs merged no mês via GitHub API
node scripts/extract-github-prs.js \
  --repo $GITHUB_REPO \
  --since $(date -d "1 month ago" +%Y-%m-%d) \
  --labels "component,token,documentation,bugfix,breaking-change" \
  --output monthly/data/prs-$(date +%Y%m).json
```

### 2. Extrair dados do Figma

```bash
# Componentes modificados no mês
node scripts/extract-figma-changes.js \
  --file-id $DS_LIBRARY_FILE_ID \
  --since $(date -d "1 month ago" +%Y-%m-%d) \
  --output monthly/data/figma-changes-$(date +%Y%m).json
```

### 3. Categorizar mudanças

```bash
# Categorizar automaticamente por tipo usando conventional commits
node scripts/categorize-ds-changes.js \
  --prs monthly/data/prs-$(date +%Y%m).json \
  --figma monthly/data/figma-changes-$(date +%Y%m).json \
  --output monthly/data/categorized-$(date +%Y%m).json

# Categorias:
# - New: Componentes e tokens novos
# - Changed: Atualizações de componentes existentes
# - Fixed: Bug fixes
# - Deprecated: Componentes/tokens deprecados
# - Breaking: Mudanças que exigem ação dos consumers
# - Docs: Atualizações de documentação
```

### 4. Gerar release notes

```bash
# Gerar documento de release notes
node scripts/generate-ds-release-notes.js \
  --input monthly/data/categorized-$(date +%Y%m).json \
  --template templates/ds-release-notes.md \
  --version "$(node -p "require('$DS_REPO_PATH/package.json').version")" \
  --output monthly/reports/release-notes-$(date +%Y%m).md

# Gerar versão para Slack
node scripts/generate-ds-release-notes.js \
  --input monthly/data/categorized-$(date +%Y%m).json \
  --format slack \
  --output monthly/reports/release-notes-slack-$(date +%Y%m).txt
```

### 5. Enriquecer com screenshots

```bash
# Adicionar screenshots de componentes novos/mudados
node scripts/add-screenshots-to-release.js \
  --release-notes monthly/reports/release-notes-$(date +%Y%m).md \
  --screenshots-dir $SCREENSHOTS_DIR/processed/ \
  --output monthly/reports/release-notes-visual-$(date +%Y%m).md
```

### 6. Publicar

```bash
# Publicar na wiki/documentação
node scripts/publish-release-notes.js \
  --file monthly/reports/release-notes-visual-$(date +%Y%m).md \
  --destination wiki

# Postar no Slack
node scripts/post-to-slack.js \
  --webhook $SLACK_WEBHOOK_URL \
  --file monthly/reports/release-notes-slack-$(date +%Y%m).txt \
  --channel "#design-system"
```

## Expected Output

```markdown
# Design System Release Notes — Março 2026 (v3.2.0)

## Highlights
- 3 novos componentes: Toast, Badge/Status, Skeleton/Card
- Dark mode tokens: primeira versão beta
- 12 bug fixes incluindo 3 de acessibilidade

## New
### Toast Component (stable)
Componente de feedback não-intrusivo com auto-dismiss.
- Variantes: success, error, warning, info
- A11y: aria-live="polite", dismiss via Escape
- Docs: [link] | Figma: [link] | Storybook: [link]

### Badge/Status (stable)
Badge para indicar status de items.
- Variantes: active, inactive, pending, error
- A11y: Contrast AA em todos os estados

### Skeleton/Card (beta)
Loading placeholder para cards.
- API pode mudar durante beta

## Changed
- **Button:** Ajuste de padding em size="sm" (12px → 16px)
- **Input:** Focus ring agora usa outline ao invés de box-shadow
- **Card:** Nova prop `elevation` (low, medium, high)

## Fixed
- **Dropdown:** Focus trap corrigido (a11y)
- **Modal:** Scroll lock em iOS Safari
- **Checkbox:** Contrast de check icon melhorado (3.2:1 → 4.8:1)

## Deprecated
- **Alert/Inline:** Substituído por Toast. Remoção em v4.0.
- **color-primary:** Usar color-action-primary. Alias até v4.0.

## Breaking Changes
Nenhum neste release.

## Migration
Nenhuma ação necessária para upgrade de v3.1 para v3.2.

## Stats
- PRs merged: 23
- Contributors: 8
- Components total: 67 (stable: 58, beta: 6, deprecated: 3)
```

## Automation Notes

- **Frequência:** Primeira segunda-feira de cada mês
- **CI/CD:** Triggered automaticamente com geração de draft para revisão
- **Review:** DS Engineer + Design Lead revisam antes de publicação
- **Screenshots:** Gerados automaticamente via `screenshot-generator.md`
- **Archive:** Todas as release notes archivadas no repositório e wiki
- **Metrics:** Feed para dashboard de DS health e adoption tracking
