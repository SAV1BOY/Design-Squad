# Measuring Design Impact

## Overview

Medir o impacto do design no negocio e um dos maiores desafios enfrentados por times de
design em todo o mundo. Este documento estabelece o framework utilizado pelo Design Squad
da MMOS para quantificar, comunicar e amplificar o valor que o design gera para a
organizacao.

A dificuldade de medir design impact reside no fato de que o design influencia resultados
de forma indireta e multifacetada — desde a percepcao de marca ate a eficiencia operacional,
passando pela satisfacao do usuario e pela conversao de vendas. Nosso framework busca
capturar essa complexidade de forma pratica e acionavel.

Este modelo e informado por pesquisas do McKinsey Design Index, pelo framework HEART do
Google, pela metodologia de Design Value Scorecard da InVision, e por praticas de
organizacoes líderes em design como Airbnb e IBM.

## Key Insights

### Por que Medir Design Impact?

A medicao de impacto de design serve a multiplos propositos:

1. **Justificar Investimentos** — Demonstrar ROI de design para a lideranca executiva
2. **Guiar Priorizacao** — Direcionar esforcos para areas de maior impacto potencial
3. **Melhorar Qualidade** — Criar feedback loops que elevam a qualidade do output
4. **Aumentar Influencia** — Fortalecer a posicao de design nas decisoes estrategicas
5. **Desenvolver o Time** — Identificar areas de crescimento e excelencia

### Framework MMOS de Design Metrics

Organizamos nossas metricas em quatro camadas, da mais proxima do usuario a mais proxima
do negocio:

#### Camada 1 — Experience Metrics (Metricas de Experiencia)

Medem a qualidade da experiencia do usuario diretamente:

| Metrica | Descricao | Ferramenta | Target |
|---------|-----------|------------|--------|
| Task Success Rate | Percentual de usuarios que completam tarefas-chave | Usability testing | > 90% |
| Time on Task | Tempo medio para completar tarefas criticas | Analytics | Reducao de 20% YoY |
| Error Rate | Frequencia de erros do usuario em fluxos principais | Analytics + Hotjar | < 5% |
| System Usability Scale (SUS) | Score padronizado de usabilidade | Surveys | > 75 |
| Customer Effort Score (CES) | Esforco percebido pelo usuario | Post-interaction survey | > 4/5 |

#### Camada 2 — Engagement Metrics (Metricas de Engajamento)

Medem como o design influencia o comportamento do usuario:

| Metrica | Descricao | Ferramenta | Target |
|---------|-----------|------------|--------|
| Feature Adoption Rate | Percentual de usuarios que adotam novas features | Analytics | > 60% em 30 dias |
| User Retention (D7/D30) | Retencao de usuarios apos 7 e 30 dias | Analytics | D7 > 70%, D30 > 50% |
| Session Duration | Tempo medio de sessao | Analytics | Aumento de 15% YoY |
| Net Promoter Score (NPS) | Probabilidade de recomendacao | Surveys | > 50 |
| Bounce Rate | Taxa de rejeicao em paginas-chave | Analytics | < 30% |

#### Camada 3 — Efficiency Metrics (Metricas de Eficiencia)

Medem como o design impacta a eficiencia interna:

| Metrica | Descricao | Ferramenta | Target |
|---------|-----------|------------|--------|
| Design System Adoption | Percentual de componentes do DS em uso | Figma analytics | > 90% |
| Design-to-Dev Handoff Time | Tempo medio do handoff design-engineering | Jira | < 2 dias |
| Rework Rate | Percentual de design que precisa ser refeito | Sprint tracking | < 10% |
| Support Ticket Reduction | Reducao de tickets relacionados a UX | Zendesk | -25% QoQ |
| Accessibility Compliance | Percentual de telas em conformidade WCAG 2.1 | Audit tools | 100% AA |

#### Camada 4 — Business Metrics (Metricas de Negocio)

Medem o impacto direto do design nos resultados financeiros:

