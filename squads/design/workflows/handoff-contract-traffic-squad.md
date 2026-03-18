# Handoff Contract: Design Squad <-> Traffic Squad

## Metadata

| Campo             | Valor                                      |
|-------------------|--------------------------------------------|
| parties           | Design Squad, Traffic Squad                |
| direction         | Bidirecional                               |
| created           | 2026-03-18                                 |
| version           | 1.0                                        |
| owners            | Design Lead, Traffic Lead                  |
| review-cycle      | Trimestral                                 |
| status            | Ativo                                      |
## Trigger

### Design -> Traffic
- Nova hipotese de design formulada que precisa de validacao quantitativa.
- Variantes de UI prontas para configuracao de A/B test.
- Necessidade de definir tracking events para novos fluxos ou componentes.

### Traffic -> Design
- Dados de comportamento indicam problema de usabilidade em fluxo existente.
- Funis de conversao mostram drop-off significativo em etapa especifica.
- Heatmaps revelam padrao de interacao inesperado que requer investigacao.
- Metricas de engajamento apos lancamento precisam de analise conjunta.
## Pre-conditions

### Para Design enviar
- Hipotese documentada no formato "Se [mudanca], entao [resultado], porque [evidencia]".
- Variantes finalizadas e aprovadas no critique.
- Tracking requirements seguem a event-taxonomy compartilhada.

### Para Traffic enviar
- Dados com amostra estatisticamente significativa (confianca minima 95%).
- Funis segmentados por device, origem e periodo.
- Heatmaps cobrem minimo 1000 sessoes por variante.

## Handoff Package

### Design envia para Traffic
| Deliverable                   | Formato              | Obrigatorio |
|-------------------------------|----------------------|-------------|
| hipoteses-de-design           | Notion page          | Sim         |
| variantes-para-ab-test        | Figma link + specs   | Sim         |
| tracking-requirements         | Spreadsheet (template)| Sim        |
| criterio-de-sucesso           | Notion page          | Sim         |
### Traffic envia para Design
| Deliverable                   | Formato              | Obrigatorio |
|-------------------------------|----------------------|-------------|
| dados-de-comportamento        | Dashboard link + PDF | Sim         |
| funis-de-conversao            | Analytics export     | Sim         |
| heatmaps                      | Hotjar/Clarity export| Sim         |
| metricas-de-engajamento       | Dashboard link       | Sim         |
### Shared artifacts
- `event-taxonomy`: documento unico com nomenclatura padrao para todos os eventos de tracking.
- `funnel-definitions`: definicoes compartilhadas de etapas de funil por produto.
## Quality Gate on Send

### Checklist antes de Design enviar
- [ ] Hipotese segue formato padrao com evidencia qualitativa de suporte.
- [ ] Variantes tem diferencas claras e isoladas (uma variavel por teste).
- [ ] Tracking events seguem nomenclatura da event-taxonomy.
- [ ] Criterio de sucesso inclui metrica primaria e metricas guardrail.

### Checklist antes de Traffic enviar
- [ ] Dados validados contra contaminacao (bots, testes internos).
- [ ] Segmentacao por device e origem aplicada e documentada.
- [ ] Funis mostram volume absoluto alem de porcentagem.
- [ ] Heatmaps incluem scroll depth e click density.

## Quality Gate on Receive

### Design valida ao receber de Traffic
- [ ] Amostra atinge significancia estatistica minima de 95%.
- [ ] Dados cobrem todos os devices e breakpoints relevantes.
- [ ] Metricas guardrail sem degradacao significativa.
- [ ] Analise inclui recomendacao acionavel, nao apenas numeros brutos.

### Traffic valida ao receber de Design
- [ ] Variantes implementaveis no framework de A/B test.
- [ ] Tracking events nao duplicam eventos existentes na taxonomy.
- [ ] Hipotese e criterio mensuraveis com ferramentas atuais.

## Communication Protocol

| Etapa                   | Canal                        | Responsavel       |
|-------------------------|------------------------------|-------------------|
| Solicitacao de teste    | Asana task com template      | Design Lead       |
| Configuracao de tracking| Thread no Slack #design-x-traffic | Traffic Lead |
| Alinhamento de hipotese | Reuniao 30min                | Ambos leads       |
| Analise conjunta        | Reuniao 45min com screenshare| Ambos squads      |
| Decisao de rollout      | Asana task update            | Design Lead + PM  |
## SLA

| Tipo de solicitacao              | Tempo de resposta | Tempo de entrega    |
|----------------------------------|-------------------|---------------------|
| Configuracao de A/B test         | 4h uteis          | 3 dias uteis        |
| Analise de heatmap sob demanda   | 8h uteis          | 5 dias uteis        |
| Dados de funil para investigacao | 4h uteis          | 2 dias uteis        |
| Resultados de teste concluido    | 4h uteis          | 3 dias uteis        |
| Tracking de novo fluxo           | 8h uteis          | 5 dias uteis        |
## Escalation

1. **SLA expirado**: mention no Slack #design-x-traffic com link da task.
2. **+24h sem resposta**: DM para o lead responsavel com contexto de impacto.
3. **+48h sem resolucao**: reuniao de desbloqueio com ambos leads e PM.
4. **Teste bloqueado**: documentar decisao tomada sem dados e registrar divida.
## Rework Loop

1. Squad receptor descreve problema no Asana task com evidencia especifica.
2. Classificar como `data-quality` (dados insuficientes), `scope-change` (nova metrica necessaria) ou `analysis-depth` (analise superficial).
3. **Data-quality**: estender periodo de coleta, novo prazo acordado entre leads.
4. **Scope-change**: revisar tracking requirements e criterio, prazo de 3 dias uteis.
5. **Analysis-depth**: solicitar detalhamento, prazo de 2 dias uteis.
6. Maximo de 2 ciclos. Apos isso, escalar para leads e PM.
## Cross-References

- `./cross-squad-handoff-protocol.md` — protocolo generico de handoff.
- `../../traffic/taxonomy/event-taxonomy.md` — taxonomia de eventos.
- `../../traffic/dashboards/funnel-definitions.md` — definicoes de funil.
