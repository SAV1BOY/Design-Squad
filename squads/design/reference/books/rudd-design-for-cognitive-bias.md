# Design for Cognitive Bias — David Dylan Thomas



## Metadata

- **Autor:** David Dylan Thomas
- **Publicacao:** 2020
- **Categoria:** Cognitive Bias, Ethical Design
- **Relevancia para o Squad:** Media-Alta — design consciente de vieses cognitivos
- **Ultima revisao:** 2026-03-06



## Summary

Design for Cognitive Bias explora como vieses cognitivos influenciam o comportamento do usuario em interfaces digitais e como designers podem tanto explorar quanto mitigar esses vieses de forma etica. Thomas apresenta os vieses mais relevantes para design digital — anchoring, framing, confirmation bias, status quo bias, loss aversion — e demonstra como cada um se manifesta em decisoes de interface.

O livro diferencia entre usar vieses para ajudar o usuario (nudging para melhores decisoes) e manipular o usuario (dark patterns que exploram vieses para beneficio da empresa). Thomas propoe um framework etico: o design deve facilitar que o usuario tome a decisao que tomaria se tivesse tempo infinito e informacao completa.

A obra e particularmente relevante no contexto atual de dark patterns e regulamentacao de interfaces manipulativas. Thomas oferece ferramentas praticas para auditar designs existentes em busca de exploracoes de vieses e para projetar interfaces que informam em vez de manipular.



## Key Concepts


### 1. Framing Effect in UI

Como a informacao e apresentada (framed) influencia a decisao tanto quanto a informacao em si. "90% de satisfacao" vs. "10% de insatisfacao" sao o mesmo dado com impacto diferente. Designers escolhem frames constantemente — em pricing pages, em dashboards, em notifications — e cada escolha influencia comportamento.


### 2. Anchoring in Pricing and Comparisons

O primeiro numero que o usuario ve ancora sua percepcao de valor. Mostrar o plano mais caro primeiro faz o segundo parecer razoavel. Mostrar o preco original riscado ancora o valor percebido do desconto. Ancoragem e inevitavel — a questao etica e se ancora para informar ou para manipular.


### 3. Status Quo Bias and Defaults

Pessoas tendem a manter a opcao default, mesmo quando alternativas sao melhores. Defaults tem poder desproporcional sobre comportamento — e por isso sao decisoes de design com responsabilidade etica. Opt-in vs. opt-out para newsletters, pre-selecao de planos, configuracoes iniciais — tudo e design de defaults.


### 4. Loss Aversion in Interface Design

Perder algo e sentido aproximadamente 2x mais intensamente que ganhar algo equivalente. "Voce vai perder acesso a..." e mais persuasivo que "Voce pode ganhar acesso a..." Loss aversion e usada eticamente em avisos de exclusao de conta e anti-eticamente em urgencia artificial.


### 5. Ethical Audit Framework

Thomas propoe avaliar cada decisao de design com: (1) Qual vies esta sendo ativado? (2) A favor de quem? (3) O usuario tomaria a mesma decisao com informacao completa e tempo infinito? Se a resposta a (3) e nao, o design esta manipulando, nao facilitando.



## Application to Design Squad

- **Bias audit em fluxos de conversao:** Auditar pricing pages, onboarding e checkout para identificar onde vieses estao sendo ativados. Avaliar se a ativacao e etica usando o framework de Thomas.
- **Default review:** Revisar todos os defaults do produto. Cada default deve servir a maioria dos usuarios, nao maximizar opt-ins involuntarios.
- **Framing guidelines:** Documentar guidelines de framing para dados e metricas no produto. Dashboards devem apresentar dados de forma balanceada, nao seletivamente positiva.
- **Dark pattern detector:** Criar checklist de dark patterns (confirmshaming, roach motel, forced continuity) para avaliar novos designs antes de aprovacao.
- **Ethical design review:** Incluir uma etapa de revisao etica em design reviews de features que envolvem conversao, retencao ou dados pessoais.



## Key Takeaways

1. **Vieses sao inevitaveis — a escolha e como lidar com eles.** Todo design ativa vieses. A questao e se o faz para informar ou manipular.

2. **Defaults sao as decisoes de design mais poderosas.** O que esta pre-selecionado determina o que a maioria faz. Use esse poder com responsabilidade.

3. **Framing muda decisoes tanto quanto fatos.** Como voce apresenta a informacao importa tanto quanto qual informacao apresenta.

4. **O teste etico e simples: informacao completa + tempo infinito.** Se o usuario mudaria a decisao com mais contexto, o design esta manipulando.

5. **Dark patterns tem custo de longo prazo.** Conversao por manipulacao gera churn, desconfianca e, crescentemente, risco regulatorio.



## Cross-References

- [Behavioral Design Ethics](../psychology/behavioral-design-ethics.md) — framework etico expandido
- [Decision Making in Interfaces](../psychology/decision-making-in-interfaces.md) — como usuarios decidem
- [Thinking Fast and Slow — Kahneman](kahneman-thinking-fast-slow.md) — fundamento teorico dos vieses
- [Nudge — Thaler](thaler-nudge.md) — nudges eticos vs. manipulativos
- [Predictably Irrational — Ariely](ariely-predictably-irrational.md) — irracionalidade previsivel
