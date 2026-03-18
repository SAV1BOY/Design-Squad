# Design Squad — Architecture

> Documento de arquitetura do Design Squad.
> Linguagem mista: estrutura em English, conteudo descritivo em PT-BR, termos tecnicos em English.

---

## 1. System Diagram

```
                         config.yaml
                             |
                             v
                    +--------+--------+
                    |      TASKS      |
                    +--------+--------+
                             |
                             v
                    +--------+--------+
                    |     AGENTS      |
                    +--------+--------+
                             |
                             v
                    +--------+--------+
                    |    WORKFLOWS    |
                    +--------+--------+
                             |
                             v
                    +--------+--------+
                    |   FRAMEWORKS    |
                    +--------+--------+
                             |
                             v
                    +--------+--------+
                    |   CHECKLISTS    |
                    +--------+--------+
                             |
                             v
                    +--------+--------+
                    |    TEMPLATES    |
                    +--------+--------+
                             |
                             v
              +--------------+--------------+
              |                             |
     +--------+--------+          +--------+--------+
     |  DATA/REGISTRIES |          |   DATA/METRICS  |
     +-----------------+          +-----------------+
```

Cada tarefa registrada no `config.yaml` aciona uma cadeia deterministica:
o roteador identifica a task, seleciona agents, aplica frameworks,
valida checklists, preenche templates e persiste resultados em registries/metrics.

---

## 2. Core Flow

```
Discovery -> Strategy -> UX -> UI -> Design System -> Prototyping -> Handoff -> QA -> Release -> Measure -> Iterate
```

O fluxo e ciclico. Apos "Iterate", o ciclo retorna a qualquer etapa anterior
conforme evidencias coletadas na fase de Measure.

---

## 3. Dependency Chain

```
Task -> Agents -> Frameworks -> Checklists -> Templates -> data/registries/ -> data/metrics/
```

Nenhuma camada pode ser executada sem que a anterior esteja resolvida.
Se um agent nao possui framework associado, o roteador levanta erro antes da execucao.

---

## 4. 9-Layer Architecture

| Layer | Descricao | Framework Reference |
|-------|-----------|---------------------|
| 1. Discovery | Pesquisa exploratoria, entrevistas, benchmarks | `frameworks/discovery-layer` |
| 2. Strategy | Definicao de problema, personas, JTBD | `frameworks/strategy-layer` |
| 3. UX Design | Fluxos, IA, wireframes, prototipos lo-fi | `frameworks/ux-layer` |
| 4. UI Design | Visual design, high-fidelity, motion specs | `frameworks/ui-layer` |
| 5. Design System | Tokens, componentes, biblioteca, documentacao | `frameworks/design-system-layer` |
| 6. Prototyping | Prototipos interativos, testes de usabilidade | `frameworks/prototyping-layer` |
| 7. Handoff | Entrega para engenharia, specs, assets | `frameworks/handoff-layer` |
| 8. QA | Revisao visual, acessibilidade, consistencia | `frameworks/qa-review-framework` |
| 9. Governance | Metricas, debt tracking, decisoes arquiteturais | `frameworks/governance-layer` |

---

## 5. Agent Architecture

### 5.1 Core Experts (3)

Agentes baseados em especialistas reconhecidos do mercado de design:

| Agent | Especialidade | Papel |
|-------|--------------|-------|
| `brad-frost` | Design Systems, Atomic Design | Consultor de arquitetura de componentes e tokens |
| `dan-mall` | Design Strategy, Design Ops | Consultor de estrategia, processos e colaboracao |
| `dave-malouf` | UX Management, Design Leadership | Consultor de gestao, cultura e maturidade de design |

### 5.2 Functional Agents (5)

Agentes operacionais que executam tarefas do dia a dia:

| Agent | Funcao |
|-------|--------|
| `design-chief` | Lider do squad, orquestra tasks, faz routing e code review de design |
| `ux-design-expert` | Especialista em pesquisa, fluxos, IA e testes de usabilidade |
| `jessica-ux-ui` | Designer generalista UX/UI, wireframes e high-fidelity |
| `design-system-architect` | Mantem tokens, componentes, biblioteca e documentacao do DS |
| `nano-banana-generator` | Gera variacoes rapidas, exploracoes visuais e swipe files |

---

## 6. Agent Collaboration Model

