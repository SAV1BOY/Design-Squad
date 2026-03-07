# Tab Navigation Patterns

## Pattern Description

Padroes de navegacao por tabs para organizar conteudo em secoes horizontais. Tabs permitem alternancia rapida entre visoes relacionadas sem mudanca de pagina.

## Examples

### Example 1: Stripe Dashboard — Contextual Tabs
Stripe usa tabs para segmentar dados de pagamento:
- Tabs: Payments, Customers, Subscriptions
- Contadores em cada tab (Payments: 1,234)
- Tab ativa com indicador de cor forte na borda inferior
- Conteudo atualiza sem reload (SPA navigation)

### Example 2: GitHub — Repository Tabs
GitHub organiza repositorios com tabs iconicas:
- Code, Issues, Pull Requests, Actions, Projects, Wiki, Settings
- Badge de contagem em Issues e PRs
- Responsivo: colapsa em dropdown "More" em telas estreitas
- Keyboard navigation com Arrow keys

### Example 3: Figma — Panel Tabs
Figma usa tabs em paineis laterais:
- Design, Prototype, Inspect
- Tabs compactas com icone + label
- Transicao suave entre conteudos do painel
- Estado persistido entre sessoes

## Analysis

Tabs eficazes:
- Maximo 7 tabs visiveis (3-5 e o ideal)
- Conteudo das tabs deve ser do mesmo nivel hierarquico
- Use overflow menu ("More") quando houver muitas tabs
- Tab ativa deve ser visualmente distinta
- Nunca use tabs para etapas sequenciais (use stepper)
- `role="tablist"` + `role="tab"` + `role="tabpanel"` para a11y

## Tags

`tabs`, `navigation`, `information-architecture`, `spa`, `a11y`
