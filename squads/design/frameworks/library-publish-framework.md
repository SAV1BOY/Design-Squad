# Library Publish Framework

## Metadata

- **Autor**: Design Squad
- **Categoria**: Design System, Operations, Publicacao
- **Complexidade**: Alta
- **Aplicacao**: Gerenciar publicacao de design system libraries com semver, changelog, migration e rollback
- **Ultima atualizacao**: 2026-03-18
- **Tags**: design-system, library, semver, changelog, migration, deprecation, rollback, communication

## Concept

O Library Publish Framework estrutura o ciclo completo de publicacao de libraries do design
system — desde versionamento semantico ate comunicacao e rollback. Publicar uma library sem
processo e como fazer deploy sem CI/CD: funciona ate dar errado, e quando da errado, o impacto
e multiplicado por todos os consumidores.

Uma library mal versionada quebra produtos downstream silenciosamente. Um changelog ausente
forca cada consumidor a descobrir sozinho o que mudou. Deprecation sem migration path cria
debt acelerado. Este framework aplica principios de software release management ao contexto
de design systems, garantindo que cada publicacao seja previsivel, documentada e reversivel.

## When to Use

- Ao publicar qualquer versao de Figma library, code library ou token package
- Quando componentes precisam ser atualizados com breaking changes
- Para deprecar componentes ou tokens que serao descontinuados
- Ao criar processo de release para design system novo
- Para padronizar comunicacao de mudancas entre squads consumidores
- Quando incidentes de publicacao mostram que o processo atual nao e robusto

## How to Apply

### Step 1 — Semantic Versioning (Semver)
Adote semver (MAJOR.MINOR.PATCH) para todas as libraries:

1. **PATCH (1.0.x)**: Bug fixes, ajustes visuais menores, correcoes de token — nao quebra nada
2. **MINOR (1.x.0)**: Novos componentes, novas variantes, novas features — backward compatible
3. **MAJOR (x.0.0)**: Breaking changes — API muda, componentes removidos, tokens renomeados
4. Mantenha branch/arquivo de versao atualizado em todas as libraries
5. Para Figma: use naming convention "[Library Name] v1.2.3" no nome do arquivo
6. Para code: package.json/pubspec/podspec com versao semantica

### Step 2 — Changelog
Para cada publicacao, documente:

1. **Versao e data**: v1.3.0 — 2026-03-18
2. **Added**: Novos componentes, variantes, tokens
3. **Changed**: Alteracoes em componentes existentes (visual, API, behavior)
4. **Deprecated**: O que sera removido em versao futura (com timeline)
5. **Removed**: O que foi removido nesta versao (somente em MAJOR)
6. **Fixed**: Bug fixes e correcoes
7. Inclua screenshots/videos para mudancas visuais
8. Inclua code snippets para mudancas de API

### Step 3 — Migration Guide (para Breaking Changes)
Para cada MAJOR version ou deprecation significativo:

1. Liste cada breaking change com: o que era > o que virou
2. Forneca mapeamento 1:1 quando possivel (ComponenteAntigo > ComponenteNovo)
3. Escreva passo-a-passo de migracao para cada mudanca
4. Estime esforco de migracao por squad consumidor (T-shirt sizing)
5. Ofereca periodo de coexistencia: versao antiga disponivel por N sprints
6. Crie codemods ou scripts de migracao automatica quando viavel
7. Defina deadline de migracao e comunique com antecedencia minima de 2 sprints

### Step 4 — Deprecation Process
1. **Anuncio**: Marque componente como deprecated no changelog (MINOR version)
2. **Alternativa**: Documente o substituto recomendado com exemplos
3. **Timeline**: Defina quando sera removido (minimo 2 MINOR versions depois)
4. **Visual**: Adicione badge "deprecated" no componente (Figma e docs)
5. **Tracking**: Monitore adocao do substituto e uso residual do deprecated
6. **Remocao**: Remova na MAJOR version seguinte, somente apos migracao de consumidores criticos

