# Handoff Contract: Design Squad <-> Movement Squad

## Metadata

| Campo             | Valor                                      |
|-------------------|--------------------------------------------|
| parties           | Design Squad, Movement Squad               |
| direction         | Bidirecional                               |
| created           | 2026-03-18                                 |
| version           | 1.0                                        |
| owners            | Design Lead, Movement Lead                 |
| review-cycle      | Trimestral                                 |
| status            | Ativo                                      |
## Trigger

### Design -> Movement
- Proposta de nova identidade visual ou refresh de marca que precisa de validacao cultural.
- Criacao de UX patterns para comunidade que requerem alinhamento com valores do movimento.
- Implementacao de brand-expression em produto novo que impacta a percepcao da comunidade.

### Movement -> Design
- Atualizacao de contexto cultural que impacta decisoes de identidade visual e tom de comunicacao.
- Novos community-insights coletados em pesquisa de campo que alteram perfis de audiencia.
- Redefinicao da movement-identity que exige reposicionamento de elementos visuais no produto.
## Pre-conditions

### Para Design enviar
- Visual-identity-alignment revisado internamente pelo Design Squad com referencia ao brand system.
- Brand-expression documentada com exemplos reais de aplicacao em telas de produto.
- Community-ux-patterns testados com pelo menos um round de usability testing interno.

### Para Movement enviar
- Cultural-context validado com liderancas comunitarias e documentado com fontes primarias.
- Community-insights baseados em pesquisa qualitativa com amostra representativa da audiencia.
- Audience-profiles atualizados com dados demograficos e comportamentais do ultimo trimestre.

## Handoff Package

### Design envia para Movement
| Deliverable                        | Formato              | Obrigatorio |
|------------------------------------|----------------------|-------------|
| visual-identity-alignment          | Figma link + PDF     | Sim         |
| brand-expression-in-product        | Figma link + Notion  | Sim         |
| community-ux-patterns              | Figma library + Notion | Sim       |
| usability-test-results             | Notion page          | Nao         |
### Movement envia para Design
| Deliverable                        | Formato              | Obrigatorio |
|------------------------------------|----------------------|-------------|
| cultural-context                   | Notion page + PDF    | Sim         |
| community-insights                 | Notion page + Slides | Sim         |
| movement-identity                  | PDF + Notion page    | Sim         |
| audience-profiles                  | Spreadsheet + Notion | Sim         |

### Shared artifacts
- `cultural-design-tokens`: arquivo JSON no design system contendo tokens visuais (cores, tipografia, iconografia) que refletem valores culturais e identidade do movimento.
- `community-pattern-library`: biblioteca compartilhada no Figma com patterns de UX validados culturalmente para uso em interfaces voltadas a comunidade.
## Quality Gate on Send

### Checklist antes de Design enviar
- [ ] Visual-identity-alignment referencia explicitamente os valores culturais documentados pelo Movement Squad.
- [ ] Brand-expression inclui exemplos de aplicacao em pelo menos tres telas-chave do produto.
- [ ] Community-ux-patterns seguem accessibility guidelines (WCAG AA) e sao inclusivos para a audiencia alvo.
- [ ] Arquivos Figma organizados com naming convention alinhada ao design system.
- [ ] Proposta visual nao utiliza simbolos ou referencias culturais sem validacao previa do Movement.

### Checklist antes de Movement enviar
- [ ] Cultural-context documenta fontes primarias e metodologia de coleta.
- [ ] Community-insights incluem citacoes diretas e temas emergentes categorizados.
- [ ] Audience-profiles contem segmentacao clara com necessidades e comportamentos distintos.
- [ ] Movement-identity inclui manifesto atualizado e principios visuais orientadores.
## Quality Gate on Receive

### Design valida ao receber de Movement
- [ ] Cultural-context e suficientemente detalhado para informar decisoes de design sem ambiguidades.
- [ ] Audience-profiles contem informacoes acionaveis para criacao de personas de design.
- [ ] Movement-identity inclui diretrizes visuais traduzíveis em design tokens.
- [ ] Community-insights nao contradizem dados de usability testing ja realizados.

### Movement valida ao receber de Design
- [ ] Visual-identity-alignment respeita valores culturais e nao apropria simbolos indevidamente.
- [ ] Community-ux-patterns sao acessiveis e inclusivos para todos os segmentos de audiencia.
- [ ] Brand-expression em produto transmite a essencia do movimento de forma autentica.

## Communication Protocol

| Etapa                   | Canal                          | Responsavel        |
|-------------------------|--------------------------------|--------------------|
| Compartilhamento de insights | Notion page + Slack #design-x-movement | Movement Lead |
| Apresentacao de proposta visual | Reuniao 60min com screenshare | Design Lead     |
| Validacao cultural      | Workshop colaborativo 90min    | Movement Lead      |
| Feedback estruturado    | Figma comments + Notion        | Squad receptor     |
| Aprovacao final         | Asana task status + Slack      | Lead do squad receptor |

## SLA

| Tipo de solicitacao                  | Tempo de resposta | Tempo de entrega   |
|--------------------------------------|-------------------|--------------------|
| Validacao cultural de proposta visual| 3 dias uteis      | 1 semana           |
| Atualizacao de cultural-context      | 1 semana          | 2 semanas          |
| Novos community-ux-patterns          | 3 dias uteis      | 2 semanas          |
| Revisao de audience-profiles         | 1 semana          | 2 semanas          |

## Escalation

1. **SLA expirado**: lembrete no Slack #design-x-movement com mention do lead responsavel e contexto.
2. **+1 semana sem resposta**: DM para Movement Lead e Design Lead com impacto documentado.
3. **+2 semanas sem resolucao**: escalar para Head of Design e Head of Community.
4. **Bloqueio de lancamento**: utilizar ultimo cultural-context aprovado e documentar risco de desalinhamento.
## Rework Loop

1. Squad receptor documenta problema com anotacoes contextuais no Figma ou Notion.
2. Classificar como `cultural-adjustment` (ajuste de referencia cultural), `pattern-revision` (mudanca de UX pattern) ou `identity-realignment` (nova direcao de identidade).
3. **Cultural-adjustment**: resolver via comentarios e ajustes pontuais, prazo de 3 dias uteis.
4. **Pattern-revision**: sessao colaborativa de 45min entre designers e lideranca de movimento, prazo de 1 semana.
5. **Identity-realignment**: requer workshop completo e nova validacao cultural, prazo de 2 semanas.
## Cross-References

- `./cross-squad-handoff-protocol.md` — protocolo generico de handoff.
- `../design-system/tokens/cultural-design-tokens.json` — tokens visuais culturais.
- `../../movement/identity/movement-identity.md` — documento de identidade do movimento.
- `../../movement/research/community-insights.md` — insights de comunidade mais recentes.
