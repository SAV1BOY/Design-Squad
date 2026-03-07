# Breadcrumb Patterns

## Pattern Description

Padroes de breadcrumb para indicar posicao hierarquica do usuario na arquitetura de informacao. Breadcrumbs sao navegacao secundaria que facilitam retorno a niveis superiores.

## Examples

### Example 1: Shopify Admin — E-commerce Breadcrumb
Shopify usa breadcrumbs em toda a area administrativa:
- Inicio > Produtos > Camiseta Azul > Editar
- Links clicaveis em cada nivel
- Pagina atual nao e link (apenas texto)
- Separador "/" discreto entre niveis

### Example 2: AWS Console — Deep Hierarchy
AWS Console navega hierarquias profundas:
- S3 > bucket-name > folder > subfolder > file.json
- Truncamento com "..." para caminhos longos
- Dropdown em cada nivel para navegar lateralmente entre siblings
- Copy path como funcionalidade integrada

### Example 3: Jira — Project Context
Jira mostra contexto de projeto em breadcrumbs:
- Projeto X > Board > Sprint 5 > TICKET-123
- Icone do projeto no primeiro nivel
- Link rapido para board e sprint ativos
- Acessivel com `aria-label="Breadcrumb"`

## Analysis

Breadcrumbs eficazes:
- Essenciais quando hierarquia tem 3+ niveis
- Nao substituem navegacao primaria (sao complementares)
- Use separadores visuais claros (/ ou >)
- Ultimo item (pagina atual) nao deve ser link
- Truncamento para caminhos longos com tooltip no hover
- `<nav aria-label="Breadcrumb">` + `<ol>` para semantica correta

## Tags

`breadcrumbs`, `navigation`, `hierarchy`, `wayfinding`, `information-architecture`
