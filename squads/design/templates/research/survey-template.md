# Survey Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Projeto**          | [PREENCHER — nome do projeto]                  |
| **Objetivo**         | [PREENCHER — o que queremos medir/entender]    |
| **Researcher**       | [PREENCHER — responsavel]                      |
| **Plataforma**       | [PREENCHER — Typeform / Google Forms / Qualtrics] |
| **Data de criacao**  | [PREENCHER — YYYY-MM-DD]                       |
| **Data de lancamento** | [PREENCHER — YYYY-MM-DD]                     |
| **Data de fechamento** | [PREENCHER — YYYY-MM-DD]                     |
| **Amostra alvo**     | [PREENCHER — numero de respostas desejadas]    |

## Instructions (Como Usar)

1. Defina claramente as research questions antes de escrever as perguntas do survey.
2. Mantenha o survey curto — idealmente menos de 15 perguntas, 5-7 minutos.
3. Faca um piloto com 3-5 pessoas para validar clareza e tempo.
4. Use logica condicional (branching) para manter o survey relevante.
5. Nao use este template para pesquisas que requerem profundidade qualitativa.

> **Dica:** Cada pergunta deve estar diretamente ligada a uma research question. Se nao esta, remova.

## Template

### 1. Research Questions

| # | Research Question                              | Tipo de dado esperado     |
|---|------------------------------------------------|---------------------------|
| 1 | [PREENCHER — pergunta de pesquisa principal]   | Quantitativo / Qualitativo |
| 2 | [PREENCHER — pergunta de pesquisa]             | Quantitativo / Qualitativo |
| 3 | [PREENCHER — pergunta de pesquisa]             | Quantitativo / Qualitativo |

### 2. Distribuicao e Amostra

**Canal de distribuicao:** [PREENCHER — in-app, email, redes sociais, painel]
**Populacao alvo:** [PREENCHER — descricao do publico]
**Amostra minima:** [PREENCHER — numero para significancia estatistica]
**Incentivo:** [PREENCHER — tipo e valor, ou nenhum]

**Criterios de inclusao:**
- [PREENCHER — criterio]
- [PREENCHER — criterio]

### 3. Introducao do Survey

> "[PREENCHER — nome da empresa/produto] gostaria de ouvir sua opiniao! Este questionario leva aproximadamente [PREENCHER — X] minutos. Suas respostas sao [PREENCHER — anonimas / confidenciais] e serao usadas para [PREENCHER — proposito]. Ao prosseguir, voce concorda com [PREENCHER — termos]."

### 4. Secao de Screener / Filtro

**Q1 — [PREENCHER — pergunta de filtro]**
- Tipo: [PREENCHER — Single choice / Multiple choice]
- Opcoes:
  - [ ] [PREENCHER — opcao A]
  - [ ] [PREENCHER — opcao B]
  - [ ] [PREENCHER — opcao C] --> [PREENCHER — logica: encerrar / pular para secao X]

**Q2 — [PREENCHER — pergunta de filtro demografico]**
- Tipo: [PREENCHER — tipo]
- Opcoes:
  - [ ] [PREENCHER]
  - [ ] [PREENCHER]

### 5. Secao Principal — [PREENCHER — tema]

**Q3 — [PREENCHER — pergunta sobre comportamento]**
- Tipo: [PREENCHER — Single choice / Scale / Open]
- Opcoes/Escala: [PREENCHER]
- Obrigatoria: [PREENCHER — Sim / Nao]
- Mapeia para RQ: [PREENCHER — numero]

**Q4 — [PREENCHER — pergunta sobre frequencia]**
- Tipo: Single choice
- Opcoes:
  - [ ] Diariamente
  - [ ] Semanalmente
  - [ ] Mensalmente
  - [ ] Raramente
  - [ ] Nunca
- Obrigatoria: [PREENCHER]
- Mapeia para RQ: [PREENCHER]

**Q5 — [PREENCHER — pergunta de satisfacao/atitude]**
- Tipo: Likert Scale (1-5)
- Escala: Discordo totalmente — Discordo — Neutro — Concordo — Concordo totalmente
- Statement: "[PREENCHER — afirmacao para avaliar]"
- Obrigatoria: [PREENCHER]
- Mapeia para RQ: [PREENCHER]

**Q6 — [PREENCHER — pergunta Likert adicional]**
- Tipo: Likert Scale (1-5)
- Statement: "[PREENCHER]"
- Mapeia para RQ: [PREENCHER]

**Q7 — [PREENCHER — pergunta de ranking]**
- Tipo: Ranking
- Itens para ordenar:
  1. [PREENCHER]
  2. [PREENCHER]
  3. [PREENCHER]
  4. [PREENCHER]
- Mapeia para RQ: [PREENCHER]

### 6. Secao Aberta

**Q8 — [PREENCHER — pergunta aberta para aprofundamento]**
- Tipo: Open text (long)
- Placeholder: "[PREENCHER — ex.: Descreva com suas palavras...]"
- Obrigatoria: Nao
- Mapeia para RQ: [PREENCHER]

**Q9 — [PREENCHER — pergunta aberta de sugestao]**
- Tipo: Open text (short)
- Obrigatoria: Nao

### 7. Secao Demografica (Opcional)

**Q10 — [PREENCHER — faixa etaria / cargo / tempo de uso]**
- Tipo: Single choice
- Opcoes: [PREENCHER]

**Q11 — [PREENCHER — outra variavel demografica]**
- Tipo: [PREENCHER]
- Opcoes: [PREENCHER]

### 8. Encerramento

> "Obrigado(a) por sua participacao! Suas respostas sao muito valiosas para [PREENCHER — proposito]. [PREENCHER — informacao sobre incentivo/sorteio, se aplicavel]. Em caso de duvidas, entre em contato: [PREENCHER — email]."

### 9. Logica Condicional (Branching)

| Condicao                              | Acao                                |
|---------------------------------------|-------------------------------------|
| Se Q1 = [PREENCHER — opcao]          | Pular para [PREENCHER — secao/Q]   |
| Se Q4 = "Nunca"                       | Pular para [PREENCHER — secao/Q]   |
| [PREENCHER — condicao]               | [PREENCHER — acao]                  |

### 10. Plano de Analise

| Research Question | Perguntas do survey | Metodo de analise                 |
|-------------------|---------------------|-----------------------------------|
| RQ1               | Q3, Q4              | [PREENCHER — frequencia, media]   |
| RQ2               | Q5, Q6              | [PREENCHER — Likert analysis]     |
| RQ3               | Q7, Q8              | [PREENCHER — ranking + coding]    |

## Example (Parcialmente Preenchido)

**Projeto:** Satisfacao com o fluxo de onboarding
**RQ1:** Qual o nivel de satisfacao dos novos usuarios com o processo de onboarding?
**Q3:** "Em uma escala de 1 a 5, o quanto voce ficou satisfeito(a) com o processo de configuracao inicial?"
**Q8:** "O que voce mudaria no processo de configuracao inicial, se pudesse?"

## Notes

- Evite perguntas duplas ("Voce achou rapido e facil?" — rapido e facil sao coisas diferentes).
- Use randomizacao de opcoes quando possivel para evitar vies de ordem.
- Teste o survey em mobile — muitos respondentes usarao o celular.
- Deixe perguntas abertas como opcionais para nao impactar taxa de conclusao.
- Monitore as primeiras 20-30 respostas para identificar problemas de interpretacao.
- Defina o plano de analise ANTES de lancar o survey, nao depois.
