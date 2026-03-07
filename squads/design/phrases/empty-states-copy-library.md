# Empty States Copy Library

## Context

Biblioteca de copy para empty states — telas ou seções sem conteúdo para exibir.
Empty states são oportunidades de design: em vez de espaço vazio, orientam o usuário
sobre o que fazer. Um bom empty state comunica (1) o que deveria estar aqui,
(2) por que está vazio, e (3) como resolver.

**Aplicação:** Listas vazias, buscas sem resultado, primeira vez de uso, estados filtrados
**Tom:** User Advocate — orientador, encorajador, acionável

## Phrases

### Primeira vez de uso (onboarding)
- **Lista de favoritos:**
  Título: "Seus favoritos aparecem aqui"
  Descrição: "Toque no coração em qualquer item para salvar e encontrar facilmente depois."
  CTA: "Explorar catálogo"

- **Carrinho vazio:**
  Título: "Seu carrinho está vazio"
  Descrição: "Adicione produtos para começar sua compra."
  CTA: "Ver produtos"

- **Notificações:**
  Título: "Nenhuma notificação ainda"
  Descrição: "Quando houver novidades sobre seus pedidos ou promoções, você verá aqui."
  CTA: (nenhum — não há ação possível)

- **Histórico de pedidos:**
  Título: "Você ainda não fez nenhum pedido"
  Descrição: "Seus pedidos e status de entrega aparecerão aqui."
  CTA: "Começar a comprar"

- **Lista de projetos:**
  Título: "Nenhum projeto ainda"
  Descrição: "Crie seu primeiro projeto para começar a organizar seu trabalho."
  CTA: "Criar projeto"

- **Dashboard vazio:**
  Título: "Seu dashboard está em branco"
  Descrição: "Adicione widgets para acompanhar as métricas que importam para você."
  CTA: "Personalizar dashboard"

### Busca sem resultado
- **Busca genérica:**
  Título: "Nenhum resultado para '[termo]'"
  Descrição: "Verifique a ortografia ou tente termos mais gerais."
  CTA: "Limpar busca"

- **Busca com filtros:**
  Título: "Nenhum resultado com esses filtros"
  Descrição: "Tente remover alguns filtros para ampliar a busca."
  CTA: "Limpar filtros"

- **Busca de pessoa/contato:**
  Título: "Nenhuma pessoa encontrada"
  Descrição: "Verifique o nome ou email e tente novamente."
  CTA: "Convidar pessoa"

### Lista filtrada sem resultado
- **Filtro de status:**
  Título: "Nenhum item com status '[status]'"
  Descrição: "Não há itens com esse filtro no momento."
  CTA: "Ver todos os itens"

- **Filtro de data:**
  Título: "Nenhuma atividade nesse período"
  Descrição: "Tente selecionar um período maior."
  CTA: "Últimos 30 dias"

### Conteúdo removido ou expirado
- **Item removido:**
  Título: "Este item não está mais disponível"
  Descrição: "Pode ter sido removido ou movido. Tente buscar novamente."
  CTA: "Voltar"

- **Link expirado:**
  Título: "Este link expirou"
  Descrição: "Solicite um novo link para continuar."
  CTA: "Solicitar novo link"

### Erro que resulta em vazio
- **Falha ao carregar:**
  Título: "Não conseguimos carregar o conteúdo"
  Descrição: "Verifique sua conexão e tente novamente."
  CTA: "Tentar novamente"

- **Sem permissão:**
  Título: "Você não tem acesso a esse conteúdo"
  Descrição: "Solicite acesso ao administrador do espaço."
  CTA: "Solicitar acesso"

## Variations

### Tom por contexto
- **Onboarding:** Encorajador e orientador — "Comece por aqui"
- **Busca vazia:** Prático e útil — "Tente isso"
- **Erro:** Empático e direto — "Algo deu errado, aqui está como resolver"
- **Conteúdo expirado:** Informativo e redirecional — "Isso mudou, vá para cá"

### Formato por plataforma
- **Desktop:** Título + descrição (2 linhas) + CTA button + ilustração
- **Mobile:** Título + descrição (1 linha) + CTA link + ícone simples
- **Componente inline:** Apenas texto + link de ação (sem ilustração)

## When to Use

- Design de novas features que incluem listas ou coleções
- Revisão de empty states existentes para melhoria de UX
- Handoff com specs completos de todos os estados
- Testes de usabilidade para validar compreensão do empty state
