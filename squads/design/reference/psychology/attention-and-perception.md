# Attention and Perception



## Metadata

- **Categoria:** Cognitive Psychology, Visual Design
- **Relevancia para o Squad:** Alta — como usuarios percebem e focam em interfaces
- **Ultima revisao:** 2026-03-06



## Summary

Atencao e percepcao determinam o que o usuario ve, processa e ignora em uma interface. O sistema visual humano e surpreendentemente seletivo — a maioria do conteudo de uma tela e ignorado. Entender como atencao funciona permite projetar interfaces que guiam o olhar e comunicam prioridade de forma eficiente.





## Key Concepts


### 1. Pre-Attentive Processing

Certos atributos visuais sao processados antes da atencao consciente (<200ms): cor, tamanho, orientacao, movimento, forma. Destacar um elemento com atributo pre-attentive garante que sera notado. Mas se muitos elementos competem por pre-attentive processing, nenhum se destaca.


### 2. Change Blindness e Inattentional Blindness

Change blindness: usuarios nao notam mudancas que ocorrem durante interrupcoes (page load, blink). Inattentional blindness: usuarios focados em uma tarefa nao percebem elementos inesperados. Implicacoes: mudancas importantes precisam de animacao/highlight; banners podem ser completamente ignorados.


### 3. F-Pattern e Z-Pattern Reading

Em paginas de conteudo (artigos, search results), usuarios escaneiam em F-pattern: horizontal no topo, um pouco menos horizontal no meio, vertical na esquerda. Em paginas de marketing (landing pages), Z-pattern: topo-esquerda > topo-direita > bottom-esquerda > bottom-direita.


### 4. Visual Hierarchy (Size, Color, Contrast, Position)

A hierarquia visual guia a atencao: elementos maiores sao vistos primeiro, cores contrastantes atraem atencao, posicao superior-esquerda e vista primeiro (culturas LTR). Hierarquia clara significa que o usuario encontra o mais importante sem esforco.


### 5. Banner Blindness

Usuarios aprenderam a ignorar tudo que parece propaganda — banners no topo, sidebars promocionais, qualquer coisa que se pareca com ad. Implicacao: comunicacoes importantes nao devem parecer com anuncios. Posicao, formato e estilo de ads sao ativamente ignorados.



## Application to Design Squad

- **Visual hierarchy audit:** Para cada tela, verificar: o que o usuario deve ver primeiro? O elemento mais importante e realmente o mais proeminente (maior, mais contrastante, melhor posicionado)?
- **Pre-attentive highlighting:** Usar atributos pre-attentive (cor, tamanho) para destacar informacao critica. Mas limitar a 1-2 destaques por viewport — muitos highlights = nenhum highlight.
- **Animation for change:** Quando conteudo muda dinamicamente (notifications, counters, status updates), usar animacao sutil para chamar atencao. Sem animacao, change blindness e real.
- **F-pattern para conteudo:** Para paginas de conteudo (dashboards, listas), colocar informacao mais importante na faixa horizontal superior e na coluna esquerda.
- **Avoid banner patterns:** Comunicacoes importantes devem nao parecer banners. Evitar posicao, tamanho e estilo de anuncios para mensagens que precisam ser lidas.



## Key Takeaways

1. **Pre-attentive attributes sao a arma secreta de visual design.** Cor e tamanho capturam atencao antes do pensamento consciente.

2. **Change blindness e real.** Se a mudanca nao e animada ou destacada, o usuario nao percebe.

3. **F-pattern em conteudo, Z-pattern em marketing.** Posicione informacao critica onde o padrao de scanning natural vai encontrar.

4. **Menos highlights = mais destaque.** Quando tudo e destacado, nada se destaca.

5. **Banner blindness e aprendida.** Nao use formato de anuncio para mensagens importantes.



## Cross-References

- [Designing with the Mind — Johnson](../books/johnson-designing-with-the-mind.md) — percepcao visual detalhada
- [Gestalt Principles](gestalt-principles-deep-dive.md) — organizacao perceptual
- [Cognitive Load Theory](cognitive-load-theory.md) — capacidade limitada de processamento
- [Don't Make Me Think — Krug](../books/krug-dont-make-me-think.md) — scanning e satisficing
- [Dashboards and Tables Patterns](../ui-patterns/dashboards-and-tables-patterns.md) — hierarquia em dashboards
