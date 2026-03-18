# Rework Loop Protocol

> Protocolo operacional de rework do Design Squad.
> Linguagem mista: headers em English, conteúdo em PT-BR, termos técnicos em English.

---

## 1. What Triggers a Rework

Rework é acionado quando um artefato de design falha em um quality gate. O artefato retorna ao agent executor com feedback específico para correção.

### Fontes de Rework

| Fonte                     | Exemplo                                                        | Gate relacionado              |
|--------------------------|----------------------------------------------------------------|-------------------------------|
| Agent-level gate         | Wireframe com fluxo incompleto                                 | wireframe-quality             |
| Inter-agent gate         | UI usando valores hardcoded em vez de tokens                   | ui-to-ds-transition           |
| Domain gate              | Componente sem spec de acessibilidade                          | component-spec-quality        |
| Mandatory gate           | Handoff sem assets exportados                                  | handoff-quality               |
| Chief review             | Artefato desalinhado com estratégia de produto                 | design-chief approval         |
| Cross-squad gate         | Contexto de tela incompleto para copy squad                    | design-to-copy-handoff        |

### O que NÃO é rework

- Iteração normal de design (exploração, refinamento) — isso é parte do processo
- Mudança de escopo por decisão de produto — isso é re-scoping, não rework
- Feedback positivo com sugestões opcionais — isso é melhoria, não correção

---

## 2. Feedback Format

Feedback que gera rework DEVE ser específico, acionável e rastreável. Feedback vago ("melhorar", "não está bom", "refazer") é proibido.

### Formato Obrigatório

```
REWORK REQUEST
Artefato: [nome do artefato]
Task: [task name conforme config.yaml routing]
Gate que reprovou: [nome do quality gate]
Reviewer: [agent que reprovou]
Iteração: [1|2|3] de 3

ITENS PARA CORREÇÃO:
1. [Item específico] — [o que está errado] → [o que é esperado]
2. [Item específico] — [o que está errado] → [o que é esperado]
3. ...

REFERÊNCIAS:
- Checklist aplicável: [path para checklist]
- Exemplo de referência: [link ou path se aplicável]

PRAZO: [data de reentrega]
```

**Exemplo ruim:** "A UI não está boa" / "Melhorar a acessibilidade"
**Exemplo bom:** "Botão primário usa #3366FF hardcoded → usar token `color.action.primary`" / "Input de email sem label → adicionar label conforme WCAG 1.3.1"

---

## 3. Max Iterations

O design squad opera com um limite rígido de 3 iterações de rework por artefato por gate.

**Fluxo:** Iteração 1 → corrige → revalida. Se reprova → Iteração 2 → corrige → revalida. Se reprova → Iteração 3 → corrige → revalida. Se AINDA reprova → **ESCALAÇÃO OBRIGATÓRIA** para design-chief.

### Escalação pós-3 iterações

Design-chief convoca troubleshooting (agent + reviewer), avalia causa raiz e decide: **reatribuir** (skill gap), **ajustar gate** (critério excessivo), **pair work** (resolver juntos) ou **re-scope** (escopo demais). Decisão registrada em `data/registries/decisions-log.yaml`.

---

## 4. Timeline Expectations

Cada iteração de rework tem prazo proporcional à complexidade do feedback.

### SLAs de Rework

| Volume de itens     | Prazo por iteração | Observação                              |
|--------------------|--------------------|-----------------------------------------|
| 1-3 itens simples  | 4 horas úteis      | Correções pontuais (cor, spacing, copy) |
| 4-8 itens médios   | 1 dia útil         | Ajustes estruturais (layout, fluxo)     |
| 9+ itens ou complexos | 2 dias úteis    | Retrabalho significativo                |

### Regras de Prazo

- O reviewer define o prazo na rework request, respeitando os SLAs acima
- Se o agent não consegue cumprir o prazo, comunica ANTES do vencimento (não depois)
- Atraso sem comunicação prévia conta como trigger de escalação Level 1
- O prazo total das 3 iterações não pode exceder 5 dias úteis para itens simples/médios

---

## 5. Registration

Todo rework DEVE ser registrado. Rework não registrado é rework invisível, e rework invisível não gera aprendizado.

### Onde Registrar

1. **Registry da task afetada** (ex: `data/registries/design-artifact-registry.yaml`, `data/registries/handoff-registry.yaml`)

```yaml
rework_history:
  - iteration: 1
    date: "YYYY-MM-DD"
    gate: "[nome do gate]"
    reviewer: "[agent]"
    items_count: N
    items_summary: "[resumo dos itens]"
    resolved: [true|false]
  - iteration: 2
    ...
```

2. **Métricas operacionais** — O rework contribui para o KPI `rework_rate` conforme config.yaml → kpis → operational. O target é < 10% de rework rate (operating-system.md) e o threshold de alerta de performance de agent é > 15% (config.yaml → score_thresholds → agent_performance).

3. **Lessons learned** — Se o rework revelou um problema sistêmico (ex: checklist desatualizada, briefing ambíguo), registrar em `data/registries/lessons-learned-registry.yaml` para que o kaizen loop processe.

---

## 6. Rework vs. Escalation Decision

- **Iteração 1-3?** → Gerar rework request, agent corrige, reviewer revalida
- **3+ iterações?** → Escalar para design-chief (skill → reatribuir, critério → ajustar, escopo → re-scope, briefing → refazer)
- **Bloqueio externo?** → Escalar conforme escalation-protocol.md
- **Total > 5 dias úteis?** → Escalar como time overrun

## 7. Prevention

| Ação preventiva                    | Responsável    | Frequência               |
|------------------------------------|----------------|--------------------------|
| Revisar checklists por atualização | design-chief   | Mensal (design-ops-sync) |
| Analisar top 3 causas de rework   | design-chief   | Quinzenal                |
| Pair review antes de submeter      | Agent executor | Sempre que possível      |
| Briefing detalhado no início       | Agent que atribui | Toda task             |

---

## Cross-References

- `config.yaml` → seção `quality_gates` — Definição de gates e critérios de aprovação
- `config.yaml` → seção `score_thresholds` — Thresholds de rework (80% mínimo, 95% GOLD, 98% SOTA)
- `checklists/` — Todos os checklists usados nos quality gates
- `agents/design-chief.md` — Autoridade para arbitrar escalações pós-3 iterações
- `docs/escalation-protocol.md` — Protocolo quando rework vira escalação
- `docs/quality-gate-cascade.md` — Detalhamento dos gates que geram rework
- `data/registries/decisions-log.yaml` — Registro de decisões de escalação de rework
- `data/registries/lessons-learned-registry.yaml` — Aprendizados de rework recorrente
