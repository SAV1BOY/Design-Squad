# Jobs to Be Done (JTBD)

## Metadata

- **Origem:** Clayton Christensen / Tony Ulwick (1990s-2000s)
- **Categoria:** User Research & Strategy Framework
- **Complexidade:** Intermediaria a Avancada
- **Aplicacao:** Descoberta de produto, inovacao, posicionamento e priorizacao
- **Tags:** jobs, forces, outcomes, hiring, firing, demand-side, innovation

## Concept

Jobs to Be Done e um framework que propoe que pessoas nao compram produtos — elas
"contratam" produtos para realizar um trabalho (job) especifico em suas vidas. O foco
muda de atributos do produto e demografias do usuario para a motivacao subjacente que
leva alguem a buscar uma solucao. Um job e estavel ao longo do tempo mesmo quando as
solucoes disponiveis mudam radicalmente.

O framework distingue entre tres tipos de jobs: funcional (a tarefa pratica), emocional
(como a pessoa quer se sentir) e social (como quer ser percebida pelos outros). As quatro
forcas que influenciam a "contratacao" de uma nova solucao sao: push (insatisfacao com a
situacao atual), pull (atracao pela nova solucao), anxiety (medo de mudar) e inertia
(habito da solucao atual). Para que a troca aconteca, push + pull devem superar
anxiety + inertia.

Tony Ulwick contribuiu com a abordagem Outcome-Driven Innovation (ODI), que estrutura
jobs em outcome statements mensuraveis no formato: "[direcao] + [metrica] + [objeto] +
[contexto]". Exemplo: "Minimizar o tempo gasto organizando documentos ao colaborar com
equipe remota". Essa estruturacao permite quantificar oportunidades de inovacao com
precisao e priorizar investimento de forma objetiva.

## When to Use

- Quando a equipe precisa entender por que usuarios realmente usam (ou abandonam) um produto
- Para identificar oportunidades de inovacao alem de melhorias incrementais
- Ao definir posicionamento e messaging de produto baseado em motivacoes reais
- Em decisoes de priorizacao de roadmap baseadas em necessidades reais dos usuarios
- Para entender competidores nao-obvios (solucoes que cumprem o mesmo job)

## How to Apply

1. **Identifique o job principal:** Conduza entrevistas de Switch Interview, perguntando
   aos usuarios sobre o momento em que decidiram buscar uma solucao. Mapeie a timeline:
   primeiro pensamento, evento trigger, busca ativa, decisao, uso e avaliacao pos-uso.

2. **Mapeie as quatro forcas:** Para cada usuario, identifique o push (o que os empurrou
   para longe da solucao anterior), pull (o que os atraiu na nova solucao), anxiety
   (medos sobre a nova solucao) e inertia (habitos e investimentos na solucao atual).

3. **Articule o job statement:** Escreva o job no formato: "Quando [situacao], eu quero
   [motivacao], para que eu possa [resultado esperado]". Exemplo: "Quando estou numa
   cidade desconhecida, quero encontrar um restaurante confiavel, para que eu possa
   ter uma boa experiencia sem risco."

4. **Defina outcome statements:** Para cada etapa do job, escreva outcomes mensuraveis
   usando o formato ODI. Agrupe e priorize outcomes com base em importancia (para o
   usuario) e satisfacao atual (com solucoes existentes no mercado).

5. **Identifique oportunidades:** Outcomes com alta importancia e baixa satisfacao sao
   oportunidades de inovacao (underserved). Outcomes com baixa importancia e alta
   satisfacao indicam over-serving — possivel simplificacao ou reducao de custo.

6. **Valide com dados:** Conduza surveys quantitativos para validar a priorizacao de
   jobs e outcomes em escala. Use os resultados para informar roadmap e decisoes de
   produto com confianca estatistica.

## Key Principles

- **Jobs sao estaveis, solucoes mudam:** O job "entreter-se durante o deslocamento"
  existe ha seculos. As solucoes mudaram de livros para radio para podcasts para TikTok.
  Projetar para o job, nao para a solucao atual, garante relevancia de longo prazo.

- **Competicao e cross-category:** Uma planilha Excel pode competir com um software de
  project management se ambos sao "contratados" para o mesmo job. Entender o job real
  revela competidores nao-obvios que analises tradicionais de mercado nao capturam.

- **Contexto e determinante:** O mesmo usuario pode "contratar" solucoes diferentes
  dependendo da situacao. Um cafe pela manha cumpre um job diferente de um cafe numa
  reuniao de negocios. Situacao importa mais que demografia.

- **Forcas emocionais superam racionais:** Anxiety e inertia frequentemente bloqueiam a
  adocao de solucoes objetivamente superiores. Reduzir barreiras emocionais pode ser
  mais eficaz que adicionar features tecnicas.

## Examples

### Plataforma de Freelancers
Entrevistas revelaram que empresas nao "contratavam" a plataforma para "encontrar
freelancers" (job superficial), mas para "reduzir o risco de contratar alguem desconhecido
para um projeto critico" (job real). Isso redirecionou o produto para investir em reviews
verificados, portfolios detalhados e garantias de qualidade em vez de apenas aumentar a
base de freelancers disponivel.

### App de Meditacao
O job principal nao era "meditar" (funcional), mas "sentir que estou cuidando de mim"
(emocional) e "parecer equilibrado para meus colegas" (social). O push era estresse
crescente; o pull era a promessa de calma. A anxiety era "nao vou conseguir manter o
habito". A equipe redesenhou o onboarding para reduzir anxiety com sessoes de 1 minuto
e streaks gentis sem punicao por falhas.

### Ferramenta de Documentacao Tecnica
ODI revelou que o outcome "minimizar o tempo para encontrar informacao relevante ao
debugar um problema em producao" era o mais underserved. A equipe priorizou busca
contextual e integracao com logs em vez de melhorar o editor de documentos — que
estava over-served segundo os dados coletados.

## Common Pitfalls

- **Confundir jobs com tasks:** "Criar uma conta" e uma task, nao um job. O job e a
  motivacao maior: "acessar [beneficio] de forma personalizada". Pergunte "por que?"
  repetidamente ate chegar ao job real subjacente.

- **Jobs muito abstratos:** "Viver uma vida melhor" e verdade para qualquer produto e
  nao e acionavel para decisoes de design. O job deve ser especifico o suficiente para
  guiar decisoes de design concretas e mensuráveis.

- **Ignorar as forcas de resistencia:** Focar apenas em push e pull sem enderecar anxiety
  e inertia gera produtos que parecem atrativos mas nao convertem. Projete ativamente
  para reduzir barreiras emocionais.

- **Tratar JTBD como substituto de pesquisa continua:** JTBD revela motivacoes profundas,
  mas nao substitui testes de usabilidade, analytics e feedback continuo. Use como
  complemento estrategico, nao como unica fonte de verdade.

## Cross-References

- [Design Thinking](design-thinking.md) — JTBD complementa a fase de Empatia com
  estrutura analitica para motivacoes e forcas
- [Problem Statement Template](problem-statement-template.md) — Job statements alimentam
  diretamente a formulacao de problem statements mais precisos
- [North Star and Success Metrics](north-star-and-success-metrics.md) — Jobs e outcomes
  informam a definicao de metricas de sucesso do produto
- [Hypothesis-Driven Design](hypothesis-driven-design.md) — Outcomes underserved geram
  hipoteses testaveis para validacao rapida
- [HEART Metrics Framework](heart-metrics-framework.md) — Metricas para validar se o
  produto esta cumprindo o job prometido ao usuario
