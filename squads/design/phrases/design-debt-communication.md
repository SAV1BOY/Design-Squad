# Design Debt Communication

## Context

Frases prontas para identificar, documentar e comunicar design debt — inconsistências,
workarounds, e decisões subótimas acumuladas ao longo do tempo que degradam a qualidade
da experiência. Design debt é análogo a tech debt: invisível para stakeholders mas
cumulativo no impacto.

**Aplicação:** Backlog grooming, sprint planning, reports, propostas de refatoração
**Tom:** System Thinker + Pragmatic Builder

## Phrases

### Identificando design debt
- "Temos [N] variações do mesmo componente [nome] em [N] squads. Deveria ser 1 no design system."
- "O fluxo de [feature] foi construído em [N] sprints diferentes sem revisão holística — há [N] inconsistências."
- "A spacing scale original de [valor] não está sendo seguida: [N]% dos componentes usam valores custom."
- "Esse pattern foi uma solução temporária do sprint [data]. Permaneceu em produção por [N] meses."
- "O audit de consistência revelou [N] problemas em [categorias]: cor ([N]), spacing ([N]), tipografia ([N])."

### Quantificando impacto
- "Cada inconsistência visual gera em média [N] horas de retrabalho por quarter."
- "O design debt acumulado adiciona [N] story points de overhead a cada nova feature."
- "A falta de componente padronizado para [nome] causou [N] bugs visuais no último quarter."
- "Desenvolvedores gastam estimados [N] horas/sprint reconciliando diferenças entre specs e design system."
- "O tempo de onboarding de novos devs inclui [N] horas extras para entender inconsistências não documentadas."

### Propondo plano de payoff
- "Proponho alocar [N]% da capacidade de cada sprint para design debt. Isso dá [N] pontos por sprint."
- "O plano de payoff em 3 fases: (1) Audit completo, (2) Priorização por impacto, (3) Execução sprint-a-sprint."
- "Quick wins (< 2 pontos cada): [lista]. Podem ser feitos em [N] sprints sem afetar features."
- "O maior item de debt é [componente/fluxo]. Resolver custa [N] pontos mas elimina [M] inconsistências."
- "Proponho 1 sprint de 'design debt payoff' por quarter. O ROI estimado é [redução de retrabalho]."

### Classificando severidade
- "Classifico o design debt em 3 níveis: Crítico (afeta UX/a11y), Moderado (inconsistência visual), Baixo (polish)."
- "Items críticos: [lista]. Estes afetam diretamente a experiência do usuário ou acessibilidade."
- "Items moderados: [lista]. Inconsistências visíveis mas sem impacto funcional."
- "Items de polish: [lista]. Refinamentos que melhoram a percepção de qualidade."

### Prevenindo novo debt
- "Para evitar acumular mais debt, proponho: design review obrigatória antes de merge."
- "Todo componente custom precisa de ticket de 'upstream para DS' criado no momento da implementação."
- "A checklist de handoff agora inclui: 'Este design usa apenas componentes do DS? Se não, justificar.'"
- "Marcar soluções temporárias com tag [DESIGN-DEBT] no Figma e no ticket para rastreamento."

### Reportando progresso
- "Design debt reduction: [N] items resolvidos neste sprint, [M] restantes."
- "O score de consistência subiu de [X] para [Y] após a resolução de [N] items de debt."
- "Tempo médio de implementação de novas features caiu [X]% após cleanup do sprint passado."

## Variations

- Para stakeholders: focar em custo ($) e velocidade de entrega
- Para engenharia: focar em componentes afetados e esforço de migração
- Para designers: focar em inconsistências visuais e padrões corretos
- Para reports trimestrais: métricas de debt acumulado vs. resolvido

## When to Use

- Backlog grooming para incluir items de design debt
- Sprint planning para negociar alocação de capacidade
- Reports trimestrais de saúde do design system
- Propostas de refatoração visual para stakeholders
- Retrospectivas para discutir causas e prevenção
