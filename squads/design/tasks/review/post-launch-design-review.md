# Post-Launch Design Review

## Metadata
- **Categoria:** Review
- **Complexidade:** Média
- **Tempo Estimado:** 2-3 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** review, post-launch, metrics, impact, retrospective, continuous-improvement

## Objective
Conduzir uma revisão estruturada do design após o lançamento de uma feature ou produto, avaliando
a fidelidade da implementação, o impacto nas métricas definidas e a qualidade percebida pelos
usuários. O review alimenta o ciclo de melhoria contínua e gera inputs para iterações futuras.

## Prerequisites
- Feature em produção por pelo menos 4 semanas
- Métricas de sucesso definidas durante planning ou discovery
- Dados de analytics e feedback de usuários disponíveis
- QA de design executado durante implementação (para referência)
- Disponibilidade dos envolvidos no projeto para sessão de review

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design Lead | Facilitar review, sintetizar aprendizados e definir next steps |
| UI/UX Designer | Comparar implementação final vs design intent |
| Product Manager | Apresentar métricas de negócio e contexto de resultado |
| Data Analyst | Extrair dados de uso e comportamento pós-launch |
| UX Researcher | Trazer feedback qualitativo e insights de pesquisa pós-launch |

## Frameworks
- **Design Impact Assessment** — avaliação quantitativa e qualitativa do impacto
- **Implementation Fidelity Check** — comparação design vs produção
- **User Feedback Synthesis** — consolidação de feedback por canal
- **Retrospective (4Ls)** — Liked, Learned, Lacked, Longed-for
- **Iteration Backlog** — lista de melhorias para próximo ciclo

## Checklists
- [ ] Métricas de sucesso originais revisadas e resultados comparados
- [ ] Fidelidade de implementação verificada (design vs produção)
- [ ] Dados de analytics pós-launch analisados
- [ ] Feedback de usuários compilado (suporte, NPS, in-app)
- [ ] Issues de design identificados em produção catalogados
- [ ] Sessão de review conduzida com stakeholders
- [ ] Aprendizados de processo documentados
- [ ] Iteration backlog criado com melhorias priorizadas
- [ ] Resultados comunicados ao squad e stakeholders
- [ ] Inputs integrados ao design backlog

## Steps
1. **Coletar métricas de impacto** — Obter dados de: adoption rate, task completion rate, NPS
   delta, support ticket volume e métricas de negócio específicas da feature.

2. **Verificar fidelidade de implementação** — Comparar telas em produção com mockups originais.
   Documentar divergências visuais e comportamentais remanescentes.

3. **Compilar feedback de usuários** — Reunir feedback de: tickets de suporte, comentários in-app,
   surveys pós-launch, session recordings e feedback direto da equipe de CS.

4. **Analisar comportamento de uso** — Revisar heatmaps, funnel completion e session recordings
   para entender como os usuários estão realmente interagindo com a feature.

5. **Identificar issues e oportunidades** — A partir dos dados, listar: problemas de usabilidade
   observados, oportunidades de melhoria e features complementares sugeridas.

6. **Facilitar sessão de review** — Conduzir sessão de 60-90 minutos com formato 4Ls. Apresentar
   dados e facilitar discussão sobre aprendizados e melhorias.

7. **Documentar aprendizados** — Registrar: decisões de design que funcionaram, decisões que
   precisam revisão, surpresas nos dados e melhorias de processo identificadas.

8. **Priorizar iteration backlog** — Criar lista de melhorias de design priorizadas por impacto.
   Separar em: quick fixes, enhancements e explorations para próximo ciclo.

9. **Comunicar e integrar** — Compartilhar resultados com stakeholders. Integrar iteration
   backlog ao design backlog do squad para planejamento do próximo ciclo.

## Output
- **Post-Launch Review Report** — Relatório com métricas, fidelidade, feedback e aprendizados
- **Iteration Backlog** — Lista priorizada de melhorias para próximo ciclo
- **Learning Log** — Aprendizados estruturados de processo e design
- **Formato:** Markdown + dashboard + Miro/FigJam board da retrospectiva
- **Nomenclatura:** `post-launch-review-[feature]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Após cada major launch (4+ semanas pós-deploy) |
| Aprovadores | Design Lead, PM |
| Repositório | `/squads/design/tasks/review/` |

## Cross-References
- [Post-Release Review](../handoff/post-release-review.md)
- [QA with Engineering](../handoff/qa-with-engineering.md)
- [Analyze Analytics for UX](../research/analyze-analytics-for-ux.md)
- [Design Debt Prioritization](../operations/design-debt-prioritization.md)
- [Quarterly Design Review](../operations/quarterly-design-review.md)
- [Design Backlog Grooming](../operations/design-backlog-grooming.md)
