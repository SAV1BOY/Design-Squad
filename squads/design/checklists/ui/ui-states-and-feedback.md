# UI States and Feedback

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Interaction Design             |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | UI Lead                        |

## Objective

Verificar se todos os componentes interativos possuem estados visuais claramente
definidos e se o sistema fornece feedback adequado para cada acao do usuario. Estados
e feedback completos comunicam responsividade, previnem erros e constroem confianca
na interface.

## When to Apply

- Em revisoes de design de componentes interativos.
- Ao auditar a completude de especificacoes antes do handoff.
- Quando usuarios reportam que a interface parece "travada" ou nao-responsiva.
- Em auditorias de qualidade visual trimestrais.

## Criteria

- [ ] Todos os elementos interativos possuem estado default claramente definido.
- [ ] Estado hover fornece feedback visual imediato ao posicionar o cursor.
- [ ] Estado active/pressed e visualmente distinto do hover.
- [ ] Estado focus e visivel e atende requisitos de acessibilidade (focus ring).
- [ ] Estado disabled e visualmente diferenciado com reducao de opacidade ou cor.
- [ ] Estado loading indica progresso com spinner, skeleton ou progress bar.
- [ ] Estado error exibe indicacao visual clara com cor e icone de alerta.
- [ ] Estado success confirma acao concluida com feedback visual positivo.
- [ ] Estado empty state orienta o usuario quando nao ha dados para exibir.
- [ ] Transicoes entre estados sao suaves e possuem duracao consistente.
- [ ] Feedback haptico (mobile) ou sonoro e utilizado quando apropriado.
- [ ] Micro-interacoes reforçam acoes do usuario sem distrair.
- [ ] Todos os estados estao documentados no Storybook ou ferramenta equivalente.
- [ ] Edge cases de estado (simultaneous hover+focus, disabled+tooltip) estao definidos.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Elemento interativo sem estado hover ou focus visivel.                    |
| Major    | Ausencia de loading state em acoes assincronas ou error state ausente.    |
| Minor    | Transicoes abruptas entre estados ou empty state generico.                |
| Info     | Oportunidade de adicionar micro-interacoes ou melhorar feedback haptico.  |

## Cross-References

- `ux/ux-error-prevention-and-recovery.md` — Prevencao e recuperacao de erros.
- `ui/ui-component-consistency.md` — Consistencia de componentes.
- `accessibility/a11y-keyboard-and-focus.md` — Teclado e foco.
- `design-system/ds-component-anatomy.md` — Anatomia de componentes.
