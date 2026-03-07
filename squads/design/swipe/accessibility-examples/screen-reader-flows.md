# Screen Reader Flow Examples

## Pattern Description

Exemplos de fluxos otimizados para screen readers (leitores de tela). Foco em semantic HTML, ARIA, live regions e anuncios apropriados.

## Examples

### Example 1: GOV.UK — Exemplar Screen Reader UX
GOV.UK e benchmark global de screen reader UX:
- HTML semantico: headings, lists, landmarks em toda pagina
- Form errors anunciados com `aria-live` region
- Progress em multi-step forms anunciado a cada passo
- Link text descritivo (nunca "clique aqui")
- Tabelas com headers associados via `scope`

### Example 2: Slack — Dynamic Content Updates
Slack anuncia atualizacoes em tempo real:
- Novas mensagens anunciadas via `aria-live="polite"`
- Typing indicators: "Ana esta digitando..."
- Channel switch anunciado com nome do canal
- Reacoes em mensagens anunciadas contextualmente
- Notificacoes lidas via screen reader sem interacao visual

### Example 3: GitHub — Code Review Accessibility
GitHub tornou code review acessivel:
- Diff navigation por teclado entre hunks
- Comentarios inline acessiveis com landmarks
- File tree com `role="tree"` e `role="treeitem"`
- Status checks anunciados via live region
- Markdown rendered com semantica HTML correta

## Analysis

Screen reader flows eficazes:
- **Semantic HTML first**: use elementos nativos antes de ARIA
- **Landmarks**: `<nav>`, `<main>`, `<aside>`, `<header>`, `<footer>`
- **Headings hierarchy**: h1 > h2 > h3 sem pular niveis
- **Live regions**: `aria-live` para conteudo dinamico
- **Labels**: todo controle interativo com label acessivel
- **Testing**: teste com NVDA (Windows), VoiceOver (Mac), TalkBack (Android)

## Tags

`screen-reader`, `a11y`, `aria`, `semantic-html`, `live-regions`, `voiceover`
