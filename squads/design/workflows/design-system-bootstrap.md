# Design System Bootstrap

## Metadata

| Campo         | Valor                                    |
| ------------- | ---------------------------------------- |
| squad         | Design                                   |
| versao        | 1.0.0                                    |
| criado_em     | 2026-03-06                               |
| owner         | Design System Lead                       |
| cadencia      | One-time (bootstrap) ou major version    |
| duracao_media | 6-10 semanas                             |
| tags          | design-system, tokens, componentes, docs |

## Trigger

Quando iniciar:

- Produto novo sem Design System existente.
- Decisao de unificar multiplos produtos sob um DS.
- DS atual considerado irrecuperavel (divida > valor).

Pre-condicoes: sponsorship de lideranca; time minimo 1 designer + 1 frontend (>= 50%); inventario de telas disponivel.

## Phases

### Fase 1 — Inventario Visual
**Agents:** Designer DS, Frontend Engineer DS, Design Lead.
**Inputs:** Screenshots de todas as telas, CSS audit, brand guidelines.
**Atividades:** Catalogar variantes de cores, tipografia, espacamento, icones; identificar inconsistencias e padroes duplicados; classificar em foundations, components, patterns; priorizar por frequencia.
**Outputs:** Audit board anotado, spreadsheet de inventario, relatorio de divida visual (top 10).

### Fase 2 — Design Tokens
**Agents:** Designer DS, Frontend Engineer DS.
**Inputs:** Inventario visual, brand guidelines, WCAG 2.2 AA.
**Atividades:** Definir primitivos (color, type scale, spacing, radius, shadows); criar semantic tokens; implementar em JSON + CSS custom properties; validar contraste contra WCAG AA; sincronizar Figma Styles/Variables.
**Outputs:** Token file versionado, Figma Variables sincronizados, naming conventions documentadas.

### Fase 3 — Componentes Core
**Agents:** Designer DS, Frontend Engineer DS, QA.
**Inputs:** Tokens, lista priorizada de componentes, API de referencia.
**Atividades:** Selecionar top 10-15 componentes; criar Figma components com auto-layout e variants; implementar em codigo com Storybook; testes unitarios e visual regression; garantir a11y (roles, labels, keyboard, focus); code review cruzado.
**Outputs:** Figma library publicada, npm package, Storybook deployado, testes baseline.

### Fase 4 — Documentacao
**Agents:** Designer DS, Technical Writer, Frontend Engineer DS.
**Inputs:** Componentes implementados, decisoes de design.
**Atividades:** Pagina por componente (quando usar, anatomia, props, exemplos); documentar foundations; guia de contribuicao; changelog e migration guide.
**Outputs:** Site de documentacao publicado, guia de contribuicao, changelog inicial.

### Fase 5 — Adocao
**Agents:** DS team, Design Lead, Tech Leads.
**Inputs:** DS publicado, documentacao, lista de squads alvo.
**Atividades:** Demo day (30-45 min); office hours semanais (4 semanas); pair programming/designing com early adopters; coletar feedback; monitorar % componentes DS vs custom.
**Outputs:** Metricas de adocao baseline, backlog de melhorias, canal de suporte.

## Quality Gates

### Gate Inventario -> Tokens
- [ ] Audit board revisado por Design Lead.
- [ ] Categorias de elementos definidas.

### Gate Tokens -> Componentes
- [ ] Contraste validado WCAG AA.
- [ ] Tokens sincronizados Figma <-> codigo.

### Gate Componentes -> Docs
- [ ] Min 10 componentes core com testes.
- [ ] A11y validada em todos.

### Gate Docs -> Adocao
- [ ] Cada componente com pagina de docs.
- [ ] Guia de contribuicao revisado.

### Gate Adocao -> Manutencao
- [ ] Min 1 squad usando DS em producao.
- [ ] Canal de suporte operacional.

## Cross-References

- `design-system-component-lifecycle.md` — Ciclo de vida pos-bootstrap.
- `design-to-code-sync.md` — Sincronizacao continua de tokens.
- `design-system-migration-workflow.md` — Major version futura.
- `design-debt-reduction-sprint.md` — Divida identificada no inventario.
- `feature-design-end-to-end.md` — Features consomem DS na Fase 3 (UI).
