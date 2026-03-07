# Design Audit — Existing Product

## Metadata
- **Categoria:** Discovery
- **Complexidade:** Alta
- **Tempo Estimado:** 5-8 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** discovery, audit, design-debt, heuristics, consistency

## Objective
Realizar um audit abrangente do produto existente para identificar inconsistências visuais,
problemas de usabilidade, dívida de design e oportunidades de melhoria. O resultado serve como
baseline para priorização de design debt e planejamento de evoluções incrementais.

## Prerequisites
- Acesso completo ao produto em todos os ambientes (staging e produção)
- Design system atual documentado (se existente)
- Dados de analytics e heatmaps disponíveis
- Tickets de suporte e feedback de usuários dos últimos 3 meses
- Ferramenta de auditoria configurada (Figma Audit plugin, ou equivalente)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design Lead | Definir escopo do audit e priorizar findings |
| UI Designer | Catalogar inconsistências visuais e de componentes |
| UX Designer | Avaliar fluxos, heurísticas e padrões de interação |
| A11y Specialist | Verificar conformidade com WCAG 2.2 nos fluxos auditados |
| Product Manager | Contextualizar decisões históricas e priorizar remediações |

## Frameworks
- **Nielsen's 10 Heuristics** — avaliação heurística estruturada
- **WCAG 2.2 (Level AA)** — critérios de acessibilidade
- **Visual Consistency Audit** — checklist de tokens, tipografia, espaçamento, cor
- **Severity Rating Scale** — classificação de 0 (cosmético) a 4 (catastrófico)
- **Design Debt Quadrant** — categorização por impacto e esforço de correção

## Checklists
- [ ] Escopo do audit definido (fluxos, páginas, plataformas)
- [ ] Checklist de heurísticas preparado e calibrado entre avaliadores
- [ ] Audit visual executado: cores, tipografia, espaçamento, iconografia
- [ ] Audit de usabilidade executado: fluxos críticos avaliados com heurísticas
- [ ] Audit de acessibilidade executado: contraste, landmarks, keyboard navigation
- [ ] Inconsistências catalogadas com screenshots e severity rating
- [ ] Design debt backlog criado e priorizado
- [ ] Relatório final revisado pelo Design Lead
- [ ] Apresentação para stakeholders realizada
- [ ] Quick wins identificados para ação imediata

## Steps
1. **Definir escopo e prioridade** — Mapear todas as páginas e fluxos do produto. Priorizar
   os mais críticos por volume de uso (analytics) e impacto de negócio.

2. **Preparar instrumentos de avaliação** — Configurar checklists de heurísticas, critérios
   WCAG e template de registro de findings. Calibrar entre avaliadores com 1 fluxo-piloto.

3. **Executar audit visual** — Percorrer sistematicamente cada tela verificando: uso correto
   de tokens, consistência tipográfica, espaçamento, hierarquia visual e uso de componentes.

4. **Executar audit de usabilidade** — Avaliar cada fluxo crítico contra as 10 heurísticas
   de Nielsen. Registrar violações com descrição, screenshot e severity rating.

5. **Executar audit de acessibilidade** — Verificar contraste de cores, estrutura de headings,
   alt texts, keyboard navigation e screen reader compatibility nos fluxos priorizados.

6. **Catalogar e classificar findings** — Consolidar todos os findings em uma planilha única
   com: localização, tipo, severidade, screenshot e recomendação de correção.

7. **Criar design debt backlog** — Transformar findings em itens acionáveis no backlog,
   classificados pelo Design Debt Quadrant (impacto x esforço).

8. **Identificar quick wins** — Selecionar 5-10 correções de alto impacto e baixo esforço
   para implementação imediata, sem necessidade de redesign.

9. **Elaborar relatório executivo** — Redigir documento com: resumo quantitativo, top findings
   por categoria, design debt backlog priorizado e roadmap de remediação sugerido.

10. **Apresentar e alinhar próximos passos** — Conduzir sessão com stakeholders para apresentar
    findings e alinhar priorização de correções no próximo ciclo de sprint.

## Output
- **Design Audit Report** — Relatório completo com findings categorizados e priorizados
- **Design Debt Backlog** — Lista de itens acionáveis com severity e esforço estimado
- **Quick Wins List** — Seleção de correções para implementação imediata
- **Formato:** Markdown + planilha de findings + screenshots no Figma/Miro
- **Nomenclatura:** `design-audit-[produto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Semestral ou por projeto major |
| Aprovadores | Design Lead, PM, Head of Design |
| Repositório | `/squads/design/tasks/discovery/` |

## Cross-References
- [Problem Definition](./problem-definition.md)
- [Competitive UI Audit](./competitive-ui-audit.md)
- [A11y Audit](../accessibility/a11y-audit.md)
- [Design Debt Prioritization](../operations/design-debt-prioritization.md)
- [DS Health Check](../design-system/ds-health-check.md)
- [Component Inventory](../design-system/component-inventory.md)
