# Insight Synthesis Framework

## Metadata

- **Autor**: Design Squad
- **Categoria**: Research, Analise, Decision-making
- **Complexidade**: Media-Alta
- **Aplicacao**: Transformar dados brutos de pesquisa em insights acionaveis e priorizados
- **Ultima atualizacao**: 2026-03-18
- **Tags**: affinity-mapping, thematic-analysis, insight-statements, prioritization, synthesis

## Concept

O Insight Synthesis Framework estrutura o processo de transformar dados brutos de pesquisa
(notas de entrevista, observacoes de testes, respostas de survey, dados de analytics) em
insights acionaveis que direcionam decisoes de design. A sintese e o momento mais critico
do research — sem ela, dados viram relatorios descritivos em vez de catalisadores de acao.

O framework combina quatro tecnicas complementares: affinity mapping para agrupar observacoes,
thematic analysis para identificar padroes, insight statements para articular discoveries
em formato acionavel, e priorizacao para focar o time nos insights de maior impacto. O output
e um conjunto priorizado de insights que conecta evidencia de usuario a oportunidades de design.

## When to Use

- Apos rodadas de entrevistas com usuarios (5+ sessoes)
- Ao consolidar dados de multiplas fontes (quali + quanti)
- Quando o time tem muitas observacoes mas nao sabe por onde comecar
- Para transformar dados de usability testing em recomendacoes
- Ao final de sprints de discovery para sintetizar aprendizados
- Para alinhar o squad sobre o que a pesquisa realmente revelou

## How to Apply

### Step 1 — Preparar Dados Brutos
1. Reuna todos os dados: notas de entrevista, clips de video, citacoes, metricas, observacoes
2. Escreva cada observacao individual em um "note" atomico (1 fato por nota)
3. Inclua contexto: participante (anonimo), fonte, momento da sessao
4. Nao interprete ainda — mantenha notas descritivas e fatuais
5. Volume esperado: 100-300 notes para 6-8 entrevistas de 45 min

### Step 2 — Affinity Mapping
1. Coloque todas as notes em um espaco visual (Miro, FigJam, parede)
2. Comece agrupando notes que parecem relacionadas — sem categorias pre-definidas
3. Trabalhe em silencio por 15-20 min (evita groupthink)
4. Grupos naturais emergirem com 3-8 notes cada
5. Rotule cada grupo com frase descritiva (nao palavra solta)
6. Identifique super-clusters: grupos de grupos que formam temas maiores
7. Notes que nao encaixam em nenhum grupo ficam separadas — podem ser outliers valiosos

### Step 3 — Thematic Analysis
1. Revise os clusters do affinity mapping e identifique temas transversais
2. Para cada tema, responda: "O que os dados estao dizendo sobre [tema]?"
3. Quantifique: em quantos participantes/fontes este tema apareceu?
4. Diferencie temas de alta recorrencia (patterns) vs. baixa recorrencia (signals)
5. Identifique contradicoes: temas onde dados de fontes diferentes divergem
6. Documente cada tema com: nome, descricao, evidencias (3+ notas), frequencia

### Step 4 — Construir Insight Statements
Para cada tema relevante, escreva um insight statement no formato:

**"[Perfil de usuario] [comportamento/necessidade observada] porque [motivacao/causa raiz],
o que significa que [implicacao para design]."**

Criterios de um bom insight:
- Baseado em evidencia (nao opiniao)
- Revela algo nao obvio (nao "usuarios querem que funcione")
- Acionavel (sugere direcao de solucao sem prescrever a solucao)
- Especifico (sobre um perfil e contexto, nao generico)

### Step 5 — Priorizar Insights
Use matriz 2x2 para priorizar:

| | Alto Impacto no Usuario | Baixo Impacto no Usuario |
|---|---|---|
| **Alta Frequencia** | P1 — Acao imediata | P3 — Monitorar |
| **Baixa Frequencia** | P2 — Investigar mais | P4 — Arquivar |

Para cada insight P1 e P2:
1. Defina como o insight se traduz em oportunidade de design
2. Estime esforco de enderecar (T-shirt sizing: S/M/L/XL)
3. Identifique dependencias e riscos
4. Conecte ao roadmap existente

### Step 6 — Documentar e Comunicar
1. Crie um research report com: contexto, metodo, insights priorizados, recomendacoes
2. Inclua citacoes representativas para cada insight (humaniza os dados)
3. Prepare apresentacao de 15 min: problema > metodo > top 3 insights > proximos passos
4. Compartilhe raw data acessivel para quem quiser aprofundar
5. Armazene no research repository para consulta futura

## Examples

### Exemplo 1 — Sintese de Discovery de Onboarding
8 entrevistas + dados de analytics de funil. Affinity mapping gerou 180 notes em 14 clusters.
3 temas principais: "medo de configurar errado" (6/8 participantes), "valor nao percebido ate
dia 3" (5/8), "tutorial ignorado sistematicamente" (7/8). Insight P1: "Novos usuarios pulam
o tutorial porque parece generico, mas travam no primeiro uso real porque nao entendem o modelo
mental do produto — onboarding precisa ser contextual e Just-in-Time, nao front-loaded."

### Exemplo 2 — Consolidacao Multi-fonte (SaaS)
Fontes: 6 entrevistas + 200 tickets de suporte + dados de NPS. Thematic analysis revelou que
85% dos detratores de NPS mencionavam o mesmo tema das entrevistas: "incerteza sobre o estado
de processos assincronos". Insight cruzado validou prioridade P1 e justificou investimento em
sistema de status e notificacoes contextuais.

## Common Pitfalls

- **Sintese individual**: Fazer sozinho amplifica bias — envolva pelo menos 2 pessoas na sessao
- **Pular affinity mapping**: Ir direto para conclusoes sem agrupar dados gera cherry-picking
- **Insights vagos**: "Usuarios querem uma experiencia melhor" nao e insight — seja especifico
- **Confirmar hipoteses**: Sintese deve descobrir o que os dados dizem, nao confirmar o que voce acha
- **Ignorar contradicoes**: Dados contraditorios frequentemente revelam segmentos diferentes
- **Sintese sem acao**: Insights bonitos que nao geram decisoes sao desperdicio de research

## Cross-References

- [UX Design Expert](../agents/ux-design-expert.md) — Agente especialista em research e sintese
- [Synthesis Quality Checklist](../checklists/synthesis-quality.md) — Checklist de qualidade da sintese
- [Insights and Opportunities Template](../templates/research/insights-and-opportunities-template.md) — Template de documentacao
- [interview-framework.md](interview-framework.md) — Dados de entrevista como input principal
- [card-sort-framework.md](card-sort-framework.md) — Dados de card sort como input
- [usability-testing-framework.md](usability-testing-framework.md) — Dados de testes como input
- [hypothesis-driven-design.md](hypothesis-driven-design.md) — Insights geram novas hipoteses
- [discovery-layer.md](discovery-layer.md) — Sintese como etapa final do discovery
