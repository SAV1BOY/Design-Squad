# Quarterly Design Metrics

## Title
Script de geração do relatório trimestral de métricas de design.

## Purpose

Consolidar métricas de impacto, qualidade e eficiência do Design Squad em
relatório trimestral para liderança. O relatório conecta o trabalho de design
a resultados de negócio, demonstrando ROI do investimento em design.

Este é o documento mais importante para justificar recursos, headcount e
investimentos em ferramentas e processos de design.

## Prerequisites

- **Node.js** >= 18.0
- **Jira/Linear API** para métricas de produtividade
- **Analytics API** (GA, Amplitude, Mixpanel) para métricas de produto
- **Figma API** para métricas de design system
- **axe-core results** para métricas de acessibilidade
- **NPS/Survey data** para métricas de satisfação

Variáveis:
```bash
export JIRA_API_TOKEN="xxxx"
export ANALYTICS_API_KEY="xxxx"
export FIGMA_API_TOKEN="figd_xxxxx"
export QUARTER="Q1-2026"
export QUARTER_START="2026-01-01"
export QUARTER_END="2026-03-31"
```

## Steps

### 1. Extrair métricas de produtividade

```bash
# Métricas do Jira/Linear
node scripts/extract-quarterly-jira.js \
  --project DESIGN \
  --start $QUARTER_START \
  --end $QUARTER_END \
  --output quarterly/data/productivity-$QUARTER.json

# Métricas extraídas:
# - Total de tickets concluídos
# - Story points entregues
# - Lead time médio
# - Rework rate
# - Features entregues por squad
```

### 2. Extrair métricas de design system

```bash
# Adoption e health do DS
node scripts/extract-ds-metrics.js \
  --start $QUARTER_START \
  --end $QUARTER_END \
  --output quarterly/data/ds-$QUARTER.json

# Métricas extraídas:
# - Adoption rate (% de telas usando DS)
# - Componentes totais (stable, beta, deprecated)
# - Token coverage
# - Releases no quarter
# - Contributors
```

### 3. Extrair métricas de acessibilidade

```bash
# Compliance WCAG e progresso
node scripts/extract-a11y-metrics.js \
  --reports-dir audit-results/ \
  --start $QUARTER_START \
  --end $QUARTER_END \
  --output quarterly/data/a11y-$QUARTER.json

# Métricas extraídas:
# - Compliance score (início vs. fim do quarter)
# - Issues por severidade
# - Issues resolvidos vs. novos
# - Fluxos com navegação por teclado completa
```

### 4. Extrair métricas de impacto no produto

```bash
# Métricas de produto influenciadas por design
node scripts/extract-product-impact.js \
  --analytics-source "amplitude" \
  --features quarterly/data/features-list-$QUARTER.json \
  --start $QUARTER_START \
  --end $QUARTER_END \
  --output quarterly/data/impact-$QUARTER.json

# Métricas extraídas:
# - Task completion rate (antes/depois de redesigns)
# - Conversion rate (para features de conversão)
# - NPS por fluxo
# - Support tickets por área de UX
# - Time-to-value para novos usuários
```

### 5. Extrair métricas de pesquisa

```bash
# Pesquisa realizada no quarter
node scripts/extract-research-metrics.js \
  --start $QUARTER_START \
  --end $QUARTER_END \
  --output quarterly/data/research-$QUARTER.json

# Métricas extraídas:
# - Estudos realizados
# - Participantes
# - Insights gerados
# - Features com input de pesquisa (%)
# - Diversidade de participantes
```

### 6. Consolidar e gerar relatório

```bash
# Consolidar todas as fontes
node scripts/consolidate-quarterly.js \
  --data-dir quarterly/data/ \
  --quarter $QUARTER \
  --output quarterly/data/consolidated-$QUARTER.json

# Gerar relatório executivo
node scripts/generate-quarterly-report.js \
  --input quarterly/data/consolidated-$QUARTER.json \
  --template templates/quarterly-report.md \
  --format md \
  --output quarterly/reports/$QUARTER-report.md

# Gerar deck de apresentação (markdown → slides)
node scripts/generate-quarterly-report.js \
  --input quarterly/data/consolidated-$QUARTER.json \
  --format slides \
  --output quarterly/reports/$QUARTER-deck.md
```

## Expected Output

```markdown
# Design Squad — Quarterly Report — Q1 2026

## Executive Summary
O Design Squad entregou [N] features em [M] squads, contribuindo para
melhoria de [X]% na conversão de checkout e [Y] pontos no NPS. A adoção
do design system atingiu [Z]% e a conformidade WCAG subiu para [W]%.

## Impact Metrics

| Métrica | Q4 2025 | Q1 2026 | Delta | Target |
|---------|---------|---------|-------|--------|
| Checkout Conversion | 3.2% | 3.8% | +18.7% | 4.0% |
| NPS — Onboarding | 23 | 31 | +8 pts | 35 |
| Support Tickets (UX) | 340/mo | 248/mo | -27% | < 200 |
| Time-to-Value | 7 days | 4.2 days | -40% | 3 days |

## Productivity Metrics

| Métrica | Q4 2025 | Q1 2026 | Delta |
|---------|---------|---------|-------|
| Features entregues | 12 | 18 | +50% |
| Lead time médio | 6.2 days | 4.8 days | -22% |
| Rework rate | 12% | 7% | -42% |
| Story points | 89 | 112 | +26% |

## Design System

| Métrica | Q4 2025 | Q1 2026 | Target |
|---------|---------|---------|--------|
| Adoption rate | 78% | 87% | > 85% |
| Components (stable) | 52 | 58 | — |
| Releases | 4 | 6 | — |
| Contributors | 5 | 8 | — |

## Accessibility

| Métrica | Q4 2025 | Q1 2026 | Target |
|---------|---------|---------|--------|
| WCAG AA Compliance | 62% | 78% | 80% |
| Critical issues | 8 | 2 | 0 |
| Keyboard nav coverage | 70% | 95% | 100% |

## Research

| Métrica | Q1 2026 |
|---------|---------|
| Estudos realizados | 6 |
| Participantes | 48 |
| Features com research | 67% |

## Q2 2026 Priorities
1. Atingir 80% WCAG AA compliance
2. Lançar dark mode (beta)
3. Reduzir support tickets para < 200/mês
4. Aumentar DS adoption para > 90%
```

## Automation Notes

- **Frequência:** Trimestral (primeira semana do quarter seguinte)
- **Preparação:** Dados extraídos automaticamente, relatório revisado manualmente
- **Apresentação:** Design Lead apresenta para VP+ na segunda semana do quarter
- **Archive:** Todos os reports archivados para análise de tendência multi-quarter
- **Benchmark:** Comparar com quarters anteriores e com benchmarks do setor
- **Distribution:** Liderança (email), Design Squad (Slack), Org (wiki)
