# Designing with the Mind in Mind — Jeff Johnson



## Metadata

- **Autor:** Jeff Johnson
- **Publicacao:** 2010 (3a edicao: 2021)
- **Categoria:** Cognitive Psychology, UI Design
- **Relevancia para o Squad:** Alta — psicologia cognitiva aplicada diretamente a decisões de UI
- **Ultima revisao:** 2026-03-06



## Summary

Designing with the Mind in Mind traduz pesquisa em psicologia cognitiva e perceptual em guidelines práticas de design de interface. Johnson apresenta como percepção visual, atenção, memória, aprendizado, leitura e tomada de decisão funcionam no cérebro humano — e o que isso significa para cada decisão de UI.

O livro é organizado por capacidade cognitiva: como vemos (percepção), como focamos (atenção), como lembramos (memória), como aprendemos (aprendizado), como lemos (reading patterns), como pensamos (decision making) e como reagimos (timing e responsiveness). Cada capítulo conecta a ciência à prática com exemplos de interfaces reais.

A terceira edição adiciona cobertura de mobile, acessibilidade e dark patterns, tornando o livro ainda mais relevante para o contexto atual. Johnson é especialmente bom em desmistificar "regras de design" — explicando quando se aplicam, quando não, e por quê.



## Key Concepts


### 1. Perception is Biased (Pre-Attentive Processing)

O sistema visual processa certas propriedades antes da atenção consciente: cor, tamanho, orientação, movimento. Esses atributos pre-attentive são percebidos em milissegundos e podem ser usados para guiar atenção. Destacar um item em vermelho em uma lista cinza funciona porque cor é processada pre-attentivamente.


### 2. Reading is Unnatural (Foveal Vision Matters)

Leitura é uma habilidade aprendida que exige esforço cognitivo. A fóvea (centro da visão) processa apenas 1-2 graus do campo visual — o equivalente a 8-10 caracteres em distância típica de tela. Isso explica por que linhas longas são difíceis de ler e por que hierarchy visual é essencial.


### 3. Memory Limitations (Working Memory is Tiny)

Working memory retém 4 +/- 1 chunks de informação por 6-12 segundos (não 7 +/- 2 como popularizado). Implicação: interfaces que exigem que o usuário lembre informação de uma tela para usar em outra violam limites cognitivos. Informação necessária deve estar visível, não memorizada.


### 4. Time Constants of Human Response

Percepção: 0.1s (feedback parece instantâneo). Atenção: 1s (tolerância para operações simples). Flow: 10s (máximo antes de perder contexto mental). Essas constantes devem guiar timing de feedback, loading states e transições.


### 5. Learning from Experience (Not Manuals)

Humanos aprendem primariamente por exploração e feedback, não por instrução. Implicação: interfaces devem ser exploráveis com segurança (undo disponível, ações reversíveis) e fornecer feedback imediato. Tutoriais e manuais são último recurso, não primeiro.



## Application to Design Squad

- **Pre-attentive attributes no design system:** Documentar quais atributos visuais (cor, tamanho, peso) são usados para destacar informação no sistema. Garantir consistência — vermelho sempre significa erro, nunca decoração.
- **Working memory checklist:** Em fluxos multi-step, verificar se algum passo exige que o usuário memorize informação de passos anteriores. Se sim, tornar a informação persistente ou visível.
- **Response time guidelines:** Definir SLAs de responsiveness: feedback < 100ms, operações simples < 1s, operações complexas com progress indicator > 1s. Documentar no design system.
- **Explorable by default:** Toda feature nova deve ser explorável sem risco — undo disponível, confirmação antes de ações destrutivas, preview antes de commit.
- **Foveal vision em layouts:** Informação crítica deve estar próxima ao ponto de foco do usuário. Não esconder feedback em cantos distantes da tela.



## Key Takeaways

1. **Working memory tem 4 slots, não 7.** Projete interfaces que não exijam memorização entre telas ou passos.

2. **Atributos pre-attentive são a ferramenta mais poderosa de UI.** Cor, tamanho e movimento capturam atenção antes do pensamento consciente.

3. **0.1s, 1s, 10s — os thresholds de responsiveness.** Respeitar essas constantes é a diferença entre uma interface "rápida" e "lenta" para o cérebro.

4. **Aprendizado por exploração supera instrução.** Interfaces seguras de explorar são mais eficazes que tutoriais detalhados.

5. **Regras de design têm razões cognitivas.** Entender o "por quê" permite aplicar princípios em contextos novos, não apenas seguir regras mecanicamente.



## Cross-References

- [Cognitive Load Theory](../psychology/cognitive-load-theory.md) — framework teórico para carga cognitiva
- [Attention and Perception](../psychology/attention-and-perception.md) — aprofundamento em atenção visual
- [Gestalt Principles](../psychology/gestalt-principles-deep-dive.md) — princípios de organização perceptual
- [100 Things — Weinschenk](weinschenk-100-things.md) — abordagem similar com foco em psicologia aplicada
- [Design of Everyday Things — Norman](norman-design-of-everyday-things.md) — fundamentos complementares
