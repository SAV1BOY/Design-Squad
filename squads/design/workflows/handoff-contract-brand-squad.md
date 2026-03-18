# Handoff Contract: Design Squad <-> Brand Squad

## Metadata

| Campo             | Valor                                      |
|-------------------|--------------------------------------------|
| parties           | Design Squad, Brand Squad                  |
| direction         | Bidirecional                               |
| created           | 2026-03-18                                 |
| version           | 1.0                                        |
| owners            | Design Lead, Brand Lead                    |
| review-cycle      | Trimestral                                 |
| status            | Ativo                                      |
## Trigger

### Design -> Brand
- Necessidade de novos icones que nao existem na iconografia-base aprovada.
- Proposta de extensao da paleta de cores para estados de UI nao cobertos.
- Aplicacao de marca em novo produto ou feature que precisa de validacao.

### Brand -> Design
- Atualizacao das brand-guidelines que impacta componentes de produto.
- Nova paleta-de-cores aprovada pela diretoria para implementacao em UI.
- Novos assets de iconografia-base adicionados ao repositorio oficial.
## Pre-conditions

### Para Design enviar
- Proposta discutida internamente no Design Squad critique.
- Aplicacoes de marca documentadas com screenshots e contexto.

### Para Brand enviar
- Guidelines aprovadas formalmente pelo Brand Manager.
- Paleta inclui valores HEX, RGB e HSL para design tokens.
- Icones exportados em SVG com artboard padronizado.

## Handoff Package

### Design envia para Brand
| Deliverable                        | Formato          | Obrigatorio |
|------------------------------------|------------------|-------------|
| aplicacoes-de-marca-em-produto     | Figma link + PDF | Sim         |
| extensoes-de-paleta-para-ui        | Figma + Spreadsheet | Sim      |
| proposta-de-novos-icones           | Figma link (SVG) | Sim         |
| contexto-de-uso                    | Notion page      | Sim         |
### Brand envia para Design
| Deliverable                        | Formato          | Obrigatorio |
|------------------------------------|------------------|-------------|
| brand-guidelines                   | PDF + Notion     | Sim         |
| paleta-de-cores                    | JSON tokens + PDF| Sim         |
| tipografia-aprovada                | Font files + spec| Sim         |
| iconografia-base                   | SVG library      | Sim         |

### Shared artifacts
- `color-tokens`: arquivo JSON no design system, fonte unica de verdade para cores.
- `typography-tokens`: arquivo JSON com escala tipografica para produto.
- `logo-assets`: repositorio compartilhado com versoes aprovadas de logotipos.
## Quality Gate on Send

### Checklist antes de Design enviar
- [ ] Proposta de icones segue o grid de 24x24px com 2px stroke da iconografia-base.
- [ ] Extensoes de paleta incluem contrast ratio documentado (WCAG AA minimo).
- [ ] Aplicacoes de marca mostram contexto real de produto, nao mockup generico.
- [ ] Arquivos Figma organizados em page dedicada com naming convention correto.

### Checklist antes de Brand enviar
- [ ] Valores de cor em HEX, RGB e HSL.
- [ ] Fontes incluem licenca para uso digital.
- [ ] Icones SVG otimizados (SVGO) sem metadata desnecessaria.
## Quality Gate on Receive

### Design valida ao receber de Brand
- [ ] Cores atendem contrast ratio WCAG AA para texto e componentes.
- [ ] Tipografia renderiza corretamente em todos os breakpoints alvo.
- [ ] Icones funcionam em 16px, 24px e 32px sem perda de legibilidade.
- [ ] Tokens sao compativeis com formato do design system, sem conflitos.

### Brand valida ao receber de Design
- [ ] Aplicacoes respeitam safe-zone e proporcoes do logo.
- [ ] Extensoes de paleta harmoniosas com a paleta principal.

## Communication Protocol

| Etapa                | Canal                       | Responsavel       |
|----------------------|-----------------------------|-------------------|
| Solicitacao inicial  | Asana task com template     | Squad solicitante |
| Apresentacao visual  | Reuniao 45min com screenshare| Squad entregando |
| Feedback estruturado | Figma comments com tags     | Squad receptor    |
| Aprovacao formal     | Asana task status + Slack   | Lead do squad receptor |
| Publicacao de tokens | PR no repositorio de tokens | Design Lead       |

## SLA

| Tipo de solicitacao            | Tempo de resposta | Tempo de entrega |
|--------------------------------|-------------------|------------------|
| Validacao de aplicacao de marca| 4h uteis          | 2 dias uteis     |
| Nova paleta / extensao         | 8h uteis          | 5 dias uteis     |
| Novos icones (ate 10)          | 4h uteis          | 5 dias uteis     |
| Atualizacao de guidelines      | 8h uteis          | 10 dias uteis    |
| Tipografia nova                | 8h uteis          | 7 dias uteis     |

## Escalation

1. **SLA expirado**: lembrete no Slack #design-x-brand com mention do lead responsavel.
2. **+24h sem resposta**: DM para Brand Lead e Design Lead com contexto e impacto.
3. **+48h sem resolucao**: escalar para Head of Design e Head of Brand.
4. **Bloqueio de release**: workaround temporario com tokens atuais, documentar divida.
## Rework Loop

1. Squad receptor documenta problema com annotated screenshots no Figma.
2. Classificar como `token-fix` (ajuste de valor), `style-revision` (mudanca estetica) ou `concept-change` (nova direcao).
3. **Token-fix**: resolver via PR direto, prazo de 1 dia util.
4. **Style-revision**: sessao de alinhamento de 30min, novo prazo de 3 dias uteis.
5. **Concept-change**: requer nova apresentacao e aprovacao, prazo de 5 dias uteis.
6. Maximo de 2 ciclos para style-revision. Concept-change reinicia o processo.
## Cross-References

- `./cross-squad-handoff-protocol.md` — protocolo generico de handoff.
- `../design-system/tokens/color-tokens.json` — tokens de cor.
- `../design-system/tokens/typography-tokens.json` — tokens tipograficos.
- `../../brand/guidelines/brand-guidelines.md` — brand guidelines oficiais.
