# Carbon Design System — IBM



## Metadata

- **Organizacao:** IBM
- **Versao:** Carbon v11 (2022+)
- **Categoria:** Design System, Enterprise UI
- **Relevancia para o Squad:** Media — referencia para design system enterprise open source
- **Ultima revisao:** 2026-03-06



## Summary

Carbon e o design system open source da IBM, usado em produtos como IBM Cloud, Watson e todo o ecossistema IBM. Como design system enterprise, Carbon e projetado para interfaces complexas, data-intensive e de uso profissional — um contexto mais proximo de ferramentas B2B/SaaS do que consumer apps.

Carbon e particularmente forte em: grid system (2x grid baseado em miniunit de 8px), design tokens bem documentados, padroes de data visualization (integrados via Carbon Charts), acessibilidade rigorosa (IBM tem um dos programas de acessibilidade mais maduros da industria) e governanca de contribuicao open source.

A abordagem open source do Carbon significa que designers e developers podem inspecionar decisoes de design no nivel mais granular — cada componente tem rationale documentado, tokens expostos e codigo auditavel. Isso o torna referencia de aprendizado alem de referencia de design.



## Key Concepts


### 1. 2x Grid System

Carbon usa um grid baseado em unidade de 8px (miniunit) com sistema de 16 columns. O "2x" refere-se ao uso de multiplos de 2 miniunit (16px) como unidade base de espacamento. Isso cria ritmo vertical e horizontal consistente em toda a interface. Margins, gutters e component spacing seguem a escala.


### 2. Design Tokens and Theming

Carbon define quatro temas (White, Gray 10, Gray 90, Gray 100) atraves de token layers. Componentes sao construidos com tokens, nao com valores diretos. Trocar de tema e trocar de layer de tokens. O sistema suporta temas custom para white-labeling.


### 3. Data Visualization (Carbon Charts)

Carbon inclui biblioteca dedicada de data visualization com bar charts, line charts, area charts, scatter plots, meter charts, gauges e mais. Cada chart type segue design tokens do sistema, garantindo consistencia visual entre componentes de UI e graficos.


### 4. Accessibility Program

IBM Accessibility Requirements (baseados em WCAG 2.1 AA + extensoes IBM) sao integrados ao processo de design e desenvolvimento de cada componente. Carbon inclui: ARIA roles e patterns corretos, keyboard interaction, high contrast support, screen reader testing e automated accessibility testing.


### 5. Open Source Governance

Carbon opera como projeto open source com processo claro de contribuicao: RFC (Request for Comments) para mudancas significativas, design reviews publicos, semver para releases, migration guides para breaking changes. O modelo e referencia para governanca de design system em qualquer organizacao.



## Application to Design Squad

- **Grid reference:** Adotar sistema de grid baseado em 8px como Carbon. O ritmo de 8px e amplamente adotado e facilita alinhamento entre design e desenvolvimento.
- **Data viz components:** Para interfaces data-intensive, referenciar Carbon Charts como benchmark de design de graficos integrados ao design system.
- **Theming architecture:** Usar o modelo de token layers de Carbon como referencia para implementar theming (light/dark, multi-brand).
- **Accessibility integration:** Seguir o modelo de Carbon de integrar acessibilidade no processo de criacao de componentes, nao como auditoria posterior.
- **Open governance model:** Adotar elementos do modelo de governanca open source de Carbon: RFCs para mudancas significativas, reviews publicos, migration guides.



## Key Takeaways

1. **8px grid cria ritmo consistente.** Multiplos de 8px para todo espacamento e sizing e convencao de industria com boas razoes.

2. **Data visualization e parte do design system.** Graficos sao componentes de UI e devem seguir os mesmos tokens e patterns.

3. **Acessibilidade integrada e mais barata que retrofitada.** Carbon prova que acessibilidade desde o design e viavel em escala enterprise.

4. **Token layers permitem theming elegante.** Trocar de tema sem alterar componentes e possivel com boa arquitetura de tokens.

5. **Open source e modelo de governanca, nao apenas licenca.** O processo de contribuicao e evolucao e tao valioso quanto o codigo.



## Cross-References

- [Material Design Notes](material-design-notes.md) — comparacao de design systems
- [Microsoft Fluent Notes](microsoft-fluent-notes.md) — outro sistema enterprise
- [Design Tokens Standard](design-tokens-standard-notes.md) — padrao de tokens
- [Enterprise Design Playbook](../industries/enterprise-design-playbook.md) — contexto enterprise
- [Dashboards and Tables Patterns](../ui-patterns/dashboards-and-tables-patterns.md) — patterns de dados
