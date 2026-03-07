# Elevation Scale

## Purpose

Escala de elevacao (shadow) padronizada para comunicar hierarquia espacial entre elementos. Define niveis de profundidade visual usando box-shadow tokens.

## Scale Definition

```
Token              | Offset-Y | Blur  | Spread | Color          | Uso
-------------------|----------|-------|--------|----------------|--------------------
--elevation-none   | 0        | 0     | 0      | transparent    | Elementos flat
--elevation-xs     | 0 1px    | 2px   | 0      | black/5%       | Subtle lift (inputs)
--elevation-sm     | 0 2px    | 4px   | -1px   | black/8%       | Cards, tiles
--elevation-md     | 0 4px    | 8px   | -2px   | black/12%      | Dropdowns, popovers
--elevation-lg     | 0 8px    | 16px  | -4px   | black/16%      | Modais, dialogs
--elevation-xl     | 0 16px   | 32px  | -8px   | black/20%      | Tooltips flutuantes
```

## Compound Shadows

Para maior realismo, combine duas camadas de shadow:

```css
--elevation-sm: 0 1px 2px rgba(0,0,0,0.06), 0 2px 4px rgba(0,0,0,0.08);
--elevation-md: 0 2px 4px rgba(0,0,0,0.04), 0 4px 8px rgba(0,0,0,0.12);
--elevation-lg: 0 4px 8px rgba(0,0,0,0.04), 0 8px 16px rgba(0,0,0,0.16);
```

## Application Rules

### Static Elevation
```
Nivel 0 (flat):    backgrounds, secoes de pagina
Nivel xs:          inputs focados, buttons hover
Nivel sm:          cards, tiles, list items
```

### Interactive Elevation
```
Nivel md:          dropdowns, popovers, tooltips de menu
Nivel lg:          modais, dialogs, drawers
Nivel xl:          tooltips, elementos de drag
```

### Elevation Transitions
```
Card default:      --elevation-sm
Card hover:        --elevation-md (lift effect)
Card pressed:      --elevation-xs (press effect)

transition: box-shadow 200ms ease-in-out;
```

## Dark Mode Considerations

```
Em dark mode, shadows sao menos eficazes.
Estrategias complementares:
- Use bordas sutis (1px solid rgba(255,255,255,0.1))
- Aumente o brilho do surface elevado (surface-elevated mais claro)
- Reduza a opacidade das shadows em ~50%
- Combine shadow + borda para clareza
```

## Validation Checklist

- [ ] Cada nivel de elevation tem uso claramente definido
- [ ] Transicoes de elevation sao suaves (200-300ms ease)
- [ ] Dark mode usa estrategia complementar
- [ ] Nao mais que 3 niveis de elevation visiveis simultaneamente
- [ ] Elevation e consistente entre componentes do mesmo tipo

## Usage Notes

- Elevation comunica interatividade e hierarquia z-index
- Menos e mais — use elevation com parcimonia
- Z-index deve acompanhar a escala de elevation
- Em mobile, elevation indica elementos deslizaveis ou flutuantes
