# Design Doc Writing

## Context

Adaptação de voz para escrita de design docs — documentos longos que capturam o
pensamento por trás de decisões de design significativas. Um design doc não é um
spec (que detalha o "como"); é um documento estratégico que explica o "porquê",
mapeia alternativas e registra o raciocínio para consulta futura.

Design docs são artefatos de longa vida — serão lidos meses ou anos depois por
pessoas que não participaram da decisão original.

**Canal:** Confluence, Notion, Google Docs, repositório de docs
**Audiência:** Cross-funcional (design, produto, engenharia, liderança)
**Formalidade:** Nível 3-4 (Profissional a Formal)
**Tom:** Evidence-Driven + System Thinker

## Document Structure

### 1. Header e Metadata
```
# [Título Descritivo do Design Doc]

| Campo            | Valor                    |
|------------------|--------------------------|
| Autor(es)        | [Nomes]                  |
| Status           | [Draft / In Review / Approved / Superseded] |
| Data de criação  | [DD/MM/AAAA]             |
| Última atualização | [DD/MM/AAAA]           |
| Reviewers        | [Nomes]                  |
| Squad            | [Nome do squad]          |
| Épico/Feature    | [Link]                   |
```

### 2. TL;DR (máximo 3 frases)
- O que estamos fazendo, por que, e qual o impacto esperado
- Quem não tem tempo de ler o doc inteiro pega o essencial aqui

### 3. Contexto e Problema
- Qual a situação atual e por que ela é insatisfatória
- Dados que evidenciam o problema (métricas, pesquisa, feedback)
- Impacto do problema no usuário e no negócio

### 4. Objetivos e Não-Objetivos
- O que este design doc resolve (escopo)
- O que este design doc NÃO resolve (explicitamente fora de escopo)
- Métricas de sucesso propostas

### 5. Solução Proposta
- Descrição detalhada da abordagem escolhida
- Mockups e protótipos de referência
- Mapeamento de fluxo e interações-chave
- Considerações de acessibilidade
- Considerações de performance e escalabilidade

### 6. Alternativas Consideradas
- Pelo menos 2 alternativas avaliadas
- Prós e contras de cada uma
- Razão objetiva para descarte

### 7. Riscos e Mitigações
- Riscos identificados (técnicos, de UX, de negócio)
- Estratégia de mitigação para cada risco
- Plano B se a solução primária falhar

### 8. Plano de Implementação
- Fases de rollout
- Dependências entre times
- Timeline estimada

### 9. Open Questions
- Perguntas ainda não respondidas
- Owner de cada pergunta
- Deadline para resolução

## Writing Rules

### Tom e linguagem
- Escrever na primeira pessoa do plural: "Propomos...", "Avaliamos..."
- Ser direto nos argumentos, sem hedging excessivo
- Dados antes de opinião: "Os testes mostram X" antes de "Acreditamos que Y"
- Reconhecer incerteza: "Com os dados disponíveis, a melhor hipótese é..."

### Estrutura e formatação
- Parágrafos de no máximo 5 linhas
- Headers claros e descritivos (não "Seção 3", mas "Alternativas Consideradas")
- Tabelas para comparações e trade-offs
- Links para artefatos ao invés de embedar screenshots gigantes
- Changelog no final para documentar evolução do doc

### Revisão e colaboração
- Compartilhar draft cedo — não esperar estar "perfeito"
- Marcar sections que precisam de input específico com [FEEDBACK NEEDED]
- Resolver comments antes de mudar status para Approved
- Versionar: v0.1 (draft), v0.5 (review), v1.0 (approved)

## Common Mistakes

- Doc tão longo que ninguém lê (ideal: 3-6 páginas sem apêndices)
- Ausência de alternativas (parece que não houve análise crítica)
- Métricas de sucesso vagas ("melhorar a experiência")
- Não atualizar quando a implementação diverge da proposta original
- Esquecer de listar não-objetivos (escopo cresce indefinidamente)

## Cross-References

- `voice/language-guides/documentation-style.md` — Estilo de documentação
- `voice/calibration/audience-depth-scale.md` — Calibração por público
- `docs/design-review-standards.md` — Processo de review de design docs
