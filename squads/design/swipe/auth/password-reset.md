# Password Reset Patterns

## Pattern Description

Padroes de recuperacao de senha que sao seguros, claros e reduzem abandono. Cobre fluxo por email, validacao de identidade, criacao de nova senha e confirmacao.

## Examples

### Example 1: Mailchimp — Friendly Reset Flow

Mailchimp torna o reset de senha acolhedor:
- Tela com texto amigavel: "Acontece com todo mundo"
- Campo de email com validacao inline
- Email enviado com link de expiracao (1 hora)
- Pagina de nova senha com password strength meter
- Confirmacao com redirect automatico para login

Destaque: tom de voz amigavel reduz frustracao em momento estressante.

### Example 2: Slack — Magic Link Alternative

Slack oferece alternativa ao reset tradicional:
- Em vez de "esqueci a senha", oferece "Sign in with email"
- Magic link enviado ao email
- Apos login via magic link, opcao de definir nova senha
- Sessoes ativas em outros dispositivos mantidas

Destaque: magic link como alternativa evita o fluxo de reset completo.

### Example 3: Apple — Identity Verification

Apple usa verificacao de identidade robusta:
- Identifica via email ou telefone associado
- Envia codigo de verificacao ao dispositivo confiavel
- Recovery key como fallback para contas com Advanced Data Protection
- Cooldown period apos tentativas falhas

Destaque: seguranca proporcional ao valor da conta (ecossistema Apple).

## Analysis

Password reset eficaz:
- **Descobribilidade**: link de "esqueci senha" proximo ao campo de senha
- **Feedback seguro**: "Se este email existir, enviaremos instrucoes"
- **Expiracao**: links de reset expiram em 1-24 horas
- **Strength meter**: mostre forca da nova senha em tempo real
- **Confirmacao**: confirme sucesso e permita login imediato
- **Notificacao**: avise por email que a senha foi alterada

Nunca revele se um email esta cadastrado — proteja contra enumeracao.

## Tags

`password-reset`, `account-recovery`, `security`, `magic-link`, `ux-writing`
