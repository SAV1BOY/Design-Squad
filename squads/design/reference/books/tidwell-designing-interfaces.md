# Designing Interfaces — Jenifer Tidwell



## Metadata

- **Autora:** Jenifer Tidwell (coautores na 3a ed.: Charles Brewer, Aynne Valencia)
- **Publicacao:** 2005 (3a edicao: 2020)
- **Categoria:** UI Patterns, Interaction Design
- **Relevancia para o Squad:** Alta — catálogo de referência de UI patterns
- **Ultima revisao:** 2026-03-06



## Summary

Designing Interfaces é o catálogo mais completo de UI patterns disponível, organizado por problema de design em vez de componente visual. Tidwell identifica padrões recorrentes que resolvem problemas comuns de interface — desde organização de conteúdo e navegação até interações complexas como data visualization e social features.

A terceira edição (2020) adiciona cobertura substancial de mobile patterns, responsive design, conversational UI e design para acessibilidade. Cada pattern segue uma estrutura consistente: problema que resolve, quando usar, por que funciona (psicologia), e exemplos de implementação. O livro funciona como referência de consulta — não precisa ser lido linearmente.

O valor principal é a linguagem de padrões que cria: quando o squad fala "vamos usar um Module Tab pattern aqui" em vez de descrever o layout, a comunicação é precisa e eficiente. Tidwell conecta cada pattern à psicologia subjacente, explicando por que funciona, não apenas como implementar.



## Key Concepts


### 1. Pattern Language for UI

Patterns não são componentes — são soluções nomeadas para problemas recorrentes. "Card layout" é um pattern (resolve o problema de apresentar múltiplos itens heterogêneos de forma escaneável), não apenas um componente visual. A linguagem de patterns permite discutir soluções em nível mais alto que pixels.


### 2. Organization Patterns

Como estruturar conteúdo: Two-Panel Selector, Canvas Plus Palette, Wizard, Dashboard, Module Tabs, Accordion, Collapsible Panels. Cada pattern atende a diferentes necessidades de density (quanto conteúdo), frequency (com que frequência muda) e relationship (como itens se relacionam).


### 3. Navigation Patterns

Como o usuário se move: Clear Entry Points, Global Navigation, Hub and Spoke, Pyramid, Modal Panel, Breadcrumbs, Annotated Scrollbar. Tidwell explica quando navegação hierárquica funciona vs. navegação flat, e como combinar patterns para sistemas complexos.


### 4. Action and Input Patterns

Como o usuário age: Smart Menu Items, Action Panel, Prominent Done Button, Multi-Level Undo, Progress Indicator, Cancelability. Foco em tornar ações claras, reversíveis e fornecendo feedback adequado em cada estado.


### 5. Information Graphics Patterns

Como apresentar dados: Overview Plus Detail, Data Spotlight, Dynamic Queries, Data Brushing, Small Multiples, Treemap. Patterns para tornar dados complexos compreensíveis e exploráveis, conectando visualização à interação.



## Application to Design Squad

- **Pattern vocabulary:** Adotar a nomenclatura de Tidwell como linguagem compartilhada em design reviews. Referenciar patterns pelo nome em vez de descrever layouts.
- **Pattern library mapping:** Mapear os componentes do design system para os patterns de Tidwell. Cada componente deve ter pelo menos um pattern associado que explica quando e por que usá-lo.
- **Decision framework:** Quando enfrentar um problema de design comum, consultar o catálogo antes de projetar do zero. Isso acelera a ideação e evita reinvenção.
- **Pattern combinations:** Documentar combinações de patterns que funcionam bem no produto (ex: Dashboard + Card Layout + Data Spotlight) para reutilização em contextos similares.
- **Anti-pattern awareness:** Para cada pattern adotado, documentar também quando não usar. O contexto inadequado transforma um bom pattern em um problema.



## Key Takeaways

1. **Patterns são soluções para problemas, não componentes visuais.** Primeiro identifique o problema, depois encontre o pattern que o resolve.

2. **Uma linguagem de patterns compartilhada acelera comunicação.** "Vamos usar Hub and Spoke aqui" é mais eficiente que descrever o layout do zero.

3. **Consulte antes de inventar.** A maioria dos problemas de UI já foi resolvida. Variações contextuais são necessárias, reinvenção raramente é.

4. **Contexto determina o pattern correto.** O melhor pattern para navigation depende da profundidade do conteúdo, frequência de uso e modelo mental do usuário.

5. **Patterns se combinam.** Interfaces complexas usam múltiplos patterns em composição. Entender como patterns se complementam é tão importante quanto conhecer cada um isoladamente.



## Cross-References

- [About Face — Cooper](cooper-about-face.md) — interaction design patterns complementares
- [Dashboards and Tables Patterns](../ui-patterns/dashboards-and-tables-patterns.md) — padrões específicos de dashboard
- [Navigation Patterns](../ui-patterns/navigation-patterns.md) — detalhamento de padrões de navegação
- [Search and Filter Patterns](../ui-patterns/search-and-filter-patterns.md) — padrões de busca e filtragem
- [Modal and Overlay Patterns](../ui-patterns/modal-and-overlay-patterns.md) — padrões de sobreposição
