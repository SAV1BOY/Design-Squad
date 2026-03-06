# Frost Maintaining Design Systems

## Metadata
- **Autor**: Brad Frost
- **Categoria**: Governanca, Design Systems
- **Complexidade**: Alta
- **Aplicacao**: Design systems em producao que precisam de evolucao sustentavel
- **Ultima atualizacao**: 2026-03-06

## Concept

Manter um design system e significativamente mais dificil do que construi-lo. Brad Frost
enfatiza que um design system nao e um projeto com inicio, meio e fim — e um produto vivo
que precisa de governanca, evolucao continua e gestao cuidadosa de breaking changes.

A manutencao envolve tres dimensoes criticas: governanca (quem decide o que), evolucao
(como o sistema cresce e muda) e comunicacao (como mudancas sao informadas e adotadas).
Sem uma estrategia explicita para cada dimensao, design systems tendem a estagnar
(ninguem atualiza), fragmentar (cada equipe cria variantes proprias) ou colapsar
(breaking changes destroem a confianca).

O framework propoe processos, papeis e rituais para manter o sistema saudavel ao longo
do tempo, equilibrando estabilidade com a necessidade de evolucao.

## When to Use

- Quando o design system ja esta em producao e sendo consumido por multiplas equipes
- Quando ha conflitos sobre quem pode modificar componentes do sistema
- Quando breaking changes estao causando problemas em equipes consumidoras
- Quando o design system esta estagnando porque ninguem se sente responsavel
- Quando novas necessidades surgem e nao ha processo claro para incorpora-las
- Quando a adocao do sistema esta caindo por falta de confianca ou relevancia

## How to Apply

### Pilar 1 — Modelo de Governanca
1. Defina quem pode propor mudancas (qualquer pessoa na organizacao)
2. Defina quem avalia propostas (comite de design system ou core team)
3. Defina quem aprova e implementa (maintainers do sistema)
4. Estabeleca criterios claros de aceitacao para novos componentes:
   - Usado por pelo menos 2 produtos/equipes diferentes
   - Documentacao completa (props, estados, guidelines, a11y)
   - Testes automatizados (unit, visual regression, a11y)
   - Review por pelo menos 1 designer e 1 dev do core team
5. Crie um RFC process para mudancas significativas

### Pilar 2 — Versionamento e Breaking Changes
1. Adote semantic versioning (semver) rigorosamente:
   - MAJOR: breaking changes (remocao de props, mudanca de comportamento)
   - MINOR: novos componentes ou features retrocompativeis
   - PATCH: bug fixes e ajustes visuais menores
2. Mantenha changelog detalhado e legivel por humanos
3. Forneca migration guides para cada major version
4. Suporte pelo menos a versao anterior (N-1) por periodo definido
5. Comunique deprecations com antecedencia minima de 2 sprints
6. Use codemods quando possivel para automatizar migracoes

### Pilar 3 — Cadencia e Rituais
1. **Semanal**: Triage de issues e PRs do design system
2. **Quinzenal**: Office hours para equipes consumidoras tirarem duvidas
3. **Mensal**: Review de metricas de adocao e satisfacao
4. **Trimestral**: Roadmap review e priorizacao estrategica
5. **Semestral**: Interface inventory para detectar drift
6. Mantenha um backlog publico e priorizado

### Pilar 4 — Comunicacao
1. Crie um canal dedicado (Slack/Teams) para o design system
2. Publique release notes a cada versao, destacando breaking changes
3. Faca demos de novas features em forums da organizacao
4. Mantenha uma pagina de status mostrando o que esta stable, beta e deprecated
5. Documente decisoes arquiteturais em ADRs (Architecture Decision Records)

### Pilar 5 — Metricas de Saude
1. **Adocao**: % de produtos usando o design system
2. **Cobertura**: % de componentes na UI que vem do sistema
3. **Satisfacao**: NPS ou survey periodico com equipes consumidoras
4. **Velocity**: Tempo medio para nova feature ser adicionada ao sistema
5. **Bugs**: Volume de bugs reportados por versao
6. **Drift**: Numero de overrides ou variantes nao-oficiais detectadas

