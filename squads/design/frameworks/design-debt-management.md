# Design Debt Management

## Metadata
- **Autor**: Design Squad
- **Categoria**: Qualidade, Gestao, Divida de Design
- **Complexidade**: Media
- **Aplicacao**: Inventariar, priorizar e reduzir divida de design sistematicamente
- **Ultima atualizacao**: 2026-03-06

## Concept

Design Debt Management e o framework para identificar, classificar, priorizar e reduzir
a divida de design acumulada em um produto. Divida de design sao decisoes de design
sub-otimas feitas intencionalmente (por restricoes de tempo/escopo) ou acidentalmente
(por falta de padrao ou atencao) que se acumulam e degradam a experiencia ao longo do tempo.

Assim como divida tecnica, divida de design gera juros: cada nova feature construida sobre
uma base inconsistente herda e amplifica as inconsistencias. Quanto mais tempo a divida
persiste, mais caro e resolve-la.

O framework propoe tres fases: inventario (identificar e documentar), priorizacao (decidir
o que resolver primeiro) e payoff (executar a reducao de forma sustentavel).

## When to Use

- Quando o produto acumulou inconsistencias visuais e de UX ao longo do tempo
- Quando a equipe sente que "tudo precisa ser refeito" mas nao sabe por onde comecar
- Quando novas features sao construidas sobre base inconsistente
- Quando se planeja investimento em qualidade de design
- Quando se quer quantificar o impacto da divida para stakeholders
- Quando a divida de design esta afetando metricas de experiencia

## How to Apply

### Fase 1 — Inventario
1. **Colete divida de multiplas fontes**:
   - Interface inventory visual (screenshots de inconsistencias)
   - Feedback de testes de usabilidade
   - Tickets de suporte relacionados a UX
   - Feedback interno de designers e devs
   - Audit de acessibilidade
   - Comparacao com design system (componentes fora do padrao)

2. **Classifique por tipo**:
   - **Cosmetica**: Inconsistencias visuais que nao afetam funcionalidade
     (cores levemente diferentes, espacamentos inconsistentes)
   - **Funcional**: Comportamentos inconsistentes que confundem usuarios
     (modals que fecham diferente, validacoes inconsistentes)
   - **Estrutural**: Problemas de IA, navegacao ou fluxo
     (categorias confusas, fluxos com dead-ends)
   - **Acessibilidade**: Barreiras para usuarios com deficiencia
     (contraste insuficiente, falta de keyboard nav)
   - **De padrao**: Desvios do design system documentado
     (componentes custom que deveriam usar DS)

3. **Documente cada item**:
   - Descricao do problema
   - Localizacao (telas/fluxos afetados)
   - Tipo e severidade
   - Screenshots/evidencia
   - Impacto estimado no usuario/negocio

### Fase 2 — Priorizacao
1. **Avalie cada item em duas dimensoes**:
   - **Impacto**: Quantos usuarios afeta x qual a severidade do impacto
     - Alto: Afeta muitos usuarios com impacto severo
     - Medio: Afeta muitos com impacto leve OU poucos com impacto severo
     - Baixo: Afeta poucos com impacto leve
   - **Esforco**: Quanto trabalho para resolver
     - Baixo: < 2 horas (quick fix)
     - Medio: 2 horas - 2 dias
     - Alto: > 2 dias

2. **Priorize usando matriz 2x2**:
   - **Do first**: Alto impacto + Baixo esforco (quick wins)
   - **Plan**: Alto impacto + Alto esforco (projetos)
   - **Fill gaps**: Baixo impacto + Baixo esforco (quando sobrar tempo)
   - **Defer**: Baixo impacto + Alto esforco (reconsiderar depois)

3. **Crie roadmap de reducao**:
   - Quick wins: resolver nas proximas 2 semanas
   - Projetos: planejar para os proximos 1-3 sprints
   - Deferred: revisar no proximo quarter

### Fase 3 — Payoff (Execucao)
1. **Aloque capacidade fixa**: Reserve 15-20% do tempo de design para divida
2. **Quick wins semanais**: 1-2 quick fixes por semana por designer
3. **Projetos de consolidacao**: Sprints focados em areas especificas
   - Sprint de consolidacao de modals
   - Sprint de a11y compliance
   - Sprint de token migration
