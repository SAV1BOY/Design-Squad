# Modal and Overlay Patterns



## Metadata

- **Categoria:** UI Patterns, Interaction Design
- **Relevancia para o Squad:** Media-Alta — padroes de sobreposicao e interrupcao
- **Ultima revisao:** 2026-03-06



## Summary

Modals, dialogs, drawers, bottom sheets e popovers sao overlays que sobrepoem conteudo sobre a interface principal. Sao ferramentas poderosas para foco e confirmacao, mas perigosas quando usadas excessivamente — cada overlay interrompe o fluxo e exige atencao.





## Key Concepts


### 1. Modal Dialog (Blocking)

Overlay centralizado que bloqueia interacao com o fundo. Para: confirmacoes criticas, acoes destrutivas, formularios curtos que requerem foco. Anti-pattern: modals com conteudo longo, modals dentro de modals, modal para qualquer acao. Focus trap obrigatorio (teclado preso dentro do modal).


### 2. Non-Modal Dialog / Drawer

Panel lateral (drawer) ou dialog que nao bloqueia o fundo. O usuario pode interagir com o conteudo atras. Ideal para: paineis de detalhes, edição contextual, filtros avancados. Drawer: lateral, full-height. Dialog nao-modal: flutuante, posicionavel.


### 3. Bottom Sheet (Mobile)

Overlay que sobe da parte inferior da tela em mobile. Pode ser: half-sheet (cobre metade da tela), full-sheet (quase toda a tela), peek (mostra preview, puxar para expandir). Ideal para: acoes contextuais, filtros, detalhes em mobile. Gesture-friendly (swipe down to dismiss).


### 4. Popover and Tooltip

Popover: pequeno overlay conectado a um trigger element, com conteudo interativo (botoes, links). Tooltip: overlay minimo com texto explicativo, nao interativo, aparece no hover/focus. Ambos devem ter posicao inteligente (nao ultrapassar viewport).


### 5. Accessibility Requirements

Focus management: focus vai para o overlay ao abrir, e capturado dentro (trap), retorna ao trigger ao fechar. Escape fecha o overlay. Screen reader: role="dialog", aria-modal="true", aria-labelledby para titulo. Overlay com backdrop: click no backdrop fecha (opcional mas convencional).



## Application to Design Squad

- **Modal decision tree:** Antes de usar modal, perguntar: isso requer foco exclusivo? E curto (<3 campos)? Nao pode ser inline? Se nao a todas, use alternativa (drawer, inline expansion, nova pagina).
- **Overlay components no design system:** Documentar variantes de overlay com: trigger, tamanho, dismissal (escape, click outside, botao), focus management, ARIA attributes.
- **Mobile bottom sheet:** Em mobile, preferir bottom sheet sobre modal centralizado. Mais natural para thumb reach e gesture dismissal.
- **No nested overlays:** Regra: nunca overlay dentro de overlay. Se o conteudo e complexo demais para um overlay, use pagina dedicada.
- **Consistent dismissal:** Todos os overlays devem ser dismissiveis por: botao X, Escape key, click/tap no backdrop. Consistencia reduz aprendizado.



## Key Takeaways

1. **Modals sao interrupcao — use com moderacao.** Cada modal tira o usuario do fluxo. Reserve para acoes que requerem foco exclusivo.

2. **Drawer > modal para conteudo extenso.** Drawers permitem referencia ao conteudo atras; modals bloqueiam tudo.

3. **Bottom sheet e o modal do mobile.** Mais natural, mais acessivel ao polegar, mais gesture-friendly.

4. **Focus management e obrigatorio, nao opcional.** Sem focus trap, overlays sao inacessiveis por teclado e screen reader.

5. **Nunca modal dentro de modal.** Se precisa de segundo nivel, a complexidade exige pagina dedicada.



## Cross-References

- [ARIA Authoring Practices](../standards/aria-authoring-practices.md) — dialog pattern e focus management
- [Cognitive Load Theory](../psychology/cognitive-load-theory.md) — por que modals aumentam carga
- [Designing Interfaces — Tidwell](../books/tidwell-designing-interfaces.md) — modal panel pattern
- [Apple HIG](../standards/apple-human-interface-guidelines.md) — sheets e popovers em iOS
- [Material Design Notes](../standards/material-design-notes.md) — dialog e bottom sheet specs
