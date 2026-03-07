# Multi-Step Form Patterns

## Pattern Description

Padroes para formularios divididos em multiplas etapas. Reduzem carga cognitiva quebrando formularios complexos em passos gerenciaveis.

## Examples

### Example 1: TurboTax — Conversational Steps
TurboTax apresenta declaracao de impostos como conversa:
- Uma pergunta por tela (maximo 2-3 campos)
- Progresso visual (barra + "Step 3 of 12")
- Resumo revisavel antes de enviar
- Salvamento automatico entre passos
- Navegacao livre entre passos completados

### Example 2: Typeform — One Question at a Time
Typeform popularizou o padrao de uma pergunta por vez:
- Tela inteira para cada pergunta
- Transicao suave entre perguntas
- Keyboard-first (Enter para avancar)
- Progress bar minimalista no topo
- Logica condicional esconde perguntas irrelevantes

### Example 3: Shopify — Checkout Steps
Shopify Checkout usa stepper classico:
- 3 passos: Information, Shipping, Payment
- Stepper visual no topo com status de cada passo
- Validacao por passo antes de avancar
- Summary do pedido persistente na lateral
- Botao "Back" para revisar passos anteriores

## Analysis

Multi-step forms eficazes:
- **Progresso visivel**: stepper ou progress bar com total de passos
- **Agrupamento logico**: campos relacionados no mesmo passo
- **Salvamento**: auto-save ou save on step completion
- **Navegacao bidirecional**: voltar sem perder dados
- **Validacao por passo**: valide antes de permitir avancar
- **Resumo final**: revisao de todos os dados antes de submit

## Tags

`multi-step`, `forms`, `wizard`, `stepper`, `progressive-disclosure`, `checkout`
