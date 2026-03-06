# Handoff Specs and Redlines

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Design Handoff                 |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Handoff Lead                   |

## Objective

Garantir que as especificacoes de design (specs) e redlines estao completas, precisas
e acessiveis para a equipe de engenharia. Specs claras reduzem interpretacoes erradas,
minimizam ciclos de revisao e aceleram a implementacao fiel ao design.

## When to Apply

- Antes de cada handoff formal para engenharia.
- Em revisoes de completude de specs pre-desenvolvimento.
- Quando implementacoes apresentam desvios significativos do design.
- Ao padronizar o processo de handoff entre squads.

## Criteria

- [ ] Todas as telas estao organizadas em paginas nomeadas com convencao clara.
- [ ] Espacamentos (padding, margin) estao anotados com valores em tokens do design system.
- [ ] Tipografia esta especificada: family, size, weight, line-height, letter-spacing.
- [ ] Cores estao referenciadas por token name, nao por valor hexadecimal bruto.
- [ ] Dimensoes de componentes (width, height) estao especificadas.
- [ ] Alinhamento e posicionamento de elementos estao documentados.
- [ ] Comportamento responsivo esta especificado para cada breakpoint.
- [ ] Estados de componentes interativos estao documentados com redlines.
- [ ] Regras de truncamento de texto (overflow, ellipsis, line clamp) estao definidas.
- [ ] Sombras e elevacao estao especificadas com valores do token de shadow.
- [ ] Border-radius de cada componente esta documentado.
- [ ] Z-index e stacking context de overlays estao especificados.
- [ ] O desenvolvedor confirmou que as specs sao suficientes para implementacao.
- [ ] Existe sessao de walkthrough das specs com o desenvolvedor responsavel.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Telas do fluxo ausentes das specs ou valores de cor como hex sem token.  |
| Major    | Responsividade nao especificada ou estados de componentes ausentes.       |
| Minor    | Regras de truncamento nao definidas ou walkthrough nao realizado.         |
| Info     | Oportunidade de automatizar geracao de specs ou melhorar nomeacao.        |

## Cross-References

- `handoff/handoff-assets-export.md` — Exportacao de assets.
- `handoff/handoff-token-sync.md` — Sincronizacao de tokens.
- `prototyping/proto-handoff-readiness.md` — Prontidao do prototipo.
- `frost/frost-frontend-style-guide-audit.md` — Style guide de frontend.
