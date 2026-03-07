# Design Critique Loop

## Metadata

| Campo         | Valor                                    |
| ------------- | ---------------------------------------- |
| squad         | Design                                   |
| versao        | 1.0.0                                    |
| criado_em     | 2026-03-06                               |
| owner         | Design Lead                              |
| cadencia      | 1-2x por semana (recorrente)             |
| duracao_media | 60 minutos por sessao                    |
| tags          | critique, feedback, decisao, peer-review |

## Trigger

Quando iniciar:

- Sessao recorrente no calendario semanal (ver `weekly-design-ops-cadence.md`).
- Designer solicita feedback ad-hoc em WIP.
- Decisao controversa que precisa de alinhamento do grupo.
- Pre-handoff review para garantir qualidade.

Pre-condicoes: presenter preparou material com contexto; min 3 participantes; facilitador designado (rotativo); 60 min reservados.

## Phases

### Fase 1 — Critique (60 min)
**Agents:** Facilitador, Presenter, Reviewers (designers + convidados).
**Inputs:** Trabalho a ser revisado (Figma link), contexto escrito (problema, constraints, perguntas), framework de critique.

**Estrutura da sessao:**
1. **Setup (5 min):** Facilitador explica formato. Foco no problema, feedback actionable.
2. **Apresentacao (7 min):** Presenter compartilha problema, constraints, alternativas exploradas, perguntas especificas.
3. **Silent review (5 min):** Participantes exploram individualmente, anotam feedback.
4. **Feedback round (20 min):** Likes (o que funciona), Wishes (o que melhorar), Questions (duvidas sobre decisoes).
5. **Discussao aberta (15 min):** Aprofundar temas — evitar solucionamento em real-time.
6. **Wrap-up (8 min):** Presenter resume takeaways, action items com owners.

**Outputs:** Feedback documentado, action items com owners e prazos, gravacao (opcional).

### Fase 2 — Decisao
**Agents:** Designer (Presenter), Design Lead (se alto impacto).
**Inputs:** Feedback da critique, constraints do projeto, dados disponiveis.
**Atividades:** Categorizar feedback (incorporar/explorar depois/descartar); para alto impacto consultar Design Lead; usar dados como desempate; documentar rationale.
**Outputs:** Decisoes com rationale, lista de feedback aceito/adiado/descartado.

### Fase 3 — Registro
**Agents:** Designer.
**Inputs:** Decisoes tomadas, feedback categorizado.
**Atividades:** Registrar decisoes no design doc ou Figma annotations; atualizar design; linkar decisoes ao contexto; arquivar alternativas descartadas (nao deletar); atualizar tracker.
**Outputs:** Design doc atualizado, alternativas arquivadas, tracker atualizado.

### Fase 4 — Follow-up
**Agents:** Facilitador, Designer.
**Inputs:** Action items, timeline do projeto.
**Atividades:** Verificar progresso no proximo standup; se exploracao necessaria, agendar timebox; apresentar resultado na proxima critique; coletar meta-feedback sobre o formato; rotacionar facilitador.
**Outputs:** Action items concluidos, meta-feedback, proximo facilitador definido.

## Quality Gates

### Gate Pre-Critique
- [ ] Presenter preparou contexto (problema, constraints, perguntas).
- [ ] Min 3 participantes confirmados.
- [ ] Facilitador designado.

### Gate Critique -> Decisao
- [ ] Feedback documentado e acessivel.
- [ ] Action items com owners.

### Gate Decisao -> Registro
- [ ] Cada feedback categorizado.
- [ ] Rationale documentado para decisoes de alto impacto.

### Gate Registro -> Follow-up
- [ ] Decisoes no design doc.
- [ ] Alternativas arquivadas.
- [ ] Action items com deadlines.

## Cross-References

- `weekly-design-ops-cadence.md` — Critique na cadencia semanal (Fase 2).
- `feature-design-end-to-end.md` — Aplicavel em qualquer fase do design.
- `design-sprint-5-day.md` — Sprint tem critique integrada (Dia 3).
- `quarterly-design-review.md` — Patterns de critique alimentam review.
- `new-designer-onboarding.md` — Novos designers aprendem o formato.
- `ralphlooping-kaizen-design.md` — Critique alimenta iteracao continua.
