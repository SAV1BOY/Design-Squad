# QA Review Framework

## Metadata

- **Autor**: Design Squad
- **Categoria**: Quality Assurance, Handoff, Design-Dev Collaboration
- **Complexidade**: Media
- **Aplicacao**: Comparar specs de design com implementacao e reportar discrepancias de forma estruturada
- **Ultima atualizacao**: 2026-03-18
- **Tags**: qa, visual-qa, pixel-comparison, behavior-testing, bug-report, severity, handoff

## Concept

O QA Review Framework estrutura o processo de verificacao visual e funcional entre o que foi
especificado no design e o que foi implementado no codigo. QA de design nao e "achar defeito" —
e garantir que a experiencia entregue ao usuario corresponde a intencao do design. Sem QA
estruturado, discrepancias se acumulam ate que o produto diverge significativamente das specs.

O framework cobre dois tipos de verificacao: pixel comparison (espacamento, cores, tipografia,
alinhamento, responsividade) e behavior testing (estados, transicoes, interacoes, edge cases).
Para cada discrepancia encontrada, define severity levels e workflow de resolucao que evita
ping-pong improdutivo entre design e dev.

## When to Use

- Apos implementacao de novas features ou componentes de UI
- Em sprints de refinamento visual antes de releases
- Quando usuarios reportam inconsistencias visuais
- Ao migrar para nova versao do design system
- Para auditar qualidade visual de telas criticas (onboarding, checkout, core flows)
- Como gate de qualidade antes de cada release

## How to Apply

### Step 1 — Preparar Review Environment
1. Abra as specs de design (Figma) e a implementacao (staging/preview) lado a lado
2. Use mesmo device ou resolucao que o design especifica (breakpoints principais)
3. Configure dados realistas na implementacao — evite "Lorem ipsum" ou dados perfeitos
4. Verifique em multiplos breakpoints: mobile (375px), tablet (768px), desktop (1440px)
5. Prepare ferramentas: browser DevTools, extensao de pixel overlay (PerfectPixel), Figma inspect
6. Tenha o design token spec acessivel para verificar valores exatos

### Step 2 — Pixel Comparison (Visual Review)
1. **Tipografia**: Fonte, tamanho, peso, line-height, letter-spacing, cor de texto
2. **Cores**: Background, bordas, shadows — compare hex/rgb exatos com tokens do DS
3. **Espacamento**: Padding, margin, gap — use DevTools para medir valores reais
4. **Alinhamento**: Elementos alinhados conforme grid? Centralizacao correta?
5. **Icones e imagens**: Tamanho correto, aspect ratio mantido, qualidade de renderizacao
6. **Responsividade**: Layout adapta corretamente em cada breakpoint especificado?
7. **Dark mode**: Se aplicavel, todos os tokens de cor invertendo corretamente?
8. Use overlay de screenshot do Figma sobre implementacao para detectar desvios sutis

### Step 3 — Behavior Testing (Functional Review)
1. **Estados de componentes**: Default, hover, focus, active, disabled, loading, error
2. **Transicoes e animacoes**: Duracao, easing, propriedades animadas conforme spec
3. **Interacoes**: Click, tap, drag, swipe, keyboard navigation funcionando como especificado
4. **Edge cases de conteudo**: Texto longo (truncation), texto curto, campos vazios, listas longas
5. **Empty states**: Tela sem dados mostra estado vazio conforme design?
6. **Error states**: Mensagens de erro aparecem no local e formato corretos?
7. **Loading states**: Skeletons, spinners, progress bars conforme spec?
8. **Acessibilidade basica**: Tab order logico, focus visible, labels de screen reader

### Step 4 — Classificar Bugs por Severity
Cada discrepancia encontrada recebe uma severity level:

| Severity | Descricao | Exemplos | SLA de Correcao |
|---|---|---|---|
| **Critical** | Bloqueia uso ou causa perda de dados | Botao de submit invisivel, form nao envia, crash visual | Antes do release |
| **Major** | Afeta funcionalidade ou experiencia significativamente | Estado de erro nao aparece, layout quebrado em mobile, contraste inacessivel | Sprint atual |
| **Minor** | Perceptivel mas nao impede uso | Espacamento 4px off, cor levemente diferente, transicao ausente | Proximo sprint |
| **Cosmetic** | Detalhe estetico sem impacto funcional | Border-radius 1px off, shadow sutil diferente, font-weight em 1 label | Backlog |

