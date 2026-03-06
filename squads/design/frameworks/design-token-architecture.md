# Design Token Architecture

## Metadata
- **Autor**: Design Squad
- **Categoria**: Design Systems, Tokens, Arquitetura
- **Complexidade**: Alta
- **Aplicacao**: Arquitetura de tokens em tres camadas — global, alias, component
- **Ultima atualizacao**: 2026-03-06

## Concept

Design Token Architecture define a estrutura hierarquica de tokens de design em tres
camadas: Global Tokens (valores primitivos), Alias Tokens (significado semantico) e
Component Tokens (valores especificos de componente). Essa arquitetura permite que um
unico design system suporte multiplas marcas, temas (light/dark) e plataformas.

Tokens sao as decisoes de design mais atomicas — cores, tamanhos, espacamentos, fontes —
codificadas em formato consumivel por design tools e codigo. A arquitetura em tres camadas
cria indirection: componentes nao referenciam valores brutos, referenciam tokens semanticos,
que por sua vez referenciam tokens globais. Isso permite mudar a aparencia inteira do sistema
alterando apenas uma camada.

## When to Use

- Quando se constroi ou reestrutura a fundacao de um design system
- Quando se precisa suportar dark mode, themes ou multi-brand
- Quando valores visuais estao hardcoded e inconsistentes no codigo
- Quando designers e devs usam valores diferentes para as mesmas propriedades
- Quando se planeja migrar o design system para novas plataformas
- Quando se quer automacao de design decisions (Figma -> codigo)

## How to Apply

### Camada 1 — Global Tokens (Primitivos)
Valores brutos sem significado semantico. Sao a paleta crua disponivel.

```json
{
  "color": {
    "blue-50": "#EFF6FF",
    "blue-100": "#DBEAFE",
    "blue-500": "#3B82F6",
    "blue-600": "#2563EB",
    "blue-900": "#1E3A8A",
    "gray-50": "#F9FAFB",
    "gray-900": "#111827"
  },
  "spacing": {
    "1": "4px",
    "2": "8px",
    "3": "12px",
    "4": "16px",
    "6": "24px",
    "8": "32px"
  },
  "font-size": {
    "xs": "12px",
    "sm": "14px",
    "md": "16px",
    "lg": "18px",
    "xl": "20px"
  }
}
```

### Camada 2 — Alias Tokens (Semanticos)
Significado atribuido, referenciando global tokens. Sao onde themes se diferenciam.

```json
{
  "color-bg-primary": "{color.white}",
  "color-bg-secondary": "{color.gray-50}",
  "color-bg-inverse": "{color.gray-900}",
  "color-text-primary": "{color.gray-900}",
  "color-text-secondary": "{color.gray-600}",
  "color-text-on-primary": "{color.white}",
  "color-action-primary": "{color.blue-600}",
  "color-action-primary-hover": "{color.blue-700}",
  "color-feedback-success": "{color.green-600}",
  "color-feedback-error": "{color.red-600}",
  "spacing-inline-sm": "{spacing.2}",
  "spacing-inline-md": "{spacing.4}",
  "spacing-stack-sm": "{spacing.2}",
  "spacing-stack-md": "{spacing.4}"
}
```

### Camada 3 — Component Tokens
Especificos de cada componente, referenciando alias tokens.

```json
{
  "button-bg-primary": "{color-action-primary}",
  "button-bg-primary-hover": "{color-action-primary-hover}",
  "button-text-primary": "{color-text-on-primary}",
  "button-padding-x": "{spacing-inline-md}",
  "button-padding-y": "{spacing-stack-sm}",
  "button-border-radius": "{radius-md}",
  "input-bg": "{color-bg-primary}",
  "input-border": "{color-border-default}",
  "input-border-focus": "{color-action-primary}",
  "input-text": "{color-text-primary}"
}
```

### Implementacao
1. Defina global tokens como paleta completa (50+ tokens)
2. Crie alias tokens para light theme como default
3. Crie alias tokens para dark theme como override
4. Defina component tokens para cada componente do sistema
5. Implemente em formato padrao: JSON -> CSS Custom Properties + Figma Variables
6. Sincronize Figma e codigo via tooling (Tokens Studio, Style Dictionary)
7. Valide que nenhum componente usa global tokens diretamente

## Key Principles

- **Indirection e poder**: Componentes nunca referenciam global tokens diretamente
- **Semantica sobre valor**: Token names descrevem funcao, nao aparencia
- **Theme-ability**: Trocar de tema = trocar alias tokens sem tocar componentes
- **Single source**: Tokens sao definidos em um lugar e distribuidos para todos
- **Naming conventions**: Nomenclatura consistente e previsivel (category-property-variant)
- **Minimal globals**: Paleta global e finita e controlada — nao cresce livremente
- **Platform-agnostic**: Tokens sao formato abstrato, transformados para cada plataforma

## Examples

### Exemplo 1 — Dark Mode via Alias Tokens
Light theme:
- `color-bg-primary` -> `{color.white}` (#FFFFFF)
- `color-text-primary` -> `{color.gray-900}` (#111827)

Dark theme (override apenas alias):
- `color-bg-primary` -> `{color.gray-900}` (#111827)
- `color-text-primary` -> `{color.gray-50}` (#F9FAFB)

Componentes nao mudam nada — referenciam os mesmos alias tokens.

### Exemplo 2 — Multi-Brand
Brand A:
- `color-action-primary` -> `{color.blue-600}`

Brand B:
- `color-action-primary` -> `{color.purple-600}`

Mesmos componentes, mesmos component tokens, mesmos alias tokens names.
Apenas os valores dos alias tokens mudam entre marcas.

### Exemplo 3 — Migration de Hardcoded para Tokens
Antes (CSS):
```css
.button { background: #2563EB; padding: 8px 16px; }
```
Depois (CSS com tokens):
```css
.button {
  background: var(--button-bg-primary);
  padding: var(--button-padding-y) var(--button-padding-x);
}
```
A migracao foi feita em 3 sprints com codemod automatizado.

## Common Pitfalls

- **Token explosion**: Criar token para cada valor possivel gera centenas de tokens inuteis.
  Comece com ~50 globais, ~80 alias, component tokens conforme demanda
- **Nomes ruins**: `color-1`, `blue-primary-dark` sao ambiguos. Use convencao semantica
- **Skip alias layer**: Ir direto de global para componente impossibilita theming
- **Tokens no design tool desincronizados com codigo**: Use tooling de sincronizacao
- **Over-engineering para single brand**: Se nao precisa de multi-brand, simplifique
- **Component tokens para tudo**: Nem toda propriedade precisa de component token.
  Use alias tokens diretamente quando faz sentido
- **Nao documentar convencoes**: Sem convencao de naming documentada, cada pessoa inventa

## Cross-References

- [design-system-layer.md](design-system-layer.md) — Tokens como fundacao do DS
- [ui-layer.md](ui-layer.md) — Decisoes visuais codificadas em tokens
- [multi-brand-design-system.md](multi-brand-design-system.md) — Theming via tokens
- [component-spec-framework.md](component-spec-framework.md) — Tokens por componente
- [handoff-layer.md](handoff-layer.md) — Tokens como lingua do handoff
- [frost-atomic-design-methodology.md](frost-atomic-design-methodology.md) — Tokens como atoms
