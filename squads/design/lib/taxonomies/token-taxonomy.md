# Token Taxonomy

## Purpose

Taxonomia de design tokens organizados em tres camadas: global (primitivos), alias (semanticos) e component (especificos). Define a hierarquia e convencao de nomenclatura.

## Token Layers

```
Layer 1: Global Tokens (Primitivos)
    ↓ referenciados por
Layer 2: Alias Tokens (Semanticos)
    ↓ referenciados por
Layer 3: Component Tokens (Especificos)
```

### Layer 1 — Global Tokens

```
Categoria     | Pattern de Nome            | Exemplo
--------------|---------------------------|---------------------------
Color         | color-{hue}-{shade}       | color-blue-600
Typography    | font-{property}-{scale}   | font-size-md
Spacing       | spacing-{scale}           | spacing-lg
Border        | radius-{scale}            | radius-md
Shadow        | shadow-{scale}            | shadow-lg
Opacity       | opacity-{scale}           | opacity-50
Motion        | duration-{scale}          | duration-normal
              | ease-{type}              | ease-out
```

### Layer 2 — Alias Tokens

```
Categoria     | Pattern de Nome            | Exemplo
--------------|---------------------------|---------------------------
Surface       | color-surface-{role}      | color-surface-default
Text          | color-text-{role}         | color-text-subtle
Action        | color-action-{role}       | color-action-primary
Feedback      | color-feedback-{type}     | color-feedback-error
Border        | color-border-{role}       | color-border-focus
Heading       | heading-{size}            | heading-lg
Body          | body-{size}               | body-md
Space         | space-{context}           | space-page-margin
```

### Layer 3 — Component Tokens

```
Categoria     | Pattern de Nome                     | Exemplo
--------------|-------------------------------------|---------------------------
Button        | button-{property}-{variant}-{state} | button-bg-primary-hover
Input         | input-{property}-{state}            | input-border-focus
Card          | card-{property}                     | card-padding
Badge         | badge-{property}-{variant}          | badge-bg-success
Modal         | modal-{property}                    | modal-overlay-opacity
```

## Naming Convention

```
Formato geral: {category}-{property}-{variant}-{state}

Regras:
- Sempre kebab-case (minusculas com hifen)
- Maximo 4 segmentos
- Categoria obrigatoria
- Property obrigatoria
- Variant e state opcionais
- Nao incluir valor no nome (nao: color-blue, sim: color-action-primary)
```

## Token Lifecycle

```
1. Proposta: designer propoe novo token com justificativa
2. Review: equipe valida necessidade e nomenclatura
3. Criacao: token adicionado aos 3 layers conforme necessidade
4. Documentacao: adicionado ao registry com exemplos de uso
5. Deprecacao: marcado como deprecated com alternativa sugerida
6. Remocao: removido apos periodo de migracao (1 release cycle)
```

## Validation Rules

```
- Global tokens nunca devem ser usados diretamente em componentes
- Alias tokens sao a camada primaria de consumo
- Component tokens sao opcionais — use quando alias nao e especifico o suficiente
- Todo token deve ter valor definido para light e dark themes
- Nomes devem ser auto-explicativos sem precisar ver o valor
```

## Usage Notes

- Mantenha o catalogo de tokens em formato JSON para tooling
- Use ferramentas como Style Dictionary para gerar tokens multi-plataforma
- Audite tokens nao utilizados trimestralmente
- Documente a relacao entre layers para facilitar debugging
