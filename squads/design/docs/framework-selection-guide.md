# Framework Selection Guide

## Overview

Guia para selecionar frameworks, metodologias e abordagens de design adequados a
cada tipo de problema. Não existe framework universal — a escolha depende do contexto,
do problema e das restrições. Este guia mapeia situações comuns a frameworks recomendados.

## Content

### Quando usar o que

#### Discovery e Pesquisa

| Situação | Framework | Por que |
|----------|-----------|--------|
| Não sabemos quem é o usuário | Personas + Jobs to be Done | Combinação de perfil + motivação |
| Não entendemos a jornada | Journey Mapping | Visualiza touchpoints e pain points |
| Precisamos explorar o espaço do problema | Design Thinking (Double Diamond) | Divergência antes de convergência |
| Queremos validar rápido | Lean UX / Build-Measure-Learn | Ciclos curtos de aprendizado |
| Precisamos comparar com mercado | Competitive Analysis Framework | Benchmark estruturado |

#### Ideação e Conceito

| Situação | Framework | Por que |
|----------|-----------|--------|
| Time precisa gerar muitas ideias | Crazy 8s / Design Sprint | Volume de ideias em pouco tempo |
| Problema complexo com múltiplas variáveis | Systems Thinking | Mapeia interdependências |
| Precisamos decidir entre alternativas | Decision Matrix / Trade-off Canvas | Avaliação objetiva multi-critério |
| Queremos inovar na experiência | SCAMPER / How Might We | Provocação criativa estruturada |
| Feature com múltiplos stakeholders | Design Charrette | Co-design com diversidade de perspectivas |

#### Avaliação e Validação

| Situação | Framework | Por que |
|----------|-----------|--------|
| Avaliar interface existente | Heuristic Evaluation (Nielsen) | Rápido, não precisa de usuário |
| Validar usabilidade | Usability Testing (Think Aloud) | Observação direta de comportamento |
| Comparar duas versões | A/B Testing | Dados quantitativos de performance |
| Avaliar arquitetura de informação | Card Sorting / Tree Testing | Valida modelo mental do usuário |
| Avaliar acessibilidade | WCAG Audit + Assistive Tech Testing | Conformidade + experiência real |

#### Estratégia e Priorização

| Situação | Framework | Por que |
|----------|-----------|--------|
| Priorizar backlog de design | RICE / Impact-Effort Matrix | Priorização baseada em dados |
| Definir principles de design | Design Principles Workshop | Co-criação com o time |
| Alinhar visão de produto | North Star Framework | Métrica única que guia decisões |
| Mapear design debt | Design Debt Matrix (severity x effort) | Priorização visual de debt |

### Framework Decision Tree

```
Qual é o problema?
├── Não entendo o problema → Discovery
│   ├── Amplo e vago → Design Thinking / Double Diamond
│   ├── Preciso de dados de usuário → User Research (ver research-standards.md)
│   └── Preciso de dados de mercado → Competitive Analysis
├── Entendo o problema, preciso de solução → Ideação
│   ├── Pouco tempo → Design Sprint (5 dias)
│   ├── Problema sistêmico → Systems Thinking
│   └── Múltiplas opções → Decision Matrix
├── Tenho solução, preciso validar → Validação
│   ├── Sem acesso a usuários → Heuristic Evaluation
│   ├── Qualitativo → Usability Testing
│   └── Quantitativo → A/B Testing
└── Preciso priorizar → Estratégia
    ├── Backlog → RICE ou Impact-Effort
    └── Debt → Design Debt Matrix
```

### Combinações Recomendadas

**Novo produto (0→1):**
Design Thinking → Lean UX → Usability Testing → A/B Testing

**Redesign de feature:**
Heuristic Evaluation → User Research → Ideação → Usability Testing

**Design System evolution:**
Systems Thinking → RFC → Design Review → Beta Testing

**Quick win / bug UX:**
Heuristic Evaluation → Fix → QA Visual

### Anti-patterns

- **Usar Design Sprint para tudo** — É intenso demais para problemas simples
- **Pular Discovery** — "Eu já sei o que o usuário quer" é o viés mais perigoso
- **A/B test sem hipótese** — Testar sem saber o que está testando
- **Framework por moda** — Jobs to be Done não substitui Personas em todos os casos
- **Excesso de frameworks** — 1-2 por fase é suficiente. Mais que isso é paralisia

## Cross-References

- `docs/research-standards.md` — Padrões de pesquisa
- `docs/design-review-standards.md` — Padrões de avaliação
- `docs/workflow-guide.md` — Fluxo de trabalho onde frameworks se encaixam
- `voice/tone-profiles/creative-explorer.md` — Tom para fases de ideação
