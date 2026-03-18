# Competitive Audit Framework

## Metadata

- **Autor**: Design Squad
- **Categoria**: Research, Estrategia, Analise Competitiva
- **Complexidade**: Media-Alta
- **Aplicacao**: Mapear e avaliar competidores em dimensoes de UI/UX para informar decisoes de design
- **Ultima atualizacao**: 2026-03-18
- **Tags**: competitive-analysis, benchmarking, audit, heuristics, matrix

## Concept

O Competitive Audit Framework estrutura o processo de analisar produtos concorrentes (diretos e
indiretos) em dimensoes relevantes de experiencia: usabilidade, design visual, information
architecture, acessibilidade, performance percebida e inovacao. O objetivo nao e copiar
competidores, mas entender o landscape competitivo para identificar gaps, oportunidades de
diferenciacao e padroes de mercado que usuarios ja aprenderam.

A auditoria gera uma matriz comparativa que permite visualizar onde seu produto esta acima,
na media ou abaixo do mercado em cada dimensao. Isso informa priorizacao de roadmap, justifica
investimento em areas criticas e estabelece benchmarks mensuráveis.

## When to Use

- No inicio de um projeto de redesign para entender o estado do mercado
- Quando stakeholders pedem diferenciacao sem dados concretos sobre competidores
- Para fundamentar decisoes de design com evidencia de mercado
- Ao entrar em um novo segmento ou lancar produto novo
- Para atualizar a estrategia de UX periodicamente (recomendado: semestral)
- Quando metricas de produto indicam perda de competitividade

## How to Apply

### Step 1 — Identificar Competidores
1. Liste competidores diretos (mesma solucao, mesmo publico)
2. Liste competidores indiretos (solucao diferente, mesmo problema)
3. Liste aspiracionais (produtos de outros dominios com UX exemplar)
4. Selecione 4-6 competidores para analise profunda (mais que isso dilui o foco)

### Step 2 — Definir Dimensoes de Avaliacao
Selecione dimensoes relevantes ao contexto. Dimensoes padrao:

| Dimensao              | O que avaliar                                             |
|-----------------------|-----------------------------------------------------------|
| Usabilidade           | Facilidade de completar tarefas-chave, clarity, learnability |
| Design Visual         | Consistencia, hierarquia, tipografia, espacamento, modernidade |
| Information Architecture | Estrutura de navegacao, findability, rotulagem         |
| Acessibilidade (a11y) | Contraste, semantica, keyboard nav, screen reader support |
| Performance Percebida | Velocidade de carregamento, feedback visual, loading states |
| Inovacao / Diferenciacao | Padroes unicos, solucoes criativas, features exclusivas |
| Content & Microcopy   | Tom de voz, clareza de instrucoes, onboarding textual    |

### Step 3 — Definir Tarefas-Chave para Avaliacao
1. Identifique 3-5 user tasks criticas do seu produto
2. Execute as mesmas tarefas em cada competidor
3. Documente a experiencia com screenshots e anotacoes
4. Cronometre cada tarefa para comparacao quantitativa

### Step 4 — Executar a Auditoria
1. Para cada competidor, avalie cada dimensao em escala 1-5:
   - 1 = Muito abaixo do esperado; 5 = Referencia de excelencia
2. Capture evidencias: screenshots, recordings, metricas observaveis
3. Documente pontos fortes e fracos especificos por competidor
4. Registre padroes de design recorrentes (patterns de mercado)

### Step 5 — Construir Matriz Comparativa
Monte tabela consolidada:

| Dimensao        | Seu Produto | Comp. A | Comp. B | Comp. C | Media Mercado |
|-----------------|-------------|---------|---------|---------|---------------|
| Usabilidade     | 3           | 4       | 3       | 5       | 3.8           |
| Design Visual   | 4           | 3       | 4       | 5       | 3.8           |
| a11y            | 2           | 3       | 2       | 4       | 2.8           |

### Step 6 — Sintetizar Findings e Oportunidades
1. Identifique gaps criticos (dimensoes onde voce esta abaixo da media)
2. Identifique diferenciais existentes (onde voce ja esta acima)
3. Identifique oportunidades de diferenciacao (onde ninguem excele)
4. Documente patterns de mercado que usuarios esperam (table stakes)
5. Priorize findings por impacto no usuario x esforco de implementacao

### Step 7 — Documentar e Comunicar
1. Crie report visual com matriz, screenshots e recomendacoes
2. Apresente ao squad com foco em insights acionaveis, nao descricao
3. Atualize o competitive landscape a cada 6 meses

## Examples

### Exemplo 1 — Audit de App de Delivery
Competidores analisados: iFood, Rappi, Uber Eats, 99Food. Tarefas: buscar restaurante,
fazer pedido, rastrear entrega. Finding principal: todos os competidores usam mapa em
real-time para tracking, mas nenhum oferece ETA por etapa (preparo vs. entrega). Oportunidade
de diferenciacao identificada e priorizada como P1.

### Exemplo 2 — Audit de SaaS B2B
Competidores: 4 ferramentas de analytics. Dimensao com maior gap: onboarding — todos
exigiam configuracao complexa. Insight: "time to first insight" era > 30min em todos.
Decisao: investir em setup wizard com dados de exemplo que mostra valor em < 5min.

## Common Pitfalls

- **Copiar em vez de aprender**: O objetivo e insight, nao imitacao — padroes do competidor podem nao funcionar no seu contexto
- **Avaliar sem tarefas**: Navegar livremente nao e audit — defina tarefas especificas e mensuráveis
- **Amostra enviesada**: Analisar so competidores que voce gosta gera confirmacao, nao insight
- **Audit sem acao**: Relatorio bonito que nao gera decisoes e desperdicio de tempo do time
- **Desatualizar**: O mercado muda — audit de 1 ano atras ja esta obsoleto
- **Ignorar competidores indiretos**: Frequentemente a disruptcao vem de fora do segmento

## Cross-References

- [discovery-layer.md](discovery-layer.md) — Audit competitiva como parte do discovery
- [nielsen-heuristics.md](nielsen-heuristics.md) — Heuristicas como base para avaliacao de usabilidade
- [information-architecture-toolkit.md](information-architecture-toolkit.md) — IA como dimensao de avaliacao
- [accessibility-wcag-aa.md](accessibility-wcag-aa.md) — Criterios de a11y para avaliacao
- [strategy-layer.md](strategy-layer.md) — Audit alimenta decisoes estrategicas de UX
- [Competitive Analysis Template](../templates/research/competitive-analysis-template.md) — Template para documentar findings
- [Design Chief](../agents/design-chief.md) — Stakeholder para resultados de audit
