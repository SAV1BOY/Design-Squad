# Component Taxonomy

## Purpose

Taxonomia hierarquica de componentes de interface organizados por funcao. Serve como vocabulario compartilhado para o time de design e desenvolvimento.

## Taxonomy Tree

### 1. Actions
```
actions/
├── button
│   ├── primary
│   ├── secondary
│   ├── tertiary (ghost)
│   ├── danger
│   └── icon-button
├── link
│   ├── inline-link
│   ├── standalone-link
│   └── nav-link
├── toggle
│   ├── switch
│   └── segmented-control
└── fab (floating action button)
```

### 2. Inputs
```
inputs/
├── text-input
│   ├── single-line
│   ├── multi-line (textarea)
│   └── masked-input
├── select
│   ├── single-select
│   ├── multi-select
│   └── combobox (searchable)
├── checkbox
├── radio
├── slider
│   ├── single
│   └── range
├── date-picker
├── time-picker
├── file-upload
└── color-picker
```

### 3. Navigation
```
navigation/
├── top-bar
├── side-nav
├── bottom-nav
├── tabs
├── breadcrumb
├── pagination
├── stepper
└── menu
    ├── dropdown-menu
    └── context-menu
```

### 4. Data Display
```
data-display/
├── table
│   ├── data-table
│   └── simple-table
├── list
│   ├── ordered-list
│   ├── unordered-list
│   └── description-list
├── card
├── avatar
├── badge
├── tag / chip
├── tooltip
├── popover
└── metric-card (KPI)
```

### 5. Feedback
```
feedback/
├── alert (inline)
├── toast / snackbar
├── banner
├── progress
│   ├── progress-bar
│   ├── spinner
│   └── skeleton
├── empty-state
└── dialog
    ├── confirmation
    ├── informational
    └── form-dialog
```

### 6. Layout
```
layout/
├── container
├── grid
├── stack (vertical/horizontal)
├── divider
├── spacer
├── card-layout
└── page-shell
    ├── header
    ├── sidebar
    ├── main
    └── footer
```

## Classification Criteria

```
Criterio          | Descricao
------------------|--------------------------------------------------
Funcao primaria   | O que o componente faz (acao, input, display, etc.)
Complexidade      | Atomico, Molecular, Organismo (Atomic Design)
Interatividade    | Estatico, Interativo, Controlado
Composicao        | Standalone ou Composto (depende de outros)
```

## Usage Notes

- Use esta taxonomia para nomear componentes no design system
- Mantenha consistencia entre Figma, codigo e documentacao
- Revise trimestralmente para incluir novos componentes
- Cada componente deve ter um e apenas um lugar na taxonomia
- Componentes compostos referenciam seus atomos constituintes
