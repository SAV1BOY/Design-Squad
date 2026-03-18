# Connection Matrix — Design Squad

> Mapa completo de conexoes entre todos os elementos operacionais do squad.
> Cada celula indica a relacao entre dois tipos de asset.
> Atualizado: 2026-03-18

---

## 1. Agent ↔ Task Matrix

Qual agent participa de qual task e com qual papel.

| Task | design-chief | ux-design-expert | jessica-ux-ui | design-system-architect | brad-frost | dan-mall | dave-malouf | nano-banana |
|------|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| problem-definition | A | E | - | - | - | - | V | - |
| competitive-ui-audit | - | R | E | - | - | - | - | - |
| design-audit-existing-product | A | - | E | - | V | - | - | - |
| plan-and-run-interviews | - | E | - | - | - | - | V | - |
| run-usability-test | - | E | S | - | - | - | - | - |
| run-card-sort | - | E | - | - | - | - | - | - |
| synthesize-insights | A | E | - | - | - | - | - | - |
| build-ia-and-sitemap | - | E | S | - | - | - | - | - |
| design-user-flows | - | E | S | - | - | - | - | - |
| create-personas-or-jtbd | - | E | - | - | - | - | V | - |
| create-journey-map | - | E | S | - | - | - | - | - |
| wireframe-pack | - | R | E | - | - | - | - | - |
| ui-design-high-fidelity | - | - | E | R | - | - | - | - |
| build-prototype | - | R | E | - | - | - | - | - |
| design-motion-specs | - | - | E | R | - | - | - | - |
| content-design-microcopy | - | E | S | - | - | - | - | - |
| create-visual-explorations | - | - | C | - | - | - | - | E |
| design-system-bootstrap | - | - | - | E | A | S | - | - |
| create-component-spec | - | - | - | E | R | - | - | - |
| create-or-update-tokens | - | - | - | E | R | - | - | - |
| publish-library | A | - | - | E | - | - | - | - |
| ds-health-check | - | - | - | E | V | V | - | - |
| a11y-audit | - | E | - | S | - | - | - | - |
| remediate-and-verify | - | - | E | V | - | - | - | - |
| dev-handoff | A | - | E | R | - | - | - | - |
| qa-with-engineering | A | - | E | - | - | - | - | - |
| post-release-review | A | E | - | - | - | V | - | - |
| design-critique-session | R | - | - | - | - | F | V | - |
| quarterly-design-review | E | - | - | - | V | V | V | - |
| design-debt-prioritization | A | - | - | E | - | V | - | - |

**Legenda:** E = Executor | A = Approver | R = Reviewer | V = Advisor | S = Support | F = Facilitator | C = Curator

---

## 2. Task ↔ Framework Matrix

Qual framework e obrigatorio (M) ou opcional (O) para qual task.

| Framework | Discovery Tasks | Research Tasks | IA Tasks | UX Tasks | UI Tasks | DS Tasks | A11y Tasks | Handoff/QA | Governance |
|-----------|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| discovery-layer | M | - | - | - | - | - | - | - | - |
| strategy-layer | - | - | - | - | - | - | - | - | - |
| ux-layer | - | - | - | M | - | - | - | - | - |
| ui-layer | - | - | - | - | M | - | - | - | - |
| design-system-layer | - | - | - | - | - | M | - | - | - |
| prototyping-layer | - | - | - | - | M | - | - | - | - |
| handoff-layer | - | - | - | - | - | - | - | M | - |
| governance-layer | - | - | - | - | - | - | - | - | M |
| competitive-audit-framework | M | - | - | - | - | - | - | - | - |
| usability-testing-framework | - | M | - | - | - | - | - | - | - |
| information-architecture-toolkit | - | - | M | - | - | - | - | - | - |
| user-journey-mapping | - | - | M | - | - | - | - | - | - |
| accessibility-wcag-aa | - | - | - | - | - | - | M | - | - |
| design-token-architecture | - | - | - | - | - | M | - | - | - |
| design-review-and-critique | - | - | - | - | - | - | - | - | M |
| design-debt-management | - | - | - | - | - | - | - | - | M |
| nielsen-heuristics | O | - | - | - | - | - | - | - | - |
| heart-metrics-framework | - | - | - | - | - | - | - | - | O |

---

## 3. Task ↔ Checklist Matrix

Qual checklist valida qual task.

| Checklist | Applies To |
|-----------|-----------|
| discovery-brief-quality | problem-definition, design-audit-existing-product |
| ux-audit-quality | competitive-ui-audit, design-audit-existing-product |
| interview-guide-quality | plan-and-run-interviews |
| usability-test-quality | run-usability-test |
| research-plan-quality | run-card-sort |
| synthesis-quality | synthesize-insights |
| ia-and-navigation-quality | build-ia-and-sitemap |
| user-flow-quality | design-user-flows |
| persona-quality | create-personas-or-jtbd |
| journey-map-quality | create-journey-map |
| wireframe-quality | wireframe-pack |
| ui-visual-quality | ui-design-high-fidelity, create-visual-explorations |
| prototyping-quality | build-prototype |
| motion-quality | design-motion-specs |
| content-design-quality | content-design-microcopy |
| design-system-quality | design-system-bootstrap, publish-library, ds-health-check |
| component-spec-quality | create-component-spec |
| token-quality | create-or-update-tokens |
| accessibility-quality | a11y-audit, remediate-and-verify |
| handoff-quality | dev-handoff, qa-with-engineering |
| design-critique-quality | design-critique-session |
| design-debt-quality | design-debt-prioritization |

