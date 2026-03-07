# Information Architecture — Louis Rosenfeld, Peter Morville, Jorge Arango



## Metadata

- **Autores:** Louis Rosenfeld, Peter Morville, Jorge Arango
- **Publicacao:** 1998 (4a edicao: 2015)
- **Categoria:** Information Architecture, Content Strategy
- **Relevancia para o Squad:** Alta — estruturação de conteúdo e navegação
- **Ultima revisao:** 2026-03-06



## Summary

Conhecido como o "Polar Bear Book" pela capa icônica, Information Architecture é a referência definitiva sobre como organizar, estruturar e rotular conteúdo em ambientes digitais. Rosenfeld, Morville e Arango definem IA como a combinação de quatro sistemas: organização, rotulação, navegação e busca — todos trabalhando juntos para tornar informação encontrável e compreensível.

O livro aborda IA como disciplina que conecta necessidades do usuário, conteúdo disponível e contexto organizacional. A quarta edição expande significativamente a cobertura de IA para ecossistemas multiplataforma, reconhecendo que informação hoje flui entre web, mobile, assistentes de voz e dispositivos IoT.

Os autores enfatizam que IA não é apenas sobre sitemaps e taxonomias — é sobre criar estruturas que façam sentido para os usuários, baseadas em seus modelos mentais, não na estrutura interna da organização. Research com card sorting, tree testing e análise de busca interna são métodos centrais.



## Key Concepts


### 1. Four Systems of IA (Organization, Labeling, Navigation, Search)

Organization systems definem como conteúdo é categorizado (hierárquico, facetado, cronológico). Labeling systems definem como categorias e links são nomeados. Navigation systems definem como o usuário se move (global, local, contextual, supplemental). Search systems definem como encontrar conteúdo por query.


### 2. Findability e Understandability

Dois critérios de sucesso de IA: o usuário encontra o que procura (findability) e entende o que encontrou (understandability). Boa navegação resolve findability; boa rotulação e organização resolvem understandability. Ambos são necessários.


### 3. Top-Down vs. Bottom-Up IA

Top-down IA é projetada intencionalmente (taxonomias, hierarquias, menus). Bottom-up IA emerge do conteúdo (tags, search, cross-links). Sistemas eficazes combinam ambos — estrutura intencional para navegação com emergência para descoberta.


### 4. Card Sorting e Tree Testing

Card sorting (aberto e fechado) revela como usuários agrupam e nomeam conceitos — informando taxonomias e labels. Tree testing valida se a estrutura de navegação permite que usuários encontrem conteúdo sem ajuda visual. Ambos são métodos baratos e poderosos para IA.


### 5. Cross-Channel IA

IA para ecossistemas onde a mesma informação existe em múltiplos canais (web, mobile, email, chatbot). O desafio é manter consistência de estrutura e rotulação sem forçar a mesma navegação em contextos diferentes. Cada canal tem constraints próprios mas a IA subjacente deve ser coerente.



## Application to Design Squad

- **IA audit periódico:** Trimestralmente, auditar a arquitetura de informação do produto: a navegação reflete o modelo mental do usuário? As labels são compreensíveis? A busca retorna resultados relevantes?
- **Card sorting para novas features:** Antes de definir a navegação de features complexas, conduzir card sorting com usuários para validar agrupamentos e nomenclatura.
- **Label consistency:** Manter glossário de labels aprovados no design system. O mesmo conceito deve ter o mesmo rótulo em todas as telas.
- **Search analytics:** Monitorar os termos mais buscados e os que retornam zero resultados. Search queries revelam gaps na IA.
- **Sitemap como artefato vivo:** Manter sitemap atualizado do produto como referência para todo o squad, revisado a cada mudança significativa de navegação.



## Key Takeaways

1. **IA é invisível quando funciona.** O sucesso é medido pela ausência de confusão, não pela presença de features.

2. **Labels são a parte mais negligenciada e impactante da IA.** Um menu com labels incompreensíveis é tão ruim quanto sem menu.

3. **Estruture para o modelo mental do usuário, não para a org chart.** Se o menu espelha departamentos internos em vez de tarefas do usuário, a IA está errada.

4. **Busca não substitui boa navegação.** Usuários que dependem de busca geralmente falharam na navegação primeiro.

5. **Teste a estrutura antes de investir no visual.** Tree testing valida IA sem custo de design visual.



## Cross-References

- [Elements of UX — Garrett](garrett-elements-of-ux.md) — IA como parte do plano Structure
- [Mental Models — Young](young-mental-models.md) — entender modelos mentais que informam IA
- [Navigation Patterns](../ui-patterns/navigation-patterns.md) — implementação visual da IA
- [Search and Filter Patterns](../ui-patterns/search-and-filter-patterns.md) — padrões de busca e filtragem
- [Don't Make Me Think — Krug](krug-dont-make-me-think.md) — usabilidade de navegação
