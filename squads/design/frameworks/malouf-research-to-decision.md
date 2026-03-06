# Malouf Research to Decision

## Metadata
- **Autor**: Dave Malouf
- **Categoria**: Research, Tomada de Decisao
- **Complexidade**: Media
- **Aplicacao**: Transformar evidencias de pesquisa em decisoes de design acionaveis
- **Ultima atualizacao**: 2026-03-06

## Concept

O framework Research to Decision de Dave Malouf formaliza o caminho entre evidencia bruta
coletada em pesquisa e decisoes concretas de design. O fluxo e: Evidence -> Insight ->
Decision. Muitas equipes falham nao por falta de pesquisa, mas por incapacidade de
transformar dados em acoes claras.

Evidencia e o que voce observou — dados brutos, citacoes, comportamentos. Insight e o
significado que emerge da analise cruzada de multiplas evidencias — o "por que" por tras
do "o que". Decisao e a escolha de design fundamentada no insight, com criterios claros
e alternativas documentadas.

O framework evita dois extremos perigosos: design baseado puramente em intuicao (sem
evidencia) e paralisia por analise (excesso de dados sem acao). O objetivo e criar um
caminho claro e rastreavel entre o que se descobriu e o que se decidiu.

## When to Use

- Apos qualquer rodada de pesquisa com usuarios (entrevistas, testes, surveys)
- Quando a equipe tem dados mas nao sabe o que fazer com eles
- Quando decisoes de design precisam ser justificadas para stakeholders
- Quando ha desacordo sobre a interpretacao de resultados de pesquisa
- Quando se quer criar rastreabilidade entre pesquisa e design decisions
- Quando a equipe precisa priorizar quais insights enderecam primeiro

## How to Apply

### Fase 1 — Evidencia (Coleta e Organizacao)
1. Reuna todos os dados brutos da pesquisa:
   - Notas de entrevista, gravacoes, transcricoes
   - Resultados quantitativos (surveys, analytics, metricas)
   - Observacoes de testes de usabilidade
   - Feedback de canais de suporte
2. Atomize em unidades de evidencia individuais:
   - Cada citacao, observacao ou data point e uma unidade
   - Registre fonte, data e contexto de cada unidade
3. Organize em categorias emergentes (affinity mapping)
4. Nao interprete ainda — apenas agrupe e organize

### Fase 2 — Insight (Analise e Sintese)
1. Para cada cluster de evidencias, pergunte: "O que isso significa?"
2. Formule insights como afirmacoes interpretativas:
   - Ruim: "5 de 8 usuarios clicaram no botao errado"
   - Bom: "Usuarios confundem acao primaria com secundaria porque ambas
     tem o mesmo peso visual"
3. Valide cada insight contra multiplas evidencias (triangulacao)
4. Priorize insights por:
   - Frequencia (quantas evidencias suportam)
   - Severidade (impacto no usuario/negocio)
   - Acionabilidade (podemos fazer algo a respeito)
5. Documente insights com evidencias que os suportam

### Fase 3 — Decision (Escolha Fundamentada)
1. Para cada insight prioritario, gere opcoes de design:
   - Opcao A: [descricao + tradeoffs]
   - Opcao B: [descricao + tradeoffs]
   - Opcao C: [descricao + tradeoffs]
2. Avalie cada opcao contra criterios definidos:
   - Impacto no problema identificado pelo insight
   - Viabilidade tecnica
   - Custo de implementacao
   - Alinhamento com principios de design
3. Documente a decisao tomada com racional explicito
4. Registre alternativas descartadas e por que
5. Defina como validar se a decisao foi correta (metricas, proximo teste)

### Fase 4 — Rastreabilidade
1. Crie um mapa visual: Evidencia -> Insight -> Decisao
2. Mantenha o mapa acessivel para toda a equipe
3. Use o mapa em design reviews para fundamentar escolhas
4. Atualize quando nova evidencia confirmar ou contradizer insights
5. Revise decisoes quando insights mudam com nova pesquisa

## Key Principles

- **Evidencia nao e insight**: Dados brutos precisam de interpretacao para gerar valor
- **Insight nao e decisao**: Entender o problema nao determina automaticamente a solucao
- **Rastreabilidade**: Decisoes devem ser rastreavels ate a evidencia que as fundamenta
- **Triangulacao**: Um insight suportado por uma unica evidencia e fragil
- **Acao como destino**: O objetivo final e sempre uma decisao de design acionavel
- **Humildade epistemica**: Insights sao interpretacoes, nao verdades absolutas
- **Iteracao**: Novas evidencias podem invalidar insights e consequentemente decisoes

## Examples

### Exemplo 1 — Redesign de Checkout
**Evidencia**: 67% de abandono no passo 3 (pagamento). Heatmap mostra cliques
no logo da empresa. 4/6 usuarios em teste disseram "nao sei se e seguro".

**Insight**: Usuarios abandonam o checkout porque nao confiam na seguranca da
transacao — nao ha sinais visuais de confianca no fluxo de pagamento.

**Decisao**: Adicionar trust badges (SSL, payment providers), logo de seguranca
e depoimentos no passo de pagamento. Medir impacto na taxa de conclusao.

### Exemplo 2 — Priorizacao de Insights
Pesquisa com 20 usuarios gerou 45 evidencias agrupadas em 8 insights.
Priorizacao resultou em:
1. Navegacao confusa (12 evidencias, severidade alta, acionavel) — Sprint atual
2. Falta de feedback apos acoes (8 evidencias, severidade media, acionavel) — Proximo sprint
3. Terminologia tecnica demais (6 evidencias, severidade media, requer content strategy) — Backlog

### Exemplo 3 — Decision Log
A equipe manteve um Decision Log no Notion com colunas:
| Decisao | Insight | Evidencias | Alternativas | Data | Status |
Apos 6 meses, o log tinha 47 decisoes rastreadas. Em 3 ocasioes, nova pesquisa
invalidou insights anteriores, e as decisoes foram revisadas proativamente.

## Common Pitfalls

- **Pular para solucoes**: Ir direto de evidencia para decisao sem interpretar ignora o "por que"
- **Confirmation bias**: Selecionar apenas evidencias que confirmam o que voce ja acreditava
- **Insight sem evidencia**: Afirmacoes interpretativas sem dados que as suportem sao opinioes
- **Paralisia por analise**: Coletar evidencias infinitamente sem nunca converter em decisao
- **Decisoes sem alternativas**: Se voce so considerou 1 opcao, nao tomou uma decisao
- **Nao revisitar**: Decisoes tomadas ha 6 meses com evidencias de ha 6 meses podem estar erradas
- **Hierarquia sobre evidencia**: Quando "o chefe quer assim" sobrepoe evidencia de pesquisa,
  o framework perde sentido. Crie cultura de decisao baseada em evidencia

## Cross-References

- [discovery-layer.md](discovery-layer.md) — Pesquisa como camada de descoberta
- [usability-testing-framework.md](usability-testing-framework.md) — Teste como fonte de evidencia
- [measurement-layer.md](measurement-layer.md) — Metricas como evidencia quantitativa
- [malouf-design-quality-model.md](malouf-design-quality-model.md) — Qualidade informada por evidencia
- [strategy-layer.md](strategy-layer.md) — Decisoes estrategicas baseadas em insights
- [malouf-ux-strategy-framework.md](malouf-ux-strategy-framework.md) — Estrategia guiada por pesquisa
