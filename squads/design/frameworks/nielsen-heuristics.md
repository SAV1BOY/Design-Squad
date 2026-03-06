# Nielsen's Usability Heuristics

## Metadata

- **Origem:** Jakob Nielsen e Rolf Molich (1990, refinado 1994)
- **Categoria:** Usability Evaluation Framework
- **Complexidade:** Basica a Intermediaria
- **Aplicacao:** Avaliacao heuristica, design review, criterios de qualidade
- **Tags:** heuristics, usability, evaluation, expert-review, design-quality

## Concept

As 10 heuristicas de usabilidade de Nielsen sao principios gerais para design de interacao.
Nao sao regras rigidas, mas heuristicas — guidelines amplas baseadas em decadas de pesquisa
em usabilidade. Desde sua publicacao em 1994, permanecem como o framework de avaliacao de
usabilidade mais utilizado no mundo por profissionais de UX.

A avaliacao heuristica e um metodo de inspecao onde especialistas examinam a interface
contra essas heuristicas, identificando violacoes e classificando sua severidade. E mais
rapida e barata que testes com usuarios, embora nao os substitua completamente. A combinacao
de avaliacao heuristica (para encontrar problemas obvios) e testes de usabilidade (para
encontrar problemas nao-obvios) e a abordagem mais eficaz.

Cada heuristica e deliberadamente ampla, aplicavel a qualquer tipo de interface — web,
mobile, desktop, voz, AR/VR. Essa generalidade e sua forca e sua fraqueza simultaneamente.
A forca e a universalidade de aplicacao. A fraqueza e que requer experiencia e julgamento
para aplicar com nuance em contextos especificos.

## When to Use

- Em design reviews para avaliar sistematicamente a qualidade de usabilidade do produto
- Como checklist antes de testes com usuarios, para eliminar problemas obvios previamente
- Para fundamentar feedback de design com criterios objetivos e amplamente reconhecidos
- Em auditorias de UX de produtos existentes para identificar areas prioritarias de melhoria
- Como vocabulario compartilhado entre designers, PMs e engenheiros ao discutir qualidade

## How to Apply

1. **Selecione avaliadores:** Recrute 3-5 especialistas em UX. Pesquisas mostram que 3-5
   avaliadores encontram aproximadamente 75% dos problemas de usabilidade. Cada avaliador
   deve inspecionar independentemente, sem influencia dos demais.

2. **Defina escopo e tarefas:** Determine quais fluxos ou areas da interface serao avaliados.
   Defina 3-5 tarefas representativas que os avaliadores devem simular durante a inspecao.

3. **Inspecione contra cada heuristica:** Cada avaliador percorre a interface executando as
   tarefas definidas, verificando violacoes de cada uma das 10 heuristicas. Documente cada
   violacao com: heuristica violada, localizacao exata, descricao e screenshot.

4. **Classifique severidade:** Use a escala de Nielsen: 0 = nao e um problema de usabilidade;
   1 = cosmetico apenas; 2 = problema menor; 3 = problema maior; 4 = catastrofico. A
   severidade combina frequencia, impacto e persistencia do problema.

5. **Consolide achados:** Reuna os achados de todos os avaliadores. Problemas encontrados
   por multiplos avaliadores independentemente tendem a ser mais graves e prioritarios.

6. **Aja sobre os resultados:** Crie action items para cada problema. Problemas de severidade
   4 devem ser resolvidos imediatamente. Severidade 3 antes do proximo release. Severidade
   1-2 conforme capacidade e oportunidade.

## Key Principles

As 10 heuristicas com descricao e exemplos praticos:

### 1. Visibility of System Status
O sistema deve informar ao usuario o que esta acontecendo, com feedback apropriado em tempo
razoavel. **Exemplo:** Barra de progresso durante upload. Indicador de "digitando..." em
chat. Confirmacao visual apos salvar. **Violacao:** Botao de envio que nao muda de estado
apos clique, deixando o usuario sem saber se a acao foi registrada.

### 2. Match Between System and the Real World
O sistema deve usar linguagem, conceitos e convencoes familiares ao usuario. **Exemplo:**
Icone de lixeira para deletar. Carrinho de compras em e-commerce. Linguagem em PT-BR sem
jargao tecnico. **Violacao:** "Error 500: Internal Server Exception" para usuarios finais.

### 3. User Control and Freedom
Usuarios escolhem funcoes por engano e precisam de saida de emergencia. Suporte a undo e
redo. **Exemplo:** "Desfazer" apos deletar email no Gmail. Botao cancelar em todo modal.
Back button funcional. **Violacao:** Wizard de 8 etapas sem opcao de voltar.

