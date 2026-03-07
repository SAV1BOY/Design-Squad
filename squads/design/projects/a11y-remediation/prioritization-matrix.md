# Prioritization Matrix Template

## Informacoes

| Campo | Valor |
|-------|-------|
| **Produto** | [Nome] |
| **Responsavel** | [Nome] |
| **Data** | [YYYY-MM-DD] |
| **Total de Issues** | [N] |
| **Baseado em** | [Audit Findings — data] |

## Criterios de Priorizacao

A priorizacao dos issues de acessibilidade considera quatro
dimensoes, cada uma com peso definido.

### Dimensoes e Pesos

| Dimensao | Peso | Descricao |
|----------|------|-----------|
| **Impacto no usuario** | 40% | Quantos usuarios sao afetados e quao severamente |
| **Risco legal** | 25% | Risco de nao-conformidade com legislacao |
| **Esforco de correcao** | 20% | Complexidade tecnica e tempo necessario |
| **Frequencia de uso** | 15% | Quao frequentemente o fluxo afetado e usado |

### Escala de Pontuacao

| Score | Impacto | Risco Legal | Esforco | Frequencia |
|-------|---------|------------|---------|-----------|
| 5 | Bloqueia uso totalmente | Violacao nivel A | Trivial (< 1h) | Core flow (diario) |
| 4 | Impacto severo | Violacao nivel AA critica | Baixo (< 4h) | Frequente (semanal) |
| 3 | Impacto moderado | Violacao nivel AA menor | Medio (1-2 dias) | Regular (mensal) |
| 2 | Impacto leve | Best practice | Alto (3-5 dias) | Ocasional |
| 1 | Impacto minimo | Melhoria opcional | Muito alto (> 1 semana) | Raro |

## Matriz de Priorizacao

### Todos os Issues Priorizados

| ID | Descricao | WCAG | Impacto (40%) | Legal (25%) | Esforco (20%) | Freq (15%) | Score Total | Prioridade |
|----|-----------|------|:---:|:---:|:---:|:---:|:---:|:---:|
| FIND-001 | [descricao] | [criterio] | [1-5] | [1-5] | [1-5] | [1-5] | [calc] | P0 |
| FIND-002 | [descricao] | [criterio] | [1-5] | [1-5] | [1-5] | [1-5] | [calc] | P0 |
| FIND-010 | [descricao] | [criterio] | [1-5] | [1-5] | [1-5] | [1-5] | [calc] | P1 |
| FIND-011 | [descricao] | [criterio] | [1-5] | [1-5] | [1-5] | [1-5] | [calc] | P1 |
| FIND-012 | [descricao] | [criterio] | [1-5] | [1-5] | [1-5] | [1-5] | [calc] | P2 |
| FIND-020 | [descricao] | [criterio] | [1-5] | [1-5] | [1-5] | [1-5] | [calc] | P2 |
| FIND-021 | [descricao] | [criterio] | [1-5] | [1-5] | [1-5] | [1-5] | [calc] | P3 |

### Calculo do Score

```
Score = (Impacto × 0.40) + (Legal × 0.25) + (Esforco_inv × 0.20) + (Freq × 0.15)

Nota: Para Esforco, a escala e invertida (5 = facil, 1 = dificil)
para que issues faceis de corrigir tenham score maior.
```

### Classificacao de Prioridade

| Prioridade | Score Range | Timeline | Descricao |
|-----------|-----------|----------|-----------|
| **P0** | 4.0 - 5.0 | Sprint atual | Bloqueante — corrigir imediatamente |
| **P1** | 3.0 - 3.9 | Proximo sprint | Alta prioridade — planejar para breve |
| **P2** | 2.0 - 2.9 | Proximo quarter | Media prioridade — incluir no roadmap |
| **P3** | 1.0 - 1.9 | Backlog | Baixa prioridade — corrigir quando possivel |

## Visualizacao: Impacto vs. Esforco

```
Alto Impacto │ ★ Quick Wins   │ ★★ Strategic
             │ (P0 — fazer    │ (P1 — planejar
             │  agora)        │  cuidadosamente)
─────────────┼────────────────┼──────────────
Baixo Impacto│ Fill-ins       │ Deprioritize
             │ (P2 — se       │ (P3 — backlog)
             │  sobrar tempo) │
─────────────┴────────────────┴──────────────
              Baixo Esforco    Alto Esforco
```

## Agrupamento por Prioridade

### P0 — Corrigir Imediatamente

| ID | Descricao | WCAG | Esforco | Responsavel |
|----|-----------|------|---------|-------------|
| [id] | [descricao] | [criterio] | [estimativa] | [nome] |
| [id] | [descricao] | [criterio] | [estimativa] | [nome] |

**Esforco total estimado**: [horas/dias]
**Sprint alvo**: [Sprint N]

### P1 — Alta Prioridade

| ID | Descricao | WCAG | Esforco | Responsavel |
|----|-----------|------|---------|-------------|
| [id] | [descricao] | [criterio] | [estimativa] | [nome] |
| [id] | [descricao] | [criterio] | [estimativa] | [nome] |

**Esforco total estimado**: [horas/dias]
**Sprint alvo**: [Sprint N+1]

### P2 — Media Prioridade

| ID | Descricao | WCAG | Esforco |
|----|-----------|------|---------|
| [id] | [descricao] | [criterio] | [estimativa] |
| [id] | [descricao] | [criterio] | [estimativa] |

**Esforco total estimado**: [horas/dias]

### P3 — Backlog

| ID | Descricao | WCAG | Esforco |
|----|-----------|------|---------|
| [id] | [descricao] | [criterio] | [estimativa] |

---
