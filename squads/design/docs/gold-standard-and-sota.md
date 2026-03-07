# Gold Standard and SOTA

## Overview

Definição dos padrões de excelência (Gold Standard) e estado da arte (State of the
Art — SOTA) para o Design Squad. Este documento estabelece o que consideramos
"excelente" em cada dimensão do nosso trabalho e quais são as referências que
perseguimos.

## Content

### O que é Gold Standard

Gold Standard é o nível de qualidade que todo artefato do Design Squad deve atingir
antes de ser considerado "pronto". Não é perfeição — é o ponto onde qualidade e
pragmatismo se encontram. Abaixo do Gold Standard, não entregamos. Acima, é bônus.

### O que é SOTA

State of the Art (SOTA) representa as melhores práticas e resultados conhecidos na
indústria. É nosso norte aspiracional — onde queremos chegar. Pode não ser atingível
em todas as dimensões simultaneamente, mas guia nossa direção.

### Dimensões de Qualidade

#### 1. Design System
**Gold Standard:**
- Todos os componentes com documentação completa (usage, API, a11y, examples)
- Token architecture em 3 layers (primitive, semantic, component)
- Figma e code sincronizados com diff < 48h
- A11y review aprovada para 100% dos componentes stable
- Visual regression tests com cobertura > 90%

**SOTA (referências):**
- Atlassian Design System — Governança e documentação
- Polaris (Shopify) — Token architecture e theming
- Carbon (IBM) — Acessibilidade e escala
- Material Design 3 (Google) — Adaptive design e tokens

#### 2. Acessibilidade
**Gold Standard:**
- WCAG 2.2 AA compliance > 80% (medido por audit trimestral)
- Zero violations critical/serious em axe-core para fluxos críticos
- Keyboard navigation funcional em 100% dos fluxos
- Screen reader testado para fluxos core
- prefers-reduced-motion respeitado em toda animação

**SOTA (referências):**
- GOV.UK Design System — Referência mundial em a11y
- Apple Human Interface Guidelines — Assistive technology integration
- Inclusive Design Principles (Microsoft) — Framework de inclusão

#### 3. Pesquisa de Usuário
**Gold Standard:**
- > 60% das features de impacto médio+ têm input de pesquisa
- Research repository organizado e searchable
- Insights conectados a decisões de design documentadas
- Diversidade de participantes (PcD incluídas em > 20% dos estudos)
- Report entregue em < 1 semana após coleta

**SOTA (referências):**
- Spotify — Research ops e democratização de insights
- Airbnb — Mixed methods e research at scale
- Gov.uk — User research com populações diversas

#### 4. Processo de Design
**Gold Standard:**
- Lead time de design < 5 dias úteis (request to handoff)
- Rework rate < 10% (telas que voltam por bug de design)
- Design critique semanal com participação > 80%
- Handoff com 0 ambiguidades (medido por perguntas de devs)
- Post-launch review para 100% das features de impacto alto

**SOTA (referências):**
- Figma (a empresa) — Design ops e eficiência de processo
- Linear — Craft e atenção a detalhes
- Vercel — Speed de iteração e qualidade

#### 5. Comunicação e Documentação
**Gold Standard:**
- Toda decisão de design documentada com rationale
- Voice guidelines seguidas em > 90% das comunicações formais
- Microcopy review para 100% das features com texto
- Documentação atualizada com diff < 1 sprint
- Onboarding de novo membro < 2 semanas para produtividade

**SOTA (referências):**
- Stripe — Documentação e comunicação técnica
- Twilio — Developer-designer communication
- Intercom — Microcopy e content design

### Métricas de Gold Standard

| Dimensão | Métrica | Gold Standard | SOTA Target |
|----------|---------|---------------|-------------|
| Design System | Adoption rate | > 85% | > 95% |
| Acessibilidade | WCAG AA compliance | > 80% | > 95% |
| Pesquisa | Features com research | > 60% | > 80% |
| Processo | Design lead time | < 5 dias | < 3 dias |
| Processo | Rework rate | < 10% | < 5% |
| Documentação | Decisões documentadas | > 80% | > 95% |
| Satisfação | Stakeholder NPS | > 70 | > 85 |

### Como Medir

- **Trimestral:** Audit completo contra Gold Standard checklist
- **Por sprint:** Métricas de processo (lead time, rework rate)
- **Semestral:** Avaliação de SOTA gap e definição de targets

## Cross-References

- `docs/design-system-governance.md` — Governance que sustenta o Gold Standard
- `docs/accessibility-policy.md` — Política que define targets de a11y
- `docs/research-standards.md` — Padrões de pesquisa
- `docs/workflow-guide.md` — Processo de design
