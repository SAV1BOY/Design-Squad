# Responsive Design System

## Metadata

| Campo         | Valor                                         |
| ------------- | --------------------------------------------- |
| Categoria     | Design System                                 |
| Complexidade  | Alta                                          |
| Autor         | Design Squad                                  |
| Versao        | 1.0                                           |
| Ultima revisao| 2026-03-06                                    |
| Tags          | responsive, breakpoints, mobile-first, density |

## Concept

Um responsive design system e uma abordagem sistematica para criar interfaces que se adaptam
de forma fluida a diferentes tamanhos de tela, densidades de pixel, e contextos de uso. Vai alem
de media queries — abrange estrategia de conteudo, hierarquia de prioridade, e design tokens
que respondem ao contexto.

### Pilares

1. **Breakpoints**: pontos de mudanca estrutural no layout.
2. **Density**: adaptacao de espacamento e tamanho ao contexto (touch vs pointer).
3. **Priority**: reordenacao e ocultacao de conteudo por importancia.
4. **Mobile-first**: progressao do menor para o maior viewport.

### Breakpoint System

| Token      | Range           | Target                    | Columns | Margins |
| ---------- | --------------- | ------------------------- | ------- | ------- |
| `xs`       | 0 - 479px       | Small phones              | 4       | 16px    |
| `sm`       | 480 - 767px     | Large phones, small tabs  | 4       | 24px    |
| `md`       | 768 - 1023px    | Tablets                   | 8       | 32px    |
| `lg`       | 1024 - 1439px   | Laptops, desktops         | 12      | 40px    |
| `xl`       | 1440 - 1919px   | Large desktops            | 12      | 64px    |
| `xxl`      | 1920+           | Ultra-wide                | 12      | auto    |

## When to Use

- Em todo produto digital — responsividade nao e opcional.
- Ao criar ou atualizar componentes no design system.
- Ao planejar layouts de pagina e templates.
- Quando analytics mostram diversidade de dispositivos no acesso.
- Ao projetar para mercados onde mobile e o acesso primario.

## How to Apply

### 1. Mobile-First Strategy

1. **Comecar pelo menor viewport** — projetar a experiencia mobile primeiro.
2. **Definir conteudo essencial** — o que e absolutamente necessario na menor tela.
3. **Adicionar complexidade progressivamente** — mais colunas, sidebars, detalhes em telas maiores.
4. **CSS mobile-first**: usar `min-width` nas media queries, nao `max-width`.

### 2. Layout Patterns

- **Stack to horizontal**: elementos empilhados no mobile viram row no desktop.
- **Off-canvas navigation**: menu em drawer no mobile, sidebar fixa no desktop.
- **Cards reflow**: grid de 1 coluna no mobile para 2-3-4 colunas no desktop.
- **Table to cards**: tabela densa vira lista de cards no mobile.
- **Priority+ navigation**: itens que nao cabem vao para menu "mais".

### 3. Density Adaptation

```
Touch density (mobile):   min-height 48px, padding 12-16px, gap 8-12px
Pointer density (desktop): min-height 32px, padding 8-12px, gap 4-8px
```

Usar `@media (pointer: fine)` e `@media (pointer: coarse)` para adaptar.

### 4. Typography Scale

| Token          | Mobile   | Desktop  |
| -------------- | -------- | -------- |
| `heading-xl`   | 28px     | 40px     |
| `heading-lg`   | 24px     | 32px     |
| `heading-md`   | 20px     | 24px     |
| `body-lg`      | 16px     | 18px     |
| `body-md`      | 14px     | 16px     |
| `body-sm`      | 12px     | 14px     |

Usar `clamp()` para escalas fluidas: `font-size: clamp(1rem, 0.5rem + 1vw, 1.25rem)`.

### 5. Image Strategy

- **`srcset` e `sizes`** para imagens responsivas.
- **Art direction** com `<picture>` para recortes diferentes por viewport.
- **Lazy loading** com `loading="lazy"` para imagens abaixo do fold.
- **Aspect ratio containers** para evitar layout shift.

## Key Principles

- **Content-first**: breakpoints devem ser definidos pelo conteudo, nao por dispositivos.
- **Fluid over fixed**: preferir unidades relativas (rem, %, vw) a pixels fixos.
- **Touch-friendly**: areas de toque minimo de 44x44px (WCAG) ou 48x48px (Material).
- **Performance**: mobile-first tambem e performance-first — menos assets, menos JS.
- **Testavel**: todo componente deve ser testado em pelo menos 3 breakpoints.
- **Container queries**: preferir container queries a media queries para componentes reutilizaveis.

## Examples

### Navigation Pattern

```
xs-sm:  Hamburger menu -> bottom sheet com links
md:     Tab bar horizontal com icones e labels
lg+:    Sidebar fixa com navegacao completa
```

### Dashboard Layout

```
xs:     Stack vertical — 1 KPI por row, grafico full-width
sm-md:  Grid 2x2 para KPIs, grafico full-width abaixo
lg:     Sidebar de filtros + grid 4 KPIs + grafico ao lado
xl+:    Mesmo que lg com mais whitespace e detalhes adicionais
```

## Common Pitfalls

| Erro                               | Consequencia                        | Correcao                                |
| ---------------------------------- | ----------------------------------- | --------------------------------------- |
| Desktop-first e depois "encolher"  | Experiencia mobile amputada         | Comecar pelo mobile, expandir           |
| Breakpoints fixos por dispositivo  | Quebra em dispositivos intermediarios| Breakpoints baseados no conteudo        |
| Esconder conteudo no mobile        | Desigualdade de experiencia         | Reprojetar, nao esconder                |
| Ignorar landscape em mobile        | Layout quebrado em tablets          | Testar orientacoes portrait e landscape |
| Touch targets pequenos             | Frustacao e erros de toque          | Minimo 44x44px para areas de toque      |
| Imagens sem srcset                 | Performance degradada               | Servir imagens otimizadas por viewport  |

## Cross-References

- [Progressive Disclosure](./progressive-disclosure.md) — disclosure pode variar por breakpoint.
- [Dark Mode System](./dark-mode-system.md) — tokens responsivos em modo escuro.
- [Accessibility WCAG AA](./accessibility-wcag-aa.md) — touch targets e reflow criterion.
- [Design System Governance](./design-system-governance.md) — versionamento de breakpoint tokens.
- [Motion Design System](./motion-design-system.md) — animacoes adaptadas por device capability.
