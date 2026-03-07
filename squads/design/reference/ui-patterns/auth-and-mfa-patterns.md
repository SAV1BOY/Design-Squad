# Authentication and MFA Patterns



## Metadata

- **Categoria:** UI Patterns, Security, Identity
- **Relevancia para o Squad:** Alta — autenticacao e o gate de toda experiencia
- **Ultima revisao:** 2026-03-06



## Summary

Patterns de autenticacao e MFA (Multi-Factor Authentication) equilibram seguranca com usabilidade. Autenticacao excessivamente complexa causa abandono; excessivamente simples causa risco de seguranca. O design deve tornar o caminho seguro tambem o caminho facil.



## Key Concepts


### 1. Login Patterns

Email + password (tradicional), magic link (email sem senha), social login (Google, Apple, GitHub), SSO (enterprise). Cada opcao tem trade-offs: social login reduz fricao mas depende de terceiro; magic link elimina senhas mas depende de email; SSO e ideal para enterprise mas complexo de implementar.


### 2. Registration Optimization

Pedir o minimo para criar conta. Nome e email (ou telefone) sao suficientes inicialmente — completar perfil depois. Social signup reduz campos a zero. WCAG 2.2 exige que autenticacao nao dependa de memoria (anti-CAPTCHA cognitivo).


### 3. MFA Patterns

SMS (menos seguro, mais familiar), authenticator app (mais seguro, menos familiar), hardware key (mais seguro, menos acessivel), biometric (rapido, device-dependent), passkeys (futuro — passwordless com device biometric). Progressive MFA: exigir em acoes sensiveis, nao em todo login.


### 4. Password Recovery

Email de recovery com link temporario (nao enviar senha em plain text). Permitir mudanca imediata sem exigir senha antiga. Comunicar claramente os passos. Oferecer alternativas (SMS, security questions como backup). O fluxo de recovery e tao importante quanto o de login.


### 5. Passwordless and Passkeys

Passkeys (FIDO2/WebAuthn) sao o futuro: autenticacao via biometria do device sem senha. Mais seguro e mais simples. Apple, Google e Microsoft suportam. O design challenge e a transicao — educar usuarios sobre passkeys enquanto mantém opcoes tradicionais.



## Application to Design Squad

- **Login friction audit:** Medir abandono no login/signup. Cada campo e cada step adicional aumenta abandono. Minimizar ao essencial.
- **Social login como opcao primaria:** Oferecer social login (Google, Apple) como opcoes mais proeminentes. Email/password como alternativa, nao como default.
- **Progressive MFA:** Implementar MFA contextual — exigir em acoes sensiveis (pagamento, mudanca de email) em vez de todo login.
- **Passkeys strategy:** Planejar migracao para passkeys. Oferecer como opcao proeminente em configuracoes de seguranca, educar gradualmente.
- **Recovery flow testing:** Testar fluxo de recovery com usuarios reais. E o momento de maior frustacao e menor paciencia.



## Key Takeaways

1. **Cada campo no signup custa conversao.** Peca o minimo; complete o perfil depois.

2. **Social login reduz fricao dramaticamente.** Ofereca como opcao primaria quando apropriado.

3. **MFA contextual equilibra seguranca e UX.** Exija em acoes sensiveis, nao em todo acesso.

4. **Passkeys sao o futuro passwordless.** Comece a oferecer como opcao agora.

5. **Recovery flow e tao critico quanto login.** Usuarios frustrados com recovery abandonam o produto.



## Cross-References

- [Forms and Validation Patterns](forms-and-validation-patterns.md) — formularios de login
- [WCAG 2.x Notes](../standards/wcag-2-x-notes.md) — autenticacao acessivel (3.3.8)
- [Trust and Credibility Signals](../psychology/trust-and-credibility-signals.md) — sinais de seguranca
- [Fintech Design Playbook](../industries/fintech-design-playbook.md) — seguranca em fintech
- [ARIA Authoring Practices](../standards/aria-authoring-practices.md) — forms acessiveis
