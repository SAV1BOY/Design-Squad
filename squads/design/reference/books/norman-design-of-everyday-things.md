# The Design of Everyday Things — Don Norman



## Metadata

- **Autor:** Don Norman
- **Publicacao:** 1988 (revisado 2013)
- **Categoria:** Design Fundamentals, Usability, Cognitive Psychology
- **Relevancia para o Squad:** Alta — fundamento teórico para toda decisão de design
- **Ultima revisao:** 2026-03-06



## Summary

The Design of Everyday Things é o texto fundacional do design centrado no humano. Norman argumenta que quando pessoas têm dificuldade com objetos ou interfaces, o problema é do design, não do usuário. O livro introduz conceitos fundamentais como affordances, signifiers, mapping, feedback e constraints — vocabulário essencial para qualquer designer.

A edição revisada de 2013 atualiza os exemplos para o contexto digital, mas os princípios permanecem atemporais. Norman apresenta o modelo de ação humana (gulf of execution e gulf of evaluation), explicando por que interfaces confundem: ou o usuário não sabe o que fazer (execution gap) ou não consegue interpretar o resultado da ação (evaluation gap). O designer deve minimizar ambos os gaps.

O livro também aborda a tensão entre estética e usabilidade, o papel do erro humano no design (errors vs. slips), e como bom design torna o correto óbvio e o incorreto difícil. Norman introduz o conceito de "human-centered design" como processo iterativo de observação, prototipagem e teste.



## Key Concepts


### 1. Affordances e Signifiers

Affordances são as possibilidades de ação que um objeto oferece (um botão pode ser pressionado). Signifiers são os sinais que comunicam essas possibilidades ao usuário (o relevo visual do botão sugere que é clicável). No digital, affordances são percebidas principalmente através de signifiers visuais — sombras, cores, ícones, cursores.


### 2. Gulf of Execution / Gulf of Evaluation

O gulf of execution é a distância entre a intenção do usuário e as ações disponíveis na interface. O gulf of evaluation é a distância entre o estado do sistema e a capacidade do usuário de interpretá-lo. Bom design minimiza ambos — tornando ações óbvias e feedback imediato e compreensível.


### 3. Mapping e Feedback

Mapping é a relação entre controles e seus efeitos. Mapping natural (botão à esquerda controla item à esquerda) reduz carga cognitiva. Feedback é a comunicação do sistema sobre o resultado da ação. Deve ser imediato, informativo e não intrusivo. Ausência de feedback é uma das maiores falhas de usabilidade.


### 4. Constraints (Physical, Cultural, Semantic, Logical)

Constraints limitam as ações possíveis, guiando o usuário para o caminho correto. Physical constraints impedem ações fisicamente (USB só encaixa de um jeito — antes do USB-C). Cultural constraints são convenções aprendidas (vermelho = erro). Semantic constraints derivam do significado da situação. Logical constraints emergem da lógica do contexto.


### 5. Slips vs. Mistakes

Slips são erros de execução — o usuário sabe o que quer mas executa errado (clicou no botão ao lado). Mistakes são erros de intenção — o usuário formou um modelo mental incorreto do que deveria fazer. Cada tipo requer estratégia de prevenção diferente: slips precisam de melhor layout e confirmação; mistakes precisam de melhor comunicação e onboarding.



## Application to Design Squad

- **Vocabulary compartilhado:** Usar affordance, signifier, mapping e feedback como linguagem padrão em design reviews. Todo componente deve ser avaliado nesses termos.
- **Checklist de gaps:** Para cada fluxo novo, avaliar explicitamente: "O usuário sabe o que fazer aqui?" (execution gap) e "O usuário entende o que aconteceu?" (evaluation gap).
- **Error prevention by design:** Classificar erros reportados como slips ou mistakes e aplicar a estratégia de prevenção adequada. Priorizar constraints que tornem erros impossíveis sobre mensagens de erro.
- **Feedback audit:** Auditar regularmente os fluxos do produto para identificar ações sem feedback adequado — loading states ausentes, confirmações silenciosas, estados de erro genéricos.
- **Natural mapping em layouts:** Garantir que a posição visual de controles corresponda logicamente ao que afetam. Quando o controle está longe do conteúdo que modifica, adicionar signifiers que conectem os dois.



## Key Takeaways

1. **Se o usuário erra, o design falhou.** Nunca culpe o usuário. Cada erro é uma oportunidade de melhorar a interface.

2. **Signifiers são mais importantes que affordances no digital.** O que importa não é o que o elemento pode fazer, mas o que o usuário percebe que pode fazer.

3. **Feedback imediato é inegociável.** Toda ação do usuário deve ter resposta visível do sistema, mesmo que seja apenas um spinner indicando processamento.

4. **Constraints são o melhor error prevention.** Tornar o errado impossível é superior a detectar e comunicar o erro depois.

5. **Modelos mentais divergentes causam frustração.** Quando o modelo mental do usuário não corresponde ao modelo do sistema, a interface falha. Pesquisa com usuários revela esses gaps.



## Cross-References

- [Don't Make Me Think — Krug](krug-dont-make-me-think.md) — aplicação prática de usabilidade web
- [Designing with the Mind in Mind — Johnson](johnson-designing-with-the-mind.md) — psicologia cognitiva para designers
- [Cognitive Load Theory](../psychology/cognitive-load-theory.md) — aprofundamento em carga cognitiva
- [Gestalt Principles](../psychology/gestalt-principles-deep-dive.md) — como percepção visual afeta signifiers
- [About Face — Cooper](cooper-about-face.md) — interaction design patterns derivados desses princípios
