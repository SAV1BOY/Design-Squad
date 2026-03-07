# Weekly Design Report

## Title
Script de geração automatizada do relatório semanal de design.

## Purpose

Gerar automaticamente o relatório semanal do Design Squad consolidando: entregas
da semana, status de trabalho em andamento, métricas de produtividade, bloqueios
e destaques. Reduz o tempo manual de preparação do report de ~1h para ~10min
(review e ajustes).

## Prerequisites

- **Node.js** >= 18.0
- **Jira/Linear API token** para extrair tickets de design
- **Figma API token** para contar entregas de design
- **Slack API token** (opcional) para postar relatório automaticamente

Variáveis:
```bash
export JIRA_API_TOKEN="xxxx"
export JIRA_BASE_URL="https://empresa.atlassian.net"
export JIRA_PROJECT="DESIGN"
export FIGMA_API_TOKEN="figd_xxxxx"
export SLACK_WEBHOOK_URL="https://hooks.slack.com/xxx"
```

## Steps

### 1. Extrair dados do project management

```bash
# Extrair tickets de design da sprint atual
node scripts/extract-jira-data.js \
  --project $JIRA_PROJECT \
  --sprint current \
  --output weekly/data/jira-$(date +%Y%m%d).json

# Dados extraídos:
# - Tickets concluídos esta semana
# - Tickets em andamento
# - Tickets bloqueados
# - Story points entregues vs. planejados
```

### 2. Extrair dados do Figma

```bash
# Contar arquivos modificados esta semana
node scripts/extract-figma-activity.js \
  --team-id $FIGMA_TEAM_ID \
  --since $(date -d "7 days ago" +%Y-%m-%d) \
  --output weekly/data/figma-$(date +%Y%m%d).json

# Dados extraídos:
# - Arquivos modificados
# - Componentes publicados
# - Comments resolvidos
```

### 3. Calcular métricas

```bash
# Consolidar métricas semanais
node scripts/calculate-weekly-metrics.js \
  --jira weekly/data/jira-$(date +%Y%m%d).json \
  --figma weekly/data/figma-$(date +%Y%m%d).json \
  --output weekly/data/metrics-$(date +%Y%m%d).json

# Métricas calculadas:
# - Telas entregues
# - Story points completados
# - Lead time médio (request to handoff)
# - Rework rate (tickets reabertos)
# - DS adoption (% de componentes do DS usados)
```

### 4. Gerar relatório

```bash
# Gerar markdown
node scripts/generate-weekly-report.js \
  --metrics weekly/data/metrics-$(date +%Y%m%d).json \
  --jira weekly/data/jira-$(date +%Y%m%d).json \
  --template templates/weekly-report.md \
  --output weekly/reports/week-$(date +%Y%m%d).md
```

### 5. Revisar e publicar

```bash
# Abrir para review manual (adicionar highlights e context)
# Após review:

# Postar no Slack
node scripts/post-to-slack.js \
  --webhook $SLACK_WEBHOOK_URL \
  --file weekly/reports/week-$(date +%Y%m%d).md \
  --channel "#design-squad"

# Enviar por email para stakeholders
node scripts/send-report-email.js \
  --file weekly/reports/week-$(date +%Y%m%d).md \
  --recipients "pm-leads@empresa.com,eng-leads@empresa.com"
```

## Expected Output

```markdown
# Design Squad — Weekly Report — Semana [N] (DD/MM — DD/MM)

## Highlights da Semana
- Entrega do redesign de checkout (3 telas, handoff completo)
- Design system v3.1 lançado com 2 novos componentes
- Audit de a11y: score subiu de 78 para 82

## Métricas
| Métrica | Esta semana | Semana anterior | Trend |
|---------|-------------|-----------------|-------|
| Telas entregues | 8 | 6 | +33% |
| Story points | 21 | 18 | +17% |
| Lead time médio | 4.2 dias | 4.8 dias | -12% |
| Rework rate | 5% | 8% | -38% |

## Entregas (Handoff Completo)
- [DESIGN-123] Checkout — Form de endereço (Squad Checkout)
- [DESIGN-124] Checkout — Resumo do pedido (Squad Checkout)
- [DESIGN-125] Dashboard — Widget de métricas (Squad Dashboard)

## Em Andamento
- [DESIGN-130] Onboarding — Welcome flow (70% — entrega prevista: sexta)
- [DESIGN-131] Mobile — Navigation redesign (40% — discovery em curso)

## Bloqueios
- [DESIGN-132] Settings — Aguardando definição de copy com marketing
  - Ação necessária: Alinhamento com marketing até quarta

## Próxima Semana
- Foco: Finalizar onboarding + iniciar pesquisa de busca
- Design review: Terça 14h — onboarding flow
- DS release: v3.2 com fix de contraste em badges
```

## Automation Notes

- **Frequência:** Sexta-feira 16h (dados extraídos) + revisão manual
- **CI/CD:** GitHub Actions scheduled para extração de dados
- **Template:** Customizável em `templates/weekly-report.md`
- **Historical:** Reports archivados para análise de tendência trimestral
- **Distribution:** Slack (#design-squad) + email para stakeholders
- **Time spent:** Automatização reduz de ~60min para ~10min de revisão
