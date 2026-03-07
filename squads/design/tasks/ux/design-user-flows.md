# Design User Flows

## Metadata
- **Categoria:** UX
- **Complexidade:** Média
- **Tempo Estimado:** 3-5 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** ux, user-flows, interaction-design, task-analysis, flowchart

## Objective
Mapear e documentar os fluxos de interação do usuário com o produto, detalhando cada etapa,
decisão e estado do sistema. Os user flows garantem que todos os caminhos (happy path e edge cases)
estão cobertos antes de avançar para wireframing e design visual.

## Prerequisites
- Information Architecture e sitemap definidos
- Personas ou JTBD documentados
- Requisitos funcionais mapeados com PM
- Ferramenta de fluxograma configurada (FigJam, Miro, Whimsical)
- Edge cases e estados de erro levantados com Tech Lead

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UX Designer | Mapear fluxos, identificar edge cases e documentar decisões |
| Product Manager | Validar requisitos funcionais e regras de negócio |
| Tech Lead | Informar restrições técnicas, estados do sistema e APIs |
| Content Designer | Definir mensagens de feedback, erro e empty states |
| Design Lead | Revisar completude e consistência dos fluxos |

## Frameworks
- **Task Flow** — sequência linear de passos para uma tarefa específica
- **User Flow** — fluxo completo incluindo decisões e bifurcações
- **Swim Lane Diagram** — para fluxos com múltiplos atores ou sistemas
- **State Diagram** — para mapear transições de estado do sistema
- **Error Flow Mapping** — para documentar todos os caminhos de erro

## Checklists
- [ ] Tarefas críticas do usuário priorizadas para mapeamento
- [ ] Happy path documentado para cada tarefa
- [ ] Edge cases e fluxos alternativos identificados
- [ ] Estados de erro e recovery mapeados
- [ ] Empty states e first-time experiences contemplados
- [ ] Loading states e feedback do sistema documentados
- [ ] Fluxos revisados por PM (regras de negócio) e Tech Lead (viabilidade)
- [ ] Nomenclatura e numeração padronizadas
- [ ] Fluxos aprovados e versionados no repositório

## Steps
1. **Priorizar tarefas-chave** — Selecionar as 5-10 tarefas mais críticas do usuário com base
   em frequência de uso, impacto de negócio e complexidade de interação.

2. **Mapear happy path** — Para cada tarefa, documentar o caminho ideal do início ao fim:
   entry point, cada passo, inputs necessários, feedback do sistema e conclusão.

3. **Identificar pontos de decisão** — Mapear onde o usuário ou sistema faz escolhas que
   bifurcam o fluxo. Documentar as condições de cada branch.

4. **Mapear edge cases** — Para cada ponto de decisão, explorar: e se o usuário erra? E se o
   sistema falha? E se não há dados? Documentar cada cenário alternativo.

5. **Definir estados do sistema** — Mapear: loading, success, error, empty, partial e offline
   para cada tela relevante. Especificar transições entre estados.

6. **Criar diagramas visuais** — Usar notação padronizada: retângulos para telas, losangos para
   decisões, setas para transições. Incluir anotações para regras de negócio.

7. **Revisar com PM e Tech Lead** — Validar que todos os fluxos respeitam regras de negócio e
   são tecnicamente viáveis. Documentar feedback e ajustar.

8. **Definir mensagens de feedback** — Com Content Designer, redigir microcopy para: confirmações,
   erros, empty states e instruções contextuais em cada fluxo.

9. **Versionar e publicar** — Organizar fluxos em arquivo Figma ou board dedicado. Numerar e
   nomear consistentemente. Compartilhar com squad para referência.

## Output
- **User Flow Diagrams** — Diagramas visuais de todos os fluxos priorizados
- **Edge Case Matrix** — Tabela de cenários alternativos por fluxo
- **State Inventory** — Lista de estados do sistema por tela
- **Formato:** FigJam/Miro + Markdown para documentação de regras
- **Nomenclatura:** `user-flows-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UX Designer |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por projeto ou feature |
| Aprovadores | Design Lead, PM, Tech Lead |
| Repositório | `/squads/design/tasks/ux/` |

## Cross-References
- [Build IA and Sitemap](./build-ia-and-sitemap.md)
- [Wireframe Pack](./wireframe-pack.md)
- [Create Journey Map](./create-journey-map.md)
- [Content Design Microcopy](./content-design-microcopy.md)
- [Dev Handoff](../handoff/dev-handoff.md)
- [Create Service Blueprint](./create-service-blueprint.md)
