# Banner Notification Patterns

## Pattern Description

Padroes para banners — notificacoes persistentes que comunicam informacoes importantes no topo ou dentro de secoes da pagina.

## Examples

### Example 1: GitHub — Security Alert Banner
GitHub alerta sobre vulnerabilidades com banners:
- Banner amarelo no topo do repositorio
- "1 Dependabot alert — View alerts"
- Persistente ate que usuario resolva ou dismiss
- Icone de atencao + texto + link de acao
- Nao bloqueia conteudo principal

### Example 2: Stripe — System Status Banner
Stripe comunica status do sistema:
- Banner azul/amarelo/vermelho conforme severidade
- "Elevated error rates on API — View status page"
- Posicao: topo do dashboard, acima da nav
- Atualizacao em tempo real
- Dismissavel mas retorna se situacao persiste

### Example 3: Notion — Feature Announcement
Notion anuncia features com banners sutis:
- Banner discreto abaixo do header
- "Novo: AI integrada ao Notion. [Experimentar]"
- Dismiss com X (nao mostra novamente)
- Design alinhado com identidade visual
- Link para mais informacoes

## Analysis

Banners eficazes:
- **Hierarquia visual**: cor indica severidade (info, warning, error, success)
- **Posicao**: topo da pagina para globais, inline para contextuais
- **Persistencia**: permanecem ate acao ou dismiss (diferentes de toasts)
- **Dismiss**: sempre ofereca opcao de fechar (exceto alertas criticos)
- **Concisao**: uma linha de texto + um CTA
- **Nao abuse**: no maximo 1 banner global visivel por vez

## Tags

`banners`, `notifications`, `alerts`, `system-status`, `announcements`