| Metrica | Descricao | Ferramenta | Target |
|---------|-----------|------------|--------|
| Conversion Rate | Taxa de conversao em fluxos redesenhados | Analytics | +15% pos-redesign |
| Customer Acquisition Cost (CAC) | Custo de aquisicao influenciado por UX | Finance + Analytics | Reducao de 10% |
| Customer Lifetime Value (CLV) | Valor vitalicio influenciado pela experiencia | Finance | Aumento de 20% |
| Revenue per User | Receita media por usuario | Finance | Aumento de 10% YoY |
| Churn Rate | Taxa de cancelamento | Analytics | Reducao de 15% |

### Atribuicao e Causalidade

Um dos maiores desafios na medicao de design impact e a atribuicao. Como saber que uma
melhoria na conversion rate foi causada pelo redesign e nao por outros fatores?

Abordagens utilizadas:

1. **A/B Testing** — Comparacao direta entre versoes com e sem mudancas de design
2. **Before/After Analysis** — Medicao de metricas antes e depois de intervencoes de design
3. **Cohort Analysis** — Comparacao entre grupos de usuarios expostos a diferentes experiencias
4. **Regression Analysis** — Analise estatistica para isolar o efeito do design
5. **Qualitative Correlation** — Conexao entre feedback qualitativo e metricas quantitativas

### O HEART Framework Adaptado

Nosso framework se inspira no HEART do Google (Happiness, Engagement, Adoption, Retention,
Task Success) mas adiciona camadas de Business Impact e Efficiency que sao especialmente
relevantes para o contexto da MMOS.

Para cada metrica, definimos:

- **Goal** — O que queremos alcançar
- **Signal** — Que comportamento indica sucesso
- **Metric** — Como medimos o sinal numericamente

## Application to MMOS

### Implementacao Pratica

**Dashboard de Design Metrics:**
- Centralizado no Looker/Data Studio com atualizacao em tempo real
- Visivel para todo o Design Squad e stakeholders
- Revisado nas retrospectivas de sprint e nos QBRs (Quarterly Business Reviews)

**Cadencia de Reporting:**

| Report | Audiencia | Frequencia | Conteudo |
|--------|-----------|------------|----------|
| Sprint Design Report | Design Squad | Bi-semanal | Experience + Efficiency metrics |
| Monthly Design Impact | Product + Engineering | Mensal | Engagement + Efficiency |
| Quarterly Design Review | Leadership | Trimestral | Todas as camadas + Trends |
| Annual Design Impact | Executive Team | Anual | ROI consolidado + Strategic insights |

**Processo de Coleta:**
1. Instrumentacao automatica via analytics tools (Amplitude, Mixpanel)
2. Surveys periodicos (NPS trimestral, SUS apos releases maiores)
3. Usability testing regular (minimo 1x por sprint)
4. Design system health check mensal
5. Analise de support tickets categorizada por tipo de issue

### Caso Pratico — Medicao do Redesign do Onboarding

No ultimo redesign do fluxo de onboarding da MMOS, aplicamos o framework completo:

- Task Success Rate: 72% → 91% (+26%)
- Time to Complete: 8.5min → 4.2min (-51%)
- D7 Retention: 58% → 71% (+22%)
- Support Tickets (onboarding): 340/mes → 180/mes (-47%)
- Conversion to Paid: 12% → 18% (+50%)

Esses resultados foram comunicados em um Design Impact Report que fortaleceu
significativamente a posicao de design nas decisoes de investimento do Q seguinte.

## Cross-References

- [Design Leadership Principles](./design-leadership-principles.md) — Como lideranca usa metricas para advocacy
- [Design Maturity Model](./design-maturity-model.md) — Metricas como indicador de maturidade
- [Design Culture Building](./design-culture-building.md) — Cultura data-informed no design
- [Google Material Design Case](./case-studies/google-material-design.md) — Como Google mede design at scale
- [Shopify Polaris Case](./case-studies/shopify-polaris.md) — Metricas de design system impact

---

> "If you can't measure it, you can't improve it — but measurement without context is just noise."
> O segredo esta em medir o que importa e interpretar com nuance.

**Ultima atualizacao:** Marco 2026
**Responsavel:** Design Lead — MMOS Design Squad
