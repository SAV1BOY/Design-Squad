# A11Y Keyboard and Focus

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Accessibility                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Accessibility Lead             |

## Objective

Verificar se todos os elementos interativos do produto sao operaveis exclusivamente
via teclado, com ordem de foco logica e indicador de foco visivel. Acessibilidade
via teclado e fundamental para usuarios de tecnologias assistivas, usuarios com
deficiencia motora e power users.

## When to Apply

- Em testes de acessibilidade de novos componentes ou fluxos.
- Em auditorias trimestrais de acessibilidade.
- Quando componentes customizados (dropdowns, modais, tabs) sao implementados.
- Ao receber feedback de usuarios que dependem de teclado.

## Criteria

- [ ] Todos os elementos interativos sao alcancaveis via Tab e Shift+Tab.
- [ ] A ordem de tabulacao segue a ordem visual logica da pagina (DOM order).
- [ ] Focus ring e visivel em todos os elementos interativos com contraste adequado.
- [ ] Focus ring nao e removido via CSS (outline: none sem alternativa).
- [ ] Modais capturam o foco (focus trap) e retornam ao trigger ao fechar.
- [ ] Tecla Escape fecha modais, dropdowns, tooltips e overlays.
- [ ] Menus e dropdowns suportam navegacao com setas (arrow keys).
- [ ] Skip links permitem pular diretamente para o conteudo principal.
- [ ] Nenhum elemento cria armadilha de foco (keyboard trap) sem saida.
- [ ] Tab panels e accordions seguem WAI-ARIA keyboard interaction patterns.
- [ ] Drag and drop possui alternativa via teclado.
- [ ] Custom scrollable areas sao acessiveis via teclado.
- [ ] O foco nao se move inesperadamente sem acao explicita do usuario.
- [ ] Atalhos de teclado (shortcuts) sao documentados e nao conflitam com o navegador.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Keyboard trap ou funcionalidade inacessivel via teclado.                 |
| Major    | Focus ring removido ou modal sem focus trap.                             |
| Minor    | Skip link ausente ou ordem de tabulacao levemente inconsistente.         |
| Info     | Oportunidade de adicionar atalhos de teclado ou melhorar arrow navigation.|

## Cross-References

- `accessibility/a11y-wcag-audit.md` — Auditoria WCAG.
- `accessibility/a11y-aria-and-semantics.md` — ARIA e semantica.
- `ui/ui-states-and-feedback.md` — Estados e feedback visual.
- `design-system/ds-component-anatomy.md` — Anatomia de componentes.
