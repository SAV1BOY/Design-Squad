# SaaS Design Playbook



## Metadata

- **Categoria:** Industry Playbook, SaaS, Product Design
- **Relevancia para o Squad:** Alta — padroes e praticas especificos de SaaS
- **Ultima revisao:** 2026-03-06



## Summary

Software as a Service (SaaS) tem desafios de design especificos: onboarding que converte trial em paying customer, dashboards que demonstram valor continuamente, pricing que escala com uso, e uma experiencia que reduz churn retendo usuarios mês a mês. Este playbook compila padroes e praticas de design especificos para o contexto SaaS.





## Key Concepts


### 1. Trial-to-Paid Conversion

O trial e a janela critica: o usuario deve atingir o "aha moment" antes do trial expirar. Design para trial: reduzir setup friction, mostrar valor rapidamente (pre-populated data, templates), comunicar progresso ("3 dias restantes, voce ja completou 80% do setup").


### 2. Feature Gating and Upgrade Paths

Decidir quais features estao em cada plano. Design challenge: mostrar que features gated existem (teaser) sem frustar excessivamente. Upgrade prompts devem ser contextuais ("Para exportar em PDF, upgrade para Pro") e nao intrusivos.


### 3. Dashboard as Value Demonstration

O dashboard SaaS demonstra valor continuamente — metricas que o usuario nao teria sem o produto. Design focus: KPIs que importam para o usuario, trends que mostram progresso, insights acionaveis. Se o dashboard nao demonstra valor, o usuario questiona a assinatura.


### 4. Churn Prevention by Design

Intervencoes de design para reduzir churn: re-engagement emails para usuarios inativos, in-app messages para features nao descobertas, cancellation flow com alternativas (pause, downgrade), e exit survey para entender razoes.


### 5. Multi-Tenant and Team Features

SaaS B2B frequentemente serve teams: roles e permissions, shared workspaces, activity feeds, admin consoles. Design challenge: escalar a experiencia de individual para team sem aumentar complexidade para usuarios solo.



## Application to Design Squad

- **Aha moment optimization:** Identificar e otimizar o aha moment — a acao que correlaciona com retencao. Medir quantos trial users atingem e em quanto tempo.
- **Upgrade moment design:** Para cada feature gated, projetar o momento de upgrade: teaser visual da feature + clear value proposition + one-click upgrade. Nao frustrar, convidar.
- **Dashboard value audit:** Trimestralmente, auditar se o dashboard demonstra valor claro. O usuario sabe por que esta pagando ao olhar o dashboard?
- **Cancellation flow design:** Projetar cancellation flow com alternativas genuinas (pause, downgrade, feedback) sem sludge (dificuldade artificial).
- **Team features roadmap:** Se o produto serve teams, priorizar roles/permissions, shared spaces e admin features como investimento de retencao.



## Key Takeaways

1. **O trial e a venda — o design do trial e o design de vendas.** Cada decisao de UX no trial impacta conversao.

2. **Dashboards demonstram valor mensalmente.** O usuario renova a assinatura mental todo mês ao ver o dashboard.

3. **Feature gating deve convidar, nao frustrar.** Mostre que mais existe; nao bloqueie o fluxo atual.

4. **Cancellation honesta retém mais que sludge.** Alternativas genuinas e exit survey sao mais eficazes que dark patterns.

5. **Team features sao retention features.** Quanto mais do time usa, maior o switching cost.



## Cross-References

- [Onboarding Patterns](../ui-patterns/onboarding-patterns.md) — trial onboarding
- [Dashboards and Tables Patterns](../ui-patterns/dashboards-and-tables-patterns.md) — dashboard design
- [Pricing and Plans Patterns](../ui-patterns/pricing-and-plans-patterns.md) — pricing SaaS
- [Hooked — Eyal](../books/eyal-hooked.md) — habit formation para retencao
- [Lean UX — Gothelf](../books/gothelf-lean-ux.md) — experimentacao continua
