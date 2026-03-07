# Feature Design Brief

## Metadata

| Campo              | Valor                                          |
|--------------------|-------------------------------------------------|
| **Feature**        | [PREENCHER — nome da feature]                   |
| **Squad / Time**   | [PREENCHER — squad responsavel]                 |
| **Designer**       | [PREENCHER — designer owner]                    |
| **PM**             | [PREENCHER — product manager]                   |
| **Data de criacao**| [PREENCHER — YYYY-MM-DD]                        |
| **Status**         | [PREENCHER — Draft / Em design / Em review / Handoff] |
| **Sprint / Ciclo** | [PREENCHER — referencia do ciclo]               |
| **Epic / Ticket**  | [PREENCHER — link para Jira/Linear/etc.]        |

## Instructions (Como Usar)

1. O PM deve preencher as secoes 1-4 antes de passar para o designer.
2. O designer completa as secoes 5-9 durante o processo de design.
3. Use este brief como referencia unica de verdade (source of truth) para a feature.
4. Revise com eng lead antes do handoff para garantir viabilidade tecnica.
5. Atualize o status conforme a feature progride pelas etapas.

> **Dica:** Vincule este brief ao ticket no tracker do time para facil rastreabilidade.

## Template

### 1. Resumo da Feature

[PREENCHER — descricao em 2-3 frases do que e a feature e qual valor ela entrega.]

### 2. Problema que Resolve

**Para quem:** [PREENCHER — persona ou segmento de usuario]
**Problema:** [PREENCHER — dor ou necessidade do usuario]
**Evidencia:** [PREENCHER — dados, pesquisa ou feedback que sustentam o problema]

### 3. Objetivos e Metricas de Sucesso

| Objetivo                           | Metrica (KPI)                       | Meta                |
|------------------------------------|-------------------------------------|---------------------|
| [PREENCHER — objetivo 1]          | [PREENCHER — metrica]               | [PREENCHER — meta]  |
| [PREENCHER — objetivo 2]          | [PREENCHER — metrica]               | [PREENCHER — meta]  |

### 4. Requisitos Funcionais

| # | Requisito                                        | Prioridade     |
|---|--------------------------------------------------|----------------|
| 1 | [PREENCHER — requisito funcional]                | Must-have      |
| 2 | [PREENCHER — requisito funcional]                | Must-have      |
| 3 | [PREENCHER — requisito funcional]                | Should-have    |
| 4 | [PREENCHER — requisito funcional]                | Nice-to-have   |

### 5. User Stories / Cenarios

**Story 1:**
> Como [PREENCHER — persona], eu quero [PREENCHER — acao] para que [PREENCHER — beneficio].

**Story 2:**
> Como [PREENCHER — persona], eu quero [PREENCHER — acao] para que [PREENCHER — beneficio].

**Cenarios de edge case:**
- [PREENCHER — cenario de erro ou excecao]
- [PREENCHER — cenario de estado vazio]
- [PREENCHER — cenario de limite/boundary]

### 6. Fluxo do Usuario (Resumo)

```
[PREENCHER — entry point] --> [PREENCHER — step 1] --> [PREENCHER — step 2] --> [PREENCHER — step final]
                                    |
                                    v
                          [PREENCHER — caminho alternativo]
```

### 7. Restricoes e Consideracoes Tecnicas

- **Plataforma:** [PREENCHER — Web / iOS / Android / Todas]
- **Restricoes tecnicas:** [PREENCHER — APIs, dependencias, limitacoes]
- **Acessibilidade:** [PREENCHER — requisitos WCAG, navegacao por teclado, etc.]
- **Performance:** [PREENCHER — limites de tempo de carregamento, tamanho de payload]

### 8. Design Assets

| Artefato                  | Link                          | Status           |
|---------------------------|-------------------------------|------------------|
| Wireframes                | [PREENCHER — link Figma]      | [PREENCHER]      |
| Hi-fi mockups             | [PREENCHER — link Figma]      | [PREENCHER]      |
| Prototipo interativo      | [PREENCHER — link]            | [PREENCHER]      |
| Especificacao de motion   | [PREENCHER — link]            | [PREENCHER]      |

### 9. Dependencias e Riscos

| Tipo          | Descricao                              | Owner          | Status     |
|---------------|----------------------------------------|----------------|------------|
| Dependencia   | [PREENCHER — ex.: API de pagamento]    | [PREENCHER]    | [PREENCHER]|
| Risco         | [PREENCHER — ex.: mudanca de escopo]   | [PREENCHER]    | [PREENCHER]|

### 10. Checklist de Handoff

- [ ] Mockups finais aprovados pelo PM
- [ ] Especificacoes de componentes documentadas
- [ ] Edge cases e estados de erro mapeados
- [ ] Assets exportados (icones, imagens)
- [ ] Anotacoes de acessibilidade incluidas
- [ ] Review com eng lead realizado

## Example (Parcialmente Preenchido)

**Feature:** Filtro avancado de busca
**Squad:** Squad Marketplace
**Problema:** Usuarios com grande volume de produtos nao conseguem encontrar itens especificos, resultando em 35% de buscas sem clique em resultados.

**User Story:** Como vendedor com mais de 100 produtos, eu quero filtrar por categoria, preco e status para encontrar rapidamente o item que preciso editar.

## Notes

- Mantenha a secao de Design Assets atualizada com os links mais recentes.
- Se a feature for descontinuada ou pausada, atualize o status e documente o motivo.
- Para features complexas, considere criar um design spec separado com mais detalhes.
- Revise este brief em conjunto com o time na planning/kick-off da feature.