---

## 4. Task ↔ Template Matrix

Qual template e gerado por qual task.

| Template | Generated By |
|----------|-------------|
| briefs/discovery-brief | problem-definition |
| research/competitive-analysis-template | competitive-ui-audit |
| reports/ux-audit-report-template | design-audit-existing-product |
| research/interview-script-template | plan-and-run-interviews |
| research/interview-notes-template | plan-and-run-interviews |
| research/usability-test-plan | run-usability-test |
| reports/usability-test-report-template | run-usability-test |
| research/card-sort-template | run-card-sort |
| research/insights-and-opportunities-template | synthesize-insights |
| ux/ia-sitemap-template | build-ia-and-sitemap |
| ux/user-flow-template | design-user-flows |
| ux/persona-template | create-personas-or-jtbd |
| ux/jtbd-template | create-personas-or-jtbd |
| ux/journey-map-template | create-journey-map |
| ui/wireframe-pack-template | wireframe-pack |
| ui/ui-style-sheet-template | ui-design-high-fidelity |
| ui/motion-spec-template | design-motion-specs |
| ui/component-spec-template | create-component-spec |
| design-system/token-spec-template | create-or-update-tokens |
| design-system/component-rfc-template | design-system-bootstrap |
| design-system/ds-health-report-template | ds-health-check |
| handoff/release-notes-template | publish-library |
| reports/a11y-audit-report-template | a11y-audit |
| handoff/dev-handoff-checklist-template | dev-handoff |
| handoff/qa-bug-template | qa-with-engineering |
| reports/design-review-report-template | post-release-review, design-critique-session |
| reports/quarterly-design-report | quarterly-design-review |
| reports/design-debt-report-template | design-debt-prioritization |

---

## 5. Task ↔ Registry Matrix

Qual registry e atualizado por qual task.

| Registry | Updated By |
|----------|-----------|
| discovery-registry | problem-definition |
| research-insights-registry | competitive-ui-audit, design-audit, plan-and-run-interviews, run-usability-test, run-card-sort, synthesize-insights, create-personas-or-jtbd, create-journey-map |
| design-artifact-registry | build-ia-and-sitemap, design-user-flows, wireframe-pack, ui-design-high-fidelity, build-prototype, design-motion-specs, create-visual-explorations |
| components-registry | design-system-bootstrap, create-component-spec, publish-library, ds-health-check |
| tokens-registry | create-or-update-tokens |
| accessibility-issues-registry | a11y-audit, remediate-and-verify |
| content-registry | content-design-microcopy |
| handoff-registry | dev-handoff |
| qa-registry | qa-with-engineering |
| governance-registry | post-release-review, design-critique-session, quarterly-design-review, design-debt-prioritization |
| decisions-log | (any significant decision across any task) |
| design-debt-registry | design-debt-prioritization, ds-health-check |
| lessons-learned-registry | quarterly-design-review, post-release-review |

---

## 6. Cross-Squad Integration Matrix

| Squad | Design Sends | Design Receives | Contract |
|-------|-------------|----------------|----------|
| Copy Squad | contexto-de-tela, fluxo-do-usuario, wireframe-com-placeholder | tom-de-voz-guidelines, glossario, microcopy | `workflows/handoff-contract-copy-squad` |
| Brand Squad | aplicacoes-de-marca, extensoes-de-paleta, novos-icones | brand-guidelines, paleta, tipografia, iconografia | `workflows/handoff-contract-brand-squad` |
| Traffic Squad | hipoteses-de-design, variantes-ab, tracking-requirements | dados-comportamento, funis, heatmaps, metricas | `workflows/handoff-contract-traffic-squad` |
| Storytelling Squad | storyboard, prototipos-narrativa, assets-case-study | narrativa-produto, scripts-onboarding, arcos-experiencia | `workflows/handoff-contract-storytelling-squad` |

---

## 7. Quality Gate Cascade Matrix

| Gate Level | Owner | Applies To | Can Override? |
|-----------|-------|-----------|---------------|
| Agent Gate | Agent executor | Cada entregavel individual | Sim (pelo reviewer) |
| Inter-Agent Transition | Agent receptor | ux→ui, ui→ds, ds→handoff | Sim (pelo design-chief) |
| Domain Gate | Especialista | Tasks do dominio | Sim (design-chief com justificativa) |
| Mandatory Gate | design-chief | Todas as tasks | **NAO** |
| Chief Approval | design-chief | Output final do squad | Apenas HRM Layer |
| Cross-Squad Gate | Squad receptor | Handoffs entre squads | Nao (devolve) |

---

*Cross-references:*
- `config.yaml` — Routing e quality gates definitivos
- `ARCHITECTURE.md` — Arquitetura e fluxos
- `docs/quality-gate-cascade.md` — Logica detalhada dos gates
- `docs/escalation-protocol.md` — Protocolo de escalacao
