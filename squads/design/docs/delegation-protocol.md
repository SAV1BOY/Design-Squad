# Delegation Protocol

> Protocolo operacional de delegação do Design Squad para squads externos.
> Linguagem mista: headers em English, conteúdo em PT-BR, termos técnicos em English.

---

## 1. When to Delegate

Delegação ocorre quando uma task sai do escopo de competência do design squad OU requer expertise especializada de outro squad. Regra geral: se o design squad não é o melhor executor para a tarefa, delegue.

### Decision Matrix

| Situação                                           | Ação              | Destino            |
|---------------------------------------------------|-------------------|--------------------|
| Task envolve UX writing / microcopy extensivo      | Delegar           | copy_squad         |
| Task envolve criação de identidade visual do zero  | Delegar           | brand_squad        |
| Task requer análise quantitativa de comportamento  | Delegar           | traffic_squad      |
| Task requer narrativa de produto ou case study     | Delegar           | storytelling_squad |
| Task exige implementação frontend                  | Handoff (não delegar) | engineering    |
| Task é de design mas requer skill específica       | Reatribuir internamente | Outro agent do squad |

**IMPORTANTE:** O design squad NUNCA implementa código. Tasks de frontend vão para engineering via dev-handoff, não via delegação.

---

## 2. Delegation Targets — O que cada squad recebe

### copy_squad
- **Recebe do design:** contexto-de-tela, fluxo-do-usuario, wireframe-com-placeholder, tom-de-voz-esperado
- **Retorna ao design:** microcopy-aprovado, tom-de-voz-guidelines, glossário-de-produto
- **Contrato:** `workflows/handoff-contract-copy-squad` (referência em config.yaml → cross_squad)
- **Quality gate on send:** Validar que contexto de tela inclui user flow completo

### brand_squad
- **Recebe do design:** briefing-visual, referências, constraints-de-produto
- **Retorna ao design:** brand-guidelines, paleta-de-cores, tipografia-aprovada, iconografia-base
- **Contrato:** `workflows/handoff-contract-brand-squad`
- **Quality gate on send:** Validar que extensões de paleta mantêm harmonia com brand

### traffic_squad
- **Recebe do design:** hipóteses, métricas-de-interesse, período-de-análise
- **Retorna ao design:** dados-de-comportamento, funis-de-conversão, heatmaps, métricas-de-engajamento
- **Contrato:** `workflows/handoff-contract-traffic-squad`
- **Quality gate on send:** Validar que variantes têm specs completas para implementação

### storytelling_squad
- **Recebe do design:** dados-de-pesquisa, assets-visuais, resultados-de-métricas
- **Retorna ao design:** narrativa-de-produto, scripts-de-onboarding, arcos-de-experiência
- **Contrato:** `workflows/handoff-contract-storytelling-squad`
- **Quality gate on send:** Validar que storyboard segue brand guidelines

### engineering (handoff, não delegação)
- **Recebe:** pacote de handoff completo via task `dev-handoff` (config.yaml routing). Gate: handoff-quality (mandatory, blocking)

---

## 3. Handoff Package — O que incluir

Pacotes incompletos serão rejeitados na quality gate.

| Seção          | O que incluir                                                              |
|---------------|-----------------------------------------------------------------------------|
| **Contexto**   | Objetivo da task, onde se encaixa no fluxo, decisões já tomadas            |
| **Constraints**| Restrições técnicas, de marca (brand guidelines) e a11y (WCAG 2.1 AA min) |
| **Expectations**| Formato do output, critérios de aceitação mensuráveis, quality gate        |
| **Deadline**   | Data de entrega, data crítica, buffer para review (min 1 dia útil)         |
| **Assets**     | Lista de arquivos/links entregues com versão                               |
| **Contato**    | Agent responsável pelo acompanhamento + canal preferido                    |

---

## 4. Quality Gate Before Sending

Antes de enviar qualquer delegação, o agent responsável DEVE passar pelo seguinte checklist:

### Pre-Delegation Checklist

- [ ] Contexto completo e autoexplicativo (alguém de fora entende?)
- [ ] Constraints documentadas (não assumir que o outro squad sabe)
- [ ] Critérios de aceitação específicos e mensuráveis
- [ ] Deadline realista (considerar SLA do squad destino)
- [ ] Assets na versão correta e acessíveis
- [ ] Quality gate on send do config.yaml cross_squad validado
- [ ] Design-chief aprovou (obrigatório quando impacta deadline)

**Quem valida:** Rotineira → agent responsável. Estratégica → design-chief. Urgente → design-chief + PM Lead. Se o pacote falhar, NÃO envie — complete primeiro.

---

## 5. Follow-Up Cadence

Após delegar, o agent responsável mantém ownership do acompanhamento.

### Cadência de Follow-Up

| Prazo da delegação  | Frequência de check-in | Formato                |
|--------------------|------------------------|------------------------|
| ≤ 3 dias úteis     | Diário                 | Mensagem async         |
| 4-7 dias úteis     | A cada 2 dias          | Mensagem async         |
| 8-14 dias úteis    | 2x por semana          | Mensagem async         |
| > 14 dias úteis    | Semanal                | Reunião sync de 15min  |

### Regras de Follow-Up

1. **Primeiro check-in (24h):** Confirmar que o squad destino recebeu e entendeu o pacote
2. **Intermediários:** Perguntar status e blockers — NÃO microgerenciar
3. **Final (1 dia antes do deadline):** Confirmar que entrega está no caminho
4. **Se atraso:** Reportar ao design-chief para renegociação ou escalação

### Quando o Output Retorna

1. Validar contra critérios de aceitação do handoff + quality gate on receive (config.yaml cross_squad)
2. Se aprovado → integrar e registrar. Se reprovado → devolver com feedback específico (itens, não "refazer")

---

## 6. Registration

Toda delegação é registrada no registry da task original E no `data/registries/decisions-log.yaml`:

```yaml
- id: DEL-YYYY-NNN
  date: "YYYY-MM-DD"
  from_squad: design
  to_squad: "[squad destino]"
  agent_responsible: "[agent]"
  task_context: "[task de origem]"
  delegation_reason: "[motivo]"
  deadline: "YYYY-MM-DD"
  status: "[pending | in_progress | delivered | accepted | rejected]"
  quality_gate_result: "[pass | fail]"
  notes: "[observações relevantes]"
```

---

## Cross-References

- `config.yaml` → seção `delegation_rules` — Regras de delegação configuradas
- `config.yaml` → seção `cross_squad` — Contratos e quality gates por squad
- `workflows/handoff-contract-copy-squad` — Contrato com copy squad
- `workflows/handoff-contract-brand-squad` — Contrato com brand squad
- `workflows/handoff-contract-traffic-squad` — Contrato com traffic squad
- `workflows/handoff-contract-storytelling-squad` — Contrato com storytelling squad
- `workflows/cross-squad-narrative-handoff.md` — Workflow de handoff narrativo
- `docs/escalation-protocol.md` — Quando delegação vira escalação (bloqueio > 3 dias)
- `docs/handoff-standards.md` — Padrões gerais de handoff
