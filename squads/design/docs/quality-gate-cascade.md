# Quality Gate Cascade

> Documentação operacional do sistema de quality gates do Design Squad.
> Linguagem mista: headers em English, conteúdo em PT-BR, termos técnicos em English.

---

## 1. Cascade Overview

O sistema de quality gates opera em cascata — cada artefato passa por gates progressivamente mais rigorosos. Se um gate falha, o artefato retorna ao responsável com feedback específico.

```
Agent Gate → Inter-Agent Gate → Domain Gate → Mandatory Gate → Chief Gate → Cross-Squad Gate
```

Nenhum gate pode ser pulado. A ordem é sequencial — um gate só é acionado se o anterior foi aprovado.

---

## 2. Gate Levels

### Gate 1: Agent-Level Gate

- **Valida:** Agent executor verifica seu trabalho contra o checklist da task antes de submeter
- **Owner:** Agent executor (jessica-ux-ui, ux-design-expert, design-system-architect, etc.)
- **Checklist:** Mapeado na task via config.yaml routing (ex: `checklists/wireframe-quality`)
- **Pass:** 100% dos itens obrigatórios. Falha = agent corrige antes de submeter (não é rework formal)

### Gate 2: Inter-Agent Gate

- **Valida:** Transição entre agents — output atende requisitos de input do próximo agent
- **Owner:** Agent receptor
- **Gates configurados:** `ux-to-ui-transition`, `ui-to-ds-transition`, `ds-to-handoff-transition` (ver config.yaml → quality_gates → inter_agent)
- **Pass:** Definido por gate. Falha = retorna ao agent de origem com itens faltantes

### Gate 3: Domain Gate

- **Valida:** Artefato atende padrões do domínio (design system, research, prototyping)
- **Owner:** `component-spec-quality` → design-system-architect | `usability-test-quality` → ux-design-expert | `metrics-review-quality` → design-chief
- **Pass:** Mínimo 90% (gate_pass_domain). Itens faltantes exigem justificativa documentada
- **Falha:** Rework loop — ver rework-loop-protocol.md

### Gate 4: Mandatory Gate

- **Valida:** Requisitos obrigatórios para TODAS as tasks — inegociável
- **Owner:** `discovery-brief-quality` → design-chief | `accessibility-quality` → ux-design-expert | `handoff-quality` → design-chief
- **Pass:** 100% dos itens — sem exceção. **NÃO pode ser overridden.**
- **Falha:** Bloqueia avanço. Rework obrigatório.

### Gate 5: Chief Gate

- **Valida:** Alinhamento estratégico, qualidade global e fit com produto
- **Owner:** design-chief (exclusivo). Acionado para tasks com `approver: design-chief` no agent_sequence
- **Pass:** Alinhamento com princípios (evidence_over_opinion, system_first, accessibility_by_default)
- **Falha:** design-chief fornece direcionamento específico — nunca apenas "reprovado"

### Gate 6: Cross-Squad Gate

- **Valida:** Output atende critérios de aceitação do squad receptor
- **Owner:** design-chief + lead do squad receptor
- **Gates:** `design-to-copy-handoff`, `brand-to-design-receive` (config.yaml → quality_gates → inter_squad)
- **Pass:** Conforme contrato do squad. Falha = devolver com feedback específico

---

## 3. Override Rules

| Gate            | Override por     | Condição                                     | Documentação             |
|-----------------|-----------------|----------------------------------------------|--------------------------|
| Agent gate      | Agent executor   | Itens não aplicáveis ao contexto             | Nota no checklist        |
| Domain gate     | design-chief     | Justificativa + score ≥ 80%                  | Entry em decisions-log   |
| Inter-agent gate| design-chief     | Urgência comprovada + plano de correção      | decisions-log + prazo    |
| Chief gate      | design-chief     | Decisão própria com justificativa            | Entry em decisions-log   |

**NUNCA overridable:** Mandatory gates (discovery-brief, accessibility, handoff). Violações críticas de WCAG 2.1 AA bloqueiam release sem exceção. Override sem documentação em decisions-log é incidente operacional.

---

## 4. Scoring Thresholds

| Score        | Classificação       | Ação                                                    |
|-------------|---------------------|----------------------------------------------------------|
| **< 80%**   | REWORK              | Retorna ao agent. Rework obrigatório (max 3 iterações)  |
| **80-89%**  | PASS (condicional)  | Aprovado para domain gates com justificativa             |
| **90-94%**  | PASS                | Aprovado. Padrão operacional.                            |
| **95-97%**  | GOLD                | Excelente. Registrar como referência interna.            |
| **≥ 98%**   | SOTA                | State of the Art. Benchmark + case study.                |

**Cálculo:** `Score = (itens aprovados / total de itens aplicáveis) × 100`. Itens N/A removidos do total. Itens `[REQUIRED]` têm peso 2x.

**GOLD:** Registrar em `data/registries/governance-registry.yaml`. Compartilhar no design-critique semanal.
**SOTA:** Incluir no quarterly-design-review. Considerar case study via storytelling_squad.

---

## 5. Documentation on Gate Failure

Quando um gate reprova, o reviewer documenta:

### Feedback de rework (formato obrigatório)

```
GATE FAILURE — [gate] | Artefato: [nome] | Score: X% | Iteração: [1|2|3]/3
Reviewer: [agent] | Data: YYYY-MM-DD | Prazo reentrega: YYYY-MM-DD

ITENS REPROVADOS:
1. [item ID] — [problema] → [correção esperada]
2. ...
```

### No registry da task

```yaml
quality_gate_history:
  - gate: "[nome]"
    date: "YYYY-MM-DD"
    score: "X%"
    result: "[pass|fail|override]"
    reviewer: "[agent]"
```

Em caso de override, registrar em `data/registries/decisions-log.yaml` com: id (OVR-YYYY-NNN), gate, score original, overridden_by, justificativa e remediation_deadline.

---

## 6. Quick Reference Table

| Step | Gate             | Quem executa           | Threshold | Blocking? | Override? |
|------|------------------|------------------------|-----------|-----------|-----------|
| 1    | Agent gate       | Agent executor         | 100%      | Self      | Sim       |
| 2    | Inter-agent gate | Agent receptor         | 100%      | Sim       | Chief     |
| 3    | Domain gate      | Domain specialist      | 90%       | Sim       | Chief     |
| 4    | Mandatory gate   | Gate owner             | 100%      | Sim       | **Não**   |
| 5    | Chief gate       | design-chief           | N/A       | Sim       | Chief     |
| 6    | Cross-squad gate | design-chief + externo | 100%      | Sim       | **Não**   |

---

## Cross-References

- `config.yaml` → `quality_gates` — Definição de todos os gates, owners e critérios
- `config.yaml` → `score_thresholds` — Thresholds numéricos (80% rework, 95% GOLD, 98% SOTA)
- `checklists/` — Todos os checklists referenciados pelos gates
- `ARCHITECTURE.md` seção 19 — Visão arquitetural do sistema de qualidade
- `agents/design-chief.md` — Autoridade para gates e overrides
- `docs/rework-loop-protocol.md` — Protocolo de rework quando gate reprova
- `docs/escalation-protocol.md` — Escalação quando rework excede 3 iterações
- `docs/gold-standard-and-sota.md` — Definição dos níveis GOLD e SOTA
- `data/registries/decisions-log.yaml` — Registro de overrides
- `data/registries/governance-registry.yaml` — Registro de artefatos GOLD e SOTA
