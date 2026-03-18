# Handoff Contract: Design Squad <-> Copy Squad

## Metadata

| Campo             | Valor                                      |
|-------------------|--------------------------------------------|
| parties           | Design Squad, Copy Squad                   |
| direction         | Bidirecional                               |
| created           | 2026-03-18                                 |
| version           | 1.0                                        |
| owners            | Design Lead, Copy Lead                     |
| review-cycle      | Trimestral                                 |
| status            | Ativo                                      |
## Trigger

### Design -> Copy
- Novo fluxo de usuario aprovado internamente pelo Design Squad.
- Wireframe com placeholder de texto pronto para revisao de copy.
- Mudanca significativa no contexto de tela que impacta a comunicacao.

### Copy -> Design
- Atualizacao do tom-de-voz-guidelines que afeta componentes existentes.
- Novo glossario-de-produto publicado com termos que alteram labels de interface.
- Microcopy aprovado pelo stakeholder pronto para integracao no layout.
## Pre-conditions

### Para Design enviar
- Wireframe passou por design critique interno com feedback incorporado.
- Fluxo do usuario documentado com ramificacoes e edge cases.
- Placeholders marcados com tag `[COPY-NEEDED]` no Figma.

### Para Copy enviar
- Microcopy passou por revisao editorial interna do Copy Squad.
- Glossario validado com PM para consistencia de termos.
## Handoff Package

### Design envia para Copy
| Deliverable                   | Formato          | Obrigatorio |
|-------------------------------|------------------|-------------|
| contexto-de-tela              | Figma link + PDF | Sim         |
| fluxo-do-usuario              | FigJam / Miro    | Sim         |
| wireframe-com-placeholder     | Figma link       | Sim         |
| restricoes-de-caracteres      | Spreadsheet      | Sim         |
### Copy envia para Design
| Deliverable                   | Formato          | Obrigatorio |
|-------------------------------|------------------|-------------|
| tom-de-voz-guidelines         | Notion page      | Sim         |
| glossario-de-produto          | Spreadsheet      | Sim         |
| microcopy-aprovado            | Figma comments   | Sim         |
### Shared artifacts
- `brand-voice-tokens`: mantidos no design system, editaveis por ambos os squads.
- `content-patterns`: biblioteca de padroes de texto reutilizaveis em componentes UI.

## Quality Gate on Send

### Checklist antes de Design enviar
- [ ] Todos os placeholders estao identificados com `[COPY-NEEDED]`.
- [ ] Restricoes de caracteres por campo estao documentadas.
- [ ] Contexto emocional do usuario esta descrito para cada tela.
- [ ] Fluxo contempla estados de erro, vazio e carregamento.
- [ ] Link do Figma tem permissao de visualizacao para Copy Squad.

### Checklist antes de Copy enviar
- [ ] Microcopy respeita restricoes de caracteres informadas.
- [ ] Termos estao consistentes com glossario-de-produto vigente.
- [ ] Variantes de copy para A/B test estao identificadas se aplicavel.
- [ ] Tom de voz esta coerente com a persona e momento do fluxo.

## Quality Gate on Receive

### Design valida ao receber de Copy
- [ ] Microcopy cabe nos componentes sem quebra de layout.
- [ ] Terminologia esta consistente em todo o fluxo.
- [ ] Copy contempla todos os estados (sucesso, erro, vazio, loading).
- [ ] Nenhum placeholder `[COPY-NEEDED]` ficou sem resposta.

### Copy valida ao receber de Design
- [ ] Contexto de tela esta claro e completo.
- [ ] Restricoes de caracteres sao realistas para comunicacao eficaz.
- [ ] Persona e momento emocional estao documentados.

## Communication Protocol

| Etapa                | Canal                  | Responsavel     |
|----------------------|------------------------|-----------------|
| Solicitacao inicial  | Asana task com template| Squad solicitante|
| Duvidas e alinhamento| Thread no Slack #design-x-copy | Ambos   |
| Review sincrona      | Reuniao 30min max      | Ambos leads     |
| Entrega final        | Comment no Figma + Asana update | Squad entregando |
| Confirmacao          | Emoji check no Slack thread | Squad receptor |

## SLA

| Tipo de solicitacao          | Tempo de resposta | Tempo de entrega |
|------------------------------|-------------------|------------------|
| Microcopy para feature nova  | 4h uteis          | 3 dias uteis     |
| Revisao de copy existente    | 2h uteis          | 1 dia util       |
| Contexto de tela novo        | 4h uteis          | 2 dias uteis     |
| Atualizacao de glossario     | 8h uteis          | 5 dias uteis     |

## Escalation

1. **SLA expirado**: lembrete no Slack com @mention do lead responsavel.
2. **+24h**: escalar para Head of Design e Head of Copy via DM conjunta.
3. **+48h**: reuniao de desbloqueio com leads e PM.
4. **Impacto em release**: ativar copy placeholder temporario aprovado pelo PM.

## Rework Loop

1. Squad receptor abre comment no Figma descrevendo o problema especifico.
2. Classificar rework como `minor` (ajuste de texto) ou `major` (reescrita de fluxo).
3. **Minor**: resolver via thread assincrona, prazo de 1 dia util.
4. **Major**: sessao de 30min para alinhar, novo prazo de 3 dias uteis.
5. Maximo de 2 ciclos de rework. Apos isso, escalar para leads.

## Cross-References

- `./cross-squad-handoff-protocol.md` — protocolo generico de handoff.
- `../processes/design-critique-loop.md` — critique pre-handoff.
- `../../copy/guidelines/tom-de-voz.md` — tom de voz do Copy Squad.
