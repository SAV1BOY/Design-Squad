# Post-Release Review

## Metadata
- **Categoria:** Handoff
- **Complexidade:** Média
- **Tempo Estimado:** 2-3 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** handoff, post-release, retrospective, metrics, impact, learning

## Objective
Avaliar o impacto de uma feature ou projeto após o release em produção, comparando resultados
reais com métricas de sucesso definidas durante o discovery. O review gera aprendizados que
alimentam decisões futuras de design e melhoria contínua do processo do squad.

## Prerequisites
- Feature em produção por pelo menos 2-4 semanas (tempo para coleta de dados)
- Métricas de sucesso definidas na fase de discovery ou planning
- Dados de analytics acessíveis para o período pós-release
- Feedback de usuários coletado (suporte, NPS, reviews)
- Disponibilidade de PM, eng e design para sessão de review

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design Lead | Facilitar review, consolidar aprendizados e definir ações |
| UI/UX Designer | Analisar dados de uso e confrontar com hipóteses de design |
| Product Manager | Fornecer contexto de negócio e métricas de produto |
| Data Analyst | Extrair e apresentar dados de analytics |
| Frontend Engineer | Compartilhar aprendizados técnicos e issues pós-release |

## Frameworks
- **Metrics Review** — confrontar resultados reais vs targets definidos
- **Retrospective Format** — what went well, what didn't, what to improve
- **Impact Assessment** — avaliação qualitativa e quantitativa do impacto
- **Learning Log** — registro estruturado de aprendizados para referência futura
- **Decision Log** — registro de decisões tomadas e seus resultados

## Checklists
- [ ] Período mínimo pós-release respeitado (2-4 semanas)
- [ ] Métricas de sucesso originais localizadas e revisadas
- [ ] Dados de analytics coletados para o período pós-release
- [ ] Feedback de usuários compilado (suporte, NPS, surveys)
- [ ] Bugs e issues pós-release catalogados
- [ ] Sessão de review agendada com todos os agents
- [ ] Retrospective facilitada (went well, didn't, improve)
- [ ] Aprendizados documentados em Learning Log
- [ ] Ações de follow-up definidas e atribuídas
- [ ] Resultados comunicados para stakeholders

## Steps
1. **Coletar dados quantitativos** — Com Data Analyst, extrair métricas de uso: adoption rate,
   task completion, time on task, error rate, funnel conversion pós-release.

2. **Coletar feedback qualitativo** — Compilar: tickets de suporte relacionados, feedback in-app,
   NPS verbatims, reviews em app stores e comentários da equipe de CS.

3. **Confrontar com targets** — Comparar resultados reais com métricas de sucesso definidas na
   fase de planning. Documentar: atingiu, superou ou ficou abaixo do target.

4. **Catalogar issues pós-release** — Listar bugs, edge cases não previstos e problemas de
   usabilidade reportados após o release. Classificar por severidade.

5. **Facilitar sessão de review** — Conduzir reunião de 60 minutos com formato de retrospectiva:
   o que funcionou bem, o que não funcionou e o que melhorar no processo.

6. **Avaliar decisões de design** — Revisitar decisões de design tomadas durante o projeto.
   Identificar quais se provaram corretas e quais precisam de revisão.

7. **Documentar aprendizados** — Registrar insights em formato estruturado: contexto, decisão
   tomada, resultado observado e recomendação para projetos futuros.

8. **Definir ações de follow-up** — Se métricas ficaram abaixo do target ou issues significativos
   foram encontrados, definir ações corretivas com owner e deadline.

9. **Comunicar resultados** — Compartilhar resumo executivo com stakeholders: impacto alcançado,
   aprendizados e próximos passos. Celebrar sucessos.

## Output
- **Post-Release Review Report** — Relatório com métricas, análise e aprendizados
- **Learning Log** — Aprendizados estruturados para referência futura
- **Follow-up Actions** — Lista de ações corretivas priorizadas
- **Formato:** Markdown + dashboard de métricas
- **Nomenclatura:** `post-release-review-[feature]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Após cada major release (2-4 semanas pós-deploy) |
| Aprovadores | Design Lead, PM |
| Repositório | `/squads/design/tasks/handoff/` |

## Cross-References
- [QA with Engineering](./qa-with-engineering.md)
- [Dev Handoff](./dev-handoff.md)
- [Analyze Analytics for UX](../research/analyze-analytics-for-ux.md)
- [Post-Launch Design Review](../review/post-launch-design-review.md)
- [Design Debt Prioritization](../operations/design-debt-prioritization.md)
- [Quarterly Design Review](../operations/quarterly-design-review.md)
