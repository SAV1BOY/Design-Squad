# Update Design System Docs

## Metadata
- **Categoria:** Operations
- **Complexidade:** Média
- **Tempo Estimado:** 2-5 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** operations, documentation, design-system, maintenance, knowledge-base

## Objective
Manter a documentação do design system atualizada, completa e acessível, refletindo o estado
atual de componentes, tokens, patterns e guidelines. A documentação é o ponto de entrada para
consumidores do DS e deve ser tratada como produto.

## Prerequisites
- Release notes da última versão do DS disponíveis
- Acesso ao site/plataforma de documentação do DS (Storybook, ZeroHeight, Notion)
- Inventory de componentes e tokens atualizado
- Feedback de consumidores sobre gaps na documentação
- Template de documentação de componente padronizado

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design System Lead | Coordenar atualização e revisar conteúdo |
| Technical Writer / Content Designer | Redigir e editar documentação |
| Frontend Engineer (DS) | Atualizar code examples e API docs |
| Design Ops | Monitorar completude e coletar feedback de consumidores |

## Frameworks
- **Documentation-as-Product** — tratar docs como produto com UX e manutenção
- **Component Doc Template** — estrutura padronizada por componente
- **Content Audit** — avaliação de completude e atualidade do conteúdo existente
- **Search Analytics** — dados de busca para identificar gaps de conteúdo
- **Versioned Documentation** — docs versionados alinhados com releases do DS

## Checklists
- [ ] Content audit executado: identificar docs desatualizados e gaps
- [ ] Release notes da última versão refletidas na documentação
- [ ] Novos componentes documentados com template completo
- [ ] Componentes atualizados com specs revisadas
- [ ] Code examples atualizados e funcionando
- [ ] Screenshots e visual examples atualizados
- [ ] Links internos verificados (sem broken links)
- [ ] Feedback de consumidores incorporado
- [ ] Search analytics revisados para identificar gaps
- [ ] Documentação publicada e comunicada

## Steps
1. **Executar content audit** — Revisar toda a documentação existente. Marcar como: atualizado,
   desatualizado, incompleto ou ausente. Gerar lista de ações necessárias.

2. **Priorizar atualizações** — Ordenar por: componentes mais usados, feedback recebido de
   consumidores e impacto da desatualização na adoção.

3. **Atualizar docs de componentes** — Para cada componente com mudanças, atualizar: props/API,
   variantes, estados, guidelines de uso, Do/Don't e code examples.

4. **Documentar novos componentes** — Para componentes recém-adicionados, criar documentação
   completa seguindo template: overview, anatomy, API, usage, a11y, examples.

5. **Atualizar visual assets** — Renovar screenshots, previews e diagramas de anatomia para
   refletir o estado atual dos componentes.

6. **Atualizar code examples** — Com Frontend Engineer, revisar e testar todos os code examples.
   Garantir que compilam e renderizam corretamente na versão atual.

7. **Verificar links e navegação** — Testar todos os links internos e externos. Corrigir broken
   links e garantir que a navegação da documentação é intuitiva.

8. **Incorporar feedback** — Revisar feedback recebido de consumidores (surveys, issues, Slack).
   Endereçar perguntas frequentes com conteúdo novo ou revisado.

9. **Publicar e comunicar** — Deployar documentação atualizada. Comunicar mudanças significativas
   via canal do DS. Incluir highlights na próxima newsletter do squad.

## Output
- **Updated Documentation** — Documentação do DS atualizada e publicada
- **Content Audit Report** — Status de cada página: updated, needs-update, new
- **Changelog** — Lista de páginas atualizadas e criadas
- **Formato:** Site de documentação + Markdown source
- **Nomenclatura:** `ds-docs-update-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design System Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | A cada release do DS ou mensal |
| Aprovadores | Design System Lead |
| Repositório | `/squads/design/tasks/operations/` |

## Cross-References
- [Publish Library](../design-system/publish-library.md)
- [Create Component Spec](../design-system/create-component-spec.md)
- [Adoption and Migration](../design-system/adoption-and-migration.md)
- [Build Research Repository](../research/build-research-repository.md)
- [Onboard New Designer](./onboard-new-designer.md)
