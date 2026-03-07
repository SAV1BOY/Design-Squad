# Layout Component Snippets

## Purpose

Snippets para componentes de layout — grid systems, containers, stacks, dividers, spacing helpers e responsive wrappers. Fundamentais para estrutura e ritmo visual consistentes.

## Snippets

### Grid System

```css
/* Grid responsivo com tokens */
.grid {
  display: grid;
  gap: var(--spacing-md);
  grid-template-columns: repeat(12, 1fr);
}

.col-4 { grid-column: span 4; }
.col-6 { grid-column: span 6; }
.col-12 { grid-column: span 12; }

@media (max-width: 768px) {
  .grid { grid-template-columns: repeat(4, 1fr); }
  .col-4, .col-6 { grid-column: span 4; }
}
```

### Stack (Vertical / Horizontal)

```html
<!-- Vertical stack -->
<div class="stack" style="--stack-gap: var(--spacing-md);">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>

<!-- Horizontal stack -->
<div class="hstack" style="--stack-gap: var(--spacing-sm);">
  <button>Cancelar</button>
  <button class="btn-primary">Salvar</button>
</div>
```

```css
.stack { display: flex; flex-direction: column; gap: var(--stack-gap, var(--spacing-md)); }
.hstack { display: flex; flex-direction: row; gap: var(--stack-gap, var(--spacing-sm)); align-items: center; }
```

### Container

```css
.container {
  width: 100%;
  max-width: var(--container-max-width, 1200px);
  margin-inline: auto;
  padding-inline: var(--spacing-lg);
}

.container--narrow { --container-max-width: 720px; }
.container--wide { --container-max-width: 1440px; }
```

### Divider

```html
<hr class="divider" role="separator" />
<hr class="divider divider--subtle" />
<hr class="divider divider--section" />
```

```css
.divider {
  border: none;
  height: 1px;
  background-color: var(--color-border-default);
  margin-block: var(--spacing-md);
}
.divider--subtle { background-color: var(--color-border-subtle); }
.divider--section { margin-block: var(--spacing-xl); height: 2px; }
```

### Page Layout Template

```
┌──────────────────────────────────────┐
│              [Top Bar]               │
├──────────┬───────────────────────────┤
│          │                           │
│ [Side    │     [Main Content]        │
│  Nav]    │                           │
│          │                           │
│          │                           │
├──────────┴───────────────────────────┤
│              [Footer]                │
└──────────────────────────────────────┘
```

```css
.page-layout {
  display: grid;
  grid-template-areas:
    "topbar topbar"
    "sidebar main"
    "footer footer";
  grid-template-columns: 260px 1fr;
  grid-template-rows: auto 1fr auto;
  min-height: 100vh;
}

@media (max-width: 768px) {
  .page-layout {
    grid-template-areas: "topbar" "main" "footer";
    grid-template-columns: 1fr;
  }
}
```

## Usage Notes

- Use CSS Grid para layouts de pagina e Flexbox para alinhamento de componentes
- Sempre defina gap com tokens de spacing, nunca valores arbitrarios
- Containers devem ter padding inline para margens laterais em mobile
- Stacks simplificam composicao — prefira sobre margin manual
- Teste layouts com conteudo real (nao lorem ipsum) para validar flexibilidade
- Dividers devem ser usados com parcimonia — whitespace e suficiente na maioria dos casos
