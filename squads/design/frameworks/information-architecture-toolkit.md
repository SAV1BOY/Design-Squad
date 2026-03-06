# Information Architecture Toolkit

## Metadata

- **Origem:** Richard Saul Wurman (1976), evoluido por Rosenfeld & Morville
- **Categoria:** Structural Design Tool
- **Complexidade:** Intermediaria
- **Aplicacao:** Organizacao de conteudo, navegacao, taxonomia, findability
- **Tags:** card-sort, tree-test, navigation, labels, taxonomy, findability, sitemaps

## Concept

Information Architecture (IA) e a disciplina de organizar, estruturar e rotular conteudo de
forma que usuarios consigam encontrar o que precisam e completar suas tarefas. IA nao e
sobre layout visual — e sobre a estrutura logica subjacente que determina como informacao e
agrupada, nomeada e acessada. Uma IA ruim gera interfaces confusas independente de quao
bonito seja o design visual aplicado.

O toolkit de IA inclui metodos de pesquisa (card sorting, tree testing), artefatos de design
(sitemaps, taxonomias, modelos de navegacao) e principios de organizacao (esquemas exatos
vs. ambiguos, estruturas hierarquicas vs. facetadas). Cada ferramenta resolve um aspecto
diferente do desafio de organizacao de informacao.

Os quatro componentes fundamentais de IA, segundo Rosenfeld e Morville, sao: Organization
Systems (como conteudo e categorizado), Labeling Systems (como categorias sao nomeadas),
Navigation Systems (como usuarios se movem pela estrutura) e Search Systems (como usuarios
buscam conteudo diretamente). Dominar IA significa projetar esses quatro componentes de
forma integrada e coerente.

## When to Use

- Ao projetar a estrutura de um novo produto, site ou aplicacao
- Quando usuarios reportam dificuldade em encontrar informacoes ou completar tarefas
- Em redesigns onde a estrutura existente nao escala com o crescimento de conteudo
- Para validar se a organizacao mental dos usuarios corresponde a estrutura do produto
- Quando novos conteudos ou features precisam ser integrados a estrutura existente

## How to Apply

1. **Conduza inventario de conteudo:** Liste todo o conteudo existente (ou planejado) que
   precisa ser organizado. Classifique por tipo, volume, frequencia de acesso e importancia
   para o usuario. Identifique redundancias, gaps e conteudo obsoleto.

2. **Realize Card Sorting:** Peca a 15-20 usuarios que agrupem cartoes de conteudo em
   categorias que facam sentido para eles. Use open card sort (usuarios criam categorias
   livremente) para descobrir modelos mentais, ou closed card sort (categorias pre-definidas)
   para validar uma estrutura proposta. Analise padroes de agrupamento com dendrogramas.

3. **Projete a estrutura:** Com base nos resultados do card sort, crie a hierarquia de
   conteudo. Defina categorias de primeiro nivel (amplas e distintas), subcategorias
   (especificas e mutuamente exclusivas) e relacoes cruzadas. Use sitemaps para visualizar
   a estrutura completa.

4. **Defina labels (rotulos):** Escolha nomes para cada categoria e item de navegacao.
   Labels devem ser familiares ao usuario, nao jargao interno da empresa. Teste
   alternativas se houver duvida — a diferenca entre "Minha conta" e "Configuracoes"
   pode ser significativa para a findability.

5. **Valide com Tree Testing:** Apresente a estrutura hierarquica (sem interface visual) a
   usuarios e peca que encontrem itens especificos. Meça taxa de sucesso, caminhos tomados
   e tempo. Tree testing isola problemas de IA de problemas de UI visual.

6. **Projete sistemas de navegacao:** Defina navegacao global (presente em todas as paginas),
   local (contextual a secao atual), utilitaria (conta, ajuda, idioma) e contextual (links
   relacionados e sugestoes). Garanta que usuarios sempre saibam onde estao e como voltar.

7. **Projete sistema de busca:** Para conteudos extensos, busca e essencial como complemento
   a navegacao. Defina como resultados sao apresentados, quais filtros estao disponiveis,
   e como zero-results sao tratados com sugestoes uteis.

## Key Principles

