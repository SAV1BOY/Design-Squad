# SUS — System Usability Scale

## Metadata

| Campo         | Valor                                        |
| ------------- | -------------------------------------------- |
| Categoria     | Metricas                                     |
| Complexidade  | Baixa                                        |
| Autor         | Design Squad                                 |
| Versao        | 1.0                                          |
| Ultima revisao| 2026-03-06                                   |
| Tags          | sus, usability, metrics, benchmark, scoring  |

## Concept

O System Usability Scale (SUS) e um questionario padronizado de 10 perguntas criado por
John Brooke em 1986 para avaliar a usabilidade percebida de um sistema. E a metrica de
usabilidade mais utilizada no mundo por ser rapida de aplicar, confiavel estatisticamente
e comparavel entre produtos.

### As 10 Perguntas

Cada pergunta e respondida em escala Likert de 1 (discordo totalmente) a 5 (concordo totalmente).

```
1. Eu acho que gostaria de usar este sistema com frequencia.
2. Eu achei o sistema desnecessariamente complexo.
3. Eu achei o sistema facil de usar.
4. Eu acho que precisaria de apoio tecnico para usar este sistema.
5. Eu achei as funcoes do sistema bem integradas.
6. Eu achei que havia muita inconsistencia neste sistema.
7. Eu imagino que a maioria das pessoas aprenderia a usar este sistema rapidamente.
8. Eu achei o sistema muito complicado de usar.
9. Eu me senti confiante ao usar o sistema.
10. Eu precisei aprender muitas coisas antes de conseguir usar o sistema.
```

Nota: perguntas impares sao positivas, pares sao negativas (invertidas).

### Scoring

```
Para perguntas impares (1, 3, 5, 7, 9): contribuicao = resposta - 1
Para perguntas pares (2, 4, 6, 8, 10):  contribuicao = 5 - resposta
Score SUS = soma das contribuicoes x 2.5
Range: 0 a 100 (nao e porcentagem!)
```

### Interpretacao

| Score     | Grade | Adjetivo     | Percentil   |
| --------- | ----- | ------------ | ----------- |
| 90-100    | A+    | Excelente    | Top 5%      |
| 80-89     | A     | Muito bom    | Top 10%     |
| 68-79     | B     | Bom          | Acima media |
| 60-67     | C     | OK           | Media       |
| 50-59     | D     | Abaixo media | Abaixo media|
| < 50      | F     | Inaceitavel  | Problematico|

**Benchmark global: 68 pontos** — a media de milhares de avaliacoes SUS.

## When to Use

- Apos testes de usabilidade (ao final da sessao).
- Em avaliacoes periodicas do produto (trimestral).
- Para comparar versoes antes/depois de um redesign.
- Para benchmark contra concorrentes ou standards do setor.
- Como metrica de acompanhamento em roadmaps de UX.
- Quando precisar de uma metrica rapida e padronizada de usabilidade.

## How to Apply

### 1. Aplicacao

1. **Momento**: aplicar imediatamente apos o usuario interagir com o sistema.
2. **Formato**: questionario digital (Google Forms, Typeform, ou in-product).
3. **Instrucao**: "Por favor, avalie sua experiencia com o sistema que acabou de usar."
4. **Sem explicacao das perguntas**: o usuario deve responder por percepcao imediata.
5. **Anonimo**: garantir anonimato para respostas honestas.

### 2. Calculo do Score

```
Exemplo de respostas: [4, 2, 5, 1, 4, 2, 5, 1, 4, 2]

Impares: (4-1) + (5-1) + (4-1) + (5-1) + (4-1) = 3+4+3+4+3 = 17
Pares:   (5-2) + (5-1) + (5-2) + (5-1) + (5-2) = 3+4+3+4+3 = 17
Total:   (17 + 17) x 2.5 = 85.0

Score SUS: 85.0 (Grade A — Muito bom)
```

### 3. Amostra Minima

- **12-14 participantes** para confianca estatistica razoavel.
- **20+ participantes** para resultados robustos.
- Para comparacoes entre versoes, usar mesma amostra ou amostras pareadas.

### 4. Analise de Resultados

- Calcular media e desvio padrao do grupo.
- Comparar com benchmark de 68 pontos.
- Segmentar por persona, experiencia ou cenario de uso.
- Acompanhar evolucao ao longo do tempo (tendencia trimestral).

### 5. Complementar com Dados Qualitativos

O SUS indica **o que** o usuario sente, nao **por que**. Sempre complementar com:
- Pergunta aberta: "O que voce mudaria neste sistema?"
- Observacao de tarefas durante testes de usabilidade.
- Analise de perguntas individuais para diagnosticar areas especificas.

## Key Principles

- **Padronizado**: nao alterar as perguntas — a validade depende da formulacao original.
- **Rapido**: 10 perguntas, menos de 2 minutos para responder.
- **Comparavel**: scores podem ser comparados entre produtos e ao longo do tempo.
- **Complementar**: SUS mede percepcao — combinar com metricas comportamentais.
- **Nao e porcentagem**: score 68 nao significa "68% usavel" — e um indice comparativo.
- **Contexto importa**: o mesmo sistema pode ter scores diferentes em tarefas diferentes.

## Examples

### Comparacao Pre/Pos Redesign

```
Antes do redesign:
  N = 25 participantes
  Media SUS: 54.2 (Grade D — Abaixo media)
  Desvio padrao: 12.3

Depois do redesign:
  N = 25 participantes
  Media SUS: 76.8 (Grade B — Bom)
  Desvio padrao: 9.1

Melhoria: +22.6 pontos (estatisticamente significativo, p < 0.01)
```

### Dashboard Trimestral de UX Metrics

```
Q1 2026: SUS 62 | Task success 71% | Time on task 4.2min
Q2 2026: SUS 68 | Task success 78% | Time on task 3.5min
Q3 2026: SUS 74 | Task success 82% | Time on task 3.1min
Q4 2026: SUS ??  | Meta: 78+
```

### Analise por Pergunta Individual

```
Perguntas com score baixo indicam areas de foco:
  Q2 (complexidade): 2.1/5 -> sistema percebido como complexo
  Q4 (apoio tecnico): 2.3/5 -> usuarios sentem necessidade de suporte
  Acao: investir em onboarding e progressive disclosure
```

## Common Pitfalls

| Erro                                | Consequencia                        | Correcao                                |
| ----------------------------------- | ----------------------------------- | --------------------------------------- |
| Alterar perguntas do SUS            | Invalida a comparabilidade          | Usar as 10 perguntas originais          |
| Amostra muito pequena (<8)         | Resultados nao confiaveis           | Minimo 12 participantes                 |
| Aplicar sem contexto de uso         | Respostas abstratas e imprecisas    | Aplicar logo apos interacao real        |
| Tratar como porcentagem             | Interpretacao errada                | Usar a tabela de grades como referencia |
| Usar SUS isoladamente               | Sabe o que mas nao o por que        | Complementar com dados qualitativos     |
| Nao acompanhar ao longo do tempo    | Perde a tendencia de evolucao       | Aplicar trimestralmente                 |

## Cross-References

- [Design Review and Critique](./design-review-and-critique.md) — usar SUS como input na critique.
- [Lean UX Framework](./lean-ux-framework.md) — SUS como metrica de validacao de hipotese.
- [Design Maturity Model](./design-maturity-model.md) — metricas de UX como indicador de maturidade.
- [Sprint Design Framework](./sprint-design-framework.md) — SUS pos-teste de design sprint.
- [Kano Model](./kano-model.md) — correlacionar SUS com satisfacao por feature.
