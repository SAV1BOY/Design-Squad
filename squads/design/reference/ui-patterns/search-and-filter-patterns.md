# Search and Filter Patterns



## Metadata

- **Categoria:** UI Patterns, Findability, Navigation
- **Relevancia para o Squad:** Alta — busca e filtragem sao operacoes core
- **Ultima revisao:** 2026-03-06



## Summary

Patterns de busca e filtragem permitem que usuarios encontrem o que precisam em conjuntos de dados grandes ou complexos. Busca e acao ativa do usuario (digita query); filtragem e refinamento de resultados (seleciona criterios). Ambos sao complementares e frequentemente combinados.



## Key Concepts


### 1. Search Input Patterns

Global search (busca no produto inteiro), scoped search (busca dentro de secao), inline search/filter (busca dentro de lista/tabela). Autocomplete com sugestoes reduz esforco e erros. Recent searches e saved searches para power users.


### 2. Filter Patterns

Filter sidebar (lateral, persistente), filter bar (horizontal, chips), filter modal (mobile-optimized), faceted filters (multiplas dimensoes simultaneas). Filtros aplicados devem ser visiveis como chips removiveis. "Clear all" para reset rapido.


### 3. Results Display

List view vs. grid view (toggle). Sorting options (relevance, date, price, name). Results count ("42 resultados"). Highlight de search terms nos resultados. Paginacao ou infinite scroll baseado no contexto.


### 4. Zero Results and Empty States

Zero results nao e beco sem saida — oferecer: sugestoes de busca, filtros para remover, categorias populares, contato com suporte. Nunca so "nenhum resultado encontrado" — sempre oferecer caminho adiante.


### 5. Saved Searches and Alerts

Para power users: salvar buscas frequentes, criar alertas para novos resultados que matchem criterios. Pattern comum em marketplaces e ecommerce. Aumenta retencao e conveniencia.



## Application to Design Squad

- **Search component no design system:** Criar componente de search input com autocomplete, recent searches e clear. Reutilizavel em todos os contextos de busca.
- **Filter chips padronizados:** Padronizar representacao visual de filtros aplicados como chips removiveis. Consistencia em todo o produto.
- **Zero results strategy:** Todo contexto de busca/filtragem deve ter zero results state projetado com caminhos alternativos.
- **Performance perception:** Para buscas que podem ser lentas, usar skeleton results ou progressive loading. Nao bloquear a interface.
- **Mobile filter pattern:** Em mobile, usar filter modal (full-screen ou bottom sheet) em vez de sidebar. Aplicar filtros com botao explicito.



## Key Takeaways

1. **Busca e filtragem sao complementares.** Oferecer ambas para diferentes estilos de usuario.

2. **Filtros aplicados devem ser visiveis e removiveis.** Chips sao o padrao de industria.

3. **Zero results e oportunidade, nao beco sem saida.** Sempre oferecer caminhos alternativos.

4. **Autocomplete reduz esforco significativamente.** Sugestoes de busca aceleram e guiam o usuario.

5. **Mobile tem padroes proprios.** Sidebar de filtros nao funciona em mobile — use modal ou bottom sheet.



## Cross-References

- [Information Architecture — Rosenfeld](../books/rosenfeld-information-architecture.md) — findability
- [Dashboards and Tables Patterns](dashboards-and-tables-patterns.md) — filtragem em tabelas
- [Navigation Patterns](navigation-patterns.md) — busca como navegacao
- [Designing Interfaces — Tidwell](../books/tidwell-designing-interfaces.md) — dynamic queries
- [Ecommerce Design Playbook](../industries/ecommerce-design-playbook.md) — busca em ecommerce
