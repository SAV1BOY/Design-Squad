# Handoff Contract: Design Squad <-> C-Level Squad

## Metadata

| Campo             | Valor                                      |
|-------------------|--------------------------------------------|
| parties           | Design Squad, C-Level Squad                |
| direction         | Bidirecional                               |
| created           | 2026-03-18                                 |
| version           | 1.0                                        |
| owners            | Design Lead, C-Level Lead                  |
| review-cycle      | Mensal                                     |
| status            | Ativo                                      |
## Trigger

### Design -> C-Level
- Fechamento de ciclo trimestral com metricas de impacto de design consolidadas.
- Proposta de investimento em ferramentas, contratacoes ou capacitacao para o time de design.
- Evolucao significativa no maturity-assessment que requer reposicionamento estrategico.

### C-Level -> Design
- Redefinicao de OKRs corporativos que impacta prioridades de design.
- Mudanca de visao de produto ou entrada em novo mercado que exige adaptacao de design strategy.
- Revisao orcamentaria que afeta recursos alocados ao Design Squad.
## Pre-conditions

### Para Design enviar
- Metricas de impacto validadas com Product e Engineering antes da apresentacao.
- Relatorio trimestral revisado internamente pelo Design Lead e aprovado pelo Head of Design.
- Proposta de investimento com business case documentado incluindo ROI estimado.

### Para C-Level enviar
- OKRs aprovados em reuniao de diretoria e documentados no formato oficial.
- Visao de produto articulada com roadmap de alto nivel e timelines.
- Restricoes orcamentarias formalizadas com valores e periodos definidos.

## Handoff Package

### Design envia para C-Level
| Deliverable                        | Formato              | Obrigatorio |
|------------------------------------|----------------------|-------------|
| design-impact-report               | Notion page + PDF    | Sim         |
| quarterly-metrics                  | Dashboard + Slides   | Sim         |
| maturity-assessment                | Spreadsheet + PDF    | Sim         |
| investment-proposals               | Notion page + Slides | Sim         |
### C-Level envia para Design
| Deliverable                        | Formato              | Obrigatorio |
|------------------------------------|----------------------|-------------|
| strategic-direction                | Slides + Notion page | Sim         |
| product-vision                     | Notion page + PDF    | Sim         |
| okrs                               | Spreadsheet + Notion | Sim         |
| budget-constraints                 | Spreadsheet + PDF    | Sim         |

### Shared artifacts
- `quarterly-reports`: documento consolidado em Notion com metricas de design, adocao de sistema, satisfacao de usuarios e alinhamento estrategico.
- `design-maturity-scorecard`: scorecard compartilhado que acompanha a evolucao da maturidade de design na organizacao trimestre a trimestre.
## Quality Gate on Send

### Checklist antes de Design enviar
- [ ] Metricas de impacto incluem baseline, target e resultado atual com fonte de dados rastreavel.
- [ ] Maturity-assessment utiliza framework acordado com C-Level no ciclo anterior.
- [ ] Propostas de investimento contem analise de custo-beneficio com cenarios otimista e conservador.
- [ ] Relatorio revisado por pelo menos dois membros senior do Design Squad.
- [ ] Apresentacao executiva com no maximo 15 slides, focada em decisoes e nao em detalhes operacionais.

### Checklist antes de C-Level enviar
- [ ] OKRs incluem key-results mensuraveis com indicadores claros para design.
- [ ] Visao de produto alinhada com demais squads e aprovada em board meeting.
- [ ] Restricoes orcamentarias detalhadas por categoria (ferramentas, pessoas, treinamento).
- [ ] Documento de strategic-direction inclui prioridades ordenadas e trade-offs explicitos.
## Quality Gate on Receive

### Design valida ao receber de C-Level
- [ ] OKRs sao traduzíveis em iniciativas de design com escopo definido.
- [ ] Visao de produto contem contexto suficiente para informar design strategy.
- [ ] Restricoes orcamentarias sao compativeis com o roadmap de design em andamento.
- [ ] Strategic-direction nao contradiz compromissos ja assumidos com outros squads.

### C-Level valida ao receber de Design
- [ ] Metricas de impacto conectam resultados de design a objetivos de negocio.
- [ ] Maturity-assessment demonstra progresso em relacao ao ciclo anterior.
- [ ] Propostas de investimento estao dentro dos parametros orcamentarios vigentes.

## Communication Protocol

| Etapa                | Canal                         | Responsavel           |
|----------------------|-------------------------------|-----------------------|
| Envio de OKRs        | Notion page + email formal   | C-Level Lead          |
| Apresentacao trimestral | Reuniao executiva 60min    | Design Lead           |
| Feedback estrategico | Reuniao 1:1 com Design Lead  | C-Level Lead          |
| Aprovacao de investimento | Email formal + Asana task | C-Level Lead       |
| Status update mensal | Slides async via Loom + Slack | Design Lead          |

## SLA

| Tipo de solicitacao              | Tempo de resposta | Tempo de entrega   |
|----------------------------------|-------------------|--------------------|
| Revisao de metricas trimestrais  | 1 semana          | 2 semanas          |
| Aprovacao de investimento        | 1 semana          | 3 semanas          |
| Atualizacao de OKRs              | 3 dias uteis      | 1 semana           |
| Revisao de strategic-direction   | 1 semana          | 2 semanas          |

## Escalation

1. **SLA expirado**: lembrete via email direto ao responsavel com contexto e deadline atualizado.
2. **+1 semana sem resposta**: reuniao extraordinaria agendada entre Design Lead e C-Level Lead.
3. **+2 semanas sem resolucao**: escalar para CEO ou COO com documento de impacto em decisoes pendentes.
4. **Bloqueio estrategico**: Design Squad opera com ultima direcao aprovada e documenta riscos.
## Rework Loop

1. Receptor documenta divergencia ou lacuna no entregavel com comentarios contextuais no Notion.
2. Classificar como `data-correction` (ajuste de numeros), `narrative-revision` (reframing estrategico) ou `scope-change` (nova direcao).
3. **Data-correction**: resolver via atualizacao direta no documento, prazo de 3 dias uteis.
4. **Narrative-revision**: sessao de alinhamento de 45min, novo prazo de 1 semana.
5. **Scope-change**: requer nova apresentacao executiva e aprovacao formal, prazo de 2 semanas.
## Cross-References

- `./cross-squad-handoff-protocol.md` — protocolo generico de handoff.
- `./quarterly-design-review.md` — workflow de revisao trimestral de design.
- `../../c-level/okrs/current-okrs.md` — OKRs vigentes da organizacao.
- `../design-system/metrics/design-impact-dashboard.md` — dashboard de metricas de impacto.
