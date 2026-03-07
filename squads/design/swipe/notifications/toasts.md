# Toast Notification Patterns

## Pattern Description

Padroes para notificacoes toast (snackbar) — mensagens temporarias que informam sobre o resultado de acoes sem interromper o fluxo do usuario.

## Examples

### Example 1: Google Workspace — Undo Toast
Google usa toasts com acao de desfazer:
- "Conversa arquivada. [Desfazer]"
- Posicao: bottom-center
- Auto-dismiss: 8 segundos
- Acao de undo como link inline
- Desaparece com animacao suave

### Example 2: Figma — Action Confirmation Toast
Figma confirma acoes com toasts minimos:
- "Component published successfully"
- Posicao: bottom-left (nao obstrui canvas)
- Auto-dismiss: 4 segundos
- Sem acao adicional (apenas confirmacao)
- Stacking: multiplos toasts empilham verticalmente

### Example 3: Slack — Rich Toast
Slack mostra toasts com mais contexto:
- Icone + mensagem + acao
- "Mensagem agendada para 14h. [Editar] [Cancelar]"
- Dismiss manual ou auto (10 segundos)
- Toasts de erro nao fazem auto-dismiss

## Analysis

Toasts eficazes:
- **Temporarios**: auto-dismiss em 4-10 segundos (exceto erros)
- **Nao bloqueantes**: nao cobrem conteudo critico
- **Acionaveis**: inclua undo quando acao e reversivel
- **Empilhaveis**: suporte a multiplos toasts (max 3 visiveis)
- **Acessiveis**: `role="status"` + `aria-live="polite"`
- **Nao criticos**: nunca use toast para informacao que o usuario PRECISA ver

## Tags

`toasts`, `snackbar`, `notifications`, `feedback`, `undo`, `a11y`
