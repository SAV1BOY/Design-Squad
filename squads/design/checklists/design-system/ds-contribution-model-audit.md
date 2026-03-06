# DS Contribution Model Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Contribution Process           |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Design System Lead             |

## Objective

Avaliar o modelo de contribuicao do design system, verificando se o processo para
squads externos proporem, desenvolverem e integrarem novos componentes ou melhorias
e claro, acessivel e eficiente. Um modelo de contribuicao saudavel distribui o
esforco de evolucao e aumenta o senso de pertencimento.

## When to Apply

- Em revisoes semestrais do modelo de contribuicao.
- Quando poucas contribuicoes externas sao recebidas.
- Ao receber feedback de que o processo de contribuicao e complexo.
- Em reestruturacoes do time de design system.

## Criteria

- [ ] O modelo de contribuicao esta documentado em guia acessivel publicamente.
- [ ] Tipos de contribuicao estao definidos: bug fix, melhoria, novo componente, documentacao.
- [ ] O fluxo de contribuicao passo a passo esta detalhado com templates e exemplos.
- [ ] Existe processo de RFC (Request for Comments) para novos componentes.
- [ ] Criterios de aceite para contribuicoes sao claros e publicos.
- [ ] Existe code review dedicado do time core para contribuicoes externas.
- [ ] SLA de resposta para contribuicoes esta definido e monitorado.
- [ ] Contribuidores recebem feedback construtivo e orientacao durante o processo.
- [ ] Existe reconhecimento publico para contribuidores (hall of fame, changelog mention).
- [ ] Templates de PR e issue estao configurados no repositorio.
- [ ] Testes e linting sao executados automaticamente em contribuicoes.
- [ ] Existe processo de escalacao quando contribuicoes ficam travadas.
- [ ] Metricas de contribuicao sao rastreadas (volume, tempo de review, acceptance rate).
- [ ] O modelo suporta contribuicoes tanto de design quanto de codigo.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Modelo de contribuicao inexistente ou nao documentado.                    |
| Major    | SLA nao definido ou contribuicoes ignoradas sem feedback.                |
| Minor    | Templates ausentes ou reconhecimento de contribuidores inexistente.       |
| Info     | Oportunidade de melhorar automacao de CI ou expandir metricas.            |

## Cross-References

- `frost/frost-design-system-governance.md` — Governanca do design system.
- `mall/mall-design-system-team-model-audit.md` — Modelo de time.
- `design-system/ds-versioning-and-changelog.md` — Versionamento.
- `design-system/ds-adoption-playbook.md` — Playbook de adocao.
