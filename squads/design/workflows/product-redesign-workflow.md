# Product Redesign Workflow

## Metadata

| Campo         | Valor                                     |
| ------------- | ----------------------------------------- |
| squad         | Design                                    |
| versao        | 1.0.0                                     |
| criado_em     | 2026-03-06                                |
| owner         | Design Lead                               |
| cadencia      | Por demanda (redesigns sao raros)         |
| duracao_media | 2-4 meses (end-to-end)                   |
| tags          | redesign, audit, strategy, exploration    |

## Trigger

Quando iniciar:

- Reposicionamento estrategico (novo mercado, nova audiencia).
- Metricas UX em declinio por 2+ trimestres.
- Divida acumulada torna iteracao incremental insuficiente.
- Competidores mudaram baseline de expectativa dos usuarios.
- Mudanca de brand identity que afeta toda a interface.

Pre-condicoes: sponsorship executivo com budget e timeline; equipe dedicada (min 2 designers, 1 researcher, PM); acordo de phased rollout (nao big-bang); baseline de metricas existente.

## Phases

### Fase 1 — Audit
**Agents:** Design Lead, Researcher, PM, Data Analyst.
**Inputs:** Produto atual, metricas historicas, feedback, competidores.
**Atividades:** **UX audit:** mapear fluxos, pain points, heuristic evaluation, SUS. **Visual audit:** inventario de inconsistencias, brand alignment, a11y score. **Data audit:** funnels de conversao, feature usage, segmentacao. **Competitivo:** benchmark 3-5 competidores, gaps e diferenciacao. Consolidar em relatorio.
**Outputs:** Relatorio completo (UX, visual, dados, competitivo), pain points priorizados, scores baseline, benchmark.

### Fase 2 — Strategy
**Agents:** Design Lead, PM, Researcher, Sponsor.
**Inputs:** Relatorio audit, objetivos estrategicos, constraints.
**Atividades:** Definir visao do redesign; 3-5 principios de design; priorizar areas (nao tudo de uma vez); phasing strategy (alpha internos -> beta 10-20% -> GA 100%); metricas de sucesso por fase; roadmap com milestones; sign-off do sponsor.
**Outputs:** Visao e principios, phasing strategy, metricas por fase, roadmap, sign-off.

### Fase 3 — Exploration
**Agents:** Designers do time de redesign.
**Inputs:** Visao, principios, DS, areas priorizadas.
**Atividades:** Moodboards e style tiles (2-3 direcoes); conceitos completos para fluxos core; internal review com stakeholders; teste de conceito com 5-8 usuarios; selecionar direcao; definir visual language (tipografia, cores, iconografia, motion); kitchen sink page.
**Outputs:** Conceitos documentados, direcao selecionada, visual language, kitchen sink, resultados teste.

### Fase 4 — Refine
**Agents:** Designers, DS Lead, Frontend Engineer.
**Inputs:** Direcao visual, areas fase 1, DS.
**Atividades:** High-fi mockups para todos os fluxos fase 1; motion design language; atualizar/criar componentes DS; responsividade e a11y; viabilidade tecnica com Tech Lead; teste de usabilidade; iterar; preparar handoff.
**Outputs:** Mockups high-fi, motion specs, componentes DS, teste concluido, handoff pronto.

### Fase 5 — Ship (Phased Rollout)
**Agents:** Designers, Engineers, QA, PM.
**Inputs:** Handoff, phasing strategy, feature flags.
**Atividades:** **Build:** via `handoff-and-build-loop.md`. **Alpha:** internos + dogfooding, corrigir criticos. **Beta:** 10-20% via feature flag, monitorar metricas, A/B se possivel. **Iterate:** ajustar com dados beta. **GA:** 100%, monitorar 30/60/90 dias vs baseline. **Proxima fase:** repetir Fases 3-5 para proximas areas.
**Outputs:** Redesign em producao (phased), metricas comparativas, relatorio de impacto, backlog proxima fase.

## Quality Gates

### Gate Audit -> Strategy
- [ ] Relatorio completo.
- [ ] Pain points priorizados.
- [ ] Scores baseline.

### Gate Strategy -> Exploration
- [ ] Visao e principios aprovados.
- [ ] Phasing strategy definida.
- [ ] Sign-off do sponsor.

### Gate Exploration -> Refine
- [ ] Min 2 conceitos explorados.
- [ ] Teste de conceito realizado.
- [ ] Visual language definida.

### Gate Refine -> Ship
- [ ] Mockups high-fi completos.
- [ ] Teste de usabilidade positivo.
- [ ] Componentes DS prontos.
- [ ] Handoff completo.

### Gate Ship -> Proxima Fase
- [ ] Beta com metricas positivas.
- [ ] GA deployado.
- [ ] Metricas 30 dias vs baseline.

## Cross-References

- `design-system-bootstrap.md` — Redesign pode demandar novo DS.
- `usability-testing-sprint.md` — Testes em Fases 3 e 4.
- `handoff-and-build-loop.md` — Build padrao.
- `design-debt-reduction-sprint.md` — Redesign resolve divida.
- `design-system-migration-workflow.md` — Se DS muda.
- `quarterly-design-review.md` — Progresso revisado trimestralmente.
