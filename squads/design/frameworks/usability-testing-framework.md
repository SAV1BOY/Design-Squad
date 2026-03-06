# Usability Testing Framework

## Metadata
- **Autor**: Design Squad
- **Categoria**: Research, Validacao, Teste de Usabilidade
- **Complexidade**: Media
- **Aplicacao**: Planejar e executar testes de usabilidade com tarefas, metricas e criterios
- **Ultima atualizacao**: 2026-03-06

## Concept

O Usability Testing Framework sistematiza o processo de testar designs com usuarios reais,
definindo tarefas concretas, metricas de sucesso, criterios de avaliacao e processo de
captura de aprendizados. O objetivo e transformar teste de usabilidade de evento ad-hoc
em pratica recorrente e padronizada.

A premissa e que usabilidade nao e opiniao — e mensuravel. Task success rate, time on task,
error rate e satisfaction score sao metricas objetivas que permitem comparar versoes de
design e rastrear evolucao ao longo do tempo.

O framework cobre desde planejamento (o que testar e com quem) ate sintese (o que aprendemos
e o que mudamos).

## When to Use

- Antes de lancar features novas ou redesigns significativos
- Quando metricas de produto indicam problemas de usabilidade
- Quando ha desacordo interno sobre qual abordagem de design funciona melhor
- Quando se quer validar prototipos antes de investir em implementacao
- Quando se precisa de evidencia para justificar decisoes de design
- Como pratica regular a cada sprint ou ciclo de design

## How to Apply

### Fase 1 — Planejamento
1. **Defina objetivos**: O que voce quer aprender com este teste?
   - "Validar se usuarios conseguem completar o checkout em < 3 min"
   - "Identificar pontos de confusao no novo onboarding"
2. **Defina tarefas** (3-5 por sessao):
   - Tarefas realistas baseadas em cenarios de uso real
   - Comece com tarefa simples para aquecer, termine com complexa
   - Formato: "Voce precisa [objetivo]. Use o produto para [acao]"
3. **Defina metricas por tarefa**:
   - Task success: completou, completou com dificuldade, nao completou
   - Time on task: segundos para completar
   - Errors: numero de erros ou desvios do caminho
   - Satisfaction: escala 1-5 apos cada tarefa
4. **Defina criterios de sucesso**:
   - "80% dos usuarios completam a tarefa sem ajuda"
   - "Tempo medio < 120 segundos"
   - "Satisfacao media > 4/5"
5. **Recrute participantes**: 5 usuarios por rodada (minimo)
   - Representativos do publico-alvo real
   - Mix de experiencia (novatos e experientes)
   - Sem envolvimento no design ou desenvolvimento

### Fase 2 — Preparacao
1. Prepare o prototipo ou ambiente de teste
2. Escreva guia de moderacao com:
   - Introducao padrao (explicar que esta testando o produto, nao a pessoa)
   - Instrucoes de cada tarefa (exatamente como serao lidas)
   - Probes para quando usuario trava: "O que voce esta procurando?"
   - Perguntas pos-tarefa e pos-sessao
3. Configure gravacao (tela + audio + camera se possivel)
4. Prepare planilha de captura de dados em tempo real
5. Faca piloto com 1 colega para validar o setup

### Fase 3 — Execucao
1. Abertura (5 min): Rapport, consentimento, explicacao do formato
2. Tarefas (30-40 min): Apresente uma tarefa por vez
   - Nao ajude — observe e capture
   - Use probes neutros: "O que voce faria agora?"
   - Incentive think-aloud: "Me conta o que esta pensando"
   - Cronometre cada tarefa
3. Debrief (10 min): Perguntas abertas pos-sessao
   - "O que foi mais dificil?"
   - "O que voce mudaria?"
   - "Qual sua impressao geral?"
4. Capture notas durante a sessao (note-taker dedicado)

