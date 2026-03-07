# Handoff Standards

## Overview

Padrões de entrega de design para desenvolvimento. O handoff é o ponto de maior
risco de perda de informação no ciclo de design. Estes padrões garantem que toda
entrega seja completa, não ambígua e verificável.

## Content

### Definition of Done — Design

Uma entrega de design é considerada "done" quando:

- [ ] Todos os estados do componente/tela estão especificados
- [ ] Comportamento responsivo definido para 3 breakpoints mínimos
- [ ] Tokens do design system referenciados (não valores hardcoded)
- [ ] Acessibilidade especificada (ARIA, keyboard, focus, contrast)
- [ ] Microcopy revisada e aprovada por UX Writer
- [ ] Protótipo interativo para fluxos complexos
- [ ] Design review aprovada
- [ ] Figma organizado no padrão de handoff

### Estados Obrigatórios

Todo componente interativo deve ter spec para:

| Estado | Obrigatório? | Notas |
|--------|-------------|-------|
| Default | Sim | Estado inicial |
| Hover | Sim (desktop) | Não aplicável em mobile |
| Focus | Sim | Obrigatório para a11y |
| Active/Pressed | Sim | Feedback de interação |
| Disabled | Sim | Quando ação não está disponível |
| Loading | Sim | Para ações assíncronas |
| Error | Sim | Para inputs e ações que podem falhar |
| Success | Condicional | Quando confirmação é necessária |
| Empty | Condicional | Para listas e coleções |
| Skeleton | Recomendado | Loading state da tela/seção |

### Breakpoints

| Breakpoint | Viewport | Obrigatório? |
|-----------|----------|-------------|
| Mobile | 375px | Sim |
| Tablet | 768px | Sim |
| Desktop | 1440px | Sim |
| Large Desktop | 1920px | Recomendado |

### Organização do Figma para Handoff

```
Frame: [Feature Name] — Handoff
├── Section: Flow Overview (fluxograma geral)
├── Section: Screen 1 — [Nome]
│   ├── Desktop
│   ├── Tablet
│   ├── Mobile
│   ├── States (hover, focus, error, etc.)
│   └── Annotations
├── Section: Screen 2 — [Nome]
│   └── (mesma estrutura)
├── Section: Components (se há componentes novos)
│   ├── Component specs
│   ├── All states
│   └── Token mapping
└── Section: Handoff Notes
    ├── Behavior specs (texto)
    ├── Token reference table
    ├── A11y specs
    └── Edge cases
```

### Token Reference Table

Todo handoff inclui tabela de tokens utilizados:

```
| Elemento | Propriedade | Token | Valor |
|----------|-------------|-------|-------|
| Background | color | color-surface-primary | #FFFFFF |
| Title | font | heading-md | 20px/28px, 700 |
| Body | font | body-md | 16px/24px, 400 |
| CTA | bg-color | color-action-primary | #1A73E8 |
| Card | border-radius | radius-lg | 12px |
| Card | padding | spacing-lg | 24px |
| Card | shadow | shadow-md | 0 4px 12px rgba(0,0,0,0.1) |
```

### Annotation Standards

Annotations no Figma devem ser:
- **Numeradas** para referência em tickets
- **Concisas** — comportamento, não justificativa
- **Focadas em ambiguidade** — especificar apenas o que não é óbvio
- **Vinculadas** ao elemento que descrevem (seta ou proximity)

Tipos de annotation:
- **Interaction:** "Click abre modal" / "Swipe para excluir"
- **Condition:** "Mostra se [condição]" / "Esconde quando [estado]"
- **Data:** "Máximo 50 caracteres, truncate com ellipsis"
- **A11y:** "aria-label: [texto]" / "role: dialog"

### Processo de Handoff

1. Designer finaliza specs e organiza Figma
2. Designer posta no #design-reviews para review assíncrona
3. Feedback incorporado (se houver)
4. Handoff meeting com dev (30 min walkthrough)
5. Dev faz perguntas, designer documenta respostas
6. Ticket criado/atualizado com link do Figma
7. QA visual pelo designer após implementação

## Cross-References

- `voice/language-guides/feedback-to-developers.md` — Linguagem para devs
- `voice/channel-adaptation/ticket-writing-for-design.md` — Escrita de tickets
- `phrases/handoff-communication.md` — Frases de handoff
- `docs/naming-conventions.md` — Convenções de nomenclatura
