# Notifications and Alerts Patterns



## Metadata

- **Categoria:** UI Patterns, Communication, Feedback
- **Relevancia para o Squad:** Alta — comunicacao sistema-usuario
- **Ultima revisao:** 2026-03-06



## Summary

Notifications e alerts sao como o sistema se comunica com o usuario — desde feedback instantaneo (toast, snackbar) ate comunicacoes persistentes (notification center, email). O desafio e comunicar sem interromper: informar o necessario, no momento certo, no canal adequado.



## Key Concepts


### 1. Notification Hierarchy

Alert (critico, requer acao imediata — vermelho), Warning (importante, requer atencao — amarelo), Info (informativo, nao requer acao — azul), Success (confirmacao de acao — verde). Cada nivel tem urgencia, persistencia e posicao proprias.


### 2. Inline vs. Toast vs. Banner vs. Modal

Inline: dentro do conteudo, contextual (form errors, field help). Toast/Snackbar: temporario, bottom ou top, auto-dismiss (sucesso, info). Banner: persistente no topo, nao auto-dismiss (avisos de sistema, manutencao). Modal: interruptivo, requer acao (confirmacao, erro critico). Escolha baseada em urgencia e necessidade de acao.


### 3. Notification Center

Hub centralizado de todas as notificacoes com: lista cronologica, read/unread status, action links, filter by type. Badge de count no icone de sino. Acessivel de qualquer tela. Notificacoes nao lidas devem ter destaque visual claro.


### 4. Push Notification Design

Titulo curto (<50 chars), corpo descritivo (<100 chars), deep link para contexto no app. Timing importa: nao enviar de madrugada, agrupar multiplas notificacoes, respeitar DND (Do Not Disturb). Personalizacao de frequencia e tipo nas configuracoes.


### 5. Notification Preferences

Permitir que usuario controle: quais notificacoes receber (por tipo), em qual canal (in-app, email, push, SMS), com qual frequencia (imediata, digest diario, semanal). Defaults devem ser uteis mas nao invasivos. Opt-in para a maioria; opt-out apenas para criticos.



## Application to Design Squad

- **Notification design system:** Padronizar no design system os quatro niveis de notificacao com cor, icone, posicao, persistencia e interatividade definidos.
- **Channel strategy:** Para cada tipo de notificacao, definir o canal adequado. Nao enviar tudo por push — reserve push para acao necessaria.
- **Preference controls:** Implementar tela de preferencias de notificacao com granularidade por tipo e canal. Respeitar escolhas do usuario.
- **Notification audit:** Revisar regularmente: quantas notificacoes o usuario recebe por dia? Quais sao ignoradas? Quais geram acao? Eliminar as ignoradas.
- **Accessibility em notifications:** Notifications dinamicas devem usar aria-live regions. Toasts com auto-dismiss devem ter duracao suficiente para leitura (minimo 5 segundos).



## Key Takeaways

1. **Urgencia determina o pattern.** Critico = modal; importante = banner; info = toast; contextual = inline.

2. **Auto-dismiss para sucesso, persistente para erro.** Sucesso nao precisa de acao; erro precisa de correcao.

3. **Respeite o controle do usuario.** Permita personalizar tipo, canal e frequencia de notificacoes.

4. **Menos e mais.** Cada notificacao dispensavel reduz o valor das necessarias. Curate agressivamente.

5. **Timing importa tanto quanto conteudo.** A notificacao certa no momento errado e ruido.



## Cross-References

- [Hooked — Eyal](../books/eyal-hooked.md) — triggers externos
- [Feedback Loops Psychology](../psychology/feedback-loops-psychology.md) — feedback como comunicacao
- [ARIA Authoring Practices](../standards/aria-authoring-practices.md) — live regions
- [Settings and Preferences Patterns](settings-and-preferences-patterns.md) — notification settings
- [Designing for Emotion — Walter](../books/walter-designing-for-emotion.md) — tom de notificacoes
