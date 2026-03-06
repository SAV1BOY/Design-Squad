# Proto Scenario Coverage

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Prototyping                    |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Prototyping Lead               |

## Objective

Verificar se o prototipo cobre todos os cenarios relevantes para validacao, incluindo
o happy path, caminhos alternativos, edge cases e estados de erro. Cobertura completa
de cenarios garante que testes de usabilidade revelam problemas reais e que o handoff
contempla todas as situacoes que o desenvolvedor precisara implementar.

## When to Apply

- Antes de iniciar testes de usabilidade com o prototipo.
- Em revisoes de design pre-handoff.
- Quando testes anteriores nao revelaram problemas que surgiram em producao.
- Ao planejar cenarios para testes de usabilidade.

## Criteria

- [ ] O happy path (fluxo principal) esta completamente prototipado e funcional.
- [ ] Caminhos alternativos (secondary flows) estao cobertos no prototipo.
- [ ] Estados de erro (validacao, falha de sistema, timeout) estao representados.
- [ ] Empty states sao mostrados para listas, dashboards e buscas sem resultado.
- [ ] Loading states e skeletons estao incluidos para acoes assincronas.
- [ ] Extremos de conteudo (texto longo, lista extensa, sem dados) estao representados.
- [ ] Fluxo de primeira vez (first-time user experience) esta prototipado.
- [ ] Fluxo de usuario recorrente (returning user) esta representado.
- [ ] Cenarios de permissao (usuario sem acesso, feature bloqueada) estao incluidos.
- [ ] Responsividade e coberta nos breakpoints criticos (mobile, tablet, desktop).
- [ ] Cenarios de offline ou conectividade instavel sao considerados quando relevante.
- [ ] O prototipo inclui entrada e saida do fluxo (de onde vem e para onde vai o usuario).
- [ ] Existe lista documentada de cenarios cobertos e nao cobertos pelo prototipo.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Happy path incompleto ou estados de erro ausentes em fluxos criticos.    |
| Major    | Empty states ou loading states nao representados no prototipo.            |
| Minor    | Extremos de conteudo ou cenarios de permissao nao cobertos.               |
| Info     | Oportunidade de cobrir cenarios de offline ou melhorar documentacao.      |

## Cross-References

- `prototyping/proto-fidelity-choice.md` — Escolha de fidelidade.
- `prototyping/proto-usability-setup.md` — Setup de usabilidade.
- `handoff/handoff-edge-cases-documented.md` — Edge cases documentados.
- `ux/ux-error-prevention-and-recovery.md` — Prevencao e recuperacao de erros.
