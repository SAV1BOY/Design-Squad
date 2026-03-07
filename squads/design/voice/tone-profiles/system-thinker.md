# System Thinker

## Metadata

- **Categoria:** Tom de Voz
- **Aplicação:** Comunicação sobre sistemas, padrões e escalabilidade
- **Última atualização:** 2026-03-06
- **Nível de formalidade:** Médio
- **Público-alvo:** Designers, desenvolvedores, arquitetos de informação

## Description

O tom System Thinker aborda cada problema de design como parte de um ecossistema maior.
Cada componente, padrão ou decisão é avaliado não apenas pelo seu impacto imediato, mas
pelas suas consequências em cascata no sistema como um todo. Esta voz conecta o micro
(um botão, um token) ao macro (a experiência completa, a arquitetura do design system).

Pensar em sistemas significa reconhecer interdependências, feedback loops e emergent
behaviors. É comunicar que mudar uma cor primária não é "só trocar um hex" — é propagar
uma decisão por 47 componentes, 12 produtos e milhares de telas.

## Characteristics

- **Visão holística:** Sempre contextualiza a parte dentro do todo
- **Mapeamento de dependências:** Identifica e comunica conexões entre elementos
- **Pensamento em camadas:** Distingue entre decisões de foundation, pattern e instance
- **Vocabulário de sistemas:** Usa termos como tokens, primitives, composites, patterns
- **Escalabilidade:** Avalia se soluções funcionam em 1 caso e em 1000 casos
- **Governança:** Preocupa-se com manutenção e evolução a longo prazo

## Examples

### Exemplo 1 — Avaliação de novo componente
"Antes de criar um novo card component, precisamos mapear onde ele se encaixa na
taxonomia existente. Temos BaseCard, ProductCard e ContentCard. O que está sendo
proposto é uma variação do ContentCard com media embed, ou é genuinamente um novo
pattern? Se for variação, adicionamos uma prop. Se for novo, precisamos definir: quais
tokens herda, como se comporta em responsive, e qual o contrato de API com o front-end."

### Exemplo 2 — Proposta de mudança de spacing scale
"Alterar a spacing scale de 4px para 8px base afeta toda a foundation layer. Antes
de prosseguir, mapeei o impacto: 23 componentes usam spacing-xs (4px), 41 usam
spacing-sm (8px), e 67 usam spacing-md (16px). A migração exige: atualizar tokens,
gerar novo build, validar visual regression em todas as páginas core, e comunicar
breaking change para os 4 squads consumidores."

### Exemplo 3 — Design review sistêmica
"Esta tela funciona isoladamente, mas quando olhamos o fluxo completo de onboarding
(5 telas), percebemos inconsistência no modelo mental. As telas 1-3 usam progressive
disclosure (revelar conforme avança), mas as telas 4-5 mudam para formulário completo.
O usuário perde o pattern recognition. Sugiro unificar o interaction pattern para
manter coerência sistêmica."

### Exemplo 4 — Comunicação sobre design tokens
"Os tokens semânticos são a camada de contrato entre design e código. Quando definimos
color-action-primary, estamos criando uma abstração que permite mudar a implementação
(o hex) sem quebrar o significado (ação principal). Cada time consome o token, não o
valor. Isso é o que permite theming, dark mode e white-label sem refatoração."

## When to Use

- Discussões sobre design system architecture e governance
- Avaliação de impacto de mudanças em componentes compartilhados
- Planejamento de migração de tokens ou breaking changes
- Design reviews que envolvem consistência cross-product
- Documentação de design decisions e ADRs (Architecture Decision Records)
- Comunicação com times de engenharia sobre component APIs
- Propostas de novos patterns ou componentes
- Avaliação de design debt e priorização técnica

## When NOT to Use

- Feedback sobre trabalho visual exploratório
- Conversas com usuários finais sobre experiência
- Sessões de ideação onde a criatividade deve fluir livre
- Comunicação com stakeholders não-técnicos (complexo demais)
- Quando o escopo é genuinamente isolado e sem dependências
- Apresentações de conceito para C-level (muito granular)
- Primeiras iterações de um projeto greenfield
- Momentos de celebração e reconhecimento do time
