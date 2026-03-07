# Stakeholder Communication

## Context

Guia de linguagem para comunicação com stakeholders — PMs, engineering managers,
diretores, C-level e outros decisores que influenciam o trabalho de design mas não
são designers. O objetivo é traduzir decisões de design em linguagem de negócio,
conectando escolhas visuais e de interação a métricas de impacto que stakeholders
valorizam: conversão, retenção, NPS, custo de suporte e tempo de desenvolvimento.

**Aplicação:** Apresentações, emails, reports, reuniões de alinhamento.
**Tom predominante:** Evidence-Driven + User Advocate
**Frequência:** Contínua — toda interação com stakeholders

## Do's

### Liderar com impacto no negócio
- "A simplificação do checkout pode reduzir abandono de carrinho em 15% (benchmark Baymard)"
- "O redesign do onboarding foca em reduzir time-to-value de 7 para 3 dias"
- "Investir em acessibilidade abre mercado de 45M de brasileiros com deficiência"

### Usar dados e benchmarks
- "Nosso NPS de experiência está em 34 — a média do setor é 42"
- "O tempo médio de task completion caiu de 4.2min para 2.8min após o redesign"
- "Cada ticket de suporte custa R$12. Prevenir 200 tickets/mês = R$2.400/mês"

### Apresentar opções com trade-offs claros
- "Opção A: 2 sprints, resolve 80% do problema. Opção B: 4 sprints, resolve 95%."
- "Podemos lançar com feature flag para 10% da base e validar antes do rollout completo"
- "Escopo reduzido entrega valor em março. Escopo completo entrega em maio."

### Conectar design a métricas existentes
- Relacionar mudanças visuais a KPIs que o stakeholder já acompanha
- Usar dashboards e reports que já existem como referência
- Propor métricas de design que complementem as métricas de produto

### Ser conciso e visual
- Bullet points ao invés de parágrafos longos
- Before/after screenshots para mudanças visuais
- Gráficos simples para mostrar tendências e impacto

## Don'ts

### Usar jargão de design sem tradução
- "Precisamos melhorar a affordance" — dizer "tornar mais claro o que é clicável"
- "O whitespace está desequilibrado" — dizer "a tela está visualmente poluída"
- "Falta progressive disclosure" — dizer "mostrar informação gradualmente"

### Apresentar sem contexto de negócio
- Mostrar telas sem explicar o problema que resolvem
- Discutir tipografia sem conectar a legibilidade e conversão
- Propor mudanças sem estimar esforço e impacto

### Ser defensivo sobre decisões de design
- "Vocês não entendem de design" — nunca, jamais
- "Confia em mim, é melhor assim" — sem evidência
- "Isso é best practice" — sem citar a fonte ou o contexto

### Surpresar com mudanças grandes
- Apresentar redesign completo sem ter alinhado direção antes
- Mudar escopo sem comunicar impacto no cronograma
- Ignorar feedback anterior de stakeholders

## Templates

### Template de email de alinhamento
```
Assunto: [Feature] — Proposta de Design — Alinhamento Necessário

Contexto: [1-2 frases sobre o problema]
Proposta: [1-2 frases sobre a solução]
Impacto esperado: [métricas]
Esforço estimado: [sprints/horas]
Trade-offs: [o que não entra nesta versão]
Decisão necessária: [o que precisa ser aprovado]
Prazo: [quando a decisão é necessária]
```

### Template de apresentação (5 slides)
```
1. O Problema (dados + impacto no negócio)
2. O Que Descobrimos (pesquisa + insights)
3. A Solução Proposta (visual + explicação)
4. Impacto Esperado (métricas + timeline)
5. Próximos Passos (ações + responsáveis)
```

### Template de status update semanal
```
## Design Status — Semana [N]

### Concluído
- [Feature/Tela] — status: em desenvolvimento
- [Feature/Tela] — status: em review

### Em andamento
- [Feature/Tela] — previsão: [data]

### Bloqueios
- [Descrição] — ação necessária: [o que precisa]

### Métricas
- Telas entregues: [N]
- Components criados: [N]
- Bugs de design resolvidos: [N]
```
