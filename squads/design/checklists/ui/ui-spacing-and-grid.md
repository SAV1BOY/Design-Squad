# UI Spacing and Grid

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Visual Design                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | UI Lead                        |

## Objective

Verificar se o espacamento e o grid system sao aplicados de forma consistente em
todas as telas do produto, seguindo os tokens definidos no design system. Espacamento
correto cria ritmo visual, melhora legibilidade e reforça a hierarquia de informacao.

## When to Apply

- Em revisoes de design antes do handoff.
- Ao auditar telas existentes para consistencia visual.
- Quando novos breakpoints ou layouts sao adicionados.
- Em revisoes de implementacao pos-desenvolvimento.

## Criteria

- [ ] O grid system (colunas, gutters, margins) esta definido para cada breakpoint.
- [ ] Todos os espacamentos utilizam valores da escala de spacing tokens (4px, 8px, 16px, etc.).
- [ ] Nenhum magic number de espacamento e utilizado fora da escala definida.
- [ ] Padding interno de componentes segue os tokens do design system.
- [ ] Margins entre secoes sao consistentes ao longo de todas as paginas.
- [ ] O grid se adapta corretamente em todos os breakpoints (mobile, tablet, desktop).
- [ ] Alinhamento vertical segue baseline grid ou ritmo vertical consistente.
- [ ] Espacamento entre elementos relacionados e menor que entre elementos nao-relacionados (proximity).
- [ ] Containers e cards utilizam padding proporcional ao seu tamanho.
- [ ] Espacamento e responsivo, ajustando-se proporcionalmente entre breakpoints.
- [ ] Limites de largura maxima (max-width) estao definidos para leitura confortavel.
- [ ] White space e utilizado intencionalmente para criar respiro visual.
- [ ] O grid suporta layouts de 1 a N colunas conforme necessidade do conteudo.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Grid inexistente ou espacamentos completamente inconsistentes.            |
| Major    | Magic numbers frequentes ou grid quebrado em breakpoints.                 |
| Minor    | Desvios pontuais de 1-2px ou padding inconsistente em poucos componentes. |
| Info     | Oportunidade de refinar baseline grid ou melhorar ritmo vertical.         |

## Cross-References

- `ui/ui-visual-hierarchy.md` — Hierarquia visual.
- `ui/ui-component-consistency.md` — Consistencia de componentes.
- `design-system/ds-token-architecture.md` — Arquitetura de tokens.
- `frost/frost-frontend-style-guide-audit.md` — Style guide de frontend.
