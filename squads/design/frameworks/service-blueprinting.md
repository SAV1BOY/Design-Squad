# Service Blueprinting

## Metadata

- **Origem:** G. Lynn Shostack (1984), evoluido por Service Design community
- **Categoria:** Service Design Tool
- **Complexidade:** Intermediaria a Avancada
- **Aplicacao:** Design de servicos, operacoes, experiencia end-to-end
- **Tags:** frontstage, backstage, support-processes, touchpoints, line-of-visibility

## Concept

Service Blueprinting e uma ferramenta de visualizacao que mapeia um servico mostrando nao
apenas a experiencia visivel ao usuario (frontstage), mas tambem os processos internos
(backstage) e as dependencias de infraestrutura que tornam o servico possivel. O blueprint
revela a complexidade oculta por tras de experiencias aparentemente simples e diretas.

O blueprint e organizado em camadas horizontais separadas por linhas conceituais. A line
of interaction separa acoes do usuario de acoes frontstage da empresa. A line of visibility
separa o que o usuario ve do que nao ve. A line of internal interaction separa backstage
de processos de suporte. Essa estrutura em camadas e o diferencial do blueprint em relacao
ao journey map — ele conecta experiencia do usuario a operacao do negocio.

Service blueprints sao especialmente valiosos quando a experiencia do usuario depende de
multiplos sistemas, equipes e processos coordenados. Uma entrega de comida envolve app,
restaurante, entregador, gateway de pagamento e suporte. O blueprint torna essas
dependencias explicitas e revela pontos de falha ocultos que journey maps nao capturam.

## When to Use

- Quando a experiencia do usuario depende de operacoes complexas com multiplos atores
- Para diagnosticar falhas de servico cujas causas raiz estao no backstage, nao no frontstage
- Ao projetar novos servicos que exigem coordenacao entre equipes e sistemas
- Para alinhar equipes de UX, engenharia e operacoes em torno da experiencia completa
- Quando journey maps nao sao suficientes para revelar a causa de problemas de experiencia

## How to Apply

1. **Defina o cenario de servico:** Escolha um cenario especifico com inicio e fim claros.
   "Usuario solicita reembolso de pedido com defeito" e melhor que "experiencia do
   marketplace". Cenarios especificos geram blueprints acionaveis e focados.

2. **Mapeie acoes do usuario (Customer Actions):** Na camada superior, documente
   cronologicamente tudo que o usuario faz — desde o trigger inicial ate a conclusao
   do cenario. Use dados de pesquisa e analytics, nao suposicoes.

3. **Mapeie frontstage (Onstage Contact Employee Actions):** Abaixo da line of interaction,
   documente o que a equipe frontstage faz em resposta as acoes do usuario. Isso inclui
   interfaces digitais, atendentes humanos, e qualquer interacao visivel ao usuario.

4. **Mapeie backstage (Backstage Contact Employee Actions):** Abaixo da line of visibility,
   documente processos que o usuario nao ve mas que sao necessarios para o servico
   funcionar. Processamento de pagamento, roteirizacao de entrega, triagem de suporte,
   verificacao de fraude.

5. **Mapeie processos de suporte (Support Processes):** Na camada inferior, documente
   sistemas, infraestrutura e servicos de terceiros que sustentam o backstage. APIs,
   databases, servicos de email, parceiros logisticos, gateways de pagamento.

6. **Adicione evidencias fisicas:** No topo do blueprint, documente artefatos tangiveis
   que o usuario encontra em cada etapa — telas do app, emails, notificacoes push,
   embalagens, recibos impressos.

7. **Identifique fail points e wait points:** Marque pontos onde o servico pode falhar
   (fail points) e onde o usuario espera sem acao (wait points). Esses sao os pontos
   criticos para melhoria. Para cada um, proponha mitigacoes concretas.

8. **Adicione metricas e KPIs:** Anote metricas relevantes em cada ponto do blueprint —
   tempo de resposta, taxa de sucesso, volume de chamados. Isso conecta o blueprint a
   dados mensuraveis e facilita priorizacao.

## Key Principles

- **Camadas revelam dependencias:** A estrutura em camadas do blueprint torna explicitas
  as dependencias entre experiencia frontstage e operacao backstage. Problemas de UX
  frequentemente tem causas raiz no backstage, invisiveis para o usuario.

