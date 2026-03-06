# Kano Model

## Metadata

| Campo         | Valor                                        |
| ------------- | -------------------------------------------- |
| Categoria     | Estrategia de Produto                        |
| Complexidade  | Media                                        |
| Autor         | Design Squad                                 |
| Versao        | 1.0                                          |
| Ultima revisao| 2026-03-06                                   |
| Tags          | kano, prioritization, satisfaction, features |

## Concept

O Kano Model, criado por Noriaki Kano em 1984, e um framework para classificar features
de produto com base no seu impacto na satisfacao do usuario. O modelo revela que a relacao
entre funcionalidade e satisfacao nao e linear — algumas features encantam, outras apenas
evitam insatisfacao.

### As 5 Categorias

```
Satisfacao
    ^
    |        * Delight (Attractive)
    |       *
    |      *                   Performance (One-dimensional)
    |     *                  /
    |    *                 /
    |---*----------------/-----------> Funcionalidade
    |  *               /
    | *    __________/
    |*    /
    |    / Must-be (Basic)
    |   /
    |  /
    v
```

1. **Must-be (Basico)**: features que o usuario espera como minimo. Sua presenca nao gera
   satisfacao, mas sua ausencia gera forte insatisfacao. Ex: login funcionar, pagina carregar.

2. **Performance (Linear)**: features onde mais e melhor — satisfacao proporcional a
   implementacao. Ex: velocidade de carregamento, quantidade de storage.

3. **Delight (Atrativo)**: features inesperadas que surpreendem positivamente. Sua ausencia
   nao causa insatisfacao, mas sua presenca encanta. Ex: atalhos inteligentes, animacoes sutis.

4. **Indifferent (Indiferente)**: features que nao afetam satisfacao nem insatisfacao.
   O usuario nao se importa se existem ou nao.

5. **Reverse (Reverso)**: features que alguns usuarios ativamente nao querem.
   Sua presenca causa insatisfacao.

### Principio Central

**Satisfacao e assimetrica**: resolver um must-be nao encanta — apenas evita frustacao.
Investir apenas em delight sem cobrir must-be resulta em produto fragil.

## When to Use

- Na priorizacao de backlog de produto com muitas features competindo.
- Para decidir onde investir esforco de design com maior impacto.
- Em planejamento estrategico de roadmap.
- Para comunicar trade-offs de priorizacao com stakeholders.
- Quando o time debate se uma feature e "essencial" ou "nice to have".
- Em pesquisa de satisfacao para entender drivers de NPS/CSAT.

## How to Apply

### 1. Listar Features Candidatas

Compilar lista de features potenciais de todas as fontes:
- Backlog do produto
- Feedback de usuarios
- Pesquisa competitiva
- Ideias internas do time

### 2. Criar Questionario Kano

Para cada feature, fazer duas perguntas (funcional e disfuncional):

```
Funcional:  "Se o produto tivesse [feature], como voce se sentiria?"
Disfuncional: "Se o produto NAO tivesse [feature], como voce se sentiria?"

Opcoes de resposta (para ambas):
  1. Eu gostaria disso
  2. Eu espero que tenha isso
  3. Sou neutro
  4. Posso tolerar isso
  5. Nao gostaria disso
```

### 3. Tabela de Classificacao

Cruzar respostas funcional x disfuncional na evaluation table:

```
                    Disfuncional
                    Gosto  Espero Neutro Tolero Nao gosto
Funcional  Gosto    Q      A      A      A      O
           Espero   R      I      I      I      M
           Neutro   R      I      I      I      M
           Tolero   R      I      I      I      M
           Nao gosto R     R      R      R      Q

A = Attractive (Delight)    M = Must-be
O = One-dimensional (Perf)  I = Indifferent
R = Reverse                 Q = Questionable
```

### 4. Agregar Resultados

Para cada feature, contar quantos respondentes a classificaram em cada categoria.
A categoria com mais votos define a classificacao da feature.

```
Feature "Dark mode":
  Must-be: 3  |  Performance: 2  |  Attractive: 12  |  Indifferent: 8  |  Reverse: 0
  Classificacao: Attractive (Delight) — 48% dos respondentes
```

### 5. Priorizar com Base na Classificacao

```
Prioridade 1: Must-be    — Resolver primeiro (evitar insatisfacao)
Prioridade 2: Performance — Investir para competir (diferencial linear)
Prioridade 3: Delight     — Surpreender e encantar (diferencial exponencial)
Ignorar:      Indifferent — Nao investir
Remover:      Reverse     — Considerar tornar opcional ou eliminar
```

## Key Principles

- **Must-be first**: nunca investir em delight antes de cobrir todos os must-be.
- **Decaimento temporal**: delight de hoje vira must-be de amanha (expectativas evoluem).
- **Segmentacao importa**: personas diferentes classificam features diferentemente.
- **Dados quantitativos**: classificacao vem de pesquisa, nao de intuicao do time.
- **Equilibrio de portfolio**: roadmap saudavel tem mix de must-be, performance e delight.
- **Contexto competitivo**: o que e delight no seu produto pode ser must-be no concorrente.

## Examples

### Classificacao para App de E-commerce

```
Must-be:     Busca, carrinho, pagamento seguro, rastreamento de pedido
Performance: Velocidade, metodos de pagamento, filtros, qualidade de fotos
Delight:     Recomendacoes personalizadas, AR, alerta de queda de preco, 1-click checkout
Indifferent: Mudar cor do tema, compartilhar wishlist no Facebook
```

### Decaimento Temporal

```
2020: Frete gratis = Delight -> 2022: Performance -> 2024: Must-be
Implicacao: reavaliar classificacao periodicamente (anual)
```

## Common Pitfalls

| Erro                                | Consequencia                        | Correcao                                |
| ----------------------------------- | ----------------------------------- | --------------------------------------- |
| Classificar por intuicao            | Bias do time, nao do usuario        | Sempre basear em pesquisa Kano formal   |
| Ignorar must-be para focar em delight| Produto fragil e frustrante        | Must-be primeiro, delight depois        |
| Nao reavaliar ao longo do tempo     | Classificacoes desatualizadas       | Reavaliar anualmente                    |
| Tratar todas as personas como uma   | Media esconde diferencias           | Segmentar resultados por persona        |
| Amostra pequena demais              | Classificacao estatisticamente fraca| Minimo 20-30 respondentes por segmento  |
| Perguntas mal traduzidas            | Respostas confusas                  | Validar questionario com piloto         |

## Cross-References

- [Lean UX Framework](./lean-ux-framework.md) — usar Kano para priorizar hipoteses.
- [Sprint Design Framework](./sprint-design-framework.md) — Kano antes do sprint para foco.
- [SUS System Usability Scale](./sus-system-usability-scale.md) — correlacionar SUS com categorias Kano.
- [Design Maturity Model](./design-maturity-model.md) — pesquisa Kano como pratica de nivel 3+.
- [Design Review and Critique](./design-review-and-critique.md) — usar Kano como criterio de review.
