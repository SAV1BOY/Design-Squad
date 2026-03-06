# North Star and Success Metrics

## Metadata

- **Origem:** Sean Ellis / Amplitude / Growth frameworks modernos
- **Categoria:** Strategy & Measurement Framework
- **Complexidade:** Intermediaria
- **Aplicacao:** Alinhamento estrategico de produto, definicao de KPIs, priorizacao
- **Tags:** north-star-metric, KPI, OKR, leading-indicators, lagging-indicators, product-strategy

## Concept

A North Star Metric (NSM) e a unica metrica que melhor captura o valor central que o
produto entrega aos usuarios. Ela serve como bussola estrategica — alinhando equipes,
informando priorizacao e conectando atividade do usuario a resultado de negocio. Diferente
de metricas de vaidade ou metricas puramente financeiras, a NSM deve refletir valor
entregue ao usuario, nao receita direta.

Metricas de sucesso complementam a NSM com indicadores mais granulares organizados em
camadas. Leading indicators medem comportamentos que preveem o resultado futuro (ex:
ativacao na primeira semana). Lagging indicators medem o resultado final (ex: retencao
em 90 dias). Input metrics medem esforcos da equipe (ex: features lancadas). Juntas,
essas camadas criam um sistema de metricas que permite diagnosticar problemas e
priorizar acoes com precisao.

O perigo de metricas mal escolhidas e real e significativo. Metricas incentivam
comportamento — da equipe e do produto. Otimizar para "tempo na plataforma" pode levar
a dark patterns que viciam usuarios. Otimizar para "tarefas completadas com sucesso"
incentiva eficiencia genuina. A escolha da NSM e uma decisao etica tanto quanto
estrategica para o produto.

## When to Use

- No inicio de um produto ou feature para definir como sucesso sera medido
- Quando a equipe esta desalinhada sobre prioridades e precisa de criterio objetivo
- Para alinhar design, engenharia e negocio em torno de um objetivo comum mensuravel
- Em revisoes trimestrais de estrategia de produto para avaliar progresso
- Quando metricas existentes nao estao gerando os comportamentos desejados na equipe

## How to Apply

1. **Identifique o valor central do produto:** Pergunte: "Qual e o momento em que o usuario
   recebe valor real do nosso produto?" Para o Spotify, e ouvir musica. Para o Slack, e
   trocar mensagens com a equipe. Para o Airbnb, e completar uma estadia. A NSM deve
   medir a frequencia ou volume desse momento de valor.

2. **Formule a North Star Metric:** A NSM deve ser: mensuravel, correlacionada com retencao
   de longo prazo, influenciavel pela equipe, e refletir valor para o usuario (nao apenas
   para o negocio). Exemplos: "Noites reservadas por semana" (Airbnb), "Mensagens enviadas
   por dia" (Slack), "Entregas completadas" (iFood).

3. **Defina input metrics (leading indicators):** Identifique 3-5 metricas que alimentam a
   NSM e que equipes especificas podem influenciar diretamente. Para "noites reservadas":
   busca de propriedades, salvamento de favoritos, mensagens para hosts, reviews publicados.

4. **Estabeleca guardrails:** Defina metricas de protecao que garantem que a otimizacao da
   NSM nao gere efeitos colaterais negativos. Se a NSM e "mensagens enviadas", um guardrail
   pode ser "satisfacao do usuario" para evitar que a metrica seja inflada por spam.

5. **Crie dashboards acessiveis:** Metricas so geram alinhamento se forem visiveis para
   todos. Crie dashboards que toda a equipe consulta regularmente. Inclua tendencias,
   metas e segmentacoes relevantes por cohort.

6. **Revise periodicamente:** A NSM pode precisar evoluir conforme o produto amadurece.
   Revise trimestralmente se a metrica ainda reflete o valor central. Mude se necessario,
   mas com parcimonia — mudancas frequentes geram confusao.

## Key Principles

- **Uma unica North Star:** Ter multiplas NSMs dilui o foco e cria conflitos de priorizacao.
  A equipe inteira deve ser capaz de responder "qual e nossa North Star?" sem hesitar.
  Sub-metricas existem, mas servem a uma unica estrela guia.