```
                    +------------------+
                    |   design-chief   |
                    +--------+---------+
                             |
            +----------------+----------------+
            |                |                |
     +------+------+  +-----+------+  +------+------+
     | ux-design-  |  | jessica-   |  | design-     |
     | expert      |  | ux-ui      |  | system-arch |
     +------+------+  +-----+------+  +------+------+
            |                |                |
            +-------+--------+--------+-------+
                    |                 |
             +------+------+   +-----+-------+
             | nano-banana |   | Core Experts|
             | generator   |   | (advisory)  |
             +-------------+   +-------------+
```

O `design-chief` distribui tasks. Agents funcionais executam.
Core experts sao acionados sob demanda para consultoria especializada.
O `nano-banana-generator` atua como agente auxiliar de qualquer outro.

---

## 7. Cross-Squad Integration

```
+----------------+       +----------------+
|   Copy Squad   | <---> | Design Squad   |
+----------------+       +-------+--------+
                                 |
+----------------+       +-------+--------+
|  Brand Squad   | <---> | Design Squad   |
+----------------+       +-------+--------+
                                 |
+----------------+       +-------+--------+
| Traffic Squad  | <---> | Design Squad   |
+----------------+       +-------+--------+
                                 |
+----------------+       +-------+--------+
|Storytelling Sq | <---> | Design Squad   |
+----------------+       +----------------+
```

Todas as integracoes sao **bidirecionais**:

- **Copy Squad**: microcopy, UX writing, tom de voz em interfaces.
- **Brand Squad**: brand guidelines, paleta, tipografia, identidade visual.
- **Traffic Squad**: dados de comportamento, funnels, heatmaps, analytics.
- **Storytelling Squad**: narrativas de produto, onboarding flows, case studies.

---

## 8. Quality Gates

### 8.1 Mandatory Gates

| Gate | Descricao |
|------|-----------|
| `discovery-brief-quality` | Todo projeto deve ter brief validado antes de avancar |
| `accessibility-quality` | WCAG 2.1 AA minimo; violacoes criticas bloqueiam release |
| `handoff-quality` | Specs completas, tokens mapeados, assets exportados |

### 8.2 Per-Domain Gates

Gates adicionais sao aplicados conforme o dominio da task:
design-system tasks exigem `component-spec-quality`;
prototyping tasks exigem `usability-test-quality`;
governance tasks exigem `metrics-review-quality`.

---

## 9. Kaizen Loop

```
Create -> Test -> Analyze -> Learn -> Adjust -> Repeat
   ^                                              |
   +----------------------------------------------+
```

Melhoria continua e parte do DNA do squad. Cada ciclo gera registros
em `data/metrics/` que alimentam decisoes do proximo ciclo.

---

## 10. Design Principles

| # | Principle | Descricao |
|---|-----------|-----------|
| 1 | `evidence_over_opinion` | Decisoes baseadas em dados e pesquisa, nao em preferencia pessoal |
| 2 | `system_first` | Componentes reutilizaveis antes de solucoes pontuais |
| 3 | `accessibility_by_default` | Acessibilidade nao e feature, e requisito desde o dia zero |
| 4 | `ship_learn_iterate` | Entregar rapido, aprender com usuarios reais, iterar com evidencia |
| 5 | `docs_as_truth` | Documentacao e a fonte de verdade; se nao esta documentado, nao existe |

---

## 11. Data Flow

```
[User Request]
      |
      v
[config.yaml router] --> seleciona task
      |
      v
[Agent(s)] --> aplica framework(s)
      |
      v
[Checklist validation] --> preenche template(s)
      |
      v
[Output artifacts]
      |
      +---> data/registries/  (registro permanente)
      +---> data/metrics/     (metricas e KPIs)
      +---> templates/        (artefatos gerados)
```

---

## 12. File Naming Conventions

| Regra | Exemplo |
|-------|---------|
| Kebab-case para todos os arquivos | `design-system-bootstrap.md` |
| Prefixo de autor para agents | `brad-frost.md`, `dan-mall.md` |
| Sufixo `-framework` para frameworks | `ux-flow-framework.md` |
| Sufixo `-checklist` para checklists | `handoff-checklist.md` |
| Sufixo `-template` para templates | `component-spec-template.md` |
| Sufixo `-registry` para registries | `component-registry.yaml` |

---

## 13. Technology Stack

