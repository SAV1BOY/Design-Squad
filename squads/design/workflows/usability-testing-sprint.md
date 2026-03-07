# Usability Testing Sprint

## Metadata

| Campo         | Valor                                     |
| ------------- | ----------------------------------------- |
| squad         | Design                                    |
| versao        | 1.0.0                                     |
| criado_em     | 2026-03-06                                |
| owner         | UX Researcher                             |
| cadencia      | Por demanda (recomendado 1x por sprint)   |
| duracao_media | 5-8 dias uteis                            |
| tags          | usability, testing, research, sintese     |

## Trigger

Quando iniciar:

- Prototipo de nova feature pronto para validacao externa.
- Redesign significativo antes do handoff.
- Metricas indicam problema de usabilidade (drop-off, erros).
- Stakeholder solicita evidencia para decisao controversa.

Pre-condicoes: prototipo navegavel ou build em staging; hipoteses documentadas; acesso a participantes; Designer e Researcher alinhados.

## Phases

### Fase 1 — Planejamento (2-3 dias)
**Agents:** Researcher, Designer, PM.
**Inputs:** Prototipo, hipoteses, perfil de usuario alvo.
**Atividades:** Definir objetivos (max 3 perguntas); escolher metodo (moderado, nao-moderado, guerrilla); criar roteiro com tarefas e cenarios; definir metricas (task success, time on task, SUS); recrutar 5-8 participantes; pilot test com colega.
**Outputs:** Plano documentado, roteiro validado, participantes agendados, setup testado.

### Fase 2 — Execucao (2-3 dias)
**Agents:** Researcher (moderador), Designer (observador), note-taker.
**Inputs:** Plano, roteiro, participantes agendados.
**Atividades:** Sessoes individuais (30-45 min cada); note-taker registra em rainbow spreadsheet; gravar tela e audio; debriefing rapido apos cada sessao; ajustar roteiro se problemas criticos surgem cedo.
**Outputs:** Gravacoes, notas por participante, observacoes iniciais.

### Fase 3 — Sintese (1-2 dias)
**Agents:** Researcher, Designer.
**Inputs:** Notas, gravacoes, metricas coletadas.
**Atividades:** Affinity mapping por tema; calcular metricas quantitativas; patterns = 3+ participantes; classificar por severidade (critico, maior, menor, oportunidade); criar highlight reel (2-3 min).
**Outputs:** Relatorio de findings, highlight reel, metricas consolidadas, affinity map.

### Fase 4 — Priorizacao (0.5 dia)
**Agents:** Designer, PM, Researcher, Tech Lead.
**Inputs:** Relatorio, roadmap, esforco tecnico estimado.
**Atividades:** Apresentar findings (30 min); mapear contra roadmap; priorizar (severidade x esforco); definir o que entra no sprint vs backlog; atribuir owners.
**Outputs:** Lista priorizada com owners, items no backlog, trade-offs documentados.

### Fase 5 — Iteracao (1-2 dias)
**Agents:** Designer, Frontend Engineer.
**Inputs:** Lista de correcoes, findings como referencia.
**Atividades:** Iterar no design; validar correcoes criticas com Researcher; atualizar prototipo; handoff das correcoes; agendar re-test se necessario.
**Outputs:** Design iterado, handoff realizado, proximo ciclo agendado (se aplicavel).

## Quality Gates

### Gate Planejamento -> Execucao
- [ ] Pilot test realizado e roteiro ajustado.
- [ ] Min 5 participantes recrutados.
- [ ] Setup tecnico validado.

### Gate Execucao -> Sintese
- [ ] Min 5 sessoes concluidas.
- [ ] Notas completas por sessao.

### Gate Sintese -> Priorizacao
- [ ] Findings classificados por severidade.
- [ ] Evidencias linkadas a cada finding.

### Gate Priorizacao -> Iteracao
- [ ] Priorizacao acordada com PM e Tech Lead.
- [ ] Owners atribuidos.

### Gate Iteracao -> Fechamento
- [ ] Correcoes criticas aplicadas.
- [ ] Handoff realizado.

## Cross-References

- `feature-design-end-to-end.md` — Teste ocorre apos Fase 4 (Prototipo).
- `design-critique-loop.md` — Critique pode preceder o teste.
- `research-to-design-pipeline.md` — Findings alimentam pipeline de pesquisa.
- `accessibility-remediation-loop.md` — Testes podem revelar problemas de a11y.
- `handoff-and-build-loop.md` — Correcoes seguem fluxo padrao de handoff.
