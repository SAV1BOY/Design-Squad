# Design Squad

## What is this

O Design Squad e o nucleo de design da organizacao. Ele cobre todas as disciplinas
de produto digital — discovery, UX research, UI design, design system, prototyping,
handoff para engenharia, QA visual e governanca de design.

Toda task e roteada pelo `config.yaml`, que mapeia automaticamente os agents,
frameworks, checklists, templates e registries necessarios para cada entrega.

---

## Quick Start

1. **Leia o `config.yaml`** — entenda quais tasks existem e como sao roteadas.
2. **Identifique a task** — encontre a tarefa que corresponde ao seu objetivo.
3. **Execute** — o roteador seleciona agents e frameworks; siga os checklists.
4. **Registre** — ao concluir, o output e persistido em `data/registries/` e `data/metrics/`.

---

## Structure

```
squads/design/
  ARCHITECTURE.md          # Documento de arquitetura completo
  README.md                # Este arquivo — visao geral do squad
  config.yaml              # Cerebro de roteamento (tasks -> agents -> frameworks)
  swipe.config             # Fontes de referencia e regras de curacao
  agents/                  # Definicoes de cada agent do squad
    brad-frost.md
    dan-mall.md
    dave-malouf.md
    design-chief.md
    ux-design-expert.md
    jessica-ux-ui.md
    design-system-architect.md
    nano-banana-generator.md
  frameworks/              # Frameworks metodologicos por disciplina
  checklists/              # Checklists de qualidade por task
  templates/               # Templates de output por entrega
  data/
    registries/            # Registros permanentes de entregas
    metrics/               # KPIs e metricas operacionais
```

---

## Agents

| Agent | Tipo | Descricao |
|-------|------|-----------|
| `design-chief` | Functional | Lider do squad; orquestra tasks e faz routing |
| `ux-design-expert` | Functional | Pesquisa, fluxos, IA e testes de usabilidade |
| `jessica-ux-ui` | Functional | Designer generalista UX/UI |
| `design-system-architect` | Functional | Tokens, componentes e biblioteca do DS |
| `nano-banana-generator` | Functional | Exploracoes visuais rapidas e swipe files |
| `brad-frost` | Core Expert | Atomic Design, arquitetura de componentes |
| `dan-mall` | Core Expert | Design strategy e design ops |
| `dave-malouf` | Core Expert | UX management e design leadership |

---

## How Routing Works

O `config.yaml` funciona como um roteador declarativo. Exemplo:

```yaml
wireframe-pack:
  agents: [jessica-ux-ui, ux-design-expert]
  frameworks: [ux-flow-framework]
  checklists: [wireframe-checklist]
  templates: [wireframe-pack-template]
  registry: [design-artifact-registry]
```

Quando a task `wireframe-pack` e acionada:

1. Os agents `jessica-ux-ui` e `ux-design-expert` sao convocados.
2. O `ux-flow-framework` guia a metodologia de trabalho.
3. O `wireframe-checklist` valida a qualidade antes da entrega.
4. O `wireframe-pack-template` estrutura o output final.
5. O resultado e registrado em `design-artifact-registry`.

---

## Cross-Squad Integration

O Design Squad integra bidireccionalmente com outros squads:

- **Copy Squad** — microcopy, UX writing, tom de voz.
- **Brand Squad** — guidelines de marca, paleta, tipografia.
- **Traffic Squad** — dados de comportamento, funnels, heatmaps.
- **Storytelling Squad** — narrativas de produto, onboarding, case studies.

Consulte a secao `cross_squad` do `config.yaml` para detalhes de handoff.

---

## Principles

| # | Principle | Significado |
|---|-----------|-------------|
| 1 | `evidence_over_opinion` | Dados e pesquisa acima de preferencia pessoal |
| 2 | `system_first` | Componentes reutilizaveis antes de solucoes avulsas |
| 3 | `accessibility_by_default` | Acessibilidade e requisito, nao feature |
| 4 | `ship_learn_iterate` | Entregar, aprender com usuarios reais, iterar |
| 5 | `docs_as_truth` | Se nao esta documentado, nao existe |

---

*Ultima atualizacao: 2026-03-06*
