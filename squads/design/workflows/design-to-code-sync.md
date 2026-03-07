# Design to Code Sync

## Metadata

| Campo         | Valor                                     |
| ------------- | ----------------------------------------- |
| squad         | Design                                    |
| versao        | 1.0.0                                     |
| criado_em     | 2026-03-06                                |
| owner         | Design System Lead + Frontend Lead        |
| cadencia      | Continuo (a cada mudanca de token)        |
| duracao_media | 1-3 dias por ciclo                        |
| tags          | tokens, sync, design-to-code, deploy      |

## Trigger

Quando iniciar:

- Token criado ou modificado no Figma.
- Atualizacao de brand (cores, tipografia, espacamento).
- Novo componente DS que introduz tokens.
- Auditoria identifica drift entre Figma e codigo.
- Mudanca de tema (dark mode, high contrast).

Pre-condicoes: source of truth definida (Figma Variables / Tokens Studio / JSON); pipeline de transformacao configurado (Style Dictionary); repositorio versionado; CI/CD automatizado.

## Phases

### Fase 1 — Design Tokens (Figma)
**Agents:** DS Designer, Design Lead (review).
**Inputs:** Necessidade de token, naming convention, estrutura vigente.
**Atividades:** Criar/modificar token no Figma (Variables ou plugin); naming: `{category}-{property}-{variant}-{state}` (ex: `color-text-primary`); definir valores por tema (light, dark, high-contrast); validar hierarquia primitivo -> semantico -> componente; documentar motivo da mudanca; Design Lead revisa.
**Outputs:** Token no Figma, changelog entry, aprovacao.

### Fase 2 — Code Tokens (Transformacao)
**Agents:** DS Engineer, DS Designer (validacao).
**Inputs:** Token exportado (JSON), pipeline Style Dictionary, formatos alvo.
**Atividades:** Exportar tokens do Figma para JSON; validar JSON (naming, valores, sem duplicatas); executar pipeline: CSS (`--color-text-primary`), SCSS, JS/TS, iOS, Android; revisar output; rodar testes (schema validation, contrast check, referencias validas); abrir PR.
**Outputs:** Token files em todos os formatos, testes passando, PR aberto.

### Fase 3 — Deploy
**Agents:** DS Engineer, CI/CD.
**Inputs:** PR aprovado, CI/CD configurado, semver strategy.
**Atividades:** Code review e merge; CI/CD automatico: build, publish, version bump (patch: correcao / minor: novo token / major: token removido/renomeado); notificar squads; atualizar docs.
**Outputs:** Package publicado, squads notificados, docs atualizadas, release notes.

### Fase 4 — Verify
**Agents:** DS Designer, DS Engineer, QA.
**Inputs:** Package publicado, app consumidora, Figma como ref.
**Atividades:** Atualizar tokens em app de referencia (staging); comparacao visual Figma vs staging; verificar temas; spot-check componentes afetados; visual regression tests; validar sem valores hard-coded sobrescrevendo; registrar drift issues.
**Outputs:** Validacao concluida, drift issues registrados, sign-off de paridade, baseline atualizado.

## Automacao Recomendada

1. **Figma -> JSON:** Plugin com export via webhook.
2. **JSON -> Code:** Style Dictionary no CI (push trigger).
3. **Publish:** GitHub Actions para build e publish automatico.
4. **Notify:** Slack bot no canal DS a cada release.
5. **Verify:** Visual regression no PR de cada app que atualiza tokens.
6. **Drift detection:** Cron semanal comparando Figma API vs token files.

## Quality Gates

### Gate Figma -> Code
- [ ] Token segue naming convention.
- [ ] Todos os temas com valor.
- [ ] Design Lead aprovou.

### Gate Code -> Deploy
- [ ] JSON validado (schema + contrast).
- [ ] Formatos gerados corretamente.
- [ ] Testes passando.

### Gate Deploy -> Verify
- [ ] Package com semver correto.
- [ ] Docs atualizadas.

### Gate Verify -> Fechamento
- [ ] Comparacao visual concluida.
- [ ] Visual regression passando.
- [ ] Baseline atualizado.

## Cross-References

- `design-system-bootstrap.md` — Tokens definidos na Fase 2 do bootstrap.
- `design-system-component-lifecycle.md` — Componentes consomem tokens.
- `design-system-migration-workflow.md` — Major version de tokens.
- `handoff-and-build-loop.md` — Tokens sincronizados antes do build.
- `feature-design-end-to-end.md` — Features usam tokens semanticos.
- `accessibility-remediation-loop.md` — Tokens de contraste validados.
