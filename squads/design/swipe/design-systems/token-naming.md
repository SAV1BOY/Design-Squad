# Token Naming Convention Patterns

## Pattern Description

Padroes de nomenclatura para design tokens em design systems maduros. Convencoes consistentes sao essenciais para escalabilidade, manutencao e adocao por times distribuidos.

## Examples

### Example 1: Salesforce Lightning — Category-Property-Variant
Lightning Design System segue padrao estruturado:
- `$color-background-brand` → `{category}-{property}-{variant}`
- `$font-size-heading-large` → `{category}-{property}-{element}-{scale}`
- `$spacing-medium` → `{category}-{scale}`
- Prefixo `$` para SASS variables
- Documentacao com descricao e deprecated status

### Example 2: GitHub Primer — Functional Naming
Primer usa nomes funcionais (nao descritivos de valor):
- `--color-fg-default` → foreground default
- `--color-bg-emphasis` → background com enfase
- `--color-border-muted` → borda discreta
- Evita nomes como "blue-500" em tokens de consumo
- Layers claras: primitive → functional → component

### Example 3: Shopify Polaris — Context-Aware Naming
Polaris inclui contexto no nome:
- `--p-color-bg-surface` → background de surface
- `--p-color-text-critical` → texto critico
- `--p-space-400` → spacing scale numerico
- Prefixo `--p-` para namespace
- Mapeamento claro entre Figma e codigo

## Analysis

Token naming eficaz:
- **Semantico**: nome descreve funcao, nao valor (nao "blue-500")
- **Previsivel**: padrao consistente em todo o sistema
- **Hierarquico**: {category}-{property}-{variant}-{state}
- **Namespaced**: prefixo para evitar conflito com outros sistemas
- **Documentado**: cada token com descricao de uso e contexto
- **Deprecation**: processo claro para renomear/remover tokens

## Tags

`design-tokens`, `naming-conventions`, `design-systems`, `scalability`, `maintainability`
