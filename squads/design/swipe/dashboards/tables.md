# Dashboard Table Patterns

## Pattern Description

Padroes para tabelas de dados em dashboards. Tabelas sao o componente mais usado para exibir dados tabulares — eficiencia de escaneamento e interatividade sao essenciais.

## Examples

### Example 1: Airtable — Spreadsheet-Like Table
Airtable combina tabela com funcionalidade de planilha:
- Inline editing com click ou double-click
- Tipos de celula ricos (select, date, attachment, link)
- Resize de colunas com drag
- Freeze de colunas (pin left)
- Sort e filter por coluna com UI intuitiva

### Example 2: Linear — Minimal Data Table
Linear usa tabelas minimalistas para issues:
- Colunas priorizadas: ID, Title, Status, Assignee, Priority
- Row hover revela acoes rapidas
- Bulk selection com checkboxes
- Keyboard navigation entre rows
- Densidade compacta para maximizar dados visiveis

### Example 3: Notion — Database Table View
Notion oferece tabelas como view de database:
- Propriedades configuráveis como colunas
- Sort, filter e group by integrados
- Toggle entre views (Table, Board, Calendar, Gallery)
- Formula columns para dados calculados
- Linked databases para relacoes entre tabelas

## Analysis

Tabelas de dashboard eficazes:
- **Density**: ofereça modos compact/comfortable
- **Sort**: click no header para sort, indicador visual de direcao
- **Pagination vs. Infinite scroll**: pagination para dados grandes, scroll para listas curtas
- **Responsive**: priorize colunas em mobile, collapse secundarias
- **Performance**: virtualize rows para 1000+ itens
- **Bulk actions**: toolbar contextual apos selecao

## Tags

`tables`, `data-display`, `dashboard`, `sort`, `filter`, `inline-editing`
