# Mall Design System Strategy

## Metadata
- **Autor**: Dan Mall
- **Categoria**: Estrategia, Design Systems
- **Complexidade**: Alta
- **Aplicacao**: Planejamento estrategico de quando, como e quem constroi o design system
- **Ultima atualizacao**: 2026-03-06

## Concept

Dan Mall propoe que um design system bem-sucedido requer estrategia explicita respondendo
tres perguntas fundamentais: When (quando investir), How (como construir e escalar) e
Who (quem e responsavel). Muitos design systems falham nao por problemas tecnicos, mas
por falta de clareza estrategica nessas tres dimensoes.

A estrategia de design system nao e um exercicio isolado — ela precisa estar alinhada com
a estrategia de produto, a cultura organizacional e as capacidades reais da equipe.
Um sistema ambicioso demais para a maturidade da organizacao falha tanto quanto um sistema
timido demais para as necessidades reais.

O framework tambem aborda o timing critico: design systems lancados cedo demais viram
abstractions prematuras, e lancados tarde demais lutam contra inércia de patterns
inconsistentes ja estabelecidos.

## When to Use

- Quando se avalia se a organizacao deve investir em um design system
- Quando o design system existente precisa de reboot estrategico
- Quando lideranca pede um plano de investimento para design system
- Quando ha confusao sobre escopo, ownership ou prioridades do sistema
- Quando diferentes stakeholders tem expectativas conflitantes sobre o DS
- Quando se planeja o roadmap do design system para o proximo ano

## How to Apply

### Dimensao 1 — When (Timing)
**Sinais de que e hora de investir**:
1. Pelo menos 3 equipes trabalham no mesmo produto ou familia de produtos
2. Inconsistencias visuais sao visiveis para usuarios e stakeholders
3. Tempo de desenvolvimento de UI esta crescendo sprint a sprint
4. Novos designers/devs demoram muito para se alinhar com padroes
5. A organizacao esta planejando escalar (novos produtos, mercados, plataformas)

**Sinais de que e cedo demais**:
1. Equipe pequena (< 5 pessoas) que se comunica facilmente
2. O produto ainda nao encontrou product-market fit
3. A interface muda radicalmente a cada 2-3 sprints
4. Nao ha padroes repetitivos suficientes para sistematizar

**Como definir o escopo temporal**:
1. Sprint 1-2: Fundacao (tokens, 5-8 componentes core, setup de tooling)
2. Sprint 3-6: Expansao (15-25 componentes, guidelines, documentacao)
3. Sprint 7-12: Maturacao (governance, contribuicao aberta, metricas)
4. Ongoing: Evolucao (novas necessidades, deprecation, refinamento)

### Dimensao 2 — How (Abordagem)
**Estrategia de construcao**:
1. **Extract from production**: Extraia patterns de produtos existentes
   - Menor risco, baseado em necessidades reais
   - Funciona quando ja ha produto em producao
2. **Build from scratch**: Construa o sistema antes dos produtos
   - Maior investimento inicial, mais consistencia desde o inicio
   - Funciona para greenfield ou redesigns completos
3. **Hybrid**: Extraia o core, construa o que falta
   - Equilibra pragmatismo com visao de futuro
   - Abordagem mais comum e recomendada

**Estrategia de adocao**:
1. Comece com 1 equipe piloto voluntaria e entusiasmada
2. Resolva os problemas reais dessa equipe primeiro
3. Use o sucesso do piloto como case para expandir
4. Nao force adocao — facilite-a
5. Crie mecanismos de feedback continuo

**Estrategia de escala**:
1. Defina tiers de componentes:
   - Tier 1: Core (usados por todos, extrema estabilidade)
   - Tier 2: Domain (usados por grupo de produtos, estabilidade alta)
   - Tier 3: Local (usados por 1 produto, flexibilidade alta)
2. Diferentes tiers tem diferentes niveis de governance
3. Promova componentes de Tier 3 para 2 e 2 para 1 conforme adocao

