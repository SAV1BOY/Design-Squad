# Login Patterns

## Pattern Description

Padroes de login que equilibram seguranca e usabilidade. Cobre email/senha, social login, magic links, passkeys e login adaptativo baseado em contexto.

## Examples

### Example 1: Google — Smart Login

Google adapta o fluxo ao contexto do usuario:
- Campo de email primeiro (identifica o usuario)
- Se tem 2FA: mostra opcoes de verificacao
- Se tem passkey: oferece autenticacao biometrica
- Se conta corporativa: redireciona para SSO
- Avatares de contas recentes para troca rapida

Destaque: fluxo adaptativo que simplifica sem comprometer seguranca.

### Example 2: Linear — Magic Link + Password

Linear oferece duas opcoes lado a lado:
- Magic link: "Enviar link de login para seu email"
- Senha: campo tradicional com autocomplete
- Social login (Google, SAML) como alternativas
- Sem CAPTCHA visivel (reCAPTCHA v3 invisivel)

Destaque: magic link como opcao primaria reduz friccao de senha esquecida.

### Example 3: Apple — Passkey First

Apple prioriza passkeys em seus servicos:
- Autenticacao biometrica (Face ID / Touch ID) como primeiro prompt
- Fallback para senha apenas se biometria falhar
- Sem campo de senha visivel inicialmente
- Transicao transparente de senha para passkey

Destaque: elimina senhas progressivamente sem alienar usuarios existentes.

## Analysis

Login patterns eficazes:
- **Adaptativo**: ajusta o fluxo ao contexto (dispositivo, historico, risco)
- **Minimo atrito**: menos campos e passos possiveis
- **Autocomplete**: suporte a password managers e autofill
- **Error handling**: mensagens claras sem expor se email existe
- **Remember me**: sessoes longas para dispositivos confiáveis

Seguranca vs. UX: a solucao nao e escolher um ou outro, mas camadas adaptativas.

## Tags

`login`, `authentication`, `magic-link`, `passkeys`, `social-login`, `security`
