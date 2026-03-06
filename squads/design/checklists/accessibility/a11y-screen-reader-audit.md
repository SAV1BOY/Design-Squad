# A11Y Screen Reader Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Accessibility                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Accessibility Lead             |

## Objective

Validar que o produto proporciona experiencia completa e compreensivel quando utilizado
exclusivamente via screen reader. Testes com screen readers reais complementam
auditorias automatizadas e revelam problemas que ferramentas nao detectam, como
ordem de leitura confusa ou anuncios verbosos.

## When to Apply

- Em auditorias trimestrais de acessibilidade.
- Ao lancar novos fluxos ou componentes complexos.
- Quando usuarios de screen reader reportam problemas.
- Apos refatoracoes significativas de HTML ou componentes.

## Criteria

- [ ] Testes foram realizados com pelo menos 2 screen readers (NVDA/JAWS no Windows, VoiceOver no Mac/iOS).
- [ ] Todas as paginas possuem titulo descritivo e unico lido pelo screen reader.
- [ ] Ordem de leitura corresponde a ordem visual logica da pagina.
- [ ] Imagens informativas possuem alt text descritivo e conciso.
- [ ] Imagens decorativas estao ocultas do screen reader (alt="" ou aria-hidden).
- [ ] Formularios anunciam labels, instrucoes e erros de forma compreensivel.
- [ ] Conteudo dinamico (toasts, alerts, live updates) e anunciado via aria-live.
- [ ] Modais anunciam titulo e conteudo ao abrir, e retornam foco ao fechar.
- [ ] Tabelas de dados sao navegaveis com anuncio de headers por celula.
- [ ] Links e botoes possuem nome acessivel que descreve a acao ou destino.
- [ ] Accordions e tabs anunciam estado (expandido/colapsado, selecionado).
- [ ] O fluxo completo (login, principal, checkout) pode ser concluido apenas com screen reader.
- [ ] Nenhum conteudo significativo esta escondido do screen reader sem justificativa.
- [ ] Tempo de resposta nao e prejudicado por anuncios excessivos ou verbosos.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Fluxo critico impossivel de completar via screen reader.                 |
| Major    | Formulario sem labels anunciadas ou conteudo dinamico nao anunciado.     |
| Minor    | Alt text generico (ex.: "imagem") ou anuncios levemente verbosos.        |
| Info     | Oportunidade de melhorar descricoes ou otimizar ordem de anuncios.       |

## Cross-References

- `accessibility/a11y-wcag-audit.md` — Auditoria WCAG.
- `accessibility/a11y-aria-and-semantics.md` — ARIA e semantica.
- `accessibility/a11y-keyboard-and-focus.md` — Teclado e foco.
- `ui/ui-data-visualization-quality.md` — Visualizacao de dados acessivel.
