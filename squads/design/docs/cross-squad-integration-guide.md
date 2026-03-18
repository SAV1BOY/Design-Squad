# Cross-Squad Integration Guide

## Overview

Guia operacional para integracao do Design Squad com os **11 squads do ecossistema MMOS**.
Cada integracao possui handoff contract formal, quality gates bidirecionais e SLAs definidos.
Este guia serve como indice de navegacao — os contratos detalhados estao em `workflows/`.

---

## Integration Tiers

As integracoes sao organizadas por frequencia de interacao:

| Tier | Frequencia | Squads |
|------|-----------|--------|
| **Tier 1** | Diaria/Semanal | Copy, Brand, Pre-Programming, Data |
| **Tier 2** | Por Sprint | Traffic, Storytelling, Deep Research |
| **Tier 3** | Mensal/Trimestral | Cybersecurity, C-Level, Advisory Board, Movement |

---

## Tier 1 — Integracao Diaria/Semanal

### Copy Squad
- **Design envia:** contexto-de-tela, fluxo-do-usuario, wireframe-com-placeholder
- **Design recebe:** tom-de-voz-guidelines, glossario-de-produto, microcopy-aprovado
- **Shared:** brand-voice-tokens, content-patterns
- **Contract:** `workflows/handoff-contract-copy-squad.md`
- **Gate on send:** Validar que contexto de tela inclui user flow completo
- **Gate on receive:** Validar que guidelines de voz estao atualizadas

### Brand Squad
- **Design envia:** aplicacoes-de-marca-em-produto, extensoes-de-paleta-para-ui, proposta-de-novos-icones
- **Design recebe:** brand-guidelines, paleta-de-cores, tipografia-aprovada, iconografia-base
- **Shared:** color-tokens, typography-tokens, logo-assets
- **Contract:** `workflows/handoff-contract-brand-squad.md`
- **Gate on send:** Validar que extensoes de paleta mantem harmonia com brand
- **Gate on receive:** Validar que brand assets seguem formato e resolucao padrao

### Pre-Programming Squad
- **Design envia:** design-specs, component-specs, token-specs, interaction-specs, asset-package
- **Design recebe:** technical-constraints, api-capabilities, platform-limitations, performance-budgets
- **Shared:** component-api-contracts, design-token-files
- **Contract:** `workflows/handoff-contract-pre-programming-squad.md`
- **Gate on send:** Validar que specs cobrem todos os estados, breakpoints e edge cases
- **Gate on receive:** Validar que constraints tecnicas estao documentadas com alternativas

### Data Squad
- **Design envia:** tracking-requirements, event-specs, metrics-definitions, experiment-hypotheses
- **Design recebe:** analytics-reports, funnel-data, user-behavior-metrics, ab-test-results
- **Shared:** event-taxonomy, metrics-dashboard-templates
- **Contract:** `workflows/handoff-contract-data-squad.md`
- **Gate on send:** Validar que tracking specs cobrem todos os fluxos e estados criticos
- **Gate on receive:** Validar que dados tem sample size e periodo adequados para decisao

---

## Tier 2 — Integracao por Sprint

### Traffic Squad
- **Design envia:** hipoteses-de-design, variantes-para-ab-test, tracking-requirements
- **Design recebe:** dados-de-comportamento, funis-de-conversao, heatmaps, metricas-de-engajamento
- **Shared:** event-taxonomy, funnel-definitions
- **Contract:** `workflows/handoff-contract-traffic-squad.md`
- **Gate on send:** Validar que variantes tem specs completas para implementacao
- **Gate on receive:** Validar que dados tem sample size minimo para decisao

### Storytelling Squad
- **Design envia:** storyboard-visual, prototipos-de-narrativa, assets-para-case-study
- **Design recebe:** narrativa-de-produto, scripts-de-onboarding, arcos-de-experiencia
- **Shared:** illustration-library, animation-assets
- **Contract:** `workflows/handoff-contract-storytelling-squad.md`
- **Gate on send:** Validar que storyboard segue brand guidelines
- **Gate on receive:** Validar que narrativa esta alinhada com pesquisa de usuario

### Deep Research Squad
- **Design envia:** research-questions, hypothesis-list, specific-inquiry-briefs
- **Design recebe:** research-briefs, market-analysis, user-behavior-reports, competitive-intelligence
- **Shared:** research-repository, insight-registry
- **Contract:** `workflows/handoff-contract-deepresearch-squad.md`
- **Gate on send:** Validar que perguntas de pesquisa sao especificas e acionaveis
- **Gate on receive:** Validar que pesquisa tem metodologia clara e fontes documentadas

---

## Tier 3 — Integracao Mensal/Trimestral