### Step 5 — Reportar Bugs de Forma Estruturada
Para cada bug, documente:
1. **Titulo**: Descricao concisa do problema (ex.: "Button spacing 8px em vez de 12px no checkout mobile")
2. **Severity**: Critical / Major / Minor / Cosmetic
3. **Screenshot**: Lado a lado — design spec vs. implementacao real
4. **Localizacao**: Tela, componente, breakpoint, estado
5. **Esperado**: O que o design spec define (inclua link para frame no Figma)
6. **Atual**: O que a implementacao mostra (inclua URL do staging)
7. **Detalhes tecnicos**: Token esperado, valor CSS encontrado, DevTools evidence
8. Agrupe bugs por tela ou componente para facilitar resolucao em batch

### Step 6 — Workflow de Resolucao
1. Designer abre issues de QA no board do sprint com severity e evidencia
2. Dev e designer fazem triage conjunta: confirmar, reclassificar ou marcar "by design"
3. Bugs critical e major sao resolvidos no sprint atual — sem negociacao
4. Bugs minor sao planejados para proximo sprint
5. Bugs cosmetic vao para backlog e sao resolvidos em sprints de polimento
6. Apos correcao, designer faz re-review e fecha a issue
7. Se a mesma discrepancia aparece repetidamente, eleve para o DS team como melhoria de specs

### Step 7 — Melhorar o Processo Continuamente
1. Track metricas: bugs por sprint, distribuicao por severity, tempo de resolucao
2. Bugs recorrentes indicam falha de handoff — melhore specs, tokens ou documentacao
3. Realize QA review checkpoint no meio do desenvolvimento (nao so no final)
4. Automatize o que for possivel: visual regression tests (Chromatic, Percy, BackstopJS)
5. Mantenha checklist vivo: adicione itens novos conforme padroes de bugs emergem

## Examples

### Exemplo 1 — QA de Feature de Checkout
Review de 5 telas de checkout em 3 breakpoints. Encontrados: 2 major (form de pagamento
sem error state visivel, botao CTA cortado em mobile), 4 minor (espacamento inconsistente
entre campos, cor de placeholder diferente do token), 3 cosmetic (shadow sutil ausente,
border-radius 2px off). Major corrigidos na sprint. Minor planejados para sprint seguinte.
Bug de error state revelou que o spec nao cobria o cenario — spec atualizado para futuros handoffs.

### Exemplo 2 — Auditoria Visual Pos-DS Migration
Apos migrar de DS v2 para v3, QA review de 12 telas core. 67 discrepancias encontradas.
Analise revelou que 80% eram do mesmo tipo: tokens de spacing antigos nao mapeados. Criado
codemod para corrigir em batch. Restantes 13 bugs eram edge cases de componentes com props
novas. Resolvidos em 2 sprints. Post-mortem gerou melhoria no migration guide do DS.

## Common Pitfalls

- **QA so no final**: Revisar apenas antes do release gera backlog enorme — faca checkpoints intermediarios
- **Sem screenshots comparativos**: "Esta diferente" sem evidencia visual gera debate improdutivo
- **Tudo e critical**: Inflar severity desgasta a relacao design-dev e dilui urgencia real
- **Ignorar edge cases**: Testar so o happy path com dados perfeitos esconde 50% dos problemas
- **Designer vs. Dev**: QA nao e adversarial — e colaborativo. Triage conjunta evita ressentimento
- **Nao automatizar**: Visual regression tests capturam regressoes que review manual nao escala

## Cross-References

- [Jessica UX/UI](../agents/jessica-ux-ui.md) — Agente especialista em UI e qualidade visual
- [Design Chief](../agents/design-chief.md) — Stakeholder para priorizacao de bugs visuais
- [Handoff Quality Checklist](../checklists/handoff-quality.md) — Checklist de qualidade do handoff design-dev
- [QA Bug Template](../templates/handoff/qa-bug-template.md) — Template para reportar bugs visuais
- [design-to-code-handoff.md](design-to-code-handoff.md) — Framework de handoff que precede o QA
- [design-token-architecture.md](design-token-architecture.md) — Tokens como fonte de verdade para comparacao
- [component-spec-framework.md](component-spec-framework.md) — Specs de componente como base para QA
- [design-review-and-critique.md](design-review-and-critique.md) — Review de design complementa QA de implementacao
