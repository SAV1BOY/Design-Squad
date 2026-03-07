# Audience Depth Scale

## Metadata

- **Categoria:** Calibração de Voz
- **Aplicação:** Ajustar profundidade do conteúdo ao público-alvo
- **Última atualização:** 2026-03-06

## Description

A Audience Depth Scale define 5 níveis de profundidade de comunicação baseados
no público-alvo. Cada nível determina vocabulário, quantidade de contexto,
nível de abstração e formato de entrega. O objetivo é evitar o erro comum de
comunicar com profundidade técnica para executivos ou com superficialidade para
especialistas.

Antes de escrever qualquer documento, apresentação ou mensagem, identifique o
nível do seu público na escala abaixo.

## Scale

### Nível 1 — Executive (C-level, Board, Investidores)
- **Vocabulário:** Negócio, impacto financeiro, métricas macro
- **Profundidade:** Resumo executivo — máximo 1 página ou 5 slides
- **Formato:** Bullets, gráficos, números de impacto
- **Contexto necessário:** Mínimo — assumir que conhecem o produto mas não o detalhe
- **Exemplo:** "O redesign do checkout reduziu abandono de carrinho em 18%, gerando
  estimativa de R$2.4M adicionais em receita anual."
- **Evitar:** Wireframes, specs técnicos, jargão de design

### Nível 2 — Leadership (Directors, VPs, Head of Product)
- **Vocabulário:** Estratégia, roadmap, priorização, impacto
- **Profundidade:** Overview com dados de suporte — 5-10 slides ou 2-3 páginas
- **Formato:** Narrativa estruturada com dados, before/after visual
- **Contexto necessário:** Médio — conhecem o contexto mas precisam de atualização
- **Exemplo:** "Priorizamos 3 iniciativas de UX para Q2 baseadas no NPS breakdown:
  onboarding (NPS 23), checkout (NPS 31) e busca (NPS 38). O onboarding tem maior
  impacto potencial — 60% dos churns acontecem nos primeiros 7 dias."
- **Evitar:** Detalhes de implementação, specs de componentes

### Nível 3 — Cross-functional (PMs, Engineers, QA)
- **Vocabulário:** Misto — design + produto + tech
- **Profundidade:** Detalhado com specs acionáveis — docs completos
- **Formato:** User stories, specs, mockups annotados, tabelas de tokens
- **Contexto necessário:** Específico — precisam entender o que fazer
- **Exemplo:** "O card component usa spacing-md (16px) interno, border-radius-lg
  (12px), e shadow-sm para elevação. Responsive breakpoint em 768px troca para
  layout stack. Figma link: [link]. Tokens: [tabela]."
- **Evitar:** Contexto estratégico extenso (já alinhado), justificativa de negócio

### Nível 4 — Design Peers (Designers sênior, Design leads)
- **Vocabulário:** Design avançado — systems thinking, heurísticas, metodologia
- **Profundidade:** Deep dive com rationale e trade-offs
- **Formato:** Critique format, explorations, design decisions documentadas
- **Contexto necessário:** Pouco — compartilham base de conhecimento
- **Exemplo:** "A decisão de usar drawer ao invés de modal para o filtro segue o
  princípio de manter contexto. O modal oclude 100% do conteúdo, enquanto o
  drawer permite comparar filtros com resultados. Trade-off: menor área de
  conteúdo no drawer em mobile. Mitigação: full-screen drawer em viewport < 768px."
- **Evitar:** Explicar conceitos básicos, over-contextualize

### Nível 5 — Design System Specialists (DS engineers, Token architects)
- **Vocabulário:** Altamente técnico — tokens, primitives, semantic layers, APIs
- **Profundidade:** Máxima — specs completos, edge cases, migration paths
- **Formato:** Documentação técnica, ADRs, component specs, token schemas
- **Contexto necessário:** Mínimo de negócio, máximo técnico
- **Exemplo:** "Proposta de refactor da token layer: migrar de flat namespace
  (color-blue-500) para semantic + component tokens (color-action-primary →
  button-color-bg-default). Breaking change. Migration script no PR #347.
  Rollout: feature flag por squad, começando pelo squad-checkout."
- **Evitar:** Narrativas de usuário, justificativas de negócio extensas

## How to Choose

1. Identifique quem vai consumir a comunicação
2. Se o público é misto, use o nível mais acessível e ofereça apêndice detalhado
3. Comece pelo impacto (o quê mudou), depois o como, depois o porquê técnico
4. Em caso de dúvida, prefira simplicidade com link para detalhamento

## Cross-References

- `voice/tone-profiles/evidence-driven.md` — Tom para Nível 1-2
- `voice/tone-profiles/system-thinker.md` — Tom para Nível 4-5
- `voice/language-guides/stakeholder-communication.md` — Guia para Nível 1-2
- `voice/language-guides/feedback-to-developers.md` — Guia para Nível 3
