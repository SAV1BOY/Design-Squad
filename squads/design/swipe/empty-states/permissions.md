# Permission Empty State Patterns

## Pattern Description

Padroes para estados de permissao negada — quando o usuario nao tem acesso ao conteudo solicitado. Devem ser informativos sem expor detalhes de seguranca.

## Examples

### Example 1: Google Drive — Request Access
Google Drive oferece fluxo de solicitacao:
- "Voce precisa de acesso"
- Nome do owner do documento (quando disponivel)
- Botao "Solicitar acesso" que envia email ao owner
- Mensagem opcional para justificar o pedido
- Confirmacao "Solicitacao enviada" apos request

### Example 2: Notion — Workspace Gate
Notion diferencia tipos de restricao:
- Pagina privada: "Esta pagina e privada"
- Workspace diferente: "Esta pagina pertence a outro workspace"
- Link expirado: "Este link de compartilhamento expirou"
- Cada cenario com CTA apropriado

### Example 3: GitHub — Private Repository
GitHub mostra contexto para repos privados:
- "404 — This is not the page you are looking for"
- Nao confirma se o repo existe (seguranca)
- Sugere verificar URL ou fazer login
- Link para documentacao de permissoes

## Analysis

Permission empty states eficazes:
- **Seguranca**: nao confirme existencia de recurso para usuarios nao autorizados
- **Caminho claro**: ofereça acao (solicitar acesso, login, contatar admin)
- **Contexto**: explique por que o acesso e restrito quando seguro
- **Diferenciacao**: distingua "nao logado" de "sem permissao"
- **Sem culpa**: tom neutro, sem implicar que o usuario fez algo errado

## Tags

`permissions`, `empty-states`, `access-control`, `security`, `authorization`
