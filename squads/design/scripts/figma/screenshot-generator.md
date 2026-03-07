# Screenshot Generator

## Title
Script de geração automatizada de screenshots de componentes e telas do Figma.

## Purpose

Gerar screenshots automatizadas de todos os componentes do design system e telas
de handoff para uso em documentação, Storybook, changelogs e comparação visual.
Elimina o trabalho manual de exportar imagens do Figma para cada atualização.

## Prerequisites

- **Node.js** >= 18.0
- **Figma API token** com acesso de leitura
- **Sharp** (processamento de imagem) — `npm install sharp`
- **Diretório de output** com espaço suficiente (estimativa: 500MB para DS completo)

Variáveis de ambiente:
```bash
export FIGMA_API_TOKEN="figd_xxxxxxxxxxxxx"
export FIGMA_FILE_ID="xxxxxxxxxxxxx"
export SCREENSHOTS_DIR="/path/to/screenshots"
```

## Steps

### 1. Listar frames para captura

```bash
# Gerar lista de frames a capturar (componentes + telas de handoff)
node scripts/figma-list-frames.js \
  --file-id $FIGMA_FILE_ID \
  --filter "type:COMPONENT,COMPONENT_SET,FRAME" \
  --exclude "Archive,Sandbox,_deprecated" \
  --output screenshots/manifest.json

# Output: lista de node IDs com metadata
```

### 2. Gerar screenshots via Figma API

```bash
# Exportar imagens via Figma Image API
node scripts/figma-export-images.js \
  --manifest screenshots/manifest.json \
  --format png \
  --scale 2 \
  --output $SCREENSHOTS_DIR/raw/

# Para SVG (ícones):
node scripts/figma-export-images.js \
  --manifest screenshots/manifest-icons.json \
  --format svg \
  --output $SCREENSHOTS_DIR/icons/
```

### 3. Processar imagens

```bash
# Otimizar e gerar thumbnails
node scripts/process-screenshots.js \
  --input $SCREENSHOTS_DIR/raw/ \
  --output $SCREENSHOTS_DIR/processed/ \
  --sizes "full,thumbnail:200x200,card:400x300" \
  --quality 90 \
  --format webp,png
```

### 4. Gerar comparação visual (antes/depois)

```bash
# Comparar com screenshots anteriores para identificar mudanças visuais
node scripts/visual-diff.js \
  --old $SCREENSHOTS_DIR/previous/ \
  --new $SCREENSHOTS_DIR/processed/ \
  --threshold 0.1 \
  --output $SCREENSHOTS_DIR/diffs/

# Output: imagens diff + relatório de mudanças
```

### 5. Publicar

```bash
# Upload para CDN/storage
node scripts/publish-screenshots.js \
  --input $SCREENSHOTS_DIR/processed/ \
  --destination $SCREENSHOTS_CDN_BUCKET \
  --prefix "ds/v$(node -p "require('./package.json').version")/"

# Atualizar referências na documentação
node scripts/update-doc-image-refs.js \
  --docs-dir docs/ \
  --cdn-base $SCREENSHOTS_CDN_URL
```

## Expected Output

```
screenshots/
├── raw/              # Exports diretos do Figma (2x)
├── processed/
│   ├── full/         # Tamanho original otimizado
│   ├── thumbnail/    # 200x200 para listas
│   └── card/         # 400x300 para cards de doc
├── icons/            # SVGs dos ícones
├── diffs/            # Comparação visual com versão anterior
│   ├── changed/      # Componentes que mudaram
│   └── report.md     # Relatório de mudanças
├── previous/         # Última versão (para comparação)
└── manifest.json     # Lista de tudo que foi capturado
```

Relatório de mudanças:
```
# Visual Changes — [Data]

## Changed (12 components)
- Button/Primary — border-radius mudou de 4px para 8px
- Card/Product — shadow atualizada
- Input/Text — focus ring color mudou

## New (3 components)
- Badge/Status
- Toast/Success
- Skeleton/Card

## Removed (1 component)
- Alert/Inline (deprecated)

## Unchanged (140 components)
```

## Automation Notes

- **Frequência:** A cada release do DS + on-demand para handoffs
- **CI/CD:** Triggered por tag de release no repositório do DS
- **Rate limiting:** Figma API tem limite de 30 req/min — script inclui throttling
- **Cache:** Screenshots são cacheadas por node_id + last_modified
- **Storage:** CDN com cache de 1 ano + cache busting por versão
- **Cleanup:** Screenshots de versões > 6 meses são archivadas automaticamente
