# Library Publish Framework

## Metadata

- **Autor**: Design Squad
- **Categoria**: Design System, Operations, Release Management
- **Complexidade**: Alta
- **Aplicacao**: Gerenciar publicacao, versionamento e comunicacao de design system libraries
- **Ultima atualizacao**: 2026-03-18
- **Tags**: semver, changelog, migration, deprecation, release, rollback, design-system, library

## Concept

O Library Publish Framework define o processo completo de publicacao de design system libraries —
desde o versionamento semantico ate a comunicacao de releases e procedimentos de rollback. Um DS
library mal publicado pode quebrar dezenas de produtos simultaneamente; por isso, disciplina de
release e tao critica quanto qualidade de componentes.

O framework adota Semantic Versioning (semver) como padrao, Keep a Changelog como formato de
documentacao, uma deprecation policy de 2 versoes de graca, e um processo de rollback testavel.
Cada release e um contrato com os consumidores: previsivel, documentado e reversivel.

## When to Use

- Ao publicar qualquer atualizacao do design system (Figma libraries, code packages, tokens)
- Quando um componente precisa ser depreciado ou removido
- Para comunicar breaking changes a squads consumidores
- Ao planejar migracao de versao major do DS
- Quando um bug em release exige rollback imediato
- Para estabelecer o processo de release em um DS novo

## How to Apply

### Step 1 — Classificar a Mudanca com Semver
1. **Patch (0.0.x)**: Bug fix visual, correcao de token, ajuste de spacing que nao altera API
2. **Minor (0.x.0)**: Novo componente, nova prop/variante, feature adicionada sem quebra
3. **Major (x.0.0)**: Breaking change — API alterada, componente removido, token renomeado
4. Regra de ouro: se o consumidor precisa mudar algo no codigo/design dele, e major
5. Pre-releases usam sufixo: `2.1.0-beta.1`, `3.0.0-rc.1`
6. Documente a classificacao no PR antes de merge

### Step 2 — Escrever Changelog (Keep a Changelog)
1. Use o formato padrao com categorias: Added, Changed, Deprecated, Removed, Fixed, Security
2. Cada entrada deve ser compreensivel sem contexto tecnico profundo
3. Inclua link para o PR ou issue relacionado
4. Para breaking changes, adicione prefixo **BREAKING:** com descricao clara do impacto
5. Exemplo de entrada:
   - `### Changed`
   - `- **BREAKING:** Button component agora requer prop "variant" (antes defaultava para "primary") [#342]`
6. Mantenha secao [Unreleased] atualizada durante o desenvolvimento

### Step 3 — Criar Migration Guide (para Major Releases)
1. Liste cada breaking change com: o que mudou, por que mudou, como migrar
2. Forneca code snippets de antes/depois para cada mudanca
3. Inclua script de codemods quando possivel (automatiza migracoes mecanicas)
4. Estime tempo de migracao por squad (T-shirt sizing)
5. Oferca office hours ou pairing sessions para squads com dificuldade
6. Publique migration guide pelo menos 2 sprints antes da data de corte

### Step 4 — Aplicar Deprecation Policy
1. Componente a ser removido recebe tag `@deprecated` com mensagem e alternativa
2. Deprecation e anunciada em release minor (nao major) — dando tempo para migrar
3. Componente depreciado permanece funcional por pelo menos 2 versoes minor
4. Na versao minor seguinte ao deprecation, adicione warning visual (badge, console warning)
5. Remocao efetiva so acontece em release major, apos o periodo de graca
6. Timeline minima: deprecation announce > 2 minor releases > removal in next major

### Step 5 — Executar Release
1. Crie branch de release: `release/v2.1.0`
2. Rode test suite completo: visual regression, unit tests, accessibility checks
3. Publique em ambiente de staging e peca validacao de 1-2 squads consumidores
4. Atualize changelog com data de release e versao final
5. Publique a library (Figma: publish library; Code: npm publish / GitHub release)
6. Tag git com versao: `git tag v2.1.0`
7. Envie comunicacao de release (ver Step 6)

### Step 6 — Comunicar Release
1. Post no canal #design-system do Slack com resumo: versao, highlights, breaking changes
2. Para major releases: apresentacao de 15 min no design sync ou engineering all-hands
3. Atualize documentacao do DS (Storybook, site, Notion) antes de anunciar
4. Envie email/mensagem direta para tech leads de squads afetados por breaking changes
5. Mantenha release notes acessiveis no repositorio (CHANGELOG.md) e no site do DS
6. Para Figma: inclua banner no arquivo main com link para release notes

### Step 7 — Procedimento de Rollback
1. Se bug critico e detectado pos-release, avalie severidade: afeta producao?
2. Para rollback de codigo: `npm unpublish` (se <72h) ou publique patch revertendo
3. Para rollback de Figma: restaure versao anterior via version history
4. Comunique rollback no mesmo canal da release original com tag @here
5. Documente post-mortem: o que falhou, por que nao foi pego em staging, como prevenir
6. Implemente fix e republique como patch version

## Examples

### Exemplo 1 — Minor Release com Novo Componente
Novo componente `Tooltip` adicionado ao DS. Version bump: 2.3.0 > 2.4.0. Changelog entry
em "Added". Nenhuma migracao necessaria. Comunicacao: post no Slack com preview visual e
link para Storybook. 3 squads adotaram na mesma sprint.

### Exemplo 2 — Major Release com Breaking Changes
Redesign do sistema de cores: tokens renomeados de `color-primary-500` para `color-brand-primary`.
Deprecation anunciado em v2.6.0 com mapeamento de nomes. Migration guide publicado com codemod
automatico. Office hours oferecidas. Release v3.0.0 apos 2 meses de deprecation period.
8 squads migraram em 3 sprints. 1 squad atrasado recebeu pairing dedicado.

## Common Pitfalls

- **Sem semver**: Bumps aleatorios destroem a confianca dos consumidores no DS
- **Changelog vago**: "Melhorias gerais" nao ajuda ninguem — seja especifico
- **Breaking change sem aviso**: Surpreender squads com quebra e a forma mais rapida de perder adocao
- **Deprecation sem alternativa**: Nao deprecie sem oferecer caminho de migracao claro
- **Rollback nao testado**: Se voce nunca testou rollback, ele nao vai funcionar quando precisar
- **Comunicacao so no Slack**: Mensagens somem — mantenha release notes permanentes e acessiveis

## Cross-References

- [Design System Architect](../agents/design-system-architect.md) — Agente responsavel por arquitetura e governanca do DS
- [Brad Frost](../agents/brad-frost.md) — Agente especialista em design systems e atomic design
- [Design System Quality Checklist](../checklists/design-system-quality.md) — Checklist de qualidade do DS
- [Release Notes Template](../templates/handoff/release-notes-template.md) — Template para release notes
- [design-system-governance.md](design-system-governance.md) — Governanca de decisoes do DS
- [design-token-architecture.md](design-token-architecture.md) — Arquitetura de tokens impactada por releases
- [design-system-migration.md](design-system-migration.md) — Framework complementar para migracoes complexas
- [atomic-design.md](atomic-design.md) — Metodologia base para estrutura de components
