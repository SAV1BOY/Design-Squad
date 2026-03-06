# Product Experiment Design

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Experimentation                |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Product Design Lead            |

## Objective

Garantir que experimentos de produto (A/B tests, feature flags, betas) sao desenhados
com rigor metodologico, hipoteses claras e metricas definidas. Experimentos bem
desenhados geram aprendizados validos que informam decisoes de design e produto
com confianca.

## When to Apply

- Ao planejar qualquer experimento A/B ou multivariate.
- Antes de lancar features em beta ou com feature flags.
- Quando ha incerteza sobre qual solucao de design gera melhor resultado.
- Em revisoes de resultados de experimentos concluidos.

## Criteria

- [ ] A hipotese do experimento esta formulada de forma clara e falsificavel.
- [ ] A variavel independente (o que muda) e a dependente (o que mede) estao definidas.
- [ ] A metrica primaria (primary metric) do experimento esta definida e instrumentada.
- [ ] Metricas guardrail (que nao devem piorar) estao definidas.
- [ ] O tamanho da amostra e a duracao do experimento sao calculados estatisticamente.
- [ ] A unidade de randomizacao (usuario, sessao, device) esta definida.
- [ ] Segmentos de exclusao (funcionarios, bots, usuarios de teste) estao configurados.
- [ ] O design visual das variantes e implementado com qualidade equivalente.
- [ ] As variantes diferem apenas na variavel sendo testada (controle de confounders).
- [ ] Existe plano de analise definido antes do inicio (nao mudar regras durante o jogo).
- [ ] Criterios de decisao (ship, iterate, kill) estao definidos antecipadamente.
- [ ] O time de dados validou a instrumentacao antes do lancamento.
- [ ] Resultados sao documentados e compartilhados independentemente do outcome.
- [ ] Aprendizados sao arquivados no repositorio de conhecimento para referencia futura.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Hipotese nao definida ou metrica primaria alterada durante o experimento. |
| Major    | Tamanho da amostra insuficiente ou variantes com qualidade desigual.     |
| Minor    | Metricas guardrail nao definidas ou resultados nao documentados.          |
| Info     | Oportunidade de melhorar processo de analise ou repositorio de learnings. |

## Cross-References

- `product/product-success-criteria.md` — Criterios de sucesso.
- `product/product-feature-design.md` — Design de features.
- `ux/ux-metrics-heart-audit.md` — Metricas HEART.
- `research/research-triangulation-quality.md` — Triangulacao de dados.
