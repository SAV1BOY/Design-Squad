# Export Tokens

## Title
Script de exportação de design tokens do Figma para formato consumível por código.

## Purpose

Automatizar a extração de design tokens definidos no Figma (via Figma Tokens plugin
ou Figma Variables) e converter para formatos consumíveis por Style Dictionary, CSS
custom properties, Swift constants e Kotlin constants.

Este script é parte do pipeline de sincronização Figma → Code e deve ser executado
sempre que tokens são atualizados no Figma.

## Prerequisites

- **Node.js** >= 18.0
- **Figma Tokens plugin** configurado com sync para repositório Git
- **Figma API token** — Gerar em Figma > Settings > Personal Access Tokens
- **Style Dictionary** >= 4.0 instalado globalmente ou como dev dependency
- **Acesso ao repositório** de tokens (design-system-tokens repo)

Variáveis de ambiente necessárias:
```bash
export FIGMA_API_TOKEN="figd_xxxxxxxxxxxxx"
export FIGMA_FILE_ID="xxxxxxxxxxxxxxx"
export TOKENS_REPO_PATH="/path/to/design-system-tokens"
```

## Steps

### 1. Extrair tokens do Figma

```bash
# Opção A: Via Figma Tokens plugin (sync com Git)
# O plugin sincroniza automaticamente para tokens.json no repositório
cd $TOKENS_REPO_PATH
git pull origin main

# Opção B: Via Figma Variables API (REST)
curl -s -H "X-Figma-Token: $FIGMA_API_TOKEN" \
  "https://api.figma.com/v1/files/$FIGMA_FILE_ID/variables/local" \
  -o raw-variables.json

# Opção C: Via script Node.js custom
node scripts/extract-figma-variables.js \
  --file-id $FIGMA_FILE_ID \
  --output tokens/raw/
```

### 2. Transformar para formato Style Dictionary

```bash
# Converter raw tokens para formato Style Dictionary
node scripts/transform-tokens.js \
  --input tokens/raw/tokens.json \
  --output tokens/transformed/ \
  --layers primitive,semantic,component
```

Estrutura de output esperada:
```
tokens/transformed/
├── primitive/
│   ├── color.json
│   ├── spacing.json
│   ├── typography.json
│   └── radius.json
├── semantic/
│   ├── color.json
│   ├── spacing.json
│   └── typography.json
└── component/
    ├── button.json
    ├── card.json
    └── input.json
```

### 3. Build com Style Dictionary

```bash
# Gerar outputs para todas as plataformas
npx style-dictionary build --config config.sd.json

# Ou por plataforma específica
npx style-dictionary build --platform web
npx style-dictionary build --platform ios
npx style-dictionary build --platform android
```

### 4. Validar output

```bash
# Verificar se todos os tokens foram gerados
node scripts/validate-token-output.js \
  --expected tokens/transformed/ \
  --generated dist/

# Verificar se não há tokens órfãos (definidos mas não usados)
node scripts/check-orphan-tokens.js --dir dist/

# Verificar se não há breaking changes não intencionais
node scripts/token-diff.js \
  --old dist-previous/ \
  --new dist/
```

### 5. Commit e PR

```bash
git add tokens/ dist/
git commit -m "chore(tokens): update from Figma [$(date +%Y-%m-%d)]"
git push origin design/tokens-update-$(date +%Y%m%d)
# Abrir PR para review
```

## Expected Output

```
dist/
├── web/
│   ├── tokens.css          # CSS custom properties
│   ├── tokens.scss         # SCSS variables
│   └── tokens.js           # JS module
├── ios/
│   └── Tokens.swift        # Swift constants
├── android/
│   └── tokens.xml          # Android resources
└── docs/
    └── token-reference.json # Para documentação
```

Exemplo de output CSS:
```css
:root {
  /* Primitive */
  --color-blue-500: #1A73E8;
  /* Semantic */
  --color-action-primary: var(--color-blue-500);
  /* Component */
  --button-color-bg-default: var(--color-action-primary);
}
```

## Automation Notes

- **CI/CD:** Este script roda automaticamente via GitHub Actions quando o branch
  `tokens/` recebe push (workflow: `.github/workflows/token-build.yml`)
- **Frequência:** On-demand (quando tokens mudam) + scheduled check semanal
- **Notificação:** Resultado postado no #design-system via Slack webhook
- **Rollback:** Se build falhar, último dist/ válido é preservado em dist-previous/
- **Monitoring:** Dashboard de token health em [link do dashboard]
