# Weekly Design Ops Cadence

## Metadata
- **Categoria:** Operations
- **Complexidade:** Baixa
- **Tempo Estimado:** 3-4 horas por semana (recorrente)
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** operations, cadence, weekly, rituals, design-ops, coordination

## Objective
Manter uma cadência semanal de rituais e operações do design squad que garanta visibilidade do
trabalho, alinhamento de prioridades, remoção de blockers e compartilhamento de conhecimento.
A cadência cria ritmo previsível e reduz overhead de coordenação.

## Prerequisites
- Calendário do squad com slots recorrentes reservados
- Board de acompanhamento de trabalho configurado (Jira, Linear, Notion)
- Canal de comunicação do squad ativo (Slack)
- Template de agenda para cada ritual definido
- Facilitador designado para cada semana (rodízio opcional)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design Lead | Definir pauta, facilitar rituais e remover blockers |
| Design Ops | Preparar materiais, atualizar boards e enviar recaps |
| Todos os designers | Participar ativamente, atualizar status e compartilhar |
| Product Manager | Participar do sync semanal para alinhamento de prioridades |

## Frameworks
- **Weekly Standup (Design)** — atualização rápida: o que fez, o que fará, blockers
- **Design Show & Tell** — compartilhamento informal de work-in-progress
- **Priority Alignment** — confirmação semanal de prioridades com PM
- **Blocker Escalation** — processo para escalar impedimentos rapidamente
- **Weekly Recap** — resumo escrito enviado ao final da semana

## Checklists
- [ ] Monday: preparar agenda e prioridades da semana
- [ ] Monday/Tuesday: conduzir design standup (15-20 min)
- [ ] Wednesday: design critique ou show & tell (30-60 min)
- [ ] Thursday: sync com PM para alignment check (15-30 min)
- [ ] Friday: weekly recap enviado via Slack
- [ ] Board de acompanhamento atualizado por todos os membros
- [ ] Blockers identificados e escalados em até 24h
- [ ] Design backlog revisado para próxima semana
- [ ] Métricas de throughput atualizadas (tasks concluídas)
- [ ] Action items da semana anterior verificados

## Steps
1. **Preparar semana (Monday AM)** — Revisar backlog, confirmar prioridades com PM, preparar
   agenda do standup e identificar tópicos para critique da semana.

2. **Conduzir standup (Monday/Tuesday)** — Reunião de 15-20 minutos. Cada designer: o que
   concluiu, o que fará esta semana, blockers. Design Lead anota blockers.

3. **Resolver blockers** — Após standup, atacar blockers identificados: agendar conversas,
   escalar para PM/Eng Lead ou redistribuir trabalho conforme necessário.

4. **Facilitar critique/show & tell (Wednesday)** — Sessão de 30-60 minutos para um designer
   apresentar WIP e receber feedback. Rotacionar apresentador semanalmente.

5. **Sync com PM (Thursday)** — Reunião de 15-30 minutos para: confirmar que prioridades
   estão alinhadas, antecipar mudanças e planejar semana seguinte.

6. **Atualizar boards** — Garantir que todos os membros atualizaram status de suas tasks no
   board de acompanhamento. Design Ops verifica e cobra pendências.

7. **Enviar weekly recap (Friday)** — Design Ops envia resumo semanal no Slack: trabalho
   concluído, decisões tomadas, blockers resolvidos e preview da próxima semana.

8. **Retrospectiva rápida (mensal)** — Uma vez por mês, dedicar 30 minutos para retrospectiva
   da cadência: o que melhorar nos rituais, o que eliminar, o que adicionar.

## Output
- **Weekly Recap** — Resumo semanal publicado no Slack
- **Updated Board** — Board de acompanhamento atualizado
- **Blocker Log** — Registro de blockers e resoluções
- **Formato:** Slack message + board online + Markdown (se recap detalhado)
- **Nomenclatura:** `weekly-recap-[YYYY]-W[nn]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design Ops |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Semanal (contínuo) |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/operations/` |

## Cross-References
- [Design Backlog Grooming](./design-backlog-grooming.md)
- [Design Critique Session](../review/design-critique-session.md)
- [Cross-Squad Sync](./cross-squad-sync.md)
- [Quarterly Design Review](./quarterly-design-review.md)
- [Design Debt Prioritization](./design-debt-prioritization.md)
