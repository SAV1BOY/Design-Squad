# Remediation Tracker Template

## Informacoes do Projeto

| Campo | Valor |
|-------|-------|
| **Produto** | [Nome] |
| **a11y Lead** | [Nome] |
| **Data de Inicio** | [YYYY-MM-DD] |
| **Data Prevista de Conclusao** | [YYYY-MM-DD] |
| **Status Geral** | [Em andamento / Concluido] |

## Dashboard de Progresso

### Resumo Geral

| Metrica | Valor |
|---------|-------|
| Total de issues | [N] |
| Issues resolvidos | [N] |
| Issues em andamento | [N] |
| Issues pendentes | [N] |
| % de conclusao | [%] |

### Progresso por Prioridade

| Prioridade | Total | Resolvidos | Em Andamento | Pendentes | % |
|-----------|-------|-----------|-------------|----------|---|
| P0 | [N] | [N] | [N] | [N] | [%] |
| P1 | [N] | [N] | [N] | [N] | [%] |
| P2 | [N] | [N] | [N] | [N] | [%] |
| P3 | [N] | [N] | [N] | [N] | [%] |

### Progresso por WCAG Principle

| Principio | Total | Resolvidos | % |
|-----------|-------|-----------|---|
| Perceivable | [N] | [N] | [%] |
| Operable | [N] | [N] | [%] |
| Understandable | [N] | [N] | [%] |
| Robust | [N] | [N] | [%] |

## Tracker Detalhado

### Sprint [N] — [Data inicio - Data fim]

| ID | WCAG | Descricao | Prioridade | Responsavel | Status | Verificado |
|----|------|-----------|-----------|-------------|--------|-----------|
| FIND-001 | [criterio] | [descricao] | P0 | [nome] | [status] | [ ] |
| FIND-002 | [criterio] | [descricao] | P0 | [nome] | [status] | [ ] |
| FIND-010 | [criterio] | [descricao] | P1 | [nome] | [status] | [ ] |
| FIND-011 | [criterio] | [descricao] | P1 | [nome] | [status] | [ ] |

**Status do sprint**: [N/N] issues resolvidos

### Sprint [N+1] — [Data inicio - Data fim]

| ID | WCAG | Descricao | Prioridade | Responsavel | Status | Verificado |
|----|------|-----------|-----------|-------------|--------|-----------|
| FIND-012 | [criterio] | [descricao] | P1 | [nome] | [status] | [ ] |
| FIND-013 | [criterio] | [descricao] | P2 | [nome] | [status] | [ ] |
| FIND-020 | [criterio] | [descricao] | P2 | [nome] | [status] | [ ] |

**Status do sprint**: [N/N] issues resolvidos

### Sprint [N+2] — [Data inicio - Data fim]

| ID | WCAG | Descricao | Prioridade | Responsavel | Status | Verificado |
|----|------|-----------|-----------|-------------|--------|-----------|
| FIND-021 | [criterio] | [descricao] | P2 | [nome] | [status] | [ ] |
| FIND-022 | [criterio] | [descricao] | P3 | [nome] | [status] | [ ] |

**Status do sprint**: [N/N] issues resolvidos

## Status Legend

| Status | Significado | Icone |
|--------|-----------|-------|
| Pendente | Ainda nao iniciado | ⬜ |
| Em andamento | Sendo trabalhado | 🔵 |
| Em review | PR aberto, aguardando review | 🟡 |
| Verificando | Fix implementado, em verificacao a11y | 🟠 |
| Resolvido | Fix verificado e aprovado | ✅ |
| Bloqueado | Dependencia impede progresso | 🔴 |
| Nao aplicavel | Reavaliado e considerado nao-issue | ⚪ |

## Verificacao de Fixes

Para cada fix implementado, verificar os seguintes itens:

### Checklist de Verificacao

| Item | Como Verificar |
|------|---------------|
| Fix resolve o issue original | Re-testar cenario original |
| Fix nao introduz novos issues | Rodar axe-core na pagina |
| Keyboard navigation funcional | Testar navegacao por teclado |
| Screen reader funcional | Testar com VoiceOver/NVDA |
| Visual regression | Verificar que layout nao quebrou |
| Cross-browser | Testar em Chrome, Firefox, Safari |

### Registro de Verificacao

| ID | Verificador | Data | Metodo | Resultado | Notas |
|----|-----------|------|--------|----------|-------|
| FIND-001 | [nome] | [data] | [manual/automatizado] | [Pass/Fail] | [notas] |
| FIND-002 | [nome] | [data] | [manual/automatizado] | [Pass/Fail] | [notas] |

## Bloqueios e Dependencias

| Issue | Bloqueio | Dependencia | Data Estimada | Status |
|-------|---------|-------------|--------------|--------|
| [ID] | [descricao do bloqueio] | [de quem/o que depende] | [data] | [status] |

## Metricas de Velocidade

### Issues Resolvidos por Sprint


---
