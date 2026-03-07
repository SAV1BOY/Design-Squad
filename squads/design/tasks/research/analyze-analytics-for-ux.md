# Analyze Analytics for UX

## Metadata
- **Categoria:** Research
- **Complexidade:** Média
- **Tempo Estimado:** 3-5 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** research, analytics, quantitative, behavioral-data, ux-metrics

## Objective
Analisar dados de analytics e comportamento do usuário para identificar padrões de uso, pontos de
atrito, drop-offs e oportunidades de melhoria na experiência. A análise traduz dados quantitativos
em hipóteses de design testáveis e prioriza áreas que necessitam de investigação qualitativa.

## Prerequisites
- Acesso a ferramentas de analytics (Google Analytics, Mixpanel, Amplitude ou equivalente)
- Tracking implementado nos fluxos relevantes (eventos, pageviews, conversões)
- Período de análise definido (mínimo 30 dias de dados)
- Métricas de negócio e benchmarks disponíveis para comparação
- Acesso a ferramentas de heatmap e session replay (Hotjar, FullStory) se disponíveis

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UX Researcher | Definir perguntas de análise e interpretar dados sob lente de UX |
| Data Analyst | Extrair dados, criar queries e gerar visualizações |
| Product Manager | Contextualizar métricas de negócio e definir prioridades |
| Design Lead | Traduzir achados em hipóteses de design e próximos passos |

## Frameworks
- **HEART Framework (Google)** — Happiness, Engagement, Adoption, Retention, Task Success
- **Funnel Analysis** — para identificar drop-offs em fluxos críticos
- **Cohort Analysis** — para comparar comportamento entre grupos de usuários
- **Behavioral Segmentation** — para identificar padrões por tipo de usuário
- **UX Metrics Dashboard** — para monitoramento contínuo de métricas de experiência

## Checklists
- [ ] Perguntas de análise documentadas (o que queremos saber?)
- [ ] Fontes de dados inventariadas e acessos verificados
- [ ] Período de análise definido e dados exportados/consultados
- [ ] Funnel analysis executado para fluxos críticos
- [ ] Heatmaps e session replays revisados (se disponíveis)
- [ ] Segmentações relevantes aplicadas (dispositivo, cohort, persona)
- [ ] Anomalias e padrões inesperados identificados
- [ ] Hipóteses de UX formuladas a partir dos dados
- [ ] Relatório com visualizações e recomendações redigido
- [ ] Findings apresentados ao squad

## Steps
1. **Formular perguntas de análise** — Definir 5-10 perguntas específicas que a análise deve
   responder. Exemplo: "Onde os usuários abandonam o fluxo de onboarding?"

2. **Mapear fontes e métricas** — Identificar quais ferramentas e eventos respondem a cada
   pergunta. Verificar qualidade do tracking e gaps de instrumentação.

3. **Executar funnel analysis** — Para cada fluxo crítico, analisar conversão por etapa.
   Identificar drop-offs acima de 20% como pontos de atenção.

4. **Analisar heatmaps e sessions** — Revisar heatmaps de scroll e click nos fluxos com maior
   drop-off. Assistir 10-20 session replays para contextualizar dados quantitativos.

5. **Segmentar por comportamento** — Aplicar segmentações por: dispositivo, sistema operacional,
   cohort de entrada, frequência de uso. Identificar diferenças significativas entre grupos.

6. **Identificar padrões e anomalias** — Cruzar dados para encontrar correlações e
   comportamentos inesperados. Documentar tanto confirmações quanto surpresas.

7. **Formular hipóteses de design** — Para cada achado relevante, articular uma hipótese
   testável: "Se [mudança], então [resultado esperado] porque [evidência]."

8. **Criar visualizações** — Produzir gráficos e dashboards que comuniquem os achados de forma
   clara para audiência não-técnica. Priorizar clareza sobre complexidade.

9. **Documentar e recomendar** — Redigir relatório com: perguntas respondidas, dados visuais,
   hipóteses e recomendações de próximos passos (pesquisa qualitativa, A/B test, redesign).

## Output
- **UX Analytics Report** — Relatório com achados, visualizações e hipóteses de design
- **UX Metrics Dashboard** — Dashboard configurado para monitoramento contínuo (se aplicável)
- **Formato:** Markdown + dashboards + exports de visualizações
- **Nomenclatura:** `analytics-ux-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UX Researcher |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Mensal (contínuo) ou por projeto |
| Aprovadores | Design Lead, PM |
| Repositório | `/squads/design/tasks/research/` |

## Cross-References
- [Survey and Analysis](./survey-and-analysis.md)
- [Synthesize Insights](./synthesize-insights.md)
- [Run Usability Test](./run-usability-test.md)
- [Problem Definition](../discovery/problem-definition.md)
- [Post-Release Review](../handoff/post-release-review.md)
- [Design Data Visualizations](../ui/design-data-visualizations.md)
