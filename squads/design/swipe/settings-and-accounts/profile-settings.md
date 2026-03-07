# Profile Settings Patterns

## Pattern Description

Padroes para paginas de configuracao de perfil do usuario. Foco em facilidade de edicao, feedback claro de salvamento e organizacao logica dos campos.

## Examples

### Example 1: GitHub — Section-Based Settings
GitHub organiza perfil em secoes claras:
- Avatar com upload e crop inline
- Public profile: nome, bio, company, location
- Social accounts: links para redes sociais
- Cada secao com botao "Update profile" proprio
- Feedback toast apos salvar

### Example 2: Linear — Minimal Profile
Linear mantém perfil minimalista:
- Avatar + nome + email em um card unico
- Full name editavel inline
- Display name separado do username
- Timezone auto-detectado com override manual
- Theme preference (light/dark/system)

### Example 3: Notion — Connected Accounts
Notion foca em contas conectadas:
- Secao de login: email, password, 2FA
- Connected apps: Google, Slack, Figma
- Import data: de outras ferramentas
- Danger zone: delete account (separada visualmente)
- Cada secao colapsavel para reduzir scroll

## Analysis

Profile settings eficazes:
- **Auto-save vs explicit save**: auto-save para preferencias, explicit para dados criticos
- **Agrupamento**: organize por tema (identidade, seguranca, preferencias)
- **Feedback**: confirme salvamento com toast ou inline success
- **Danger zone**: acoes irreversiveis isoladas visualmente
- **Validation**: inline para email, nome, etc.
- **Responsive**: funcional em mobile com campos empilhados

## Tags

`settings`, `profile`, `account`, `preferences`, `inline-editing`, `auto-save`
