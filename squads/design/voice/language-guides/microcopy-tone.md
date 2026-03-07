# Microcopy Tone

## Context

Guia de tom para microcopy — os pequenos textos que guiam o usuário durante a interação
com o produto: labels, placeholders, mensagens de erro, tooltips, empty states, botões,
notificações e textos de ajuda. Microcopy é a voz do produto falando diretamente com
o usuário, e cada palavra conta.

Microcopy eficaz é invisível — o usuário completa a tarefa sem perceber que foi guiado.
Microcopy ruim causa fricção, confusão e frustração.

**Aplicação:** Toda interface do produto.
**Tom predominante:** User Advocate + Pragmatic Builder
**Idioma do conteúdo:** Português brasileiro (PT-BR)
**Frequência:** Contínua — cada tela tem microcopy

## Do's

### Ser claro e direto
- "Salvar alterações" ao invés de "Submeter modificações realizadas"
- "Email ou telefone" ao invés de "Insira suas credenciais de identificação"
- "Voltar" ao invés de "Retornar à página anterior"

### Usar linguagem do usuário
- "Foto de perfil" ao invés de "Avatar"
- "Endereço de entrega" ao invés de "Endereço de shipping"
- "Forma de pagamento" ao invés de "Método de transação"

### Dar contexto suficiente sem excesso
- Placeholder: "nome@exemplo.com" (mostra o formato esperado)
- Helper text: "Mínimo 8 caracteres, com letra e número"
- Tooltip: "Esse valor aparece na nota fiscal"

### Mensagens de erro que ajudam
- "O CPF precisa ter 11 dígitos" ao invés de "Campo inválido"
- "Essa senha é muito curta. Use pelo menos 8 caracteres" ao invés de "Erro"
- "Não encontramos esse CEP. Verifique e tente novamente" ao invés de "CEP inválido"

### Manter consistência de tratamento
- Sempre "você" (não alternar entre tu/você/o senhor)
- Tom conversacional mas respeitoso
- Sem gírias, mas sem formalidade excessiva

## Don'ts

### Linguagem técnica ou jargão
- "Ocorreu um erro 500 no servidor" — o usuário não precisa saber disso
- "Timeout na requisição" — dizer "Demorou mais que o esperado. Tente novamente"
- "Null reference exception" — dizer "Algo deu errado. Estamos trabalhando nisso"

### Tom condescendente ou infantilizado
- "Opa! Parece que você errou!" — não culpar o usuário
- "Ei, calma aí!" — não ser informal demais em erros
- "Isso é facinho!" — não minimizar a dificuldade do usuário

### Mensagens genéricas que não ajudam
- "Erro" — sem contexto
- "Ação não permitida" — sem explicar por quê
- "Tente novamente mais tarde" — sem dizer quando

### Excesso de texto
- Parágrafos longos em tooltips
- Instruções de 5 linhas em placeholders
- Modais com mais texto que uma landing page

### Humor em momentos inapropriados
- Piada em mensagem de erro de pagamento
- Trocadilho em alerta de segurança
- Emoji excessivo em contextos sérios

## Templates

### Template de mensagem de erro
```
[O que aconteceu]. [Como resolver].
Exemplo: "O email já está cadastrado. Tente fazer login ou use outro email."
```

### Template de empty state
```
[Título — o que deveria estar aqui]
[Descrição — por que está vazio e o que fazer]
[CTA — ação para resolver]
```

### Template de confirmação
```
[O que vai acontecer]
[Consequência — se irreversível]
[Botão primário: ação afirmativa] [Botão secundário: cancelar]
```

### Template de sucesso
```
[O que foi concluído com sucesso]
[Próximo passo — se aplicável]
```

### Template de loading/progress
```
[O que está acontecendo]
[Estimativa de tempo — se possível]
```
