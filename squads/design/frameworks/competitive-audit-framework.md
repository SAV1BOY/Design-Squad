# Competitive Audit Framework

## Metadata

- **Autor**: Design Squad
- **Categoria**: Research, Discovery, Analise Competitiva
- **Complexidade**: Media-Alta
- **Aplicacao**: Mapear e avaliar concorrentes em dimensoes de UI/UX para gerar insights acionaveis
- **Tags:** competitive-analysis, benchmarking, UX-audit, usability, visual-design, a11y, performance
- **Ultima atualizacao**: 2026-03-18

## Concept

O Competitive Audit Framework estrutura o processo de analisar produtos concorrentes (diretos
e indiretos) sob multiplas dimensoes de experiencia: usabilidade, design visual, arquitetura de
informacao, acessibilidade e performance. Diferente de uma analise competitiva de negocio
(que foca em pricing, market share e features), esta auditoria foca exclusivamente na
experiencia do usuario e na qualidade da interface.

O objetivo nao e copiar — e mapear o estado da arte do mercado, identificar gaps e
oportunidades, e estabelecer um baseline contra o qual medir o proprio produto. Uma auditoria
competitiva bem feita revela padroes de interacao que usuarios ja aprenderam (e que voce deve
respeitar), diferenciais reais (nao cosmeticos) de experiencia, e areas onde nenhum competidor
resolve bem o problema (oportunidades de inovacao).

O framework produz dois artefatos principais: uma matriz comparativa com scores por dimensao
e um documento de insights acionaveis com recomendacoes priorizadas para o proprio produto.

## When to Use

- No inicio de um projeto de redesign para entender o cenario competitivo
- Quando se quer validar se o produto esta acima ou abaixo do padrao de mercado
- Para identificar padroes de UX que usuarios ja esperam (table stakes)
- Quando stakeholders pedem justificativa baseada em dados para investir em UX
- Para alimentar decisoes de estrategia de produto com perspectiva de experiencia
- Antes de definir design directions para um novo produto ou feature

## How to Apply

### Fase 1 — Definicao de Escopo

1. **Identifique competidores**: Liste 4-6 competidores divididos em:
   - Diretos: mesma categoria de produto e publico-alvo
   - Indiretos: resolve o mesmo problema de forma diferente
   - Aspiracionais: referencia de excelencia em UX (mesmo fora da categoria)
2. **Defina fluxos a avaliar**: Escolha 3-5 fluxos criticos comparaveis entre todos:
   - Ex: onboarding, busca/discovery, core task, checkout/conversao, suporte
3. **Defina dimensoes de avaliacao**:
   - Usabilidade: eficiencia dos fluxos, clareza de affordances, tratamento de erros
   - Design visual: hierarquia, consistencia, qualidade tipografica, uso de cor
   - Arquitetura de informacao: navegacao, findability, labels, organizacao
   - Acessibilidade: contraste, semantica, navegacao por teclado, suporte a screen reader
   - Performance: tempo de carregamento, responsividade, percepcao de velocidade
   - Content design: clareza do microcopy, tom de voz, onboarding textual

### Fase 2 — Coleta de Dados

1. **Percorra cada fluxo** em cada competidor como usuario real
   - Crie conta, complete tarefas, force erros, teste edge cases
   - Capture screenshots de cada etapa relevante
   - Cronometre tarefas e conte numero de passos
2. **Avalie acessibilidade** com ferramentas automatizadas (axe, Lighthouse)
   - Teste navegacao por teclado manualmente
   - Verifique contraste com color contrast checker
3. **Meca performance**: Lighthouse scores, Core Web Vitals, tempo de first meaningful paint
4. **Documente padroes de interacao**: Que patterns de UI cada competidor usa para os mesmos
   problemas? (ex: como fazem onboarding? filtros? empty states? error recovery?)
5. **Capture microcopy**: Anote exemplos de copy em pontos criticos (CTAs, erros, empty states,
   confirmacoes)

### Fase 3 — Scoring e Matriz Comparativa

1. Para cada dimensao, avalie cada competidor em escala 1-5:
   - 1: Abaixo do aceitavel — problemas graves e frequentes
   - 2: Fraco — problemas notaveis que impactam experiencia
   - 3: Adequado — funciona mas sem destaque
   - 4: Bom — experiencia solida com poucos problemas
   - 5: Excelente — referencia de qualidade, experiencia fluida
2. Monte tabela comparativa:
   ```
   | Dimensao          | Produto | Comp A | Comp B | Comp C |
   |-------------------|---------|--------|--------|--------|
   | Usabilidade       |    3    |   4    |   2    |   4    |
   | Visual            |    2    |   5    |   3    |   4    |
   | IA                |    3    |   3    |   4    |   3    |
   | Acessibilidade    |    1    |   2    |   2    |   4    |
   | Performance       |    4    |   3    |   3    |   5    |
   | Content design    |    3    |   4    |   2    |   3    |
   ```
