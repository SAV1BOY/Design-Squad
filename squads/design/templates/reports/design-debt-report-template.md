# Design Debt Report Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Produto**          | [PREENCHER — nome do produto]                  |
| **Autor(a)**         | [PREENCHER — design lead / manager]            |
| **Data do report**   | [PREENCHER — YYYY-MM-DD]                       |
| **Periodo de analise** | [PREENCHER — periodo coberto]                |
| **Total de itens**   | [PREENCHER — numero de debitos catalogados]    |
| **Status**           | [PREENCHER — Draft / Apresentado / Em acao]    |

## Instructions (Como Usar)

1. Catalogue todos os itens de design debt conhecidos pelo time.
2. Classifique por tipo, severidade e impacto no usuario/negocio.
3. Priorize usando a matriz de impacto vs. esforco.
4. Negocie com PM um % de capacidade dedicada a resolver design debt.
5. Atualize regularmente conforme itens sao resolvidos ou novos surgem.

> **Dica:** Design debt e como divida financeira — se nao pago, cresce com juros. Torne-o visivel para a lideranca.

## Template

### 1. O que e Design Debt

Design debt refere-se a decisoes de design abaixo do ideal que foram tomadas para acelerar entregas, acumulando problemas que precisam ser resolvidos futuramente. Inclui: inconsistencias visuais, fluxos confusos, componentes ad-hoc, falta de estados, e problemas de acessibilidade.

### 2. Resumo do Estado Atual

**Total de itens de design debt:** [PREENCHER]
**Estimativa de esforco total:** [PREENCHER — story points / sprints]

| Severidade | Quantidade | % do total    |
|------------|------------|---------------|
| Critico    | [PREENCHER]| [PREENCHER]   |
| Alto       | [PREENCHER]| [PREENCHER]   |
| Medio      | [PREENCHER]| [PREENCHER]   |
| Baixo      | [PREENCHER]| [PREENCHER]   |

**Tendencia vs. periodo anterior:** [PREENCHER — aumentando / estavel / diminuindo]

### 3. Tipos de Design Debt

| Tipo                        | Quantidade | Exemplos                           |
|-----------------------------|------------|------------------------------------|
| Inconsistencia visual       | [PREENCHER]| [PREENCHER — onde aparece]         |
| Componentes ad-hoc (fora DS)| [PREENCHER]| [PREENCHER — quais]               |
| Fluxos confusos/incompletos | [PREENCHER]| [PREENCHER — quais fluxos]        |
| Estados faltantes           | [PREENCHER]| [PREENCHER — empty/error/loading]  |
| Acessibilidade              | [PREENCHER]| [PREENCHER — issues a11y]          |
| Copy/UX Writing             | [PREENCHER]| [PREENCHER — textos inconsistentes]|
| Responsividade              | [PREENCHER]| [PREENCHER — breakpoints faltantes]|
| [PREENCHER — outro]         | [PREENCHER]| [PREENCHER]                        |

### 4. Catalogo de Design Debt

#### Debt #1: [PREENCHER — titulo]

| Campo           | Valor                                           |
|-----------------|--------------------------------------------------|
| **Tipo**        | [PREENCHER — tipo de debt]                        |
| **Severidade**  | [PREENCHER — Critico / Alto / Medio / Baixo]      |
| **Area/Tela**   | [PREENCHER — onde existe]                          |
| **Descricao**   | [PREENCHER — o que esta errado]                    |
| **Impacto usuario** | [PREENCHER — como afeta o usuario]             |
| **Impacto negocio** | [PREENCHER — impacto em metricas]              |
| **Causa**       | [PREENCHER — por que foi criado]                   |
| **Esforco fix** | [PREENCHER — estimativa]                           |
| **Screenshot**  | [PREENCHER — evidencia]                            |

---

#### Debt #2: [PREENCHER — titulo]

