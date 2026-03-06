# Hick's Law

## Metadata

- **Origem:** William Edmund Hick e Ray Hyman (1952)
- **Categoria:** Cognitive Performance Principle
- **Complexidade:** Basica
- **Aplicacao:** Simplificacao de interfaces, menus, navegacao, tomada de decisao
- **Tags:** choice, decision-time, progressive-disclosure, paradox-of-choice, simplicity, cognitive-load

## Concept

Hick's Law (ou Hick-Hyman Law) estabelece que o tempo necessario para tomar uma decisao
aumenta logaritmicamente com o numero de opcoes disponiveis. Matematicamente:
T = b * log2(n + 1), onde T e o tempo de decisao e n e o numero de alternativas
apresentadas. Em termos praticos, cada opcao adicional aumenta o tempo de decisao,
embora o impacto marginal diminua conforme o numero total cresce.

Para designers de interface, a implicacao e clara: quanto mais opcoes apresentadas
simultaneamente ao usuario, mais tempo ele leva para decidir e maior a probabilidade de
paralisia, erro ou abandono do fluxo. Isso nao significa que interfaces devem ter poucas
funcionalidades — significa que devem apresentar opcoes de forma progressiva e estruturada,
nao simultanea e desorganizada.

A lei se conecta ao Paradox of Choice (Barry Schwartz): alem de um certo ponto, mais
opcoes nao aumentam satisfacao — diminuem. Usuarios expostos a muitas opcoes experimentam
ansiedade de decisao, arrependimento antecipado sobre opcoes nao escolhidas, e menor
satisfacao com a escolha final. Progressive disclosure e a principal estrategia de design
para mitigar esse efeito negativo.

## When to Use

- Ao projetar menus, navegacoes e sistemas de opcoes em qualquer interface
- Para simplificar fluxos com muitas etapas ou decisoes sequenciais
- Quando analytics mostram abandono em telas com muitas opcoes simultaneas
- Ao projetar onboarding e primeira experiencia do usuario no produto
- Para decidir quanta informacao e quantas acoes apresentar por tela

## How to Apply

1. **Reduza opcoes simultaneas:** Avalie cada tela: quantas decisoes o usuario precisa tomar
   de uma vez? Elimine opcoes redundantes, agrupe opcoes relacionadas e remova o que nao e
   essencial para o contexto atual. O objetivo e o minimo necessario para a tarefa, nao o
   minimo possivel em absoluto.

2. **Aplique progressive disclosure sistematicamente:** Mostre apenas as opcoes mais
   relevantes inicialmente. Revele opcoes adicionais conforme o usuario avanca ou solicita
   explicitamente. Menus com "Ver mais", filtros expansiveis e wizard steps sao
   implementacoes praticas de progressive disclosure.

3. **Use categorias como atalhos cognitivos:** Em vez de uma lista plana de 50 itens,
   agrupe em 5-7 categorias de 7-10 itens cada. O usuario decide primeiro a categoria
   (5 opcoes) e depois o item (7-10 opcoes) — duas decisoes faceis e rapidas em vez de
   uma decisao impossivel e paralisante.

4. **Destaque defaults e recomendacoes:** Quando ha uma opcao recomendada ou mais popular,
   destaque-a visualmente com badge ou posicao privilegiada. Defaults reduzem a decisao a
   "aceitar ou mudar" (efetivamente 2 opcoes) em vez de "escolher entre N opcoes". A
   maioria dos usuarios aceita o default oferecido.

5. **Implemente busca e filtros para conjuntos grandes:** Quando o numero de opcoes e
   genuinamente grande (catalogo de produtos, lista de contatos), nao tente reduzir
   artificialmente. Ofereca busca, filtros e ordenacao que permitem ao usuario reduzir
   o conjunto por conta propria de forma eficiente.

6. **Simplifique onboarding radicalmente:** Na primeira experiencia com o produto, cada
   decisao e uma barreira potencial para abandono. Reduza ao absoluto minimo. Pergunte
   apenas o essencial para comecar. Use defaults inteligentes baseados em contexto.
   Permita customizacao completa posteriormente via configuracoes.

7. **Teste com metricas de decisao:** Meça tempo de decisao por tela, taxa de abandono
   por tela, e taxa de uso do default vs. customizacao. Essas metricas revelam
   objetivamente onde a carga de decisao e excessiva para o usuario.

## Key Principles

- **Logaritmico, nao linear:** Ir de 2 para 4 opcoes tem impacto proporcionalmente maior
  no tempo de decisao que ir de 20 para 22. O custo marginal de cada opcao adicional
  diminui, mas nunca chega a zero. Isso significa que reduzir opcoes em telas simples
  gera mais impacto que em telas ja complexas.

