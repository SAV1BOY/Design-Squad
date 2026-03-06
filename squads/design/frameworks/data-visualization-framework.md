# Data Visualization Framework

## Metadata
- **Autor**: Design Squad
- **Categoria**: Data Visualization, UI, Acessibilidade
- **Complexidade**: Media-Alta
- **Aplicacao**: Principios, tipos de graficos, acessibilidade e guidelines de data viz
- **Ultima atualizacao**: 2026-03-06

## Concept

O Data Visualization Framework define principios, taxonomia e guidelines para representar
dados de forma clara, honesta e acessivel. Data visualization nao e "fazer graficos bonitos" —
e comunicar insights de dados de forma que o usuario entenda rapidamente e tome decisoes
informadas.

A premissa central e que todo grafico conta uma historia, e o designer e responsavel por
garantir que a historia seja verdadeira, clara e acessivel. Graficos enganosos, confusos
ou inacessiveis sao falhas de design tao graves quanto interfaces inutilizaveis.

O framework cobre tres dimensoes: principios de comunicacao visual de dados, taxonomia de
tipos de grafico com recomendacoes de uso, e requisitos de acessibilidade especificos
para data visualization.

## When to Use

- Quando o produto precisa exibir dados quantitativos para usuarios
- Quando se projeta dashboards, relatorios ou analytics
- Quando se quer padronizar como dados sao representados no produto
- Quando graficos existentes sao confusos ou enganosos
- Quando se precisa garantir acessibilidade em visualizacoes de dados
- Quando se adiciona data viz ao design system

## How to Apply

### Principios de Data Visualization
1. **Clareza sobre estetica**: O grafico mais simples que comunica o insight e o melhor
2. **Honestidade**: Eixos sempre comecam em zero para bar charts. Escalas consistentes
3. **Hierarquia de informacao**: Destaque o insight principal, detalhe sob demanda
4. **Contexto**: Numeros sem contexto nao tem significado. Compare com benchmarks,
   periodos anteriores, metas
5. **Anotacoes**: Use labels, legendas e anotacoes para guiar interpretacao
6. **Responsividade**: Graficos devem funcionar em mobile (simplificados se necessario)
7. **Interatividade com proposito**: Tooltips e drill-down adicionam valor, animacoes
   decorativas nao

### Taxonomia de Tipos de Grafico
**Comparacao**:
- Bar chart (horizontal): Comparar categorias por valor
- Column chart (vertical): Comparar categorias ao longo do tempo
- Grouped bar: Comparar sub-categorias
- Radar/spider: Comparar multiplas dimensoes simultaneamente

**Tendencia**:
- Line chart: Mostrar mudanca ao longo do tempo (serie continua)
- Area chart: Line chart com enfase no volume total
- Sparkline: Tendencia minima embutida em texto ou tabela

**Composicao**:
- Pie/donut chart: Proporcoes de um todo (max 5-6 fatias)
- Stacked bar: Composicao comparada entre categorias
- Treemap: Hierarquia proporcional

**Distribuicao**:
- Histogram: Distribuicao de frequencia
- Box plot: Distribuicao estatistica (quartis, outliers)
- Scatter plot: Relacao entre duas variaveis

**Relacao**:
- Scatter plot: Correlacao entre variaveis
- Bubble chart: Scatter com terceira dimensao (tamanho)
- Heatmap: Intensidade em duas dimensoes

### Selecao de Tipo
| Pergunta             | Tipo Recomendado       |
|----------------------|------------------------|
| Quanto?              | Bar chart              |
| Como mudou?          | Line chart             |
| Que proporcao?       | Donut chart            |
| Existe correlacao?   | Scatter plot           |
| Como se distribui?   | Histogram              |
| Qual a composicao?   | Stacked bar / treemap  |

### Acessibilidade em Data Viz
1. **Nao dependa apenas de cor**: Use patterns, shapes e labels alem de cor
2. **Contraste**: Todas as cores de dados com contraste 3:1 contra fundo
3. **Alt text**: Cada grafico com descricao textual do insight principal
4. **Data table**: Forneca tabela de dados como alternativa ao grafico
5. **Keyboard access**: Tooltips e interacoes acessiveis via teclado
6. **Screen reader**: Anuncie mudancas em graficos dinamicos
7. **Color blindness**: Teste com simuladores de daltonismo (protanopia, deuteranopia)

### Guidelines de Implementacao
1. Defina paleta de cores para data viz no design system (6-8 cores distintas)
2. Padronize tamanhos de tipografia para labels, eixos, titulos
3. Defina comportamento responsivo: simplificar, nao apenas reduzir
4. Padronize tooltips: formato, timing, posicao
5. Defina empty states para graficos sem dados
6. Defina loading states (skeleton ou placeholder)

## Key Principles

- **Menos e mais**: Remova chartjunk (elementos decorativos sem informacao)
- **Honestidade visual**: Escala, baseline e proporcoes devem ser honestas
- **Contexto da decisao**: O grafico deve ajudar o usuario a tomar uma decisao
- **Acessivel por padrao**: Data viz inacessivel exclui usuarios
- **Consistencia no sistema**: Todos os graficos seguem mesma linguagem visual
- **Interatividade sob demanda**: Overview first, details on demand
- **Mobile-ready**: Graficos precisam funcionar em telas pequenas

## Examples

### Exemplo 1 — Dashboard KPIs
Design de dashboard com 4 KPIs e 2 graficos:
- KPI cards: Numero grande + tendencia (sparkline) + comparacao com meta
- Line chart: Receita mensal dos ultimos 12 meses com anotacao de eventos
- Bar chart: Top 5 produtos por receita com benchmark do quarter anterior
Cada grafico com alt text descrevendo o insight e data table como fallback.

### Exemplo 2 — Paleta de Data Viz
Paleta distinta da paleta de UI, otimizada para distinguibilidade:
- 6 cores sequenciais (tons de azul para intensidade)
- 6 cores categoricas (cores distintas para categorias)
- 3 cores semanticas (verde=positivo, vermelho=negativo, amarelo=neutro)
Todas testadas para contraste 3:1 e distinguiveis em protanopia/deuteranopia.

### Exemplo 3 — Grafico Responsivo
Desktop: Line chart completo com 12 meses, tooltips, legend
Tablet: Line chart com 6 meses, legend simplificada
Mobile: Sparkline com valor atual + tendencia (seta up/down)
Fallback: Data table com valores e formatacao condicional por cor

## Common Pitfalls

- **Pie chart para tudo**: Pie charts so funcionam com poucas categorias (max 6).
  Para comparacao precisa, bar charts sao melhores
- **3D charts**: Adicionar perspectiva 3D distorce proporcoes. Nunca use 3D
- **Dual Y-axis**: Dois eixos Y em escalas diferentes criam correlacoes ilusorias
- **Truncar eixo Y**: Bar charts com eixo Y nao comecando em zero exageram diferencas
- **Cores demais**: Mais de 6-7 cores em um grafico e indistinguivel
- **Sem data table**: Graficos sem alternativa textual sao inacessiveis
- **Animacoes longas**: Transicoes de grafico maiores que 500ms sao irritantes

## Cross-References

- [ui-layer.md](ui-layer.md) — Data viz como parte do sistema visual
- [design-system-layer.md](design-system-layer.md) — Componentes de data viz no DS
- [accessibility-by-default.md](accessibility-by-default.md) — A11y em data viz
- [design-token-architecture.md](design-token-architecture.md) — Tokens de cor para data viz
- [measurement-layer.md](measurement-layer.md) — Dashboards que usam data viz
- [component-spec-framework.md](component-spec-framework.md) — Spec de componentes de grafico
