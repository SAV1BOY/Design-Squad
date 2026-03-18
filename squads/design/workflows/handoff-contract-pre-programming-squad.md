# Handoff Contract: Design Squad <-> Pre-Programming Squad

## Metadata

| Campo             | Valor                                      |
|-------------------|--------------------------------------------|
| parties           | Design Squad, Pre-Programming Squad        |
| direction         | Bidirecional                               |
| created           | 2026-03-18                                 |
| version           | 1.0                                        |
| owners            | Design Lead, Pre-Programming Lead          |
| review-cycle      | Trimestral                                 |
| status            | Ativo                                      |
## Trigger

### Design -> Pre-Programming
- Novo componente ou feature aprovado no design critique requer avaliacao de viabilidade tecnica.
- Atualizacao de design tokens impacta componentes existentes e exige escopo de implementacao.
- Especificacao de interacao complexa precisa de validacao de performance antes da implementacao.

### Pre-Programming -> Design
- Restricao tecnica descoberta durante scoping que inviabiliza abordagem de design proposta.
- Nova capacidade de API disponivel que habilita padroes de interacao antes nao possiveis.
- Budget de performance atualizado que impacta animacoes ou carregamento de assets.
## Pre-conditions

### Para Design enviar
- Design specs passaram por design critique interno com feedback incorporado.
- Component specs estao documentados com todos os estados, variantes e breakpoints.
- Token specs estao alinhados com o design system vigente e versionados.

### Para Pre-Programming enviar
- Restricoes tecnicas foram validadas com a arquitetura atual do sistema.
- Capacidades de API estao documentadas com endpoints, payloads e limitacoes.
- Budget de performance foi mensurado com ferramentas de profiling em ambiente de staging.
## Handoff Package

### Design envia para Pre-Programming
| Deliverable                   | Formato          | Obrigatorio |
|-------------------------------|------------------|-------------|
| design-specs                  | Figma link + PDF | Sim         |
| component-specs               | Figma + Notion   | Sim         |
| token-specs                   | JSON / YAML      | Sim         |
| interaction-specs             | Figma prototype  | Sim         |
| asset-package                 | Figma export SVG/PNG | Sim     |
### Pre-Programming envia para Design
| Deliverable                   | Formato          | Obrigatorio |
|-------------------------------|------------------|-------------|
| technical-constraints         | Notion page      | Sim         |
| api-capabilities              | Swagger / Notion | Sim         |
| platform-limitations          | Spreadsheet      | Sim         |
| performance-budgets           | Notion page      | Sim         |
### Shared artifacts
- `component-api-contracts`: contratos de API por componente mantidos no repositorio do design system, editaveis por ambos os squads.
- `design-token-files`: arquivos de tokens em JSON/YAML sincronizados entre Figma e codebase via pipeline automatizado.

## Quality Gate on Send

### Checklist antes de Design enviar
- [ ] Todos os estados do componente estao especificados (default, hover, active, disabled, error, loading).
- [ ] Tokens de cor, tipografia e espacamento estao mapeados e nao usam valores hardcoded.
- [ ] Interacoes possuem especificacao de timing, easing e comportamento responsivo.
- [ ] Assets estao exportados nos formatos e resolucoes corretos para cada plataforma.
- [ ] Specs incluem anotacoes de acessibilidade (roles, labels, ordem de foco).

### Checklist antes de Pre-Programming enviar
- [ ] Restricoes tecnicas incluem justificativa e alternativa viavel quando aplicavel.
- [ ] Capacidades de API estao documentadas com exemplos de request/response.
- [ ] Limitacoes de plataforma especificam versoes e dispositivos afetados.
- [ ] Budget de performance inclui metricas de referencia (LCP, FID, CLS).

## Quality Gate on Receive

### Design valida ao receber de Pre-Programming
- [ ] Restricoes tecnicas nao invalidam o objetivo de experiencia do usuario.
- [ ] Alternativas propostas mantem a intencao de design original.
- [ ] Budget de performance e compativel com as interacoes especificadas.
- [ ] Limitacoes de plataforma estao mapeadas com fallbacks aceitaveis.

### Pre-Programming valida ao receber de Design
- [ ] Especificacoes sao implementaveis com o stack tecnologico atual.
- [ ] Tokens estao no formato correto e sao parseados sem erro pelo pipeline.
- [ ] Assets possuem tamanho e formato otimizados para performance.

## Communication Protocol

| Etapa                | Canal                  | Responsavel     |
|----------------------|------------------------|-----------------|
| Solicitacao inicial  | Asana task com template| Squad solicitante|
| Duvidas e alinhamento| Thread no Slack #design-x-preprog | Ambos  |
| Review sincrona      | Reuniao 45min max      | Ambos leads     |
| Entrega final        | PR no repo + Asana update | Squad entregando |
| Confirmacao          | Emoji check no Slack thread | Squad receptor |

## SLA

| Tipo de solicitacao          | Tempo de resposta | Tempo de entrega |
|------------------------------|-------------------|------------------|
| Avaliacao de viabilidade     | 4h uteis          | 2 dias uteis     |
| Component spec completo      | 4h uteis          | 3 dias uteis     |
| Atualizacao de tokens        | 2h uteis          | 1 dia util       |
| Restricao tecnica critica    | 2h uteis          | 4h uteis         |

## Escalation

1. **SLA expirado**: lembrete no Slack com @mention do lead responsavel.
2. **+24h**: escalar para Head of Design e Head of Pre-Programming via DM conjunta.
3. **+48h**: reuniao de desbloqueio com leads, Tech Lead e PM.
4. **Impacto em release**: implementar versao simplificada aprovada por ambos os leads como solucao temporaria.

## Rework Loop

1. Squad receptor abre issue no repositorio ou comment no Figma descrevendo o problema especifico.
2. Classificar rework como `minor` (ajuste de valor ou formato) ou `major` (reespecificacao de componente).
3. **Minor**: resolver via thread assincrona, prazo de 1 dia util.
4. **Major**: sessao de 45min para alinhar, novo prazo de 3 dias uteis.
5. Maximo de 2 ciclos de rework. Apos isso, escalar para leads.

## Cross-References

- `./cross-squad-handoff-protocol.md` — protocolo generico de handoff.
- `../processes/design-critique-loop.md` — critique pre-handoff.
- `../../pre-programming/guidelines/technical-feasibility.md` — criterios de viabilidade do Pre-Programming Squad.
