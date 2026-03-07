# Bottom Navigation (Mobile) Patterns

## Pattern Description

Padroes de navegacao inferior para aplicacoes mobile. Bottom nav fornece acesso com uma mao aos destinos principais do app, seguindo a zona de alcance natural do polegar.

## Examples

### Example 1: Instagram — Icon-First Bottom Nav
Instagram usa bottom nav iconica minimalista:
- 5 itens: Home, Search, Reels, Shop, Profile
- Icones preenchidos quando ativos, outlined quando inativos
- Sem labels de texto (apenas icones reconheciveis)
- Ponto de notificacao vermelho sobre Activity

### Example 2: Google Maps — Contextual Bottom Nav
Google Maps adapta bottom nav ao contexto:
- Explore, Go, Saved, Contribute, Updates
- Labels visiveis em todos os itens
- Icone + label para clareza (melhor a11y)
- Fundo translucido para manter visibilidade do mapa
- Animacao suave de transicao entre secoes

### Example 3: Nubank — Branded Bottom Nav
Nubank integra bottom nav com identidade visual:
- Home, Cartao, PIX, Emprestimo, Shopping
- Icone central (PIX) destacado com cor de marca
- Micro-animacao no tap de cada item
- Badge numerico para notificacoes pendentes

## Analysis

Bottom nav eficaz:
- **3-5 itens**: nunca mais que 5 (padrao Material Design)
- **Labels**: sempre inclua labels por acessibilidade (nao apenas icones)
- **Icones**: distintos e reconheciveis sem label
- **Estado ativo**: mudanca visual clara (cor, fill, peso)
- **Touch target**: minimo 48x48dp por item
- **Scroll behavior**: considere hide-on-scroll para mais area de conteudo
- Nao use bottom nav em tablet/desktop — mude para side nav ou top nav

## Tags

`bottom-nav`, `mobile-navigation`, `thumb-zone`, `material-design`, `ios`, `touch`