- **Progressive disclosure e a estrategia central:** Nao se trata de remover
  funcionalidades do produto — se trata de revelar no momento certo de uso. Um editor
  de texto pode ter 200 funcoes, mas o usuario tipico precisa de 10 por vez. Esconda
  complexidade, nao elimine-a.

- **Defaults sao decisoes de design de alto impacto:** Escolher o default e uma das
  decisoes de design mais impactantes que uma equipe pode tomar. O default sera a
  experiencia da maioria dos usuarios. Invista tempo significativo em escolher defaults
  inteligentes e eticos.

- **Contexto reduz opcoes efetivas automaticamente:** Opcoes que o sistema pode inferir
  do contexto nao precisam ser perguntadas ao usuario. Se o usuario esta editando um
  documento, "Salvar" e mais relevante que "Criar novo". Contexto permite esconder
  opcoes irrelevantes sem perda de funcionalidade.

- **Paradox of Choice e real e mensuravel:** Mais opcoes geram mais ansiedade, nao mais
  satisfacao. Usuarios que escolhem entre 3 planos ficam mais satisfeitos que usuarios
  que escolhem entre 12, mesmo que os 12 incluam uma opcao objetivamente melhor para
  eles.

## Examples

### Simplificacao de Menu de Navegacao
Problema: mega-menu com 87 itens organizados em 12 categorias causava paralisia visivel.
Analytics mostravam que usuarios levavam em media 12 segundos para clicar em qualquer
item — e 30% saiam da pagina sem clicar em nada. Solucao: reducao para 6 categorias
primarias no menu, com subcategorias acessiveis via hover. Busca proeminente como
alternativa direta. Tempo medio de decisao caiu para 4 segundos e a taxa de uso da
busca subiu 200%.

### Tela de Pricing
Problema: 6 planos de pricing com matriz comparativa de features de 30 linhas. Usuarios
nao conseguiam diferenciar planos e ligavam para vendas pedindo ajuda para escolher.
Solucao: reducao para 3 planos (Basico, Pro, Enterprise) com highlight visual claro no
plano recomendado ("Mais popular"). Toggle simples entre mensal/anual. Tabela de
comparacao detalhada disponivel via progressive disclosure ("Comparar todos os planos").
Conversao self-serve subiu 40%.

### Onboarding de App de Produtividade
Problema: onboarding pedia 8 decisoes antes do primeiro uso — integracoes, cor do tema,
layout preferido, notificacoes, timezone, idioma, formato de data, avatar. Taxa de
conclusao do onboarding: 23%. Solucao: reduziu para 2 decisoes essenciais (nome e uma
integracao principal). Restante inferido por defaults inteligentes (timezone do device,
idioma do OS, tema claro como default). Customizacao total disponivel em "Configuracoes"
a qualquer momento. Taxa de conclusao do onboarding subiu para 89%.

## Common Pitfalls

- **Confundir menos opcoes com menos funcionalidade:** Hick's Law nao pede que voce remova
  features do produto. Pede que voce as organize e revele progressivamente no momento
  certo. Um produto pode ser poderoso e parecer simples simultaneamente.

- **Aplicar a lei igualmente a novatos e experts:** Hick's Law tem maior impacto em
  novatos que ainda nao formaram modelos mentais. Usuarios experts ja conhecem a estrutura
  e navegam rapidamente. Projete simplicidade para novatos com atalhos para experts
  (conforme Nielsen heuristica 7).

- **Defaults manipulativos que prejudicam o usuario:** Usar defaults para forçar escolhas
  que beneficiam a empresa mas prejudicam o usuario e um dark pattern antiético. Defaults
  devem ser a melhor opcao para o usuario, nao para o revenue da empresa.

- **Reducao arbitraria sem dados:** Cortar opcoes sem pesquisa de uso pode remover
  exatamente a opcao que usuarios mais precisam e valorizam. Analise dados de uso real
  antes de eliminar. Esconda via progressive disclosure antes de remover permanentemente
  — e mais seguro.

## Cross-References

- [Fitts's Law](fitts-law.md) — Hick mede tempo de decisao cognitiva, Fitts mede tempo
  de execucao motora. Juntas, preveem tempo total de interacao
- [Nielsen Heuristics](nielsen-heuristics.md) — Heuristicas 6 (recognition over recall) e
  8 (aesthetic/minimalist design) se conectam diretamente a Hick
- [Information Architecture Toolkit](information-architecture-toolkit.md) — IA estrutura
  opcoes em categorias que reduzem carga de decisao por nivel
- [Interaction Design Principles](interaction-design-principles.md) — Progressive disclosure
  e constraints sao implementacoes praticas de Hick's Law
- [Gestalt Principles](gestalt-principles.md) — Agrupamento visual (similaridade,
  proximidade) ajuda o usuario a processar opcoes mais rapidamente
