# HEART Metrics Framework

## Metadata

- **Origem:** Google (Kerry Rodden, Hilary Hutchinson, Xin Fu, 2010)
- **Categoria:** UX Measurement Framework
- **Complexidade:** Intermediaria
- **Aplicacao:** Definicao de metricas de UX, avaliacao de qualidade de experiencia
- **Tags:** happiness, engagement, adoption, retention, task-success, goals-signals-metrics

## Concept

O HEART framework e um sistema de metricas de UX criado pelo Google para medir a qualidade
da experiencia do usuario em cinco dimensoes: Happiness (satisfacao subjetiva), Engagement
(nivel de envolvimento), Adoption (adesao de novos usuarios), Retention (retorno de usuarios
existentes) e Task Success (eficiencia e eficacia na completacao de tarefas).

O diferencial do HEART em relacao a outros frameworks de metricas e sua abordagem
Goals-Signals-Metrics (GSM). Para cada dimensao, a equipe primeiro define Goals (o que
queremos alcançar), depois identifica Signals (comportamentos ou atitudes que indicam
progresso) e finalmente especifica Metrics (como medir esses sinais quantitativamente).
Isso evita a armadilha de medir o que e facil em vez de medir o que realmente importa
para a experiencia.

Nem todas as cinco dimensoes sao relevantes para todo projeto. A equipe deve selecionar
as dimensoes mais criticas para o contexto especifico. Um redesign de checkout pode focar
em Task Success e Happiness. Um novo produto social pode priorizar Adoption e Engagement.
A seletividade e uma feature do framework, nao um bug.

## When to Use

- Ao definir metricas de UX para um produto, feature ou redesign especifico
- Quando a equipe precisa ir alem de metricas de negocio e medir qualidade de experiencia
- Para avaliar o impacto de mudancas de design de forma estruturada e mensuravel
- Em design reviews e retrospectivas para fundamentar discussoes em dados concretos
- Para comunicar resultados de UX a stakeholders em linguagem mensuravel e compreensivel

## How to Apply

1. **Selecione dimensoes relevantes:** Nao use todas as cinco dimensoes para todo projeto.
   Escolha 2-3 que sao mais criticas para o contexto. Um projeto de onboarding pode focar
   em Adoption e Task Success. Um projeto de engajamento pode focar em Engagement e
   Retention.

2. **Defina Goals para cada dimensao:** Para cada dimensao selecionada, articule o objetivo
   de UX em linguagem clara e especifica. Exemplo para Happiness: "Usuarios devem se sentir
   confiantes e no controle durante o processo de checkout."

3. **Identifique Signals:** Para cada goal, identifique comportamentos observaveis ou
   atitudes que indicariam sucesso ou fracasso. Para o goal acima: signal positivo =
   completar checkout sem voltar a etapas anteriores; signal negativo = abandonar carrinho
   na etapa de pagamento.

4. **Especifique Metrics:** Transforme sinais em metricas quantificaveis com definicao
   precisa e inequivoca. "Taxa de conclusao de checkout sem retrocesso" (Task Success),
   "CSAT pos-checkout >= 4.2/5" (Happiness), "Tempo medio de conclusao < 90 segundos"
   (Task Success).

5. **Implemente instrumentacao:** Trabalhe com engenharia para instrumentar analytics que
   capturam as metricas definidas. Garanta que a coleta e confiavel e consistente antes
   de usar os dados para tomar decisoes.

6. **Estabeleca baselines e metas:** Meça o estado atual antes de implementar mudancas.
   Defina metas realistas baseadas em benchmarks do setor e dados historicos do produto.
   Monitore tendencias ao longo do tempo, nao apenas snapshots isolados.

## Key Principles

- **Goals-Signals-Metrics em sequencia:** Nunca comece pela metrica. Comece pelo objetivo
  de UX, identifique sinais observaveis, e so entao defina como medir. Inverter a ordem
  leva a medir o que e facil, nao o que importa.

