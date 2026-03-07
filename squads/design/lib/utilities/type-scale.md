# Type Scale

## Purpose

Escala tipografica padronizada para hierarquia visual consistente em toda a interface. Define tamanhos, pesos, alturas de linha e espacamento entre letras.

## Scale Definition

```
Token              | Size  | Weight  | Line-H | Letter-S | Uso
-------------------|-------|---------|--------|----------|------------------
--text-xs          | 11px  | 400     | 1.5    | 0.02em   | Captions, footnotes
--text-sm          | 13px  | 400     | 1.5    | 0.01em   | Helper text, labels
--text-md          | 15px  | 400     | 1.5    | 0        | Body text padrao
--text-lg          | 17px  | 400     | 1.4    | -0.01em  | Body enfatizado
--heading-sm       | 20px  | 600     | 1.3    | -0.01em  | Subtitulos, card headers
--heading-md       | 24px  | 600     | 1.25   | -0.02em  | Section headings
--heading-lg       | 32px  | 700     | 1.2    | -0.02em  | Page titles
--heading-xl       | 40px  | 700     | 1.15   | -0.03em  | Hero headings
--display-sm       | 48px  | 800     | 1.1    | -0.03em  | Landing sections
--display-lg       | 64px  | 800     | 1.05   | -0.04em  | Marketing heroes
```

## Font Families

```css
:root {
  --font-family-heading: 'Inter', -apple-system, sans-serif;
  --font-family-body: 'Inter', -apple-system, sans-serif;
  --font-family-mono: 'JetBrains Mono', 'Fira Code', monospace;
}
```

## Application Rules

### Hierarchy Pairing

```
Pattern tipico de pagina:
  Page title:        --heading-lg
  Section heading:   --heading-md
  Subsection:        --heading-sm
  Body:              --text-md
  Helper/caption:    --text-sm
```

### Weight Usage

```
400 (Regular):  body text, paragrafos
500 (Medium):   labels, navigation items
600 (Semibold): headings secundarios, botoes
700 (Bold):     headings principais, enfase forte
800 (Extrabold): display text, marketing
```

### Responsive Typography

```css
@media (max-width: 768px) {
  :root {
    --heading-lg: 28px;  /* reduzido de 32px */
    --heading-xl: 34px;  /* reduzido de 40px */
    --display-sm: 40px;  /* reduzido de 48px */
    --display-lg: 48px;  /* reduzido de 64px */
  }
}
```

## Validation Checklist

- [ ] Maximo 3 niveis de hierarquia por pagina
- [ ] Contraste minimo AA para todos os tamanhos de texto
- [ ] Line-height adequado para blocos longos de texto (>= 1.5)
- [ ] Sem font-size menor que 11px em qualquer contexto
- [ ] Responsive scaling aplicado em mobile

## Usage Notes

- Nunca pule mais de 2 niveis na hierarquia (ex: heading-xl direto para text-sm)
- Use font-weight para criar contraste, nao apenas tamanho
- Letter-spacing negativo em headings melhora legibilidade em tamanhos grandes
- Teste com conteudo em portugues (acentos, cedilha) para validar rendering
