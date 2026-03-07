# Phase: Audit Findings

## Objective

Executar a auditoria e documentar todos os findings de acessibilidade com evidencia, classificacao e localizacao precisa.

## Inputs

- Escopo e metodos definidos (00-audit-scope.md)
- Ferramentas configuradas
- Acesso ao produto (staging + producao)

## Activities

### 1. Automated Scanning
Rodar axe-core em todas as paginas do escopo. Exportar resultados em formato padronizado. Categorizar por WCAG criterion e severidade. Eliminar falsos positivos com review manual.

### 2. Keyboard Testing
Navegar cada fluxo usando apenas teclado. Verificar: tab order logico, focus visivel, sem keyboard traps, todos os controles acessiveis, skip links funcionais. Documentar cada failure com screenshot.

### 3. Screen Reader Testing
Testar fluxos principais com VoiceOver (Mac) e NVDA (Windows). Verificar: anuncios corretos, landmarks presentes, form labels claros, dynamic content announced, headings hierarchy. Gravar sessoes para evidencia.

### 4. Contrast & Visual Audit
Verificar todas as combinacoes de cor contra WCAG AA. Testar com simuladores de daltonismo. Verificar que informacao nao depende apenas de cor. Testar zoom ate 400% sem perda de funcionalidade.

### 5. Consolidation
Consolidar findings de todos os metodos. Eliminar duplicatas. Classificar por WCAG criterion, principio, severidade e componente. Criar database de issues (accessibility-issues-registry.yaml).

## Output

- Lista completa de issues com evidencia
- Issues classificados por severidade e principio WCAG
- Compliance score geral e por area
- Database de issues no registry
- Recomendacao de correcao por issue

## Next Phase

→ `02-prioritization.md` — Priorizacao de Fixes
