# Component RFC Template

## Metadata

| Campo                | Valor                                            |
|----------------------|--------------------------------------------------|
| **RFC ID**           | [PREENCHER — ex.: RFC-DS-2026-005]               |
| **Componente**       | [PREENCHER — nome do componente proposto]        |
| **Tipo**             | [PREENCHER — Novo / Major change / Deprecacao]   |
| **Autor(a)**         | [PREENCHER — quem esta propondo]                 |
| **Reviewers**        | [PREENCHER — quem deve revisar]                  |
| **Data de criacao**  | [PREENCHER — YYYY-MM-DD]                         |
| **Deadline review**  | [PREENCHER — data limite para feedback]          |
| **Status**           | [PREENCHER — Draft / Em review / Aprovado / Rejeitado / Implementado] |

## Instructions (Como Usar)

1. Escreva este RFC antes de iniciar o design detalhado de um novo componente.
2. Distribua para reviewers e colete feedback dentro do deadline.
3. Enderece todos os comentarios e atualize o RFC com decisoes.
4. Obtenha aprovacao formal antes de prosseguir para implementacao.
5. Use como referencia durante todo o ciclo de vida do componente.

> **Dica:** RFCs bons previnem retrabalho. Invista tempo na justificativa e na analise de alternativas.

## Template

### 1. Resumo

[PREENCHER — em 3-5 frases, descreva o que esta sendo proposto e por que.]

### 2. Motivacao

**Problema:**
[PREENCHER — qual problema este componente resolve? Que inconsistencia ou gap ele endereca?]

**Impacto do problema:**
- Squads afetados: [PREENCHER — numero e nomes]
- Implementacoes duplicadas hoje: [PREENCHER — quantas versoes customizadas existem]
- Inconsistencias de UX: [PREENCHER — onde e como]
- Custo de manutencao: [PREENCHER — estimativa de tempo gasto]

### 3. Proposta Detalhada

**Nome do componente:** [PREENCHER — nome proposto]
**Categoria:** [PREENCHER — Primitive / Composite / Pattern]

**Descricao funcional:**
[PREENCHER — o que o componente faz, como se comporta, onde e usado]

**API proposta (Props):**

| Prop           | Tipo           | Default      | Descricao                          |
|----------------|----------------|--------------|-------------------------------------|
| [PREENCHER]    | [PREENCHER]    | [PREENCHER]  | [PREENCHER]                         |
| [PREENCHER]    | [PREENCHER]    | [PREENCHER]  | [PREENCHER]                         |
| [PREENCHER]    | [PREENCHER]    | [PREENCHER]  | [PREENCHER]                         |
| [PREENCHER]    | [PREENCHER]    | [PREENCHER]  | [PREENCHER]                         |
| [PREENCHER]    | [PREENCHER]    | [PREENCHER]  | [PREENCHER]                         |

**Variantes:**
- [PREENCHER — variante 1 e descricao]
- [PREENCHER — variante 2 e descricao]
- [PREENCHER — variante 3 e descricao]

**Estados:**
- [PREENCHER — lista de estados com breve descricao]

### 4. Design Visual

**Link para exploracoes:** [PREENCHER — link Figma]

**Anatomia do componente:**
```
[PREENCHER — representacao ASCII da estrutura]
```

**Tokens utilizados:**
| Propriedade      | Token                          |
|------------------|--------------------------------|
| Background       | [PREENCHER — nome do token]    |
| Text color       | [PREENCHER]                    |
| Border           | [PREENCHER]                    |
| Border radius    | [PREENCHER]                    |
| Spacing          | [PREENCHER]                    |

### 5. Acessibilidade

- **ARIA role:** [PREENCHER — role semantica]
- **Keyboard:** [PREENCHER — interacoes de teclado]
- **Screen reader:** [PREENCHER — como sera anunciado]
- **Focus management:** [PREENCHER — comportamento de foco]
- **Contraste:** [PREENCHER — ratio verificado]
- **WCAG criteria:** [PREENCHER — criterios atendidos]

### 6. Casos de Uso

