# Component Anatomy Snippets

## Purpose

Referencia rapida para a anatomia estrutural dos componentes mais comuns em design systems. Cada snippet documenta as camadas internas, slots e areas de conteudo que formam um componente.

## Snippets

### Button Anatomy

```
┌─────────────────────────────┐
│  [icon-slot] [label] [icon] │
│  padding: token(spacing-md) │
└─────────────────────────────┘
```

Camadas:
- **Container**: superfície clicavel com border-radius e elevation
- **Label**: texto principal usando token(font-button)
- **Leading icon** (opcional): icone antes do label
- **Trailing icon** (opcional): icone apos o label

### Card Anatomy

```
┌──────────────────────────────┐
│  [media-slot]                │
│  [header]                    │
│  [body]                      │
│  [actions]                   │
└──────────────────────────────┘
```

Camadas:
- **Media**: imagem ou video no topo
- **Header**: titulo e subtitulo
- **Body**: conteudo principal com tipografia body
- **Actions**: botoes ou links de acao

### Input Field Anatomy

```
┌──────────────────────────────┐
│  [label]                     │
│  ┌────────────────────────┐  │
│  │ [prefix] [value] [sfx] │  │
│  └────────────────────────┘  │
│  [helper-text / error]       │
└──────────────────────────────┘
```

Camadas:
- **Label**: rotulo descritivo posicionado acima
- **Container**: borda com estados (default, focus, error, disabled)
- **Prefix/Suffix**: icones ou texto auxiliar
- **Helper text**: descricao ou mensagem de erro

### Modal / Dialog Anatomy

```
┌──────────────────────────────┐
│  [overlay / scrim]           │
│  ┌────────────────────────┐  │
│  │ [header + close]       │  │
│  │ [body / content]       │  │
│  │ [footer / actions]     │  │
│  └────────────────────────┘  │
└──────────────────────────────┘
```

Camadas:
- **Scrim**: overlay semi-transparente (token: color-overlay)
- **Header**: titulo e botao de fechar
- **Body**: conteudo scrollable
- **Footer**: acoes primaria e secundaria

### Tooltip Anatomy

```
     ┌────────────────┐
     │  [content]      │
     └───────▲────────┘
             │ (arrow)
```

Camadas:
- **Container**: fundo escuro com border-radius pequeno
- **Content**: texto curto, max 2 linhas
- **Arrow**: seta apontando para o elemento trigger

## Usage Notes

- Sempre use tokens de spacing para padding interno dos componentes
- A anatomia deve ser consistente entre variantes (size, color, state)
- Documente slots opcionais claramente na API do componente
- Mantenha a hierarquia visual: header > body > actions
- Teste cada camada com conteudo minimo e maximo para validar flexibilidade
- Considere a ordem de leitura para screen readers ao definir a estrutura DOM
