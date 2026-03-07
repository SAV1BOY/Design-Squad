# Phase: Accessibility Audit Scope

## Objective

Definir escopo, metodos e ferramentas para uma auditoria abrangente de acessibilidade do produto contra WCAG 2.2 AA.

## Inputs

- Mapa completo do produto (paginas e fluxos)
- WCAG 2.2 AA success criteria
- Ferramentas de teste (axe-core, Lighthouse, screen readers)
- Dados de usuarios com deficiencia (se disponivel)
- Requisitos legais aplicaveis (ADA, LBI, EAA)

## Activities

### 1. Scope Definition
Priorizar areas por volume de uso e risco legal. Definir quais paginas e fluxos serao auditados. Para auditoria completa: todas as paginas. Para auditoria focada: top 20 paginas por volume + fluxos criticos (signup, purchase, settings).

### 2. Method Selection
Definir mix de metodos: automated scanning (axe-core em 100% das paginas), keyboard navigation test (100% dos fluxos), screen reader test (fluxos principais com VoiceOver + NVDA), contrast audit (todas as combinacoes de cor), manual WCAG checklist (amostra de paginas).

### 3. Tool Setup
Configurar axe-core no CI pipeline. Instalar extensoes de browser (axe DevTools, WAVE, Stark). Preparar screen readers para teste. Criar templates de report para cada metodo.

### 4. Team Allocation
Designar responsaveis por cada metodo. Treinar time em uso de ferramentas (se necessario). Definir timeline de execucao (2-4 semanas para audit).

## Output

- Documento de escopo aprovado
- Metodos e ferramentas configurados
- Timeline de auditoria
- Team alocado e treinado
- Templates de report preparados

## Next Phase

→ `01-findings.md` — Audit Findings