- **Seletividade sobre completude:** Usar todas as cinco dimensoes para cada projeto dilui
  o foco da equipe. Escolha as dimensoes mais relevantes e meça-as bem, em vez de medir
  tudo superficialmente sem profundidade.

- **Atitudinal e comportamental:** O HEART combina metricas atitudinais (Happiness, via
  surveys) com comportamentais (Engagement, Retention, via analytics). Essa combinacao
  da uma visao mais completa do que qualquer tipo isolado.

- **Nivel adequado de granularidade:** HEART pode ser aplicado no nivel de produto inteiro,
  de feature especifica, ou de task individual. Escolha o nivel que corresponde ao escopo
  da decisao de design que precisa ser informada.

## Examples

### Redesign de Dashboard Analytics
Dimensoes selecionadas: Task Success, Happiness, Engagement. Goals: usuarios devem
encontrar insights relevantes rapidamente (Task Success); sentir-se competentes usando
a ferramenta (Happiness); retornar ao dashboard diariamente (Engagement). Metrics: tempo
para primeiro insight < 30s, SUS score > 75, DAU/MAU ratio > 40%. Apos redesign, tempo
para primeiro insight caiu de 2min para 25s, e DAU/MAU subiu de 28% para 45%.

### Novo Fluxo de Cadastro
Dimensoes: Adoption, Task Success. Goals: maximizar conversao de visitante para usuario
registrado (Adoption); minimizar friccao no processo de cadastro (Task Success). Signals:
taxa de conclusao do cadastro, campos com erro, abandono por etapa especifica. Metrics:
taxa de conclusao > 70%, erro por campo < 5%, tempo total < 2 minutos. O framework
revelou que o campo "telefone obrigatorio" era responsavel por 30% dos abandonos.

### Feature de Busca em App Mobile
Dimensoes: Task Success, Happiness. Goals: usuarios devem encontrar o que procuram na
primeira busca (Task Success); sentir que a busca e inteligente e util (Happiness).
Metrics: taxa de clique no primeiro resultado > 60%, zero-result rate < 5%, CSAT da
busca >= 4.0. A analise mostrou zero-result rate de 18%, levando a investimento em
sinonimos e busca fuzzy que resolveu o problema.

## Common Pitfalls

- **Medir tudo sem foco:** Instrumentar todas as cinco dimensoes para cada feature gera
  data overload sem insight acionavel. Selecione conscientemente e meça bem as dimensoes
  que realmente importam para o contexto.

- **Happiness sem contexto:** Surveys de satisfacao sao facilmente enviesados por timing,
  formulacao e fadiga de resposta. Triangule dados atitudinais com dados comportamentais
  para ter confianca nos resultados obtidos.

- **Confundir Engagement com vicio:** Alto engagement pode indicar que o produto e valioso
  ou que e manipulativamente viciante. Sempre cruze Engagement com Happiness para
  distinguir os dois cenarios e garantir etica.

- **Metricas sem acao:** Coletar dados sem agir sobre eles e desperdicar esforco de
  instrumentacao. Para cada metrica, defina previamente: "Se o resultado for X, faremos
  Y. Se for Z, faremos W."

## Cross-References

- [North Star and Success Metrics](north-star-and-success-metrics.md) — HEART fornece
  metricas de UX que complementam a North Star Metric do produto
- [Hypothesis-Driven Design](hypothesis-driven-design.md) — Metricas HEART servem como
  criterios de sucesso para experimentos de validacao
- [Nielsen Heuristics](nielsen-heuristics.md) — Heuristicas informam o que medir em
  Task Success e Happiness do usuario
- [User Journey Mapping](user-journey-mapping.md) — Mapas de jornada revelam onde
  instrumentar metricas de cada dimensao HEART
- [Jobs to Be Done](jobs-to-be-done.md) — Jobs definem o que constitui Task Success do
  ponto de vista do usuario e suas necessidades