### Dimensao 3 — Who (Responsabilidade)
1. **Executive sponsor**: Garante budget e visibilidade organizacional
2. **Core team**: Implementa e mantém o sistema (ver team models)
3. **Contributors**: Propoem e implementam novos componentes
4. **Consumers**: Usam o sistema e fornecem feedback
5. **Governance board**: Toma decisoes sobre evolucao e breaking changes

Defina RACI (Responsible, Accountable, Consulted, Informed) para:
- Adicionar novos componentes
- Modificar componentes existentes
- Breaking changes e major versions
- Definicao de roadmap e prioridades
- Resolucao de conflitos entre consumidores

## Key Principles

- **Estrategia antes de execucao**: Clareza no when/how/who evita retrabalho
- **Alinhamento com negocio**: DS existe para servir objetivos de negocio, nao para existir
- **Timing importa**: Nem cedo demais (premature abstraction) nem tarde demais (inércia)
- **Escopo incremental**: Comece pequeno, valide, expanda. Nao tente resolver tudo no dia 1
- **Adocao voluntaria**: Forca gera resistencia. Facilidade gera adocao
- **Metricas de sucesso**: Defina como voce sabera que o DS esta funcionando
- **Revisao periodica**: Estrategia nao e estatica — revise a cada quarter

## Examples

### Exemplo 1 — Estrategia para Startup (30 pessoas)
- **When**: Apos 2 produtos lancados com patterns comuns identificados
- **How**: Extract from production, foco em tokens e 8 componentes core
- **Who**: 1 designer + 1 dev dedicam 30% do tempo. Sem equipe separada
- **Timeline**: v1.0 em 6 semanas, iteracao continua
- **Sucesso**: Tempo de build de nova tela reduz 30% em 3 meses

### Exemplo 2 — Estrategia para Enterprise (2000 pessoas)
- **When**: 15 produtos com 40% de sobreposicao visual nao padronizada
- **How**: Equipe dedicada de 6 pessoas, governance board de 8 (reps de cada area)
- **Who**: Core team + federated contributors com review obrigatorio
- **Timeline**: v1.0 em 3 meses, v2.0 em 9 meses com cobertura de 80%
- **Sucesso**: Adocao de 70% dos produtos em 12 meses, NPS > 60

### Exemplo 3 — Reboot Estrategico
Um design system existente com baixa adocao (25%) fez reboot:
1. Pesquisaram por que equipes nao adotavam (survey + entrevistas)
2. Top 3 razoes: componentes nao flexiveis, docs ruins, breaking changes frequentes
3. Nova estrategia: estabilizar v2 com zero breaking changes por 6 meses,
   investir 50% do tempo em docs e DX, criar variantes mais flexiveis
4. Resultado: adocao subiu para 72% em 2 quarters

## Common Pitfalls

- **Estrategia sem execucao**: Plano perfeito no papel que nunca sai do slide deck
- **Execucao sem estrategia**: Comecar a construir sem clareza de escopo e prioridades
- **Ignorar politica organizacional**: DS precisa de sponsor executivo para sobreviver
- **Escopo ambicioso demais**: Tentar ser "o sistema perfeito" no v1 garante fracasso
- **Foco em tech stack**: A ferramenta importa menos que a estrategia e a governanca
- **Nao medir adocao**: Se voce nao sabe se equipes estao usando, nao sabe se funciona
- **Estrategia estatica**: Revisar a cada 6 meses no minimo; o contexto muda

## Cross-References

- [mall-design-system-team-models.md](mall-design-system-team-models.md) — Modelos de equipe (Who)
- [mall-selling-design-to-stakeholders.md](mall-selling-design-to-stakeholders.md) — Vender a estrategia
- [mall-1000-dollar-exercise.md](mall-1000-dollar-exercise.md) — Priorizar investimento
- [frost-maintaining-design-systems.md](frost-maintaining-design-systems.md) — Manutencao pos-lancamento
- [design-system-layer.md](design-system-layer.md) — Camada tecnica do DS
- [governance-layer.md](governance-layer.md) — Governance como parte da estrategia
