# Publish Library

## Metadata
- **Categoria:** Design System
- **Complexidade:** Média-Alta
- **Tempo Estimado:** 2-3 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** design-system, library, figma, publish, versioning, release

## Objective
Publicar uma nova versão da library do design system no Figma (e/ou package de código), garantindo
versionamento semântico, release notes claras, migração documentada e comunicação eficiente para
todos os consumidores. O processo minimiza breaking changes e facilita adoção.

## Prerequisites
- Componentes e tokens novos/atualizados aprovados e finalizados
- Specs de componentes documentadas e revisadas
- Checklist de qualidade do DS executado
- Figma library file organizado e pronto para publicação
- Canal de comunicação com consumidores configurado (Slack, email)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design System Lead | Coordenar release, redigir release notes e publicar |
| UI Designer | Validar componentes em contexto antes da publicação |
| Frontend Engineer | Sincronizar release de código com release de design |
| Design Ops | Comunicar release e apoiar adoção |
| Design Lead | Aprovar release e resolver conflitos de prioridade |

## Frameworks
- **Semantic Versioning (SemVer)** — MAJOR.MINOR.PATCH para versionamento
- **Release Notes Template** — estrutura padronizada: new, updated, fixed, deprecated, removed
- **Migration Guide** — instruções para atualizar de versão anterior
- **Pre-Release Checklist** — validações obrigatórias antes de publicar
- **Communication Plan** — canais e timing de notificação

## Checklists
- [ ] Todos os componentes da release testados em contexto
- [ ] Naming conventions verificadas e consistentes
- [ ] Auto-layout e component properties funcionando corretamente
- [ ] Tokens atualizados e conectados via Figma Variables
- [ ] Versão semântica definida (major, minor ou patch)
- [ ] Release notes redigidas com categorias: new, updated, fixed, deprecated
- [ ] Migration guide criado para breaking changes (se major)
- [ ] Branch/file de staging validado antes de merge na library principal
- [ ] Publicação executada no Figma
- [ ] Comunicação de release enviada via canais definidos

## Steps
1. **Revisar changelist** — Listar todas as mudanças desde a última release: componentes novos,
   atualizados, corrigidos, deprecados e removidos. Classificar por tipo.

2. **Definir versão SemVer** — Baseado na changelist: PATCH (fix sem mudança de API), MINOR
   (novo componente ou variante, backward compatible), MAJOR (breaking change).

3. **Executar QA de componentes** — Testar cada componente alterado: auto-layout, variants,
   overrides, detach behavior e aplicação de tokens. Verificar em diferentes contextos.

4. **Validar em contexto** — Aplicar componentes atualizados em 2-3 telas reais de projeto
   para garantir que funcionam em cenários de uso reais sem regressões.

5. **Redigir release notes** — Documentar cada mudança com: descrição, screenshot before/after
   (se visual), e instruções de migração quando aplicável.

6. **Criar migration guide** — Para breaking changes, detalhar: o que muda, por que mudou,
   como atualizar e timeline para deprecation de versão anterior.

7. **Publicar library** — Executar publish no Figma com description clara. Sincronizar com
   Frontend para release de código alinhado (se aplicável).

8. **Comunicar release** — Enviar notificação via Slack e/ou email com: versão, highlights,
   link para release notes e migration guide. Incluir preview visual.

9. **Monitorar adoção** — Acompanhar se consumidores atualizam a library. Oferecer suporte
   para migração e coletar feedback nos primeiros 5 dias úteis.

## Output
- **Published Library** — Nova versão da library disponível no Figma
- **Release Notes** — Documento detalhado de mudanças
- **Migration Guide** — Instruções de atualização (se breaking changes)
- **Formato:** Figma library + Markdown + Slack notification
- **Nomenclatura:** `ds-release-v[X.Y.Z]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design System Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | A cada ciclo de release (quinzenal ou mensal) |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/design-system/` |

## Cross-References
- [Create Component Spec](./create-component-spec.md)
- [Create or Update Tokens](./create-or-update-tokens.md)
- [Adoption and Migration](./adoption-and-migration.md)
- [DS Health Check](./ds-health-check.md)
- [Update Design System Docs](../operations/update-design-system-docs.md)
