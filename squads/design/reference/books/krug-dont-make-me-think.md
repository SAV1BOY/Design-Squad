# Don't Make Me Think — Steve Krug



## Metadata

- **Autor:** Steve Krug
- **Publicacao:** 2000 (3a edicao: 2014)
- **Categoria:** Web Usability, UX Fundamentals
- **Relevancia para o Squad:** Alta — guia prático essencial de usabilidade
- **Ultima revisao:** 2026-03-06



## Summary

Don't Make Me Think é o guia mais conciso e acessível sobre usabilidade web já escrito. A tese central de Krug é que uma interface é boa quando o usuário não precisa pensar para usá-la — cada decisão, cada clique, cada rótulo deve ser auto-evidente. O livro desafia a tendência de over-design e argumenta que usuários não leem, escaneiam; não escolhem a melhor opção, satisfazem com a primeira razoável; e não descobrem como as coisas funcionam, improvisam.

Krug apresenta princípios práticos de usabilidade com exemplos visuais claros: hierarquia visual, convenções web, navegação eficiente, e a importância de eliminar "happy talk" (texto desnecessário). A terceira edição adiciona considerações sobre mobile e acessibilidade.

O livro é propositalmente curto e direto — praticando o que prega. Cada capítulo pode ser lido em minutos e aplicado imediatamente. Krug argumenta que usabilidade testing não precisa ser caro ou elaborado — testes com três a cinco pessoas usando protótipos de papel já revelam os problemas mais graves.



## Key Concepts


### 1. Don't Make Me Think (Self-Evidence Principle)

A interface ideal é aquela que o usuário entende instantaneamente, sem deliberação. Se um rótulo, ícone ou layout exige que o usuário pare para pensar "o que isso faz?", é um problema de design. Auto-evidência é o padrão de qualidade — se não pode ser auto-evidente, pelo menos deve ser auto-explicativo.


### 2. Scanning, Satisficing, Muddling Through

Usuários reais não leem páginas — eles escaneiam buscando algo que pareça relevante. Não avaliam todas as opções — clicam na primeira que parece razoável (satisficing). Não constroem modelo mental completo — improvisam e voltam quando erram. Design deve acomodar esse comportamento, não lutar contra ele.


### 3. Visual Hierarchy e Conventions

Uma hierarquia visual clara (tamanho, cor, espaço, peso tipográfico) comunica importância e estrutura sem exigir leitura. Convenções web (logo no topo esquerdo, carrinho no topo direito, links sublinhados) devem ser seguidas a menos que a alternativa seja inequivocamente melhor.


### 4. Trunk Test (Navigation Check)

Para avaliar qualquer página, imagine que foi teletransportado para ela sem contexto: consegue responder — onde estou? (site, seção), o que posso fazer aqui? como cheguei aqui? onde está a busca? Se não consegue, a navegação precisa melhorar.


### 5. Less is More (Omit Needless Words)

Krug cita Strunk & White: "Omit needless words." Cada palavra na interface que não ajuda ativamente atrapalha. Happy talk (texto de boas-vindas genérico), instruções óbvias e jargão interno devem ser eliminados. O melhor copy é o que nem é percebido como copy.



## Application to Design Squad

- **Heurística de revisão:** Em toda design review, aplicar o teste: "o usuário precisa pensar para entender isso?" Se sim, simplificar.
- **Trunk Test em novos fluxos:** Aplicar o trunk test em cada tela de novos fluxos antes de seguir para desenvolvimento. Documentar as respostas para cada tela.
- **Redução de copy:** Em revisões de conteúdo, desafiar cada palavra na interface — pode ser removida sem perda de compreensão? Se sim, remover.
- **Design para scanning:** Usar hierarquia visual clara, bullet points, bold keywords e whitespace generoso. Nunca depender de blocos de texto para comunicar ações.
- **Convenções antes de inovação:** Seguir convenções estabelecidas como padrão. Inovar apenas quando há evidência de que a alternativa é significativamente melhor e testar para confirmar.



## Key Takeaways

1. **Se o usuário precisa pensar, simplifique.** Auto-evidência é o padrão de ouro para qualquer elemento de interface.

2. **Projete para scanning, não para leitura.** Hierarquia visual e scanability são mais importantes que conteúdo detalhado.

3. **Siga convenções — a não ser que tenha algo inquestionavelmente melhor.** Inovação em UI tem custo cognitivo para o usuário.

4. **Elimine palavras desnecessárias.** Cada palavra que sobra compete por atenção com as que importam.

5. **Teste cedo e barato.** Um teste com três pessoas revela mais problemas do que meses de debate interno.



## Cross-References

- [Rocket Surgery Made Easy — Krug](krug-rocket-surgery-made-easy.md) — guia prático de usability testing do mesmo autor
- [Design of Everyday Things — Norman](norman-design-of-everyday-things.md) — fundamento teórico dos princípios aplicados aqui
- [Cognitive Load Theory](../psychology/cognitive-load-theory.md) — base científica para "don't make me think"
- [Attention and Perception](../psychology/attention-and-perception.md) — por que scanning funciona assim
- [Navigation Patterns](../ui-patterns/navigation-patterns.md) — padrões que passam no trunk test
