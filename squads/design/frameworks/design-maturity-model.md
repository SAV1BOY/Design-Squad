# Design Maturity Model

## Metadata

| Campo         | Valor                                          |
| ------------- | ---------------------------------------------- |
| Categoria     | Estrategia                                     |
| Complexidade  | Alta                                           |
| Autor         | Design Squad                                   |
| Versao        | 1.0                                            |
| Ultima revisao| 2026-03-06                                     |
| Tags          | maturity, organization, design-ops, strategy   |

## Concept

O Design Maturity Model e um framework para avaliar e desenvolver a capacidade de design de
uma organizacao ao longo de 5 niveis progressivos. Cada nivel representa um conjunto de
praticas, processos e mindsets que indicam quao integrado e estrategico o design e dentro
da empresa.

### Os 5 Niveis

```
Nivel 5: Design-Driven   ████████████████████  Design como diferencial estrategico
Nivel 4: Integrado        ████████████████      Design integrado em toda decisao de produto
Nivel 3: Sistematico      ████████████          Processos, design system, metricas
Nivel 2: Funcional        ████████              Design existe mas e reativo
Nivel 1: Inicial          ████                  Design ad-hoc, sem processo
```

### Dimensoes de Avaliacao

O modelo avalia maturidade em 6 dimensoes:

1. **Processo**: como o trabalho de design e estruturado e executado.
2. **Pessoas**: tamanho, skill e autonomia do time de design.
3. **Ferramentas**: design system, tooling, infraestrutura.
4. **Cultura**: como a organizacao percebe e valoriza design.
5. **Pesquisa**: presenca e impacto de user research.
6. **Metricas**: como design e medido e accountable.

## When to Use

- Para diagnosticar o estado atual da pratica de design na organizacao.
- Para criar um roadmap de evolucao com metas e milestones concretos.
- Para comunicar com lideranca sobre investimento necessario em design.
- Para benchmark contra organizacoes similares do setor.
- Em planejamento estrategico anual do time de design.

## How to Apply

### 1. Assessment por Dimensao

Para cada dimensao, identificar o nivel atual com base nos criterios abaixo.

**Nivel 1 — Inicial**

| Dimensao  | Caracteristicas                                    |
| --------- | -------------------------------------------------- |
| Processo  | Sem processo definido; design feito por devs ou PMs|
| Pessoas   | 0-1 designers; sem career ladder                   |
| Ferramentas| Sem design system; ferramentas ad-hoc              |
| Cultura   | "Design e deixar bonito"; nao participa de decisoes|
| Pesquisa  | Nenhuma pesquisa com usuarios                      |
| Metricas  | Design nao e medido                                |

**Nivel 2 — Funcional**

| Dimensao  | Caracteristicas                                    |
| --------- | -------------------------------------------------- |
| Processo  | Design como etapa do pipeline; handoff manual      |
| Pessoas   | Designers dedicados; sem especializacao             |
| Ferramentas| Biblioteca de componentes basica, inconsistente    |
| Cultura   | Design e respeitado mas consultado tarde           |
| Pesquisa  | Testes de usabilidade esporadicos                  |
| Metricas  | Satisfacao do usuario medida ocasionalmente        |

**Nivel 3 — Sistematico**

| Dimensao  | Caracteristicas                                    |
| --------- | -------------------------------------------------- |
| Processo  | Rituais definidos (critique, review); design ops   |
| Pessoas   | Especializacoes (UI, UX, research); career ladder  |
| Ferramentas| Design system documentado e versionado             |
| Cultura   | Design participa de discovery e planning           |
| Pesquisa  | Research continuo; insights compartilhados         |
| Metricas  | UX metrics no dashboard do produto (SUS, NPS, CSAT)|

**Nivel 4 — Integrado**

