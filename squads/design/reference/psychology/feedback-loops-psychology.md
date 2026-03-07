# Feedback Loops Psychology



## Metadata

- **Categoria:** Behavioral Psychology, Interaction Design
- **Relevancia para o Squad:** Media-Alta — feedback como motor de engajamento e aprendizado
- **Ultima revisao:** 2026-03-06



## Summary

Feedback loops sao ciclos de acao-resultado-ajuste que permitem ao usuario (e ao sistema) melhorar continuamente. Em interfaces, feedback pode ser imediato (animacao de clique), de curto prazo (resultado de busca), ou de longo prazo (progress dashboard). Feedback eficaz informa, motiva e corrige.





## Key Concepts


### 1. Immediate Feedback (Microinteractions)

Resposta visual/sonora/haptica a cada acao do usuario: hover states, click animations, loading indicators, success confirmations. A ausencia de feedback imediato e percebida como "o sistema nao respondeu" — causando re-clicks e frustração.


### 2. Short-Term Feedback (Action Results)

Resultado da acao em segundos a minutos: resultado de busca, confirmacao de envio, preview de mudanca. Deve ser especifico (nao apenas "sucesso" — dizer o que aconteceu), acionavel (o que fazer em seguida) e reversivel quando possivel (undo).


### 3. Long-Term Feedback (Progress and Growth)

Dashboard de progresso, achievement systems, streak counters, skill development metrics. Feedback de longo prazo mostra ao usuario que esta evoluindo, reforçando investimento continuo no produto. Goal-gradient effect: progresso visivel aumenta motivacao.


### 4. Positive vs. Corrective Feedback

Positive: "Otimo! Perfil 80% completo." Corrective: "Este campo precisa de formato DD/MM/AAAA." A proporcao ideal e mais positivo que corrective. Feedback exclusivamente corrective cria sensacao de "nada que faco esta certo."


### 5. System Feedback vs. Social Feedback

System feedback: do sistema para o usuario (validacao, confirmacao, metricas). Social feedback: de outros usuarios (likes, comentarios, reviews). Social feedback e mais motivador mas menos controlavel. Combinar ambos maximiza engajamento.



## Application to Design Squad

- **Feedback audit por fluxo:** Para cada fluxo critico, mapear onde o usuario recebe feedback. Identificar gaps (acoes sem feedback) e excessos (feedback redundante).
- **Response time guidelines:** < 100ms para feedback visual (hover, click). < 1s para resultado de acao simples. < 10s para operacao complexa (com progress indicator). Documentar no design system.
- **Positive/corrective ratio:** Em interfaces de input (formularios, configuracao), garantir que feedback positivo (checkmarks, mensagens de sucesso) e tao presente quanto corrective (erros).
- **Progress visualization:** Para fluxos longos (onboarding, setup, learning), implementar visualizacao de progresso que mostra quanto ja foi feito e quanto falta.
- **Feedback consistency:** Padronizar feedback no design system: success = toast verde, error = inline vermelho, warning = banner amarelo, info = toast azul. Consistencia reduz aprendizado.



## Key Takeaways

1. **Ausencia de feedback = sistema quebrado.** Toda acao do usuario deve ter resposta visivel, mesmo que minima.

2. **Tres escalas de feedback: imediato, curto prazo, longo prazo.** Cada uma serve proposito diferente.

3. **Mais feedback positivo que corretivo.** A proporcao importa para a experiencia emocional geral.

4. **Progresso visivel motiva continuidade.** Mostrar quanto ja foi feito e tao motivador quanto mostrar quanto falta.

5. **Consistencia de feedback reduz carga cognitiva.** O usuario aprende uma vez o que cada tipo de feedback significa.



## Cross-References

- [Design of Everyday Things — Norman](../books/norman-design-of-everyday-things.md) — feedback como principio fundamental
- [Peak-End Rule](peak-end-rule-in-ux.md) — feedback em momentos de pico
- [Hooked — Eyal](../books/eyal-hooked.md) — variable reward como feedback
- [Notifications and Alerts Patterns](../ui-patterns/notifications-and-alerts-patterns.md) — padroes de feedback
- [Designing with the Mind — Johnson](../books/johnson-designing-with-the-mind.md) — time constants
