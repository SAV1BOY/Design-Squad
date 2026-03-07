# Phase: Remediation

## Objective

Implementar correcoes de acessibilidade seguindo o plano priorizado, com quality gates para prevenir regressoes.

## Inputs

- Remediation plan (02-prioritization.md)
- Jira tickets com acceptance criteria
- Design system resources
- A11y testing tools configurados

## Activities

### 1. Design System Fixes First
Corrigir issues no design system (componentes e tokens) primeiro. Cada fix no DS propaga para todas as instancias automaticamente. Atualizar documentacao de a11y por componente. Adicionar testes automatizados ao componente.

### 2. Page-Level Fixes
Corrigir issues especificos de paginas. Seguir prioridade do remediation plan. Para cada fix: implementar, testar, documentar. Pair com designer para fixes que alteram UX.

### 3. CI Quality Gates
Implementar axe-core como quality gate no CI. PRs com novos a11y issues sao bloqueados automaticamente. Threshold: zero critical/high issues permitidos. Warning para medium/low (nao blocking).

### 4. Education
Conduzir sessao de a11y para todo o time de eng (2h). Criar a11y checklist para PRs. Documentar patterns de a11y mais comuns. Nomear a11y champion por squad.

### 5. Progress Tracking
Dashboard de progresso: issues resolvidos vs total. Compliance score atualizado semanalmente. Report para stakeholders bi-semanal.

## Output

- Issues corrigidos conforme plan
- CI quality gates implementados
- Time educado em a11y basics
- Progress tracked e reportado
- Compliance score melhorado

## Next Phase

→ `04-verification.md` — Verificacao e Validacao
