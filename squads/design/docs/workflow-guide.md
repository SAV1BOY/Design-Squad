# Workflow Guide

## Overview

Guia do fluxo de trabalho do Design Squad — do recebimento de uma demanda até a
validação pós-lançamento. Define etapas, gates de qualidade, responsáveis e
artefatos esperados em cada fase.

## Content

### Visão Geral do Fluxo

```
Request → Discovery → Definition → Design → Review → Handoff → QA → Launch → Learn
```

### Fase 1: Request
**Duração:** 1-2 dias
**Responsável:** PM + Design Lead

- PM submete request com contexto de negócio e requisitos
- Design Lead avalia escopo, prioridade e aloca designer
- Kickoff de 30 min: PM + Designer + Dev Lead

**Gate:** Request tem problema claro, público definido e métrica de sucesso

### Fase 2: Discovery
**Duração:** 2-5 dias (dependendo da complexidade)
**Responsável:** Product Designer + UX Researcher

- Review de dados existentes (analytics, suporte, pesquisas anteriores)
- Benchmark de concorrentes e referências
- Pesquisa com usuários (se necessário e tempo permite)
- Síntese de insights e definição de oportunidades

**Gate:** Insights documentados, oportunidade de design definida
**Artefatos:** Research brief, competitive analysis, opportunity statement

### Fase 3: Definition
**Duração:** 2-3 dias
**Responsável:** Product Designer

- Fluxos de usuário e information architecture
- Wireframes low-fi para validação de estrutura
- Definição de escopo com PM (in/out)
- Alinhamento técnico com engenharia (viabilidade)

**Gate:** Fluxo aprovado por PM, viabilidade confirmada por dev
**Artefatos:** User flows, wireframes, scope document

### Fase 4: Design
**Duração:** 3-5 dias
**Responsável:** Product Designer + UX Writer

- Mockups hi-fi usando design system
- Todos os estados (default, hover, error, empty, loading)
- Responsivo (mobile, tablet, desktop)
- Microcopy integrada
- Protótipo interativo para fluxos complexos

**Gate:** Design critique com feedback incorporado
**Artefatos:** Mockups, protótipos, microcopy document

### Fase 5: Review
**Duração:** 1-2 dias
**Responsável:** Design Squad + Stakeholders

- Design review com PM e engenharia
- A11y review
- DS consistency check
- Feedback incorporado, versão final aprovada

**Gate:** Aprovação de PM, design lead e a11y reviewer
**Artefatos:** Review notes, versão final aprovada

### Fase 6: Handoff
**Duração:** 1 dia
**Responsável:** Product Designer

- Figma organizado no padrão de handoff
- Token reference table completa
- Annotations de comportamento e a11y
- Handoff meeting com dev (30 min walkthrough)
- Ticket(s) criados/atualizados

**Gate:** Dev confirma que tem todas as informações necessárias
**Artefatos:** Figma handoff, tickets, handoff notes

### Fase 7: QA Visual
**Duração:** Durante o sprint de desenvolvimento
**Responsável:** Product Designer + QA

- Review visual durante implementação (não esperar o final)
- Bug visual reportado com severidade e fix sugerido
- Aprovação final antes de merge para produção

**Gate:** Zero blockers visuais, zero critical a11y issues
**Artefatos:** QA report, bug tickets (se houver)

### Fase 8: Launch
**Responsável:** PM + Todo o squad

- Feature flag para rollout gradual quando aplicável
- Monitoramento de métricas nas primeiras 48h
- Hotfix de design se necessário

### Fase 9: Learn
**Duração:** 1-4 semanas pós-launch
**Responsável:** Product Designer + UX Researcher

- Análise de métricas de sucesso definidas na request
- Feedback qualitativo (suporte, app store, pesquisa)
- Documentação de learnings
- Input para próxima iteração

**Artefatos:** Post-launch report, learnings document

### Estimativas por Complexidade

| Complexidade | Discovery | Definition | Design | Review+Handoff | Total |
|-------------|-----------|------------|--------|----------------|-------|
| Pequena | 1d | 1d | 2d | 1d | 5d |
| Média | 3d | 2d | 4d | 2d | 11d |
| Grande | 5d | 3d | 5d | 2d | 15d |
| Épico | 10d+ | 5d+ | 10d+ | 3d+ | 28d+ |

## Cross-References

- `docs/operating-system.md` — Cadências e rituais
- `docs/design-review-standards.md` — Detalhamento da fase de review
- `docs/handoff-standards.md` — Detalhamento da fase de handoff
- `docs/research-standards.md` — Detalhamento da fase de discovery
