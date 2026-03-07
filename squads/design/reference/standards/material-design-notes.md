# Material Design — Google



## Metadata

- **Organizacao:** Google
- **Versao atual:** Material Design 3 (Material You, 2021+)
- **Categoria:** Design System, UI Guidelines
- **Relevancia para o Squad:** Media — referencia de design system maduro e abrangente
- **Ultima revisao:** 2026-03-06



## Summary

Material Design e o sistema de design do Google, usado em Android, Google Workspace e produtos Google em geral. Originado em 2014 como linguagem visual baseada em metafora de material fisico (paper, ink, shadow), evoluiu para Material Design 3 (Material You) com foco em personalizacao, dynamic color e expressividade.

Como sistema de design, Material e uma das referencias mais completas existentes — cobrindo componentes, tokens, patterns de interacao, motion, tipografia, cor, iconografia e acessibilidade. O valor para designers que nao trabalham com Android e como referencia de decisoes de design system bem documentadas e a logica por tras de cada decisao.

Material Design 3 introduziu dynamic color (cores extraidas do wallpaper do usuario), design tokens como camada de abstracao, e maior flexibilidade para personalizacao de marca — respondendo a critica de que Material 1 e 2 tornavam todos os apps indistinguiveis.



## Key Concepts


### 1. Design Tokens Architecture

Material 3 usa tres niveis de tokens: reference tokens (paleta completa — md.ref.palette.primary40), system tokens (decisoes semanticas — md.sys.color.primary), component tokens (aplicacao especifica — md.comp.filled-button.container.color). Essa arquitetura permite theming sem alterar componentes.


### 2. Dynamic Color and Theming

Material You introduziu dynamic color — cores da interface derivadas automaticamente do wallpaper ou imagem de marca do usuario. O sistema garante acessibilidade (contraste) e harmonia independente da cor de origem. Para design systems proprios, o principio de palette generation algoritmica e aplicavel.


### 3. Motion System

Material define motion com principios: informative (transicoes comunicam relacao entre telas), focused (atencao direcionada ao que mudou), expressive (personalidade da marca). O sistema inclui easing curves, duration scales e transition patterns padronizados.


### 4. Component Specifications

Cada componente tem spec detalhada: anatomy (partes constituintes), states (enabled, hovered, focused, pressed, disabled), behavior (interacao e resposta), accessibility (roles, keyboard), theming (quais tokens customizar). Essa profundidade de spec e modelo para qualquer design system.


### 5. Responsive Layout Grid

Sistema de grid responsivo baseado em columns (4 mobile, 8 tablet, 12 desktop), margins e gutters. Material define breakpoints e como componentes se adaptam a cada range. O grid e complementado por layout patterns (feed, hero, supporting pane).



## Application to Design Squad

- **Referencia de spec quality:** Usar Material como benchmark de qualidade de documentacao de componentes. Cada componente no design system deve ter anatomy, states, behavior e theming documentados.
- **Token architecture inspiration:** Adotar o modelo de tres niveis de tokens (reference, system, component) como base para o design system proprio.
- **Motion guidelines:** Se o design system nao tem motion system, usar o Material como ponto de partida para definir easing curves, durations e transition patterns.
- **Layout grid adoption:** Se nao existe grid system formal, usar o Material como referencia para definir columns, margins e breakpoints.
- **Accessibility patterns:** Referenciar Material para estados de componentes (hover, focus, pressed, disabled) — sao bem documentados e testados em escala.



## Key Takeaways

1. **Tres niveis de tokens permitem theming sem alterar componentes.** Reference > System > Component e um modelo comprovado.

2. **Specs de componentes devem cobrir anatomy, states, behavior e accessibility.** Material e o benchmark de completude.

3. **Motion e sistema, nao decoracao.** Transicoes consistentes comunicam relacoes e guiam atencao.

4. **Design systems devem evoluir.** Material 1 > 2 > 3 demonstra que rigidez mata — flexibilidade planejada mantém relevancia.

5. **Personalizacao nao sacrifica consistencia.** Dynamic color prova que e possivel oferecer customizacao mantendo acessibilidade e harmonia.



## Cross-References

- [Apple Human Interface Guidelines](apple-human-interface-guidelines.md) — design system alternativo
- [Design Tokens Standard](design-tokens-standard-notes.md) — padrao de tokens complementar
- [Carbon Design System](carbon-design-system-notes.md) — design system enterprise comparavel
- [Figma Library Governance](../tools/figma-library-governance.md) — implementacao de libraries
- [Atomic Design — Frost](../books/frost-atomic-design.md) — composicao de componentes
