# Ralphlooping Kaizen Design

## Metadata

| Campo         | Valor                                     |
| ------------- | ----------------------------------------- |
| squad         | Design                                    |
| versao        | 1.0.0                                     |
| criado_em     | 2026-03-06                                |
| owner         | Design Lead                               |
| cadencia      | Continuo (loop infinito)                  |
| duracao_media | Cada ciclo: 1-2 semanas                   |
| tags          | kaizen, iteracao, loop, melhoria-continua |

## Trigger

Quando iniciar:

- Feature em producao precisa de melhoria continua.
- Metricas indicam oportunidade de otimizacao (conversion, engagement, satisfaction).
- Design Lead opta por iteracao incremental em vez de redesign completo.
- Produto em growth que demanda experimentacao constante.

Pre-condicoes: feature em producao com metricas sendo coletadas; analytics configurado (eventos, funnels); canal de feedback ativo; time com mindset kaizen.

## Phases

### Fase 1 — Sandbox (Exploracao Livre)
**Agents:** Designer, qualquer membro interessado.
**Inputs:** Feature atual, metricas baseline, feedback qualitativo, benchmarks.
**Atividades:** Timebox de exploracao (2-4 horas); experimentar sem restricao (sketches, wireframes, mockups rapidos); documentar hipoteses ("Se X, acreditamos que Y melhora em Z%"); gerar min 3 ideias por ciclo sem filtro; manter board acumulado de ideias; incluir wild ideas.
**Outputs:** Board de exploracao, hipoteses escritas, nivel de esforco estimado (gut feeling).

### Fase 2 — Feedback (Validacao Rapida)
**Agents:** Designer, PM, 2-3 stakeholders ou usuarios.
**Inputs:** Top 1-3 ideias do sandbox priorizadas por impacto.
**Atividades:** Criar artefato minimo (sketch anotado, wireframe, mockup low-fi); guerrilla test com 3-5 internos (15 min cada); review assincrono via Loom + form; dot voting com squad; documentar feedback; decidir: pivotar, persistir, ou descartar.
**Outputs:** Feedback por ideia, decisao go/no-go, ideia selecionada para dados.

### Fase 3 — Dados (Medicao e Evidencia)
**Agents:** Designer, Data Analyst (ou PM), Frontend Engineer.
**Inputs:** Ideia validada, metricas baseline, hipotese escrita.
**Atividades:** Definir metricas de sucesso (leading e lagging); decidir metodo (A/B test, feature flag, before/after); instrumentar tracking; implementar com feature flag; coletar dados (min 1 semana ou n estatistico); analisar contra hipotese.
**Outputs:** Dados analisados, resultado (confirmada/parcial/refutada), recomendacao, doc do experimento.

### Fase 4 — Iteracao (Aplicar e Recomecar)
**Agents:** Designer, Frontend Engineer, Design Lead.
**Inputs:** Resultado do experimento, feedback pos-lancamento, backlog de ideias.
**Atividades:** Se confirmada: rollout completo, nova baseline. Se parcial: iterar, voltar Fase 2/3. Se refutada: documentar aprendizado, reverter, voltar Fase 1. Compartilhar aprendizado com squad (5 min). Alimentar sandbox com novas ideias. **Recomecar o loop.**
**Outputs:** Baseline atualizado, aprendizado documentado, proximo ciclo iniciado.

### Condicoes de Saida do Loop

O loop eh infinito, mas pode ser pausado quando: feature atinge plateau; feature descontinuada; resources realocados; decisao explicita do Design Lead. Ao pausar: documentar estado, metricas finais, ideias pendentes.

## Quality Gates

### Gate Sandbox -> Feedback
- [ ] Min 3 ideias exploradas.
- [ ] Hipoteses escritas para cada ideia.

### Gate Feedback -> Dados
- [ ] Feedback de min 3 pessoas.
- [ ] Decisao go/no-go documentada.

### Gate Dados -> Iteracao
- [ ] Metricas definidas antes do experimento.
- [ ] Dados coletados por periodo significativo.
- [ ] Resultado documentado.

### Gate Iteracao -> Proximo Ciclo
- [ ] Baseline atualizado.
- [ ] Aprendizado compartilhado.
- [ ] Sandbox alimentado.

## Cross-References

- `feature-design-end-to-end.md` — Kaizen aplica-se a features entregues.
- `usability-testing-sprint.md` — Feedback mais rigoroso na Fase 2.
- `design-critique-loop.md` — Critique nas ideias do sandbox.
- `quarterly-design-review.md` — Resultados alimentam review trimestral.
- `design-debt-reduction-sprint.md` — Iteracoes podem resolver divida.
- `research-to-design-pipeline.md` — Insights alimentam sandbox.
