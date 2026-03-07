# Weekly Design Ops Cadence

## Metadata

| Campo         | Valor                                      |
| ------------- | ------------------------------------------ |
| squad         | Design                                     |
| versao        | 1.0.0                                      |
| criado_em     | 2026-03-06                                 |
| owner         | Design Ops Lead                            |
| cadencia      | Semanal (recorrente)                       |
| duracao_media | Ciclo continuo                             |
| tags          | ops, cadencia, backlog, critique, releases |

## Trigger

Quando iniciar:

- Todo inicio de semana (segunda-feira), automaticamente.
- Ao formar novo Design Squad que precisa de ritmo operacional.
- Apos retro que identifica falta de cadencia como problema.

Pre-condicoes: squad com min 2 designers; backlog de design existente; calendario com slots reservados.

## Phases

### Fase 1 — Segunda: Backlog Grooming
**Agents:** Design Lead, Designers, PM (convidado). **Timebox:** 45 min.
**Inputs:** Backlog atualizado, prioridades do sprint, novas solicitacoes.
**Atividades:** Triagem de itens novos; estimar com t-shirt sizing (S/M/L/XL); priorizar (impacto x esforco); atribuir owners; identificar dependencias; atualizar status.
**Outputs:** Backlog priorizado e atribuido, dependencias sinalizadas, bloqueios escalados.

### Fase 2 — Terca/Quarta: Design Critique
**Agents:** Todos os designers, convidados opcionais. **Timebox:** 60 min.
**Inputs:** Trabalho em andamento, contexto de cada projeto, framework de critique.
**Atividades:** Cada designer apresenta WIP (5-7 min); feedback estruturado (likes, wishes, questions); facilitador registra decisoes e action items; identificar patterns para DS.
**Outputs:** Feedback documentado, action items com owners, candidates para DS.

### Fase 3 — Quinta: Releases e Handoffs
**Agents:** Designers, Frontend Engineers, QA. **Timebox:** Variavel (30-45 min por handoff).
**Inputs:** Designs finalizados, checklist de handoff, calendario de releases.
**Atividades:** Revisar designs prontos; executar checklist de qualidade; realizar sessoes de handoff; acompanhar QA visual; registrar releases.
**Outputs:** Handoffs com documentacao completa, QA em andamento, release log atualizado.

### Fase 4 — Sexta: Divida e Housekeeping
**Agents:** Design Lead, Designers. **Timebox:** 2h (individual + 15 min sync).
**Inputs:** Backlog de divida, inconsistencias da semana, metricas DS.
**Atividades:** Registrar nova divida; dedicar 1-2h para pagar divida priorizada; organizar Figma files; revisar docs desatualizadas; preparar resumo semanal.
**Outputs:** Divida atualizada, Figma organizado, resumo semanal enviado.

## Quality Gates

### Gate Semanal — Backlog
- [ ] Itens novos triados e estimados.
- [ ] Owners atribuidos.
- [ ] Dependencias sinalizadas.

### Gate Semanal — Critique
- [ ] Min 1 sessao realizada.
- [ ] Feedback documentado.
- [ ] Action items com owners.

### Gate Semanal — Releases
- [ ] Handoffs com checklist completo.
- [ ] QA visual executado.

### Gate Semanal — Divida
- [ ] Novas dividas registradas.
- [ ] Min 1 item resolvido.
- [ ] Resumo enviado ate sexta 17h.

### Gate Mensal — Health Check
- [ ] Throughput revisado (itens/semana).
- [ ] Cycle time comparado com mes anterior.

## Cross-References

- `design-critique-loop.md` — Framework detalhado de critique (Fase 2).
- `handoff-and-build-loop.md` — Processo de handoff (Fase 3).
- `design-debt-reduction-sprint.md` — Sprint quando divida acumula (Fase 4).
- `quarterly-design-review.md` — Revisao trimestral alimentada por dados semanais.
- `feature-design-end-to-end.md` — Features seguem este pipeline.
