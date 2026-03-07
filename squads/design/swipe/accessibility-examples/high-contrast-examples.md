# High Contrast Mode Examples

## Pattern Description

Exemplos de design que funcionam bem em modos de alto contraste e para usuarios com baixa visao. Cobre Windows High Contrast Mode, forced colors e design para baixa visao.

## Examples

### Example 1: Microsoft — Windows High Contrast Native
Aplicacoes Microsoft respeitam High Contrast Mode:
- Cores do sistema usadas automaticamente via `forced-colors: active`
- Bordas visiveis em todos os controles interativos
- Icones usam `currentColor` para herdar cor do sistema
- Focus indicators com alto contraste automatico
- Nenhuma informacao perdida em forced colors

### Example 2: GOV.UK — Designed for Low Vision
GOV.UK e funcional com zoom de 400%:
- Layout reflows completamente em zoom alto
- Sem scroll horizontal em nenhum zoom level
- Fontes grandes por padrao (19px body text)
- Contraste > 7:1 para texto principal (AAA)
- Sem perda de funcionalidade em text spacing override

### Example 3: Stripe — Dark Mode as Accessibility
Stripe trata dark mode como feature de acessibilidade:
- Reduz glare para usuarios sensiveis a luz
- Contraste mantido em ambos os temas (AA minimo)
- Nunca pure white (#fff) em dark — usa off-white para reduzir strain
- Nunca pure black (#000) em light — usa near-black
- Toggle de tema acessivel em configuracoes

## Analysis

High contrast eficaz:
- **Forced colors**: teste com `forced-colors: active` media query
- **Borders**: nao dependa apenas de sombras para delimitar elementos
- **currentColor**: use para icones que devem herdar cor do contexto
- **Contrast ratios**: 4.5:1 minimo (AA), 7:1 ideal (AAA)
- **Text spacing**: suporte a override de line-height, letter-spacing
- **Zoom reflow**: conteudo deve reflowir ate 400% sem scroll horizontal

```css
@media (forced-colors: active) {
  .button {
    border: 2px solid ButtonText;
  }
  .icon {
    color: currentColor;
  }
}
```

## Tags

`high-contrast`, `forced-colors`, `low-vision`, `a11y`, `dark-mode`, `zoom`
