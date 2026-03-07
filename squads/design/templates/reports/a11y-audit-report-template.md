# Accessibility Audit Report Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Produto / Area**   | [PREENCHER — o que foi auditado]               |
| **Auditor(a)**       | [PREENCHER — quem conduziu]                    |
| **Data do report**   | [PREENCHER — YYYY-MM-DD]                       |
| **Standard**         | [PREENCHER — WCAG 2.1 AA / WCAG 2.2 AA]       |
| **Paginas auditadas**| [PREENCHER — numero de paginas]                |
| **Issues encontradas**| [PREENCHER — numero total]                    |
| **Status**           | [PREENCHER — Draft / Final / Em remediacao]    |

## Instructions (Como Usar)

1. Conduza testes automatizados e manuais conforme o plan de auditoria.
2. Registre cada issue com o criterio WCAG especifico violado.
3. Classifique por severidade e impacto no usuario.
4. Inclua screenshots e sugestoes de correcao para cada issue.
5. Acompanhe a remediacao e planeje retest.

> **Dica:** Teste sempre com pelo menos 1 screen reader real e navegacao por teclado — ferramentas automatizadas nao capturam tudo.

## Template

### 1. Resumo Executivo

[PREENCHER — em 5-8 frases, resuma o nivel de conformidade atual, areas mais problematicas e recomendacoes prioritarias.]

**Nivel de conformidade:** [PREENCHER — Compliant / Partially compliant / Non-compliant]
**Issues criticas:** [PREENCHER — numero]
**Issues totais:** [PREENCHER — numero]

### 2. Escopo da Auditoria

| # | Pagina / Tela            | URL                       | Auditada |
|---|--------------------------|---------------------------|----------|
| 1 | [PREENCHER — pagina]     | [PREENCHER — URL]         | Sim      |
| 2 | [PREENCHER]              | [PREENCHER]               | Sim      |
| 3 | [PREENCHER]              | [PREENCHER]               | Sim      |
| 4 | [PREENCHER]              | [PREENCHER]               | Sim      |

**Ferramentas utilizadas:**
- [PREENCHER — ex.: axe DevTools v4.x]
- [PREENCHER — ex.: WAVE]
- [PREENCHER — ex.: NVDA + Firefox]
- [PREENCHER — ex.: VoiceOver + Safari]
- [PREENCHER — ex.: Keyboard-only testing]

### 3. Resultados por Principio WCAG

| Principio       | Issues encontradas | Criticas | Altas | Medias | Baixas |
|------------------|-------------------|----------|-------|--------|--------|
| 1. Perceivable   | [PREENCHER]       | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |
| 2. Operable      | [PREENCHER]       | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |
| 3. Understandable| [PREENCHER]       | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |
| 4. Robust        | [PREENCHER]       | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |
| **Total**        | [PREENCHER]       | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |

### 4. Issues Detalhadas

#### Issue #1: [PREENCHER — titulo descritivo]

| Campo                | Valor                                      |
|----------------------|--------------------------------------------|
| **WCAG Criterion**   | [PREENCHER — ex.: 1.1.1 Non-text Content] |
| **Level**            | [PREENCHER — A / AA / AAA]                |
| **Severidade**       | [PREENCHER — Critica / Alta / Media / Baixa] |
| **Pagina(s)**        | [PREENCHER — onde ocorre]                  |
| **Descricao**        | [PREENCHER — o que esta errado]            |
| **Impacto**          | [PREENCHER — como afeta usuarios com deficiencia] |
| **Screenshot**       | [PREENCHER — evidencia]                    |
| **Sugestao de fix**  | [PREENCHER — como corrigir, com exemplo de codigo se possivel] |
| **Esforco**          | [PREENCHER — Baixo / Medio / Alto]         |

---

#### Issue #2: [PREENCHER — titulo]

| Campo                | Valor                                      |
|----------------------|--------------------------------------------|
| **WCAG Criterion**   | [PREENCHER]                                |
| **Level**            | [PREENCHER]                                |
| **Severidade**       | [PREENCHER]                                |
| **Pagina(s)**        | [PREENCHER]                                |
| **Descricao**        | [PREENCHER]                                |
| **Impacto**          | [PREENCHER]                                |
| **Sugestao de fix**  | [PREENCHER]                                |

---

#### Issue #3: [PREENCHER — titulo]

| Campo                | Valor                                      |
|----------------------|--------------------------------------------|
| **WCAG Criterion**   | [PREENCHER]                                |
| **Severidade**       | [PREENCHER]                                |
| **Pagina(s)**        | [PREENCHER]                                |
| **Descricao**        | [PREENCHER]                                |
| **Sugestao de fix**  | [PREENCHER]                                |

> Adicione mais issues seguindo o mesmo formato.

### 5. Resultados por Pagina

| Pagina          | Total issues | Criticas | Pass rate (criterios) |
|-----------------|--------------|----------|-----------------------|
| [PREENCHER]     | [PREENCHER]  | [PREENCHER] | [PREENCHER — %]    |
| [PREENCHER]     | [PREENCHER]  | [PREENCHER] | [PREENCHER — %]    |
| [PREENCHER]     | [PREENCHER]  | [PREENCHER] | [PREENCHER — %]    |

### 6. Plano de Remediacao

| Prioridade | Issue(s)        | Acao                          | Responsavel  | Prazo        |
|------------|-----------------|-------------------------------|--------------|--------------|
| P0         | #[PREENCHER]    | [PREENCHER — fix]             | [PREENCHER]  | [PREENCHER]  |
| P1         | #[PREENCHER]    | [PREENCHER]                   | [PREENCHER]  | [PREENCHER]  |
| P2         | #[PREENCHER]    | [PREENCHER]                   | [PREENCHER]  | [PREENCHER]  |

### 7. Retest Plan

| Issue(s)      | Data de retest     | Responsavel     | Status         |
|---------------|--------------------|-----------------| ---------------|
| #[PREENCHER]  | [PREENCHER]        | [PREENCHER]     | [PREENCHER]    |
| #[PREENCHER]  | [PREENCHER]        | [PREENCHER]     | [PREENCHER]    |

### 8. Comparacao com Auditoria Anterior (se aplicavel)

| Metrica                | Auditoria anterior  | Auditoria atual   | Tendencia  |
|------------------------|---------------------|--------------------|------------|
| Total issues           | [PREENCHER]         | [PREENCHER]        | [PREENCHER]|
| Issues criticas        | [PREENCHER]         | [PREENCHER]        | [PREENCHER]|
| Pass rate              | [PREENCHER]         | [PREENCHER]        | [PREENCHER]|

## Example (Parcialmente Preenchido)

**Issue #1 — Imagens sem alt text:** WCAG 1.1.1, Severidade Alta. 15 imagens na pagina de produtos nao possuem texto alternativo. Screen readers anunciam apenas "image" sem contexto. Fix: Adicionar alt descritivo a cada imagem. Esforco: Baixo.

## Notes

- Ferramentas automatizadas capturam ~30% dos problemas — teste manual e indispensavel.
- Priorize issues que bloqueiam tarefas criticas (login, compra, cadastro).
- Inclua exemplos de codigo correto nas sugestoes de fix quando possivel.
- Auditorias devem ser recorrentes, nao pontuais — acessibilidade e continua.
- Considere envolver usuarios com deficiencia em testes complementares.
