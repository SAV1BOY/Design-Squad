# Handoff Contract: Design Squad <-> Deep Research Squad

## Metadata

| Campo             | Valor                                      |
|-------------------|--------------------------------------------|
| parties           | Design Squad, Deep Research Squad          |
| direction         | Bidirecional                               |
| created           | 2026-03-18                                 |
| version           | 1.0                                        |
| owners            | Design Lead, Deep Research Lead            |
| review-cycle      | Trimestral                                 |
| status            | Ativo                                      |
## Trigger

### Design -> Deep Research
- Nova feature requer entendimento profundo de comportamento do usuario antes da concepcao.
- Hipotese de design precisa de validacao com pesquisa de mercado ou analise competitiva.
- Redesign de fluxo critico demanda investigacao de pain points e necessidades nao atendidas.

### Deep Research -> Design
- Pesquisa de mercado concluida revela oportunidade de experiencia nao explorada pelo produto.
- Analise competitiva identifica padrao de interacao adotado por concorrentes relevantes.
- Relatorio de comportamento do usuario apresenta insight acionavel que impacta decisoes de design.
## Pre-conditions

### Para Design enviar
- Perguntas de pesquisa estao formuladas com objetivo claro e escopo delimitado.
- Hipoteses estao documentadas com criterios de validacao ou refutacao definidos.
- Contexto do projeto e restricoes de prazo estao comunicados ao Deep Research Squad.

### Para Deep Research enviar
- Pesquisa passou por revisao metodologica interna do Deep Research Squad.
- Fontes estao documentadas e classificadas por nivel de confiabilidade.
- Insights estao sintetizados em formato acionavel e nao apenas como dados brutos.
## Handoff Package

### Design envia para Deep Research
| Deliverable                   | Formato          | Obrigatorio |
|-------------------------------|------------------|-------------|
| research-questions            | Notion template  | Sim         |
| hypothesis-list               | Notion page      | Sim         |
| specific-inquiry-briefs       | Notion brief     | Sim         |
### Deep Research envia para Design
| Deliverable                   | Formato          | Obrigatorio |
|-------------------------------|------------------|-------------|
| research-briefs               | Notion report    | Sim         |
| market-analysis               | Notion + Slides  | Sim         |
| user-behavior-reports         | Notion page      | Sim         |
| competitive-intelligence      | Spreadsheet + PDF| Sim         |
### Shared artifacts
- `research-repository`: repositorio centralizado de pesquisas realizadas, indexado por tema e data, acessivel por ambos os squads.
- `insight-registry`: registro de insights validados com status de aplicacao, utilizado para rastreabilidade de decisoes de design.

## Quality Gate on Send

### Checklist antes de Design enviar
- [ ] Perguntas de pesquisa estao priorizadas por impacto na decisao de design.
- [ ] Hipoteses incluem contexto do problema e evidencias preliminares disponiveis.
- [ ] Briefing especifica o nivel de profundidade esperado (exploratoria, validacao, benchmarking).
- [ ] Prazo de necessidade esta comunicado com justificativa de urgencia se aplicavel.
- [ ] Duplicidade foi verificada no research-repository antes de solicitar nova pesquisa.

### Checklist antes de Deep Research enviar
- [ ] Metodologia utilizada esta documentada e e replicavel.
- [ ] Fontes primarias e secundarias estao listadas com links e datas de acesso.
- [ ] Insights possuem nivel de confianca indicado (alto, medio, baixo).
- [ ] Recomendacoes estao conectadas as perguntas de pesquisa originais.

## Quality Gate on Receive

### Design valida ao receber de Deep Research
- [ ] Insights respondem diretamente as perguntas de pesquisa formuladas.
- [ ] Nivel de profundidade e compativel com o briefing original.
- [ ] Recomendacoes sao acionaveis dentro das restricoes do projeto.
- [ ] Analise competitiva inclui players relevantes para o segmento do produto.

### Deep Research valida ao receber de Design
- [ ] Perguntas de pesquisa sao especificas o suficiente para direcionar a investigacao.
- [ ] Escopo e prazo sao realistas para o nivel de profundidade solicitado.
- [ ] Contexto do projeto permite priorizacao adequada dos temas de pesquisa.

## Communication Protocol

| Etapa                | Canal                  | Responsavel     |
|----------------------|------------------------|-----------------|
| Solicitacao inicial  | Asana task com template| Squad solicitante|
| Duvidas e alinhamento| Thread no Slack #design-x-research | Ambos |
| Review sincrona      | Reuniao 30min max      | Ambos leads     |
| Entrega final        | Link Notion + Asana update | Squad entregando |
| Confirmacao          | Emoji check no Slack thread | Squad receptor |

## SLA

| Tipo de solicitacao          | Tempo de resposta | Tempo de entrega |
|------------------------------|-------------------|------------------|
| Pesquisa exploratoria        | 4h uteis          | 5 dias uteis     |
| Analise competitiva focada   | 4h uteis          | 3 dias uteis     |
| Validacao de hipotese        | 2h uteis          | 3 dias uteis     |
| Consulta rapida ao repositorio| 2h uteis         | 1 dia util       |

## Escalation

1. **SLA expirado**: lembrete no Slack com @mention do lead responsavel.
2. **+24h**: escalar para Head of Design e Head of Deep Research via DM conjunta.
3. **+48h**: reuniao de desbloqueio com leads e PM.
4. **Impacto em release**: prosseguir com hipotese mais provavel documentando risco de decisao sem pesquisa completa.

## Rework Loop

1. Squad receptor abre comment na Notion page descrevendo lacuna ou inconsistencia encontrada.
2. Classificar rework como `minor` (complemento de dado ou fonte) ou `major` (nova linha de investigacao).
3. **Minor**: resolver via thread assincrona, prazo de 1 dia util.
4. **Major**: sessao de 30min para realinhar escopo, novo prazo de 3 dias uteis.
5. Maximo de 2 ciclos de rework. Apos isso, escalar para leads.

## Cross-References

- `./cross-squad-handoff-protocol.md` — protocolo generico de handoff.
- `../processes/design-critique-loop.md` — critique pre-handoff.
- `../../deep-research/guidelines/research-methodology.md` — metodologia padrao do Deep Research Squad.
