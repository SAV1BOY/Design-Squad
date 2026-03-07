# Phase: Prioritization

## Objective

Priorizar findings da auditoria para criacao de plano de acao executavel, equilibrando impacto no usuario com esforco de implementacao.

## Inputs

- Findings report completo (02-findings.md)
- Estimativas de esforco do Engineering
- Roadmap de produto e prioridades de negocio
- Metricas de impacto por area

## Activities

### 1. Impact Assessment
Para cada finding: quantificar usuarios afetados, frequencia do problema, impacto na tarefa (bloqueia, dificulta, incomoda), risco legal (a11y compliance).

### 2. Effort Estimation
Workshop com Engineering para estimar esforco: small (< 1 dia), medium (1-3 dias), large (3+ dias). Mapear dependencias entre fixes.

### 3. Priority Matrix
Plotar findings em matriz Impact x Effort. Classificar em: Quick Wins (alto impacto, baixo esforco), Strategic (alto impacto, alto esforco), Fill-ins (baixo impacto, baixo esforco), Deprioritize (baixo impacto, alto esforco).

### 4. Phased Plan
Organizar em phases: Phase 1 (quick wins, 2 semanas), Phase 2 (strategic items, 4-6 semanas), Phase 3 (remaining items, ongoing).

## Output

- Priority matrix documentada
- Phased action plan com timeline
- Jira epics/tickets criados
- Resource allocation definida
- Stakeholder sign-off

## Next Phase

→ `04-plan.md` — Plano de Execucao
