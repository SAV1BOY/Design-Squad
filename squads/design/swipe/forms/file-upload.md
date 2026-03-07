# File Upload Patterns

## Pattern Description

Padroes para upload de arquivos que tornam o processo intuitivo, com feedback claro de progresso e tratamento de erros.

## Examples

### Example 1: Dropbox — Drag and Drop Zone
Dropbox usa drop zone proeminente:
- Area grande com borda tracejada e icone
- Texto: "Arraste arquivos aqui ou clique para selecionar"
- Highlight visual quando arquivo e arrastado sobre a area
- Preview de arquivos selecionados com thumbnail
- Progress bar individual por arquivo

### Example 2: Figma — Paste and Drop
Figma aceita multiplos metodos de upload:
- Drag-and-drop diretamente no canvas
- Ctrl+V para colar imagem da area de transferencia
- Menu File > Import
- Processamento visual imediato no canvas
- Suporte a formatos multiplos (SVG, PNG, JPG, PDF)

### Example 3: Gmail — Inline Upload
Gmail integra upload naturalmente no fluxo de email:
- Drag-and-drop no corpo do email
- Botao de clip no toolbar
- Progress bar na parte inferior do compose
- Preview do anexo com tamanho e tipo
- Remove com click no X antes de enviar

## Analysis

File upload eficaz:
- **Multiplos metodos**: drag-and-drop + click + paste
- **Feedback**: progress bar com percentual e velocidade
- **Preview**: thumbnail ou icone de tipo para arquivos selecionados
- **Limites claros**: informe formatos aceitos e tamanho maximo antes do upload
- **Error handling**: mensagem especifica (arquivo grande, formato invalido)
- **Batch**: suporte a multiplos arquivos simultaneos

## Tags

`file-upload`, `drag-and-drop`, `progress`, `forms`, `media`
