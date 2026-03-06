# Proto Interaction Fidelity

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Interaction Design             |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Prototyping Lead               |

## Objective

Avaliar se o nivel de fidelidade interativa do prototipo e adequado para comunicar
corretamente o comportamento esperado da interface. Interacoes bem prototipadas
permitem validar fluxos com usuarios, alinhar expectativas com engenharia e reduzir
ambiguidade sobre comportamentos dinamicos.

## When to Apply

- Ao decidir o nivel de interatividade necessario para cada prototipo.
- Antes de testes de usabilidade que dependem de interacao realista.
- Em revisoes de prototipo pre-handoff focadas em comportamento.
- Quando feedback de testes indica que o prototipo nao representava o comportamento real.

## Criteria

- [ ] Transicoes entre telas sao representadas com animacao adequada (slide, fade, push).
- [ ] Micro-interacoes criticas (toggle, accordion, dropdown) funcionam no prototipo.
- [ ] Gestos mobile (swipe, pinch, long press) estao prototipados quando relevantes.
- [ ] Scroll behavior (parallax, sticky, infinite scroll) e representado fielmente.
- [ ] Formularios permitem input simulado suficiente para o cenario de teste.
- [ ] Feedback visual (loading, success, error) e disparado corretamente nas interacoes.
- [ ] Drag and drop e reordenacao sao representados quando fazem parte do fluxo.
- [ ] Tooltips e popovers aparecem no contexto correto de interacao.
- [ ] Transicoes condicionais (if/else) representam caminhos diferentes do fluxo.
- [ ] O prototipo simula delays realistas para acoes assincronas.
- [ ] Interacoes de teclado (Tab, Enter, Escape) sao suportadas quando necessario.
- [ ] O nivel de interatividade nao excede o necessario para o objetivo do prototipo.
- [ ] Limitacoes de interacao do prototipo estao documentadas para moderadores de teste.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Interacao critica ausente que invalida resultados de teste de usabilidade.|
| Major    | Transicoes entre telas ausentes ou feedback visual nao representado.      |
| Minor    | Gestos mobile nao prototipados ou delays nao realistas.                  |
| Info     | Oportunidade de adicionar interacoes condicionais ou melhorar fidelidade. |

## Cross-References

- `prototyping/proto-fidelity-choice.md` — Escolha de fidelidade.
- `prototyping/proto-scenario-coverage.md` — Cobertura de cenarios.
- `ui/ui-states-and-feedback.md` — Estados e feedback visual.
- `prototyping/proto-handoff-readiness.md` — Prontidao de handoff.
