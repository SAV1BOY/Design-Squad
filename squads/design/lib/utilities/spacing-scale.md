# Spacing Scale

## Purpose

Escala de espacamento padronizada para uso consistente em todos os componentes e layouts. Baseada em uma unidade base de 4px com progressao geometrica controlada.

## Scale Definition

```
Token              | Value  | px   | rem    | Uso tipico
-------------------|--------|------|--------|---------------------------
--spacing-none     | 0      | 0    | 0      | Reset de margem/padding
--spacing-3xs      | 0.25   | 1px  | 0.0625 | Bordas e separadores finos
--spacing-2xs      | 0.5    | 2px  | 0.125  | Gaps minimos entre icones
--spacing-xs       | 1      | 4px  | 0.25   | Padding interno compacto
--spacing-sm       | 2      | 8px  | 0.5    | Gap entre elementos inline
--spacing-md       | 4      | 16px | 1      | Padding padrao de componentes
--spacing-lg       | 6      | 24px | 1.5    | Gap entre secoes de form
--spacing-xl       | 8      | 32px | 2      | Margin entre blocos de conteudo
--spacing-2xl      | 12     | 48px | 3      | Separacao entre secoes de pagina
--spacing-3xl      | 16     | 64px | 4      | Espacamento de hero sections
--spacing-4xl      | 24     | 96px | 6      | Margem vertical de pagina
```

## Application Rules

### Componentes Internos (padding)
```
Componente compacto (badge, tag):     --spacing-xs a --spacing-sm
Componente medio (button, input):     --spacing-sm a --spacing-md
Componente grande (card, modal):      --spacing-md a --spacing-lg
```

### Layout (gaps e margens)
```
Entre elementos inline:               --spacing-sm
Entre campos de formulario:           --spacing-md
Entre secoes de conteudo:             --spacing-xl
Entre blocos de pagina:               --spacing-2xl a --spacing-3xl
```

### Responsive Adjustments
```
Mobile:   base spacing (valores acima)
Tablet:   +1 step para gaps de secao
Desktop:  +1-2 steps para gaps de secao e page margins
```

## Design Principles

- **Consistencia**: use apenas tokens da escala, nunca valores arbitrarios
- **Ritmo vertical**: mantenha espacamento consistente para criar ritmo visual
- **Hierarquia**: mais espaco = mais separacao visual = menos relacao percebida
- **Respiro**: elementos criticos precisam de mais espaco ao redor
- **Proporcao**: mantenha relacoes proporcionais entre padding e margin

## Validation Checklist

- [ ] Nenhum valor magico de spacing no codigo
- [ ] Espacamento consistente entre componentes similares
- [ ] Ritmo vertical perceptivel em paginas longas
- [ ] Responsive spacing aplicado em todos os breakpoints
- [ ] Touch targets com espacamento adequado (min 8px entre alvos)

## Usage Notes

- A unidade base de 4px facilita alinhamento em grids de 4/8px
- Para micro-ajustes, use 2xs (2px) — nunca 1px manual
- Em sistemas com density modes (compact/comfortable/spacious), escale toda a escala
- Documente excecoes com comentarios no codigo
