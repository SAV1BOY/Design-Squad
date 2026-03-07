# Side Navigation Patterns

## Pattern Description

Padroes de navegacao lateral (sidebar) para aplicacoes com muitas secoes. Side nav fornece orientacao persistente e acesso rapido a areas principais do produto.

## Examples

### Example 1: Linear — Collapsible Side Nav
Linear implementa side nav colapsavel:
- Icone + label no estado expandido
- Apenas icone no estado colapsado
- Secoes agrupadas: Inbox, My Issues, Projects, Teams
- Favoritos fixados no topo
- Drag-and-drop para reorganizar

### Example 2: Notion — Tree Navigation
Notion usa tree view hierarquica como side nav:
- Paginas aninhadas com indentacao visual
- Expand/collapse de secoes
- Quick search integrado no topo
- Drag-and-drop para mover paginas
- Hover revela acoes (adicionar subpagina, mais opcoes)

### Example 3: Figma — Layers Panel
Figma usa panel lateral para navegacao de layers:
- Estrutura em arvore espelhando o canvas
- Selecao sincronizada (click no layer = seleciona no canvas)
- Multi-selecao com Ctrl/Cmd + click
- Rename inline com double-click
- Drag para reordenar layers

## Analysis

Side nav eficaz:
- Colapsavel para maximizar area de conteudo
- Grupos logicos com headers de secao
- Estado ativo claro (highlight, indicator)
- Responsive: off-canvas overlay em mobile
- Keyboard navigable com Arrow Up/Down
- Persistente entre paginas (nao recarrega)

## Tags

`side-nav`, `sidebar`, `navigation`, `tree-view`, `responsive`, `collapsible`
