# UI Visual Hierarchy

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Visual Design                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | UI Lead                        |

## Objective

Avaliar se a hierarquia visual das telas orienta o olhar do usuario de forma eficaz,
destacando elementos de maior importancia e subordinando elementos secundarios. Uma
hierarquia visual clara reduz carga cognitiva, acelera a compreensao e direciona
o usuario para as acoes desejadas.

## When to Apply

- Em revisoes de design de telas novas ou redesenhadas.
- Quando testes de usabilidade indicam confusao sobre a acao principal.
- Em auditorias de consistencia visual entre telas e fluxos.
- Ao avaliar landing pages ou telas de conversao.

## Criteria

- [ ] A escala tipografica define niveis claros de headings (H1-H6) com contraste suficiente.
- [ ] Existe um unico ponto focal principal (hero element) por tela ou secao.
- [ ] CTAs primarios, secundarios e terciarios sao visualmente distintos entre si.
- [ ] Tamanho, cor e peso tipografico sao usados consistentemente para indicar importancia.
- [ ] Elementos de menor prioridade sao visualmente subordinados (menor tamanho, cor neutra).
- [ ] O fluxo de leitura (F-pattern ou Z-pattern) e respeitado no layout.
- [ ] Contraste entre foreground e background reforça a hierarquia.
- [ ] White space e utilizado para separar niveis hierarquicos distintos.
- [ ] Icones e imagens complementam a hierarquia, nao competem com texto.
- [ ] A hierarquia se mantém consistente entre telas do mesmo fluxo.
- [ ] Squint test (olhar borrado) revela os elementos principais corretamente.
- [ ] A hierarquia funciona em diferentes tamanhos de tela sem perder clareza.
- [ ] Elementos interativos sao visualmente distinguiveis de elementos estaticos.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Nenhum ponto focal claro ou hierarquia plana sem distincao de niveis.    |
| Major    | CTA primario nao se destaca ou compete visualmente com elementos secundarios. |
| Minor    | Hierarquia inconsistente entre telas do mesmo fluxo.                     |
| Info     | Oportunidade de refinar uso de white space ou melhorar squint test.      |

## Cross-References

- `ui/ui-spacing-and-grid.md` — Espacamento e grid.
- `ux/ux-cognitive-load-audit.md` — Carga cognitiva.
- `ux/ux-information-scent-audit.md` — Information scent.
- `accessibility/a11y-color-contrast.md` — Contraste de cores.
