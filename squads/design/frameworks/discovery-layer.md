# Discovery Layer

## Metadata
- **Autor**: Design Squad
- **Categoria**: Stack Layer, Research, Discovery
- **Complexidade**: Media
- **Aplicacao**: Fase inicial de qualquer projeto de design — pesquisa, dados, contexto
- **Ultima atualizacao**: 2026-03-06

## Concept

A Discovery Layer e a primeira camada do stack de design, responsavel por garantir que
a equipe entenda profundamente o problema antes de projetar solucoes. Engloba pesquisa
com usuarios, analise de dados, mapeamento de contexto de negocio e definicao clara
do espaco do problema.

O principio fundamental e: a qualidade da solucao e limitada pela qualidade do entendimento
do problema. Discovery mal feita leva a solucoes elegantes para problemas errados —
o tipo mais caro de desperdicio em design.

A camada nao se limita ao inicio do projeto. Discovery e continua: cada iteracao de
design gera novos aprendizados que alimentam novas questoes de pesquisa.

## When to Use

- No inicio de qualquer projeto ou feature nova
- Quando a equipe nao tem confianca de que entende o problema
- Quando dados qualitativos e quantitativos divergem
- Quando stakeholders tem visoes conflitantes sobre o que o usuario precisa
- Quando se redesenha uma experiencia existente
- Quando metricas de produto indicam problemas sem causa clara

## How to Apply

### Dimensao 1 — Pesquisa com Usuarios
1. **Entrevistas exploratórias**: 5-8 usuarios, 45-60 min cada
   - Foco em comportamentos e motivacoes, nao opinioes
   - Perguntas abertas: "Me conta como voce faz X hoje"
   - Observe o que fazem, nao so o que dizem
2. **Observacao contextual**: Assista usuarios em seu ambiente real
3. **Surveys quantitativos**: Para validar hipoteses em escala
4. **Analise de suporte**: Tickets, chamados, FAQs — dor real

### Dimensao 2 — Dados e Analytics
1. Mapeie funis de conversao existentes — onde usuarios desistem?
2. Analise comportamento: heatmaps, session recordings, clickmaps
3. Identifique segmentos com comportamentos distintos
4. Cruze dados quanti com insights quali para triangulacao
5. Defina baseline metrics para medir impacto de mudancas futuras

### Dimensao 3 — Contexto de Negocio
1. Entenda objetivos de negocio e como o projeto se conecta a eles
2. Mapeie restricoes: tecnicas, legais, financeiras, temporais
3. Analise competidores: o que fazem, como se diferenciam
4. Identifique stakeholders e suas expectativas
5. Documente premissas e riscos

### Dimensao 4 — Definicao do Problema
1. Sintetize pesquisa em problem statements claros:
   - "Usuarios de [segmento] precisam de [necessidade] porque [motivacao],
     mas atualmente [barreira] impede que [resultado desejado]"
2. Valide problem statements com usuarios e stakeholders
3. Priorize problemas por impacto e viabilidade
4. Defina escopo: o que esta dentro e fora desta iniciativa
5. Crie success criteria: como saberemos que o problema foi resolvido

## Key Principles

- **Problema antes de solucao**: Entender antes de projetar
- **Multiplas fontes**: Triangule entre pesquisa qualitativa, quantitativa e analytics
- **Usuarios reais**: Fale com usuarios, nao com proxies (PMs, suporte, stakeholders)
- **Bias awareness**: Reconheca e mitigue vieses de pesquisa
- **Discovery continua**: Nao e uma fase — e uma pratica permanente
- **Suficiencia, nao exaustao**: Pesquise o suficiente para decidir, nao para publicar
- **Compartilhamento**: Insights sao da equipe, nao do pesquisador

## Examples

### Exemplo 1 — Discovery para Redesign de Onboarding
- 8 entrevistas com usuarios que abandonaram (qualitativo)
- Analise de funil: 67% drop-off no step 3 de 5 (quantitativo)
- Heatmap: usuarios procuravam botao "pular" inexistente
- Problem statement: "Novos usuarios abandonam o onboarding porque o step 3
  pede informacoes que eles nao tem disponivel no momento, e nao ha opcao
  de continuar sem essas informacoes"
- Solucao informada: tornar step 3 opcional com lembrete posterior

### Exemplo 2 — Discovery Leve (1 Semana)
Para features menores, discovery leve funciona:
- 3 entrevistas rapidas (30 min cada)
- Review de tickets de suporte relacionados (2h)
- Analise de analytics existente (2h)
- Sintese e problem statement (2h)
Total: ~15 horas. Suficiente para features pequenas e medias.

### Exemplo 3 — Discovery com Dados Contraditorios
Analytics mostrava que 85% dos usuarios completavam um fluxo. Entrevistas revelaram
que muitos completavam mas com frustacao ("eu consegui mas foi horrivel").
A triangulacao entre dados e pesquisa redefiniu o problema: nao era conclusao, era
experiencia durante a conclusao.

## Common Pitfalls

- **Skip discovery**: "Nos ja sabemos o que o usuario quer" e a frase mais perigosa
- **Discovery eterna**: Pesquisar indefinidamente para evitar decidir. Defina timebox
- **Confirmation bias**: Buscar evidencia que confirme sua hipotese pre-existente
- **Amostra enviesada**: Falar so com power users ou so com usuarios insatisfeitos
- **Dados sem contexto**: "60% clicaram no botao" nao e insight — por que clicaram?
- **Discovery sem sintese**: Horas de entrevista sem sintese estruturada sao desperdicadas
- **Insights engavetados**: Pesquisa que nao informa decisoes de design e desperdicio

## Cross-References

- [strategy-layer.md](strategy-layer.md) — Discovery informa estrategia
- [ux-layer.md](ux-layer.md) — Discovery alimenta decisoes de UX
- [malouf-research-to-decision.md](malouf-research-to-decision.md) — Evidencia -> insight -> decisao
- [usability-testing-framework.md](usability-testing-framework.md) — Teste como discovery avaliativa
- [measurement-layer.md](measurement-layer.md) — Dados quantitativos como discovery
- [malouf-facilitation-framework.md](malouf-facilitation-framework.md) — Workshops de discovery
