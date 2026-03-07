# Phase: Post-Release Monitoring

## Objective

Monitorar o impacto da feature apos lancamento, validar hipoteses e identificar oportunidades de melhoria.

## Inputs

- Metricas de sucesso definidas no brief (00-brief.md)
- Baseline de metricas pre-lancamento
- Feature lançada em producao
- Canais de feedback ativos (support, analytics, NPS)

## Activities

### 1. Launch Monitoring (Week 1)
```
Monitoramento diario:
- Error rates e crashes relacionados a feature
- Adoption rate (% de usuarios que usaram)
- Completion rate do fluxo principal
- Support tickets relacionados
- Sentiment em canais de feedback
```

### 2. Metrics Analysis (Week 2-4)
```
Analise vs baseline:
- Metrica primaria: [atual] vs [target]
- Metricas secundarias: [atuais] vs [targets]
- Segmentacao: performance por cohort (new vs returning)
- Funnel analysis: onde usuarios abandonam
```

### 3. Qualitative Feedback (Week 2-4)
```
Coleta:
- Review de support tickets relacionados
- NPS comments mentioning the feature
- In-app feedback (se disponivel)
- 3-5 user interviews pos-lancamento (se indicado)
```

### 4. Iteration Planning (Week 4)
```
Decisoes baseadas em dados:
- O que esta funcionando? (manter)
- O que nao esta funcionando? (iterar)
- O que falta? (backlog)
- O que surpreendeu? (learn)

Output: backlog priorizado de melhorias
```

### 5. Retrospective
```
Com o time completo:
- O que funcionou bem no processo?
- O que podemos melhorar?
- Quais learnings levamos para o proximo projeto?
- Atualizar lessons-learned-registry.yaml
```

## Output

- Post-launch report com metricas e insights
- Backlog de melhorias priorizado
- Lessons learned documentadas
- Updated success metrics (actual vs target)
- Case study draft (se resultados significativos)

## Next Phase

→ Iteracao (voltar para qualquer fase conforme necessario)