- **Line of visibility e estrategica:** Decidir o que o usuario ve e o que nao ve e uma
  decisao de design. Mostrar progresso de processamento (frontstage) reduz ansiedade
  mesmo sem mudar o processo (backstage) subjacente.

- **Fail points sao oportunidades:** Cada ponto de falha potencial e uma oportunidade de
  design. Planejar para falhas (error handling, fallbacks, comunicacao proativa)
  diferencia servicos mediocres de servicos excelentes.

- **Tempo e visivel no blueprint:** Wait points devem ser explicitamente representados
  com duracao estimada. O tempo que o usuario espera entre acoes e parte da experiencia
  e frequentemente a maior fonte de frustracao.

- **Colaboracao cross-functional:** Blueprints so podem ser criados com input de multiplas
  areas — UX, engenharia, operacoes, suporte. Nenhuma equipe sozinha tem visao completa
  de todas as camadas do servico.

## Examples

### Processo de Devolucao em E-commerce
Customer Actions: abrir pedido > selecionar item > solicitar devolucao > imprimir etiqueta
> postar pacote > acompanhar reembolso. Frontstage: interface de devolucao, email de
confirmacao, tracking page, notificacao de reembolso. Backstage: validacao de elegibilidade,
geracao de etiqueta, autorizacao logistica reversa, processamento de reembolso. Support:
API de logistica, gateway de pagamento, sistema de estoque. Fail point critico: demora
entre recebimento do pacote e processamento do reembolso (media 7 dias) gerava 60% dos
chamados de suporte ao cliente.

### Telemedicina
Customer Actions: agendar > receber lembrete > entrar na sala virtual > consultar >
receber prescricao > comprar medicamento. Frontstage: app de agendamento, sala de video,
chat com medico, receita digital. Backstage: matching medico-paciente, verificacao de
agenda, prontuario eletronico, prescricao digital assinada. Support: infra de video,
sistema de prontuario, API de farmacia parceira. O blueprint revelou que o fail point
principal era a transicao entre agendamento e sala virtual — 15% dos pacientes nao
conseguiam entrar na chamada por problemas tecnicos.

### Delivery de Comida
O blueprint revelou 23 processos backstage para cada pedido — desde notificacao ao
restaurante ate alocacao de entregador e calculo de rota. O wait point mais critico era
entre "pedido aceito" e "saiu para entrega". Sem comunicacao nesse intervalo, usuarios
ligavam para o suporte. Adicionar status intermediarios ("restaurante preparando",
"pronto para coleta") reduziu chamados ao suporte em 35%.

## Common Pitfalls

- **Blueprint sem dados reais:** Assim como journey maps, blueprints baseados em suposicoes
  sao ficcao operacional. Envolva operacoes, suporte e engenharia para mapear o backstage
  real, nao o idealizado em documentacoes antigas.

- **Excesso de detalhe:** Um blueprint com 100 etapas em todas as camadas e ilegivel.
  Mantenha nivel de detalhe consistente e aprofunde apenas nos pontos criticos
  identificados como fail points e wait points.

- **Ignorar o backstage:** Tratar o blueprint como um journey map sofisticado, sem mapear
  processos backstage e dependencias de suporte, perde o valor principal da ferramenta
  e seu diferencial analitico.

- **Artefato estatico nunca atualizado:** Servicos evoluem constantemente. Blueprints devem
  ser atualizados quando processos mudam significativamente. Um blueprint desatualizado e
  pior que nenhum — gera decisoes baseadas em informacao incorreta.

## Cross-References

- [User Journey Mapping](user-journey-mapping.md) — Journey maps focam na experiencia
  do usuario; blueprints expandem para incluir operacoes e dependencias
- [Information Architecture Toolkit](information-architecture-toolkit.md) — IA informa a
  estrutura de informacao nos touchpoints frontstage do servico
- [Design Thinking](design-thinking.md) — Blueprints sao ferramentas da fase Define,
  conectando empatia do usuario a operacao do negocio
- [HEART Metrics Framework](heart-metrics-framework.md) — Metricas HEART podem ser
  mapeadas a pontos especificos do blueprint
- [Double Diamond](double-diamond.md) — Blueprints apoiam a fase de Discover ao revelar
  complexidade oculta do servico atual
