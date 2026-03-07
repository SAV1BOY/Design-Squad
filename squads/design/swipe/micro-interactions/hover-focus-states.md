# Hover and Focus State Patterns

## Pattern Description

Padroes para estados de hover e focus em elementos interativos. Esses micro-estados comunicam interatividade e guiam a atencao do usuario.

## Examples

### Example 1: Linear — Subtle Hover Elevation
Linear aplica hover sutil em cards e rows:
- Background change: transparent → surface-hover (5% opacity)
- Transicao: 150ms ease-out
- Sem mudanca de tamanho ou layout shift
- Cursor: pointer para elementos clicaveis
- Row actions aparecem on hover (edit, delete)

### Example 2: Stripe — Focus Ring System
Stripe implementa focus rings consistentes:
- Ring azul (2px) em todos os elementos focaveis
- `:focus-visible` para evitar ring no click (apenas keyboard)
- Custom focus ring que respeita border-radius do elemento
- Offset de 2px para nao cobrir bordas
- Alto contraste do ring em light e dark mode

### Example 3: Apple — Scale on Hover
Apple usa scale sutil no hover:
- Cards: `transform: scale(1.02)` no hover
- Transicao: 200ms ease-in-out
- Shadow aumenta simultaneamente
- Preview de conteudo no hover prolongado
- Reduced motion: apenas mudanca de cor, sem scale

## Analysis

Hover e focus eficazes:
- **Consistencia**: mesmos patterns em todo o produto
- **Sutileza**: mudancas devem ser perceptiveis mas nao distrativas
- **Performance**: anime apenas transform e opacity para 60fps
- **A11y**: `:focus-visible` para keyboard-only focus
- **Reduced motion**: fallback sem animacao para `prefers-reduced-motion`
- **Touch devices**: hover nao existe — nao dependa dele para funcionalidade

## Tags

`hover`, `focus`, `micro-interactions`, `states`, `a11y`, `animation`
