# Adoption and Migration

## Metadata
- **Categoria:** Design System
- **Complexidade:** Alta
- **Tempo Estimado:** Contínuo (sprints dedicados)
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** design-system, adoption, migration, rollout, governance

## Objective
Planejar e executar a adoção do design system por squads consumidores, incluindo migração de
componentes legados, treinamento de designers e engineers, e monitoramento de métricas de adoção.
O processo garante que o DS é efetivamente utilizado e não apenas publicado.

## Prerequisites
- Design system library publicada com componentes estáveis
- Documentação de componentes e tokens disponível
- Inventário de componentes legados que precisam migrar
- Buy-in de Engineering Leads dos squads consumidores
- Métricas de adoção definidas e instrumentadas

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design System Lead | Coordenar estratégia de adoção e apoiar migração |
| Design Ops | Monitorar métricas, criar materiais de enablement |
| Design Lead | Promover adoção e resolver resistências no squad |
| Frontend Engineer (DS) | Apoiar migração técnica e resolver issues |
| Squad Designers | Executar migração nos projetos e reportar issues |

## Frameworks
- **Adoption Funnel** — awareness > trial > adoption > advocacy
- **Migration Playbook** — guia passo a passo para migrar componentes legados
- **DS Adoption Score** — métrica composta de uso de componentes, tokens e patterns
- **Office Hours Model** — sessões recorrentes de suporte ao vivo
- **Champion Program** — designar embaixadores do DS em cada squad

## Checklists
- [ ] Estratégia de rollout definida (big bang vs incremental)
- [ ] Squads priorizados para adoção (por impacto e readiness)
- [ ] Migration playbook redigido e testado internamente
- [ ] Treinamento para designers criado e agendado
- [ ] Treinamento para engineers criado e agendado
- [ ] Champions identificados em cada squad consumidor
- [ ] Office hours semanais agendadas e divulgadas
- [ ] Métricas de adoção instrumentadas (% de componentes DS em uso)
- [ ] Feedback loop configurado (channel, issue tracker)
- [ ] Review mensal de adoção agendado

## Steps
1. **Definir estratégia de rollout** — Escolher entre: big bang (todos os squads simultaneamente)
   ou incremental (squad por squad). Considerar maturidade do DS e capacidade de suporte.

2. **Priorizar squads** — Classificar squads consumidores por: impacto da adoção, readiness
   técnica e willingness. Começar pelos mais receptivos para gerar momentum.

3. **Criar migration playbook** — Documentar passo a passo: como substituir componentes legados,
   como conectar libraries, como resolver conflitos e como reportar issues.

4. **Recrutar champions** — Identificar 1 designer e 1 engineer por squad como embaixadores do
   DS. Oferecer: acesso antecipado, input em decisões e reconhecimento.

5. **Conduzir treinamentos** — Realizar workshops de 60-90 minutos para: designers (como usar
   componentes e tokens) e engineers (como consumir packages e contribuir).

6. **Estabelecer office hours** — Criar sessão semanal de 30 minutos aberta para dúvidas, issues
   e sugestões. Documentar perguntas frequentes para FAQ.

7. **Executar migração assistida** — Para o primeiro squad, trabalhar side-by-side na migração
   de 1-2 features para criar precedente e refinar o playbook.

8. **Monitorar métricas** — Acompanhar: % de componentes DS em uso, número de detach do Figma,
   issues reportados, tempo de onboarding e satisfação dos consumidores.

9. **Iterar e escalar** — Com base no feedback e métricas, ajustar playbook e abordagem.
   Escalar para próximos squads conforme confiança e capacidade de suporte.

10. **Comunicar progresso** — Compartilhar métricas de adoção mensalmente com leadership. Celebrar
    marcos (ex: "80% de adoção no Squad X") para manter momentum.

## Output
- **Adoption Strategy** — Documento com plano de rollout e timeline
- **Migration Playbook** — Guia de migração para consumidores
- **Training Materials** — Slides e exercises para workshops
- **Adoption Dashboard** — Métricas de adoção por squad e por componente
- **Formato:** Markdown + slides + dashboard
- **Nomenclatura:** `ds-adoption-plan-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design System Lead + Design Ops |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Contínuo com review mensal |
| Aprovadores | Design Lead, Head of Design |
| Repositório | `/squads/design/tasks/design-system/` |

## Cross-References
- [Publish Library](./publish-library.md)
- [Component Inventory](./component-inventory.md)
- [DS Health Check](./ds-health-check.md)
- [Onboard New Designer](../operations/onboard-new-designer.md)
- [Cross-Squad Sync](../operations/cross-squad-sync.md)
- [Update Design System Docs](../operations/update-design-system-docs.md)
