# Build IA and Sitemap

## Metadata
- **Categoria:** UX
- **Complexidade:** Alta
- **Tempo Estimado:** 5-8 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** ux, information-architecture, sitemap, navigation, taxonomy

## Objective
Projetar a information architecture do produto definindo estrutura hierárquica, taxonomia,
navegação e relações entre conteúdos. O sitemap resultante serve como blueprint estrutural que
guia o design de navegação, fluxos e organização de conteúdo.

## Prerequisites
- Resultados de card sort e/ou tree test disponíveis (se realizados)
- Inventário de conteúdo ou funcionalidades do produto
- Personas ou JTBD definidos para contextualizar modelos mentais
- Requisitos de negócio e product roadmap acessíveis
- Ferramenta de diagramação configurada (FigJam, Miro, OmniGraffle)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UX Designer | Projetar IA, criar sitemap e documentar decisões |
| Content Designer | Definir taxonomia, labels e convenções de nomenclatura |
| UX Researcher | Fornecer dados de card sort, tree test e mental models |
| Product Manager | Validar escopo de conteúdo e prioridades de negócio |
| Tech Lead | Avaliar viabilidade técnica da estrutura proposta |

## Frameworks
- **LATCH** — Location, Alphabet, Time, Category, Hierarchy
- **Top-Down vs Bottom-Up IA** — abordagens complementares de estruturação
- **Object-Oriented UX (OOUX)** — para identificar objetos-chave e suas relações
- **Navigation Patterns** — global nav, local nav, contextual nav, breadcrumbs
- **Controlled Vocabulary** — para padronizar terminologia

## Checklists
- [ ] Inventário de conteúdo/funcionalidades completo
- [ ] Dados de pesquisa de IA revisados (card sort, tree test)
- [ ] Objetos-chave identificados via OOUX (se aplicável)
- [ ] Estrutura hierárquica de 2-4 níveis definida
- [ ] Labels de navegação revisados por Content Designer
- [ ] Sitemap visual criado e versionado
- [ ] Padrões de navegação definidos (global, local, contextual)
- [ ] Validação com tree test executada (se tempo permitir)
- [ ] Sitemap aprovado por PM e Tech Lead
- [ ] Documentação de decisões de IA registrada

## Steps
1. **Inventariar conteúdo** — Listar todos os conteúdos, funcionalidades e objetos que o produto
   precisa organizar. Classificar por tipo, importância e frequência de acesso.

2. **Revisar dados de pesquisa** — Analisar resultados de card sort, tree test e entrevistas
   para entender modelos mentais dos usuários e padrões de agrupamento.

3. **Identificar objetos-chave** — Usando OOUX, definir os objetos principais do sistema, seus
   atributos, relações e ações associadas (CTAs por objeto).

4. **Definir estrutura hierárquica** — Organizar conteúdo em hierarquia de 2-4 níveis. Balancear
   profundidade (muitos cliques) vs largura (muitas opções por nível).

5. **Criar sitemap visual** — Diagramar a estrutura usando ferramenta visual. Incluir: páginas,
   seções, links entre áreas e indicações de navegação contextual.

6. **Definir padrões de navegação** — Especificar: navegação global (sempre visível), local
   (por seção), contextual (inline) e auxiliar (busca, breadcrumbs, atalhos).

7. **Revisar labels com Content Designer** — Garantir que todos os labels são claros, consistentes,
   seguem convenções do produto e evitam jargão técnico.

8. **Validar com stakeholders** — Apresentar sitemap para PM e Tech Lead. Confirmar que a
   estrutura atende requisitos de negócio e é tecnicamente viável.

9. **Documentar decisões** — Registrar decisões de IA com justificativas: por que certos itens
   estão agrupados, trade-offs considerados e riscos identificados.

## Output
- **Sitemap** — Diagrama visual da estrutura hierárquica completa
- **IA Spec Document** — Documento com taxonomia, labels, decisões e justificativas
- **Navigation Model** — Especificação dos padrões de navegação por área
- **Formato:** FigJam/Miro + Markdown para documentação
- **Nomenclatura:** `ia-sitemap-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UX Designer |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por projeto ou reestruturação major |
| Aprovadores | Design Lead, PM, Tech Lead |
| Repositório | `/squads/design/tasks/ux/` |

## Cross-References
- [Run Card Sort](../research/run-card-sort.md)
- [Run Tree Test](../research/run-tree-test.md)
- [Design User Flows](./design-user-flows.md)
- [Content Design Microcopy](./content-design-microcopy.md)
- [Wireframe Pack](./wireframe-pack.md)
- [Create Personas or JTBD](./create-personas-or-jtbd.md)