| Campo           | Valor                                           |
|-----------------|--------------------------------------------------|
| **Tipo**        | [PREENCHER]                                       |
| **Severidade**  | [PREENCHER]                                       |
| **Area/Tela**   | [PREENCHER]                                       |
| **Descricao**   | [PREENCHER]                                       |
| **Impacto usuario** | [PREENCHER]                                    |
| **Esforco fix** | [PREENCHER]                                       |

---

#### Debt #3: [PREENCHER — titulo]

| Campo           | Valor                                           |
|-----------------|--------------------------------------------------|
| **Tipo**        | [PREENCHER]                                       |
| **Severidade**  | [PREENCHER]                                       |
| **Area/Tela**   | [PREENCHER]                                       |
| **Descricao**   | [PREENCHER]                                       |
| **Impacto usuario** | [PREENCHER]                                    |
| **Esforco fix** | [PREENCHER]                                       |

> Continue listando conforme necessario.

### 5. Priorizacao

| # | Debt item                    | Impacto (1-5) | Esforco (1-5) | Score     | Prioridade |
|---|------------------------------|---------------|---------------|-----------|------------|
| 1 | [PREENCHER]                  | [PREENCHER]   | [PREENCHER]   | [PREENCHER]| P0        |
| 2 | [PREENCHER]                  | [PREENCHER]   | [PREENCHER]   | [PREENCHER]| P1        |
| 3 | [PREENCHER]                  | [PREENCHER]   | [PREENCHER]   | [PREENCHER]| P1        |
| 4 | [PREENCHER]                  | [PREENCHER]   | [PREENCHER]   | [PREENCHER]| P2        |

> Score = Impacto / Esforco. Maior score = maior prioridade.

### 6. Plano de Reducao

**Estrategia:** [PREENCHER — ex.: 20% da capacidade de cada sprint dedicada a design debt]

| Quarter    | Itens planejados para resolver       | Esforco estimado  |
|------------|--------------------------------------|-------------------|
| [PREENCHER]| [PREENCHER — lista de itens]         | [PREENCHER]       |
| [PREENCHER]| [PREENCHER]                          | [PREENCHER]       |
| [PREENCHER]| [PREENCHER]                          | [PREENCHER]       |

### 7. Prevenção de Novo Debt

| Pratica                                    | Status        |
|--------------------------------------------|---------------|
| Design review obrigatoria antes de handoff | [PREENCHER]   |
| Uso obrigatorio do design system           | [PREENCHER]   |
| Edge cases documentados antes de build     | [PREENCHER]   |
| QA visual por designer pos-implementacao   | [PREENCHER]   |
| [PREENCHER — outra pratica]                | [PREENCHER]   |

### 8. Impacto Financeiro Estimado

| Aspecto                          | Custo estimado                    |
|----------------------------------|-----------------------------------|
| Horas gastas em workarounds      | [PREENCHER — horas/quarter]       |
| Tickets de suporte por UX ruim   | [PREENCHER — tickets/mes]         |
| Impacto em conversao/retencao    | [PREENCHER — estimativa]          |
| Custo de fix se adiado 6+ meses  | [PREENCHER — estimativa]          |

## Example (Parcialmente Preenchido)

**Debt #1 — "3 versoes diferentes de modal":** Tipo: Inconsistencia visual. 3 squads criaram modais customizados com comportamentos distintos. Impacto: Usuarios aprendem 3 padroes diferentes; a11y comprometida em 2 das 3 versoes. Esforco fix: Migrar para componente Modal do DS — estimativa 2 sprints para todos os squads. Score: 4.5/5 impacto, 3/5 esforco = prioridade P0.

## Notes

- Torne design debt visivel no board do time — ao lado de tech debt.
- Negocie com PM: design debt nao resolvido gera mais debt e piora metricas.
- Prevenir e mais barato que remediar — invista em processos de qualidade.
- Atualize este report mensalmente ou ao menos a cada quarter.
- Use metricas de impacto (NPS, support tickets, conversao) para justificar investimento.
