# Lean UX Framework

## Metadata

| Campo         | Valor                                         |
| ------------- | --------------------------------------------- |
| Categoria     | Metodologia                                   |
| Complexidade  | Media                                         |
| Autor         | Design Squad                                  |
| Versao        | 1.0                                           |
| Ultima revisao| 2026-03-06                                    |
| Tags          | lean-ux, hypothesis, mvp, validated-learning  |

## Concept

Lean UX e uma abordagem de design que integra principios de Lean Startup e Agile para
reduzir desperdicio no processo de design. Em vez de deliverables pesados e especificacoes
exaustivas, o foco esta em aprendizado rapido por meio de hipoteses, experimentacao e
validacao com usuarios reais.

### O Ciclo Lean UX

```
Think  ->  Make  ->  Check
  |          |          |
Hipotese   MVP      Aprendizado
  |          |      Validado
  +----------+----------+
         (Repetir)
```

1. **Think (Hipotese)**: declarar crencas sobre o usuario, o problema e a solucao.
2. **Make (MVP)**: construir o minimo necessario para testar a hipotese.
3. **Check (Aprendizado Validado)**: medir resultados e decidir pivotar ou perseverar.

### Hipotese Lean UX

Formato padrao:

```
Acreditamos que [resultado esperado]
para [persona/segmento]
se [mudanca/feature/intervencao].

Saberemos que estamos certos quando [metrica observavel]
atingir [threshold de sucesso].
```

## When to Use

- Em fases iniciais de produto onde ha alta incerteza sobre problema e solucao.
- Quando o time esta preso em ciclos longos de design sem validacao.
- Em ambientes ageis onde design precisa se integrar a sprints curtas.
- Quando ha pressao para entregar rapido sem sacrificar qualidade de decisao.
- Para alinhar stakeholders em torno de outcomes em vez de outputs.

## How to Apply

### 1. Declarar Hipoteses

Listar as suposicoes mais arriscadas do projeto e transforma-las em hipoteses testaveis.

**Tecnica: Assumption Mapping**

```
          Alta certeza
               |
  Importante --+-- Nao importante
               |
          Baixa certeza

Priorizar: Alta importancia + Baixa certeza = testar primeiro
```

### 2. Definir MVP (Minimum Viable Product/Prototype)

O MVP nao e o produto final — e o menor artefato que permite testar a hipotese.

| Tipo de MVP              | Fidelidade | Tempo      | Quando usar                    |
| ------------------------ | ---------- | ---------- | ------------------------------ |
| Paper prototype          | Baixa      | Horas      | Testar fluxo e conceito        |
| Clickable prototype      | Media      | 1-2 dias   | Testar interacao e usabilidade |
| Wizard of Oz             | Alta       | 2-3 dias   | Simular backend manualmente    |
| Concierge MVP            | Alta       | 1 semana   | Testar proposta de valor       |
| Feature flag             | Alta       | 1-2 sprints| Testar com usuarios reais      |
| A/B test                 | Alta       | 2-4 semanas| Validar impacto em escala      |

### 3. Definir Metricas de Sucesso

Cada hipotese precisa de uma metrica observavel e um threshold.

```
Hipotese: Onboarding simplificado aumenta ativacao
Metrica:  Taxa de conclusao do onboarding
Baseline: 34%
Threshold: 50% (meta minima para validar)
Prazo:    2 semanas apos lancamento
```

### 4. Executar Experimento

- Recrutar participantes (minimo 5 para testes qualitativos).
- Definir roteiro de teste alinhado a hipotese.
- Observar sem interferir.
- Documentar comportamentos, citacoes e metricas.

### 5. Sintetizar e Decidir

```
Resultados possiveis:
  Validada:  metrica atingiu threshold -> implementar e iterar
  Invalidada: metrica abaixo do threshold -> pivotar abordagem
  Inconclusiva: dados insuficientes -> ajustar experimento e repetir
```

## Key Principles

- **Outcomes over outputs**: medir sucesso por impacto no usuario, nao por entregas.
- **Aprendizado rapido**: ciclos curtos de hipotese-teste-aprendizado.
- **Trabalho colaborativo**: design, produto e engenharia juntos desde o inicio.
- **Minimo desperdicio**: nao produzir mais do que o necessario para aprender.
- **Humildade epistemica**: assumir que nao sabemos ate que os dados confirmem.
- **Transparencia de risco**: tornar suposicoes explicitas e visiveis para todos.
- **Iteracao continua**: nenhuma solucao e final — tudo pode ser melhorado com dados.

## Examples

### Hipotese de Onboarding

```
Acreditamos que a taxa de ativacao vai aumentar de 34% para 50%
para novos usuarios do plano free
se reduzirmos o onboarding de 8 etapas para 3 etapas.

Saberemos que estamos certos quando a taxa de conclusao do onboarding
atingir 50% em 14 dias apos o lancamento do teste A/B.
```

### Assumption Map — E-commerce

```
Alta importancia + Baixa certeza (testar primeiro):
  - "Usuarios preferem filtro por categoria a busca por texto"
  - "Frete gratis acima de R$99 aumenta ticket medio"

Alta importancia + Alta certeza (monitorar):
  - "Usuarios abandonam carrinho se frete for caro"

Baixa importancia (ignorar por enquanto):
  - "Usuarios querem wishlist compartilhavel"
```

### Ciclo Completo — Feature de Favoritos

```
Sprint 1: Hipotese + paper prototype + 5 testes de usabilidade
Sprint 2: Clickable prototype + refinamento baseado em feedback
Sprint 3: Feature flag para 10% dos usuarios + metricas
Sprint 4: Analise de resultados -> decisao de rollout ou pivot
```

## Common Pitfalls

| Erro                                 | Consequencia                       | Correcao                                |
| ------------------------------------ | ---------------------------------- | --------------------------------------- |
| Hipotese vaga sem metrica            | Impossivel validar ou invalidar    | Sempre incluir metrica e threshold      |
| MVP grande demais                    | Ciclo lento, desperdicio           | Perguntar "o que posso cortar?"         |
| Bias de confirmacao                  | Ignorar dados que contradizem      | Definir criterios de sucesso antes      |
| Pular a fase de sintese             | Aprendizado nao se converte em acao| Ritual obrigatorio de sintese pos-teste |
| Stakeholder quer certeza, nao teste  | Resistencia ao processo            | Mostrar custo de nao validar            |
| Testar com colegas, nao com usuarios | Feedback enviesado                 | Recrutar usuarios reais, sempre         |

## Cross-References

- [Sprint Design Framework](./sprint-design-framework.md) — design sprint como formato intensivo de Lean UX.
- [Design Review and Critique](./design-review-and-critique.md) — critique para refinar hipoteses.
- [SUS System Usability Scale](./sus-system-usability-scale.md) — metrica de usabilidade para validacao.
- [Kano Model](./kano-model.md) — priorizar features por tipo de satisfacao.
- [Design Maturity Model](./design-maturity-model.md) — Lean UX como pratica de maturidade avancada.
