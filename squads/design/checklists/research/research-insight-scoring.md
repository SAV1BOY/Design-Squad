# Research Insight Scoring

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Research Analysis              |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Research Lead                  |

## Objective

Garantir que insights de pesquisa sao avaliados e priorizados de forma sistematica,
utilizando criterios claros de pontuacao que considerem impacto, confianca, frequencia
e acionabilidade. Scoring estruturado previne vieses de recencia ou saliencia e
assegura que os insights mais importantes sao priorizados.

## When to Apply

- Apos a fase de sintese de cada rodada de pesquisa.
- Ao priorizar insights para inclusao no backlog de produto.
- Quando ha mais insights do que capacidade de acao e priorizacao e necessaria.
- Em revisoes de qualidade do repositorio de insights.

## Criteria

- [ ] Cada insight possui score de impacto (quao relevante e para o usuario e o negocio).
- [ ] Cada insight possui score de confianca (qualidade e volume das evidencias).
- [ ] Cada insight possui score de frequencia (quantos participantes reportaram o mesmo).
- [ ] Cada insight possui score de acionabilidade (quao viavel e agir sobre ele).
- [ ] A escala de scoring esta definida e documentada (ex.: 1-5 para cada criterio).
- [ ] O scoring e realizado por pelo menos 2 pesquisadores para reduzir vieses.
- [ ] Insights com scores divergentes entre avaliadores sao discutidos e calibrados.
- [ ] O score final pondera os criterios com pesos definidos pela equipe.
- [ ] Insights de alta prioridade possuem recomendacao de acao especifica.
- [ ] Insights de baixa prioridade sao arquivados com justificativa, nao descartados.
- [ ] O scoring e revisado quando novas evidencias sao adicionadas ao insight.
- [ ] Existe visualizacao (matrix ou dashboard) que facilita priorizacao pelo time.
- [ ] Insights priorizados sao traduzidos em backlog items com referencia a evidencia.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Insights priorizados sem criterio definido ou apenas por opiniao.         |
| Major    | Scoring feito por apenas 1 pessoa ou sem considerar acionabilidade.      |
| Minor    | Visualizacao de priorizacao ausente ou insights arquivados sem justificativa.|
| Info     | Oportunidade de automatizar scoring ou melhorar calibracao entre avaliadores.|

## Cross-References

- `malouf/malouf-research-synthesis-standards.md` — Padroes de sintese.
- `research/research-triangulation-quality.md` — Triangulacao de dados.
- `research/research-repository-hygiene.md` — Higiene do repositorio.
- `product/product-roadmap-alignment.md` — Alinhamento de roadmap.
