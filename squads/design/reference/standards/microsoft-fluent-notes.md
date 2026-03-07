# Microsoft Fluent Design System



## Metadata

- **Organizacao:** Microsoft
- **Versao:** Fluent 2 (2023+)
- **Categoria:** Design System, Enterprise UI
- **Relevancia para o Squad:** Media — referencia para design enterprise e produtividade
- **Ultima revisao:** 2026-03-06



## Summary

Fluent Design System e o sistema de design da Microsoft, usado em Windows, Microsoft 365, Teams, Azure e todo o ecossistema de produtividade. Fluent 2 e uma evolucao significativa que unifica a linguagem visual entre web, desktop e mobile, com foco em produtividade, acessibilidade e escalabilidade.

Como design system para ferramentas de produtividade enterprise, Fluent e particularmente relevante para equipes que projetam dashboards, ferramentas de colaboracao, interfaces de administracao e workflows complexos. A escala do ecossistema Microsoft (bilhoes de usuarios) significa que cada decisao de design e testada em diversidade extrema de casos de uso.

Fluent 2 introduziu design tokens consistentes, componentes acessiveis por default, theming avancado e suporte a high contrast mode. A biblioteca de componentes e open source (Fluent UI React, Fluent UI Web Components), servindo como referencia tecnica alem do design.



## Key Concepts


### 1. Design Principles (Accessible, Coherent, Familiar, Responsive, Empowering)

Accessible: AA minimum, designed for assistive tech. Coherent: visual e behavioral consistency cross-platform. Familiar: conventions que reduzem learning curve. Responsive: adapta a qualquer device e viewport. Empowering: tools that help users achieve goals, not show off technology.


### 2. Compound Components

Fluent usa "compound components" — componentes complexos compostos de partes menores intercambiaveis. Um DataGrid e composto de Header, Row, Cell, etc. Cada parte pode ser customizada independentemente. Esse modelo e ideal para enterprise UI onde customizacao e necessidade, nao luxo.


### 3. High Contrast and Forced Colors

Fluent suporta nativamente Windows High Contrast mode e forced-colors media query. Todo componente e testado em high contrast. Para design systems proprios, isso e referencia de como pensar acessibilidade alem de cores "padrao."


### 4. Density Modes (Comfortable, Compact)

Fluent oferece dois modos de densidade: comfortable (mais espaco, melhor para touch e novatos) e compact (menos espaco, mais informacao, para power users e desktop). O mesmo componente se adapta sem redesign — apenas muda spacing tokens.


### 5. Enterprise-Scale Patterns

Fluent documenta patterns especificos de enterprise: CommandBar, Ribbon, DataGrid, DetailsList, Panel, Dialog, MessageBar. Cada pattern e projetado para alta densidade de informacao, workflows complexos e uso repetitivo — necessidades de enterprise que consumer UI patterns nao atendem.



## Application to Design Squad

- **Enterprise pattern reference:** Para interfaces de dashboard, admin e configuracao, consultar Fluent como referencia. Patterns como DataGrid e CommandBar sao otimizados para produtividade.
- **Density options:** Considerar oferecer modos de densidade (comfortable/compact) para features de uso intensivo. Power users apreciam densidade; novatos apreciam espaco.
- **High contrast testing:** Incluir teste em high contrast mode no checklist de acessibilidade. Nao depender apenas de cores para comunicar informacao.
- **Compound component architecture:** Adotar modelo de compound components para componentes complexos — permite customizacao sem refactor.
- **Consistency cross-platform:** Para produtos multi-plataforma, usar Fluent como referencia de como manter coerencia visual sem forcar uniformidade.



## Key Takeaways

1. **Enterprise UI tem necessidades especificas.** Alta densidade, workflows complexos e uso repetitivo exigem patterns diferentes de consumer UI.

2. **Modos de densidade servem diferentes usuarios.** Oferecer comfortable e compact e melhor que escolher um para todos.

3. **High contrast e obrigatorio, nao opcional.** Usuarios com baixa visao dependem de high contrast mode — teste para ele.

4. **Compound components escalam melhor.** Componentes compostos de partes independentes permitem customizacao sem complexidade.

5. **Produtividade e o objetivo, nao beleza.** Em enterprise, o design deve tornar o trabalho mais eficiente. Estética serve a produtividade.



## Cross-References

- [Material Design Notes](material-design-notes.md) — comparacao de design systems
- [Carbon Design System](carbon-design-system-notes.md) — outro sistema enterprise
- [Enterprise Design Playbook](../industries/enterprise-design-playbook.md) — design para enterprise
- [Dashboards and Tables Patterns](../ui-patterns/dashboards-and-tables-patterns.md) — patterns de data density
- [WCAG 2.x Notes](wcag-2-x-notes.md) — acessibilidade
