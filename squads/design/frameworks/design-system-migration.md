# Design System Migration

## Metadata
- **Autor**: Design Squad
- **Categoria**: Design Systems, Migracao, Breaking Changes
- **Complexidade**: Alta
- **Aplicacao**: Migrar produtos para novo design system ou nova versao com rollout faseado
- **Ultima atualizacao**: 2026-03-06

## Concept

Design System Migration e o framework para migrar produtos de um design system antigo
(ou nenhum sistema) para um novo, gerenciando breaking changes, rollout faseado e
coexistencia temporaria de sistemas. A migracao e um dos momentos mais criticos e
arriscados na vida de um design system.

A premissa e que migracoes big-bang ("vamos trocar tudo de uma vez") quase sempre falham.
O framework propoe migracao incremental com fases definidas, metricas de progresso e
estrategias de coexistencia que permitem que o sistema novo e o antigo convivam
temporariamente sem caos.

O custo de uma migracao mal planejada e enorme: regressoes visuais em producao, queda
de confianca no design system, e equipes que resistem a futuras atualizacoes.

## When to Use

- Quando se lanca uma major version do design system com breaking changes
- Quando se migra de "sem design system" para um design system formal
- Quando se consolida multiplos design systems em um unico
- Quando se muda de tecnologia base (ex: CSS Modules para CSS-in-JS para Tailwind)
- Quando se faz rebranding que afeta a camada visual inteira
- Quando se migra entre ferramentas de design (ex: Sketch para Figma)

## How to Apply

### Fase 0 — Planejamento (2-4 semanas)
1. **Inventario do estado atual**:
   - Quantos produtos/telas usam o sistema antigo?
   - Quais componentes sao mais usados?
   - Quais areas tem mais customizacoes/overrides?
   - Quantos desenvolvedores serao impactados?
2. **Mapeamento de breaking changes**:
   - O que mudou entre v1 e v2?
   - Quais mudancas podem ser automatizadas (codemods)?
   - Quais mudancas requerem decisao humana?
3. **Estrategia de coexistencia**:
   - Como v1 e v2 coexistem no mesmo app? (namespace, CSS isolation)
   - Qual o periodo maximo de coexistencia? (ideal: 1-3 meses)
4. **Definicao de sucesso**:
   - Meta de migracao: X% dos componentes migrados em Y semanas
   - Zero regressoes visuais criticas
   - Zero downtime

### Fase 1 — Foundation (1-2 sprints)
1. Migre tokens primeiro (cores, tipografia, espacamento)
   - Tokens sao a base — migra-los primeiro garante consistencia visual
   - Use CSS custom properties com fallbacks para coexistencia
2. Migre utilities (grid, helpers, reset)
3. Valide que a fundacao funciona em todas as plataformas/browsers target
4. Crie adapter layer se necessario (v1 API -> v2 API)
5. Documente cada token migrado com mapeamento old -> new

### Fase 2 — Core Components (2-4 sprints)
1. Priorize por frequencia de uso:
   - Top 10 componentes mais usados primeiro
   - Tipicamente: Button, Input, Select, Card, Modal, Table
2. Para cada componente:
   - Crie codemod se possivel (automacao de rename/refactor)
   - Documente migration guide com before/after
   - Migre em um produto piloto primeiro
   - Valide com visual regression tests
   - Expanda para demais produtos
3. Mantenha v1 funcionando — nao force migracao imediata
4. Comunique progresso semanalmente

### Fase 3 — Extended Components (2-4 sprints)
1. Migre componentes restantes em ordem de prioridade
2. Enderece customizacoes e overrides:
   - Customizacao legítima -> criar variante no v2
   - Customizacao acidental -> migrar para componente padrao
   - Customizacao obsoleta -> remover
3. Migre patterns e composicoes
4. Atualize documentacao e exemplos

### Fase 4 — Cleanup (1-2 sprints)
1. Remova dependencias do v1 que nao sao mais usadas
2. Remova adapter layers e compatibility shims
3. Remova CSS e codigo morto do sistema antigo
4. Valide que nenhuma referencia ao v1 permanece
5. Atualize CI/CD para usar apenas v2
6. Documente a migracao completa como case study

