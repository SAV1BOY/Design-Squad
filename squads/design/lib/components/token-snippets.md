# Token Snippets

## Purpose

Catalogo de snippets para aplicacao correta de design tokens em componentes. Demonstra como tokens de cor, tipografia, spacing e elevation se conectam a propriedades visuais.

## Snippets

### Color Token Application

```css
/* Semantic color tokens */
.button-primary {
  background-color: var(--color-action-primary);
  color: var(--color-text-on-action);
  border: 1px solid var(--color-action-primary);
}

.button-primary:hover {
  background-color: var(--color-action-primary-hover);
}

.button-primary:disabled {
  background-color: var(--color-action-disabled);
  color: var(--color-text-disabled);
}
```

Regras de aplicacao:
- Use tokens semanticos, nunca valores hard-coded
- Tokens de cor seguem o padrao: `color-{role}-{variant}`
- Sempre defina estados: default, hover, active, focus, disabled

### Typography Token Application

```css
/* Typography scale tokens */
.heading-lg {
  font-family: var(--font-family-heading);
  font-size: var(--font-size-2xl);
  font-weight: var(--font-weight-bold);
  line-height: var(--line-height-tight);
  letter-spacing: var(--letter-spacing-tight);
}

.body-md {
  font-family: var(--font-family-body);
  font-size: var(--font-size-md);
  line-height: var(--line-height-normal);
}
```

### Spacing Token Application

```css
/* Spacing scale: 4px base unit */
.card {
  padding: var(--spacing-lg);       /* 24px */
  gap: var(--spacing-md);           /* 16px */
  margin-bottom: var(--spacing-xl); /* 32px */
}

.card-header {
  padding-bottom: var(--spacing-sm); /* 8px */
  border-bottom: 1px solid var(--color-border-subtle);
}
```

### Elevation Token Application

```css
/* Elevation / shadow tokens */
.card { box-shadow: var(--elevation-sm); }
.dropdown { box-shadow: var(--elevation-md); }
.modal { box-shadow: var(--elevation-lg); }
.tooltip { box-shadow: var(--elevation-xl); }
```

Niveis de elevation:
- **sm**: cards e containers sutis
- **md**: dropdowns e popovers
- **lg**: modais e dialogs
- **xl**: tooltips e elementos flutuantes

### Border Radius Token Application

```css
.button { border-radius: var(--radius-md); }
.input { border-radius: var(--radius-sm); }
.card { border-radius: var(--radius-lg); }
.avatar { border-radius: var(--radius-full); }
.badge { border-radius: var(--radius-pill); }
```

## Usage Notes

- Tokens sao a unica fonte de verdade para valores visuais
- Nunca use valores magicos — sempre mapeie para um token existente
- Se um valor nao tem token, proponha a criacao antes de usar hard-coded
- Tokens facilitam temas (light/dark) e white-label
- Documente a relacao entre global tokens, alias tokens e component tokens
- Revise tokens periodicamente para remover os nao utilizados
