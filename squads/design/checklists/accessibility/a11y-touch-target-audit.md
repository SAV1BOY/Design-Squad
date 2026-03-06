# A11Y Touch Target Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Accessibility                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Accessibility Lead             |

## Objective

Verificar se os alvos de toque e clique no produto atendem aos tamanhos minimos
recomendados para garantir operabilidade por usuarios com deficiencia motora,
usuarios de dispositivos moveis e contextos de uso com precisao reduzida.
Touch targets adequados previnem erros de toque e melhoram a experiencia para todos.

## When to Apply

- Em auditorias de acessibilidade mobile.
- Ao projetar interfaces touch-first ou responsivas.
- Quando analytics indicam alta taxa de mis-taps em elementos especificos.
- Ao adaptar interfaces desktop para mobile ou wearables.

## Criteria

- [ ] Touch targets possuem tamanho minimo de 44x44px (WCAG 2.5.5) ou 48x48dp (Material Design).
- [ ] Espacamento entre touch targets adjacentes e de pelo menos 8px para evitar mis-taps.
- [ ] Botoes de acao primaria possuem area de toque generosa (minimo 48x48px).
- [ ] Links inline em texto possuem padding suficiente para toque preciso.
- [ ] Checkboxes e radio buttons possuem area clicavel expandida alem do icone.
- [ ] Icones interativos sem texto possuem area de toque estendida via padding.
- [ ] Close buttons (X) em modais e toasts possuem tamanho adequado.
- [ ] Elementos de navegacao (tabs, menu items) atendem tamanho minimo.
- [ ] Toggle switches possuem area de toque que cobre todo o componente.
- [ ] Inputs de formulario possuem altura minima confortavel para toque.
- [ ] Acoes destrutivas nao estao posicionadas adjacentes a acoes frequentes.
- [ ] Touch targets foram testados em dispositivos reais, nao apenas emulador.
- [ ] O design considera uso com uma mao (thumb zone) em dispositivos moveis.
- [ ] Componentes de paginacao e stepper possuem alvos de toque adequados.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Touch target abaixo de 24x24px em acao critica ou destrutiva.            |
| Major    | Touch targets abaixo de 44x44px em areas de alta interacao.              |
| Minor    | Espacamento insuficiente entre targets adjacentes ou close button pequeno.|
| Info     | Oportunidade de otimizar thumb zone ou expandir areas clicaveis.         |

## Cross-References

- `accessibility/a11y-wcag-audit.md` — Auditoria WCAG (criterio 2.5.5).
- `accessibility/a11y-keyboard-and-focus.md` — Teclado e foco.
- `ui/ui-spacing-and-grid.md` — Espacamento e grid.
- `ui/ui-states-and-feedback.md` — Estados e feedback visual.
