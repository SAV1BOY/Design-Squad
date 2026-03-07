# Research to Design Pipeline

## Metadata

| Campo         | Valor                                     |
| ------------- | ----------------------------------------- |
| squad         | Design                                    |
| versao        | 1.0.0                                     |
| criado_em     | 2026-03-06                                |
| owner         | UX Researcher                             |
| cadencia      | Continuo (por projeto de pesquisa)        |
| duracao_media | 3-6 semanas (pesquisa ate design)         |
| tags          | research, insights, opportunity, pipeline |

## Trigger

Quando iniciar:

- Novo quarter com objetivos que demandam pesquisa generativa.
- Gap de conhecimento sobre usuarios identificado por PM ou Design Lead.
- Metricas anomalas que precisam de investigacao qualitativa.
- Nova persona ou segmento a explorar.

Pre-condicoes: objetivo de pesquisa aprovado por PM e Design Lead; Researcher alocado; budget para recrutamento; timeline acordada.

## Phases

### Fase 1 — Research (Planejamento e Execucao)
**Agents:** Researcher, PM, Design Lead.
**Inputs:** Objetivo estrategico, dados secundarios, perfil de participantes.
**Atividades:** Definir perguntas (max 5); escolher metodologia (entrevistas, diary studies, contextual inquiry, surveys); criar guia (roteiro, screener, consentimento); recrutar (8-12 generativa, 5-8 avaliativa); conduzir pesquisa; documentar dados brutos.
**Outputs:** Plano documentado, dados brutos coletados, debrief notes.

### Fase 2 — Insights (Sintese)
**Agents:** Researcher, Designer.
**Inputs:** Dados brutos, framework de sintese.
**Atividades:** Codificar observacoes atomicas; affinity mapping por tema; patterns = 3+ participantes; formular insights (observacao + implicacao); priorizar por impacto e confianca; atualizar personas/journey maps; relatorio com evidencias.
**Outputs:** Relatorio de insights priorizados, affinity map, personas atualizadas, highlight reel (3-5 min).

### Fase 3 — Opportunity Mapping
**Agents:** Researcher, Designer, PM.
**Inputs:** Insights priorizados, roadmap, OKRs.
**Atividades:** Apresentar insights (30-45 min); mapear contra roadmap; identificar novas oportunidades; Opportunity Solution Tree; priorizar com ICE (Impact, Confidence, Ease); definir quais viram briefs de design.
**Outputs:** Opportunity map, oportunidades priorizadas, briefs de design, decisoes documentadas.

### Fase 4 — Design (Conceituacao)
**Agents:** Designer, Researcher (consultivo).
**Inputs:** Brief baseado em oportunidade, insights, DS.
**Atividades:** Explorar 3+ alternativas; usar insights como guardrails (decisoes traceaeis); wireframes/mockups; critique com squad; selecionar e refinar; criar prototipo.
**Outputs:** Alternativas documentadas, direcao com rationale, prototipo, mapa decisoes-insights.

### Fase 5 — Test (Validacao)
**Agents:** Researcher, Designer.
**Inputs:** Prototipo, insights originais, hipoteses.
**Atividades:** Planejar teste (ver `usability-testing-sprint.md`); executar com 5-8 participantes; sintetizar; comparar com insights originais; decidir: aprovar, iterar (volta Fase 4), ou pivotar.
**Outputs:** Resultados de validacao, decisao documentada, design pronto para handoff (se aprovado).

## Quality Gates

### Gate Research -> Insights
- [ ] Minimo de participantes atingido.
- [ ] Dados brutos completos.

### Gate Insights -> Opportunity
- [ ] Insights com evidencia (nao suposicoes).
- [ ] Priorizacao por impacto e confianca.

### Gate Opportunity -> Design
- [ ] Insights apresentados a stakeholders.
- [ ] Briefs de design criados.

### Gate Design -> Test
- [ ] Min 3 alternativas exploradas.
- [ ] Decisoes traceaeis a insights.
- [ ] Critique realizada.

### Gate Test -> Outcome
- [ ] Min 5 participantes testados.
- [ ] Decisao documentada.

## Cross-References

- `usability-testing-sprint.md` — Fase 5 usa sprint de teste.
- `feature-design-end-to-end.md` — Design validado entra no pipeline.
- `design-critique-loop.md` — Critique na Fase 4.
- `design-sprint-5-day.md` — Sprint como metodo na Fase 4.
- `quarterly-design-review.md` — Insights alimentam estrategia.
- `ralphlooping-kaizen-design.md` — Insights alimentam sandbox.
