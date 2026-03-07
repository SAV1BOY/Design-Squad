# Run Card Sort

## Metadata
- **Categoria:** Research
- **Complexidade:** Média
- **Tempo Estimado:** 3-5 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** research, card-sort, information-architecture, navigation, mental-model

## Objective
Conduzir sessões de card sorting (aberto, fechado ou híbrido) para compreender como os usuários
categorizam e agrupam informações. Os resultados informam decisões de information architecture,
navegação e taxonomia do produto.

## Prerequisites
- Lista de conteúdos ou funcionalidades a serem organizadas (30-60 cards)
- Tipo de card sort definido (aberto, fechado ou híbrido)
- Ferramenta de card sort configurada (Optimal Workshop, Maze ou presencial)
- Perfil de participante definido e recrutamento iniciado
- Objetivo de IA claramente articulado (nova IA ou reestruturação)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UX Researcher | Planejar estudo, definir cards, moderar e analisar resultados |
| UX Designer | Colaborar na definição dos cards e aplicar resultados na IA |
| Content Designer | Revisar labels dos cards e garantir clareza da nomenclatura |
| Product Manager | Validar escopo de conteúdos incluídos no estudo |

## Frameworks
- **Open Card Sort** — participantes criam categorias livremente
- **Closed Card Sort** — participantes organizam cards em categorias pré-definidas
- **Hybrid Card Sort** — categorias pré-definidas com opção de criar novas
- **Dendrogram Analysis** — para identificar agrupamentos hierárquicos nos dados
- **Similarity Matrix** — para visualizar frequência de co-ocorrência entre cards

## Checklists
- [ ] Tipo de card sort selecionado e justificado
- [ ] Lista de cards redigida e revisada por Content Designer
- [ ] Categorias pré-definidas criadas (se fechado ou híbrido)
- [ ] Ferramenta configurada e testada
- [ ] Piloto realizado com 2-3 participantes internos
- [ ] 15-30 participantes recrutados
- [ ] Sessões executadas (remotas ou presenciais)
- [ ] Dados exportados e analisados (dendrogram + similarity matrix)
- [ ] Relatório com recomendações de IA elaborado
- [ ] Resultados apresentados ao squad

## Steps
1. **Definir tipo e objetivo** — Escolher entre card sort aberto (discovery de IA), fechado
   (validação de IA existente) ou híbrido. Documentar objetivo e como os dados serão usados.

2. **Criar lista de cards** — Selecionar 30-60 itens representativos do conteúdo ou funcionalidades
   do produto. Cada card deve ter label claro e, se necessário, descrição curta.

3. **Revisar nomenclatura** — Com o Content Designer, garantir que os labels são compreensíveis,
   sem jargão interno e consistentes em formato e nível de abstração.

4. **Configurar ferramenta** — Montar o estudo na ferramenta escolhida. Incluir instruções
   claras para o participante e mensagem de agradecimento ao final.

5. **Executar piloto** — Rodar com 2-3 colegas internos para verificar clareza das instruções,
   tempo necessário e funcionamento técnico. Ajustar conforme feedback.

6. **Recrutar e executar** — Distribuir para 15-30 participantes. Monitorar taxa de completude
   e enviar lembretes se necessário. Prazo típico de coleta: 3-5 dias.

7. **Analisar dados** — Gerar dendrogram e similarity matrix. Identificar agrupamentos naturais,
   cards problemáticos (frequentemente movidos entre grupos) e outliers.

8. **Interpretar e recomendar** — Traduzir achados em recomendações concretas de IA: estrutura
   de navegação, nomenclatura de categorias e hierarquia de conteúdo.

9. **Documentar e compartilhar** — Redigir relatório com metodologia, dados visuais e
   recomendações. Apresentar ao squad em sessão colaborativa.

## Output
- **Card Sort Report** — Relatório com análise de dendrogram, similarity matrix e recomendações
- **IA Recommendations** — Proposta de estrutura de navegação baseada nos dados
- **Formato:** Markdown + exports da ferramenta de análise
- **Nomenclatura:** `card-sort-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UX Researcher |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por projeto de IA ou reestruturação de navegação |
| Aprovadores | Design Lead, UX Designer |
| Repositório | `/squads/design/tasks/research/` |

## Cross-References
- [Run Tree Test](./run-tree-test.md)
- [Build IA and Sitemap](../ux/build-ia-and-sitemap.md)
- [Synthesize Insights](./synthesize-insights.md)
- [Content Design Microcopy](../ux/content-design-microcopy.md)
- [Build Research Repository](./build-research-repository.md)
