# Frost Pattern Library Quality

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Frost                          |
| Domain      | Design System                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Frost Lead                     |

## Objective

Avaliar a qualidade da pattern library do design system, verificando se os patterns
documentados sao consistentes, reutilizaveis e cobrem os cenarios mais comuns de uso.
Patterns bem definidos reduzem retrabalho e aceleram o desenvolvimento de novas features.

## When to Apply

- A cada novo pattern adicionado a biblioteca.
- Em revisoes semestrais de qualidade do design system.
- Quando novos fluxos de usuario sao criados e precisam de patterns.
- Ao receber feedback recorrente de inconsistencia visual de squads consumidores.

## Criteria

- [ ] Cada pattern possui descricao clara de contexto de uso (quando usar e quando nao usar).
- [ ] Patterns incluem exemplos visuais com estados: default, hover, active, focus e disabled.
- [ ] Existe codigo de exemplo funcional acompanhando cada pattern documentado.
- [ ] Patterns sao compostos por componentes do design system, sem elementos ad-hoc.
- [ ] A nomenclatura dos patterns segue convencao consistente e pesquisavel.
- [ ] Patterns possuem guidelines de responsividade com breakpoints documentados.
- [ ] Cada pattern tem pelo menos dois exemplos de uso real em produtos ativos.
- [ ] Patterns incluem consideracoes de acessibilidade especificas para o contexto.
- [ ] Existe versionamento individual para patterns, com changelog acessivel.
- [ ] Patterns deprecados possuem alternativa recomendada e migration path.
- [ ] A pattern library e pesquisavel e possui navegacao por categoria e tag.
- [ ] Testes de visual regression cobrem todos os patterns em estado stable.
- [ ] Feedback de consumidores e coletado e priorizado para evolucao dos patterns.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Pattern sem exemplos visuais ou usando componentes fora do design system. |
| Major    | Pattern sem guidelines de acessibilidade ou responsividade.               |
| Minor    | Nomenclatura inconsistente ou falta de exemplos de uso real.              |
| Info     | Oportunidade de adicionar mais variantes ou melhorar documentacao.        |

## Cross-References

- `frost/frost-atomic-design-audit.md` — Validacao da hierarquia atomic design.
- `frost/frost-component-inventory-audit.md` — Inventario de componentes.
- `frost/frost-documentation-and-adoption.md` — Documentacao e adocao.
- `ui/ui-component-consistency.md` — Consistencia de componentes UI.
