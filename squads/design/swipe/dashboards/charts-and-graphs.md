# Charts and Graphs Patterns

## Pattern Description

Padroes para visualizacao de dados com graficos em dashboards. Cada tipo de grafico tem um proposito especifico — escolher o tipo certo e tao importante quanto o design visual.

## Examples

### Example 1: Stripe — Line Charts for Trends
Stripe usa line charts para tendencias temporais:
- Linha principal com area preenchida (gradiente sutil)
- Tooltip rico no hover com breakdown
- Comparison line (periodo anterior) em cor secundaria
- Eixo Y com formatacao de moeda
- Periodo selecionavel: 1D, 1W, 1M, 3M, 1Y

### Example 2: Mixpanel — Funnel Visualization
Mixpanel visualiza funis de conversao:
- Barras horizontais decrescentes
- Percentual de conversao entre cada step
- Cor gradativa do verde (inicio) ao laranja (final)
- Hover mostra numeros absolutos e percentuais
- Breakdown por segmento em hover/click

### Example 3: Figma — Donut Charts for Composition
Figma Analytics usa donut charts para composicao:
- Distribuicao de component usage por tipo
- Legenda interativa (click filtra)
- Valor central mostra total ou metrica-chave
- Animacao de entrada suave
- Cores acessiveis (distintas em grayscale)

## Analysis

Graficos eficazes:
- **Tipo certo**: line (tendencia), bar (comparacao), pie (composicao), scatter (correlacao)
- **Dados primeiro**: minimize decoracao, maximize data-ink ratio
- **Interatividade**: tooltips, zoom, filter por legenda
- **A11y**: cores distintas em daltonismo, patterns alem de cor, keyboard nav
- **Responsivo**: simplifique em telas pequenas (menos data points, labels)
- **Empty state**: mostre mensagem util quando nao ha dados

## Tags

`charts`, `data-visualization`, `dashboard`, `line-chart`, `bar-chart`, `a11y`
