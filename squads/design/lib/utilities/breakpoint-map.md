# Breakpoint Map

## Purpose

Mapa de breakpoints padronizado para design responsivo. Define pontos de quebra, colunas de grid, margens e comportamentos adaptativos para cada faixa de viewport.

## Breakpoint Definitions

```
Token          | Min-Width | Max-Width | Colunas | Margin | Gutter | Target
---------------|-----------|-----------|---------|--------|--------|------------------
--bp-xs        | 0         | 359px     | 4       | 16px   | 8px    | Small phones
--bp-sm        | 360px     | 599px     | 4       | 16px   | 16px   | Phones
--bp-md        | 600px     | 904px     | 8       | 24px   | 16px   | Tablets portrait
--bp-lg        | 905px     | 1239px    | 12      | 24px   | 24px   | Tablets landscape
--bp-xl        | 1240px    | 1439px    | 12      | 32px   | 24px   | Desktops
--bp-2xl       | 1440px    | ---       | 12      | auto   | 24px   | Large desktops
```

## CSS Custom Properties

```css
:root {
  --breakpoint-sm: 360px;
  --breakpoint-md: 600px;
  --breakpoint-lg: 905px;
  --breakpoint-xl: 1240px;
  --breakpoint-2xl: 1440px;
}
```

## Media Query Patterns

```css
/* Mobile first (recomendado) */
@media (min-width: 600px) { /* md+ */ }
@media (min-width: 905px) { /* lg+ */ }
@media (min-width: 1240px) { /* xl+ */ }

/* Range queries (CSS4) */
@media (600px <= width < 905px) { /* apenas md */ }

/* Container queries (componentes) */
@container (min-width: 400px) { /* componente largo */ }
```

## Layout Behaviors por Breakpoint

### xs-sm (Mobile)
```
- Navegacao: bottom nav ou hamburger
- Grid: 4 colunas, stack vertical
- Tabelas: card list ou scroll horizontal
- Modais: full-screen
- Touch targets: min 44x44px
- Tipografia: escala reduzida (-2 steps para headings)
```

### md (Tablet Portrait)
```
- Navegacao: top bar com menu colapsavel
- Grid: 8 colunas, layouts hibridos
- Tabelas: colunas priorizadas + expandable rows
- Modais: centered, max-width 560px
- Side panels: overlay, nao inline
```

### lg (Tablet Landscape / Small Desktop)
```
- Navegacao: side nav ou top bar completo
- Grid: 12 colunas
- Tabelas: completas com scroll se necessario
- Modais: centered, max-width 640px
- Side panels: inline
```

### xl-2xl (Desktop)
```
- Navegacao: side nav permanente ou top bar
- Grid: 12 colunas, max-width container
- Tabelas: completas com sort e filter
- Modais: centered, max-width 720px
- Multi-panel layouts possiveis
```

## Usage Notes

- Sempre use mobile-first approach
- Breakpoints sao baseados em conteudo, nao em dispositivos especificos
- Teste com dispositivos reais, nao apenas redimensionando browser
- Container queries sao preferidos para componentes reutilizaveis
- Documente comportamento de cada componente por breakpoint
