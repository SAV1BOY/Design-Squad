# A11y Integration Workflow

## Metadata

| Campo         | Valor                                       |
| ------------- | ------------------------------------------- |
| squad         | Design                                      |
| versao        | 1.0.0                                       |
| criado_em     | 2026-03-06                                  |
| owner         | A11y Champion (Design)                      |
| cadencia      | Continuo (integrado a cada feature)         |
| duracao_media | Atividade continua (nao sprint isolado)     |
| tags          | a11y, accessibility, integrado, shift-left  |

## Trigger

Quando iniciar: **sempre**. Este workflow eh o estado padrao — a11y como parte de cada feature, nao bolt-on. Diferente do `accessibility-remediation-loop.md` (remediacao), este trata prevencao.

Pre-condicoes: WCAG 2.2 AA como target; A11y Champion identificado; designers treinados em fundamentos; checklist integrado aos workflows.

## Phases

### Fase 1 — A11y na Discovery
**Agents:** Designer, Researcher.
**Inputs:** Brief, personas (incluindo com deficiencia), dados de a11y.
**Atividades:** Considerar diversidade (visual: cegueira, baixa visao, daltonismo; motora: keyboard-only, switch; auditiva; cognitiva: TDAH, dislexia; situacional: sol forte, uma mao); incluir min 1 participante com deficiencia em pesquisa (quando possivel); documentar requisitos e riscos de a11y.
**Outputs:** Requisitos de a11y no brief, riscos identificados, inclusao planejada.

### Fase 2 — A11y no Design (UX/UI)
**Agents:** Designer, A11y Champion (consultivo).
**Inputs:** Wireframes/mockups, WCAG checklist, DS.
**Atividades:** **Estrutura:** heading hierarchy (h1-h6) semantica; tab order logico; skip links; landmarks (main, nav, aside). **Visual:** contraste min 4.5:1 texto / 3:1 UI elements; nao depender so de cor; touch targets min 44x44px; zoom 200% sem quebra. **Interacao:** keyboard access em tudo; focus states visiveis; focus trapping em modais; timeouts generosos. **Conteudo:** alt text funcional; labels em inputs; erros associados ao campo; copy claro. **Motion:** respeitar `prefers-reduced-motion`; nada piscando > 3x/seg; fallback estatico. **Anotar no Figma:** heading levels, tab order, ARIA labels, alt text.
**Outputs:** Design com a11y integrada, anotacoes no Figma, checklist preenchido.

### Fase 3 — A11y no Handoff
**Agents:** Designer, Frontend Engineer.
**Inputs:** Design com anotacoes, checklist.
**Atividades:** Incluir na sessao de handoff: heading hierarchy, tab order, ARIA labels/roles, alt text, keyboard patterns; referenciar componentes DS (a11y built-in); especificar screen reader behavior; acceptance criteria de a11y na story ("Navegavel por keyboard", "Screen reader anuncia X").
**Outputs:** Handoff com specs a11y, acceptance criteria na story.

### Fase 4 — A11y no Build
**Agents:** Frontend Engineer, A11y Champion (consultivo).
**Inputs:** Specs a11y, DS acessivel, acceptance criteria.
**Atividades:** HTML semantico (nao div soup); componentes DS com ARIA built-in; ARIA adicional apenas onde semantico nao basta; focus management; axe-core durante dev; keyboard test local; testes automatizados (jest-axe/cypress-axe).
**Outputs:** Build com a11y, testes passando, self-check de keyboard e screen reader.

### Fase 5 — A11y no QA
**Agents:** Designer, QA, A11y Champion.
**Inputs:** Build em staging, acceptance criteria, WCAG checklist.
**Atividades:** **Automatizado:** axe-core zero violations. **Keyboard:** tab through pagina, focus order logico, focus visible, sem traps. **Screen reader:** VoiceOver/NVDA, navegar por headings/landmarks, executar tarefas. **Visual:** zoom 200% sem quebra, high contrast mode, contraste em todos os estados. Registrar issues com criterio WCAG.
**Outputs:** Resultado QA a11y, issues registrados, sign-off.

## Quality Gates

### Gate Discovery
- [ ] Requisitos a11y no brief.
- [ ] Diversidade considerada.

### Gate Design
- [ ] Heading hierarchy definida.
- [ ] Contraste verificado (4.5:1 / 3:1).
- [ ] Touch targets >= 44x44px.
- [ ] Focus states definidos.
- [ ] Anotacoes a11y no Figma.

### Gate Handoff
- [ ] Specs a11y incluidos.
- [ ] Acceptance criteria na story.

### Gate Build
- [ ] HTML semantico.
- [ ] Testes a11y passando.
- [ ] Focus management implementado.

### Gate QA
- [ ] axe-core zero violations.
- [ ] Keyboard funcional.
- [ ] Screen reader correto.
- [ ] Zoom 200% sem quebra.

## Cross-References

- `accessibility-remediation-loop.md` — Remediacao quando issues escapam.
- `feature-design-end-to-end.md` — Integra-se a cada fase do pipeline.
- `handoff-and-build-loop.md` — Handoff inclui specs a11y.
- `design-system-component-lifecycle.md` — DS com a11y built-in.
- `design-to-code-sync.md` — Tokens a11y sincronizados.
- `new-designer-onboarding.md` — Treinamento a11y no onboarding.
- `usability-testing-sprint.md` — Incluir usuarios com deficiencia.
