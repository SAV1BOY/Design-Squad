# Design System Migration Workflow

## Metadata

| Campo         | Valor                                             |
| ------------- | ------------------------------------------------- |
| squad         | Design                                            |
| versao        | 1.0.0                                             |
| criado_em     | 2026-03-06                                        |
| owner         | Design System Lead                                |
| cadencia      | Por major version do DS                           |
| duracao_media | 2-4 meses (planejamento ate sunset v1)            |
| tags          | design-system, migration, breaking-changes, rollout|

## Trigger

Quando iniciar:

- DS precisa de breaking changes impossiveis em minor/patch.
- Mudanca de tecnologia (e.g., CSS-in-JS -> CSS Modules).
- Mudanca massiva de token structure (rename, nova hierarquia).
- Rebranding completo que afeta foundations.
- Merge de dois DS (pos-aquisicao).

Pre-condicoes: justificativa documentada (por que minor nao resolve); sponsorship de Design Lead + Eng Manager; inventario de consumidores; timeline realista aprovado.

## Phases

### Fase 1 — Planning
**Agents:** DS Lead, DS Engineer, Design Lead, Tech Leads.
**Inputs:** Breaking changes necessarias, inventario de consumidores, arquitetura atual vs proposta.
**Atividades:** Catalogar breaking changes (tokens renomeados/removidos, APIs alteradas, componentes deprecados, mudancas de build/imports); avaliar impacto por squad; definir phasing (phased rollout recomendado, coexistence period v1+v2); timeline com milestones (alpha -> beta -> RC -> GA -> sunset v1); migration guide (rascunho); comunicar plano.
**Outputs:** Catalogo de breaking changes, phasing strategy, timeline, migration guide rascunho, comunicacao inicial.

### Fase 2 — Build (DS v2)
**Agents:** DS Designer, DS Engineer, A11y Champion.
**Inputs:** Breaking changes, arquitetura proposta, DS v1.
**Atividades:** Implementar nova arquitetura de tokens (migrar/renomear, temas, validar a11y); migrar componentes para nova API (testes, a11y); criar Figma library v2 (nova, nao sobrescrever v1); criar codemods e migration scripts (renomear tokens, atualizar imports, migrar props); testar codemods; criar compatibility layer se viavel (wrapper API v1 -> impl v2).
**Outputs:** DS v2 alpha (tokens + componentes + Figma), codemods, compatibility layer, testes passando.

### Fase 3 — Migration Guide e Tooling
**Agents:** DS Lead, DS Engineer, Technical Writer.
**Inputs:** DS v2 alpha, catalogo de breaking changes, codemods.
**Atividades:** Migration guide completo (visao geral, passo-a-passo por componente, antes/depois, como usar codemods, troubleshooting); checklist por squad; documentar compatibility layer; release notes; canal de suporte dedicado (Slack); preparar workshop de migracao.
**Outputs:** Guide completo, checklist por squad, release notes, canal de suporte, workshop preparado.

### Fase 4 — Phased Rollout
**Agents:** DS team, Tech Leads, Engineers dos squads.
**Inputs:** DS v2 beta/RC, guide, tooling, phasing strategy.
**Atividades:** **Wave 1 (1-2 early adopters):** migrar com suporte proximo, coletar feedback, iterar guide e tooling. **Wave 2:** workshop + migracao com suporte via canal + office hours. **Wave 3+:** migracao autonoma. Monitorar dashboard (% migrados, issues). Figma migration: squads swap para library v2.
**Outputs:** Squads migrados por wave, dashboard atualizado, feedback incorporado.

### Fase 5 — Sunset v1
**Agents:** DS Lead, Design Lead, Tech Leads.
**Inputs:** Dashboard de migracao, timeline, issues pendentes.
**Atividades:** Comunicar deadline (min 1 mes antecedencia); suporte direto para squads restantes; deprecation warnings no package v1; remover compatibility layer apos grace period; arquivar v1 (Figma archive, package final com deprecation notice, docs marcadas deprecated); post-mortem; atualizar workflows para v2.
**Outputs:** v1 archived, v2 unica versao ativa, post-mortem, workflows atualizados, metricas finais.

## Quality Gates

### Gate Planning -> Build
- [ ] Breaking changes catalogadas com impacto.
- [ ] Phasing strategy aprovada.
- [ ] Timeline com milestones.

### Gate Build -> Guide
- [ ] v2 alpha feature-complete.
- [ ] Componentes testados.
- [ ] Figma library v2 criada.
- [ ] Codemods testados.

### Gate Guide -> Rollout
- [ ] Guide completo e revisado.
- [ ] Canal de suporte operacional.
- [ ] v2 beta/RC publicado.

### Gate Rollout -> Sunset
- [ ] Early adopters migrados.
- [ ] >= 80% squads migrados.
- [ ] Nenhum issue critico pendente.

### Gate Sunset -> Fechamento
- [ ] 100% migrados (ou excecoes documentadas).
- [ ] v1 archived.
- [ ] Post-mortem realizado.

## Cross-References

- `design-system-bootstrap.md` — Bootstrap cria v1; este migra para v2+.
- `design-system-component-lifecycle.md` — Lifecycle dentro de cada versao.
- `design-to-code-sync.md` — Token sync para nova estrutura.
- `design-debt-reduction-sprint.md` — Migracao como oportunidade de pagar divida.
- `product-redesign-workflow.md` — Redesign pode acionar migration.
- `quarterly-design-review.md` — Progresso revisado trimestralmente.
- `new-designer-onboarding.md` — Onboarding atualizado para v2.
