# Accessibility Remediation Loop

## Metadata

| Campo         | Valor                                     |
| ------------- | ----------------------------------------- |
| squad         | Design                                    |
| versao        | 1.0.0                                     |
| criado_em     | 2026-03-06                                |
| owner         | A11y Champion (Design)                    |
| cadencia      | Continuo (triggered por audit ou report)  |
| duracao_media | 1-3 sprints por ciclo                     |
| tags          | accessibility, a11y, WCAG, remediation    |

## Trigger

Quando iniciar:

- Audit de acessibilidade programado (trimestral recomendado).
- Report de usuario sobre barreira de acessibilidade.
- Resultado de teste automatizado abaixo do threshold (axe, Lighthouse).
- Nova regulamentacao ou requisito legal de a11y.

Pre-condicoes: WCAG target definido (2.2 AA minimo); ferramentas configuradas (axe-core, Lighthouse); A11y Champion identificado; baseline documentado.

## Phases

### Fase 1 — Audit
**Agents:** A11y Champion, Designer, Frontend Engineer.
**Inputs:** Produto em producao/staging, WCAG 2.2 checklist, ferramentas automatizadas, baseline anterior.
**Atividades:** Scan automatizado (axe-core, Lighthouse); teste manual de keyboard (tab order, focus, traps); teste com screen reader (NVDA/VoiceOver); color contrast em todos os estados; verificar `prefers-reduced-motion`; testar zoom 200%; documentar issues com criterio WCAG, severidade, localizacao, screenshot.
**Outputs:** Relatorio completo, score atualizado, issues no tracker, comparacao com baseline.

### Fase 2 — Fix
**Agents:** Designer, Frontend Engineer, A11y Champion (consultivo).
**Inputs:** Relatorio priorizado, WCAG criteria, DS components.
**Atividades:** Priorizar (critico > maior > menor); ajustar design (cores, contraste, sizing, touch targets); corrigir codigo (semantics, ARIA, focus management, alt text); escalar issues de DS ao maintainer; adicionar testes automatizados (jest-axe, cypress-axe); documentar rationale.
**Outputs:** Fixes em design e codigo, testes adicionados, PRs abertos, issues DS escalados.

### Fase 3 — Verify
**Agents:** A11y Champion, QA, Designer.
**Inputs:** Fixes em staging, criterios WCAG originais, testes automatizados.
**Atividades:** Re-testar cada issue contra criterio original; scan automatizado pos-fix; teste manual keyboard e screen reader; verificar ausencia de regressoes; sign-off do A11y Champion.
**Outputs:** Issues verificados e fechados, score pos-remediation, sign-off, issues pendentes documentados.

### Fase 4 — Regression Prevention
**Agents:** A11y Champion, Frontend Engineer, Design Lead.
**Inputs:** Issues corrigidos, testes implementados, patterns recorrentes.
**Atividades:** Adicionar a11y checks ao CI/CD (axe-core no PR); atualizar checklist de handoff; criar/atualizar guidelines de a11y para designers; agendar proximo audit; knowledge sharing com squad; atualizar baseline.
**Outputs:** CI/CD checks configurados, checklist atualizado, guidelines atualizadas, proximo audit agendado.

## Quality Gates

### Gate Audit -> Fix
- [ ] Issues documentados com criterio WCAG e severidade.
- [ ] Issues no tracker com labels.
- [ ] Priorizacao acordada com PM.

### Gate Fix -> Verify
- [ ] Issues criticos corrigidos.
- [ ] Testes automatizados para cada fix.
- [ ] Issues DS escalados.

### Gate Verify -> Prevention
- [ ] Cada fix re-testado manualmente.
- [ ] Score de a11y melhorou.
- [ ] Sign-off do A11y Champion.

### Gate Prevention -> Proximo Ciclo
- [ ] CI/CD checks operacionais.
- [ ] Baseline atualizado.
- [ ] Proximo audit agendado.

## Cross-References

- `a11y-integration-workflow.md` — A11y integrada ao processo (prevencao).
- `feature-design-end-to-end.md` — Validacao de a11y na Fase 6 (QA).
- `design-system-component-lifecycle.md` — Fixes em componentes DS.
- `handoff-and-build-loop.md` — Checklist de handoff inclui a11y.
- `design-to-code-sync.md` — Tokens de a11y sincronizados.
- `quarterly-design-review.md` — Score revisado trimestralmente.
