# Design System Health Report

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Design System**    | [PREENCHER — nome do DS]                       |
| **Periodo**          | [PREENCHER — ex.: Janeiro-Marco 2026]          |
| **Autor(a)**         | [PREENCHER — DS lead]                          |
| **Data do report**   | [PREENCHER — YYYY-MM-DD]                       |
| **Versao atual DS**  | [PREENCHER — ex.: v4.1.0]                      |
| **Audiencia**        | [PREENCHER — lideranca / todos os squads]      |

## Instructions (Como Usar)

1. Gere este report ao final de cada quarter ou periodo definido.
2. Colete dados de multiplas fontes (analytics, surveys, codebase scans).
3. Compare com periodos anteriores para mostrar tendencias.
4. Use como input para o roadmap do proximo periodo.
5. Compartilhe com lideranca para demonstrar ROI do DS.

> **Dica:** Automatize a coleta de metricas para reduzir esforco e garantir consistencia.

## Template

### 1. Resumo Executivo

[PREENCHER — 3-5 frases sobre o estado geral do DS, principais conquistas e desafios do periodo.]

**Health Score:** [PREENCHER — X/10] (anterior: [PREENCHER — X/10])

### 2. KPIs Principais

| KPI                             | Meta       | Anterior   | Atual      | Status     |
|---------------------------------|------------|------------|------------|------------|
| Adocao (% componentes DS)       | [PREENCHER]| [PREENCHER]| [PREENCHER]| [PREENCHER — On track / At risk / Off track] |
| Cobertura (componentes no DS)   | [PREENCHER]| [PREENCHER]| [PREENCHER]| [PREENCHER]|
| Qualidade (bugs abertos)        | [PREENCHER]| [PREENCHER]| [PREENCHER]| [PREENCHER]|
| Satisfacao (NPS interno)        | [PREENCHER]| [PREENCHER]| [PREENCHER]| [PREENCHER]|
| Velocidade (time to new component)| [PREENCHER]| [PREENCHER]| [PREENCHER]| [PREENCHER]|

### 3. Adocao por Squad

| Squad              | Adocao %   | Anterior % | Tendencia  | Bloqueadores           |
|--------------------|------------|------------|------------|------------------------|
| [PREENCHER]        | [PREENCHER]| [PREENCHER]| [PREENCHER]| [PREENCHER]            |
| [PREENCHER]        | [PREENCHER]| [PREENCHER]| [PREENCHER]| [PREENCHER]            |
| [PREENCHER]        | [PREENCHER]| [PREENCHER]| [PREENCHER]| [PREENCHER]            |
| [PREENCHER]        | [PREENCHER]| [PREENCHER]| [PREENCHER]| [PREENCHER]            |

### 4. Catalogo do DS

| Metrica                    | Valor                |
|----------------------------|----------------------|
| Total de componentes       | [PREENCHER]          |
| Componentes adicionados    | [PREENCHER]          |
| Componentes deprecados     | [PREENCHER]          |
| Total de tokens            | [PREENCHER]          |
| Releases no periodo        | [PREENCHER]          |
| Breaking changes           | [PREENCHER]          |

### 5. Qualidade e Suporte

| Metrica                         | Valor              |
|---------------------------------|---------------------|
| Bugs reportados no periodo      | [PREENCHER]         |
| Bugs resolvidos no periodo      | [PREENCHER]         |
| Tempo medio de resolucao        | [PREENCHER — dias]  |
| Requests recebidos              | [PREENCHER]         |
| Requests atendidos              | [PREENCHER]         |
| Tempo medio de atendimento      | [PREENCHER — dias]  |
| A11y compliance %               | [PREENCHER]         |

### 6. Impacto e ROI

**Tempo economizado estimado:**
- [PREENCHER — horas de desenvolvimento economizadas por componente reutilizado]
- [PREENCHER — reducao de QA/bug fixes por consistencia]

**Consistencia:**
- [PREENCHER — reducao de variacoes visuais detectadas]
- [PREENCHER — melhoria em metricas de UX]

**Velocidade de entrega:**
- [PREENCHER — reducao de tempo de design-to-ship]

### 7. Top Requests e Gaps

| # | Request / Gap                         | Squads solicitantes | Status         |
|---|---------------------------------------|---------------------|----------------|
| 1 | [PREENCHER — componente solicitado]   | [PREENCHER]         | [PREENCHER]    |
| 2 | [PREENCHER]                           | [PREENCHER]         | [PREENCHER]    |
| 3 | [PREENCHER]                           | [PREENCHER]         | [PREENCHER]    |

### 8. Acoes do Proximo Periodo

| # | Acao                                  | Tipo              | Responsavel    | Meta         |
|---|---------------------------------------|-------------------|----------------|--------------|
| 1 | [PREENCHER — acao prioritaria]        | [PREENCHER]       | [PREENCHER]    | [PREENCHER]  |
| 2 | [PREENCHER]                           | [PREENCHER]       | [PREENCHER]    | [PREENCHER]  |
| 3 | [PREENCHER]                           | [PREENCHER]       | [PREENCHER]    | [PREENCHER]  |

## Example (Parcialmente Preenchido)

**Health Score:** 7.5/10 (anterior: 7.0)
**Conquista:** Adocao subiu de 68% para 76%. Squad Checkout migrou 100% para DS.
**Desafio:** 8 bugs de a11y abertos ha mais de 30 dias. NPS interno caiu de 72 para 65 — principal reclamacao: documentacao desatualizada.

## Notes

- Mantenha formato consistente entre reports para facilitar comparacao.
- Automatize metricas de adocao usando ferramentas de scan de codebase.
- Use o report para negociar recursos e headcount para o time de DS.
- Celebre conquistas publicamente — reconhecimento motiva o time.
- Vincule cada acao do proximo periodo a um KPI especifico.
