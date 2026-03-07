# Phase: Heuristic Evaluation

## Objective

Conduzir avaliacao heuristica sistematica de cada area do produto, identificando violacoes de usabilidade e acessibilidade.

## Inputs

- Escopo e criterios definidos (00-scope.md)
- Acesso ao produto (ambientes de staging/producao)
- Templates de avaliacao
- Heuristicas de Nielsen e WCAG checklist

## Activities

### 1. Independent Evaluation
Cada avaliador (minimo 3) percorre todas as telas e fluxos no escopo independentemente. Para cada issue encontrado: descrever o problema, identificar a heuristica violada, classificar severidade (0-4), tirar screenshot e sugerir correcao.

### 2. Accessibility Scan
Rodar axe-core em cada pagina do escopo. Testar navegacao por teclado em cada fluxo. Verificar contraste de cor com ferramenta automatizada. Testar com screen reader (VoiceOver ou NVDA) nos fluxos principais.

### 3. Analytics Review
Analisar metricas quantitativas por area: bounce rate, exit rate, time-on-task, error rate, funnel drop-offs. Correlacionar dados quantitativos com findings heuristicos.

### 4. Consolidation
Reunir avaliadores para consolidar findings. Eliminar duplicatas, alinhar severidades, agrupar por tema. Criar lista unificada de issues com consensus de severidade.

## Output

- Lista consolidada de issues com severidade
- Screenshots e descricoes de cada issue
- Dados quantitativos correlacionados
- Accessibility scan results
- Heatmaps e recordings (se disponivel)

## Next Phase

→ `02-findings.md` — Findings Report
