# UX Information Scent Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Information Architecture       |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | UX Lead                        |

## Objective

Avaliar a qualidade do information scent nos fluxos do produto, verificando se
labels, links, icones e hierarquia de conteudo fornecem pistas suficientes para
que o usuario navegue com confianca ate seu objetivo. Information scent fraco
causa navegacao errante, abandono e frustacao.

## When to Apply

- Em auditorias de arquitetura de informacao.
- Quando analytics mostram caminhos de navegacao confusos ou loops.
- Ao redesenhar menus, navegacao ou estrutura de conteudo.
- Apos testes de tree testing ou card sorting revelarem problemas.

## Criteria

- [ ] Labels de navegacao usam linguagem do usuario, nao jargao interno.
- [ ] Links descritivos indicam claramente o destino (evitar "clique aqui" ou "saiba mais").
- [ ] Icones sao acompanhados de texto descritivo, nao usados isoladamente.
- [ ] Breadcrumbs fornecem contexto de localizacao em hierarquias profundas.
- [ ] A pagina de resultados de busca apresenta snippets relevantes e keywords destacadas.
- [ ] CTAs primarios comunicam claramente a acao e seu resultado esperado.
- [ ] Titulos de pagina e headings refletem o conteudo real da secao.
- [ ] Cards e previews fornecem informacao suficiente para decisao de click/no-click.
- [ ] A hierarquia visual reforça a importancia relativa dos elementos de navegacao.
- [ ] Menus nao ultrapassam 7 itens no nivel principal (Miller's Law).
- [ ] Landing pages comunicam proposta de valor em ate 5 segundos (5-second test).
- [ ] Caminhos alternativos para o mesmo destino sao consistentes e nao conflitantes.
- [ ] Testes de tree testing ou primeiro-click validam a eficacia da estrutura.
- [ ] Conteudo esta organizado por modelo mental do usuario, nao por estrutura organizacional.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Labels de navegacao incompreensiveis ou estrutura baseada em organograma. |
| Major    | Links genericos sem descricao ou icones sem texto.                        |
| Minor    | Breadcrumbs ausentes ou menus com mais de 7 itens.                        |
| Info     | Oportunidade de validar com tree testing ou melhorar snippets de busca.   |

## Cross-References

- `ux/ux-cognitive-load-audit.md` — Carga cognitiva.
- `ux/ux-heuristic-evaluation.md` — Avaliacao heuristica.
- `ui/ui-visual-hierarchy.md` — Hierarquia visual.
- `ui/ui-iconography-quality.md` — Qualidade de iconografia.
