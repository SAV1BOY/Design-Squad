# Handoff Contract: Design Squad <-> Advisory Board Squad

## Metadata

| Campo             | Valor                                      |
|-------------------|--------------------------------------------|
| parties           | Design Squad, Advisory Board Squad         |
| direction         | Bidirecional                               |
| created           | 2026-03-18                                 |
| version           | 1.0                                        |
| owners            | Design Lead, Advisory Board Lead           |
| review-cycle      | Trimestral                                 |
| status            | Ativo                                      |
## Trigger

### Design -> Advisory Board
- Fechamento de ciclo trimestral com scorecard de maturidade e evolucao de praticas de design.
- Identificacao de riscos operacionais ou de qualidade que requerem orientacao de governanca.
- Necessidade de validacao de conformidade com padroes organizacionais antes de lancamentos criticos.

### Advisory Board -> Design
- Publicacao ou revisao de governance-guidelines que impactam processos de design.
- Atualizacao de industry-benchmarks que alteram expectativas de qualidade ou maturidade.
- Definicao de novos organizational-standards para padronizacao entre squads.
## Pre-conditions

### Para Design enviar
- Scorecard trimestral consolidado com dados de todos os projetos do ciclo.
- Risk-assessment revisado internamente pelo Design Lead com input de Tech Lead.
- Evidencias de evolucao de maturidade documentadas com comparativo ao ciclo anterior.

### Para Advisory Board enviar
- Guidelines aprovadas em sessao formal do Advisory Board com quorum minimo.
- Benchmarks validados com fontes externas reconhecidas e contextualizados para a organizacao.
- Standards documentados em formato estruturado com criterios de aceitacao claros.

## Handoff Package

### Design envia para Advisory Board
| Deliverable                        | Formato              | Obrigatorio |
|------------------------------------|----------------------|-------------|
| quarterly-scorecard                | Spreadsheet + PDF    | Sim         |
| maturity-evolution                 | Notion page + Slides | Sim         |
| risk-assessments                   | Notion page + PDF    | Sim         |
| compliance-evidence                | Notion page          | Nao         |
### Advisory Board envia para Design
| Deliverable                        | Formato              | Obrigatorio |
|------------------------------------|----------------------|-------------|
| governance-guidelines              | PDF + Notion page    | Sim         |
| industry-benchmarks                | Spreadsheet + PDF    | Sim         |
| organizational-standards           | Notion page + PDF    | Sim         |
| audit-findings                     | PDF                  | Nao         |

### Shared artifacts
- `governance-framework`: documento em Notion que define principios, politicas e processos de governanca aplicaveis a pratica de design na organizacao.
- `maturity-model`: modelo compartilhado em Spreadsheet que estabelece niveis de maturidade, criterios de avaliacao e metas por dimensao de design.
## Quality Gate on Send

### Checklist antes de Design enviar
- [ ] Scorecard preenchido com dados quantitativos e qualitativos de todas as dimensoes do maturity-model.
- [ ] Risk-assessments classificados por severidade (critico, alto, medio, baixo) com plano de mitigacao.
- [ ] Maturity-evolution inclui comparativo visual com ciclo anterior e projecao para proximo ciclo.
- [ ] Documentos revisados por Design Lead e pelo menos um senior designer do squad.

### Checklist antes de Advisory Board enviar
- [ ] Guidelines aprovadas em ata formal com assinaturas dos membros presentes.
- [ ] Benchmarks incluem fonte, data de coleta e metodologia de comparacao.
- [ ] Standards contem criterios objetivos de verificacao, nao apenas recomendacoes subjetivas.
- [ ] Documentos versionados com changelog explicito em relacao a versao anterior.
## Quality Gate on Receive

### Design valida ao receber de Advisory Board
- [ ] Guidelines sao aplicaveis ao contexto operacional do Design Squad sem ambiguidades.
- [ ] Benchmarks sao relevantes para o segmento e escala da organizacao.
- [ ] Standards incluem prazo de adequacao realista considerando o roadmap em andamento.
- [ ] Nao ha contradicoes entre novos standards e guidelines ja vigentes.

### Advisory Board valida ao receber de Design
- [ ] Scorecard cobre todas as dimensoes acordadas no maturity-model.
- [ ] Risk-assessments estao fundamentados em dados e nao apenas em percepcoes.
- [ ] Maturity-evolution demonstra tendencia consistente com os planos de acao anteriores.

## Communication Protocol

| Etapa                   | Canal                          | Responsavel            |
|-------------------------|--------------------------------|------------------------|
| Envio de guidelines     | Email formal + Notion          | Advisory Board Lead    |
| Apresentacao trimestral | Reuniao de governanca 90min    | Design Lead            |
| Feedback de conformidade| Notion comments + email        | Advisory Board Lead    |
| Aprovacao de scorecard  | Email formal + ata de reuniao  | Advisory Board Lead    |
| Acompanhamento mensal   | Report async via Notion        | Design Lead            |

## SLA

| Tipo de solicitacao                  | Tempo de resposta | Tempo de entrega   |
|--------------------------------------|-------------------|--------------------|
| Revisao de scorecard trimestral      | 2 semanas         | 4 semanas          |
| Publicacao de novas guidelines       | 1 semana          | 1 mes              |
| Avaliacao de risk-assessment         | 1 semana          | 2 semanas          |
| Atualizacao de benchmarks            | 2 semanas         | 1 mes              |

## Escalation

1. **SLA expirado**: lembrete formal via email ao Advisory Board Lead com status e impacto documentados.
2. **+2 semanas sem resposta**: reuniao extraordinaria solicitada entre Design Lead e Advisory Board Lead.
3. **+1 mes sem resolucao**: escalar para Head of Design e presidente do Advisory Board.
4. **Bloqueio de conformidade**: Design Squad registra excecao formal e opera com ultimo standard aprovado.
## Rework Loop

1. Receptor documenta inconsistencia ou lacuna com referencia ao criterio de qualidade nao atendido.
2. Classificar como `data-gap` (informacao faltante), `methodology-revision` (mudanca de abordagem) ou `standard-update` (novo padrao requerido).
3. **Data-gap**: complementar com dados adicionais, prazo de 1 semana.
4. **Methodology-revision**: sessao de alinhamento de 60min entre leads, novo prazo de 2 semanas.
5. **Standard-update**: requer aprovacao do Advisory Board em sessao formal, prazo de 1 mes.
## Cross-References

- `./cross-squad-handoff-protocol.md` — protocolo generico de handoff.
- `./quarterly-design-review.md` — workflow de revisao trimestral de design.
- `../../advisory-board/governance/governance-framework.md` — framework de governanca oficial.
- `../../advisory-board/maturity/maturity-model.md` — modelo de maturidade compartilhado.
