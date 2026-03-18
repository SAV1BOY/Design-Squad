# Card Sort Framework

## Metadata

- **Autor**: Design Squad
- **Categoria**: Research, Information Architecture, Estrutura
- **Complexidade**: Media
- **Aplicacao**: Planejar e executar card sorting para informar information architecture
- **Ultima atualizacao**: 2026-03-18
- **Tags**: card-sort, open-sort, closed-sort, hybrid-sort, IA, taxonomy, dendrogram

## Concept

O Card Sort Framework guia o processo de usar card sorting — tecnica onde participantes
organizam itens em grupos — para descobrir como usuarios categorizam informacao mentalmente.
O resultado informa decisoes de information architecture: estrutura de navegacao, rotulagem
de menus, agrupamento de features e taxonomia de conteudo.

Existem tres variantes: aberto (participantes criam categorias), fechado (categorias
pre-definidas) e hibrido (categorias sugeridas mas editaveis). Cada uma serve a um momento
diferente do projeto. A analise transforma agrupamentos individuais em estrutura consensual
usando dendrogramas, similarity matrices e completion rates.

## When to Use

- Ao criar a information architecture de um produto novo
- Quando testes de usabilidade revelam problemas de findability
- Para validar ou refinar uma estrutura de navegacao existente
- Ao reorganizar conteudo apos crescimento significativo do produto
- Para comparar modelos mentais de diferentes segmentos de usuarios
- Quando stakeholders discordam sobre estrutura — dados de usuarios resolvem debates

## How to Apply

### Step 1 — Definir Tipo e Objetivo
1. **Open sort**: Use quando nao existe estrutura — quer descobrir categorias naturais
2. **Closed sort**: Use quando a estrutura existe — quer validar se itens encaixam
3. **Hybrid sort**: Use quando ha estrutura proposta mas flexibilidade para ajustes
4. Defina a pergunta: "Como usuarios agrupam [tipo de conteudo] no contexto de [produto]?"

### Step 2 — Preparar os Cards
1. Liste todos os itens a serem categorizados (features, paginas, conteudos)
2. Limite a 30-60 cards — mais que isso causa fadiga e reduz qualidade
3. Escreva labels claros e auto-explicativos (sem jargao interno)
4. Teste os labels com 2-3 pessoas para verificar ambiguidade
5. Randomize a ordem de apresentacao para cada participante
6. Para closed sort: defina 5-10 categorias com labels intuitivos

### Step 3 — Recrutar Participantes
1. Minimo 15 participantes para analise estatistica confiavel (ideal: 20-30)
2. Recrute do publico-alvo real, nao colegas internos
3. Inclua diversidade de experiencia (novatos e experientes com o dominio)
4. Para card sort remoto: use ferramentas como Optimal Workshop ou Maze
5. Para presencial: prepare cards fisicos ou post-its

### Step 4 — Executar
1. Explique a tarefa: "Agrupe estes itens da forma que faz sentido pra voce"
2. Para open sort: "Crie grupos e de um nome para cada grupo"
3. Para closed sort: "Coloque cada item na categoria que voce acha mais adequada"
4. Nao interfira durante a atividade — observe silenciosamente
5. Apos agrupar, peca para o participante explicar suas decisoes (think-aloud)
6. Registre tempo total e dificuldades observadas
7. Permita que participantes criem grupo "nao sei" para itens ambiguos

### Step 5 — Analisar Resultados
1. **Similarity matrix**: Calcule % de vezes que cada par de itens foi agrupado junto
2. **Dendrogram**: Gere arvore hierarquica mostrando clusters naturais
3. **Standardization matrix** (closed sort): % de participantes que colocou item em cada categoria
4. Identifique itens problematicos: baixa concordancia = label ambiguo ou item cross-category
5. Identifique categorias emergentes (open sort): nomes mais frequentes para cada grupo
6. Compare resultados entre segmentos de usuarios se houver

### Step 6 — Converter para Information Architecture
1. Clusters com alta concordancia (>70%) viram categorias na navegacao
2. Itens com baixa concordancia precisam de solucao: cross-linking, busca, ou re-rotulagem
3. Crie draft da estrutura de navegacao baseada nos clusters
4. Valide o draft com tree testing (complemento do card sort)
5. Itere: card sort > draft IA > tree test > refinamento > implementacao

## Examples

### Exemplo 1 — IA de App de Saude
40 cards (features do app), open sort com 25 participantes. Resultado: usuarios criaram
consistentemente 6 grupos. Surpresa: "Agendar consulta" e "Telemedicina" foram agrupados
juntos por 88% — mas no app estavam em secoes separadas. Redesign unificou em "Consultas"
com filtro presencial/online. Findability da feature subiu 34%.

### Exemplo 2 — Reorganizacao de Menu (SaaS B2B)
Closed sort com 7 categorias de menu existentes, 35 cards. Resultado: 12 itens tinham
concordancia <40% — usuarios nao sabiam onde encontra-los. 3 categorias tinham overlap
significativo. Solucao: merge de 7 para 5 categorias + busca contextual. Tree test posterior
confirmou melhoria de 22% em task completion.

## Common Pitfalls

- **Cards ambiguos**: Se o label nao e claro, voce esta testando compreensao do label, nao a IA
- **Muitos cards**: Acima de 60, a fadiga distorce os ultimos agrupamentos
- **Amostra pequena**: Com <15 participantes, patterns individuais parecem consenso
- **Ignorar outliers**: Agrupamentos incomuns podem revelar modelos mentais de segmentos especificos
- **Card sort sem tree test**: Card sort mostra como usuarios agrupam, tree test valida se encontram
- **Apenas um tipo**: Open sort descobre, closed sort valida — use ambos em fases diferentes

## Cross-References

- [UX Design Expert](../agents/ux-design-expert.md) — Agente especialista em research de IA
- [Research Plan Quality Checklist](../checklists/research-plan-quality.md) — Checklist de qualidade do plano de pesquisa
- [Card Sort Template](../templates/research/card-sort-template.md) — Template para planejamento e documentacao
- [information-architecture-toolkit.md](information-architecture-toolkit.md) — Toolkit completo de IA
- [discovery-layer.md](discovery-layer.md) — Card sort como atividade de discovery
- [interview-framework.md](interview-framework.md) — Entrevistas complementam card sort com contexto qualitativo
- [insight-synthesis-framework.md](insight-synthesis-framework.md) — Sintese de resultados de card sort
