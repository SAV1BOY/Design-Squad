# Build Research Repository

## Metadata
- **Categoria:** Research
- **Complexidade:** Alta
- **Tempo Estimado:** 5-10 dias (setup inicial), contínuo após
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** research, repository, knowledge-management, atomic-research, ops

## Objective
Criar e manter um repositório centralizado de pesquisa que armazene, organize e torne acessíveis
todos os insights, artefatos e evidências gerados pelo squad. O repository elimina pesquisa
duplicada, democratiza o acesso ao conhecimento e acelera decisões de design baseadas em evidência.

## Prerequisites
- Ferramenta de repository definida (Dovetail, Notion, Airtable ou equivalente)
- Taxonomia de tags e categorias acordada pelo squad
- Template de Atomic Research Nuggets definido
- Governança de acesso e permissões configurada
- Backlog de pesquisas anteriores para migração inicial

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UX Researcher | Projetar estrutura, definir taxonomia e liderar setup |
| Design Ops | Configurar ferramenta, automações e integrações |
| Design Lead | Aprovar estrutura e promover adoção no squad |
| Todos os designers | Contribuir com inputs e consultar o repository regularmente |

## Frameworks
- **Atomic Research** — estrutura de nuggets: Evidence > Fact > Insight > Recommendation
- **LATCH (Richard Saul Wurman)** — princípios de organização: Location, Alphabet, Time,
  Category, Hierarchy
- **Knowledge Management Lifecycle** — criação, organização, acesso, manutenção, arquivamento
- **Tagging Taxonomy** — sistema hierárquico de classificação por temas

## Checklists
- [ ] Ferramenta selecionada e configurada
- [ ] Taxonomia de tags e categorias documentada
- [ ] Templates de nuggets e estudos criados
- [ ] Permissões e governança de acesso configuradas
- [ ] 3-5 estudos existentes migrados como referência
- [ ] Guia de contribuição redigido e compartilhado
- [ ] Sessão de onboarding realizada com o squad
- [ ] Processo de manutenção e higiene definido
- [ ] Métricas de adoção configuradas (consultas, contribuições)
- [ ] Revisão trimestral de saúde do repository agendada

## Steps
1. **Definir requisitos** — Levantar com o squad: tipos de artefatos, volume esperado, integrações
   necessárias, níveis de acesso e expectativas de busca e filtragem.

2. **Selecionar ferramenta** — Avaliar opções (Dovetail, Notion, Airtable) contra requisitos.
   Considerar: custo, integrações, busca, tagging e facilidade de contribuição.

3. **Projetar taxonomia** — Definir sistema de tags hierárquico cobrindo: tipo de estudo, método,
   produto/feature, persona, fase do projeto, tema e confiança do insight.

4. **Criar templates** — Desenvolver templates para: estudo completo, atomic nugget, highlight
   clip e artefato de síntese. Garantir campos obrigatórios e opcionais claros.

5. **Configurar ferramenta** — Montar estrutura na ferramenta escolhida: databases, views,
   templates, automações de tagging e integrações com outras ferramentas do squad.

6. **Migrar estudos existentes** — Selecionar 3-5 estudos recentes e migrá-los como referência.
   Extrair nuggets atômicos de cada estudo para popular o repository.

7. **Redigir guia de contribuição** — Documentar: como adicionar um estudo, como criar nuggets,
   convenções de tagging, processo de review e frequência de contribuição esperada.

8. **Onboarding do squad** — Conduzir sessão de 45 minutos demonstrando o repository, fluxo de
   contribuição e benefícios. Responder dúvidas e coletar feedback.

9. **Definir processo de manutenção** — Estabelecer rotina mensal de higiene: revisar tags
   inconsistentes, arquivar estudos obsoletos e verificar qualidade dos nuggets.

10. **Monitorar adoção** — Acompanhar métricas de uso: contribuições por mês, consultas, nuggets
    citados em decisões de design. Ajustar processo conforme feedback contínuo.

## Output
- **Research Repository** — Plataforma configurada e populada com estudos e nuggets
- **Contribution Guide** — Documento de referência para contribuidores
- **Taxonomy Document** — Estrutura de tags e categorias do repository
- **Formato:** Ferramenta configurada + documentação em Markdown
- **Nomenclatura:** `research-repository-setup-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UX Researcher + Design Ops |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Setup único + manutenção contínua (mensal) |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/research/` |

## Cross-References
- [Synthesize Insights](./synthesize-insights.md)
- [Plan and Run Interviews](./plan-and-run-interviews.md)
- [Run Usability Test](./run-usability-test.md)
- [Survey and Analysis](./survey-and-analysis.md)
- [Update Design System Docs](../operations/update-design-system-docs.md)
- [Onboard New Designer](../operations/onboard-new-designer.md)
