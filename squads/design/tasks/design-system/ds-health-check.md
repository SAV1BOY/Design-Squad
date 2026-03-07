# DS Health Check

## Metadata
- **Categoria:** Design System
- **Complexidade:** Média
- **Tempo Estimado:** 2-3 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** design-system, health-check, metrics, quality, governance

## Objective
Executar uma avaliação periódica da saúde do design system medindo: adoção, consistência, qualidade
de documentação, satisfação dos consumidores e alinhamento design-código. O health check gera
um scorecard acionável que orienta investimentos e melhorias no DS.

## Prerequisites
- Design system em uso por pelo menos 1 squad consumidor
- Métricas de adoção instrumentadas (Figma analytics, code coverage)
- Acesso ao repositório de código dos componentes
- Canal de feedback com consumidores ativo
- Health check anterior (se não é o primeiro) como baseline

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design System Lead | Coordenar avaliação, coletar métricas e redigir report |
| Design Ops | Apoiar coleta de dados e métricas de adoção |
| Frontend Engineer (DS) | Avaliar saúde técnica: coverage, performance, bundle size |
| A11y Specialist | Verificar cobertura de acessibilidade nos componentes |
| Design Lead | Revisar scorecard e priorizar ações corretivas |

## Frameworks
- **DS Health Scorecard** — scorecard com dimensões ponderadas (0-100)
- **Adoption Metrics** — % componentes DS em uso, detach rate, coverage
- **Quality Metrics** — bugs, a11y compliance, documentation completeness
- **Satisfaction Survey (CSAT/NPS)** — percepção dos consumidores
- **Design-Code Parity** — % de alinhamento entre Figma e implementação

## Checklists
- [ ] Métricas de adoção coletadas (Figma analytics + code usage)
- [ ] Detach rate analisado (componentes removidos da library pelos consumidores)
- [ ] Coverage de componentes avaliado (% de features usando DS)
- [ ] Quality audit executado: bugs abertos, a11y compliance, token coverage
- [ ] Design-code parity verificado para top 10 componentes
- [ ] Documentação auditada: completude, atualização, acessibilidade
- [ ] Satisfaction survey distribuído e analisado
- [ ] Scorecard preenchido com scores por dimensão
- [ ] Top issues identificados e priorizados
- [ ] Action plan para o próximo ciclo definido

## Steps
1. **Coletar métricas de adoção** — Extrair dados de: Figma analytics (usage de componentes),
   code coverage (imports de DS packages), e detach rate (desvinculações de componentes).

2. **Avaliar qualidade técnica** — Com Frontend Engineer, verificar: bugs abertos, performance
   de componentes, bundle size, TypeScript coverage e test coverage.

3. **Auditar acessibilidade** — Verificar cobertura de ARIA patterns nos componentes publicados.
   Testar top 10 componentes com screen reader e keyboard.

4. **Verificar design-code parity** — Para os 10 componentes mais usados, comparar implementação
   com spec no Figma. Registrar divergências visuais e comportamentais.

5. **Auditar documentação** — Verificar para cada componente: spec existe, está atualizada,
   contém guidelines de uso, exemplos, props e acessibilidade.

6. **Distribuir satisfaction survey** — Enviar questionário curto (5-10 perguntas) para designers
   e engineers consumidores. Medir: facilidade de uso, qualidade, suporte.

7. **Calcular scorecard** — Preencher scorecard com scores de 0-100 para cada dimensão: adoção,
   qualidade, documentação, acessibilidade, parity, satisfação.

8. **Identificar top issues** — A partir do scorecard e survey, listar os 5-10 issues mais
   impactantes que precisam ser endereçados no próximo ciclo.

9. **Definir action plan** — Para cada issue, definir: owner, ação proposta, timeline e métrica
   de sucesso. Priorizar por impacto x esforço.

10. **Comunicar resultados** — Apresentar scorecard para Design Lead e stakeholders. Publicar
    resumo no canal do DS para transparência com consumidores.

## Output
- **DS Health Scorecard** — Scorecard visual com scores por dimensão
- **Health Check Report** — Relatório detalhado com dados, analysis e recomendações
- **Action Plan** — Lista priorizada de ações corretivas para próximo ciclo
- **Formato:** Markdown + scorecard visual + planilha de métricas
- **Nomenclatura:** `ds-health-check-[YYYY-Qn]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design System Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Trimestral |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/design-system/` |

## Cross-References
- [Component Inventory](./component-inventory.md)
- [Adoption and Migration](./adoption-and-migration.md)
- [Publish Library](./publish-library.md)
- [Design Audit Existing Product](../discovery/design-audit-existing-product.md)
- [Quarterly Design Review](../operations/quarterly-design-review.md)
- [Design Debt Prioritization](../operations/design-debt-prioritization.md)
