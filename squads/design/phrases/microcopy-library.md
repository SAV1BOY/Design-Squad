# Microcopy Library

## Context

Biblioteca de microcopy reutilizável em PT-BR para componentes e padrões recorrentes
da interface. Cada frase foi avaliada por clareza, tom e adequação cultural para o
público brasileiro. Use como ponto de partida — adapte conforme o contexto específico.

**Aplicação:** Toda interface do produto — botões, labels, helpers, placeholders
**Tom:** User Advocate — claro, direto, respeitoso

## Phrases

### Labels de formulário
- "Nome completo" (não "Nome e sobrenome" — pode confundir nome do meio)
- "Email" (não "Endereço de email" — redundante)
- "Telefone com DDD" (explicitar formato esperado)
- "CPF (apenas números)" (indicar que não precisa de pontuação)
- "Data de nascimento" (não "Aniversário" — aniversário é a celebração)
- "Senha" / "Nova senha" / "Confirme a senha"
- "CEP" (não "Código postal" — brasileiros conhecem como CEP)

### Placeholders
- Email: "nome@exemplo.com"
- Telefone: "(11) 99999-9999"
- CPF: "000.000.000-00"
- CEP: "00000-000"
- Busca: "Buscar por nome, código ou categoria"
- Valor monetário: "R$ 0,00"

### Helper texts
- "Mínimo 8 caracteres, com pelo menos uma letra e um número"
- "Usamos seu email para login e comunicações importantes"
- "O CEP preenche automaticamente cidade e estado"
- "Esse dado aparece na nota fiscal"
- "Você pode alterar isso depois nas configurações"
- "Formato aceito: JPG, PNG ou PDF. Máximo 5MB"

### Botões de ação primária
- "Continuar" (fluxo multi-step — avançar)
- "Salvar" (persistir alterações)
- "Confirmar" (ação final — com consequência)
- "Enviar" (submeter formulário)
- "Criar conta" (não "Registrar" — mais natural em PT-BR)
- "Entrar" (não "Fazer login" — mais direto)
- "Buscar" (ação de search)
- "Aplicar" (filtros, configurações)

### Botões de ação secundária
- "Cancelar" (desistir da ação)
- "Voltar" (retornar ao passo anterior)
- "Pular" (skip step opcional)
- "Depois" (adiar ação não obrigatória)
- "Descartar alterações" (confirmar perda de dados)
- "Ver detalhes" (expandir informação)

### Links de ação
- "Esqueceu a senha?" (não "Recuperar senha" — mais conversacional)
- "Saiba mais" (link para informação complementar)
- "Ver todos" (lista com mais itens disponíveis)
- "Editar" (modificar item existente)
- "Remover" (deletar item — confirmar antes)

### Feedback de sistema
- Loading: "Carregando..." / "Processando..." / "Quase pronto..."
- Salvando: "Salvando alterações..." / "Suas alterações foram salvas"
- Sincronizando: "Sincronizando dados..." / "Tudo atualizado"
- Upload: "Enviando arquivo..." / "Arquivo enviado com sucesso"

## Variations

### Formal (institucional, contratos)
- "Prosseguir" ao invés de "Continuar"
- "Concordo com os termos" ao invés de "Li e aceito"
- "Finalizar cadastro" ao invés de "Criar conta"

### Conciso (mobile, espaço limitado)
- "Salvar" ao invés de "Salvar alterações"
- "OK" ao invés de "Entendi" (quando espaço é crítico)
- "Pronto" ao invés de "Tudo certo, suas alterações foram salvas"

### Acessível (screen readers)
- Botões com aria-label descritivo: aria-label="Remover produto Camiseta Azul do carrinho"
- Links com contexto: "Saiba mais sobre planos de assinatura" (não apenas "Saiba mais")
- Loading com aria-live="polite": "Carregando lista de produtos"

## When to Use

- Criação de novas interfaces e componentes
- Revisão de microcopy existente para consistência
- Handoff de design para desenvolvimento (referência de copy)
- Testes de usabilidade (validar compreensão)
- Localização de interfaces para PT-BR
