# Slack Design Comms

## Context

Adaptação de voz para comunicação do Design Squad no Slack — o canal mais frequente
e informal de comunicação do dia a dia. Slack é síncrono-assíncrono: pode ser lido
em tempo real ou horas depois. Isso exige que mensagens sejam auto-contidas e
scannable, mesmo sem o contexto verbal.

**Canal:** Slack (canais internos e cross-team)
**Audiência:** Varia por canal — time design, cross-funcional, all-hands
**Formalidade:** Nível 1-2 (Casual a Profissional Relaxado)
**Tom:** Pragmatic Builder + Creative Explorer

## Channel Strategy

### #design-squad (interno)
- **Propósito:** Comunicação interna do time de design
- **Tom:** Casual, direto, colaborativo
- **Conteúdo:** Updates rápidos, pedidos de pair, compartilhamento de referências
- **Regra:** Threaded conversations para manter o canal limpo

### #design-reviews (cross-team)
- **Propósito:** Compartilhar trabalho para feedback assíncrono
- **Tom:** Profissional relaxado, estruturado
- **Conteúdo:** Links de Figma com contexto, pedidos específicos de feedback
- **Regra:** Sempre incluir: contexto, link, tipo de feedback desejado

### #design-system (cross-team)
- **Propósito:** Updates e discussões sobre design system
- **Tom:** Profissional, técnico quando necessário
- **Conteúdo:** Releases, breaking changes, novas componentes, deprecations
- **Regra:** Tag de severidade para changes que afetam outros times

### #general ou canais de produto
- **Propósito:** Comunicação do design com audiência ampla
- **Tom:** Profissional relaxado, acessível, sem jargão
- **Conteúdo:** Celebrações, compartilhamento de resultados, pedidos de input
- **Regra:** Traduzir termos de design para linguagem comum

## Message Formatting

### Update de status
```
*[Feature Name]* — Status update
Estado: [Em andamento / Review / Entregue]
O que foi feito: [1-2 pontos]
Próximo passo: [ação]
Bloqueio: [se houver, tag a pessoa relevante]
```

### Pedido de feedback
```
Preciso de feedback sobre [feature/tela]:
Link: [Figma link direto para o frame]
Contexto: [1-2 frases]
Foco: [O que especificamente quer feedback]
Prazo: [Até quando precisa]
```

### Anúncio de release de design system
```
*DS Release v[X.Y.Z]*
Novidades:
• [Componente/Token] — [descrição curta]
• [Componente/Token] — [descrição curta]
Breaking changes: [sim/não — se sim, detalhar em thread]
Migration guide: [link]
Storybook: [link]
```

### Compartilhamento de referência/inspiração
```
Referência interessante para [contexto]:
[Link ou imagem]
O que achei relevante: [1-2 frases]
Aplicação para nós: [como podemos usar]
```

## Slack Etiquette

### Do's
- Usar threads para manter canais limpos
- Reagir com emoji para confirmar leitura (evita "ok" como mensagem)
- Mencionar pessoas específicas quando precisa de ação
- Formatar com bold, bullets e code blocks para scanability
- Agrupar updates em uma mensagem ao invés de 5 mensagens curtas

### Don'ts
- @channel ou @here sem necessidade real (respeitar notificações)
- Mensagens longas sem formatação (wall of text em Slack é ignorado)
- Feedback negativo em canal público (usar DM ou thread privada)
- Áudio/vídeo sem resumo em texto (nem todos podem ouvir no momento)
- Assumir que todos leram — se é importante, confirme recebimento

## Cross-References

- `voice/calibration/formality-scale.md` — Níveis 1-2 para Slack
- `voice/calibration/cultural-adaptation-br.md` — Tom relacional no Slack
- `phrases/handoff-communication.md` — Frases para comunicar entregas
