# Dashboards and Tables Patterns



## Metadata

- **Categoria:** UI Patterns, Data Display, Enterprise UI
- **Relevancia para o Squad:** Alta — padroes para interfaces data-intensive
- **Ultima revisao:** 2026-03-06



## Summary

Dashboards e tabelas sao os padroes mais complexos de UI — combinam data visualization, interacao, filtragem, paginacao e responsiveness em interfaces de alta densidade informacional. Este documento cobre padroes para projetar dashboards eficazes e tabelas usaveis em escala.





## Key Concepts


### 1. Dashboard Layout Patterns

KPI cards no topo (metricas headline), graficos no meio (tendencias e comparacoes), tabela detalhada na base (drill-down). Layout em grid de 12 colunas com cards de 4, 6 ou 12 colunas. Prioridade: informacao mais acionavel no topo-esquerda.


### 2. Data Table Patterns

Sorting (click no header), filtering (inline ou panel), pagination vs. infinite scroll vs. virtual scroll, row actions (inline buttons ou kebab menu), row selection (checkboxes), column resizing e reordering. Para tabelas com muitas colunas: horizontal scroll com coluna fixa.


### 3. Empty, Loading and Error States

Dashboard vazio: skeleton screens ou placeholder com instrucao de como popular. Loading: skeleton shimmer por card/secao, nao spinner global. Error: mensagem especifica por widget, com retry, nao falha global. Cada widget carrega independentemente.


### 4. Filtering and Date Range

Filter bar persistente (top ou lateral) com filtros aplicaveis a todos os widgets. Date range picker e o filtro mais comum em dashboards. Presets uteis: Today, Last 7 days, Last 30 days, Custom. Filtros aplicados devem ser visiveis e removiveis (chips).


### 5. Responsive Dashboard

Em mobile: cards KPI empilhados, graficos full-width simplificados, tabela substituida por cards ou lista. Nao tente comprimir desktop dashboard em mobile — redesenhe priorizando as metricas mais acionaveis.



## Application to Design Squad

- **Dashboard template no design system:** Criar template de dashboard com grid, KPI cards, chart containers e data table. Reutilizar para todos os dashboards do produto.
- **Loading strategy por widget:** Implementar loading independente por widget (skeleton shimmer), nao loading global. Permite que partes do dashboard sejam usaveis enquanto outras carregam.
- **Filter persistence:** Filtros aplicados devem persistir entre sessoes (saved in user preferences). O usuario nao deve re-filtrar a cada acesso.
- **Mobile-first dashboard:** Para dashboards responsivos, projetar mobile first — selecionar as 3-5 metricas mais criticas para mobile, expandir para desktop.
- **Data table component robusto:** Investir em componente de data table no design system com sorting, filtering, pagination, selection e responsive. E o componente mais reutilizado em enterprise.



## Key Takeaways

1. **Informacao acionavel primeiro.** KPIs e tendencias no topo; detalhes sob demanda.

2. **Loading independente por widget.** O dashboard nao e monoblock — cada widget carrega e falha independentemente.

3. **Filtros persistentes e removiveis.** Filtros devem sobreviver entre sessoes e ser visivelmente removiveis.

4. **Mobile dashboard e redesign, nao compressao.** Selecione metricas, nao comprima layout.

5. **Data table e investimento de longo prazo.** Um componente de tabela robusto serve dezenas de contextos no produto.



## Cross-References

- [Visual Display of Information — Tufte](../books/tufte-visual-display-of-information.md) — data visualization
- [Truthful Art — Cairo](../books/cairo-truthful-art.md) — escolha de graficos
- [Search and Filter Patterns](search-and-filter-patterns.md) — filtragem
- [Enterprise Design Playbook](../industries/enterprise-design-playbook.md) — dashboards enterprise
- [Microsoft Fluent Notes](../standards/microsoft-fluent-notes.md) — DataGrid pattern
