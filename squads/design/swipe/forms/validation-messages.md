# Form Validation Message Patterns

## Pattern Description

Padroes para mensagens de validacao em formularios que comunicam erros de forma clara e ajudam usuarios a corrigir problemas rapidamente.

## Examples

### Example 1: Stripe — Real-time Card Validation
Stripe valida campos de cartao em tempo real:
- Numero do cartao: detecta bandeira enquanto digita (Visa, Mastercard)
- Validade: valida formato MM/YY e se nao expirou
- CVC: valida comprimento baseado na bandeira
- Erros inline posicionados abaixo de cada campo
- Icone de check verde quando campo valido

### Example 2: Mailchimp — Friendly Error Messages
Mailchimp usa linguagem amigavel em validacoes:
- "Hmm, esse e-mail nao parece certo" (em vez de "Email invalido")
- "Sua senha precisa de pelo menos 8 caracteres" (em vez de "Senha fraca")
- Sugestoes proativas: "Voce quis dizer gmail.com?"
- Erros aparecem on blur (nao enquanto digita)

### Example 3: GitHub — Progressive Validation
GitHub valida username progressivamente:
- Verifica disponibilidade em tempo real (debounced)
- Mostra regras e quais estao satisfeitas (checklist visual)
- Verde para regras atendidas, vermelho para nao atendidas
- Spinner durante verificacao de disponibilidade

## Analysis

Validacao eficaz:
- **Timing**: valide on blur ou apos pause na digitacao (nao on keystroke)
- **Linguagem**: diga o que esta errado E como corrigir
- **Posicao**: inline, abaixo do campo, nunca apenas no topo do form
- **Visual**: cor + icone + texto (nao apenas cor)
- **Summary**: para forms longos, erro summary no topo com links para campos
- **A11y**: `aria-invalid="true"` + `aria-describedby` no campo com erro

## Tags

`validation`, `forms`, `error-messages`, `ux-writing`, `real-time`, `a11y`
