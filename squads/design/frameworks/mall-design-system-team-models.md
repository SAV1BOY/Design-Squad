# Mall Design System Team Models

## Metadata
- **Autor**: Dan Mall
- **Categoria**: Organizacao de Equipes, Design Systems
- **Complexidade**: Alta
- **Aplicacao**: Organizacoes decidindo como estruturar equipes de design system
- **Ultima atualizacao**: 2026-03-06

## Concept

Dan Mall identifica tres modelos fundamentais de equipe para design systems: Centralized,
Federated e Hybrid. Cada modelo tem tradeoffs distintos em termos de consistencia,
velocidade, ownership e escalabilidade. A escolha do modelo correto depende do tamanho
da organizacao, maturidade do design system e cultura organizacional.

Nao existe modelo universalmente melhor — existe o modelo mais adequado para o contexto
atual da organizacao, e esse modelo deve evoluir conforme a organizacao muda.

O framework ajuda liderancas de design a tomar decisoes informadas sobre estrutura de
equipe e a antecipar os desafios de cada modelo.

## When to Use

- Quando a organizacao esta criando ou reestruturando a equipe de design system
- Quando o modelo atual nao esta funcionando (consistencia baixa, velocidade lenta)
- Quando a organizacao cresceu e o modelo precisa evoluir
- Quando ha debate sobre ownership do design system
- Quando se planeja investimento em design system e precisa definir headcount
- Quando equipes de produto reclamam que o sistema nao atende suas necessidades

## How to Apply

### Modelo 1 — Centralized (Equipe Dedicada)
**Estrutura**: Uma equipe separada e dedicada exclusivamente ao design system.
Nao trabalha em nenhum produto — o sistema e o produto deles.

**Como implementar**:
1. Monte uma equipe de 3-8 pessoas (designers + devs + tech writer)
2. Defina a equipe como dona do design system — todos os componentes, tokens e docs
3. Equipes de produto sao consumidoras: usam o sistema e reportam necessidades
4. A equipe central prioriza, implementa e publica updates
5. Mantenha canal de comunicacao aberto para requests e feedback
6. Publique roadmap trimestral baseado nas necessidades dos consumidores

**Tradeoffs**:
- Alta consistencia e qualidade
- Pode se desconectar das necessidades reais dos produtos
- Pode se tornar bottleneck se demanda superar capacidade
- Custo alto de headcount dedicado

### Modelo 2 — Federated (Distribuido)
**Estrutura**: Nao ha equipe dedicada. Designers e devs de cada produto contribuem
para o design system como parte do seu trabalho regular.

**Como implementar**:
1. Designe 1 "champion" de design system em cada equipe de produto
2. Champions se reunem regularmente para coordenar contribuicoes
3. Estabeleca guidelines de contribuicao claras (quality bar, process)
4. Cada equipe contribui componentes que criou para uso geral
5. Um "governance board" de champions aprova novas adicoes
6. Rotacione responsabilidades de manutencao entre equipes

**Tradeoffs**:
- Conectado as necessidades reais dos produtos
- Ownership distribuido pode resultar em inconsistencia
- Depende da boa vontade e tempo disponivel dos champions
- Dificulta manter qualidade uniforme

### Modelo 3 — Hybrid (Combinado)
**Estrutura**: Uma equipe core pequena dedicada ao sistema, complementada por
contribuidores das equipes de produto.

**Como implementar**:
1. Monte equipe core de 2-4 pessoas para: arquitetura, tokens, governance, docs
2. Equipes de produto contribuem componentes seguindo guidelines do core team
3. Core team revisa, valida e integra contribuicoes
4. Core team define standards, ferramentas e processos
5. Contribuidores de produto implementam seguindo esses standards
6. Office hours semanais para alinhamento e suporte

**Tradeoffs**:
- Equilibra consistencia com conexao ao produto
- Requer coordenacao cuidadosa entre core e contribuidores
- Core team precisa ser excelente em review e feedback
- Custo moderado de headcount

