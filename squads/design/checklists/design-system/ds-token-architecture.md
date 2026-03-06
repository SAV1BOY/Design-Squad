# DS Token Architecture

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Design Tokens                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Design System Lead             |

## Objective

Avaliar a arquitetura de design tokens, verificando se a estrutura de naming, hierarquia
(global, alias, component) e distribuicao estao corretas e sustentaveis. Uma arquitetura
de tokens bem definida e a fundacao de um design system escalavel e tematizavel.

## When to Apply

- Ao criar ou reestruturar o sistema de tokens.
- Antes de adicionar suporte a novos temas (dark mode, high-contrast, white-label).
- Em auditorias semestrais da base de tokens.
- Quando inconsistencias de estilo sao reportadas entre plataformas.

## Criteria

- [ ] Tokens estao organizados em 3 niveis: global (primitivos), alias (semanticos) e component.
- [ ] Global tokens definem valores brutos (color-blue-500, spacing-4) sem contexto de uso.
- [ ] Alias tokens definem intencao (color-primary, color-error, spacing-section).
- [ ] Component tokens vinculam alias tokens a propriedades especificas de componentes.
- [ ] Nomenclatura segue convencao consistente: CTI (Category-Type-Item) ou similar.
- [ ] Tokens sao a single source of truth, usados tanto em design tool quanto em codigo.
- [ ] Existe processo automatizado de sync entre design tool e repositorio de tokens.
- [ ] Tokens suportam multi-theme sem duplicacao de valores.
- [ ] Tokens cobrem todas as propriedades visuais: cor, tipografia, espacamento, sombra, borda, motion.
- [ ] Tokens deprecados possuem alias de migração e aviso de remocao.
- [ ] Existe documentacao completa de cada token com valor, uso e contexto.
- [ ] Tokens sao distribuidos em formatos consumiveis por todas as plataformas (CSS, iOS, Android).
- [ ] Existe validacao automatizada (lint) para uso correto de tokens no codigo.
- [ ] A quantidade de tokens e gerenciavel e nao ha excesso de granularidade.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Tokens nao sao fonte unica de verdade ou divergem entre design e codigo.  |
| Major    | Hierarquia de tokens inexistente (tudo flat) ou naming inconsistente.     |
| Minor    | Tokens deprecados sem alias de migracao ou documentacao incompleta.       |
| Info     | Oportunidade de automatizar sync ou expandir formatos de distribuicao.    |

## Cross-References

- `frost/frost-frontend-style-guide-audit.md` — Style guide de frontend.
- `design-system/ds-design-code-sync-audit.md` — Sincronizacao design-code.
- `design-system/ds-versioning-and-changelog.md` — Versionamento e changelog.
- `ui/ui-dark-mode-quality.md` — Qualidade do dark mode.
