# Handoff Contract: Design Squad <-> Data Squad

## Metadata

| Campo             | Valor                                      |
|-------------------|--------------------------------------------|
| parties           | Design Squad, Data Squad                   |
| direction         | Bidirecional                               |
| created           | 2026-03-18                                 |
| version           | 1.0                                        |
| owners            | Design Lead, Data Lead                     |
| review-cycle      | Trimestral                                 |
| status            | Ativo                                      |
## Trigger

### Design -> Data
- Novo fluxo de usuario requer definicao de eventos de tracking para mensurar eficacia.
- Hipotese de experimento formulada pelo Design Squad precisa de validacao quantitativa.
- Redesign de feature existente demanda baseline de metricas atuais para comparacao.

### Data -> Design
- Analise de funil revela ponto de friccao com drop-off significativo que exige revisao de UX.
- Resultado de teste A/B concluido com recomendacao de variante vencedora para implementacao.
- Novo relatorio de comportamento do usuario identifica padroes que impactam decisoes de design.
## Pre-conditions

### Para Design enviar
- Fluxo do usuario esta documentado com todas as etapas e pontos de decisao mapeados.
- Hipoteses de experimento estao formuladas com metrica primaria e criterio de sucesso definidos.
- Especificacoes de tracking passaram por revisao interna do Design Squad.

### Para Data enviar
- Relatorio de analytics passou por validacao interna de qualidade dos dados.
- Resultados de teste A/B atingiram significancia estatistica minima acordada.
- Dados estao anonimizados e em conformidade com politica de privacidade vigente.
## Handoff Package

### Design envia para Data
| Deliverable                   | Formato          | Obrigatorio |
|-------------------------------|------------------|-------------|
| tracking-requirements         | Spreadsheet      | Sim         |
| event-specs                   | JSON schema      | Sim         |
| metrics-definitions           | Notion page      | Sim         |
| experiment-hypotheses         | Notion template  | Sim         |
### Data envia para Design
| Deliverable                   | Formato          | Obrigatorio |
|-------------------------------|------------------|-------------|
| analytics-reports             | Looker dashboard | Sim         |
| funnel-data                   | Spreadsheet + viz| Sim         |
| user-behavior-metrics         | Notion page      | Sim         |
| ab-test-results               | Notion report    | Sim         |
### Shared artifacts
- `event-taxonomy`: taxonomia unificada de eventos mantida no repositorio compartilhado, editavel por ambos os squads.
- `metrics-dashboard-templates`: templates padrao de dashboards reutilizaveis para acompanhamento de metricas de produto.

## Quality Gate on Send

### Checklist antes de Design enviar
- [ ] Cada evento de tracking possui nome, descricao, propriedades e tipo definidos.
- [ ] Metricas primarias e secundarias estao claramente diferenciadas por experimento.
- [ ] Hipoteses seguem formato estruturado: "Se [acao], entao [resultado], medido por [metrica]".
- [ ] Fluxo contempla eventos para estados de erro, sucesso e abandono.
- [ ] Event-specs estao alinhados com a event-taxonomy vigente.

### Checklist antes de Data enviar
- [ ] Dados possuem intervalo de confianca e tamanho amostral documentados.
- [ ] Visualizacoes incluem periodo de coleta e filtros aplicados.
- [ ] Insights estao traduzidos em linguagem acionavel para decisoes de design.
- [ ] Resultados de A/B test incluem recomendacao explicita com justificativa.

## Quality Gate on Receive

### Design valida ao receber de Data
- [ ] Metricas reportadas correspondem as metricas solicitadas no briefing original.
- [ ] Periodo de analise e segmentacao de usuarios estao documentados.
- [ ] Insights possuem evidencia quantitativa e nao apenas observacoes qualitativas.
- [ ] Recomendacoes sao acionaveis e compativeis com restricoes tecnicas conhecidas.

### Data valida ao receber de Design
- [ ] Especificacoes de eventos sao implementaveis com a infraestrutura atual de tracking.
- [ ] Metricas de sucesso definidas sao mensuraveis com os dados disponiveis.
- [ ] Hipoteses possuem criterio de sucesso numerico e prazo definidos.

## Communication Protocol

| Etapa                | Canal                  | Responsavel     |
|----------------------|------------------------|-----------------|
| Solicitacao inicial  | Asana task com template| Squad solicitante|
| Duvidas e alinhamento| Thread no Slack #design-x-data | Ambos   |
| Review sincrona      | Reuniao 30min max      | Ambos leads     |
| Entrega final        | Link do dashboard + Asana update | Squad entregando |
| Confirmacao          | Emoji check no Slack thread | Squad receptor |

## SLA

| Tipo de solicitacao          | Tempo de resposta | Tempo de entrega |
|------------------------------|-------------------|------------------|
| Definicao de tracking specs  | 4h uteis          | 2 dias uteis     |
| Relatorio de analytics ad-hoc| 4h uteis          | 3 dias uteis     |
| Resultado de teste A/B       | 8h uteis          | Apos significancia|
| Baseline de metricas         | 4h uteis          | 2 dias uteis     |

## Escalation

1. **SLA expirado**: lembrete no Slack com @mention do lead responsavel.
2. **+24h**: escalar para Head of Design e Head of Data via DM conjunta.
3. **+48h**: reuniao de desbloqueio com leads e PM.
4. **Impacto em release**: utilizar metricas proxy ja disponiveis como baseline temporario.

## Rework Loop

1. Squad receptor abre comment na Notion page descrevendo a inconsistencia ou lacuna encontrada.
2. Classificar rework como `minor` (ajuste de parametro ou filtro) ou `major` (recoleta ou nova analise).
3. **Minor**: resolver via thread assincrona, prazo de 1 dia util.
4. **Major**: sessao de 30min para alinhar escopo, novo prazo de 3 dias uteis.
5. Maximo de 2 ciclos de rework. Apos isso, escalar para leads.

## Cross-References

- `./cross-squad-handoff-protocol.md` — protocolo generico de handoff.
- `../processes/design-critique-loop.md` — critique pre-handoff.
- `../../data/guidelines/event-taxonomy.md` — taxonomia de eventos do Data Squad.
