# Dark Mode System

## Metadata

| Campo         | Valor                                      |
| ------------- | ------------------------------------------ |
| Categoria     | Design System                              |
| Complexidade  | Alta                                       |
| Autor         | Design Squad                               |
| Versao        | 1.0                                        |
| Ultima revisao| 2026-03-06                                 |
| Tags          | dark-mode, tokens, contrast, theming       |

## Concept

Um dark mode system e uma arquitetura de tokens de cor que permite a alternancia entre temas
claro e escuro de forma sistematica, acessivel e consistente. Nao se trata de "inverter cores" —
e uma reinterpretacao completa da hierarquia visual usando superficies escuras como base.

### Fundamentos

- **Tokens semanticos**: cores referenciadas por funcao (background-primary, text-secondary),
  nao por valor (gray-100, blue-500).
- **Superficies elevadas sao mais claras**: no dark mode, elevacao = luminosidade crescente.
- **Contraste acessivel**: WCAG AA exige minimo 4.5:1 para texto normal, 3:1 para texto grande.
- **Reducao de luminancia total**: dark mode reduz brilho da tela, nao apenas inverte.

### Arquitetura de Tokens

```
Primitive tokens:  gray-900: #1a1a1a, gray-800: #2d2d2d, blue-400: #60a5fa
     |
Semantic tokens:   surface-primary: {gray-900}, text-primary: {gray-50}
     |
Component tokens:  button-bg: {surface-primary}, card-bg: {surface-secondary}
```

## When to Use

- Quando o produto sera usado em ambientes com pouca luz (apps mobile, streaming).
- Quando o publico-alvo inclui usuarios com sensibilidade a luz ou fotofobia.
- Quando ha demanda explicita de usuarios por dark mode.
- Como parte de uma estrategia de design system madura com token architecture.
- Em qualquer produto moderno — dark mode se tornou expectativa de mercado.

## How to Apply

### 1. Definir Semantic Token Map

| Token                 | Light Mode | Dark Mode  | Uso                          |
| --------------------- | ---------- | ---------- | ---------------------------- |
| `surface-base`        | #FFFFFF    | #121212    | Fundo principal              |
| `surface-raised`      | #F5F5F5    | #1E1E1E    | Cards, modals                |
| `surface-overlay`     | #EBEBEB    | #2C2C2C    | Dropdowns, popovers          |
| `text-primary`        | #1A1A1A    | #E0E0E0    | Texto principal              |
| `text-secondary`      | #616161    | #A0A0A0    | Texto auxiliar               |
| `text-disabled`       | #9E9E9E    | #666666    | Texto desabilitado           |
| `border-default`      | #E0E0E0    | #333333    | Bordas de componentes        |
| `interactive-primary` | #1976D2    | #64B5F6    | Botoes, links                |
| `status-error`        | #D32F2F    | #EF5350    | Erros                        |
| `status-success`      | #2E7D32    | #66BB6A    | Sucesso                      |

### 2. Regras de Elevacao

```
Dark mode elevation:
  Level 0 (base):    #121212 (0% overlay)
  Level 1 (card):    #1E1E1E (5% white overlay)
  Level 2 (modal):   #232323 (7% white overlay)
  Level 3 (tooltip): #2C2C2C (11% white overlay)
  Level 4 (popover): #333333 (15% white overlay)
```

### 3. Implementacao CSS

```css
:root {
  --surface-base: #FFFFFF;
  --text-primary: #1A1A1A;
}

[data-theme="dark"] {
  --surface-base: #121212;
  --text-primary: #E0E0E0;
}

@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) {
    --surface-base: #121212;
    --text-primary: #E0E0E0;
  }
}
```

### 4. Validacao de Contraste

- Usar ferramentas como Stark, axe DevTools ou Colour Contrast Analyser.
- Verificar todos os pares token de texto + token de superficie.
- Manter planilha de contraste atualizada a cada mudanca de token.

## Key Principles

- **Semantico, nunca hardcoded**: toda referencia de cor deve usar tokens semanticos.
- **Nao e inversao**: dark mode e um tema paralelo com decisoes proprias.
- **Contraste sempre acessivel**: testar cada combinacao em ambos os temas.
- **Respeitar preferencia do sistema**: usar `prefers-color-scheme` como default.
- **Permitir override manual**: usuario pode forcar light ou dark independente do OS.
- **Persistir escolha**: salvar preferencia do usuario em local storage ou perfil.
- **Shadows vs elevation**: no dark mode, shadows sao invisiveis — usar superficie mais clara.

## Examples

### Toggle de Tema

```
1. Verificar `prefers-color-scheme` do sistema
2. Verificar preferencia salva do usuario (localStorage)
3. Prioridade: preferencia do usuario > sistema > default (light)
4. Aplicar `data-theme` no <html>
5. Transicao suave: `transition: background-color 200ms ease, color 200ms ease`
```

### Imagens e Ilustracoes

```
Light mode: ilustracao com fundo branco, tracos escuros
Dark mode:  mesma ilustracao com fundo transparente, tracos claros
Implementacao: <picture> com media="(prefers-color-scheme: dark)"
Alternativa: filtro CSS — filter: brightness(0.9) para fotos
```

### Status Colors Adaptation

```
Light: error red #D32F2F sobre surface branca (contraste 7.1:1)
Dark:  error red #EF5350 sobre surface #1E1E1E (contraste 5.2:1)
Nota:  a versao dark usa um vermelho mais claro para manter contraste
```

## Common Pitfalls

| Erro                                | Consequencia                        | Correcao                                |
| ----------------------------------- | ----------------------------------- | --------------------------------------- |
| Usar cores hardcoded                | Texto invisivel no dark mode        | Referenciar apenas tokens semanticos    |
| Preto puro (#000000) como fundo     | Contraste excessivo, fadiga visual  | Usar cinza muito escuro (#121212)       |
| Mesmo vermelho em light e dark      | Contraste insuficiente no dark      | Criar variantes de cor por tema         |
| Ignorar imagens e ilustracoes       | Elementos claros "brilham" no dark  | Adaptar assets ou usar filtros          |
| Shadow como unico indicador de depth| Depth invisivel no dark mode        | Usar combinacao de shadow + surface     |
| Nao testar formularios              | Inputs com borda invisivel          | Verificar todos os estados de form      |

## Cross-References

- [Responsive Design System](./responsive-design-system.md) — tokens responsivos que cruzam com temas.
- [Accessibility WCAG AA](./accessibility-wcag-aa.md) — requisitos de contraste para ambos os temas.
- [Design System Governance](./design-system-governance.md) — governanca de tokens de cor.
- [Motion Design System](./motion-design-system.md) — transicao entre temas com motion tokens.
- [Content Design Microcopy](./content-design-microcopy.md) — labels do toggle de tema.
