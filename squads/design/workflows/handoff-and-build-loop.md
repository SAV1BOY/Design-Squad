# Handoff and Build Loop

## Metadata

| Campo         | Valor                                  |
| ------------- | -------------------------------------- |
| squad         | Design                                 |
| versao        | 1.0.0                                  |
| criado_em     | 2026-03-06                             |
| owner         | Designer responsavel + Tech Lead       |
| cadencia      | Por feature/story                      |
| duracao_media | 1-2 sprints (handoff ate QA sign-off)  |
| tags          | handoff, build, QA, specs, ajustes     |

## Trigger

Quando iniciar:

- Design aprovado e pronto para implementacao.
- Quality gate de handoff atingido no `feature-design-end-to-end.md`.
- Hotfix visual que precisa de specs rapidos.

Pre-condicoes: design finalizado com todos os estados; tokens e componentes DS mapeados; frontend engineer alocado; story com acceptance criteria.

## Phases

### Fase 1 — Specs
**Agents:** Designer, Frontend Engineer.
**Inputs:** Design finalizado (Figma), tokens, story com acceptance criteria.
**Atividades:** Preparar handoff page no Figma (espacamento, tipografia, cores com tokens semanticos; estados: default, hover, focus, active, disabled, loading, error, empty; breakpoints e responsividade; motion specs); exportar assets; mapear componentes DS vs custom; documentar copy final; sessao de handoff sync (45-60 min) com walkthrough completo.
**Outputs:** Handoff page completa, assets exportados, notas da sessao, canal de duvidas definido.

### Fase 2 — Build
**Agents:** Frontend Engineer, Designer (consultivo).
**Inputs:** Handoff page, componentes DS, story.
**Atividades:** Implementar seguindo specs com componentes DS; consultar designer para duvidas; implementar todos os estados; usar tokens semanticos (sem hard-coded); implementar responsividade e a11y; self-review visual; abrir PR com screenshots comparativos.
**Outputs:** PR com implementacao, screenshots design vs build, build em preview/staging.

### Fase 3 — QA Visual
**Agents:** Designer, QA Engineer, Frontend Engineer.
**Inputs:** Build em staging, design como ref, acceptance criteria.
**Atividades:** Pixel comparison por breakpoint; verificar todos os estados; validar motion; spot-check a11y (tab order, focus, contraste); registrar bugs com screenshot lado-a-lado, breakpoint, browser, severidade (P1 blocker / P2 deve corrigir / P3 nice-to-have).
**Outputs:** Lista de bugs priorizados, status: aprovado / com ressalvas / reprovado.

### Fase 4 — Ajustes
**Agents:** Frontend Engineer, Designer (validacao).
**Inputs:** Bugs priorizados, design como ref.
**Atividades:** Corrigir P1 imediatamente; P2 no mesmo sprint; P3 vai para backlog de divida; designer re-valida cada correcao; ciclo repete ate P1+P2 zerados; sign-off final; documentar aprendizados.
**Outputs:** P1+P2 resolvidos, sign-off do designer, P3 no backlog, feature pronta para release.

## Quality Gates

### Gate Specs -> Build
- [ ] Handoff page com todos os estados.
- [ ] Sessao de handoff realizada.
- [ ] Assets exportados.

### Gate Build -> QA
- [ ] Todos os estados implementados.
- [ ] Tokens semanticos (sem hard-coded).
- [ ] Self-review visual feito.
- [ ] PR com screenshots comparativos.

### Gate QA -> Ajustes
- [ ] Review lado-a-lado concluido.
- [ ] Bugs categorizados por severidade.

### Gate Ajustes -> Release
- [ ] P1 e P2 resolvidos.
- [ ] Sign-off do designer.
- [ ] Aprendizados documentados.

## Cross-References

- `feature-design-end-to-end.md` — Detalha Fases 5 e 6 do pipeline.
- `design-to-code-sync.md` — Tokens sincronizados antes do build.
- `accessibility-remediation-loop.md` — Issues de a11y no QA.
- `weekly-design-ops-cadence.md` — Handoffs na cadencia de quinta.
- `design-critique-loop.md` — Critique pre-handoff.
- `design-debt-reduction-sprint.md` — P3 alimentam backlog de divida.
