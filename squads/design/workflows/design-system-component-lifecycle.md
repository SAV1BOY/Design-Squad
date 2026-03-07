# Design System Component Lifecycle

## Metadata

| Campo         | Valor                                       |
| ------------- | ------------------------------------------- |
| squad         | Design                                      |
| versao        | 1.0.0                                       |
| criado_em     | 2026-03-06                                  |
| owner         | Design System Lead                          |
| cadencia      | Por componente (continuo)                   |
| duracao_media | 2-4 semanas (proposta ate publish)          |
| tags          | design-system, componente, RFC, lifecycle   |

## Trigger

Quando iniciar:

- Novo componente necessario em 2+ squads.
- Pattern repetido em audit de consistencia.
- Componente existente precisa de major update (breaking change).

Pre-condicoes: necessidade validada (2+ squads); sem componente DS equivalente; DS Lead aprovou inclusao no backlog.

## Phases

### Fase 1 — Proposta
**Agents:** Designer solicitante, DS Lead.
**Inputs:** Necessidade (link do projeto), DS existente, exemplos de uso.
**Atividades:** Solicitante preenche template (nome, problema, contextos de uso, screenshots, por que DS existente nao serve); DS Lead faz triagem (duplicacao, escopo, priorizacao); decisao: aceitar, rejeitar, ou adiar.
**Outputs:** Proposta documentada, decisao de triagem, issue no backlog DS (se aceita).

### Fase 2 — RFC (Request for Comments)
**Agents:** DS Designer, DS Engineer, squads consumidores.
**Inputs:** Proposta aceita, pesquisa de patterns (Material, Carbon, Radix), use cases.
**Atividades:** Elaborar RFC: anatomia (parts, slots), variants (size, color, state), API (props, events), exemplos do/don't, a11y (roles, keyboard, screen reader), responsividade, tokens; publicar para review (3-5 dias); coletar e incorporar feedback; DS Lead aprova.
**Outputs:** RFC aprovado, API finalizada, estimativa de esforco.

### Fase 3 — Build
**Agents:** DS Designer (Figma), DS Engineer (codigo), QA.
**Inputs:** RFC aprovado, tokens, Storybook setup.
**Atividades:** **Figma:** componente com auto-layout, variants, todos os estados. **Codigo:** implementar API do RFC, tokens semanticos, a11y (ARIA, keyboard, focus), testes unitarios (>= 80%), visual regression, Storybook stories. **Sync:** paridade Figma <-> codigo, nomenclatura alinhada.
**Outputs:** Figma component, codigo com testes, Storybook stories, visual regression baseline.

### Fase 4 — Review
**Agents:** DS Lead, Engineer senior, A11y Champion, 1 consumidor.
**Inputs:** Componente Figma e codigo, RFC, checklist de review.
**Atividades:** Design review (DS Lead valida Figma); code review (patterns, performance); a11y review (keyboard, screen reader, contraste); consumer review (integracao no contexto real); corrigir issues e re-review.
**Outputs:** Todas as reviews aprovadas, issues corrigidos.

### Fase 5 — Publish
**Agents:** DS Engineer, DS Designer.
**Inputs:** Componente aprovado, changelog entry, documentacao.
**Atividades:** Publicar Figma library update; publicar package (semver minor); atualizar docs no site; changelog com uso e migration; anunciar no canal DS; atualizar Storybook.
**Outputs:** Library e package publicados, docs live, changelog, anuncio enviado.

### Fase 6 — Maintain
**Agents:** DS team, consumidores.
**Inputs:** Componente em uso, bug reports, feature requests, metricas.
**Atividades:** Monitorar bugs e requests; patches (semver patch); enhancements (minor); deprecation com migration guide; metricas de adocao.
**Outputs:** Componente mantido, metricas trackeadas, feedback loop ativo.

## Quality Gates

### Gate Proposta -> RFC
- [ ] Necessidade validada (2+ squads).
- [ ] Sem duplicacao.

### Gate RFC -> Build
- [ ] RFC revisado por consumidores.
- [ ] API e a11y documentados.
- [ ] DS Lead sign-off.

### Gate Build -> Review
- [ ] Figma com variants e estados.
- [ ] Testes >= 80% cobertura.
- [ ] Paridade Figma <-> codigo.

### Gate Review -> Publish
- [ ] Design, code, a11y e consumer reviews aprovadas.

### Gate Publish -> Maintain
- [ ] Package com semver correto.
- [ ] Docs live e completas.
- [ ] Anuncio enviado.

## Cross-References

- `design-system-bootstrap.md` — Bootstrap cria componentes core iniciais.
- `design-system-migration-workflow.md` — Major versions.
- `design-to-code-sync.md` — Tokens sincronizados.
- `accessibility-remediation-loop.md` — A11y issues em componentes.
- `feature-design-end-to-end.md` — Features consomem componentes.
- `quarterly-design-review.md` — Saude do DS revisada.