## Key Principles

- **Sistema como produto**: Trate o design system com o mesmo rigor de qualquer produto
- **Estabilidade e contrato**: Consumidores precisam confiar que updates nao vao quebrar nada
- **Evolucao gradual**: Prefira mudancas incrementais a reescritas completas
- **Transparencia total**: Decisoes, roadmap e problemas devem ser visiveis para todos
- **Feedback continuo**: Equipes consumidoras sao stakeholders que precisam ser ouvidos
- **Automacao de conformidade**: Use tooling para detectar drift e inconsistencias
- **Deprecation consciente**: Nao remova nada sem aviso previo e alternativa clara

## Examples

### Exemplo 1 — Processo de RFC
Uma equipe estabeleceu um RFC process para mudancas no design system:
1. Autor cria documento descrevendo problema, proposta e impacto
2. Periodo de comentarios de 5 dias uteis
3. Core team avalia feedback e decide: aceitar, modificar ou recusar
4. Se aceito, entra no backlog com prioridade definida
5. Implementacao segue o processo normal de PR + review

Em 6 meses, 34 RFCs foram submetidos, 28 aceitos, 4 modificados, 2 recusados.
O processo reduziu conflitos sobre mudancas em 70%.

### Exemplo 2 — Gestao de Breaking Change
Ao mudar a API de um componente Button (removendo prop `variant` em favor de `appearance`):
1. Versao 3.x: `appearance` adicionado, `variant` marcado como deprecated com warning
2. Versao 3.x: Codemod publicado para migrar automaticamente
3. 4 sprints de aviso antes do major bump
4. Versao 4.0: `variant` removido, migration guide publicado
5. Versao 3.x mantida com security fixes por mais 3 meses

### Exemplo 3 — Dashboard de Saude
Uma equipe criou um dashboard automatizado mostrando:
- 87% de adocao (13% dos produtos ainda nao migraram)
- 234 componentes no sistema, 12 deprecated, 8 em beta
- NPS de 72 com consumidores (survey trimestral)
- Tempo medio de 11 dias para nova feature ir de RFC a release
O dashboard era revisado mensalmente pelo core team e lideranca.

## Common Pitfalls

- **"Launch and forget"**: Construir o sistema e nao investir em manutencao e a forma
  mais comum de fracasso. Reserve pelo menos 30% da capacidade para manutencao
- **Governanca muito rigida**: Processos excessivos desincentivam contribuicoes.
  Equilibre rigor com agilidade
- **Governanca muito frouxa**: Sem criterios claros, o sistema vira um dump de componentes
  sem qualidade consistente
- **Breaking changes sem comunicacao**: Nada destroi confianca mais rapido do que um update
  que quebra algo em producao sem aviso
- **Ignorar metricas**: Sem dados, decisoes de priorizacao sao baseadas em opinioes e
  quem grita mais alto
- **Core team isolado**: Se o time do design system nao conversa regularmente com consumidores,
  o sistema perde relevancia
- **Nao investir em DX**: Developer experience do sistema (docs, API, tooling) e tao
  importante quanto a qualidade visual

## Cross-References

- [frost-pitfalls-of-design-systems.md](frost-pitfalls-of-design-systems.md) — O que da errado e como evitar
- [mall-design-system-team-models.md](mall-design-system-team-models.md) — Modelos de equipe para manutencao
- [mall-design-system-strategy.md](mall-design-system-strategy.md) — Estrategia de longo prazo
- [governance-layer.md](governance-layer.md) — Camada de governanca no stack
- [design-debt-management.md](design-debt-management.md) — Gestao da divida de design
- [design-ops-cadence.md](design-ops-cadence.md) — Cadencias operacionais
