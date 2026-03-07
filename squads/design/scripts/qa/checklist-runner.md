# Checklist Runner

## Title
Script de execução automatizada de checklists de QA de design.

## Purpose

Automatizar a verificação de checklists de qualidade de design durante o QA —
verificando tokens, consistência de componentes, estados implementados e critérios
de acessibilidade. Reduz o tempo de QA manual e garante que nenhum critério seja
esquecido.

## Prerequisites

- **Node.js** >= 18.0
- **Playwright** para inspeção de DOM e estilos
- **Checklists** definidas em formato JSON
- **Produto rodando** em ambiente testável

Dependências:
```bash
npm install @playwright/test
```

## Steps

### 1. Definir checklist

```bash
# Checklist por tipo de componente/feature
cat > checklists/form.json << 'EOF'
{
  "name": "Form Quality Checklist",
  "version": "1.0",
  "checks": [
    {
      "id": "form-labels",
      "description": "Todos os inputs têm label associado",
      "type": "automated",
      "selector": "input, select, textarea",
      "validation": "hasAssociatedLabel",
      "severity": "critical"
    },
    {
      "id": "form-error-states",
      "description": "Inputs com validação têm estado de erro implementado",
      "type": "automated",
      "selector": "[required], [pattern], [minlength]",
      "validation": "hasErrorState",
      "severity": "critical"
    },
    {
      "id": "form-helper-text",
      "description": "Campos complexos têm helper text",
      "type": "manual",
      "description_detail": "Verificar campos de senha, CPF, CEP, telefone",
      "severity": "major"
    },
    {
      "id": "form-tab-order",
      "description": "Tab order segue ordem visual dos campos",
      "type": "automated",
      "validation": "tabOrderMatchesVisual",
      "severity": "critical"
    },
    {
      "id": "form-submit-feedback",
      "description": "Botão de submit mostra loading state durante processamento",
      "type": "semi-automated",
      "validation": "buttonShowsLoading",
      "trigger": "submitForm",
      "severity": "major"
    }
  ]
}
EOF
```

### 2. Executar checks automatizados

```bash
# Rodar checklist contra uma página
node scripts/checklist-runner.js \
  --checklist checklists/form.json \
  --url "$BASE_URL/cadastro" \
  --output qa/results/cadastro-form-$(date +%Y%m%d).json

# Rodar todas as checklists contra todas as páginas
node scripts/checklist-runner.js \
  --checklist-dir checklists/ \
  --urls audit-urls.json \
  --base-url $BASE_URL \
  --output qa/results/full-run-$(date +%Y%m%d).json
```

### 3. Verificar tokens

```bash
# Verificar se a implementação usa os tokens corretos
node scripts/token-checker.js \
  --url "$BASE_URL/cadastro" \
  --tokens dist/web/tokens.css \
  --output qa/results/token-check-$(date +%Y%m%d).json

# Detecta:
# - Cores hardcoded que deveriam ser tokens
# - Fonts hardcoded que deveriam ser tokens
# - Spacing values que não seguem a escala
```

### 4. Gerar relatório

```bash
# Relatório interativo
node scripts/generate-qa-report.js \
  --input qa/results/full-run-$(date +%Y%m%d).json \
  --format html \
  --output qa/reports/qa-report-$(date +%Y%m%d).html

# Relatório para Slack
node scripts/generate-qa-report.js \
  --input qa/results/full-run-$(date +%Y%m%d).json \
  --format slack \
  --output qa/reports/qa-slack.txt
```

### 5. Tracking de resultados

```bash
# Salvar resultado para tracking de tendência
node scripts/save-qa-metrics.js \
  --input qa/results/full-run-$(date +%Y%m%d).json \
  --metrics-db qa/metrics.json
```

## Expected Output

```markdown
# QA Checklist Report — Cadastro — [Data]

## Score: 85% (17/20 checks passed)

## Results by Severity

| Severity | Total | Passed | Failed | Manual |
|----------|-------|--------|--------|--------|
| Critical | 8 | 7 | 1 | 0 |
| Major | 7 | 5 | 1 | 1 |
| Minor | 5 | 5 | 0 | 0 |

## Failed Checks

### [CRITICAL] form-labels
Input "Telefone secundário" não tem label associado.
- Elemento: input#secondary-phone
- Fix: Adicionar <label for="secondary-phone">

### [MAJOR] form-submit-feedback
Botão "Criar conta" não mostra loading state durante submit.
- Elemento: button[type="submit"]
- Fix: Adicionar spinner/disabled durante processamento

## Manual Checks Required
- [ ] form-helper-text: Verificar manualmente campos de senha, CPF, CEP
```

## Automation Notes

- **Frequência:** A cada PR com mudanças de UI + pré-release
- **CI/CD:** Integrado ao pipeline como step pós-deploy em staging
- **Custom checklists:** Criar checklists por tipo de feature (form, table, modal, etc.)
- **Extensível:** Novas regras são adicionadas ao JSON sem mudança no runner
- **Integração:** Resultados podem gerar tickets automaticamente no Jira/Linear
- **Histórico:** Métricas armazenadas para tracking de qualidade ao longo do tempo