- **Modelo mental do usuario prevalece:** A estrutura deve refletir como usuarios pensam
  sobre o conteudo, nao como a empresa esta organizada internamente. Card sorting e a
  ferramenta principal para acessar modelos mentais reais.

- **Progressive disclosure:** Nao exponha toda a complexidade de uma vez so. Mostre opcoes
  de alto nivel primeiro e revele detalhes conforme o usuario aprofunda. Isso reduz carga
  cognitiva sem esconder informacao necessaria.

- **Labels sao interface:** Rotulos ambiguos sao a causa numero um de erros de navegacao.
  Um label deve comunicar inequivocamente o que o usuario encontrara ao clicar nele.
  Teste labels com usuarios reais, nao apenas com a equipe interna.

- **Escala desde o inicio:** Projete a estrutura para acomodar crescimento futuro. Se o
  produto tem 10 categorias hoje e tera 50 em um ano, a arquitetura deve suportar
  expansao sem reestruturacao completa.

- **Multiplos caminhos para o mesmo conteudo:** Usuarios diferentes procuram o mesmo
  conteudo de formas diferentes. Cross-links, tags, busca e navegacao facetada garantem
  que nao ha um unico caminho rigido para cada destino.

## Examples

### Redesign de Portal Corporativo
Card sorting com 80 funcionarios revelou que a estrutura departamental (RH, Financeiro,
TI) nao correspondia ao modelo mental dos usuarios, que pensavam por tarefa ("solicitar
ferias", "abrir chamado", "enviar nota fiscal"). A IA foi reestruturada por tarefas no
primeiro nivel, com acesso departamental como caminho secundario. Tree testing validou
aumento de findability de 45% para 82%.

### E-commerce de Moda
Tree testing revelou que usuarios nao encontravam "vestidos" sob "Roupas > Feminino >
Vestidos" porque esperavam acesso direto no primeiro nivel de navegacao. Solucao:
navegacao facetada combinando tipo de peca, genero, ocasiao e tamanho, permitindo
multiplos caminhos para o mesmo produto. Taxa de sucesso na navegacao subiu de
58% para 89%.

### App de Documentacao Tecnica
Inventario revelou 3.000+ artigos com nomenclatura inconsistente e estrutura fragmentada
em 12 categorias arbitrarias. Card sort com desenvolvedores identificou 7 categorias
naturais. Labels foram padronizados (ex: "Getting Started" em vez de 5 variacoes como
"Quickstart", "Tutorial", "Intro", "Primeiros Passos", "Guia Rapido"). Busca full-text
com filtros por linguagem e versao completou a solucao.

## Common Pitfalls

- **Espelhar organograma:** Estruturar o produto conforme departamentos da empresa ignora
  completamente o modelo mental do usuario. "Departamento de Sucesso do Cliente" nao e
  uma categoria que faz sentido para quem usa o produto.

- **Labels internos como rotulos publicos:** Usar jargao corporativo ou tecnico como rotulos
  de navegacao confunde usuarios. "Engagement Hub" pode fazer sentido internamente, mas
  "Comunicacoes" e mais claro para o usuario final.

- **Card sort sem tree test:** Card sorting revela como usuarios agrupam conteudo, mas nao
  valida se a estrutura resultante e realmente navegavel. Tree testing e o complemento
  necessario para validacao completa.

- **Navegacao profunda demais:** Hierarquias com mais de 3-4 niveis de profundidade geram
  frustracao e desorientacao. Prefira categorias mais amplas no topo com filtros e busca
  para refinamento contextual.

## Cross-References

- [Atomic Design](atomic-design.md) — IA informa a estrutura de templates e organizacao
  de organismos na composicao de paginas
- [Gestalt Principles](gestalt-principles.md) — Principios de agrupamento visual reforçam
  a estrutura logica de IA na interface
- [Nielsen Heuristics](nielsen-heuristics.md) — Heuristicas como "recognition over recall"
  e "user control" se aplicam diretamente a navegacao
- [Hick's Law](hick-law.md) — Numero de opcoes de navegacao simultaneas impacta diretamente
  o tempo de decisao do usuario
- [Service Blueprinting](service-blueprinting.md) — IA informa a estrutura de informacao
  nos touchpoints frontstage do servico
