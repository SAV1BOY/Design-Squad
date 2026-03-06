# A11Y ARIA and Semantics

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Accessibility                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Accessibility Lead             |

## Objective

Verificar se o HTML semantico e os atributos ARIA sao utilizados corretamente para
comunicar estrutura, significado e estado dos elementos para tecnologias assistivas.
Semantica correta e a base para uma experiencia acessivel, permitindo que screen
readers e outros assistivos interpretem o conteudo adequadamente.

## When to Apply

- Ao desenvolver novos componentes para o design system.
- Em auditorias de acessibilidade de paginas existentes.
- Quando screen readers nao interpretam corretamente a interface.
- Ao refatorar componentes de HTML nao-semantico para semantico.

## Criteria

- [ ] Elementos HTML semanticos sao priorizados sobre divs genericos (nav, main, article, section).
- [ ] Headings seguem hierarquia logica (H1 > H2 > H3) sem pular niveis.
- [ ] Landmarks (banner, navigation, main, contentinfo) estao definidos na pagina.
- [ ] Listas sao marcadas com ul/ol/li, nao com divs estilizados.
- [ ] Tabelas de dados usam th, scope e caption para estrutura semantica.
- [ ] Formularios usam label associado via for/id ou wrapping.
- [ ] Botoes usam button element, nao div ou span com onClick.
- [ ] Links usam a element com href, nao span ou div simulando link.
- [ ] ARIA roles sao usados somente quando HTML semantico nao e suficiente.
- [ ] aria-label e aria-labelledby sao usados para elementos sem texto visivel.
- [ ] aria-live regions notificam mudancas dinamicas de conteudo.
- [ ] aria-expanded, aria-selected, aria-checked refletem estado atual do componente.
- [ ] aria-hidden e tabindex="-1" sao usados corretamente para esconder elementos decorativos.
- [ ] Validacao automatizada (axe, WAVE) nao reporta erros de ARIA usage.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Botao implementado como div sem role ou formulario sem labels.            |
| Major    | Landmarks ausentes ou headings fora de hierarquia.                       |
| Minor    | ARIA roles redundantes em elementos nativos ou aria-live mal configurado. |
| Info     | Oportunidade de enriquecer semantica com microdata ou melhorar captions.  |

## Cross-References

- `accessibility/a11y-wcag-audit.md` — Auditoria WCAG.
- `accessibility/a11y-screen-reader-audit.md` — Auditoria de screen reader.
- `accessibility/a11y-keyboard-and-focus.md` — Teclado e foco.
- `design-system/ds-component-anatomy.md` — Anatomia de componentes.
