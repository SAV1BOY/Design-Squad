# Mall System-First Product Fit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Mall                           |
| Domain      | Product-System Alignment       |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Mall Lead                      |

## Objective

Avaliar se o processo de design adota uma abordagem system-first, onde componentes e
patterns do design system sao priorizados antes de solucoes customizadas. Esta abordagem
maximiza a reutilizacao, mantém consistencia e reduz custo de manutencao a longo prazo.

## When to Apply

- No inicio da fase de ideacao de novas features.
- Em design reviews antes do handoff para engenharia.
- Quando um squad solicita criacao de novo componente customizado.
- Em auditorias trimestrais de aderencia ao design system.

## Criteria

- [ ] Designers consultam o design system antes de criar solucoes visuais novas.
- [ ] Novos designs priorizam componentes existentes do sistema sobre solucoes ad-hoc.
- [ ] Quando customizacao e necessaria, existe justificativa documentada.
- [ ] Propostas de novos componentes passam por avaliacao de reutilizabilidade.
- [ ] Existe mecanismo de feedback do produto para o design system (upstream contribution).
- [ ] Features sao desenhadas considerando o ecossistema completo, nao apenas o contexto local.
- [ ] O design system e atualizado quando patterns recorrentes emergem de features.
- [ ] Metricas de aderencia ao design system sao rastreadas por squad e por produto.
- [ ] Designers conhecem e utilizam a biblioteca de patterns antes de criar novos fluxos.
- [ ] A avaliacao de system-first e parte formal do processo de design review.
- [ ] Existe catalogo de excecoes aprovadas com justificativas documentadas.
- [ ] O time de design system e consultado para componentes que fogem dos patterns.
- [ ] Existe processo para promover solucoes locais bem-sucedidas ao design system.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Feature inteira construida sem consulta ao design system.                 |
| Major    | Componentes customizados criados sem justificativa documentada.           |
| Minor    | Metricas de aderencia nao rastreadas ou feedback upstream ausente.        |
| Info     | Oportunidade de promover componente local ao design system.              |

## Cross-References

- `frost/frost-component-inventory-audit.md` — Inventario de componentes.
- `frost/frost-design-system-governance.md` — Governanca do design system.
- `design-system/ds-adoption-playbook.md` — Playbook de adocao.
- `design-system/ds-contribution-model-audit.md` — Modelo de contribuicao.
