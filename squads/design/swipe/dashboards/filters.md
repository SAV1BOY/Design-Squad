# Dashboard Filter Patterns

## Pattern Description

Padroes de filtragem para dashboards que permitem usuarios refinar dados exibidos. Filtros eficazes equilibram poder de segmentacao com simplicidade de interface.

## Examples

### Example 1: Google Analytics — Filter Bar
GA4 usa barra de filtros superior:
- Date range picker como filtro primario
- Segmentos de usuario como filtro secundario
- Comparacao de periodos toggle
- Filtros aplicados afetam todos os widgets simultaneamente
- Salvamento de combinacoes de filtro como "views"

### Example 2: Shopify — Faceted Filters
Shopify Admin filtra pedidos com facetas:
- Status, Payment status, Fulfillment status
- Date range, Channel, Location
- Chips de filtro ativo removiveis
- Contagem de resultados atualizada em tempo real
- Saved filters para combinacoes frequentes

### Example 3: Jira — JQL + Visual Filters
Jira combina filtros visuais com linguagem de query:
- Quick filters: botoes toggle no topo do board
- Filter bar: dropdowns para assignee, type, priority
- Advanced: JQL query builder para power users
- Switch entre visual e JQL modes

## Analysis

Filtros de dashboard eficazes:
- **Progressive disclosure**: filtros comuns visiveis, avancados escondidos
- **Feedback imediato**: atualize dados conforme filtros mudam
- **State visible**: mostre filtros ativos como chips removiveis
- **Reset facil**: botao "Limpar todos os filtros"
- **URL sync**: filtros refletidos na URL para compartilhamento
- **Saved views**: salvar combinacoes de filtro para reutilizacao

## Tags

`filters`, `dashboard`, `faceted-search`, `date-picker`, `saved-views`
