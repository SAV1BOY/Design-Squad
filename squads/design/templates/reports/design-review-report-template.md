# Design Review Report Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Feature / Projeto**| [PREENCHER — o que foi revisado]               |
| **Designer(s)**      | [PREENCHER — designer(s) da feature]           |
| **Reviewer(s)**      | [PREENCHER — quem fez a review]                |
| **Data da review**   | [PREENCHER — YYYY-MM-DD]                       |
| **Tipo de review**   | [PREENCHER — Crit / Peer review / Stakeholder review] |
| **Fase do design**   | [PREENCHER — Conceito / Wireframe / Hi-fi / Pre-handoff] |
| **Status**           | [PREENCHER — Aprovado / Aprovado com ajustes / Necessita revisao] |

## Instructions (Como Usar)

1. O reviewer preenche este report apos a sessao de design review.
2. Categorize o feedback em: Must-fix, Should-fix, Consider, Positive.
3. O designer endereca cada item e atualiza o status.
4. Use como registro historico das decisoes de design.
5. Vincule ao ticket da feature para rastreabilidade.

> **Dica:** Design reviews devem ser construtivas. Foque no trabalho, nao na pessoa. Comece pelos pontos positivos.

## Template

### 1. Contexto da Review

**O que foi apresentado:** [PREENCHER — descricao do que foi revisado]
**Objetivo da feature:** [PREENCHER — o que a feature resolve]
**Formato da review:** [PREENCHER — sincrono / assincrono / misto]
**Duracao:** [PREENCHER — tempo da sessao]
**Link do design:** [PREENCHER — link Figma]

### 2. Pontos Positivos

| # | Destaque                                       |
|---|------------------------------------------------|
| 1 | [PREENCHER — o que esta bem feito]             |
| 2 | [PREENCHER — decisao de design acertada]       |
| 3 | [PREENCHER — elemento criativo ou inovador]    |

### 3. Feedback — Must-fix (Obrigatorio)

Itens que devem ser corrigidos antes de prosseguir.

| # | Feedback                                | Justificativa                     | Status          |
|---|------------------------------------------|-----------------------------------|-----------------|
| 1 | [PREENCHER — o que corrigir]             | [PREENCHER — por que]             | [PREENCHER — Pendente / Feito] |
| 2 | [PREENCHER]                              | [PREENCHER]                       | [PREENCHER]     |
| 3 | [PREENCHER]                              | [PREENCHER]                       | [PREENCHER]     |

### 4. Feedback — Should-fix (Recomendado)

Itens importantes mas que nao bloqueiam o avanco.

| # | Feedback                                | Justificativa                     | Status          |
|---|------------------------------------------|-----------------------------------|-----------------|
| 1 | [PREENCHER]                              | [PREENCHER]                       | [PREENCHER]     |
| 2 | [PREENCHER]                              | [PREENCHER]                       | [PREENCHER]     |

### 5. Feedback — Consider (Para Considerar)

Sugestoes e exploracoes que podem agregar valor.

| # | Sugestao                                | Contexto                          |
|---|------------------------------------------|-----------------------------------|
| 1 | [PREENCHER — sugestao]                   | [PREENCHER — por que considerar]  |
| 2 | [PREENCHER]                              | [PREENCHER]                       |

### 6. Perguntas Levantadas

| # | Pergunta                                | Resposta / Decisao                |
|---|------------------------------------------|-----------------------------------|
| 1 | [PREENCHER — pergunta durante a review]  | [PREENCHER — resposta ou TBD]     |
| 2 | [PREENCHER]                              | [PREENCHER]                       |
| 3 | [PREENCHER]                              | [PREENCHER]                       |

### 7. Checklist de Cobertura

O reviewer verificou:
- [ ] Fluxo do usuario completo (happy path + alternativos)
- [ ] Todos os estados (default, loading, error, empty, success)
- [ ] Responsividade (mobile, tablet, desktop)
- [ ] Acessibilidade (contraste, labels, keyboard)
- [ ] Consistencia com design system
- [ ] Copy e UX writing
- [ ] Edge cases documentados
- [ ] Viabilidade tecnica considerada

### 8. Decisoes Tomadas

| # | Decisao                                 | Racional                           |
|---|------------------------------------------|-------------------------------------|
| 1 | [PREENCHER — decisao]                   | [PREENCHER — por que]               |
| 2 | [PREENCHER]                              | [PREENCHER]                         |

### 9. Proximos Passos

| # | Acao                                    | Responsavel     | Prazo           |
|---|-----------------------------------------|-----------------|-----------------|
| 1 | [PREENCHER — acao pos-review]           | [PREENCHER]     | [PREENCHER]     |
| 2 | [PREENCHER]                             | [PREENCHER]     | [PREENCHER]     |
| 3 | [PREENCHER]                             | [PREENCHER]     | [PREENCHER]     |

### 10. Veredicto Final

**Resultado:** [PREENCHER — Aprovado / Aprovado com ajustes / Necessita nova review]

**Condicoes para aprovacao (se aplicavel):**
- [ ] [PREENCHER — condicao 1]
- [ ] [PREENCHER — condicao 2]

**Proxima review agendada:** [PREENCHER — data, se necessario]

## Example (Parcialmente Preenchido)

**Feature:** Modal de upgrade de plano
**Fase:** Hi-fi (pre-handoff)
**Positivo:** Hierarquia clara entre os planos, comparacao lado a lado facilita decisao.
**Must-fix #1:** Botao "Upgrade" no plano Free esta com a mesma cor do plano Pro — confunde o usuario sobre qual plano esta selecionando. Sugestao: Diferenciar visualmente o CTA por plano.
**Veredicto:** Aprovado com ajustes — corrigir 2 must-fixes e 1 should-fix, nao precisa nova review.

## Notes

- Reviews devem acontecer em checkpoints definidos, nao apenas no final.
- Mantenha o tom construtivo — "e se..." e mais produtivo que "isso esta errado".
- Diferencie feedback de preferencia pessoal vs. problema real de usabilidade.
- Registre todas as decisoes — evita re-discussoes futuras.
- O designer nao precisa aceitar todo feedback — mas deve justificar quando discordar.
