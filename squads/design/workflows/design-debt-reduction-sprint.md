# Design Debt Reduction Sprint

## Metadata

| Campo         | Valor                                         |
| ------------- | --------------------------------------------- |
| squad         | Design                                        |
| versao        | 1.0.0                                         |
| criado_em     | 2026-03-06                                    |
| owner         | Design Lead                                   |
| cadencia      | Trimestral ou quando divida atinge threshold  |
| duracao_media | 1-2 sprints dedicados                         |
| tags          | divida, debt, reducao, sprint, payoff         |

## Trigger

Quando iniciar:

- Backlog de divida atinge threshold (30+ itens ou 20% do backlog total).
- Review trimestral identifica divida como risco.
- Multiplos designers reportam friccao por inconsistencias.
- NPS em declinio correlacionado com issues visuais.

Pre-condicoes: backlog de divida existente e categorizado; Design Lead e PM acordam alocacao de sprint; metricas de impacto estimadas.

## Phases

### Fase 1 — Inventario
**Agents:** Design Lead, Designers.
**Inputs:** Backlog existente, audit visual, feedback, bugs P3 acumulados.
**Atividades:** Consolidar todas as fontes em lista unica (componentes detached, inconsistencias visuais, patterns desatualizados, fluxos com usabilidade ruim, copy inconsistente, a11y issues); categorizar por tipo (visual, interacao, informacao, a11y, DS drift) e area; estimar impacto (usuario, velocidade do time, brand consistency): alto/medio/baixo.
**Outputs:** Inventario consolidado e categorizado, impacto por item, metricas (total, distribuicao, idade media).

### Fase 2 — Priorizacao
**Agents:** Design Lead, PM, Tech Lead.
**Inputs:** Inventario, roadmap, capacidade do sprint.
**Atividades:** RICE score (Reach, Impact, Confidence, Effort); agrupar itens por area/componente (batch); identificar quick wins (alto impacto, baixo esforco); definir meta do sprint (numero de itens ou % reducao); criar sprint backlog; alinhar com engenharia sobre itens de codigo.
**Outputs:** Sprint backlog priorizado, quick wins, meta definida, alinhamento com engenharia.

### Fase 3 — Sprint de Reducao
**Agents:** Designers, Frontend Engineers (itens de codigo).
**Inputs:** Sprint backlog, DS vigente, guidelines.
**Atividades:** Atualizar componentes detached para DS; corrigir inconsistencias visuais; atualizar patterns; melhorar fluxos; para itens de codigo: designer prepara specs, engineer implementa, QA simplificado; daily standup dedicado (15 min); registrar itens concluidos.
**Outputs:** Itens resolvidos, inventario atualizado, PRs abertos, decisoes documentadas.

### Fase 4 — Payoff (Validacao)
**Agents:** Design Lead, QA, PM.
**Inputs:** Itens resolvidos, builds em staging, inventario.
**Atividades:** Review visual; QA em staging; calcular metricas de payoff (itens resolvidos vs meta, % reducao, areas impactadas); comunicar resultados (before/after screenshots, metricas); atualizar baseline; definir acoes preventivas.
**Outputs:** Relatorio de payoff, baseline atualizado, acoes preventivas, proximo ciclo agendado.

## Acoes Preventivas

1. Check de consistencia no handoff (ver `handoff-and-build-loop.md`).
2. 10-15% da capacidade semanal para divida (ver `weekly-design-ops-cadence.md`).
3. Monitorar DS adoption (detached components = nova divida).
4. Threshold de alerta: backlog > N itens aciona sprint.

## Quality Gates

### Gate Inventario -> Priorizacao
- [ ] Fontes consolidadas.
- [ ] Itens categorizados e impacto estimado.

### Gate Priorizacao -> Sprint
- [ ] RICE score calculado.
- [ ] Meta definida e acordada.
- [ ] Quick wins identificados.

### Gate Sprint -> Payoff
- [ ] Itens priorizados trabalhados.
- [ ] Inventario atualizado.

### Gate Payoff -> Fechamento
- [ ] Metricas calculadas.
- [ ] Resultados comunicados.
- [ ] Acoes preventivas definidas.

## Cross-References

- `weekly-design-ops-cadence.md` — Sexta dedicada a divida.
- `quarterly-design-review.md` — Divida revisada trimestralmente.
- `design-system-bootstrap.md` — Inventario identifica divida.
- `handoff-and-build-loop.md` — P3 alimentam backlog.
- `accessibility-remediation-loop.md` — A11y issues como divida.
- `design-system-component-lifecycle.md` — Componentes desatualizados.
