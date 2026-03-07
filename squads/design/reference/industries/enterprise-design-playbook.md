# Enterprise Design Playbook



## Metadata

- **Categoria:** Industry Playbook, Enterprise, B2B
- **Relevancia para o Squad:** Media-Alta — padroes para produtos B2B complexos
- **Ultima revisao:** 2026-03-06



## Summary

Enterprise design atende organizacoes como clientes — decisao de compra e coletiva, uso e diario e intensivo, dados sao complexos e volumosos, e a experiencia deve servir desde o admin que configura ate o usuario final que executa. O desafio e balancear poder (features avancadas) com usabilidade (onboarding e dia-a-dia).





## Key Concepts


### 1. Multiple User Roles

Enterprise tem multiplos roles com necessidades diferentes: admin (configura, gerencia), power user (usa intensivamente), casual user (usa ocasionalmente), viewer (apenas consulta). Cada role precisa de experiencia adequada — mas no mesmo produto. Role-based views e progressive disclosure atendem essa diversidade.


### 2. Data Density and Efficiency

Power users enterprise processam volumes altos de dados diariamente. Design para eficiencia: keyboard shortcuts, bulk actions, saved views, customizable dashboards, compact density mode. Performance percebida e critica — tabelas de 10.000 rows devem ser fluidas.


### 3. Admin and Configuration

Console de admin para: user management, permissions, billing, integrations, audit logs. Design challenge: tornar configuracao complexa manuseavel. Wizards para setup inicial, search em settings, undo para configuracoes erradas.


### 4. Onboarding Organizations (Not Just Users)

Enterprise onboarding e organizacional: SSO configuration, data import/migration, team setup, permission configuration, integration setup. E um projeto, nao um tutorial. Design: checklist de implementacao, status tracking, dedicated support chat.


### 5. Compliance and Audit

Enterprise requires: audit trails (quem fez o que quando), data export, retention policies, compliance certifications (SOC 2, ISO 27001). Design implication: activity logs accessiveis, export functionality, compliance badges visiveis.



## Application to Design Squad

- **Role-based design:** Mapear os roles do produto e projetar experiencias adequadas para cada um. Um unico layout nao serve admin e casual user.
- **Density modes:** Implementar comfortable e compact modes. Power users querem mais dados por tela; novatos querem mais espaco.
- **Keyboard shortcuts:** Para acoes frequentes, implementar shortcuts documentados. Shortcut hint (tooltip "Ctrl+K") nos elementos.
- **Admin console design:** Investir em admin console como produto separado. Admin experience impacta retenção organizacional.
- **Enterprise onboarding:** Projetar onboarding como checklist de implementacao com progress tracking, nao como tour de features.



## Key Takeaways

1. **Enterprise serve roles, nao apenas usuarios.** Design role-appropriate, nao one-size-fits-all.

2. **Eficiencia e o valor principal.** Power users enterprise medem valor em tempo economizado, nao em beleza.

3. **Admin experience e retention feature.** O admin que configura o produto decide se a org continua usando.

4. **Onboarding enterprise e projeto, nao tutorial.** Checklist de implementacao com semanas de ramp-up.

5. **Compliance e feature, nao restricao.** Audit logs, exports e certifications sao selling points para enterprise.



## Cross-References

- [Microsoft Fluent Notes](../standards/microsoft-fluent-notes.md) — enterprise design system
- [Carbon Design System](../standards/carbon-design-system-notes.md) — IBM enterprise
- [Dashboards and Tables Patterns](../ui-patterns/dashboards-and-tables-patterns.md) — data density
- [Settings and Preferences Patterns](../ui-patterns/settings-and-preferences-patterns.md) — admin settings
- [Auth and MFA Patterns](../ui-patterns/auth-and-mfa-patterns.md) — SSO enterprise
