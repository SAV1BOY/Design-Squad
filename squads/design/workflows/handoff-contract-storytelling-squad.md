# Handoff Contract: Design Squad <-> Storytelling Squad

## Metadata

| Campo             | Valor                                          |
|-------------------|-------------------------------------------------|
| parties           | Design Squad, Storytelling Squad               |
| direction         | Bidirecional                                    |
| created           | 2026-03-18                                      |
| version           | 1.0                                             |
| owners            | Design Lead, Storytelling Lead                  |
| review-cycle      | Trimestral                                      |
| status            | Ativo                                           |
## Trigger

### Design -> Storytelling
- Feature pronta para criacao de case study visual.
- Novo fluxo de onboarding que precisa de narrativa estruturada.
- Prototipo de narrativa interativa que precisa de revisao de storytelling.

### Storytelling -> Design
- Nova narrativa-de-produto definida que precisa de materializacao visual.
- Scripts de onboarding prontos para serem transformados em UI.
- Arcos de experiencia mapeados que precisam de traducao em jornada visual.
## Pre-conditions

### Para Design enviar
- Storyboard passou por critique interno com feedback aplicado.
- Prototipos em fidelidade alta com interacoes funcionais.
- Assets exportados em resolucao adequada (2x minimo).

### Para Storytelling enviar
- Narrativa validada com PM e stakeholders de negocio.
- Scripts de onboarding testados em leitura com usuarios reais ou proxy.
- Arcos mapeiam emocao esperada em cada momento do fluxo.

## Handoff Package

### Design envia para Storytelling
| Deliverable                   | Formato              | Obrigatorio |
|-------------------------------|----------------------|-------------|
| storyboard-visual             | Figma link + PDF     | Sim         |
| prototipos-de-narrativa       | Figma prototype link | Sim         |
| assets-para-case-study        | PNG/SVG exports      | Sim         |
| contexto-de-usuario           | Notion page          | Sim         |
### Storytelling envia para Design
| Deliverable                   | Formato              | Obrigatorio |
|-------------------------------|----------------------|-------------|
| narrativa-de-produto          | Notion page          | Sim         |
| scripts-de-onboarding         | Google Docs / Notion | Sim         |
| arcos-de-experiencia          | FigJam / Miro        | Sim         |
### Shared artifacts
- `illustration-library`: biblioteca compartilhada de ilustracoes aprovadas para produto e comunicacao.
- `animation-assets`: repositorio de assets de animacao (Lottie, SVG animado) reutilizaveis.
## Quality Gate on Send

### Checklist antes de Design enviar
- [ ] Storyboard tem sequencia logica com inicio, meio e fim.
- [ ] Prototipos incluem transicoes e microinteracoes relevantes.
- [ ] Assets nomeados segundo convencao do design system, resolucao 2x e 1x.
- [ ] Contexto inclui persona, cenario de uso e objetivo da narrativa.

### Checklist antes de Storytelling enviar
- [ ] Narrativa tem arco claro: problema, jornada, resolucao.
- [ ] Scripts especificam conteudo por tela/step com indicacao de timing.
- [ ] Arcos mapeiam emocao e intencao do usuario em cada momento.
- [ ] Conteudo revisado por Copy Squad para consistencia de tom de voz.

## Quality Gate on Receive

### Design valida ao receber de Storytelling
- [ ] Narrativa traduzivel em fluxo de telas com quantidade viavel de steps.
- [ ] Scripts respeitam boas praticas de progressive disclosure.
- [ ] Conteudo cabe nos componentes e layouts do design system.

### Storytelling valida ao receber de Design
- [ ] Storyboard comunica a narrativa de forma clara e emocional.
- [ ] Prototipos mantem ritmo e pacing adequados ao conteudo.
- [ ] Transicoes e animacoes reforcam a narrativa, nao distraem.

## Communication Protocol

| Etapa                    | Canal                          | Responsavel         |
|--------------------------|--------------------------------|---------------------|
| Kickoff de narrativa     | Reuniao 45min presencial/video | Ambos leads         |
| Solicitacao formal       | Asana task com template        | Squad solicitante   |
| Review de storyboard     | Sessao de feedback no Figma    | Storytelling Lead   |
| Review de script         | Comment no Google Docs / Notion| Design Lead         |
| Aprovacao final          | Asana task update + Slack      | Lead do squad receptor |
| Publicacao de assets     | PR no repositorio compartilhado| Design Lead         |
## SLA

| Tipo de solicitacao            | Tempo de resposta | Tempo de entrega    |
|--------------------------------|-------------------|---------------------|
| Narrativa para novo produto    | 8h uteis          | 7 dias uteis        |
| Script de onboarding           | 4h uteis          | 5 dias uteis        |
| Arco de experiencia            | 8h uteis          | 5 dias uteis        |
| Storyboard visual              | 4h uteis          | 5 dias uteis        |
| Assets para case study         | 4h uteis          | 3 dias uteis        |
## Escalation

1. **SLA expirado**: mention no Slack #design-x-storytelling com link da task e impacto.
2. **+24h sem resposta**: DM para o lead responsavel descrevendo bloqueio.
3. **+48h sem resolucao**: reuniao de desbloqueio com ambos leads e PM.
4. **Risco em lancamento**: acionar versao simplificada da narrativa usando templates existentes e registrar divida de storytelling.

## Rework Loop

1. Squad receptor documenta feedback com exemplos visuais ou textuais concretos.
2. Classificar como `tone-adjustment` (ajuste de tom), `structure-change` (mudanca de arco) ou `asset-revision` (retrabalho visual).
3. **Tone-adjustment**: resolver via comments assincronos, prazo de 2 dias uteis.
4. **Structure-change**: reuniao de realinhamento de 45min, novo prazo de 5 dias uteis.
5. **Asset-revision**: lista especifica de alteracoes visuais, prazo de 3 dias uteis.
6. Maximo de 2 ciclos para tone-adjustment e asset-revision. Structure-change permite 1 adicional.
## Cross-References

- `./cross-squad-handoff-protocol.md` — protocolo generico de handoff.
- `../../storytelling/narratives/narrative-templates.md` — templates de narrativa.
- `../design-system/assets/illustration-library/` — biblioteca de ilustracoes.
- `../design-system/assets/animation-assets/` — repositorio de animacoes.