| Ferramenta | Categoria | Uso |
|------------|-----------|-----|
| Figma | Design Tool | UI design, prototyping, componentes |
| Storybook | Component Dev | Documentacao e preview de componentes |
| Style Dictionary | Token Management | Geracao de design tokens multiplataforma |
| axe | Accessibility | Auditoria automatizada de acessibilidade |
| Maze | User Testing | Testes de usabilidade remotos e nao-moderados |
| Chromatic | Visual Regression | Testes de regressao visual automatizados |
| Zeroheight | Documentation | Documentacao publica do design system |
| GitHub | Version Control | Versionamento de assets, tokens e specs |
| Lottie | Animation | Exportacao e integracao de motion specs |
| Contrast | Color A11y | Verificacao de contraste de cores |

---

## 14. Memory Model & Learning

O squad possui um sistema de memoria operacional em multiplas camadas:

```
[Execucao de Task]
        |
        v
[data/registries/] --- registro permanente de artefatos, decisoes, insights
        |
        v
[data/metrics/] --- KPIs e metricas quantitativas
        |
        v
[data/learnings/] --- lessons learned e patterns identificados
        |
        v
[data/scorecards/] --- avaliacao periodica de performance
        |
        v
[Kaizen Loop] --- alimenta proximas decisoes e prioridades
```

### Como o squad aprende:

1. **Post-execution capture** — Toda task concluida gera entrada no registry correspondente.
2. **Lessons learned** — Quando algo falha ou supera expectativas, registra-se em `data/learnings/learning-log.yaml`.
3. **Quarterly review** — A cada trimestre, o squad revisa registries + metrics para identificar patterns.
4. **Kaizen loop** — Insights da review alimentam ajustes em frameworks, checklists e processos.
5. **Decision traceability** — Toda decisao significativa e registrada em `data/registries/decisions-log.yaml` com contexto, alternativas e racional.

### Principio de memoria:

> Se uma decisao, insight ou aprendizado nao esta registrado, ele nao existe para o sistema.
> O squad opera com memoria explicita, nunca implicita.

---

## 15. Escalation & Delegation Protocol

### Escalation dentro do squad:

| Trigger | Acao | Responsavel |
|---------|------|-------------|
| Agent nao resolve task em 2x tempo estimado | Reavaliacao de escopo ou reassignment | design-chief |
| Dois agents discordam sobre abordagem | Arbitragem baseada em evidencias | design-chief |
| Quality gate reprova 3x consecutivas | Sessao de troubleshooting | design-chief + agent + reviewer |
| Bloqueio por dependencia externa | Comunicacao formal ao squad bloqueador | design-chief |

### Escalation cross-squad:

| Trigger | Acao | Responsavel |
|---------|------|-------------|
| Dependencia bloqueia task > 3 dias uteis | Escalar para PM Lead | design-chief |
| Output recebido nao atende quality gate | Devolver com feedback + sessao de alinhamento | design-chief |
| Conflito de prioridade entre squads > 5 dias | Escalar para HRM Chief / Central Command | design-chief |

### Delegation:

O design squad delega quando a task sai do seu escopo:
- **Copy/microcopy extensivo** → Copy Squad
- **Identidade visual from scratch** → Brand Squad
- **Analise quantitativa de comportamento** → Traffic Squad
- **Narrativa de produto / case study** → Storytelling Squad
- **Implementacao frontend** → NUNCA delega; faz handoff para Engineering

Protocolo completo em `docs/escalation-protocol.md` e `docs/delegation-protocol.md`.

---

## 16. Rework Loop Protocol

Quando um quality gate reprova um entregavel:

```
[Output do Agent]
        |
        v
[Quality Gate Check]
        |
   PASS?--YES--> [Proximo step / Handoff]
        |
       NO
        |
        v
[Feedback especifico gerado]
        |
        v
[Retorno ao Agent responsavel]
        |
        v
[Agent corrige com base no feedback]
        |
        v
[Re-submissao ao Quality Gate]
        |
   PASS?--YES--> [Proximo step]
        |
       NO (3a vez)
        |
        v
[Escalation para design-chief]
        |
        v
[Troubleshooting session]
```

### Regras do rework loop:

