# Handoff Contract: Design Squad <-> Cybersecurity Squad

## Metadata

| Campo             | Valor                                      |
|-------------------|--------------------------------------------|
| parties           | Design Squad, Cybersecurity Squad          |
| direction         | Bidirecional                               |
| created           | 2026-03-18                                 |
| version           | 1.0                                        |
| owners            | Design Lead, Cybersecurity Lead            |
| review-cycle      | Trimestral                                 |
| status            | Ativo                                      |
## Trigger

### Design -> Cybersecurity
- Novo fluxo de autenticacao ou recuperacao de conta requer validacao de seguranca.
- Padrao de UX para consentimento ou privacidade precisa de revisao de conformidade.
- Redesign de tela com dados sensiveis demanda avaliacao de exposicao de informacao.

### Cybersecurity -> Design
- Novo requisito de seguranca impacta fluxos de usuario existentes e exige adaptacao de UX.
- Vulnerabilidade identificada em padrao de interacao requer correcao imediata no design.
- Atualizacao de norma de compliance (LGPD, SOC2) altera requisitos de consentimento e privacidade.
## Pre-conditions

### Para Design enviar
- Fluxos de autenticacao e consentimento estao documentados com todos os caminhos possiveis.
- Padroes de privacidade seguem as diretrizes atuais do design system.
- Review interno de UX foi realizado com foco em seguranca e edge cases de abuso.

### Para Cybersecurity enviar
- Requisitos de seguranca estao documentados com justificativa e norma de referencia.
- Vulnerabilidades possuem classificacao de severidade e vetor de ataque descrito.
- Padroes de autenticacao propostos foram testados contra cenarios de ataque conhecidos.
## Handoff Package

### Design envia para Cybersecurity
| Deliverable                   | Formato          | Obrigatorio |
|-------------------------------|------------------|-------------|
| security-ux-review            | Notion page      | Sim         |
| auth-flow-designs             | Figma link + PDF | Sim         |
| privacy-ux-patterns           | Figma link       | Sim         |
| consent-flows                 | Figma prototype  | Sim         |
### Cybersecurity envia para Design
| Deliverable                   | Formato          | Obrigatorio |
|-------------------------------|------------------|-------------|
| security-requirements         | Notion page      | Sim         |
| compliance-constraints        | Spreadsheet      | Sim         |
| vulnerability-reports         | Notion report    | Sim         |
| auth-patterns                 | Notion + diagrama| Sim         |
### Shared artifacts
- `auth-pattern-library`: biblioteca de padroes de autenticacao aprovados por seguranca e UX, mantida no design system.
- `privacy-consent-templates`: templates reutilizaveis de telas de consentimento e privacidade, validados por compliance.

## Quality Gate on Send

### Checklist antes de Design enviar
- [ ] Fluxos de autenticacao contemplam cenarios de forca bruta, phishing e engenharia social.
- [ ] Telas com dados sensiveis possuem mascaramento e niveis de visibilidade documentados.
- [ ] Consent flows atendem requisitos minimos de LGPD e politica de privacidade vigente.
- [ ] Padroes de recuperacao de conta incluem verificacao de identidade multi-fator.
- [ ] Anotacoes de acessibilidade nao comprometem requisitos de seguranca (ex: autocomplete em senhas).

### Checklist antes de Cybersecurity enviar
- [ ] Requisitos de seguranca incluem impacto esperado na experiencia do usuario.
- [ ] Padroes de autenticacao propostos especificam metodos e fatores aceitos.
- [ ] Restricoes de compliance referenciam norma e artigo especificos.
- [ ] Vulnerabilidades incluem recomendacao de correcao compativel com UX.

## Quality Gate on Receive

### Design valida ao receber de Cybersecurity
- [ ] Requisitos de seguranca sao implementaveis sem degradacao critica da experiencia do usuario.
- [ ] Padroes de autenticacao propostos sao compativeis com o design system existente.
- [ ] Restricoes de compliance possuem alternativas de UX quando impactam usabilidade.
- [ ] Correcoes de vulnerabilidade incluem prazo compativel com roadmap de design.

### Cybersecurity valida ao receber de Design
- [ ] Fluxos de autenticacao nao introduzem vetores de ataque conhecidos.
- [ ] Consent flows atendem requisitos legais minimos de coleta e armazenamento de dados.
- [ ] Padroes de privacidade nao expoe dados sensiveis em estados intermediarios.

## Communication Protocol

| Etapa                | Canal                  | Responsavel     |
|----------------------|------------------------|-----------------|
| Solicitacao inicial  | Asana task com template| Squad solicitante|
| Duvidas e alinhamento| Thread no Slack #design-x-cybersec | Ambos |
| Review sincrona      | Reuniao 30min max      | Ambos leads     |
| Entrega final        | Notion link + Asana update | Squad entregando |
| Confirmacao          | Emoji check no Slack thread | Squad receptor |

## SLA

| Tipo de solicitacao          | Tempo de resposta | Tempo de entrega |
|------------------------------|-------------------|------------------|
| Revisao de fluxo de auth     | 2h uteis          | 2 dias uteis     |
| Validacao de consent flow    | 4h uteis          | 3 dias uteis     |
| Correcao de vulnerabilidade  | 1h util           | 1 dia util       |
| Atualizacao de compliance    | 4h uteis          | 5 dias uteis     |

## Escalation

1. **SLA expirado**: lembrete no Slack com @mention do lead responsavel.
2. **+24h**: escalar para Head of Design e Head of Cybersecurity via DM conjunta.
3. **+48h**: reuniao de desbloqueio com leads, PM e compliance officer.
4. **Vulnerabilidade critica**: bypass de SLA padrao, correcao imediata com war room dedicada.

## Rework Loop

1. Squad receptor abre comment na Notion page descrevendo a falha de seguranca ou UX identificada.
2. Classificar rework como `minor` (ajuste de label ou fluxo secundario) ou `major` (redesign de fluxo de auth).
3. **Minor**: resolver via thread assincrona, prazo de 1 dia util.
4. **Major**: sessao de 45min com ambos os leads e security engineer, novo prazo de 3 dias uteis.
5. Maximo de 2 ciclos de rework. Apos isso, escalar para leads e compliance officer.

## Cross-References

- `./cross-squad-handoff-protocol.md` — protocolo generico de handoff.
- `../processes/design-critique-loop.md` — critique pre-handoff.
- `../../cybersecurity/guidelines/auth-security-standards.md` — padroes de seguranca de autenticacao do Cybersecurity Squad.
