# Decision Making in Interfaces



## Metadata

- **Categoria:** Behavioral Psychology, UX Design
- **Relevancia para o Squad:** Alta — toda interface e uma serie de decisoes
- **Ultima revisao:** 2026-03-06



## Summary

Toda interacao com uma interface e uma decisao: clicar ou nao? Este campo ou aquele? Este plano ou aquele? Entender como humanos tomam decisoes — especialmente sob incerteza, pressao de tempo e sobrecarga de informacao — permite projetar interfaces que facilitam boas decisoes e reduzem paralisia.



## Key Concepts


### 1. Hick's Law (Choice Overload)

Tempo de decisao aumenta logaritmicamente com o numero de opcoes. Com mais opcoes, usuarios demoram mais e ficam menos satisfeitos com a escolha (paradox of choice). Reducao de opcoes ou agrupamento em categorias reduz tempo e aumenta satisfacao.


### 2. Satisficing vs. Maximizing

Satisficers escolhem a primeira opcao "boa o suficiente." Maximizers avaliam todas as opcoes para escolher a "melhor." A maioria dos usuarios de interface sao satisficers — projetar para a primeira impressao e mais eficaz que oferecer comparacao exaustiva.


### 3. Default Bias

A grande maioria dos usuarios aceita o default, independente de ser a melhor opcao para eles. Defaults carregam enorme responsabilidade etica — o que esta pre-selecionado e o que a maioria faz. Smart defaults baseados em dados de uso real servem a maioria.


### 4. Paradox of Choice

Mais opcoes nao significam melhor experiencia. Estudo de Iyengar: 24 sabores de geleia geraram mais interesse mas menos compras que 6 sabores. Implicacao: curar opcoes e servico ao usuario. Menos opcoes relevantes > muitas opcoes genericas.


### 5. Decision Fatigue

A qualidade das decisoes deteriora apos muitas decisoes consecutivas. Implicacao: formularios longos, configuracoes extensas e flows com muitas decisoes causam "fadiga decisoria" que leva a defaults aceitos cegamente ou abandono.



## Application to Design Squad

- **Option reduction:** Para cada tela com escolhas, perguntar: todas as opcoes sao necessarias? Pode agrupar? Pode esconder opcoes avancadas? Pode pre-selecionar a melhor?
- **Smart defaults baseados em dados:** Analisar dados de uso para definir defaults que servem a maioria. Documentar o racional de cada default.
- **Decision sequencing:** Em flows com multiplas decisoes, ordenar da mais importante/facil para a menos importante/dificil. Nao esgotar o usuario com decisoes dificeis no inicio.
- **Recommendation over choice:** Em vez de "escolha entre A, B e C," oferecer "recomendamos B porque..." Curadoria reduz carga decisoria.
- **Undo como safety net:** Quando possivel, tornar decisoes reversiveis. "Voce pode mudar depois" reduz ansiedade de decisao.



## Key Takeaways

1. **Menos opcoes = decisoes melhores.** Curar opcoes e servico, nao limitacao.

2. **Defaults sao decisoes de design com poder desproporcional.** A maioria aceita o default — escolha-o com cuidado.

3. **Satisficers sao a maioria.** Projete para a primeira impressao boa, nao para comparacao exaustiva.

4. **Decision fatigue e real.** Minimize o numero de decisoes por sessao.

5. **Recomendacao reduz carga.** "Recomendamos X" e melhor que "escolha entre X, Y e Z."



## Cross-References

- [Thinking Fast and Slow — Kahneman](../books/kahneman-thinking-fast-slow.md) — System 1 e System 2
- [Nudge — Thaler](../books/thaler-nudge.md) — choice architecture
- [Predictably Irrational — Ariely](../books/ariely-predictably-irrational.md) — irracionalidade em escolhas
- [Universal Principles — Lidwell](../books/brown-universal-principles-of-design.md) — Hick's Law
- [Pricing and Plans Patterns](../ui-patterns/pricing-and-plans-patterns.md) — decisao de compra
