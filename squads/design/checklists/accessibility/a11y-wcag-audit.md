# A11Y WCAG Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Accessibility                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Accessibility Lead             |

## Objective

Conduzir auditoria de conformidade com as diretrizes WCAG (Web Content Accessibility
Guidelines) nivel AA, identificando barreiras de acessibilidade que impedem ou
dificultam o uso do produto por pessoas com deficiencia. Conformidade WCAG e requisito
legal em muitas jurisdicoes e principio fundamental de design inclusivo.

## When to Apply

- Em auditorias semestrais de acessibilidade do produto.
- Antes de lancamentos major de features ou redesigns.
- Quando ha requisitos legais ou contratuais de conformidade.
- Ao receber feedback de usuarios com deficiencia.

## Criteria

- [ ] Perceivable: todo conteudo nao-textual possui alternativa textual (alt text, captions).
- [ ] Perceivable: conteudo de audio e video possui legendas e/ou transcricao.
- [ ] Perceivable: contraste de texto atinge minimo 4.5:1 (AA) para texto normal.
- [ ] Perceivable: conteudo e compreensivel sem depender exclusivamente de cor.
- [ ] Operable: toda funcionalidade e acessivel via teclado sem armadilhas de foco.
- [ ] Operable: usuario tem tempo suficiente para interagir (sem timeouts agressivos).
- [ ] Operable: conteudo nao causa convulsoes (nada pisca mais que 3 vezes por segundo).
- [ ] Operable: navegacao e consistente e previsivel em todas as paginas.
- [ ] Understandable: linguagem da pagina esta definida no atributo lang.
- [ ] Understandable: formularios possuem labels associadas e instrucoes claras.
- [ ] Understandable: erros sao identificados e sugestoes de correcao sao fornecidas.
- [ ] Robust: HTML e semantico e validado sem erros significativos.
- [ ] Robust: componentes customizados possuem roles e states ARIA corretos.
- [ ] Ferramenta automatizada (axe, Lighthouse) e executada e resultados documentados.
- [ ] Testes manuais complementam resultados automatizados em fluxos criticos.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Funcionalidade inacessivel via teclado ou contraste abaixo de 3:1.       |
| Major    | Imagens sem alt text ou formularios sem labels associadas.                |
| Minor    | Atributo lang ausente ou heading levels fora de ordem.                   |
| Info     | Oportunidade de atingir nivel AAA ou melhorar experiencia assistiva.     |

## Cross-References

- `accessibility/a11y-keyboard-and-focus.md` — Teclado e foco.
- `accessibility/a11y-color-contrast.md` — Contraste de cores.
- `accessibility/a11y-aria-and-semantics.md` — ARIA e semantica.
- `accessibility/a11y-screen-reader-audit.md` — Auditoria de screen reader.
