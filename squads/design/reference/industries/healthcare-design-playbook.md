# Healthcare Design Playbook



## Metadata

- **Categoria:** Industry Playbook, HealthTech, Regulated Design
- **Relevancia para o Squad:** Baixa-Media — padroes para contextos de saude
- **Ultima revisao:** 2026-03-06



## Summary

Healthcare design opera sob restricoes unicas: regulamentacao rigorosa (HIPAA, LGPD para dados de saude), usuarios em estados emocionais vulneráveis, necessidade de precisao absoluta e diversidade extrema de literacia de saude. O design deve ser acessivel, empático, preciso e compliance-first.



## Key Concepts


### 1. Patient-Centric Design

Pacientes sao usuarios em contexto de vulnerabilidade. Design empático: linguagem clara (evitar jargão medico), tom tranquilizador, affordances obvias, reduzir ansiedade de espera com informação transparente.


### 2. Data Privacy and Compliance

HIPAA (USA), LGPD (Brasil), GDPR para dados de saude requerem protecoes especiais. Consent explicito, data minimization, access logging, encryption. Design implication: consentimento informado integrado ao fluxo, nao escondido em termos.


### 3. Accessibility as Necessity

Usuarios de saude incluem idosos, pessoas com deficiencia visual, motora e cognitiva em proporcao maior que media. WCAG AAA e recomendado (nao apenas AA). Font sizes maiores, contraste alto, navegacao simples, linguagem de nivel basico de leitura.


### 4. Clinical Decision Support

Para interfaces de profissionais de saude: alertas claros para interacoes medicamentosas, dosagens, alergias. Hierarquia visual rigorosa (critico > importante > informativo). Minimizar alert fatigue (muitos alertas = todos ignorados).


### 5. Telemedicine UX

Video consultation: preparacao pre-consulta (checklist de sintomas), sala de espera virtual com estimativa de tempo, interface de video simples, compartilhamento de documentos, resumo pos-consulta com proximos passos.



## Application to Design Squad

- **Empathy-first design:** Se o produto toca contexto de saude, treinar o squad em design empático. Usuarios podem estar ansioso, com dor ou confusos.
- **LGPD para dados de saude:** Dados de saude tem protecao especial na LGPD. Garantir consentimento explicito e especifico para cada tipo de dado de saude coletado.
- **Accessibility elevated:** Para contextos de saude, mirar WCAG AAA, nao apenas AA. Font sizes maiores, contraste mais alto, linguagem mais simples.
- **Alert hierarchy:** Se o produto tem alertas de saude, definir hierarquia clara e limitada (max 3 niveis). Reduzir alert fatigue priorizando apenas alertas acionaveis.
- **Simple language:** Toda comunicação de saude deve ser em linguagem de nivel basico de leitura. Testar com usuarios de baixa literacia de saude.



## Key Takeaways

1. **Usuarios de saude sao vulneraveis — design deve ser empatico.** Tom, linguagem e affordances devem acomodar ansiedade.

2. **Dados de saude tem protecao legal especial.** LGPD para saude e mais restritiva que LGPD geral.

3. **Acessibilidade e necessidade, nao nice-to-have.** A base de usuarios de saude inclui proporcao alta de pessoas com necessidades especiais.

4. **Menos alertas = alertas mais eficazes.** Alert fatigue e risco real em healthcare — curar alertas agressivamente.

5. **Linguagem simples salva vidas.** Instrução medica incompreendida pode ter consequencias graves.



## Cross-References

- [WCAG 2.x Notes](../standards/wcag-2-x-notes.md) — acessibilidade elevada
- [Behavioral Design Ethics](../psychology/behavioral-design-ethics.md) — etica com vulneraveis
- [Trust and Credibility Signals](../psychology/trust-and-credibility-signals.md) — confianca em saude
- [Forms and Validation Patterns](../ui-patterns/forms-and-validation-patterns.md) — formularios de saude
- [Notifications and Alerts Patterns](../ui-patterns/notifications-and-alerts-patterns.md) — alertas clinicos
