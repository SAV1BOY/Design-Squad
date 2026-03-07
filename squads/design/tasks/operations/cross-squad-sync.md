# Cross-Squad Sync

## Metadata
- **Categoria:** Operations
- **Complexidade:** Baixa-Média
- **Tempo Estimado:** 1-2 horas por sessão (bi-semanal ou mensal)
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** operations, cross-squad, sync, alignment, collaboration, dependencies

## Objective
Coordenar o alinhamento entre o design squad e outros squads (engenharia, produto, outros design
squads) para resolver dependências, compartilhar decisões de design impactantes, evitar trabalho
duplicado e garantir consistência cross-product.

## Prerequisites
- Calendário de syncs recorrentes estabelecido com squads relevantes
- Agenda template preparada para cada tipo de sync
- Board de dependências cross-squad visível e atualizado
- Canal de comunicação assíncrona configurado (Slack)
- Representantes de cada squad confirmados

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design Lead | Representar o squad, comunicar decisões e resolver conflitos |
| Design Ops | Preparar agenda, documentar decisões e follow up de ações |
| Product Manager | Alinhar prioridades de produto entre squads |
| Design Leads (outros squads) | Compartilhar contexto e resolver dependências |
| Tech Lead | Participar quando há dependências técnicas |

## Frameworks
- **Dependency Map** — visualização de dependências entre squads
- **RACI por Decisão** — quem é Responsible, Accountable, Consulted, Informed
- **Decision Log** — registro de decisões tomadas em syncs
- **Async-First Communication** — priorizar comunicação assíncrona quando possível
- **Conflict Resolution Protocol** — escalation path para desacordos

## Checklists
- [ ] Agenda preparada e compartilhada 24h antes do sync
- [ ] Dependências atuais mapeadas e status atualizado
- [ ] Decisões de design com impacto cross-squad identificadas
- [ ] Conflitos de prioridade ou design sinalizados previamente
- [ ] Sync conduzido dentro do timebox (30-45 min)
- [ ] Decisões documentadas e comunicadas via canal assíncrono
- [ ] Action items atribuídos com owner e deadline
- [ ] Follow up de ações da sessão anterior verificado
- [ ] Riscos de inconsistência cross-product identificados

## Steps
1. **Preparar agenda** — Design Ops compila: updates do squad, dependências a resolver, decisões
   a comunicar e conflitos a endereçar. Compartilhar 24h antes.

2. **Atualizar dependency map** — Antes do sync, revisar e atualizar o mapa de dependências:
   o que precisamos de outros squads e o que eles precisam de nós.

3. **Conduzir sync** — Design Lead facilita sessão de 30-45 minutos. Estrutura: updates rápidos
   (5 min/squad), dependências (15 min), decisões/conflitos (15 min).

4. **Compartilhar decisões de design** — Comunicar decisões recentes que impactam outros squads:
   mudanças no DS, novos patterns, alterações de IA ou UI compartilhada.

5. **Resolver dependências** — Para cada dependência ativa, alinhar: status, próximo passo,
   owner e deadline. Escalar se não houver resolução no sync.

6. **Verificar consistência** — Identificar áreas onde squads diferentes podem estar projetando
   soluções divergentes para problemas similares. Alinhar abordagem.

7. **Documentar decisões** — Registrar todas as decisões no Decision Log com: contexto, decisão,
   rationale, impacto e pessoas informadas.

8. **Comunicar via canal assíncrono** — Postar resumo do sync no canal compartilhado para
   visibilidade dos membros que não participaram da sessão.

## Output
- **Sync Notes** — Resumo da sessão com updates, decisões e action items
- **Updated Dependency Map** — Mapa de dependências atualizado
- **Decision Log Entry** — Registro de decisões tomadas
- **Formato:** Markdown + Slack post + dependency board
- **Nomenclatura:** `cross-squad-sync-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design Ops |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Bi-semanal ou mensal (conforme volume de dependências) |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/operations/` |

## Cross-References
- [Weekly Design Ops Cadence](./weekly-design-ops-cadence.md)
- [Quarterly Design Review](./quarterly-design-review.md)
- [Adoption and Migration](../design-system/adoption-and-migration.md)
- [Create Service Blueprint](../ux/create-service-blueprint.md)
- [Dev Handoff](../handoff/dev-handoff.md)
