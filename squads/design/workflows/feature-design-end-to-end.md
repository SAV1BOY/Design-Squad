# Feature Design End-to-End

## Metadata

| Campo         | Valor                                   |
| ------------- | --------------------------------------- |
| squad         | Design                                  |
| versao        | 1.0.0                                   |
| criado_em     | 2026-03-06                              |
| owner         | Design Lead                             |
| cadencia      | Por feature request                     |
| duracao_media | 2-4 sprints                             |
| tags          | feature, end-to-end, discovery, handoff |

## Trigger

Quando iniciar:

- Nova feature aprovada no roadmap do produto.
- PM abre epic com requisitos iniciais definidos.
- Demanda cross-squad com impacto em UX confirmado.

Pre-condicoes: epic criado com problema e hipotese documentados; dados de contexto disponiveis; designer responsavel alocado.

## Phases

### Fase 1 — Discovery
**Agents:** Designer, UX Researcher, PM.
**Inputs:** Brief (epic link), analytics, feedback qualitativo.
**Atividades:** Desk research e benchmarks; stakeholder interviews (min 2); mapear JTBD ou Opportunity Solution Tree; documentar assumptions e riscos.
**Outputs:** Discovery brief (1-2 pags), lista de assumptions priorizada, metricas de sucesso definidas.

### Fase 2 — UX Design
**Agents:** Designer, Researcher (consultivo).
**Inputs:** Discovery brief, personas, DS tokens e patterns.
**Atividades:** Gerar min 3 alternativas de fluxo (wireframes); mapear edge cases e estados de erro; validar com PM e Tech Lead.
**Outputs:** Wireframes aprovados (Figma), mapa de fluxo com edge cases, lista de micro-interacoes.

### Fase 3 — UI Design
**Agents:** Designer, DS maintainer (consultivo).
**Inputs:** Wireframes aprovados, design tokens, brand guidelines.
**Atividades:** Aplicar visual usando componentes DS; criar variantes responsivas; definir motion specs; revisar consistencia com DS.
**Outputs:** Mockups high-fidelity (todos os breakpoints), motion specs, redlines de custom elements.

### Fase 4 — Prototipo Interativo
**Agents:** Designer.
**Inputs:** Mockups high-fidelity, motion specs.
**Atividades:** Montar prototipo navegavel (happy path + 1 fluxo alternativo); guerrilla test com 2-3 colegas.
**Outputs:** Link do prototipo compartilhavel, anotacoes de ajustes.

### Fase 5 — Handoff
**Agents:** Designer, Tech Lead, Frontend Engineer.
**Inputs:** Prototipo final, specs, tokens mapeados.
**Atividades:** Sessao de handoff (45-60 min); documentar decisoes no Figma; criar acceptance criteria visuais; exportar assets.
**Outputs:** Handoff page no Figma, acceptance criteria na story, canal de duvidas definido.

### Fase 6 — QA Visual
**Agents:** Designer, QA Engineer.
**Inputs:** Build em staging, acceptance criteria, prototipo como ref.
**Atividades:** Pixel-level review por breakpoint; testar estados (loading, empty, error); spot-check a11y; registrar bugs com screenshots.
**Outputs:** Bugs visuais priorizados (P1-P3), sign-off do designer, retro de handoff.

## Quality Gates

### Gate Discovery -> UX
- [ ] Discovery brief revisado pelo PM.
- [ ] Metricas de sucesso definidas.
- [ ] Assumptions documentadas.

### Gate UX -> UI
- [ ] Wireframes aprovados por PM e Tech Lead.
- [ ] Viabilidade tecnica confirmada.

### Gate UI -> Prototipo
- [ ] Mockups revisados pelo DS maintainer.
- [ ] Responsividade coberta.

### Gate Prototipo -> Handoff
- [ ] Teste interno realizado (min 2 participantes).
- [ ] Prototipo cobre happy path + alternativo.

### Gate Handoff -> QA
- [ ] Sessao de handoff realizada.
- [ ] Acceptance criteria na story.

### Gate QA -> Release
- [ ] Bugs P1 resolvidos, sign-off registrado.

## Cross-References

- `design-system-bootstrap.md` — Tokens e componentes usados na Fase 3.
- `handoff-and-build-loop.md` — Detalha o loop Handoff -> Build -> QA.
- `usability-testing-sprint.md` — Acionado apos Fase 4.
- `design-critique-loop.md` — Aplicavel em qualquer fase.
- `accessibility-remediation-loop.md` — Complementa a11y na Fase 6.
- `design-to-code-sync.md` — Sincronizacao de tokens.
