# Technical Depth Scale

## Metadata

- **Categoria:** Calibração de Voz
- **Aplicação:** Ajustar profundidade técnica conforme o contexto
- **Última atualização:** 2026-03-06

## Description

A Technical Depth Scale define quando e como aprofundar em detalhes técnicos de
design. Nem toda comunicação precisa de specs pixel-perfect, e nem toda conversa
pode ficar no nível conceitual. Esta escala ajuda a calibrar a quantidade de
detalhe técnico conforme a fase do projeto, o canal e o objetivo da comunicação.

## Scale

### Nível 1 — Conceitual
- **Quando:** Fase de discovery, ideação, pitch de conceito
- **Detalhe:** Zero specs. Foco em conceito, fluxo e proposta de valor
- **Artefatos:** Sketches, storyboards, wireframes low-fi, journey maps
- **Linguagem:** "O usuário precisa conseguir...", "A experiência deve sentir..."
- **Exemplo:** "O conceito propõe um onboarding progressivo onde cada interação
  ensina uma feature. Sem tutoriais, sem tours. O próprio uso é o aprendizado."

### Nível 2 — Estrutural
- **Quando:** Fase de definição, wireframes mid-fi, fluxos
- **Detalhe:** Layout, hierarquia, fluxo de navegação, IA
- **Artefatos:** Wireframes, sitemaps, fluxogramas, content maps
- **Linguagem:** "A tela tem 3 seções...", "O fluxo tem 4 etapas..."
- **Exemplo:** "O form de cadastro tem 4 etapas: dados pessoais, endereço,
  pagamento, confirmação. Progressive disclosure — cada etapa revela a seguinte.
  Back navigation disponível em todas as etapas."

### Nível 3 — Visual
- **Quando:** Fase de UI design, mockups hi-fi, protótipos
- **Detalhe:** Cores, tipografia, spacing, componentes, estados
- **Artefatos:** Mockups, protótipos interativos, redlines, style guides
- **Linguagem:** Tokens, valores exatos, referências ao design system
- **Exemplo:** "Header usa heading-lg (24px/32px, weight 700), cor text-primary.
  CTA usa button-primary (height 48px, padding-x 24px, border-radius 8px).
  Spacing entre seções: spacing-xl (32px)."

### Nível 4 — Spec Completo
- **Quando:** Handoff para desenvolvimento, documentação de componente
- **Detalhe:** Todos os estados, responsivo, edge cases, a11y, tokens
- **Artefatos:** Specs annotados, tabelas de tokens, component APIs
- **Linguagem:** Precisa e exaustiva — todos os cenários cobertos
- **Exemplo:** "Button Primary States: Default (bg: #1A73E8, text: #FFFFFF),
  Hover (bg: #1557B0), Active (bg: #0D47A1), Disabled (bg: #E0E0E0, text:
  #9E9E9E, cursor: not-allowed), Focus (ring: 2px solid #1A73E8, offset 2px).
  Min-width: 120px. Loading state: spinner 16px substitui label."

### Nível 5 — Arquitetural
- **Quando:** Design system evolution, token architecture, breaking changes
- **Detalhe:** Layers de abstração, dependências, migration paths, versionamento
- **Artefatos:** Token schemas, dependency graphs, ADRs, migration guides
- **Linguagem:** Altamente técnica — APIs, schemas, build pipelines
- **Exemplo:** "Token architecture refactor: 3 layers. Primitive (color-blue-500:
  #1A73E8), Semantic (color-action-primary: {color-blue-500}), Component
  (button-bg-default: {color-action-primary}). Build pipeline: Figma Tokens →
  Style Dictionary → CSS custom properties + Swift/Kotlin constants."

## Matching Phase to Depth

| Fase do Projeto   | Nível Primário | Nível Secundário |
|-------------------|---------------|-----------------|
| Discovery         | 1 Conceitual  | 2 Estrutural    |
| Definition        | 2 Estrutural  | 3 Visual        |
| Design            | 3 Visual      | 4 Spec          |
| Handoff           | 4 Spec        | 5 Arquitetural  |
| Design System     | 5 Arquitetural| 4 Spec          |

## Common Mistakes

- Apresentar specs detalhados em reunião de discovery (overwhelm)
- Discutir cores e fontes antes de validar o fluxo (detalhe prematuro)
- Fazer handoff sem specs completos (ambiguidade → retrabalho)
- Discutir arquitetura de tokens em sprint planning (audiência errada)

## Cross-References

- `voice/calibration/audience-depth-scale.md` — Calibração por público
- `voice/language-guides/feedback-to-developers.md` — Nível 4 na prática
- `docs/handoff-standards.md` — Padrões de entrega técnica
