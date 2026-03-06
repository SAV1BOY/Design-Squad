# Design Debt Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Design Operations
- **Version:** 1.0.0
- **Owner Agent:** Design Debt Agent

## Objective
Garantir que o design debt seja identificado, catalogado, priorizado e tratado de forma sistematica para manter a qualidade do produto ao longo do tempo.
Gerenciar design debt proativamente evita degradacao cumulativa da experiencia do usuario.

## When to Apply
- Ao identificar inconsistencias, workarounds ou desvios do design ideal no produto.
- Em auditorias periodicas de qualidade e consistencia.
- Ao planejar sprints para incluir reducao de design debt.

## Criteria
- [ ] Existe um inventario centralizado de design debt com todos os itens catalogados
- [ ] Cada item de debt possui descricao clara do problema e do impacto no usuario
- [ ] Os itens estao classificados por tipo (visual, interacao, acessibilidade, conteudo, pattern)
- [ ] A severidade de cada item esta avaliada (critico, major, minor)
- [ ] O esforco estimado para resolver cada item esta documentado (T-shirt sizing ou pontos)
- [ ] Os itens estao priorizados usando criterios de impacto vs esforco
- [ ] Cada item possui referencia visual (screenshot, link) do estado atual
- [ ] A solucao desejada ou target state esta indicada para cada item
- [ ] Os itens de debt estao associados as areas ou features do produto afetadas
- [ ] Existe um processo definido para adicionar novos itens de debt ao inventario
- [ ] O design debt e revisado periodicamente (mensal ou por sprint) para repriorizacao
- [ ] Existe um budget ou alocacao de tempo dedicada para reducao de design debt
- [ ] Os itens resolvidos sao marcados e removidos do inventario ativo
- [ ] As metricas de design debt sao acompanhadas ao longo do tempo (trend)
- [ ] Os stakeholders estao cientes do nivel de design debt e seu impacto
- [ ] O design debt e considerado no planejamento de novas features (nao apenas como backlog)

## Severity Guide

### Critico
- Ausencia de qualquer inventario ou tracking de design debt.
- Design debt critico acumulado sem visibilidade para stakeholders.
- Nenhum budget ou tempo alocado para reducao de debt.

### Major
- Itens de debt sem priorizacao ou classificacao de severidade.
- Inventario desatualizado com itens ja resolvidos ou obsoletos.
- Falta de estimativa de esforco impedindo planejamento.

### Minor
- Metricas de trend nao acompanhadas formalmente.
- Screenshots desatualizadas no inventario de itens antigos.
- Processo de adicao de novos itens nao formalizado.

## Cross-References
- [Design Documentation Quality](design-documentation-quality.md)
- [Design System Quality](design-system-quality.md)
- [UX Audit Quality](ux-audit-quality.md)
- [Performance UX Quality](performance-ux-quality.md)
- [Accessibility Quality](accessibility-quality.md)
