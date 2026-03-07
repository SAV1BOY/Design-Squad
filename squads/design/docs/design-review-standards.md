# Design Review Standards

## Overview

Padrões para design reviews — o ritual de avaliação de qualidade de design antes
de avançar para handoff. Reviews estruturadas elevam a qualidade e criam
aprendizado coletivo. Reviews desestruturadas desperdiçam tempo.

## Content

### Tipos de Review

#### 1. Peer Critique (entre designers)
- **Frequência:** Semanal (terça, 1h)
- **Objetivo:** Melhorar qualidade do design, compartilhar conhecimento
- **Formato:** 1-2 designers apresentam, time dá feedback
- **Critérios:** Usabilidade, consistência, criatividade, a11y
- **Output:** Lista de feedback, designer incorpora antes de handoff

#### 2. Stakeholder Review (com PM, engenharia)
- **Frequência:** Por demanda, antes de handoff
- **Objetivo:** Alinhar expectativas, validar viabilidade, aprovar direção
- **Formato:** Designer apresenta, grupo discute, decisão ao final
- **Critérios:** Alinhamento com requisitos, viabilidade, escopo
- **Output:** Aprovação, lista de ajustes, ou redirect

#### 3. A11y Review (com a11y specialist)
- **Frequência:** Antes de handoff para features com UI
- **Objetivo:** Garantir conformidade com WCAG AA
- **Formato:** Checklist + walkthrough com screen reader
- **Critérios:** Contrast, keyboard, ARIA, focus, semântica
- **Output:** Lista de issues com severidade e fix sugerido

#### 4. DS Consistency Review (com DS engineer)
- **Frequência:** Antes de handoff para features com novos componentes
- **Objetivo:** Garantir uso correto do design system
- **Formato:** Review assíncrona no Figma ou walkthrough rápido
- **Critérios:** Token usage, component consistency, naming
- **Output:** Lista de ajustes ou aprovação

### Critérios de Avaliação

| Critério | Peso | O que avaliar |
|----------|------|---------------|
| Usabilidade | Alto | Fluxo claro, feedback de sistema, prevenção de erro |
| Consistência | Alto | Uso de DS, patterns reconhecíveis, linguagem |
| Acessibilidade | Alto | Contraste, keyboard, screen reader, touch targets |
| Viabilidade | Médio | Implementável no prazo, componentes disponíveis |
| Completude | Médio | Todos os estados, responsivo, edge cases |
| Estética | Baixo | Alinhamento visual, hierarquia, polish |

### Como Apresentar

1. **Contextualizar** (2 min): Problema, público, restrições
2. **Definir escopo de feedback** (1 min): "Busco feedback sobre X, não Y"
3. **Apresentar solução** (10-15 min): Fluxo + telas + rationale
4. **Coletar feedback** (15-20 min): Estruturado por critério
5. **Sintetizar** (5 min): Consensos, divergências, action items

### Como Dar Feedback

**Formato:** Observação → Impacto → Sugestão

- "O CTA está competindo com o banner [observação]. Isso pode reduzir clicks
  na ação principal [impacto]. Sugiro reduzir o contraste do banner ou mover
  o CTA acima [sugestão]."

**Regras:**
- Específico > Vago ("o padding está 12px, deveria ser 16px" > "tá apertado")
- Construtivo > Destrutivo (propor alternativa ao apontar problema)
- Baseado em critério > Baseado em gosto ("viola heurística X" > "não gostei")
- Pergunta antes de afirmação ("qual o racional?" antes de "está errado")

### Escalation Path

Se não há consenso na review:
1. **Designer** incorpora feedback consensual e revisa pontos abertos
2. **Design Lead** tem voto de desempate em decisões de design
3. **PM** tem voto de desempate em decisões de escopo e prioridade
4. **Data** resolve o empate quando disponível (A/B test, pesquisa)

### Template de Review Notes

```
# Review Notes — [Feature] — [Data]

## Contexto
[1-2 frases]

## Participantes
[Lista]

## Feedback por Critério

### Usabilidade
- [Feedback] — Severidade: [Blocker/Major/Minor] — Status: [Aceito/Discutindo]

### Consistência
- [Feedback]

### Acessibilidade
- [Feedback]

## Decisões
- [Decisão tomada]

## Action Items
- [ ] [Ação] — [Owner] — [Prazo]

## Próximo Checkpoint
[Data e foco]
```

## Cross-References

- `voice/language-guides/design-critique-language.md` — Linguagem de critique
- `voice/channel-adaptation/design-review-presentation.md` — Apresentação em reviews
- `phrases/critique-prompts.md` — Prompts para critique
- `docs/handoff-standards.md` — Padrão de entrega pós-review