### 4. Consistency and Standards
Usuarios nao devem se perguntar se palavras ou acoes diferentes significam a mesma coisa.
**Exemplo:** Botao primario sempre com mesmo estilo. Links sempre sublinhados ou em azul.
**Violacao:** "Salvar" em uma tela, "Gravar" em outra, "Confirmar" em terceira — mesma acao.

### 5. Error Prevention
Melhor que mensagens de erro e design que previne erros. **Exemplo:** Confirmacao antes de
deletar conta. Autocomplete em campos de endereco. Botao desabilitado ate validacao.
**Violacao:** Campo de data que aceita texto livre sem validacao.

### 6. Recognition Rather Than Recall
Minimize carga de memoria tornando elementos e opcoes visiveis. **Exemplo:** Historico de
buscas recentes. Sugestoes de autocomplete. Breadcrumbs. Thumbnails de documentos.
**Violacao:** Exigir memorizacao de codigo de referencia sem exibi-lo.

### 7. Flexibility and Efficiency of Use
Atalhos invisiveis para novatos podem acelerar a interacao para experts. **Exemplo:**
Atalhos de teclado (Ctrl+K para busca). Gestos de swipe. Templates pre-definidos.
**Violacao:** 5 cliques para acao que experts realizam 50 vezes por dia, sem atalho.

### 8. Aesthetic and Minimalist Design
Dialogos nao devem conter informacao irrelevante que compete com informacao relevante.
**Exemplo:** Checkout com apenas campos essenciais. Onboarding com uma acao por tela.
**Violacao:** Homepage com 15 banners, pop-up, chatbot e cookie notice simultaneamente.

### 9. Help Users Recognize, Diagnose and Recover from Errors
Mensagens de erro em linguagem simples, indicando problema e sugerindo solucao. **Exemplo:**
"Email ja cadastrado. Esqueceu sua senha?" em vez de "Error: duplicate entry".
**Violacao:** "Ocorreu um erro inesperado. Tente novamente mais tarde."

### 10. Help and Documentation
Informacao de ajuda deve ser facil de buscar, focada na tarefa e com passos concretos.
**Exemplo:** Tooltips contextuais. Centro de ajuda com busca. Onboarding interativo.
**Violacao:** FAQ com 200 perguntas sem busca ou categorizacao util.

## Examples

### Auditoria de App Bancario
Avaliacao com 4 especialistas identificou 47 violacoes em fluxos criticos. Severidade 4:
transferencia PIX sem confirmacao antes de enviar (heuristica 5). Severidade 3: mensagens
de erro em ingles tecnico (heuristica 9). Severidade 2: atalhos inexistentes para
operacoes frequentes (heuristica 7). Priorizacao por severidade permitiu corrigir
problemas criticos em 2 sprints.

### Redesign de Painel Administrativo
Avaliacao revelou violacoes sistematicas: heuristica 1 (nenhuma acao bulk tinha progresso),
heuristica 4 (tres estilos diferentes de tabela), heuristica 6 (filtros complexos sem
salvar configuracoes). O redesign unificou padroes e adicionou feedback a todas as acoes.

## Common Pitfalls

- **Avaliacao sem severidade:** Listar problemas sem classificar severidade nao ajuda a
  priorizar acoes. Use a escala 0-4 consistentemente para cada violacao.

- **Confundir heuristica com regra rigida:** Heuristicas sao guidelines, nao leis absolutas.
  Confirmacao antes de cada acao menor (heuristica 5) pode violar eficiencia (heuristica 7).

- **Avaliador unico:** Um unico avaliador encontra apenas 35% dos problemas. Use minimo
  3 avaliadores independentes para cobertura adequada.

- **Substituir testes com usuarios:** Avaliacao heuristica encontra problemas previsiveis.
  Testes com usuarios encontram problemas que ninguem previu. Ambos sao necessarios.

## Cross-References

- [Interaction Design Principles](interaction-design-principles.md) — Principios de IxD
  fundamentam e complementam as heuristicas de usabilidade
- [Gestalt Principles](gestalt-principles.md) — Gestalt fundamenta a heuristica 8
  (aesthetic and minimalist design)
- [Fitts's Law](fitts-law.md) — Informa decisoes sobre tamanho e posicao de alvos
- [Hick's Law](hick-law.md) — Informa decisoes sobre complexidade de menus e opcoes
- [HEART Metrics Framework](heart-metrics-framework.md) — Metricas para quantificar o
  impacto de violacoes de heuristicas na experiencia
