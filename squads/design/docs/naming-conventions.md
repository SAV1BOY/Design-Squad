# Naming Conventions

## Overview

Convenções de nomenclatura para todos os artefatos do Design Squad — arquivos Figma,
componentes, tokens, layers, branches e documentos. Nomenclatura consistente reduz
tempo de busca, evita duplicatas e facilita automação.

## Content

### Princípios Gerais

1. **Inglês para nomes técnicos** — Componentes, tokens, variáveis em inglês
2. **Português para conteúdo** — Labels, documentação, comentários em PT-BR
3. **kebab-case para arquivos** — `design-review-standards.md`
4. **PascalCase para componentes** — `ButtonPrimary`, `CardProduct`
5. **camelCase para tokens** — `colorActionPrimary` (ou kebab: `color-action-primary`)
6. **Sem acentos em nomes técnicos** — Sem caracteres especiais
7. **Descritivo sobre abreviado** — `backgroundColor` não `bgClr`

### Figma

#### Files
- Pattern: `[Produto] — [Feature] — [Status]`
- Exemplos:
  - `Checkout — Redesign Form — In Progress`
  - `Onboarding — Welcome Flow — Handed Off`
  - `DS Core — Component Library — v3.2`
- Status permitidos: `Exploration` | `In Progress` | `Review` | `Handed Off` | `Archive`

#### Pages (dentro do file)
- Pattern: `[Fase] — [Conteúdo]`
- Exemplos:
  - `01 — Cover`
  - `02 — Research & References`
  - `03 — Wireframes`
  - `04 — Design — Desktop`
  - `05 — Design — Mobile`
  - `06 — Handoff`
  - `07 — Archive`

#### Frames
- Pattern: `[Tela/Seção] / [Estado] / [Viewport]`
- Exemplos:
  - `Login / Default / Desktop`
  - `Login / Error / Mobile`
  - `Dashboard / Loading / Tablet`

#### Layers
- Auto Layout frames: nome descritivo — `Header`, `Content Area`, `Footer Actions`
- Não aceitar: `Frame 1`, `Group 3`, `Rectangle 47`
- Ícones: prefixo `icon/` — `icon/arrow-left`, `icon/check`

#### Components
- Pattern: `[Categoria] / [Nome] / [Variante]`
- Exemplos:
  - `Button / Primary / Default`
  - `Button / Primary / Hover`
  - `Card / Product / With Image`
  - `Input / Text / Error`

### Design Tokens

#### Token Naming Architecture

```
[category]-[property]-[element]-[variant]-[state]
```

#### Primitive Tokens (raw values)
- `color-blue-500` → #1A73E8
- `color-gray-100` → #F5F5F5
- `font-size-16` → 16px
- `spacing-16` → 16px
- `radius-8` → 8px

#### Semantic Tokens (meaning)
- `color-action-primary` → {color-blue-500}
- `color-text-primary` → {color-gray-900}
- `color-surface-primary` → {color-white}
- `color-feedback-error` → {color-red-500}
- `color-feedback-success` → {color-green-500}

#### Component Tokens (scoped)
- `button-color-bg-default` → {color-action-primary}
- `button-color-bg-hover` → {color-blue-600}
- `button-color-text` → {color-white}
- `card-color-bg` → {color-surface-primary}
- `card-shadow` → {shadow-md}

### Documents

#### Files
- kebab-case: `design-review-standards.md`
- Prefixo de tipo quando relevante: `adr-001-color-system.md`
- Sem numeração genérica: não `doc-01.md` mas `getting-started.md`

#### Headings dentro de docs
- H1: Título do documento (1 por doc)
- H2: Seções principais
- H3: Sub-seções
- Nunca pular nível (H1 → H3 sem H2)

### Git / Branches

- Feature: `design/feature-[nome]`
- Fix: `design/fix-[nome]`
- Token update: `design/tokens-[descrição]`
- Exemplo: `design/feature-checkout-redesign`

## Cross-References

- `docs/design-system-governance.md` — Governança que usa estas convenções
- `docs/handoff-standards.md` — Handoff que segue estas convenções
- `docs/documentation-style.md` — Estilo de documentação
