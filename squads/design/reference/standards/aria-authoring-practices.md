# ARIA Authoring Practices Guide (APG)



## Metadata

- **Organizacao:** W3C (Web Accessibility Initiative)
- **Versao:** APG 1.2 (continuamente atualizado)
- **Categoria:** Accessibility, Interaction Patterns
- **Relevancia para o Squad:** Alta — padrao de implementacao de acessibilidade em componentes
- **Ultima revisao:** 2026-03-06



## Summary

O ARIA Authoring Practices Guide (APG) e o guia oficial da W3C para implementar WAI-ARIA (Accessible Rich Internet Applications) em componentes de interface. Enquanto WCAG define o que deve ser acessivel, o APG define como — com padroes de interacao por teclado, roles, states e properties para cada tipo de componente.

O APG fornece design patterns detalhados para componentes comuns: accordion, alert, breadcrumb, carousel, combobox, dialog (modal), disclosure, listbox, menu, radio group, slider, switch, tabs, toolbar, tooltip, treeview. Cada pattern especifica o comportamento esperado de teclado, os ARIA roles e properties necessarios, e exemplos de implementacao.

Para designers, o APG e essencial porque define como componentes devem se comportar para usuarios de screen readers e navegacao por teclado. Se o designer especifica um componente que diverge do APG, a implementacao acessivel se torna exponencialmente mais complexa.



## Key Concepts


### 1. ARIA Roles, States and Properties

Roles definem o que um elemento e (button, dialog, navigation, alert). States comunicam condicoes atuais (aria-expanded, aria-selected, aria-checked). Properties definem caracteristicas (aria-label, aria-describedby, aria-required). ARIA complementa HTML semantico — nao substitui.


### 2. Keyboard Interaction Patterns

Cada componente tem padrao de teclado esperado: Tab move entre componentes, Arrow keys navegam dentro de componentes, Enter/Space ativam, Escape fecha. O APG documenta o padrao exato para cada tipo de componente — seguir esses padroes garante que usuarios de teclado sabem como interagir.


### 3. Focus Management

Componentes complexos (modals, menus, trees) precisam de focus management explicito: onde o focus vai quando o componente abre? Como o focus e capturado dentro do componente? Para onde retorna quando fecha? O APG define o comportamento esperado para cada caso.


### 4. Live Regions for Dynamic Content

Quando conteudo muda dinamicamente (notifications, counters, status updates), aria-live regions anunciam a mudanca para screen readers. aria-live="polite" (anuncia quando conveniente) e aria-live="assertive" (anuncia imediatamente) cobrem a maioria dos casos.


### 5. First Rule of ARIA: Don't Use ARIA

Se um elemento HTML nativo faz o que voce precisa, use-o em vez de ARIA. button e melhor que div role="button". input type="checkbox" e melhor que div role="checkbox". HTML semantico tem acessibilidade built-in; ARIA e para quando nao existe elemento nativo equivalente.



## Application to Design Squad

- **Keyboard spec em componentes:** Todo componente no design system deve ter especificacao de comportamento de teclado documentada, seguindo os patterns do APG.
- **Focus order em specs:** Em todo fluxo com componentes complexos (modals, menus, accordions), especificar a ordem de focus e o comportamento de focus trap/return.
- **Component mapping ao APG:** Mapear cada componente do design system ao pattern correspondente no APG. Usar como referencia de comportamento esperado.
- **Dynamic content annotation:** Em designs com conteudo dinamico (notifications, form validation, counters), anotar qual aria-live region usar e a prioridade (polite/assertive).
- **HTML-first approach:** Ao projetar componentes, preferir semantica HTML nativa. Usar ARIA apenas quando o comportamento desejado nao tem equivalente em HTML.



## Key Takeaways

1. **O APG define como componentes devem se comportar acessivelmente.** E o contrato entre design e implementacao acessivel.

2. **Keyboard interaction patterns sao padronizados.** Tab entre componentes, arrows dentro, Enter/Space para ativar, Escape para fechar. Nao invente.

3. **Focus management e responsabilidade do design.** Para onde o focus vai, como e capturado, para onde retorna — tudo deve ser especificado no design.

4. **HTML semantico primeiro, ARIA quando necessario.** Elementos nativos tem acessibilidade built-in. ARIA e complemento, nao substituto.

5. **Live regions comunicam mudancas dinamicas.** Sem aria-live, usuarios de screen reader nao sabem que algo mudou na tela.



## Cross-References

- [WCAG 2.x Notes](wcag-2-x-notes.md) — criterios que o APG ajuda a atender
- [Accessibility Tools](../tools/accessibility-tools.md) — ferramentas de teste
- [Modal and Overlay Patterns](../ui-patterns/modal-and-overlay-patterns.md) — focus management em modals
- [Navigation Patterns](../ui-patterns/navigation-patterns.md) — keyboard navigation
- [Storybook for Design Systems](../tools/storybook-for-design-systems.md) — testes de acessibilidade integrados
