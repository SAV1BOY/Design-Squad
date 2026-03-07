# Media and Content Design Playbook



## Metadata

- **Categoria:** Industry Playbook, Media, Content Platforms
- **Relevancia para o Squad:** Baixa-Media — padroes para plataformas de conteudo
- **Ultima revisao:** 2026-03-06



## Summary

Plataformas de media e conteudo (streaming, news, blogs, podcasts) tem desafios especificos: discovery de conteudo em catálogos massivos, consumo otimizado para diferentes formatos (texto, video, audio), retencao baseada em habito de consumo e monetizacao (ads, subscricao, freemium).



## Key Concepts


### 1. Content Discovery and Recommendations

Em catalogos grandes, busca e browse sao insuficientes — recomendacoes algoritmicas sao essenciais. Personalizacao baseada em: historico de consumo, preferencias explicitas, similaridade de conteudo, trending/popular. Balance entre personalizacao (relevancia) e serendipity (descoberta inesperada).


### 2. Reading/Viewing Experience

Para texto: tipografia otimizada para leitura longa (serif, line-height 1.6, 50-75 chars/line), dark mode, adjustable font size, estimated reading time. Para video: player controls intuitivos, quality auto-adjustment, continue watching, subtitles. Para audio: background playback, speed control, sleep timer.


### 3. Content Cards and Feeds

Cards como unidade atomic de conteudo: imagem, titulo, metadata (autor, data, duracao), snippet. Feed algoritmico vs. cronologico (ou toggle). Infinite scroll com performance optimizada. Skeleton loading para perceived performance.


### 4. Paywall and Monetization Patterns

Metered paywall (X artigos gratis/mês), hard paywall (assinatura obrigatoria), freemium (conteudo basico gratis, premium pago). Design challenge: mostrar valor do conteudo premium sem frustrar free users excessivamente. Teaser (primeiros paragrafos) + CTA de upgrade contextual.


### 5. Engagement and Retention

Daily digest, personalized newsletters, push notifications para conteudo novo relevante. Streak patterns (leitura diaria), bookmarks/save for later, offline download. A retencao depende de criar habito de consumo regular.



## Application to Design Squad

- **Content card component:** Se o produto exibe conteudo (artigos, posts, items), investir em card component rico: imagem, titulo, metadata, snippet, acoes (save, share). Variantes: compact, featured, horizontal.
- **Reading/viewing optimization:** Para conteudo long-form, otimizar tipografia e layout para leitura/visualizacao. Testar com conteudo real, nao com placeholder.
- **Discovery patterns:** Para catalogos grandes, implementar: busca com autocomplete, categorias navegaveis, "Recomendado para voce," "Popular," "Novo." Discovery e retencao.
- **Paywall design ethical:** Se o produto tem paywall, projetar transicao suave: mostrar valor do conteudo, CTA claro, opcoes de plano, trial quando possivel.
- **Consumption metrics:** Rastrear metricas de consumo: artigos lidos, tempo de leitura, completion rate. Usar para melhorar recomendacoes e identificar content gaps.



## Key Takeaways

1. **Discovery e tao importante quanto criacao de conteudo.** O melhor conteudo e inutil se ninguem encontra.

2. **Experiencia de consumo e o produto.** Em media, a interface de leitura/video/audio e onde o valor e entregue — otimize obsessivamente.

3. **Cards sao a unidade atomic.** Investir em card component rico e flexivel atende feed, search results, recommendations e mais.

4. **Habito de consumo = retencao.** Daily digest, streaks e notifications personalizadas criam rotina.

5. **Paywall deve demonstrar valor, nao frustrar.** Mostrar por que vale pagar, nao apenas bloquear.



## Cross-References

- [Hooked — Eyal](../books/eyal-hooked.md) — habit formation para media
- [Habit Formation Design](../psychology/habit-formation-design.md) — habito de consumo
- [Search and Filter Patterns](../ui-patterns/search-and-filter-patterns.md) — content discovery
- [Elements of Typographic Style — Bringhurst](../books/bringhurst-elements-of-typographic-style.md) — tipografia para leitura
- [Notifications and Alerts Patterns](../ui-patterns/notifications-and-alerts-patterns.md) — content notifications
