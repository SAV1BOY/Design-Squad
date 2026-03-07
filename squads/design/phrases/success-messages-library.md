# Success Messages Library

## Context

Biblioteca de mensagens de sucesso em PT-BR para confirmação de ações do usuário.
Mensagens de sucesso completam o ciclo de feedback — informam que a ação foi
realizada com sucesso e, quando aplicável, orientam o próximo passo. Devem ser
breves, positivas e não interruptivas.

**Aplicação:** Toasts, banners, telas de confirmação, inline feedback
**Tom:** User Advocate — positivo, breve, orientador

## Phrases

### Ações de CRUD
- **Criar:** "Item criado com sucesso." / "[Nome do item] foi criado."
- **Salvar:** "Alterações salvas." / "Suas alterações foram salvas."
- **Atualizar:** "Dados atualizados com sucesso."
- **Excluir:** "[Item] foi removido." / "Item excluído com sucesso."
- **Duplicar:** "Cópia criada com sucesso."
- **Mover:** "[Item] movido para [destino]."
- **Arquivar:** "[Item] foi arquivado. Desfazer"

### Ações de conta e perfil
- **Cadastro:** "Conta criada com sucesso. Bem-vindo!"
- **Login:** (geralmente não precisa de mensagem — redirecionar é suficiente)
- **Logout:** "Você saiu da sua conta."
- **Senha alterada:** "Senha alterada com sucesso. Use a nova senha no próximo login."
- **Email verificado:** "Email verificado com sucesso."
- **Perfil atualizado:** "Seu perfil foi atualizado."
- **Foto alterada:** "Foto de perfil atualizada."

### Ações de comunicação
- **Email enviado:** "Email enviado para [endereço]."
- **Convite enviado:** "Convite enviado para [nome/email]."
- **Mensagem enviada:** "Mensagem enviada com sucesso."
- **Feedback enviado:** "Obrigado pelo feedback. Ele nos ajuda a melhorar."
- **Report enviado:** "Denúncia recebida. Vamos analisar em até [N] horas."

### Ações transacionais
- **Pagamento aprovado:** "Pagamento aprovado. Seu pedido foi confirmado."
- **Pedido realizado:** "Pedido #[número] realizado com sucesso. Acompanhe o status em 'Meus Pedidos'."
- **Assinatura ativada:** "Assinatura ativada. Você já pode aproveitar todos os benefícios."
- **Cancelamento:** "Assinatura cancelada. Você ainda tem acesso até [data]."
- **Reembolso:** "Reembolso solicitado. O valor será devolvido em até [N] dias úteis."

### Ações de configuração
- **Notificações atualizadas:** "Preferências de notificação atualizadas."
- **Idioma alterado:** "Idioma alterado para [idioma]."
- **Tema alterado:** (mudança visual é o feedback — mensagem opcional)
- **Integração conectada:** "[Serviço] conectado com sucesso."
- **Integração desconectada:** "[Serviço] desconectado."

### Ações de upload e importação
- **Upload concluído:** "Arquivo enviado com sucesso."
- **Importação concluída:** "[N] itens importados com sucesso."
- **Exportação pronta:** "Seu arquivo está pronto para download."

### Ações com próximo passo
- **Cadastro com verificação:** "Conta criada. Enviamos um link de verificação para [email]."
- **Recuperação de senha:** "Enviamos instruções para redefinir sua senha para [email]."
- **Pedido com entrega:** "Pedido confirmado. Prazo de entrega: [data]. Acompanhe em 'Meus Pedidos'."
- **Publicação com review:** "Conteúdo enviado para revisão. Você será notificado quando for aprovado."

## Variations

### Formato toast (não intrusivo)
- Máximo 1 linha: "Alterações salvas."
- Auto-dismiss em 4-5 segundos
- Ação de desfazer quando aplicável: "Item excluído. Desfazer"

### Formato banner (mais contexto)
- Título + próximo passo: "Pedido confirmado. Acompanhe o status em Meus Pedidos."
- Dismiss manual quando contém informação importante

### Formato tela completa (ações importantes)
- Ilustração + título + descrição + CTA
- Usar para: cadastro completo, compra finalizada, onboarding concluído
- Exemplo: Ilustração de check / "Pedido realizado!" / "Seu pedido #1234..." / "Acompanhar pedido"

## When to Use

- Confirmação de qualquer ação do usuário que modifica dados
- Finalização de fluxos multi-step
- Feedback positivo após interações importantes
- Handoff de design com specs completos de estados de sucesso
