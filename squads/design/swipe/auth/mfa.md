# Multi-Factor Authentication Patterns

## Pattern Description

Padroes de MFA (autenticacao multi-fator) que adicionam seguranca sem criar friccao excessiva. Cobre TOTP, push notifications, SMS, security keys e autenticacao adaptativa.

## Examples

### Example 1: GitHub — Flexible MFA Options

GitHub oferece multiplas opcoes de segundo fator:
- TOTP app (Authenticator) como padrao
- Security key (YubiKey, passkey) como upgrade
- SMS como fallback (com aviso de menor seguranca)
- Recovery codes gerados no setup
- Push notification via GitHub Mobile

Destaque: hierarquia clara de opcoes por seguranca com fallbacks acessiveis.

### Example 2: Stripe — Adaptive MFA

Stripe aplica MFA adaptativamente:
- Login de dispositivo conhecido: sem MFA adicional
- Novo dispositivo: MFA obrigatorio
- Acoes sensíveis (pagamentos): re-autenticacao
- Dashboard de seguranca com historico de dispositivos

Destaque: MFA proporcional ao risco reduz friccao em 80% dos logins.

### Example 3: 1Password — Biometric + Master Password

1Password combina fatores de forma transparente:
- Primeiro uso no dia: master password
- Usos subsequentes: biometria (Face ID / fingerprint)
- Timeout configuravel pelo usuario
- Travel mode que remove vaults sensiveis

Destaque: UX de "unlock" e familiar e rapida apos setup inicial.

## Analysis

MFA patterns eficazes:
- **Risk-based**: aplique MFA proporcionalmente ao risco da acao
- **Multiplas opcoes**: nunca dependa de um unico metodo
- **Recovery claro**: recovery codes acessiveis e faceis de salvar
- **Setup guiado**: wizard com instrucoes visuais passo-a-passo
- **Feedback claro**: confirme sucesso e falha de cada verificacao

Equilibrio: seguranca maxima com friccao minima, adaptando ao contexto.

## Tags

`mfa`, `2fa`, `authentication`, `security`, `totp`, `passkeys`, `adaptive-auth`