| Dimensao  | Caracteristicas                                    |
| --------- | -------------------------------------------------- |
| Processo  | Design embedded em squads; co-criacao com eng/PM   |
| Pessoas   | Ratio designer:dev saudavel (1:5-8); IC senior+    |
| Ferramentas| Design system como produto com roadmap proprio     |
| Cultura   | Designers em decisoes estrategicas de produto      |
| Pesquisa  | Research informa roadmap e estrategia              |
| Metricas  | Design KPIs ligados a outcomes de negocio          |

**Nivel 5 — Design-Driven**

| Dimensao  | Caracteristicas                                    |
| --------- | -------------------------------------------------- |
| Processo  | Design thinking em toda a organizacao              |
| Pessoas   | CDO/VP Design no C-level; design como competencia org|
| Ferramentas| Design system referencia no mercado                |
| Cultura   | Design e diferencial competitivo reconhecido       |
| Pesquisa  | Research generativo influencia estrategia de negocio|
| Metricas  | ROI de design medido e comunicado para board       |

### 2. Gap Analysis e Roadmap

Para cada dimensao: identificar nivel atual, nivel alvo (proximo, nao pular), gap, timeline e investimento.

Regra: subir um nivel por vez. Q1: consolidar atual. Q2: pilotar proximo nivel com 1 squad.
Q3: escalar para todas as squads. Q4: re-assessment para proximo ciclo.

## Key Principles

- **Honestidade no assessment**: avaliar onde esta, nao onde gostaria de estar.
- **Progressao incremental**: um nivel por vez, consolidando antes de avancar.
- **Contexto importa**: nem toda organizacao precisa ser nivel 5.
- **Equilíbrio entre dimensoes**: subir todas juntas, nao apenas uma.
- **Evidencias, nao percepcoes**: basear assessment em praticas observaveis.
- **Lideranca buy-in**: evolucao de maturidade requer investimento organizacional.

## Examples

### Assessment de uma Startup (Serie A)

```
Processo:    Nivel 2 (design no pipeline, handoff basico)
Pessoas:     Nivel 2 (2 designers generalistas)
Ferramentas: Nivel 1 (sem design system, Figma desorganizado)
Cultura:     Nivel 3 (founders valorizam design, envolvem cedo)
Pesquisa:    Nivel 1 (nenhuma pesquisa formal)
Metricas:    Nivel 1 (sem metricas de UX)

Media: 1.7 — Foco: elevar Ferramentas e Pesquisa para Nivel 2
```

### Roadmap 12 Meses (Nivel 2 -> 3)

```
Q1: Criar design system basico (tokens + 10 componentes core)
Q2: Estabelecer rituais (critique semanal, review de handoff)
Q3: Contratar UX researcher; iniciar testes quinzenais
Q4: Implementar UX metrics (SUS trimestral, task success rate)
```

## Common Pitfalls

| Erro                               | Consequencia                        | Correcao                                |
| ---------------------------------- | ----------------------------------- | --------------------------------------- |
| Autoavaliacao generosa              | Plano de acao inadequado            | Usar evidencias observaveis, nao percepcoes|
| Tentar pular niveis               | Praticas avancadas sem fundacao     | Consolidar nivel atual antes de avancar |
| Focar so em ferramentas            | Design system sem cultura ou pesquisa| Evoluir todas as dimensoes em paralelo  |
| Nao envolver lideranca             | Sem budget nem suporte              | Apresentar business case com ROI        |
| Assessment unico sem follow-up     | Diagnostico sem tratamento          | Re-assessment trimestral                |
| Comparar com empresas de outro porte| Expectativas irrealistas            | Benchmark com organizacoes similares    |

## Cross-References

- [Design System Governance](./design-system-governance.md) — governanca como pratica de nivel 3+.
- [Design Review and Critique](./design-review-and-critique.md) — rituais como indicador de nivel 3.
- [Lean UX Framework](./lean-ux-framework.md) — Lean UX como pratica de nivel 4+.
- [SUS System Usability Scale](./sus-system-usability-scale.md) — metricas como indicador de nivel 3.
- [Sprint Design Framework](./sprint-design-framework.md) — design sprints como pratica de nivel 3.
