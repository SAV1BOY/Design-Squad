# Navigation Patterns

## Summary

Padrões de navegação são os blocos fundamentais que permitem aos usuários se moverem através de uma aplicação ou website. Uma navegação bem projetada reduz a carga cognitiva e ajuda os usuários a encontrarem o que precisam de forma eficiente. Este documento cobre os principais padrões de navegação utilizados em interfaces modernas, incluindo nav bars, sidebars, breadcrumbs, tabs e mega menus.

## Key Concepts

### Navigation Bar (Nav Bar)

A barra de navegação principal é o elemento mais reconhecível de qualquer interface. Geralmente posicionada no topo da página, ela contém os links primários da aplicação e serve como ponto de referência constante para o usuário.

- **Horizontal Nav Bar**: Ideal para aplicações com 3-7 itens de navegação principal
- **Sticky Nav Bar**: Permanece visível durante o scroll, garantindo acesso contínuo
- **Responsive Nav Bar**: Adapta-se para hamburger menu em viewports menores

### Sidebar Navigation

A navegação lateral é preferida quando a aplicação possui muitos níveis de hierarquia. Sidebars são comuns em dashboards, painéis administrativos e ferramentas de produtividade.

- **Collapsible Sidebar**: Pode ser recolhida para maximizar o espaço de conteúdo
- **Multi-level Sidebar**: Suporta navegação hierárquica com submenus expansíveis
- **Icon-only Mode**: Exibe apenas ícones quando recolhida, economizando espaço

### Breadcrumbs

Breadcrumbs fornecem uma trilha de navegação que mostra ao usuário sua localização atual dentro da hierarquia do site. São essenciais para sites com estruturas profundas.

- **Location-based**: Mostra a posição na hierarquia do site
- **Path-based**: Mostra o caminho que o usuário percorreu
- **Attribute-based**: Comum em e-commerce, mostra filtros aplicados

### Tabs

Tabs organizam conteúdo em seções distintas dentro de uma mesma página. São ideais quando o usuário precisa alternar entre visões relacionadas sem perder o contexto.

- **Horizontal Tabs**: O padrão mais comum, posicionado acima do conteúdo
- **Vertical Tabs**: Úteis quando há muitas categorias ou labels longos
- **Scrollable Tabs**: Permitem mais tabs do que o espaço visível comporta

### Mega Menus

Mega menus são dropdowns expandidos que mostram múltiplas colunas de links e, frequentemente, imagens ou promoções. São ideais para sites com grande volume de categorias.

- **Full-width Mega Menu**: Ocupa toda a largura do viewport
- **Sectioned Mega Menu**: Divide conteúdo em categorias visuais claras
- **Featured Mega Menu**: Inclui elementos promocionais como imagens e CTAs

## When to Use

| Padrão | Cenário Ideal | Evitar Quando |
|--------|--------------|---------------|
| Nav Bar | Sites com navegação simples e direta | Existem mais de 7 itens principais |
| Sidebar | Aplicações complexas com hierarquia profunda | O conteúdo principal precisa de toda a largura |
| Breadcrumbs | Sites com mais de 2 níveis de profundidade | A estrutura é flat ou tem apenas 1 nível |
| Tabs | Conteúdo relacionado que precisa de alternância rápida | Há dependência sequencial entre as seções |
| Mega Menu | Sites de e-commerce ou portais com muitas categorias | O site tem poucas páginas ou categorias |

## Anatomy

### Nav Bar Structure

```
[Logo] [Nav Item 1] [Nav Item 2] [Nav Item 3] ... [Search] [User Menu]
```

Elementos obrigatórios incluem o logo (que serve como link para home), os itens de navegação principal e, idealmente, um indicador visual do item ativo. Elementos opcionais incluem search bar, notificações e menu do usuário.

### Sidebar Structure

```
[Logo/Brand]
├── [Section Label]
│   ├── [Nav Item] [Icon]
│   ├── [Nav Item] [Icon] [Badge]
│   └── [Nav Item] [Icon]
├── [Section Label]
│   ├── [Nav Item]
│   └── [Submenu]
│       ├── [Sub Item]
│       └── [Sub Item]
└── [Footer / Settings]
```

A sidebar deve ter agrupamentos lógicos, separadores visuais entre seções e indicadores claros de expansão para submenus.

## Variations

### Navigation por Contexto

- **Global Navigation**: Persistente em todas as páginas, contém links principais
- **Local Navigation**: Específica de uma seção, complementa a navegação global
- **Contextual Navigation**: Links inline relacionados ao conteúdo atual
- **Utility Navigation**: Funcionalidades secundárias como idioma, conta, ajuda

### Navigation por Dispositivo

- **Desktop**: Nav bars completas com mega menus e hover states
- **Tablet**: Nav bars simplificadas com sidebars colapsáveis
- **Mobile**: Hamburger menus, bottom navigation bars, full-screen overlays

## Best Practices

1. **Mantenha consistência**: A navegação principal deve ser idêntica em todas as páginas
2. **Limite as opções**: Aplique a regra de Miller (7 mais ou menos 2 itens) para menus principais
3. **Indique a localização atual**: Use visual indicators para mostrar onde o usuário está
4. **Priorize por frequência de uso**: Itens mais acessados devem ter maior destaque
5. **Ofereça múltiplos caminhos**: Combine breadcrumbs com sidebar para flexibilidade
6. **Teste com usuários reais**: Card sorting e tree testing revelam a melhor estrutura
7. **Considere deep linking**: Cada estado de navegação deve ter uma URL compartilhável
8. **Use labels claros**: Evite jargões internos; prefira termos que os usuários reconhecem
9. **Minimize cliques**: Reduza a profundidade necessária para alcançar qualquer página

## Accessibility Considerations

- Utilize o elemento semantico nav com aria-label descritivo para cada região de navegação
- Implemente keyboard navigation com Tab, Arrow keys e Enter/Space
- Garanta que o focus order segue uma sequência lógica e visível
- Breadcrumbs devem usar ol com aria-label="Breadcrumb" e aria-current="page" no item atual
- Mega menus precisam de aria-expanded, aria-haspopup e gerenciamento de focus adequado
- Tabs devem implementar o ARIA tabs pattern com role="tablist", role="tab" e role="tabpanel"
- Forneça skip navigation links para permitir que usuários de screen reader pulem diretamente ao conteúdo
- O contraste de cores entre texto e background deve atender WCAG 2.1 AA (mínimo 4.5:1)
- Sidebar colapsável deve anunciar seu estado (expandida/recolhida) para assistive technologies

## Cross-References

- Ver form-patterns.md para integração de search forms na navegação
- Ver mobile-patterns.md para padrões de bottom navigation e gestures
- Ver dashboard-patterns.md para navegação em contextos de dashboard
- Ver authentication-patterns.md para fluxos de login/logout no user menu
- Ver search-patterns.md para implementação de search integrado à nav bar
