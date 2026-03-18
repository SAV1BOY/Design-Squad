# Escalation Protocol

> Protocolo operacional de escalação do Design Squad.
> Linguagem mista: headers em English, conteúdo em PT-BR, termos técnicos em English.

---

## 1. Escalation Triggers

Escale imediatamente quando qualquer uma destas condições ocorrer:

| Trigger                    | Descrição                                                                 | Prazo para escalar        |
|---------------------------|---------------------------------------------------------------------------|---------------------------|
| **Time overrun**          | Agent não consegue resolver a task em 2x o tempo estimado                 | Assim que detectado       |
| **Quality gate failure**  | Quality gate reprova o mesmo artefato 3x consecutivas                     | Na terceira reprovação    |
| **Agent disagreement**    | Dois ou mais agents discordam sobre abordagem e não há consenso em 24h    | Após 24h sem resolução    |
| **External block**        | Dependência de outro squad ou stakeholder bloqueia task por 3+ dias úteis | No terceiro dia útil      |
| **Scope conflict**        | Stakeholder pede mudança que contradiz pesquisa ou dados existentes       | Imediatamente             |
| **Resource overload**     | Squad sobrecarregado sem possibilidade de repriorizacao interna           | Quando confirmado         |

---

## 2. Escalation Levels

A escalação segue uma cadeia hierárquica. Nunca pule níveis, exceto em emergências (ex: bloqueio total de release).

### Level 1 — Agent → Design Chief

- **Quem escala:** Qualquer agent do squad (brad-frost, dan-mall, dave-malouf, jessica-ux-ui, ux-design-expert, design-system-architect, nano-banana-generator)
- **Para quem:** design-chief
- **Quando:** Time overrun, quality gate failure (1ª ou 2ª), disagreement entre agents, bloqueio interno
- **SLA de resposta:** 4 horas úteis
- **Ação esperada:** design-chief avalia, reatribui task, arbitra decisão ou convoca sessão de troubleshooting

### Level 2 — Design Chief → PM Lead

- **Quem escala:** design-chief
- **Para quem:** PM Lead (product management)
- **Quando:** Bloqueio cross-squad por 3+ dias úteis, conflito de prioridade entre squads, scope conflict com stakeholders, dependência externa não resolvida
- **SLA de resposta:** 1 dia útil
- **Ação esperada:** PM Lead renegocia prioridades, media conflito entre squads, ajusta roadmap se necessário

### Level 3 — PM Lead → HRM Chief

- **Quem escala:** PM Lead ou design-chief (com autorização do PM Lead)
- **Para quem:** HRM Chief / Central Command
- **Quando:** Conflito de prioridade não resolvido em 5 dias úteis, necessidade de realocação de recursos entre squads, bloqueio sistêmico que afeta múltiplos squads
- **SLA de resposta:** 2 dias úteis
- **Ação esperada:** HRM Chief arbitragem final, realocação de recursos, decisão estratégica

---

## 3. Communication Format

Cada escalação DEVE incluir as seguintes informações, formatadas de forma estruturada.

### Level 1 — Mensagem para Design Chief

```
ESCALATION — Level 1
Agent: [nome do agent]
Task: [nome da task conforme config.yaml routing]
Trigger: [time_overrun | quality_failure | disagreement | block]
Contexto: [descrição objetiva do problema em 2-3 linhas]
Tentativas de resolução: [o que já foi feito]
Impacto: [o que está bloqueado, deadline em risco]
Ação solicitada: [o que você precisa do design-chief]
```

### Level 2 — Mensagem para PM Lead

```
ESCALATION — Level 2
Escalado por: design-chief
Origem: [agent + task original]
Trigger: [cross_squad_block | priority_conflict | scope_conflict]
Histórico: [resumo do Level 1 + ações já tomadas]
Impacto no squad: [tasks bloqueadas, deadlines comprometidos]
Impacto no produto: [releases afetadas, métricas em risco]
Proposta de resolução: [1-2 opções concretas]
Prazo necessário: [data limite para decisão]
```

### Level 3 — Mensagem para HRM Chief

```
ESCALATION — Level 3
Escalado por: PM Lead + design-chief
Histórico completo: [timeline desde Level 1]
Squads envolvidos: [lista de squads afetados]
Impacto organizacional: [escopo do impacto]
Opções de resolução: [mínimo 2 opções com trade-offs]
Recomendação: [opção preferida com justificativa]
Documentação de suporte: [links para registries e decisões]
```

---

## 4. Response Time Expectations

| Level | SLA de Resposta   | SLA de Resolução      | Formato de Resposta       |
|-------|------------------|-----------------------|---------------------------|
| 1     | 4 horas úteis    | 1 dia útil            | Mensagem no canal + ação  |
| 2     | 1 dia útil       | 3 dias úteis          | Documento + reunião sync  |
| 3     | 2 dias úteis     | 5 dias úteis          | Decisão formal registrada |

Se o SLA de resposta não for cumprido, o escalador avança automaticamente para o próximo nível com nota de "SLA breach" no histórico.

---

## 5. Resolution Documentation

Toda escalação resolvida DEVE ser documentada em `data/registries/decisions-log.yaml` com o seguinte formato:

```yaml
- id: ESC-YYYY-NNN
  date: "YYYY-MM-DD"
  trigger: "[tipo do trigger]"
  level_reached: [1|2|3]
  agents_involved: [lista]
  task: "[task name]"
  problem_summary: "[resumo do problema]"
  resolution: "[decisão tomada]"
  rationale: "[justificativa baseada em evidências]"
  outcome: "[resultado após resolução]"
  time_to_resolve: "[dias úteis]"
  lessons_learned: "[o que pode ser melhorado]"
```

Adicionalmente:
- Se a escalação gerou mudança de processo, registrar em `data/registries/lessons-learned-registry.yaml`
- Se a escalação envolveu rework, registrar também no registry da task afetada
- Design-chief revisa escalações mensalmente no `design-ops-sync` semanal para identificar padrões

---

## Cross-References

- `agents/design-chief.md` — Autoridade e heurísticas de decisão do orchestrator
- `config.yaml` → seção `escalation_rules` — Triggers e ações de escalação configuradas
- `data/registries/decisions-log.yaml` — Registro de todas as decisões de escalação
- `data/registries/lessons-learned-registry.yaml` — Lessons learned de escalações passadas
- `docs/operating-system.md` — Cadência operacional e fluxo de decisão
- `docs/rework-loop-protocol.md` — Protocolo de rework (trigger de escalação Level 1)
- `docs/quality-gate-cascade.md` — Quality gates que podem gerar escalação
