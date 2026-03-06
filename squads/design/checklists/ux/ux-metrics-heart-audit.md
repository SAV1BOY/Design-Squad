# UX Metrics HEART Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | UX Measurement                 |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | UX Lead                        |

## Objective

Avaliar a implementacao do framework HEART (Happiness, Engagement, Adoption, Retention,
Task Success) para medicao de qualidade de UX. Metricas bem definidas permitem ao time
tomar decisoes baseadas em dados, medir impacto de mudancas e demonstrar valor do
design para a organizacao.

## When to Apply

- Ao definir metricas para um novo produto ou feature.
- Em revisoes trimestrais de performance de UX.
- Quando stakeholders questionam o impacto do trabalho de design.
- Ao estabelecer OKRs relacionados a experiencia do usuario.

## Criteria

- [ ] Happiness: metricas de satisfacao (CSAT, SUS, NPS) sao coletadas regularmente.
- [ ] Engagement: metricas de engajamento (session duration, actions per session) sao rastreadas.
- [ ] Adoption: metricas de adocao (new users, feature adoption rate) sao monitoradas.
- [ ] Retention: metricas de retencao (churn, DAU/MAU ratio) sao acompanhadas.
- [ ] Task Success: metricas de sucesso de tarefa (completion rate, time on task, error rate) existem.
- [ ] Cada metrica tem goal, signal e metric definidos conforme framework GSM.
- [ ] Metricas sao segmentadas por persona, plataforma ou fluxo relevante.
- [ ] Existe dashboard acessivel ao time de design com as metricas HEART.
- [ ] Baselines foram estabelecidas para cada metrica antes de intervencoes.
- [ ] Metricas sao revisadas em cerimonias regulares com o time (sprint review, monthly).
- [ ] Correlacoes entre metricas de UX e metricas de negocio sao documentadas.
- [ ] Alertas automaticos notificam o time quando metricas caem abaixo do threshold.
- [ ] Decisoes de design sao retroalimentadas com dados de impacto pos-lancamento.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Nenhuma metrica de UX e rastreada ou nao ha baseline definido.            |
| Major    | Metricas coletadas mas nao revisadas ou sem conexao com decisoes.         |
| Minor    | Dashboard inacessivel ou metricas nao segmentadas.                        |
| Info     | Oportunidade de adicionar alertas automaticos ou melhorar correlacoes.    |

## Cross-References

- `malouf/malouf-ux-strategy-audit.md` — Estrategia de UX.
- `ux/ux-task-completion-audit.md` — Auditoria de conclusao de tarefas.
- `product/product-success-criteria.md` — Criterios de sucesso do produto.
- `product/product-experiment-design.md` — Design de experimentos.