3. Calcule score medio por competidor e por dimensao
4. Identifique onde seu produto esta acima/abaixo da media do mercado

### Fase 4 — Analise de Patterns e Insights

1. **Identifique table stakes**: Patterns presentes em 3+ competidores sao expectativas do
   usuario. Se voce nao tem, e um gap.
2. **Identifique diferenciais**: O que apenas 1 competidor faz bem? E replicavel? E relevante?
3. **Identifique oportunidades**: Onde nenhum competidor resolve bem? Esse e o espaco para
   inovacao real.
4. Para cada insight, documente:
   - Observacao: o que foi visto
   - Implicacao: o que isso significa para o usuario
   - Recomendacao: o que fazer no proprio produto
   - Prioridade: alta/media/baixa baseado em impacto x esforco

### Fase 5 — Documentacao e Comunicacao

1. Compile em relatorio visual com screenshots side-by-side
2. Destaque top 5-7 insights mais acionaveis
3. Conecte cada insight a uma area do proprio produto que pode ser melhorada
4. Apresente para stakeholders com foco em oportunidades (nao apenas problemas)
5. Armazene na base de pesquisa para consulta futura

## Key Principles

- **Avaliar experiencia, nao features**: Nao e sobre quem tem mais features — e sobre quem
  resolve melhor o problema do usuario
- **Competidor indireto importa**: Usuarios comparam sua experiencia com tudo que usam, nao
  apenas com concorrentes diretos
- **Screenshots sao evidencia**: Sempre documente visualmente — memoria e seletiva
- **Score sem contexto e inutil**: Um "3" em usabilidade precisa de exemplos concretos
- **Repita periodicamente**: O cenario competitivo muda. Auditorias devem ser anuais no minimo
- **Separar table stakes de diferenciais**: Nem tudo que o competidor faz e relevante para copiar

## Examples

### Exemplo 1 — Auditoria de App de Fintech
Avaliados 5 apps bancarios (Nubank, Inter, C6, Neon, Itau). Dimensao com maior variacao:
acessibilidade (scores de 1 a 4). Insight principal: nenhum app tratava bem erros de
transferencia com linguagem clara — oportunidade de diferenciar via content design.
Recomendacao: investir em microcopy de erro como diferencial competitivo.

### Exemplo 2 — SaaS B2B de Project Management
Comparacao entre Asana, Linear, Monday e Notion. Todos tinham onboarding em 5+ passos.
Tree test com usuarios revelou que 60% abandonava onboarding no step 3. Insight: mercado
inteiro tem onboarding longo — oportunidade de diferenciar com progressive onboarding que
ensina durante o uso real.

### Exemplo 3 — E-commerce de Moda
Auditoria revelou que 4 de 5 competidores usavam filtro lateral em desktop e bottom sheet
em mobile — table stake confirmado. Proprio produto usava modal para filtros em ambas
plataformas, gerando 35% mais cliques para completar filtro. Correcao gerou +12% de
conversao em filtro.

## Common Pitfalls

- **Avaliar tudo de todos**: Focar em 3-5 fluxos criticos. Auditoria exaustiva nunca termina
- **Copiar sem entender**: Adotar pattern de competidor sem entender o contexto do proprio
  usuario gera Frankenstein UX
- **Bias de confirmacao**: Nao comece com conclusao e depois colete evidencia. Avalie com
  criterios pre-definidos
- **Ignorar contexto de uso**: Um app bancario usado em transporte publico tem restricoes
  diferentes de um SaaS usado em desktop
- **Auditoria como exercicio academico**: Se nao gera recomendacoes acionaveis conectadas
  ao roadmap, e desperdicio de tempo
- **Comparar versoes diferentes**: Documente versao e data da avaliacao — produtos mudam rapido

## Cross-References

- `tasks/discovery/competitive-ui-audit` — Task detalhada de execucao da auditoria
- `templates/research/competitive-analysis-template` — Template de documento de analise
- `agents/ux-design-expert` — Agente que executa auditorias competitivas
- `frameworks/nielsen-heuristics` — Heuristicas usadas como lens de avaliacao de usabilidade
- `frameworks/accessibility-wcag-aa` — Criterios de avaliacao de acessibilidade
- `frameworks/heart-metrics-framework` — Metricas para comparar experiencia entre produtos
- `checklists/usability-test-quality` — Criterios de qualidade para validacoes pos-auditoria
- `frameworks/information-architecture-toolkit` — Avaliacao de IA como dimensao da auditoria
