# UX Task Completion Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | UX Performance                 |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | UX Lead                        |

## Objective

Avaliar a eficacia dos fluxos do produto em permitir que usuarios completem tarefas
com sucesso, eficiencia e satisfacao. A auditoria mede task success rate, time on task
e identifica pontos de abandono que impactam a experiencia e os resultados de negocio.

## When to Apply

- Em auditorias trimestrais de performance dos fluxos criticos.
- Quando metricas indicam queda em task completion rate.
- Apos redesign de fluxos para medir impacto das mudancas.
- Ao comparar performance entre plataformas (web vs. mobile).

## Criteria

- [ ] Tarefas criticas do produto estao identificadas e priorizadas para auditoria.
- [ ] Task success rate e medido para cada tarefa critica com meta definida.
- [ ] Time on task e medido e comparado com benchmarks ou versoes anteriores.
- [ ] Pontos de abandono (drop-off points) sao identificados com funnel analysis.
- [ ] Error rate por tarefa e rastreado e categorizado por tipo de erro.
- [ ] O numero de passos para completar cada tarefa e minimizado e justificado.
- [ ] Caminhos alternativos para mesma tarefa sao mapeados e otimizados.
- [ ] Usuarios conseguem retomar tarefas interrompidas sem perda de progresso.
- [ ] Confirmacao de sucesso e clara e celebra a conclusao da tarefa.
- [ ] Tarefas frequentes sao acessiveis em ate 3 cliques ou taps da tela inicial.
- [ ] Performance tecnica (load time, latencia) nao impacta a conclusao de tarefas.
- [ ] Testes de usabilidade modulados validam tarefas criticas periodicamente.
- [ ] Resultados da auditoria alimentam backlog de melhorias priorizadas.
- [ ] Comparacao entre task completion em diferentes segmentos de usuarios e realizada.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Task success rate abaixo de 70% em tarefa critica do produto.             |
| Major    | Drop-off point com mais de 30% de abandono sem intervencao planejada.    |
| Minor    | Tarefa frequente exigindo mais de 5 cliques ou ausencia de confirmacao.   |
| Info     | Oportunidade de otimizar caminhos alternativos ou melhorar celebracao.    |

## Cross-References

- `ux/ux-metrics-heart-audit.md` — Metricas HEART (Task Success).
- `ux/ux-cognitive-load-audit.md` — Carga cognitiva.
- `ux/ux-error-prevention-and-recovery.md` — Prevencao e recuperacao de erros.
- `product/product-success-criteria.md` — Criterios de sucesso do produto.
