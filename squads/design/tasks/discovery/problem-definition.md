# Problem Definition

## Metadata
- **Categoria:** Discovery
- **Complexidade:** Alta
- **Tempo Estimado:** 3-5 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** discovery, problem-framing, alignment, strategy

## Objective
Definir com clareza o problema de design a ser resolvido, garantindo alinhamento entre stakeholders,
produto e design antes de iniciar qualquer exploração de solução. O artefato final deve servir como
referência única (single source of truth) durante todo o ciclo de projeto.

## Prerequisites
- Acesso ao backlog de produto e roadmap atualizado
- Briefing inicial do Product Manager ou sponsor do projeto
- Dados qualitativos ou quantitativos que evidenciem o problema
- Acesso a ferramentas de documentação (Notion, Confluence ou equivalente)
- Contexto de negócio e métricas atuais (KPIs relevantes)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design Lead | Facilitar workshops de framing e consolidar o documento final |
| Product Manager | Fornecer contexto de negócio, restrições e priorização |
| UX Researcher | Trazer evidências de pesquisa e dados de comportamento do usuário |
| Tech Lead | Sinalizar restrições técnicas e viabilidade |
| Stakeholder | Validar escopo e aprovar definição final |

## Frameworks
- **How Might We (HMW)** — para reformular o problema em oportunidades de design
- **5 Whys** — para identificar a causa-raiz do problema
- **Problem Statement Canvas** — para estruturar contexto, usuário, dor e impacto
- **Jobs To Be Done (JTBD)** — para articular a motivação do usuário
- **Impact x Effort Matrix** — para priorizar sub-problemas quando aplicável

## Checklists
- [ ] Briefing de produto recebido e lido por todos os participantes
- [ ] Workshop de framing agendado e facilitado
- [ ] Hipóteses de problema documentadas
- [ ] Causa-raiz identificada via 5 Whys ou análise equivalente
- [ ] Problem Statement redigido no formato padronizado
- [ ] Métricas de sucesso definidas (leading e lagging indicators)
- [ ] Documento revisado por PM e Tech Lead
- [ ] Aprovação formal do stakeholder registrada
- [ ] Documento publicado no repositório do squad

## Steps
1. **Coletar contexto inicial** — Reunir briefing de produto, dados de analytics, tickets de suporte
   e qualquer pesquisa prévia relacionada ao tema. Organizar em um documento de intake.

2. **Mapear stakeholders e expectativas** — Identificar todos os envolvidos e registrar suas
   expectativas, restrições e definição de sucesso para o projeto.

3. **Facilitar workshop de Problem Framing** — Conduzir sessão colaborativa utilizando o Problem
   Statement Canvas. Duração recomendada: 90 minutos com todos os agents listados.

4. **Aplicar 5 Whys na causa-raiz** — Partindo dos sintomas identificados, executar o exercício
   de 5 Whys para cada hipótese de problema levantada no workshop.

5. **Redigir Problem Statement** — Consolidar os achados em um statement claro seguindo o formato:
   "[Usuário] precisa de [necessidade] porque [insight], mas atualmente [barreira]."

6. **Definir métricas de sucesso** — Estabelecer de 2 a 4 métricas mensuráveis que indicarão se
   o problema foi resolvido. Incluir baseline atual e target desejado.

7. **Gerar perguntas HMW** — Transformar o problem statement em 3-5 perguntas How Might We que
   guiarão a fase de ideação subsequente.

8. **Revisar e validar com stakeholders** — Apresentar o documento consolidado para PM, Tech Lead
   e sponsor. Incorporar feedback e obter aprovação formal.

9. **Publicar e comunicar** — Disponibilizar o documento final no repositório do squad e comunicar
   via canal do Slack para visibilidade cross-squad.

## Output
- **Problem Definition Document** — Documento estruturado contendo: contexto, problem statement,
  causa-raiz, métricas de sucesso, perguntas HMW e aprovações
- **Formato:** Markdown no repositório ou página no Notion/Confluence
- **Nomenclatura:** `problem-definition-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por projeto (início de cada discovery) |
| Aprovadores | PM, Design Lead, Stakeholder |
| Repositório | `/squads/design/tasks/discovery/` |

## Cross-References
- [Stakeholder Interviews](./stakeholder-interviews.md)
- [Opportunity Framing](./opportunity-framing.md)
- [Competitive UI Audit](./competitive-ui-audit.md)
- [Create Personas or JTBD](../ux/create-personas-or-jtbd.md)
- [Design Backlog Grooming](../operations/design-backlog-grooming.md)
- [Synthesize Insights](../research/synthesize-insights.md)
