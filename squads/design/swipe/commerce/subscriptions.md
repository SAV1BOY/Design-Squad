# Subscription Management Patterns

## Pattern Description

Padroes para gerenciamento de assinaturas — upgrade, downgrade, cancelamento e billing. Foco em transparencia, retencao e facilidade de gerenciamento.

## Examples

### Example 1: Spotify — Easy Upgrade/Downgrade
Spotify simplifica mudanca de plano:
- Comparacao clara entre plano atual e opcoes
- "Upgrade" como CTA primario destacado
- Downgrade disponivel mas menos proeminente
- Pro-rata automatico na mudanca
- Confirmacao com resumo de mudancas no valor

### Example 2: Netflix — Retention-Focused Cancel
Netflix usa fluxo de cancelamento com retencao:
- "Cancel Membership" acessivel em configuracoes (sem esconder)
- Pergunta motivo do cancelamento
- Oferece pause (manter conta sem cobrar por 1-3 meses)
- Mostra o que sera perdido (perfis, recomendacoes)
- Confirma data final de acesso

### Example 3: GitHub — Transparent Billing
GitHub mostra billing com total transparencia:
- Dashboard de billing com historico de faturas
- Usage meters para features com limite
- Alerta antes de atingir limites
- Downgrade path claro com aviso de features perdidas
- Invoice download em PDF para cada cobranca

## Analysis

Subscription management eficaz:
- **Transparencia**: sem dark patterns para cancelar
- **Self-service**: usuario deve conseguir mudar/cancelar sem contatar suporte
- **Proration**: calcule pro-rata justo em mudancas mid-cycle
- **Retention honesta**: ofereça alternativas (pause, downgrade) sem manipular
- **Billing history**: faturas acessiveis e downloadable
- **Alertas**: notifique antes de renovacao e antes de limites

## Tags

`subscriptions`, `billing`, `retention`, `upgrade`, `downgrade`, `cancel`, `saas`
