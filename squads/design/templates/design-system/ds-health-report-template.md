# Design System Health Report Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Design System**    | [PREENCHER — nome do DS]                       |
| **Periodo**          | [PREENCHER — ex.: Q1 2026]                     |
| **Autor(a)**         | [PREENCHER — DS lead ou analista]              |
| **Data do report**   | [PREENCHER — YYYY-MM-DD]                       |
| **Versao atual DS**  | [PREENCHER — ex.: v3.4.2]                      |
| **Status**           | [PREENCHER — Draft / Publicado]                |

## Instructions (Como Usar)

1. Colete metricas ao final de cada quarter (ou periodo definido).
2. Compare com periodos anteriores para identificar tendencias.
3. Use como base para priorizar o roadmap do DS.
4. Compartilhe com stakeholders para demonstrar valor e pedir recursos.
5. Aja sobre os problemas identificados — o report so tem valor se gerar acao.

> **Dica:** Automatize a coleta de metricas sempre que possivel para reduzir esforco e aumentar frequencia.

## Template

### 1. Resumo Executivo

[PREENCHER — em 3-5 frases, resuma o estado de saude do DS neste periodo. Destaque wins e areas de preocupacao.]

**Health Score geral:** [PREENCHER — ex.: 7.2/10]

### 2. Metricas de Adocao

| Metrica                           | Periodo anterior | Periodo atual | Tendencia      |
|-----------------------------------|------------------|---------------|----------------|
| % componentes DS em producao      | [PREENCHER]      | [PREENCHER]   | [PREENCHER — up/down/stable] |
| Squads usando DS                  | [PREENCHER]      | [PREENCHER]   | [PREENCHER]    |
| Componentes custom (fora do DS)   | [PREENCHER]      | [PREENCHER]   | [PREENCHER]    |
| % tokens DS vs. hardcoded         | [PREENCHER]      | [PREENCHER]   | [PREENCHER]    |
| Figma library adocao              | [PREENCHER]      | [PREENCHER]   | [PREENCHER]    |

### 3. Metricas de Qualidade

| Metrica                           | Valor            | Meta           | Status         |
|-----------------------------------|------------------|----------------|----------------|
| Bugs reportados (periodo)         | [PREENCHER]      | [PREENCHER]    | [PREENCHER]    |
| Bugs resolvidos (periodo)         | [PREENCHER]      | [PREENCHER]    | [PREENCHER]    |
| Tempo medio de resolucao de bug   | [PREENCHER]      | [PREENCHER]    | [PREENCHER]    |
| A11y issues abertos               | [PREENCHER]      | [PREENCHER]    | [PREENCHER]    |
| Visual regression incidents       | [PREENCHER]      | [PREENCHER]    | [PREENCHER]    |
| Test coverage %                   | [PREENCHER]      | [PREENCHER]    | [PREENCHER]    |

### 4. Metricas de Atividade

| Metrica                           | Valor            |
|-----------------------------------|------------------|
| Releases no periodo               | [PREENCHER]      |
| Componentes adicionados           | [PREENCHER]      |
| Componentes atualizados           | [PREENCHER]      |
| Componentes deprecados            | [PREENCHER]      |
| PRs de contribuicao externa       | [PREENCHER]      |
| Requests recebidos                | [PREENCHER]      |
| Requests atendidos                | [PREENCHER]      |

### 5. Satisfacao dos Consumidores

**NPS / Satisfaction Score:** [PREENCHER — score]

**Feedback qualitativo:**

| Fonte          | Feedback                               | Sentimento        |
|----------------|----------------------------------------|-------------------|
| [PREENCHER]    | _"[PREENCHER — quote]"_               | Positivo / Negativo |
| [PREENCHER]    | _"[PREENCHER — quote]"_               | Positivo / Negativo |
| [PREENCHER]    | _"[PREENCHER — quote]"_               | Positivo / Negativo |

**Top 3 elogios:**
1. [PREENCHER]
2. [PREENCHER]
3. [PREENCHER]

**Top 3 reclamacoes:**
1. [PREENCHER]
2. [PREENCHER]
3. [PREENCHER]

### 6. Cobertura de Componentes

| Categoria         | Componentes no DS | Componentes custom detectados | Gap   |
|-------------------|-------------------|-------------------------------|-------|
| Navigation        | [PREENCHER]       | [PREENCHER]                   | [PREENCHER] |
| Forms             | [PREENCHER]       | [PREENCHER]                   | [PREENCHER] |
| Data display      | [PREENCHER]       | [PREENCHER]                   | [PREENCHER] |
| Feedback          | [PREENCHER]       | [PREENCHER]                   | [PREENCHER] |
| Layout            | [PREENCHER]       | [PREENCHER]                   | [PREENCHER] |
| [PREENCHER]       | [PREENCHER]       | [PREENCHER]                   | [PREENCHER] |

### 7. Performance e Bundle

| Metrica                    | Valor atual      | Meta             | Status         |
|----------------------------|------------------|------------------|----------------|
| Bundle size total          | [PREENCHER]      | [PREENCHER]      | [PREENCHER]    |
| Tree-shaking funcional     | [PREENCHER]      | Sim              | [PREENCHER]    |
| Tempo de build             | [PREENCHER]      | [PREENCHER]      | [PREENCHER]    |
| Lighthouse perf score      | [PREENCHER]      | [PREENCHER]      | [PREENCHER]    |

### 8. Acessibilidade

| Metrica                         | Valor            | Meta             |
|---------------------------------|------------------|------------------|
| Componentes com a11y completo   | [PREENCHER — %]  | [PREENCHER]      |
| WCAG AA compliance              | [PREENCHER — %]  | 100%             |
| Keyboard navigable              | [PREENCHER — %]  | 100%             |
| Screen reader tested            | [PREENCHER — %]  | [PREENCHER]      |

### 9. Problemas Criticos e Acoes

| # | Problema                          | Severidade | Acao planejada          | Owner       | Prazo       |
|---|-----------------------------------|------------|-------------------------|-------------|-------------|
| 1 | [PREENCHER — problema critico]    | Alta       | [PREENCHER — acao]      | [PREENCHER] | [PREENCHER] |
| 2 | [PREENCHER — problema]            | Media      | [PREENCHER]             | [PREENCHER] | [PREENCHER] |
| 3 | [PREENCHER — problema]            | Media      | [PREENCHER]             | [PREENCHER] | [PREENCHER] |

### 10. Recomendacoes para Proximo Periodo

| Prioridade | Recomendacao                              | Impacto esperado           |
|------------|-------------------------------------------|----------------------------|
| P0         | [PREENCHER — acao urgente]                | [PREENCHER]                |
| P1         | [PREENCHER — acao importante]             | [PREENCHER]                |
| P2         | [PREENCHER — melhoria continua]           | [PREENCHER]                |

## Example (Parcialmente Preenchido)

**Health Score:** 7.2/10 (anterior: 6.8)
**Win:** Adocao subiu de 62% para 74% — Squad Growth migrou 100% para DS.
**Preocupacao:** 12 bugs de a11y abertos ha mais de 30 dias — precisamos de sprint dedicado.
**Feedback:** _"O DS acelerou nosso desenvolvimento em 30% este quarter."_ — Tech Lead, Squad Payments

## Notes

- Colete metricas de forma automatizada para evitar vies e reduzir esforco manual.
- Compare sempre com o periodo anterior para mostrar evolucao.
- Use o report para justificar investimento em headcount e ferramentas para o time de DS.
- Compartilhe amplamente — transparencia gera confianca e engajamento.
- Aja sobre os problemas criticos antes do proximo report — demonstre responsividade.
