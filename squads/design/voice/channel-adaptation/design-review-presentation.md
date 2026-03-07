# Design Review Presentation

## Context

Adaptação de voz para apresentações em design reviews — o momento formal onde o
time apresenta e avalia trabalho de design com stakeholders, PMs, engenheiros e
outros designers. A apresentação é o veículo; a comunicação eficaz é o objetivo.

**Canal:** Reunião presencial ou remota (Zoom/Meet/Teams)
**Duração típica:** 30-60 minutos
**Audiência:** Cross-funcional (design, produto, engenharia, QA)
**Formalidade:** Nível 3 (Profissional)
**Tom:** Evidence-Driven + User Advocate

## Adaptation Rules

### Abertura (2-3 minutos)
- Contextualizar o problema antes de mostrar a solução
- Definir expectativas: "Hoje busco feedback sobre [X], não sobre [Y]"
- Informar o estágio: "Isto é exploração / conceito validado / spec final"
- Listar critérios de avaliação: usabilidade, viabilidade, consistência, a11y

### Apresentação (10-20 minutos)
- Narrar o fluxo do ponto de vista do usuário, não da tela
- Mostrar decisões de design com rationale — não apenas o resultado
- Antecipar perguntas: "Vocês podem estar pensando 'por que não modal?' — vou explicar"
- Mostrar alternativas consideradas e por que foram descartadas
- Destacar trade-offs explicitamente: "Ganhamos X, abrimos mão de Y"

### Coleta de feedback (10-20 minutos)
- Direcionar: "Gostaria de feedback específico sobre [área]"
- Anotar tudo — não rebater no momento, absorver
- Perguntar: "Isso é blocker ou nice-to-have na sua avaliação?"
- Sintetizar ao final: "Então os consensos são [A, B] e os pontos abertos são [C, D]"

### Fechamento (2-3 minutos)
- Listar action items com owners e prazos
- Definir próximo checkpoint
- Agradecer as contribuições específicas

## Visual Communication Tips

- Tela cheia para mockups — sem distrações de Figma UI
- Usar prototype mode para demonstrar interações
- Annotations visíveis para chamar atenção para decisões-chave
- Before/after para mudanças em features existentes
- Redlines e specs apenas se a audiência for técnica

## Common Mistakes

- Mostrar 30 telas sem narrar o contexto (overwhelm)
- Não definir o tipo de feedback desejado (recebe tudo, maioria inútil)
- Defender cada pixel agressivamente (postura defensiva)
- Não ter protótipo e esperar que a audiência imagine a interação
- Apresentar como "finalizado" quando ainda quer feedback
- Não documentar decisões tomadas durante a review

## Templates

### Template de agenda de design review
```
## Design Review — [Feature Name] — [Data]

### Agenda
1. Contexto e problema (3 min)
2. Apresentação da solução (15 min)
3. Feedback dirigido (15 min)
4. Action items e próximos passos (5 min)

### Pré-leitura (opcional)
- [Link para o doc de specs]
- [Link para o protótipo]

### Tipo de feedback solicitado
- [ ] Usabilidade do fluxo
- [ ] Viabilidade técnica
- [ ] Consistência com design system
- [ ] Acessibilidade
- [ ] Microcopy e conteúdo
```

### Template de notas pós-review
```
## Review Notes — [Feature] — [Data]

### Decisões tomadas
- [Decisão 1]
- [Decisão 2]

### Feedback a incorporar
- [Feedback] — Responsável — Prazo

### Pontos em aberto
- [Questão] — Próximo passo para resolver

### Próxima review
- Data: [quando]
- Foco: [o que será apresentado]
```