### Gestao de Breaking Changes
1. **Categorize breaking changes**:
   - Rename: propriedade mudou de nome (automavel com codemod)
   - Behavior: funcionalidade mudou (requer review humano)
   - Removal: feature removida (requer alternativa)
   - Visual: aparencia mudou significativamente (requer design review)
2. **Para cada breaking change, forneca**:
   - Descricao clara do que mudou
   - Racional (por que mudou)
   - Antes/depois com codigo
   - Codemod se aplicavel
   - Guia manual se nao automavel

### Rollout Strategy
1. **Canary**: Deploy v2 em 1 produto interno nao-critico
2. **Early Adopters**: 2-3 equipes voluntarias migram
3. **General Availability**: v2 disponivel para todas as equipes
4. **Enforcement**: Deadline para migracao, v1 em deprecation notice
5. **Sunset**: v1 removido, apenas v2 suportado

## Key Principles

- **Incremental, nao big-bang**: Migracoes faseadas sao mais seguras e gerenciaveis
- **Coexistencia temporaria**: v1 e v2 devem poder conviver sem conflito
- **Automate o que for possivel**: Codemods economizam centenas de horas
- **Comunique, comunique, comunique**: Equipes precisam saber o que esta mudando e quando
- **Fundacao primeiro**: Tokens antes de componentes
- **Piloto antes de escala**: Valide em 1 produto antes de expandir
- **Zero regressao como meta**: Visual regression tests sao obrigatorios

## Examples

### Exemplo 1 — Migracao de DS v1 para v2
- v1: 45 componentes, CSS Modules, sem tokens formais
- v2: 52 componentes, CSS Custom Properties, token architecture
- Codemods criados: 23 (cobrindo 70% das mudancas)
- Timeline: 12 semanas (planejamento: 2, foundation: 2, core: 4, extended: 3, cleanup: 1)
- Produtos migrados: 4 (gradualmente, 1 por semana apos validacao)
- Regressoes em producao: 2 minor (corrigidas em < 24h)

### Exemplo 2 — Rebranding via Token Migration
Uma empresa mudou branding (cores, tipografia, border-radius).
Porque tinham token architecture solida, a migracao foi:
1. Atualizaram 34 alias tokens (cores e tipografia)
2. Zero mudancas em componentes
3. Deploy em 1 dia para todos os produtos
4. Rollback plan: reverter tokens (testado previamente)
Total effort: 3 dias de trabalho incluindo testes.

### Exemplo 3 — Migration Tracker Dashboard
| Produto    | Total Components | Migrated | % Complete | ETA     |
|------------|-----------------|----------|------------|---------|
| App Web    | 234             | 198      | 85%        | Semana 8|
| App Mobile | 156             | 156      | 100%       | Done    |
| Admin      | 89              | 45       | 51%        | Semana 10|
| Marketing  | 67              | 12       | 18%        | Semana 12|

Dashboard atualizado diariamente, visivel para toda a organizacao.

## Common Pitfalls

- **Big-bang migration**: Trocar tudo de uma vez garante regressoes. Migre incrementalmente
- **Sem codemods**: Migracao manual de centenas de componentes e lenta e error-prone
- **Coexistencia infinita**: Definir deadline para sunset do v1 — sem deadline, v1 nunca morre
- **Sem visual regression tests**: Regressoes so sao detectadas em producao
- **Comunicacao insuficiente**: Equipes surpresas por mudancas perdem confianca
- **Ignorar customizacoes**: Customizacoes nao mapeadas quebram silenciosamente
- **Subestimar esforco**: Migracoes sempre levam mais tempo que o planejado. Adicione 30% buffer

## Cross-References

- [frost-maintaining-design-systems.md](frost-maintaining-design-systems.md) — Versionamento e breaking changes
- [design-token-architecture.md](design-token-architecture.md) — Tokens como base de migracao
- [design-system-layer.md](design-system-layer.md) — Estrutura do DS
- [governance-layer.md](governance-layer.md) — Politica de deprecation e versioning
- [design-debt-management.md](design-debt-management.md) — Migracao como payoff de divida
- [mall-design-system-strategy.md](mall-design-system-strategy.md) — Estrategia de longo prazo
