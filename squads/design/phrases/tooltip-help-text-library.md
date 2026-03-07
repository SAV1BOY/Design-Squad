# Tooltip & Help Text Library

## Context

Biblioteca de tooltips e textos de ajuda contextual em PT-BR. Tooltips e help texts
são a camada de suporte da interface — aparecem quando o usuário precisa de contexto
adicional sem sair do fluxo. Devem ser breves, informativos e não repetir o que já
está visível na tela.

Princípio: se o tooltip é necessário para entender a interface, a interface precisa
ser redesenhada. Tooltips complementam, não substituem boa UX.

**Aplicação:** Tooltips, helper texts, info icons, contextual help
**Tom:** User Advocate — informativo, breve, contextual

## Phrases

### Tooltips para ícones de ação
- Ícone de editar: "Editar [item]"
- Ícone de excluir: "Excluir [item]"
- Ícone de copiar: "Copiar para a área de transferência"
- Ícone de compartilhar: "Compartilhar [item]"
- Ícone de download: "Baixar [item]"
- Ícone de filtro: "Filtrar resultados"
- Ícone de configurações: "Configurações"
- Ícone de notificações: "Notificações ([N] novas)"
- Ícone de ajuda: "Ajuda"
- Ícone de fechar: "Fechar"

### Tooltips informativos (ícone de info "i")
- **Campo de CPF:** "Usamos o CPF para identificação fiscal e emissão de nota."
- **Campo de email secundário:** "Email alternativo para recuperação de conta."
- **Toggle de notificações:** "Ativando, você recebe alertas sobre [tipo de conteúdo]."
- **Badge de verificado:** "Identidade verificada por [método]."
- **Indicador de status:** "Online: ativo nos últimos 5 minutos."
- **Selo de segurança:** "Conexão protegida com criptografia de ponta a ponta."
- **Indicador de força de senha:** "Senhas fortes combinam letras, números e caracteres especiais."
- **Preço anterior:** "Preço original antes do desconto."
- **Data de expiração:** "Após essa data, o [item/oferta] não estará mais disponível."
- **Limite de uso:** "Você usou [N] de [M] disponíveis neste período."

### Helper texts para formulários
- **Nome de usuário:** "Será visível para outros usuários. Use entre 3 e 20 caracteres."
- **Bio/Descrição:** "Máximo [N] caracteres. Conte um pouco sobre você ou sua empresa."
- **URL personalizada:** "Será o endereço do seu perfil: [domínio]/[username]"
- **Valor monetário:** "Insira o valor em reais. Centavos separados por vírgula."
- **Data:** "Formato: DD/MM/AAAA"
- **Telefone internacional:** "Inclua o código do país. Ex: +55 11 99999-9999"
- **Código promocional:** "Insira o código e clique em Aplicar para ver o desconto."
- **Campo de busca avançada:** "Use aspas para busca exata. Ex: 'design system'"

### Tooltips para métricas e dashboards
- **NPS:** "Net Promoter Score: mede a probabilidade de recomendação. Escala de -100 a 100."
- **Taxa de conversão:** "Percentual de visitantes que completaram a ação desejada."
- **Bounce rate:** "Percentual de visitas com apenas 1 página visualizada."
- **Tempo médio:** "Média de tempo que os usuários passam nesta página."
- **Tendência:** "Comparado com o mesmo período anterior."
- **Meta:** "Linha pontilhada indica a meta definida para este período."

### Tooltips para estados e badges
- **Draft:** "Rascunho — visível apenas para você."
- **Em revisão:** "Aguardando aprovação de [pessoa/time]."
- **Publicado:** "Visível para [público]."
- **Arquivado:** "Removido da listagem, mas não excluído."
- **Expirado:** "Não está mais ativo. [Ação possível: renovar/recriar]."
- **Destaque:** "Item fixado no topo da lista."

### Contextual help (help panels, sidebars)
- **O que é [feature]:** "[Feature] permite que você [benefício principal]. [Link para doc completa]."
- **Como funciona:** "1. [Passo]. 2. [Passo]. 3. [Passo]. Precisa de mais ajuda? [Link]."
- **Atalhos de teclado:** "Ctrl+S: Salvar / Ctrl+Z: Desfazer / Ctrl+K: Buscar / ?: Ver todos os atalhos"

## Variations

### Formato por tipo
- **Tooltip simples:** 1 frase, max 80 caracteres, aparece on hover/focus
- **Tooltip rico:** Título + descrição + link opcional, aparece on click
- **Helper text:** Abaixo do campo, sempre visível, max 2 linhas
- **Contextual help:** Painel lateral ou popover com conteúdo extenso

### Acessibilidade
- Tooltips devem ser acessíveis via focus (não apenas hover)
- Conteúdo de tooltip deve ser anunciado via aria-describedby
- Helper text vinculado ao campo via aria-describedby="[id]"
- Tooltips não devem conter ações — apenas informação

## When to Use

- Design de interfaces com campos ou ações que precisam de contexto
- Revisão de tooltips existentes para clareza e consistência
- Handoff com specs de microcopy contextual
- Dashboards e interfaces com métricas que precisam de explicação