### Step 5 — Comunicacao
Para cada publicacao, comunique nos canais apropriados:

1. **PATCH**: Mensagem no canal do DS (Slack/Teams) com changelog resumido
2. **MINOR**: Changelog detalhado + demo das novidades em DS review meeting
3. **MAJOR**: Announcement formal + migration guide + sessao de Q&A com squads
4. Mantenha pagina de releases acessivel (docs site, Notion, wiki)
5. Notifique squads afetados diretamente quando houver breaking changes
6. Use template padrao para consistencia na comunicacao

### Step 6 — Rollback Plan
Para cada publicacao, tenha plano de rollback:

1. Antes de publicar: garanta que versao anterior esta acessivel e funcional
2. Defina criterios de rollback: "Se [condicao], reverteremos para v1.2.x"
3. Em Figma: mantenha backup do arquivo pre-publicacao (branch ou versao nomeada)
4. Em code: garanta que versao anterior esta no registry e instalavel
5. Comunique rollback imediatamente se necessario, com motivo e ETA de fix
6. Post-mortem: documente o que causou o rollback e como prevenir

### Step 7 — Checklist Pre-Publicacao
Antes de cada release, verifique:

- [ ] Versao atualizada seguindo semver
- [ ] Changelog completo e revisado
- [ ] Migration guide pronta (se breaking change)
- [ ] Testes de componentes passando (visual regression, unit, a11y)
- [ ] Review por pelo menos 1 membro do DS team
- [ ] Comunicacao rascunhada e agendada
- [ ] Rollback plan definido
- [ ] Backup da versao anterior acessivel

## Examples

### Exemplo 1 — MINOR Release: Novo Componente de Stepper
v2.4.0: Added Stepper component com 3 variantes (horizontal, vertical, compact). Changelog
com screenshots, props documentation e usage guidelines. Comunicacao: post no canal #design-system
com demo GIF + link para docs. Nenhuma migracao necessaria — puramente aditivo.

### Exemplo 2 — MAJOR Release: Redesign de Button
v3.0.0: Button refatorado com nova API (variant prop substituiu type + style). Migration guide
mapeando todas as combinacoes antigas para novas. Codemod criado para migracao automatica em
React. Periodo de coexistencia: v2.x mantida por 3 sprints. 8 squads migrados em 4 semanas
com suporte do DS team.

## Common Pitfalls

- **Publicar sem changelog**: Consumidores descobrem mudancas por trial and error — destroi confianca
- **Breaking change em MINOR**: Maior fonte de incidentes de DS — semver existe por uma razao
- **Deprecar sem alternativa**: Dizer "nao use mais" sem dizer "use isso" cria paralisia
- **Timeline de migracao irreal**: Squads tem prioridades proprias — negocie, nao imponha
- **Rollback impossivel**: Sem backup acessivel, o unico caminho e "fix forward" sob pressao
- **Comunicacao so no canal**: Mudancas criticas precisam de comunicacao ativa, nao passiva

## Cross-References

- [design-system-governance.md](design-system-governance.md) — Governanca de decisoes de publicacao
- [design-system-migration.md](design-system-migration.md) — Estrategias de migracao entre versoes
- [design-token-architecture.md](design-token-architecture.md) — Tokens como parte da library
- [design-debt-management.md](design-debt-management.md) — Deprecation mal gerenciado gera debt
- [design-ops-cadence.md](design-ops-cadence.md) — Cadencia de releases no calendario de ops
- [Changelog Template](../templates/design-system/changelog-template.md) — Template de changelog
- [DS Contribution Guide](../templates/design-system/ds-contribution-guide-template.md) — Guia de contribuicao
- [Component RFC Template](../templates/design-system/component-rfc-template.md) — RFC antes de mudancas grandes
- [Design System Architect](../agents/design-system-architect.md) — Agente responsavel por publicacao
