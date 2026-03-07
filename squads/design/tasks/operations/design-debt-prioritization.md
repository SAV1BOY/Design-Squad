# Design Debt Prioritization

## Metadata
- **Categoria:** Operations
- **Complexidade:** Média
- **Tempo Estimado:** 1-2 dias por sessão
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** operations, design-debt, prioritization, quality, technical-debt

## Objective
Identificar, catalogar e priorizar itens de design debt do produto para garantir que
inconsistências visuais, problemas de usabilidade e desvios do design system são endereçados
de forma estratégica, sem bloquear entregas de features novas.

## Prerequisites
- Design audit ou reviews anteriores com findings pendentes
- Inventário de issues conhecidos de design (tickets, feedback)
- Métricas de impacto dos issues (analytics, suporte)
- Acesso ao backlog de produto para integração
- Critérios de priorização alinhados com PM

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design Lead | Facilitar priorização e negociar alocação com PM |
| Design Ops | Manter inventário de debt e métricas associadas |
| UI/UX Designer | Avaliar severidade e estimar esforço de cada item |
| Product Manager | Alinhar prioridade de debt vs features novas |
| Tech Lead | Avaliar dependências técnicas e esforço de implementação |

## Frameworks
- **Design Debt Quadrant** — alto impacto/fácil fix, alto impacto/difícil, baixo impacto/fácil, baixo/difícil
- **Cost of Delay** — impacto de não resolver o debt ao longo do tempo
- **Boy Scout Rule** — melhorar o que toca (debt oportunístico)
- **Debt Sprint** — sprint dedicado a resolver debt acumulado
- **Debt Budget** — % do sprint alocado continuamente para debt (ex: 20%)

## Checklists
- [ ] Inventário de design debt atualizado com todos os itens conhecidos
- [ ] Cada item classificado por tipo: visual, usability, DS drift, a11y, content
- [ ] Impacto estimado por item (usuários afetados, frequência, severidade)
- [ ] Esforço estimado por item (T-Shirt sizing)
- [ ] Itens posicionados no Design Debt Quadrant
- [ ] Top 10 itens priorizados com justificativa
- [ ] Estratégia de alocação definida: debt budget, debt sprint ou oportunístico
- [ ] Itens priorizados integrados ao design backlog
- [ ] Acordo com PM sobre alocação de capacidade para debt
- [ ] Métricas de debt burn-down atualizadas

## Steps
1. **Atualizar inventário** — Compilar todos os itens de design debt de: audits, reviews, QA
   reports, feedback de usuários e observações do squad. Remover itens já resolvidos.

2. **Classificar por tipo** — Categorizar cada item: inconsistência visual, problema de
   usabilidade, desvio do DS, issue de acessibilidade ou debt de conteúdo.

3. **Avaliar impacto** — Para cada item, estimar: número de usuários afetados, frequência de
   encontro, severidade do problema e custo de suporte associado.

4. **Estimar esforço** — Com designer e eng, estimar esforço de resolução usando T-Shirt sizing.
   Considerar: design time, dev time e QA time.

5. **Posicionar no quadrante** — Mapear itens no Design Debt Quadrant (impacto x esforço).
   Prioridade natural: alto impacto + baixo esforço primeiro.

6. **Identificar debt oportunístico** — Listar items de debt que podem ser resolvidos quando o
   squad estiver trabalhando em features na mesma área (Boy Scout Rule).

7. **Definir estratégia de alocação** — Negociar com PM: debt budget contínuo (20% do sprint),
   debt sprints periódicos ou abordagem oportunística. Documentar acordo.

8. **Integrar ao backlog** — Adicionar top items ao design backlog com labels de debt. Garantir
   visibilidade e tracking junto com work de features.

9. **Monitorar burn-down** — Acompanhar: items de debt resolvidos por sprint, novos items
   adicionados (debt creation rate) e net debt trend (acumulando ou reduzindo).

## Output
- **Design Debt Inventory** — Lista completa e categorizada de itens de debt
- **Prioritized Debt Backlog** — Top items priorizados com impacto e esforço
- **Debt Strategy** — Documento com estratégia de alocação e acordo com PM
- **Formato:** Planilha/board + Markdown
- **Nomenclatura:** `design-debt-prioritization-[YYYY-Qn]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design Lead + Design Ops |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Mensal ou trimestral |
| Aprovadores | Design Lead, PM |
| Repositório | `/squads/design/tasks/operations/` |

## Cross-References
- [Design Audit Existing Product](../discovery/design-audit-existing-product.md)
- [Design Backlog Grooming](./design-backlog-grooming.md)
- [DS Health Check](../design-system/ds-health-check.md)
- [Post-Launch Design Review](../review/post-launch-design-review.md)
- [Quarterly Design Review](./quarterly-design-review.md)
- [Remediate and Verify](../accessibility/remediate-and-verify.md)
