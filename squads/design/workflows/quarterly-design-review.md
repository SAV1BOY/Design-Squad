# Quarterly Design Review

## Metadata

| Campo         | Valor                                     |
| ------------- | ----------------------------------------- |
| squad         | Design                                    |
| versao        | 1.0.0                                     |
| criado_em     | 2026-03-06                                |
| owner         | Design Lead                               |
| cadencia      | Trimestral                                |
| duracao_media | 1 semana (prep + review + follow-up)      |
| tags          | review, trimestral, metricas, estrategia  |

## Trigger

Quando iniciar:

- Inicio de cada trimestre (Q1 jan, Q2 abr, Q3 jul, Q4 out).
- Final de ciclo estrategico que demanda avaliacao.
- Mudanca significativa no squad (reorg, novo leadership).

Pre-condicoes: dados semanais acumulados; metricas coletaveis; stakeholders disponiveis.

## Phases

### Fase 1 — Coleta de Metricas
**Agents:** Design Lead, Design Ops.
**Inputs:** Dados semanais, tracker, metricas DS, a11y, feedback.
**Atividades:** **Throughput:** features entregues, cycle time (request -> design pronto), handoff-to-release time. **Qualidade:** bugs visuais por feature, iteracoes pos-handoff, SUS/task success. **DS:** % adocao, componentes publicados, drift report. **A11y:** score atual vs anterior, issues abertos vs resolvidos. **Divida:** backlog cresceu ou reduziu, itens resolvidos. **Feedback qualitativo:** pesquisa com PM/Eng/designers (5 perguntas), NPS interno.
**Outputs:** Dashboard de metricas, comparativo com trimestre anterior, feedback compilado.

### Fase 2 — Analise de Divida
**Agents:** Design Lead, DS Lead.
**Inputs:** Backlog de divida, DS drift, a11y issues.
**Atividades:** Categorizar divida por tipo e area; tendencias (crescendo/estavel/reduzindo); calcular custo (tempo extra por divida); identificar concentracoes; recomendar sprint de reducao se necessario; avaliar eficacia das acoes preventivas.
**Outputs:** Relatorio de divida, tendencias, recomendacao, avaliacao preventivas.

### Fase 3 — Sessao de Review
**Agents:** Design Lead, PM Lead, Eng Lead, Designers.
**Inputs:** Dashboard, relatorio de divida, feedback, OKRs do trimestre.
**Atividades:** Apresentacao de metricas (20 min); retro (30 min): o que funcionou, nao funcionou, surpreendeu; review de OKRs (15 min): atingidos, parciais, nao atingidos; divida e saude DS (15 min); celebrar conquistas (10 min); identificar temas para proximo trimestre (15 min).
**Outputs:** Ata da sessao, OKRs avaliados, temas para proximo trimestre, conquistas celebradas.

### Fase 4 — Estrategia para Proximo Trimestre
**Agents:** Design Lead, PM Lead.
**Inputs:** Temas identificados, roadmap, feedback, gaps.
**Atividades:** Definir OKRs de design; alinhar com roadmap; iniciativas de melhoria de processo (workflows, rituais, ferramentas); investimentos DS (componentes, sprints de divida, a11y); investimentos people (treinamentos, contratacoes, mentoria); comunicar estrategia ao squad.
**Outputs:** OKRs do proximo trimestre, plano de iniciativas, plano DS, plano people, comunicacao ao squad.

## Quality Gates

### Gate Metricas Coletadas
- [ ] Todas as categorias compiladas.
- [ ] Comparativo com trimestre anterior.
- [ ] Feedback qualitativo coletado.

### Gate Divida Analisada
- [ ] Tendencias identificadas.
- [ ] Recomendacao feita.

### Gate Review Realizada
- [ ] Sessao com stakeholders concluida.
- [ ] OKRs avaliados.
- [ ] Conquistas celebradas.

### Gate Estrategia Definida
- [ ] OKRs definidos e alinhados.
- [ ] Plano de iniciativas documentado.
- [ ] Comunicacao ao squad realizada.

## Cross-References

- `weekly-design-ops-cadence.md` — Dados semanais alimentam review.
- `design-debt-reduction-sprint.md` — Sprint recomendado se necessario.
- `design-system-component-lifecycle.md` — Saude DS revisada.
- `accessibility-remediation-loop.md` — Score a11y revisado.
- `research-to-design-pipeline.md` — Insights informam estrategia.
- `new-designer-onboarding.md` — Plano people inclui onboarding.
- `ralphlooping-kaizen-design.md` — Resultados kaizen informam review.