1. **Feedback especifico** — Gate nunca diz apenas "reprovado". Sempre lista itens faltantes e criterios nao atendidos.
2. **Max 3 iteracoes** — Se falha 3x, escala para design-chief.
3. **Prazo de correcao** — Agent recebe prazo proporcional a complexidade da correcao.
4. **Registro** — Toda reprovacao e registrada em `data/registries/` com motivo e resolucao.
5. **No punishment** — Rework e oportunidade de melhoria, nao punicao.

Protocolo completo em `docs/rework-loop-protocol.md`.

---

## 17. Ambiguity Resolution Protocol

Quando uma task e ambigua ou tem requisitos conflitantes:

| Tipo de Ambiguidade | Resolucao |
|---------------------|-----------|
| Escopo nao claro | Agent solicita clarificacao ao design-chief antes de iniciar |
| Requisitos conflitantes | Design-chief convoca alinhamento com stakeholders |
| Sem dados para decisao | Agent propoe 2-3 opcoes com trade-offs documentados |
| Dominio incerto (UX vs UI vs DS) | Design-chief decide routing com base na natureza primaria da task |
| Task fora do escopo do squad | Design-chief avalia delegation para squad adequado |

### Principio:

> Ambiguidade nao e desculpa para inacao. Quando ha duvida, o agent deve
> (1) documentar a ambiguidade, (2) propor opcoes, (3) solicitar decisao.
> Nunca assumir silenciosamente.

---

## 18. HRM Integration

O Design Squad opera como um setor dentro de um sistema HRM (Hierarchical Role Modeling) multi-camadas:

```
+----------------------------------+
|      HRM Chief / Central Cmd     |  <- Nivel 0: Governanca do sistema
+----------------------------------+
                |
+----------------------------------+
|         Squad Chiefs             |  <- Nivel 1: Orquestracao local
|  (design-chief, copy-chief...)   |
+----------------------------------+
                |
+----------------------------------+
|    Functional Teams / Swarms     |  <- Nivel 2: Coordenacao de dominio
|  (research_team, ui_team, etc.)  |
+----------------------------------+
                |
+----------------------------------+
|      Individual Agents           |  <- Nivel 3: Execucao
|  (jessica-ux-ui, brad-frost...)  |
+----------------------------------+
```

### Como o squad se conecta ao sistema:

1. **Reporting** — Design-chief reporta metricas e status ao HRM Layer via scorecards trimestrais.
2. **Escalation** — Conflitos nao resolvidos no nivel do squad sobem para HRM Chief.
3. **Cross-squad coordination** — Handoffs entre squads seguem contratos formais em `workflows/handoff-contract-*.md`.
4. **Resource allocation** — HRM Layer pode realocar agents entre squads em caso de sobrecarga.
5. **Quality standards** — GOLD/SOTA thresholds sao definidos pelo HRM Layer e aplicados localmente.

---

## 19. Quality Gate Cascade

Os quality gates operam em cascata, do mais granular ao mais geral:

```
[Agent Gate]
    |
    v
[Inter-Agent Transition Gate]
    |
    v
[Domain Gate]
    |
    v
[Mandatory Gate]
    |
    v
[Chief Approval]
    |
    v
[Cross-Squad Handoff Gate]
    |
    v
[HRM Layer Review] (se aplicavel)
```

### Logica de cada nivel:

| Nivel | Quem aplica | Pode ser overridado? | Consequencia de falha |
|-------|------------|---------------------|----------------------|
| Agent Gate | O proprio agent | Sim, pelo reviewer | Rework pelo agent |
| Inter-Agent Transition | Agent receptor | Sim, pelo design-chief | Retorno ao agent anterior |
| Domain Gate | Especialista do dominio | Sim, pelo design-chief com justificativa | Rework pelo time do dominio |
| Mandatory Gate | design-chief | **NAO** | Bloqueio total ate resolucao |
| Chief Approval | design-chief | Apenas pelo HRM Layer | Rework do squad inteiro se necessario |
| Cross-Squad Gate | Squad receptor | Nao (devolve ao squad emissor) | Refazer handoff |

### Override rules:

- Gates **mandatory** NUNCA podem ser overridados por ninguem dentro do squad.
- Gates **per_domain** podem ser overridados pelo design-chief com justificativa documentada em `data/registries/decisions-log.yaml`.
- Gates **inter_agent** podem ser flexibilizados em contexto de prototipacao rapida, desde que registrado.

Detalhamento completo em `docs/quality-gate-cascade.md`.

---

*Ultima atualizacao: 2026-03-18*
