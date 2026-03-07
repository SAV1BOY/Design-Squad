# Operating System

## Overview

O Operating System do Design Squad define como o time funciona no dia a dia —
rituais, cadências, fluxos de decisão e mecanismos de comunicação. É o "manual de
operação" que garante previsibilidade sem burocracia.

## Content

### Princípios Operacionais

1. **Async-first:** Decisões que podem ser assíncronas devem ser. Reuniões são para
   discussão, não para leitura de documentos.
2. **Default to public:** Toda comunicação é em canal público por padrão. DMs apenas
   para assuntos pessoais ou sensíveis.
3. **Write it down:** Se não está documentado, não existe. Decisões verbais são
   confirmadas por escrito.
4. **Single source of truth:** Cada tipo de informação tem um lugar canônico. Não
   duplicar entre Figma, Slack e Wiki.

### Cadência Semanal

| Dia | Ritual | Duração | Participantes |
|-----|--------|---------|---------------|
| Seg | Sprint Planning (quinzenal) | 1h | Design Squad + PM |
| Seg | Design Sync | 30min | Design Squad |
| Ter | Design Critique | 1h | Design Squad |
| Qua | Design Office Hours | 30min | Design Squad + org |
| Qui | 1:1s (design lead + membros) | 30min | Individual |
| Sex | Retro (quinzenal) | 45min | Design Squad |

### Fluxo de Decisão

#### Decisões do dia a dia (< 1h de impacto)
- Designer decide com autonomia
- Informar no canal se afetar outros
- Reverter se feedback indicar necessidade

#### Decisões de design (1 dia - 1 semana de impacto)
- Discutir na design critique ou assíncrono no Figma
- Design lead tem voto de desempate se necessário
- Documentar a decisão e o rationale

#### Decisões de design system (impacto cross-squad)
- RFC escrita com proposta, alternativas e trade-offs
- Período de feedback de 1 semana
- Aprovação do DS committee (design lead + DS engineer + 1 consumer rep)

#### Decisões estratégicas (impacto de quarter+)
- Design doc completo com análise de dados
- Review com liderança de produto
- Alinhamento com roadmap de produto

### Comunicação

#### Canais e propósito
| Canal | Propósito | Resposta esperada |
|-------|-----------|-------------------|
| #design-squad | Comunicação interna do time | Mesmo dia |
| #design-reviews | Feedback assíncrono de design | 48h |
| #design-system | Updates e discussões do DS | 48h |
| DM | Assuntos pessoais | 24h |
| Email | Comunicação formal / externa | 48h |

#### Regras de comunicação
- Mensagens importantes: canal público + tag específico
- Decisões em thread: resumo da decisão no canal principal
- Bloqueios: escalar em 24h se não resolvido
- Feedback negativo: DM primeiro, canal público se necessário

### Gestão de Trabalho

#### Figma Organization
```
Team: Design Squad
├── Project: [Produto A]
│   ├── File: [Feature] — Sprint [N]
│   ├── File: [Feature] — Sprint [M]
│   └── File: Archive
├── Project: [Produto B]
├── Project: Design System
│   ├── File: DS Core Library
│   ├── File: DS Icons
│   └── File: DS Documentation
└── Project: Sandbox
    └── File: Explorations
```

#### Naming Convention para Files
- `[Produto] — [Feature] — [Status]`
- Status: Exploration | In Progress | Review | Handed Off | Archive
- Exemplo: "Checkout — Redesign Form — In Progress"

### Métricas Operacionais

| Métrica | Como medir | Target |
|---------|------------|--------|
| Lead time de design | Da request ao handoff | < 5 dias úteis |
| Review turnaround | Do pedido ao feedback | < 48h |
| Rework rate | Telas que voltam por bug de design | < 10% |
| DS coverage | % de telas usando apenas DS components | > 85% |
| Sprint velocity | Story points de design entregues | Consistente |

## Cross-References

- `docs/squad-overview.md` — Contexto e estrutura do squad
- `docs/workflow-guide.md` — Fluxo de trabalho detalhado
- `docs/design-review-standards.md` — Padrões de review
- `docs/naming-conventions.md` — Convenções de nomenclatura