### Cybersecurity Squad
- **Design envia:** security-ux-review, auth-flow-designs, privacy-ux-patterns, consent-flows
- **Design recebe:** security-requirements, compliance-constraints, vulnerability-reports, auth-patterns
- **Shared:** auth-pattern-library, privacy-consent-templates
- **Contract:** `workflows/handoff-contract-cybersecurity-squad.md`
- **Gate on send:** Validar que fluxos de auth cobrem todos os cenarios de erro e recuperacao
- **Gate on receive:** Validar que requisitos incluem nivel de risco e prioridade

### C-Level Squad
- **Design envia:** design-impact-report, quarterly-metrics, maturity-assessment, investment-proposals
- **Design recebe:** strategic-direction, product-vision, okrs, budget-constraints
- **Shared:** quarterly-reports, design-maturity-scorecard
- **Contract:** `workflows/handoff-contract-c-level-squad.md`
- **Gate on send:** Validar que reports incluem metricas quantitativas e recomendacoes acionaveis
- **Gate on receive:** Validar que direcao estrategica tem KPIs mensuraveis e timeline

### Advisory Board Squad
- **Design envia:** quarterly-scorecard, maturity-evolution, risk-assessments
- **Design recebe:** governance-guidelines, industry-benchmarks, organizational-standards
- **Shared:** governance-framework, maturity-model
- **Contract:** `workflows/handoff-contract-advisory-board-squad.md`
- **Gate on send:** Validar que scorecards refletem dados reais do periodo com evidencias
- **Gate on receive:** Validar que guidelines tem criterios verificaveis e aplicaveis

### Movement Squad
- **Design envia:** visual-identity-alignment, brand-expression-in-product, community-ux-patterns
- **Design recebe:** cultural-context, community-insights, movement-identity, audience-profiles
- **Shared:** cultural-design-tokens, community-pattern-library
- **Contract:** `workflows/handoff-contract-movement-squad.md`
- **Gate on send:** Validar que alinhamento visual respeita guidelines de marca e cultura
- **Gate on receive:** Validar que contexto cultural tem fontes e validacao com comunidade

---

## Modelo de Atendimento

O Design Squad opera em modelo **embedded + centralized**:
- Designers sao alocados a squads de produto (embedded) para proximidade
- Mas pertencem ao Design Squad (centralized) para consistencia e desenvolvimento

**Proporcao:** 1 designer para cada 1-2 squads de produto (dependendo da complexidade)

### Como solicitar design
1. Squad solicitante cria request no board compartilhado com template preenchido
2. Design Lead avalia prioridade e aloca designer em ate 2 dias uteis
3. Kickoff de alinhamento (30 min) entre leads
4. Designer segue o workflow padrao (ver `docs/workflow-guide.md`)

### SLAs de Atendimento

| Prioridade | Inicio do trabalho | Entrega estimada |
|-----------|-------------------|-----------------|
| P0 (Critico) | Mesmo dia | 1-2 dias |
| P1 (Urgente) | 1-2 dias | 3-5 dias |
| P2 (Normal) | 3-5 dias | 1-2 sprints |
| P3 (Nice-to-have) | Proximo sprint | 2-3 sprints |

---

## Resolucao de Conflitos

| Conflito | Quem resolve |
|----------|-------------|
| Prioridade entre squads | Design Chief + PM Lead |
| Escopo de design vs. prazo | PM do squad + Designer |
| Padrao de DS vs. necessidade do squad | DS Committee |
| Qualidade vs. velocidade | Design Chief tem ultima palavra em qualidade |
| Conflito cross-squad nao resolvido em 5 dias | Escalar para HRM Chief |

---

## Communication Channels

| Tipo de comunicacao | Canal |
|--------------------|-------|
| Request de design | Board compartilhado (Jira/Linear) |
| Updates de progresso | Slack canal do squad |
| Feedback de implementacao | Slack + Figma comments |
| Escalacao | DM com Design Chief |
| Design system questions | #design-system |
| Cross-squad sync | Reuniao biweekly (ver config.yaml cadence) |

---

## Cross-References

- `config.yaml` — Routing e cross_squad integration entries
- `ARCHITECTURE.md` — Secao 7: Cross-Squad Integration
- `docs/squad-overview.md` — Estrutura do Design Squad
- `docs/workflow-guide.md` — Fluxo de trabalho
- `docs/handoff-standards.md` — Padroes de entrega
- `docs/escalation-protocol.md` — Protocolo de escalacao
- `docs/delegation-protocol.md` — Protocolo de delegacao
- `voice/language-guides/stakeholder-communication.md` — Comunicacao com stakeholders
- `workflows/cross-squad-handoff-protocol.md` — Protocolo generico de handoff
