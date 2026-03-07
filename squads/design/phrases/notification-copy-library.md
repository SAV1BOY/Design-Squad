# Notification Copy Library

## Context

Biblioteca de copy para notificações — push, in-app, email e SMS. Notificações são
interrupções no fluxo do usuário, portanto devem ser relevantes, concisas e
acionáveis. Cada notificação compete com dezenas de outras pela atenção do usuário.

Regra de ouro: se o usuário desativaria essa notificação, provavelmente não deveria
existir. Notificações devem criar valor, não irritação.

**Aplicação:** Push notifications, in-app notifications, notification center, emails transacionais
**Tom:** User Advocate — relevante, conciso, acionável

## Phrases

### Transacionais (ação do próprio usuário)
- **Pedido confirmado:** "Pedido #[número] confirmado. Entrega prevista: [data]."
- **Pagamento aprovado:** "Pagamento de R$ [valor] aprovado no cartão final [XXXX]."
- **Envio realizado:** "Seu pedido saiu para entrega. Acompanhe: [link]."
- **Entrega realizada:** "Pedido #[número] entregue. Tudo certo? Conte para a gente."
- **Senha alterada:** "Sua senha foi alterada. Se não foi você, entre em contato imediatamente."
- **Cadastro concluído:** "Bem-vindo ao [Produto]. Sua conta está pronta."
- **Assinatura renovada:** "Sua assinatura foi renovada até [data]. Valor: R$ [valor]."

### Informativas (atualizações do sistema)
- **Nova feature:** "[Feature] está disponível. [Benefício em 1 frase]. Experimente."
- **Manutenção programada:** "Manutenção em [data] das [hora] às [hora]. O serviço pode ficar instável."
- **Atualização de termos:** "Atualizamos nossos termos de uso. Veja o que mudou."
- **Nova versão:** "Versão [X.Y] disponível com [melhoria principal]. Atualize agora."

### Sociais (ações de outros usuários)
- **Novo seguidor:** "[Nome] começou a seguir você."
- **Curtida:** "[Nome] curtiu seu [item]."
- **Comentário:** "[Nome] comentou em [item]: '[preview do comentário]'."
- **Menção:** "[Nome] mencionou você em [contexto]."
- **Convite:** "[Nome] te convidou para [espaço/time/projeto]."
- **Compartilhamento:** "[Nome] compartilhou [item] com você."

### Alertas e urgências
- **Segurança:** "Detectamos um login incomum em [localização]. Foi você? [Sim/Não]."
- **Expiração:** "Seu plano expira em [N] dias. Renove para não perder acesso."
- **Limite:** "Você atingiu [X]% do seu limite de [recurso]. Veja opções de upgrade."
- **Falha:** "Não conseguimos processar seu pagamento. Atualize seus dados."
- **Inatividade:** "Faz [N] dias que você não acessa. [Motivo para voltar]."

### Promoções e engajamento (usar com moderação)
- **Desconto:** "[X]% de desconto em [categoria]. Válido até [data]."
- **Recomendação:** "Baseado no que você gosta: [item]. Confira."
- **Milestone:** "Parabéns! Você completou [N] [ações] no [Produto]."
- **Inatividade positiva:** "Sentimos sua falta. [Novidade relevante] desde sua última visita."

### Notificações agrupadas
- "[Nome] e mais [N] pessoas curtiram seu [item]."
- "Você tem [N] novas mensagens de [Nome 1] e [Nome 2]."
- "[N] novos items foram adicionados a [coleção/lista] que você segue."
- "[N] atualizações no [projeto/espaço] desde sua última visita."

## Variations

### Por canal
- **Push (mobile):** Max 2 linhas. Título bold + descrição. Deep link para ação.
- **In-app:** Ícone + título + descrição + timestamp. Ação on click.
- **Email transacional:** Subject conciso + corpo com detalhes + CTA button.
- **SMS:** Max 160 caracteres. Essencial + link curto.

### Por urgência
- **Alta:** Usar imediatamente. Ex: segurança, falha de pagamento.
- **Média:** Dentro de 24h. Ex: entrega, prazo expirando.
- **Baixa:** Batch (agrupar). Ex: sociais, recomendações.

### Acessibilidade
- Notificações in-app devem usar aria-live="polite" para screen readers
- Push notifications devem funcionar com VoiceOver/TalkBack
- Não depender apenas de cor para comunicar urgência

## When to Use

- Design de sistema de notificações e alertas
- Revisão de copy de notificações existentes
- Definição de estratégia de notificações por canal
- Handoff com specs de todos os tipos de notificação
- Testes com usuários sobre fadiga de notificação