| # | Caso de uso                              | Squad / Contexto     | Prioridade |
|---|------------------------------------------|----------------------|------------|
| 1 | [PREENCHER — uso principal]              | [PREENCHER]          | Must-have  |
| 2 | [PREENCHER — uso secundario]             | [PREENCHER]          | Should-have|
| 3 | [PREENCHER — edge case]                  | [PREENCHER]          | Nice-to-have|

### 7. Alternativas Consideradas

**Alternativa A: [PREENCHER — descricao]**
- Pros: [PREENCHER]
- Cons: [PREENCHER]
- Motivo de rejeicao: [PREENCHER]

**Alternativa B: [PREENCHER — descricao]**
- Pros: [PREENCHER]
- Cons: [PREENCHER]
- Motivo de rejeicao: [PREENCHER]

**Alternativa C: Nao fazer nada**
- Pros: [PREENCHER — zero esforco]
- Cons: [PREENCHER — problemas continuam]

### 8. Plano de Implementacao

| Fase                    | Descricao                          | Estimativa    |
|-------------------------|------------------------------------|---------------|
| Design spec             | [PREENCHER — detalhamento visual]  | [PREENCHER]   |
| Figma component         | [PREENCHER — biblioteca Figma]     | [PREENCHER]   |
| Code (React/Web)        | [PREENCHER — implementacao]        | [PREENCHER]   |
| Code (iOS)              | [PREENCHER — se aplicavel]         | [PREENCHER]   |
| Code (Android)          | [PREENCHER — se aplicavel]         | [PREENCHER]   |
| Documentacao            | [PREENCHER — Storybook + docs]     | [PREENCHER]   |
| Testes                  | [PREENCHER — unit + visual]        | [PREENCHER]   |
| Migracao de squads      | [PREENCHER — adocao]               | [PREENCHER]   |

### 9. Migracao e Breaking Changes

**E breaking change?** [PREENCHER — Sim / Nao]
**Componentes que substitui:** [PREENCHER — lista de componentes deprecados]
**Plano de migracao:** [PREENCHER — como squads vao migrar]
**Codemods disponivel?** [PREENCHER — Sim / Nao / Planejado]

### 10. Questoes em Aberto

| # | Questao                                      | Status            | Decisao            |
|---|----------------------------------------------|-------------------|--------------------|
| 1 | [PREENCHER — duvida sobre API ou design]     | [PREENCHER]       | [PREENCHER]        |
| 2 | [PREENCHER — duvida sobre escopo]            | [PREENCHER]       | [PREENCHER]        |
| 3 | [PREENCHER — duvida sobre timeline]          | [PREENCHER]       | [PREENCHER]        |

### 11. Feedback dos Reviewers

| Reviewer        | Data        | Feedback resumido                    | Status         |
|-----------------|-------------|--------------------------------------|----------------|
| [PREENCHER]     | [PREENCHER] | [PREENCHER]                          | [PREENCHER — Endereçado / Pendente] |
| [PREENCHER]     | [PREENCHER] | [PREENCHER]                          | [PREENCHER]    |

## Example (Parcialmente Preenchido)

**RFC:** Novo componente DatePicker
**Motivacao:** 3 squads implementaram date pickers customizados; ha 4 versoes diferentes em producao com comportamentos inconsistentes e 2 delas falham em navegacao por teclado.
**API prop:** `value` (Date), `onChange` (callback), `minDate`/`maxDate` (Date), `locale` (string), `disabled` (boolean)
**Alternativa rejeitada:** Usar lib externa (react-datepicker) — rejeitada por nao se integrar com nossos tokens e ter bundle size elevado.

## Notes

- RFCs devem ter periodo minimo de review de [PREENCHER — ex.: 5 dias uteis].
- Todos os DS team members devem revisar. Feedback de squads consumidores e bem-vindo.
- Se a RFC for rejeitada, documente o motivo para referencia futura.
- Mantenha o RFC atualizado durante a implementacao — ele vira o doc de referencia.
- Apos implementacao, arquive o RFC e vincule a documentacao final do componente.