4. **Prevencao de nova divida**:
   - Quality gates no processo (design review, QA visual)
   - Componentes do DS como padrao (nao custom)
   - A11y check automatizado no CI
5. **Monitoramento continuo**: Dashboard de divida atualizado mensalmente

## Key Principles

- **Divida visivel**: O que nao esta documentado nao existe para priorizacao
- **Quick wins primeiro**: Resolver items de alto impacto e baixo esforco gera momentum
- **Capacidade dedicada**: Sem tempo explicitamente alocado, divida nunca e reduzida
- **Prevencao > correcao**: Evitar criar divida e mais barato que paga-la
- **Quantificacao**: Conecte divida a metricas de negocio para justificar investimento
- **Incrementalismo**: Pagar toda a divida de uma vez e irreal. Reduza consistentemente
- **Celebre progresso**: Comunique reducao de divida como win para a equipe e organizacao

## Examples

### Exemplo 1 — Inventario de Divida
Uma equipe identificou 67 itens de divida de design:
- Cosmetica: 28 itens (42%)
- Funcional: 15 itens (22%)
- Acessibilidade: 12 itens (18%)
- De padrao: 8 itens (12%)
- Estrutural: 4 itens (6%)

Priorizacao resultou em: 14 quick wins, 8 projetos, 45 deferred.
Quick wins resolvidos em 3 semanas. Projetos planejados em 3 sprints.

### Exemplo 2 — Quantificacao para Stakeholders
"Nossa divida de acessibilidade (12 itens) nos expoe a risco legal sob LGPD/ADA.
Corrigir os 5 itens criticos requer ~40h de trabalho (1 sprint de 1 designer + 1 dev).
O custo de nao corrigir: potencial multa de R$50M + dano reputacional."

"Nossa divida funcional (15 inconsistencias em forms) gera ~200 tickets de suporte/mes.
A R$15/ticket (tempo de atendimento), sao R$3000/mes. Resolver leva 2 sprints.
ROI positivo em 3 meses."

### Exemplo 3 — Dashboard de Divida ao Longo do Tempo
| Mes   | Total | Criada | Paga | Saldo | Tendencia |
|-------|-------|--------|------|-------|-----------|
| Jan   | 67    | -      | -    | 67    | Baseline  |
| Fev   | 67    | 5      | 18   | 54    | Diminuindo|
| Mar   | 54    | 3      | 12   | 45    | Diminuindo|
| Abr   | 45    | 8      | 10   | 43    | Estavel   |
| Mai   | 43    | 2      | 9    | 36    | Diminuindo|

Tendencia saudavel: mais divida paga do que criada por mes.

## Common Pitfalls

- **Inventario sem acao**: Listar 200 itens de divida e nao resolver nenhum
- **Perfeccionismo**: Querer resolver tudo antes de lancar qualquer coisa nova
- **Divida invisivel**: Se nao esta documentada e priorizada, sera ignorada
- **Zero alocacao**: "Vamos pagar quando der tempo" significa nunca
- **Focar em cosmetica**: Resolver 30 inconsistencias de cor enquanto 5 problemas
  de a11y criticos persistem e ma priorizacao
- **Nao prevenir**: Pagar divida sem mudar o processo que a criou e enxugar gelo
- **Nao medir progresso**: Sem tracking, nao ha como saber se esta melhorando

## Cross-References

- [frost-interface-inventory.md](frost-interface-inventory.md) — Inventario como ferramenta de identificacao
- [design-ops-cadence.md](design-ops-cadence.md) — Cadencia para reducao de divida
- [governance-layer.md](governance-layer.md) — Quality gates para prevencao
- [accessibility-by-default.md](accessibility-by-default.md) — Divida de a11y
- [mall-selling-design-to-stakeholders.md](mall-selling-design-to-stakeholders.md) — Justificar investimento
- [measurement-layer.md](measurement-layer.md) — Metricas de divida
