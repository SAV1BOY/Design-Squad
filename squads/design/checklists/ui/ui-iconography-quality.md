# UI Iconography Quality

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Visual Design                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | UI Lead                        |

## Objective

Avaliar a qualidade, consistencia e usabilidade da iconografia utilizada no produto.
Icones bem projetados comunicam significado rapidamente, reforçam a identidade visual
e complementam a hierarquia de informacao sem adicionar ruido visual.

## When to Apply

- Ao adicionar novos icones ao icon set do design system.
- Em auditorias visuais trimestrais do produto.
- Quando usuarios reportam confusao sobre significado de icones.
- Ao migrar ou unificar icon sets de diferentes fontes.

## Criteria

- [ ] Todos os icones seguem grid e tamanhos padronizados (16px, 20px, 24px, etc.).
- [ ] Stroke width e consistente em todo o icon set.
- [ ] Corner radius e angulos sao uniformes em toda a colecao.
- [ ] Icones sao pixel-perfect nos tamanhos definidos (sem blur ou antialiasing excessivo).
- [ ] Cada icone possui significado claro e reconhecivel sem texto de apoio.
- [ ] Icones ambiguos sao sempre acompanhados de label descritivo.
- [ ] O icon set cobre todas as acoes e conceitos necessarios do produto.
- [ ] Icones duplicados ou muito similares foram eliminados.
- [ ] Icones possuem versoes filled e outlined quando necessario para indicar estado.
- [ ] Export e feito em SVG otimizado com paths limpos e sem elementos desnecessarios.
- [ ] Icones possuem aria-label ou alt text para acessibilidade.
- [ ] A biblioteca de icones e pesquisavel por nome, categoria e tag.
- [ ] Icones sao testados em contexto real para validar legibilidade em tamanho minimo.
- [ ] Existe processo definido para solicitar novos icones ao time de design.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Icones sem acessibilidade (sem aria-label) ou significado ambiguo em acoes criticas. |
| Major    | Inconsistencia de stroke width ou grid entre icones do mesmo set.        |
| Minor    | SVG nao otimizado ou icones duplicados no set.                           |
| Info     | Oportunidade de expandir o set ou melhorar sistema de busca.             |

## Cross-References

- `ui/ui-visual-hierarchy.md` — Hierarquia visual.
- `ui/ui-component-consistency.md` — Consistencia de componentes.
- `accessibility/a11y-aria-and-semantics.md` — ARIA e semantica.
- `handoff/handoff-assets-export.md` — Exportacao de assets.
