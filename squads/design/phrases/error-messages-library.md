# Error Messages Library

## Context

Biblioteca de mensagens de erro em PT-BR para situações recorrentes na interface.
Mensagens de erro são o momento mais crítico da comunicação com o usuário — quando
algo deu errado, a clareza e empatia da mensagem determinam se o usuário persiste
ou abandona.

Princípio fundamental: toda mensagem de erro deve dizer (1) o que aconteceu,
(2) por que aconteceu (se relevante), e (3) como resolver.

**Aplicação:** Formulários, fluxos transacionais, estados de erro, sistema
**Tom:** User Advocate — claro, empático, acionável

## Phrases

### Erros de formulário — Campos
- **Email inválido:** "Esse email não parece correto. Verifique se tem @ e um domínio (ex: nome@exemplo.com)."
- **CPF inválido:** "O CPF precisa ter 11 dígitos. Confira e tente novamente."
- **CEP não encontrado:** "Não encontramos esse CEP. Verifique o número e tente novamente."
- **Campo obrigatório:** "Esse campo é obrigatório." (não "Preencha este campo")
- **Senha curta:** "A senha precisa ter pelo menos 8 caracteres."
- **Senha fraca:** "Adicione pelo menos uma letra maiúscula e um número para fortalecer sua senha."
- **Senhas não coincidem:** "As senhas não coincidem. Verifique e tente novamente."
- **Telefone inválido:** "O telefone precisa ter DDD + 9 dígitos (ex: 11 999999999)."
- **Valor mínimo:** "O valor mínimo é R$ [valor]."
- **Limite de caracteres:** "Máximo de [N] caracteres. Você usou [M]."

### Erros de formulário — Validação
- **Email já cadastrado:** "Esse email já tem uma conta. Tente fazer login ou use outro email."
- **CPF já cadastrado:** "Esse CPF já está vinculado a uma conta. Precisa de ajuda? Fale com o suporte."
- **Username indisponível:** "Esse nome de usuário já está em uso. Que tal [sugestão 1] ou [sugestão 2]?"
- **Data inválida:** "Essa data não é válida. Use o formato DD/MM/AAAA."
- **Data futura não permitida:** "A data de nascimento não pode ser no futuro."

### Erros de autenticação
- **Login incorreto:** "Email ou senha incorretos. Verifique seus dados e tente novamente."
- **Conta bloqueada:** "Sua conta foi bloqueada temporariamente por segurança. Tente novamente em [N] minutos."
- **Sessão expirada:** "Sua sessão expirou. Faça login novamente para continuar."
- **Token expirado:** "O link expirou. Solicite um novo para continuar."
- **Sem permissão:** "Você não tem permissão para acessar essa página. Fale com o administrador."

### Erros de pagamento
- **Cartão recusado:** "O pagamento não foi aprovado. Verifique os dados do cartão ou tente outra forma de pagamento."
- **Cartão expirado:** "Esse cartão está vencido. Atualize a data de validade ou use outro cartão."
- **Saldo insuficiente:** "O pagamento não foi aprovado. Verifique o saldo ou tente outro cartão."
- **Transação duplicada:** "Esse pagamento já foi processado. Verifique seu extrato antes de tentar novamente."
- **Timeout de pagamento:** "O pagamento não pôde ser confirmado. Nenhum valor foi cobrado. Tente novamente."

### Erros de sistema
- **Erro genérico:** "Algo deu errado. Tente novamente. Se o problema persistir, fale com o suporte."
- **Servidor indisponível:** "O serviço está temporariamente indisponível. Tente novamente em alguns minutos."
- **Timeout:** "A conexão demorou mais que o esperado. Verifique sua internet e tente novamente."
- **Sem conexão:** "Sem conexão com a internet. Verifique sua rede e tente novamente."
- **Manutenção:** "Estamos em manutenção programada. Voltamos às [hora]. Pedimos desculpa pelo inconveniente."
- **Limite excedido:** "Muitas tentativas em pouco tempo. Aguarde [N] minutos e tente novamente."

### Erros de upload
- **Formato não suportado:** "Formato não suportado. Use JPG, PNG ou PDF."
- **Arquivo muito grande:** "O arquivo excede o limite de [N]MB. Reduza o tamanho e tente novamente."
- **Upload falhou:** "O envio do arquivo falhou. Verifique sua conexão e tente novamente."

## Variations

### Formato curto (mobile, espaço limitado)
- "Email inválido" + helper text com formato esperado
- "Campo obrigatório"
- "Senha muito curta"

### Formato acessível (screen readers)
- Prefixar com role="alert" para anúncio automático
- Incluir instrução de correção, não apenas o erro
- Referenciar o campo: "Erro no campo Email: formato inválido"

## When to Use

- Implementação de formulários e fluxos transacionais
- Revisão de microcopy de mensagens de erro existentes
- Handoff de design com specs de estados de erro
- Testes de usabilidade focados em recuperação de erro
