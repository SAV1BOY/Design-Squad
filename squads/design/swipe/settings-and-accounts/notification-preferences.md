# Notification Preferences Patterns

## Pattern Description

Padroes para configuracao de preferencias de notificacao. Usuarios devem ter controle granular sobre o que recebem e por qual canal, sem complexidade excessiva.

## Examples

### Example 1: GitHub — Matrix Control
GitHub usa matriz tipo x canal:
- Linhas: tipos de notificacao (Issues, PRs, Releases, Security)
- Colunas: canais (Email, Web, Mobile)
- Toggle por celula da matriz
- Agrupamento por repositorio/organizacao
- Custom routing rules para power users

### Example 2: Slack — Channel-Level Control
Slack permite controle por canal e workspace:
- Mute de canais individuais
- Notification schedule (Do Not Disturb)
- Keywords para highlight (mencionam seu nome/termo)
- Device-specific settings (desktop vs mobile)
- Sound and appearance customization

### Example 3: Linear — Simple Toggles
Linear simplifica com categorias claras:
- Inbox notifications: on/off por tipo
- Email digest: daily/weekly/never
- Desktop notifications: all/mentions/none
- Mobile push: same as desktop or custom
- Cada toggle com descricao do que controla

## Analysis

Notification preferences eficazes:
- **Defaults sensatos**: comece com defaults razoaveis, nao "tudo ligado"
- **Granularidade progressiva**: simple toggles primeiro, advanced depois
- **Preview**: mostre exemplo de cada tipo de notificacao
- **Do Not Disturb**: schedule configuravel
- **Channel control**: email, push, in-app separadamente
- **Unsubscribe facil**: link em cada email para ajustar preferencias

## Tags

`notifications`, `preferences`, `settings`, `email`, `push`, `dnd`
