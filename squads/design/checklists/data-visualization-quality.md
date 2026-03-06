# Data Visualization Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Data Design
- **Version:** 1.0.0
- **Owner Agent:** Data Visualization Agent

## Objective
Garantir que visualizacoes de dados sejam precisas, acessiveis, compreensíveis e que comuniquem insights de forma eficaz sem distorcer a informacao.
Uma boa data viz transforma dados complexos em conhecimento actionable.

## When to Apply
- Ao projetar dashboards, graficos, charts e outras representacoes visuais de dados.
- Ao revisar visualizacoes existentes para precisao e clareza.
- Ao definir o sistema visual para dados e metricas do produto.

## Criteria
- [ ] O tipo de chart ou visualizacao e adequado para o tipo de dado e a mensagem a comunicar
- [ ] Os eixos estao corretamente rotulados com unidades e escala visivel
- [ ] A escala dos eixos nao distorce ou exagera diferencas (evitar truncamento enganoso do eixo Y)
- [ ] As cores utilizadas sao distinguiveis e acessiveis para daltonicos
- [ ] Existe legenda clara quando multiplas series ou categorias sao representadas
- [ ] Os data labels e tooltips fornecem valores exatos quando necessario
- [ ] A visualizacao funciona com volumes reais de dados (nao apenas dados de exemplo)
- [ ] Os estados de dados ausentes, zerados ou negativos estao tratados
- [ ] A visualizacao e responsiva e legivel em diferentes tamanhos de tela
- [ ] As interacoes (hover, click, zoom, filter) estao definidas e sao intuitivas
- [ ] O data-ink ratio e otimizado (sem chart junk ou decoracoes desnecessarias)
- [ ] A narrativa visual guia o usuario do overview para detalhes (overview first, details on demand)
- [ ] Os numeros e valores estao formatados adequadamente (milhares, percentuais, casas decimais)
- [ ] A atualizacao em tempo real (real-time) esta tratada sem flicker ou confusao visual
- [ ] As comparacoes sao justas e contextualizadas (benchmarks, periodos anteriores)
- [ ] A fonte dos dados e a data de atualizacao estao visiveis

## Severity Guide

### Critico
- Escala de eixo distorcendo ou misrepresentando os dados.
- Tipo de visualizacao completamente inadequado para o dado apresentado.
- Cores indistinguiveis impedindo leitura por usuarios daltonicos.

### Major
- Legenda ausente em visualizacoes com multiplas categorias.
- Visualizacao nao funcional com volumes reais de dados.
- Dados ausentes ou zerados sem tratamento visual.

### Minor
- Data-ink ratio nao otimizado com elementos decorativos leves.
- Fonte dos dados nao exibida mas conhecida pelos usuarios.
- Formatacao de numeros levemente inconsistente.

## Cross-References
- [Color System Quality](color-system-quality.md)
- [Accessibility Quality](accessibility-quality.md)
- [Responsive Breakpoints Quality](responsive-breakpoints-quality.md)
- [Performance UX Quality](performance-ux-quality.md)
- [Content Design Quality](content-design-quality.md)
