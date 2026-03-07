# KPI Card Patterns

## Pattern Description

Padroes para cards de indicadores-chave de performance (KPIs) em dashboards. KPI cards comunicam metricas criticas de negocio de forma rapida e escaneavel.

## Examples

### Example 1: Stripe — Revenue Metrics
Stripe exibe metricas financeiras em cards limpos:
- Valor grande e proeminente (R$ 125.432,00)
- Label descritivo acima (Gross Revenue)
- Trend indicator (+12.3% vs. ultimo periodo)
- Sparkline mini-grafico no canto
- Click abre drill-down com detalhes

### Example 2: Mixpanel — Engagement Metrics
Mixpanel mostra engajamento em cards interativos:
- Numero central (DAU: 45.2K)
- Comparacao temporal selecionavel (vs. ontem, semana, mes)
- Cor do trend: verde (positivo), vermelho (negativo)
- Tooltip com breakdown por segmento no hover

### Example 3: Datadog — Infra Metrics
Datadog monitora infraestrutura com cards de status:
- Valor com unidade (CPU: 78%, Memory: 4.2GB)
- Status color-coded: verde (ok), amarelo (warn), vermelho (crit)
- Threshold lines no mini-grafico
- Alert badge quando valor excede limite

## Analysis

KPI cards eficazes:
- **Hierarquia**: valor > trend > label > contexto
- **Formatacao**: use formatacao apropriada (moeda, percentual, abreviacao)
- **Comparacao**: sempre mostre contexto temporal (vs. periodo anterior)
- **Cor com proposito**: verde/vermelho apenas para tendencia, nao decoracao
- **Drill-down**: click deve revelar mais detalhes
- **Responsive**: cards devem reflowir em grid de 2-4 colunas

## Tags

`kpi`, `metrics`, `dashboard`, `data-visualization`, `cards`, `analytics`
