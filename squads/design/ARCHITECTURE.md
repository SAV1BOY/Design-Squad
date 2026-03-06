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
| 1. Discovery | Pesquisa exploratoria, entrevistas, benchmarks | `discovery-brief-framework` |
| 2. Strategy | Definicao de problema, personas, JTBD | `strategy-canvas-framework` |
| 3. UX Design | Fluxos, IA, wireframes, prototipos lo-fi | `ux-flow-framework` |
| 4. UI Design | Visual design, high-fidelity, motion specs | `ui-visual-framework` |
| 5. Design System | Tokens, componentes, biblioteca, documentacao | `design-system-framework` |
| 6. Prototyping | Prototipos interativos, testes de usabilidade | `prototyping-test-framework` |
| 7. Handoff | Entrega para engenharia, specs, assets | `handoff-spec-framework` |
| 8. QA | Revisao visual, acessibilidade, consistencia | `qa-review-framework` |
| 9. Governance | Metricas, debt tracking, decisoes arquiteturais | `governance-ops-framework` |

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

*Ultima atualizacao: 2026-03-06*