### Fase 4 — Analise e Sintese
1. Compile dados quantitativos por tarefa em tabela
2. Identifique padroes qualitativos: o que causou dificuldade e por que
3. Classifique findings por severidade:
   - Critico: Impede conclusao da tarefa
   - Major: Causa frustacao significativa ou desvio longo
   - Minor: Causa confusao breve mas usuario se recupera
   - Enhancement: Oportunidade de melhoria, nao problema
4. Priorize por severidade x frequencia
5. Documente recommendations com racional

### Fase 5 — Learnings e Acao
1. Apresente resultados para a equipe (sessao de 30 min)
2. Priorize fixes conforme severidade e esforco
3. Incorpore fixes no backlog do sprint
4. Defina data para re-teste apos implementacao dos fixes
5. Adicione learnings ao knowledge base da equipe

## Key Principles

- **5 usuarios revelam 85% dos problemas**: Nao precisa de 50 participantes
- **Observar > perguntar**: O que usuarios fazem importa mais que o que dizem
- **Tarefas realistas**: Cenarios artificiais geram insights artificiais
- **Criterios pre-definidos**: Defina sucesso antes de testar, nao depois
- **Severidade objetiva**: Classifique por impacto, nao por preferencia
- **Think-aloud e ouro**: O que o usuario pensa enquanto navega revela o modelo mental
- **Teste frequente**: Testes pequenos e frequentes > testes grandes e raros

## Examples

### Exemplo 1 — Teste de Checkout (5 usuarios)
| Tarefa              | Success | Time (avg) | Errors (avg) | Satisfaction |
|---------------------|---------|------------|--------------|--------------|
| Adicionar ao cart   | 5/5     | 12s        | 0            | 4.8/5        |
| Aplicar cupom       | 3/5     | 45s        | 1.4          | 3.2/5        |
| Finalizar compra    | 4/5     | 138s       | 0.8          | 3.6/5        |

Finding critico: Campo de cupom nao visivel — 2 usuarios nao encontraram.
Finding major: Formulario de endereco exige formato especifico sem indicar qual.

### Exemplo 2 — Teste Nao Moderado em Escala
Usando Maze, 30 usuarios testaram novo dashboard:
- Mission 1 (encontrar metrica): 87% direct success, 8s median time
- Mission 2 (filtrar por periodo): 63% direct success, 22s median time
- Mission 3 (exportar relatorio): 43% direct success, 35s median time
Heatmap de cliques revelou que 40% dos usuarios clicavam no grafico
esperando drill-down que nao existia.

### Exemplo 3 — Cadencia de Teste
Uma equipe instituiu "Test Tuesdays": toda terca, 1-2 testes de usabilidade.
Em 6 meses: 48 sessoes, 240 insights, 67 fixes implementados.
SUS do produto subiu de 58 para 74 no periodo.

## Common Pitfalls

- **Leading questions**: "Voce achou facil o checkout?" induz resposta. Use neutro
- **Ajudar o usuario**: Intervir quando o usuario trava invalida o dado
- **Amostra de conveniencia**: Testar com colegas ou pessoas tech-savvy enviesou
- **Muitas tarefas**: 3-5 tarefas por sessao. Mais que isso e exaustivo
- **Findings sem acao**: Teste que gera relatorio lindo e nenhuma mudanca e desperdicio
- **Testar muito tarde**: Testar depois de implementar elimina o beneficio de custo
- **Nao re-testar**: Sem re-teste, nao ha evidencia de que o fix funcionou

## Cross-References

- [discovery-layer.md](discovery-layer.md) — Testes como parte de discovery
- [prototyping-layer.md](prototyping-layer.md) — Prototipos como objeto de teste
- [measurement-layer.md](measurement-layer.md) — Metricas de usabilidade
- [malouf-research-to-decision.md](malouf-research-to-decision.md) — Findings como evidencia
- [malouf-design-quality-model.md](malouf-design-quality-model.md) — Usabilidade como dimensao
- [accessibility-by-default.md](accessibility-by-default.md) — Teste de a11y com usuarios
