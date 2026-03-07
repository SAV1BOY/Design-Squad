# Cognitive Load Theory



## Metadata

- **Categoria:** Cognitive Psychology, Usability, Information Design
- **Relevancia para o Squad:** Alta — base teorica para simplicidade em design
- **Ultima revisao:** 2026-03-06



## Summary

Cognitive Load Theory (CLT), desenvolvida por John Sweller, explica como a capacidade limitada da working memory afeta aprendizado e performance. Para designers, CLT fundamenta por que interfaces simples funcionam melhor: o cerebro tem recursos cognitivos limitados, e toda complexidade desnecessaria consome recursos que deveriam ser usados para a tarefa real.

CLT identifica tres tipos de carga: intrinsic (complexidade inerente da tarefa), extraneous (complexidade adicionada pelo design da interface) e germane (esforço produtivo de aprendizado). O objetivo do designer e minimizar extraneous load, gerenciar intrinsic load e facilitar germane load.



## Key Concepts


### 1. Three Types of Cognitive Load

Intrinsic: complexidade da propria tarefa (calcular imposto e intrinsecamente complexo). Extraneous: complexidade adicionada pela interface (navegacao confusa, layout poluido). Germane: esforco de construir modelos mentais uteis (aprender como o sistema funciona). Design deve minimizar extraneous, nao intrinsic.


### 2. Working Memory Constraints

Working memory retém 4 +/- 1 chunks por 6-12 segundos. Interfaces que exigem que o usuario memorize informacao de uma tela para outra violam esse limite. Solução: informacao necessaria visivel, nao memorizada.


### 3. Chunking

Agrupar informação em unidades significativas reduz carga cognitiva. Numero de telefone como (11) 9999-9999 em vez de 1199999999. Formularios em secoes tematicas. Menus em categorias. Chunking transforma muitos itens em poucos grupos.


### 4. Progressive Disclosure

Mostrar so o necessario para a decisao atual; revelar mais sob demanda. Reduz extraneous load escondendo complexidade ate que seja relevante. Menus hierarquicos, accordions, "show more" e wizards sao implementacoes de progressive disclosure.


### 5. Split Attention Effect

Quando informacao relacionada e separada espacial ou temporalmente, o usuario gasta esforco extra para integra-la mentalmente. Implicacao: labels proximos dos campos, error messages proximas do campo com erro, tooltips contextuais em vez de pagina de ajuda separada.



## Application to Design Squad

- **Extraneous load audit:** Para cada tela, perguntar: o que nesta tela nao contribui para a tarefa do usuario? Cada elemento que nao ajuda atrapalha.
- **Information proximity:** Garantir que informacao relacionada esta visualmente proxima. Labels junto a campos, errors junto a inputs, context junto a actions.
- **Progressive disclosure como default:** Para features complexas, mostrar apenas o essencial inicialmente. Avancado sob demanda (expand, "more options").
- **Chunking em formularios:** Formularios longos divididos em secoes tematicas. Cada secao e um chunk cognitivo manuseavel.
- **No memorization required:** Nenhum fluxo deve exigir que o usuario lembre informacao de passos anteriores. Se precisa, torne a informacao persistente.



## Key Takeaways

1. **Toda complexidade desnecessaria e custo.** Extraneous load e divida de design que o usuario paga.

2. **4 chunks e o limite real.** Projete para 4 itens simultaneos, nao 7 (o "7 +/- 2" foi revisado para baixo).

3. **Proximidade reduz split attention.** Informacao relacionada deve estar visualmente junta.

4. **Progressive disclosure e gerenciamento de carga.** Mostre o necessario agora; revele o resto sob demanda.

5. **Chunking transforma complexidade em manuseabilidade.** Agrupe informacoes em unidades significativas.



## Cross-References

- [Designing with the Mind — Johnson](../books/johnson-designing-with-the-mind.md) — working memory constraints
- [Don't Make Me Think — Krug](../books/krug-dont-make-me-think.md) — aplicacao pratica
- [Gestalt Principles](gestalt-principles-deep-dive.md) — organização perceptual
- [Progressive Disclosure Psychology](progressive-disclosure-psychology.md) — aprofundamento
- [Forms and Validation Patterns](../ui-patterns/forms-and-validation-patterns.md) — carga em formularios
