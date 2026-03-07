# Design Backlog Grooming

## Metadata
- **Categoria:** Operations
- **Complexidade:** Média
- **Tempo Estimado:** 2-3 horas por sessão (bi-semanal)
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** operations, backlog, grooming, prioritization, planning

## Objective
Manter o design backlog organizado, priorizado e acionável através de sessões regulares de
grooming. O processo garante que o squad trabalha sempre nas tarefas de maior impacto, que novos
itens são triados rapidamente e que o backlog reflete a realidade atual do roadmap.

## Prerequisites
- Design backlog configurado em ferramenta de gestão (Jira, Linear, Notion)
- Product roadmap acessível e atualizado
- Critérios de priorização definidos e acordados com PM
- Design Lead e PM disponíveis para sessão bi-semanal
- Inputs de pesquisa, audits e reviews para alimentar o backlog

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design Lead | Facilitar grooming, priorizar e atribuir tasks |
| Design Ops | Manter backlog limpo, atualizar status e gerar métricas |
| Product Manager | Fornecer contexto de roadmap e prioridades de negócio |
| UX Researcher | Trazer inputs de pesquisa para informar priorização |
| Designers do squad | Estimar esforço e levantar dependências |

## Frameworks
- **RICE Scoring** — Reach, Impact, Confidence, Effort para priorização
- **MoSCoW** — Must have, Should have, Could have, Won't have
- **Design Debt Quadrant** — categorização de debt por impacto x esforço
- **T-Shirt Sizing** — estimativa de esforço: XS, S, M, L, XL
- **Kanban Flow** — backlog > ready > in progress > review > done

## Checklists
- [ ] Novos itens triados e descritos com contexto mínimo
- [ ] Itens sem movimentação há 30+ dias revisados (archive ou re-priorize)
- [ ] Priorização RICE ou MoSCoW aplicada aos top 20 itens
- [ ] Estimativa de esforço (T-Shirt) definida para itens no topo
- [ ] Dependências entre itens mapeadas e documentadas
- [ ] Itens de design debt revisados e posicionados no backlog
- [ ] Backlog alinhado com roadmap atual do produto
- [ ] Próximas 2 semanas de trabalho definidas (sprint-ready)
- [ ] Itens bloqueados identificados com owner para desbloqueio
- [ ] Métricas de throughput e lead time atualizadas

## Steps
1. **Triar novos itens** — Revisar itens adicionados desde o último grooming. Garantir que cada
   item tem: descrição, contexto, solicitante e categoria (feature, debt, research).

2. **Revisar itens estagnados** — Identificar itens sem movimentação há 30+ dias. Decidir:
   manter com nova prioridade, arquivar ou remover do backlog.

3. **Atualizar prioridades** — Aplicar RICE scoring nos top 20-30 itens. Reordenar backlog
   conforme novos scores. Considerar mudanças no roadmap e insights de pesquisa.

4. **Estimar esforço** — Para os 10-15 itens mais prioritários, definir T-Shirt sizing com
   input dos designers que provavelmente executarão o trabalho.

5. **Mapear dependências** — Identificar itens que dependem de: engenharia, pesquisa, decisão
   de produto ou outro squad. Documentar e comunicar dependências.

6. **Integrar design debt** — Revisar itens de design debt pendentes. Posicionar no backlog
   de acordo com severidade e oportunidade (ex: debt em área sendo redesenhada).

7. **Definir sprint-ready items** — Selecionar itens para as próximas 2 semanas considerando:
   prioridade, capacidade do squad, dependências resolvidas e blockers.

8. **Comunicar plano** — Compartilhar com o squad e PM: o que será trabalhado nas próximas 2
   semanas, o que foi re-priorizado e blockers pendentes.

9. **Atualizar métricas** — Registrar: throughput (itens concluídos), lead time (tempo do
   backlog ao done), WIP (work in progress) e burn rate de design debt.

## Output
- **Groomed Backlog** — Backlog priorizado e estimado
- **Sprint Plan** — Itens selecionados para as próximas 2 semanas
- **Metrics Update** — Throughput, lead time e WIP atualizados
- **Formato:** Board online + Slack update
- **Nomenclatura:** `backlog-grooming-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design Lead + Design Ops |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Bi-semanal |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/operations/` |

## Cross-References
- [Weekly Design Ops Cadence](./weekly-design-ops-cadence.md)
- [Design Debt Prioritization](./design-debt-prioritization.md)
- [Opportunity Framing](../discovery/opportunity-framing.md)
- [Post-Launch Design Review](../review/post-launch-design-review.md)
- [Quarterly Design Review](./quarterly-design-review.md)
