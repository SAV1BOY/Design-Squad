# UI Dark Mode Quality

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Theming                        |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | UI Lead                        |

## Objective

Avaliar a qualidade da implementacao do dark mode, verificando se cores, contrastes,
imagens e elementos visuais foram adaptados adequadamente. Dark mode bem implementado
reduz fadiga visual, melhora legibilidade em ambientes escuros e respeita as
preferencias do sistema operacional do usuario.

## When to Apply

- Ao implementar dark mode pela primeira vez.
- Em auditorias visuais pos-implementacao de dark mode.
- Quando usuarios reportam problemas de legibilidade em dark mode.
- Ao adicionar novos componentes que precisam suportar dark mode.

## Criteria

- [ ] Cores de background usam tons escuros (nao preto puro #000) para reduzir contraste extremo.
- [ ] Cores de texto em dark mode atingem contraste minimo de 4.5:1 (WCAG AA).
- [ ] Elevacao e representada por clareza de superficie, nao por sombra.
- [ ] Imagens e ilustracoes possuem versoes adaptadas ou overlay para dark mode.
- [ ] Icones com cor fixa foram adaptados para manter visibilidade em fundo escuro.
- [ ] Cores semanticas (success, error, warning) foram ajustadas para manter legibilidade.
- [ ] Inputs e formularios possuem bordas visiveis em fundo escuro.
- [ ] A transicao entre light e dark mode e suave, sem flash de conteudo.
- [ ] O tema respeita a preferencia do sistema operacional (prefers-color-scheme).
- [ ] O usuario pode override manual da preferencia do sistema.
- [ ] Tokens de cor sao mapeados para semantic tokens que adaptam por tema automaticamente.
- [ ] Componentes de terceiros (mapas, embeds, videos) sao compativeis com dark mode.
- [ ] Testes visuais (visual regression) cobrem ambos os temas.
- [ ] Scroll bars e selecoes de texto sao visiveis em dark mode.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Texto ilegivel em dark mode ou contraste abaixo de 3:1.                  |
| Major    | Imagens nao adaptadas ou componentes de terceiros incompativeis.          |
| Minor    | Flash na transicao de tema ou sombras usadas em vez de elevacao.          |
| Info     | Oportunidade de adicionar tema high-contrast ou melhorar transicao.      |

## Cross-References

- `accessibility/a11y-color-contrast.md` — Contraste de cores.
- `design-system/ds-token-architecture.md` — Arquitetura de tokens.
- `frost/frost-frontend-style-guide-audit.md` — Style guide de frontend.
- `ui/ui-component-consistency.md` — Consistencia de componentes.