- **Valor para o usuario primeiro:** A NSM deve medir valor entregue ao usuario, nao receita
  diretamente. Se os usuarios recebem valor consistente, resultados financeiros seguem
  naturalmente. Receita e um lagging indicator do valor entregue.

- **Leading sobre lagging:** Priorize metricas que a equipe pode influenciar agora (leading)
  sobre metricas que reportam o passado (lagging). Leading indicators permitem correcao
  de curso proativa antes que o problema se torne critico.

- **Metricas mudam comportamento:** Toda metrica incentiva certo comportamento na equipe.
  Escolha conscientemente metricas que incentivam os comportamentos que voce quer ver —
  tanto na equipe quanto nos usuarios do produto.

- **Simplicidade sobre completude:** Um sistema de metricas com 50 KPIs nao gera
  alinhamento. Prefira 1 NSM + 3-5 input metrics + 2-3 guardrails. Menos e mais quando
  se trata de foco organizacional.

## Examples

### Plataforma de Educacao Online
NSM: "Aulas completadas por semana". Input metrics: taxa de ativacao (primeira aula em
48h), taxa de engajamento (minutos de video assistidos), taxa de quiz completion.
Guardrails: NPS do estudante, taxa de reembolso. A equipe descobriu que otimizar para
"aulas completadas" ao inves de "cadastros" redirecionou esforcos para qualidade de
conteudo e UX de aprendizado, gerando retencao superior.

### App de Financas Pessoais
NSM: "Transacoes categorizadas por mes". Isso reflete o momento de valor — quando o
usuario entende para onde seu dinheiro vai. Input metrics: conexao de contas bancarias,
frequencia de abertura do app, configuracao de orcamentos. Guardrails: erros de
categorizacao automatica, tempo para completar setup. A metrica anterior era "usuarios
ativos diarios", que incentivava notificacoes excessivas sem gerar valor real.

### Marketplace de Servicos Locais
NSM: "Servicos completados com avaliacao positiva por semana". Isso captura a transacao
bem-sucedida com satisfacao de ambos os lados. Input metrics: buscas realizadas,
orcamentos solicitados, taxa de match (contratacao apos orcamento). Guardrails:
reclamacoes por servico, tempo de resposta de prestadores.

## Common Pitfalls

- **Metrica de vaidade como NSM:** "Usuarios registrados" ou "downloads" nao medem valor
  entregue. Sao metricas que so crescem e nao indicam saude real do produto. Prefira
  metricas de atividade e valor entregue.

- **Otimizacao sem guardrails:** Sem metricas de protecao, a equipe pode otimizar a NSM
  de formas que prejudicam a experiencia. Mais "tempo no app" pode significar UX confusa,
  nao engajamento genuino do usuario.

- **NSM desconectada do trabalho diario:** Se a equipe nao consegue conectar seu trabalho
  cotidiano a NSM, a metrica nao gera alinhamento. Input metrics devem ser acionaveis
  por equipes especificas em seus sprints.

- **Mudar a NSM frequentemente:** Cada mudanca de NSM requer recalibracao de toda a
  estrategia e dashboards. Mude apenas quando ha evidencia clara de que a metrica
  atual nao reflete mais o valor central do produto.

## Cross-References

- [HEART Metrics Framework](heart-metrics-framework.md) — Framework complementar para
  metricas de UX que podem servir como input metrics da NSM
- [Hypothesis-Driven Design](hypothesis-driven-design.md) — Metricas de sucesso definem
  criterios para validacao de hipoteses em experimentos
- [Jobs to Be Done](jobs-to-be-done.md) — O job principal do usuario informa qual momento
  de valor a NSM deve capturar e medir
- [Problem Statement Template](problem-statement-template.md) — Problem statements devem
  ser conectados a metricas mensuraveis de sucesso
- [User Journey Mapping](user-journey-mapping.md) — Mapas de jornada ajudam a identificar
  onde medir leading indicators ao longo da experiencia
