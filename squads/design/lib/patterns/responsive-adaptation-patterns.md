# Responsive Adaptation Patterns

## Pattern Description

Padroes para adaptacao responsiva de layouts e componentes entre breakpoints. Cobre estrategias de reflow, priority+ pattern, off-canvas, stacking e adaptive content.

## Patterns

### Reflow: Multi-Column to Stack

```
Desktop (>= 1024px):
┌──────┬──────┬──────┐
│ Col1 │ Col2 │ Col3 │
└──────┴──────┴──────┘

Tablet (768-1023px):
┌──────┬──────┐
│ Col1 │ Col2 │
├──────┴──────┤
│    Col3     │
└─────────────┘

Mobile (< 768px):
┌─────────────┐
│    Col1     │
├─────────────┤
│    Col2     │
├─────────────┤
│    Col3     │
└─────────────┘
```

### Priority+ Navigation

```
Desktop: [Home] [Produtos] [Sobre] [Blog] [Contato] [Carreiras]

Tablet:  [Home] [Produtos] [Sobre] [Mais ▼]
                                    └── Blog
                                    └── Contato
                                    └── Carreiras

Mobile:  [☰] Menu
```

### Off-Canvas Sidebar

```
Desktop:
┌──────────┬───────────────────┐
│ Sidebar  │     Content       │
│ (visible)│                   │
└──────────┴───────────────────┘

Mobile:
┌───────────────────────────────┐
│ [☰]        Content            │
│                               │
└───────────────────────────────┘
  ← Sidebar slides in on toggle
```

### Responsive Table

```
Desktop: tabela completa com todas as colunas

Tablet: colunas secundarias colapsadas
┌────────┬────────┬────────┐
│ Nome   │ Status │ [...]  │ ← mais detalhes em expandable row
└────────┴────────┴────────┘

Mobile: card list
┌──────────────────────┐
│ Ana Silva            │
│ Status: Ativo        │
│ Data: 15/01/2026     │
│ [Editar] [Excluir]   │
└──────────────────────┘
```

### Adaptive Content

```
Desktop: titulo completo + descricao + imagem + metadata
Tablet: titulo completo + descricao truncada + imagem
Mobile: titulo truncado + imagem (descricao via expandir)
```

### Responsive Spacing

```css
:root {
  --page-padding: var(--spacing-lg); /* 24px mobile */
}
@media (min-width: 768px) {
  :root { --page-padding: var(--spacing-xl); } /* 32px tablet */
}
@media (min-width: 1024px) {
  :root { --page-padding: var(--spacing-2xl); } /* 48px desktop */
}
```

## Analysis

Principios de adaptacao responsiva:
- Content-first: priorize conteudo sobre chrome/decoracao
- Breakpoints baseados em conteudo, nao em dispositivos
- Teste com conteudo real em cada breakpoint
- Touch targets: minimo 44x44px em mobile
- Evite scroll horizontal — sempre adapte para viewport
- Use container queries quando disponivel para componentes independentes

## Tags

`responsive`, `breakpoints`, `mobile-first`, `adaptive`, `layout`, `container-queries`
