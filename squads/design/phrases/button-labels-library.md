# Button Labels Library

## Context

Biblioteca de labels para botões em PT-BR, organizados por tipo de ação e contexto.
O label de um botão é a microcopy mais crítica da interface — deve comunicar
exatamente o que vai acontecer quando clicado, em no máximo 3 palavras idealmente.

Princípios: verbo de ação + objeto (quando necessário). "Salvar" é suficiente.
"Clique aqui para salvar" é redundante.

**Aplicação:** Buttons, CTAs, links de ação em toda a interface
**Tom:** Pragmatic Builder — claro, direto, sem ambiguidade

## Phrases

### Ações primárias (criar, avançar, confirmar)
- "Criar" / "Criar [item]" — iniciar algo novo
- "Continuar" — avançar no fluxo (não "Próximo" — confuso sem contexto)
- "Confirmar" — ação final com consequência
- "Enviar" — submeter formulário ou mensagem
- "Salvar" — persistir alterações
- "Publicar" — tornar público
- "Concluir" — finalizar processo multi-step
- "Começar" — iniciar fluxo ou onboarding
- "Aceitar" — concordar com termos ou convite
- "Aplicar" — aplicar filtros ou configurações

### Ações secundárias (cancelar, voltar, descartar)
- "Cancelar" — desistir da ação (sem consequência)
- "Voltar" — retornar ao passo anterior
- "Fechar" — fechar modal ou painel
- "Pular" — ignorar passo opcional
- "Depois" — adiar ação não urgente
- "Descartar" — descartar alterações não salvas
- "Desfazer" — reverter última ação

### Ações destrutivas (excluir, remover)
- "Excluir" — deletar permanentemente
- "Remover" — tirar de uma lista/grupo (não deleta)
- "Desativar" — tornar inativo sem excluir
- "Cancelar assinatura" — encerrar plano
- "Sair" — logout
- "Desconectar" — remover integração

### Ações de navegação
- "Ver detalhes" — expandir informação
- "Ver todos" — mostrar lista completa
- "Saiba mais" — informação complementar
- "Expandir" / "Recolher" — toggle de conteúdo
- "Voltar ao início" — retornar à home
- "Ir para [destino]" — navegação explícita

### Ações de edição
- "Editar" — entrar em modo de edição
- "Editar perfil" — edição de contexto específico
- "Alterar" — trocar algo (ex: "Alterar senha")
- "Atualizar" — refresh de dados ou update de informação
- "Renomear" — mudar nome/título
- "Mover para" — reorganizar item
- "Duplicar" — criar cópia

### Ações de comunicação
- "Enviar mensagem" — compor e enviar
- "Responder" — reply
- "Encaminhar" — forward
- "Convidar" — enviar convite
- "Compartilhar" — share
- "Copiar link" — clipboard

### Ações de upload e download
- "Fazer upload" / "Enviar arquivo" — upload
- "Baixar" / "Download" — download (ambos aceitos em PT-BR)
- "Exportar" — gerar arquivo para download
- "Importar" — trazer dados de fonte externa

### Ações de filtro e busca
- "Buscar" — executar busca
- "Filtrar" — aplicar filtros
- "Limpar filtros" — resetar filtros
- "Ordenar por" — sorting
- "Aplicar filtros" — confirmar seleção de filtros

## Variations

### Contexto determina o label
- Genérico: "Salvar" → Específico: "Salvar rascunho" / "Salvar e publicar"
- Genérico: "Enviar" → Específico: "Enviar convite" / "Enviar feedback"
- Genérico: "Criar" → Específico: "Criar projeto" / "Criar equipe"

### Confirmação de ação destrutiva
- Botão de trigger: "Excluir"
- Modal de confirmação: "Sim, excluir" / "Cancelar"
- Nunca: "Sim" / "Não" (ambíguo — sim o quê?)

### Button com estado de loading
- Default: "Salvar" → Loading: "Salvando..." → Sucesso: "Salvo"
- Default: "Enviar" → Loading: "Enviando..." → Sucesso: "Enviado"
- Default: "Criar conta" → Loading: "Criando..." → Sucesso: (redirect)

### Acessibilidade
- Botões de ícone precisam de aria-label: aria-label="Excluir item [nome]"
- Botões genéricos precisam de contexto: aria-label="Ver detalhes do pedido #1234"
- Toggle buttons: aria-pressed="true/false"

## When to Use

- Design de novas interfaces — referência rápida para labels consistentes
- Revisão de consistência de labels entre diferentes telas
- Handoff para desenvolvimento com copy definida
- Tradução e localização de interfaces para PT-BR
