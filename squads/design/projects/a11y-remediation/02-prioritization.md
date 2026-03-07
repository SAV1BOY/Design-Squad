# Phase: Prioritization

## Objective

Priorizar issues de acessibilidade para remediacao, equilibrando impacto nos usuarios, risco legal e esforco de implementacao.

## Inputs

- Lista completa de findings (01-findings.md)
- Estimativas de esforco do Engineering
- Risk assessment legal
- User impact data (analytics + personas)

## Activities

### 1. Impact Assessment
Para cada issue avaliar: quantos usuarios sao afetados (por tipo de deficiencia), severidade do impacto (bloqueia, dificulta, incomoda), frequencia de encontro (pagina de alto vs baixo trafego), risco legal (regulacao aplicavel).

### 2. Effort Estimation
Workshop com Engineering: categorizar cada fix como small (< 4h), medium (4-16h) ou large (16h+). Identificar dependencias entre fixes. Mapear fixes que resolvem multiplos issues de uma vez (fix no DS component = fix em todas as instancias).

### 3. Priority Ranking
Aplicar formula: Priority = (User Impact x Legal Risk) / Effort. Classificar em tiers: Tier 1 (sprint atual): critical + high impact quick wins, Tier 2 (proximo sprint): high impact medium effort, Tier 3 (backlog): medium/low impact ou high effort.

### 4. Remediation Plan
Criar plano detalhado com: issues por sprint, responsaveis, acceptance criteria, verificacao method. Estimar data de compliance AA.

## Output

- Priority ranking de todos os issues
- Remediation plan com sprints e responsaveis
- Estimativa de timeline para compliance AA
- Jira tickets criados e priorizados
- Stakeholder communication

## Next Phase

→ `03-remediation.md` — Remediacao
