# Design Audit Framework

## Metadata

- **Autor**: Design Squad
- **Categoria**: Quality Assurance, Avaliacao, Diagnostico
- **Complexidade**: Alta
- **Aplicacao**: Auditar produtos digitais existentes gerando diagnostico com severidade
- **Ultima atualizacao**: 2026-03-18
- **Tags**: heuristic-evaluation, visual-audit, design-system-consistency, a11y, severity

## Concept

O Design Audit Framework combina quatro lentes de avaliacao — heuristic evaluation, audit
visual, design system consistency e acessibilidade — para gerar um diagnostico abrangente de
um produto digital existente. Cada finding recebe classificacao de severidade, permitindo
priorizacao objetiva de melhorias.

Diferente de uma avaliacao informal ("acho que esta tela esta confusa"), o audit segue criterios
pre-definidos, documenta evidencia concreta e produz um plano de acao priorizavel. O resultado
e um report estruturado que comunica problemas e oportunidades para stakeholders tecnicos e
nao-tecnicos.

## When to Use

- Ao assumir um produto legado que precisa de modernizacao
- Antes de um redesign para mapear o estado atual com rigor
- Quando metricas de UX indicam problemas mas nao se sabe onde
- Para avaliar consistencia apos multiplos squads trabalharem no mesmo produto
- Como health check periodico (recomendado: trimestral)
- Para justificar investimento em design debt com dados concretos

## How to Apply

### Step 1 — Definir Escopo e Criterios
1. Delimite quais telas, fluxos ou features serao auditados
2. Selecione lentes de avaliacao (pode usar todas ou subset):
   - **Heuristic Evaluation**: Nielsen's 10 heuristics como framework base
   - **Visual Audit**: Consistencia visual, hierarquia, grid, tipografia, spacing
   - **DS Consistency**: Aderencia ao design system (tokens, componentes, patterns)
   - **Accessibility (a11y)**: WCAG 2.1 AA como baseline
3. Defina escala de severidade:
   - **Critico (S1)**: Impede usuario de completar tarefa ou viola requisito legal
   - **Major (S2)**: Causa frustracao significativa ou inconsistencia grave
   - **Minor (S3)**: Causa confusao breve, usuario se recupera sozinho
   - **Enhancement (S4)**: Oportunidade de melhoria, nao problema atual

### Step 2 — Heuristic Evaluation
Para cada tela/fluxo, avalie contra as 10 heuristicas de Nielsen:
1. Visibilidade do status do sistema
2. Correspondencia entre sistema e mundo real
3. Controle e liberdade do usuario
4. Consistencia e padroes
5. Prevencao de erros
6. Reconhecimento em vez de recordacao
7. Flexibilidade e eficiencia de uso
8. Design estetico e minimalista
9. Ajuda ao usuario para reconhecer e recuperar de erros
10. Ajuda e documentacao

Para cada violacao: descreva o problema, aponte a tela, atribua severidade, sugira correcao.

### Step 3 — Visual Audit
1. Capture todas as variacoes de tipografia usadas (fontes, tamanhos, pesos)
2. Documente todas as cores usadas e compare com o sistema definido
3. Verifique consistencia de spacing, grid e alinhamentos
4. Avalie hierarquia visual: o que chama atencao primeiro esta correto?
5. Identifique inconsistencias entre telas semelhantes
6. Registre cada desvio como finding com screenshot

### Step 4 — Design System Consistency Check
1. Para cada componente na tela, verifique se existe equivalente no DS
2. Identifique componentes "off-system" (custom ou desatualizados)
3. Verifique uso correto de design tokens (cores, spacing, typography)
4. Documente porcentagem de aderencia por tela: componentes DS / total
5. Classifique desvios: intencional (justificado) vs. acidental (debt)

### Step 5 — Accessibility Audit
1. Teste contraste de cores (WCAG AA: 4.5:1 texto, 3:1 elementos graficos)
2. Verifique navegacao por teclado em todos os fluxos
3. Teste com screen reader (VoiceOver / NVDA)
4. Verifique labels, roles e estados de componentes interativos
5. Teste comportamento com zoom ate 200%
6. Documente cada violacao com criterio WCAG especifico

### Step 6 — Consolidar Diagnostico
1. Compile todos os findings em tabela unica com: ID, lente, descricao, tela, severidade
2. Calcule distribuicao por severidade e por lente
3. Identifique padroes: problemas sistemicos vs. pontuais
4. Priorize por: severidade x frequencia x esforco de correcao
5. Gere recomendacoes acionaveis com estimativa de esforco

## Examples

### Exemplo 1 — Audit de Produto Legado (E-commerce)
Escopo: 12 telas do fluxo principal. Resultado: 47 findings (8 criticos, 15 major,
18 minor, 6 enhancements). Padrao sistemico: 60% dos criticos eram de a11y (contraste
insuficiente em CTAs). DS consistency: apenas 45% dos componentes seguiam o design system.
Recomendacao: sprint dedicado a a11y + migration plan para componentes off-system.

### Exemplo 2 — Health Check Trimestral (SaaS)
Audit focado em 3 features lancadas no trimestre. Resultado: DS consistency subiu de 72%
para 85% vs. trimestre anterior. 2 findings criticos de heuristicas: mensagens de erro
genericas ("Algo deu errado") sem orientacao de recuperacao. Quick win implementado em 1 sprint.

## Common Pitfalls

- **Audit sem criterio**: Sem framework definido, o audit vira lista de opinioes pessoais
- **Tudo e critico**: Inflar severidade destrói credibilidade — seja rigoroso na classificacao
- **Audit gigante sem acao**: Melhor auditar 5 telas e agir do que 50 telas e engavetar
- **Ignorar contexto**: Um desvio do DS pode ser intencional — investigue antes de classificar
- **Auditor unico**: Idealmente 2-3 avaliadores independentes para reduzir bias individual
- **Nao re-auditar**: Sem follow-up, o audit nao fecha o loop de melhoria

## Cross-References

- [nielsen-heuristics.md](nielsen-heuristics.md) — Base da lente de heuristic evaluation
- [design-system-governance.md](design-system-governance.md) — Criterios de aderencia ao DS
- [design-token-architecture.md](design-token-architecture.md) — Tokens como referencia para visual audit
- [accessibility-wcag-aa.md](accessibility-wcag-aa.md) — Criterios WCAG para lente de a11y
- [design-debt-management.md](design-debt-management.md) — Findings alimentam o backlog de debt
- [UX Audit Report Template](../templates/reports/ux-audit-report-template.md) — Template para documentar resultados
- [A11y Audit Report Template](../templates/reports/a11y-audit-report-template.md) — Template especifico para a11y
- [Design System Review Task](../tasks/review/design-system-review.md) — Task relacionada