### Decisao — Como Escolher
| Criterio                    | Centralized | Federated | Hybrid |
|-----------------------------|-------------|-----------|--------|
| Organizacao < 50 pessoas    |             | Bom       | Ideal  |
| Organizacao 50-200 pessoas  | Bom         |           | Ideal  |
| Organizacao > 200 pessoas   | Ideal       |           | Bom    |
| DS em fase inicial          |             | Bom       | Ideal  |
| DS maduro e estavel         | Ideal       | Bom       |        |
| Alta necessidade de inovacao|             | Ideal     | Bom    |
| Alta necessidade de controle| Ideal       |           | Bom    |

## Key Principles

- **Contexto determina modelo**: Nao ha modelo universalmente superior
- **Evolucao e natural**: Comece com um modelo e evolua conforme a necessidade
- **Ownership claro**: Independente do modelo, alguem precisa ser responsavel por cada parte
- **Comunicacao proporcional**: Modelos mais distribuidos requerem mais coordenacao
- **Incentivos alinhados**: Contribuidores precisam ser reconhecidos e recompensados
- **Quality bar unico**: Independente de quem contribui, o padrao de qualidade e o mesmo
- **Sustentabilidade financeira**: O modelo precisa ser defensavel em termos de investimento

## Examples

### Exemplo 1 — Transicao Federated para Hybrid
Uma startup de 80 pessoas comecou com modelo federated: designers de 5 squads contribuiam
componentes. Apos 1 ano, inconsistencias acumularam — 3 variacoes de modal, tokens
divergentes entre squads. Solucao: contrataram 1 designer de sistemas + 1 dev frontend
como core team. Em 3 meses, consolidaram os gaps e estabeleceram governance.
Squads continuaram contribuindo, agora com review do core team.

### Exemplo 2 — Centralized com Embaixadores
Uma empresa de 500 pessoas tinha equipe centralizada de 6 pessoas. Problema:
equipes de produto sentiam que o sistema nao atendia necessidades especificas.
Solucao: designaram 1 "embaixador do DS" em cada squad de produto. Embaixadores
participavam de planning do core team e levavam necessidades de volta.
Satisfacao com o DS subiu de 5.8/10 para 8.2/10 em 2 quarters.

### Exemplo 3 — Hybrid com Rotation Program
Uma empresa criou um programa de rotacao: a cada quarter, 1 designer de produto
passava 3 meses embarcado no core team do DS. Beneficios: o rotacionado aprendia
profundamente sobre o sistema e voltava para sua squad como expert.
Em 1 ano, 4 squads tinham um expert em DS, melhorando a adocao organicamente.

## Common Pitfalls

- **Copiar o modelo de outra empresa**: O que funciona para Shopify nao funciona para
  sua startup de 30 pessoas. Avalie seu contexto real
- **Modelo hibrido sem core team empoderado**: Se o core team nao tem autoridade para
  recusar contribuicoes de baixa qualidade, o modelo nao funciona
- **Federated sem incentivos**: Se contribuir para o DS nao e valorizado na avaliacao
  de performance, ninguem vai priorizar
- **Centralized sem feedback loop**: Equipe isolada que nao ouve consumidores perde relevancia
- **Mudar de modelo sem preparacao**: Transicoes de modelo precisam de comunicacao,
  expectativas claras e periodo de adaptacao
- **Subestimar o custo de coordenacao**: Modelos distribuidos requerem investimento
  significativo em comunicacao e alinhamento
- **Nao definir ownership de componentes**: Em qualquer modelo, cada componente precisa
  ter um owner claro

## Cross-References

- [mall-design-that-scales.md](mall-design-that-scales.md) — Escala como driver de modelo
- [mall-superfriendly-model.md](mall-superfriendly-model.md) — Modelo fluido de alocacao
- [mall-design-system-strategy.md](mall-design-system-strategy.md) — Estrategia que informa modelo
- [frost-maintaining-design-systems.md](frost-maintaining-design-systems.md) — Manutencao por modelo
- [malouf-designops-framework.md](malouf-designops-framework.md) — Operacoes que suportam cada modelo
- [governance-layer.md](governance-layer.md) — Governanca adaptada ao modelo
