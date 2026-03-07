# Design Systems — Alla Kholmatova



## Metadata

- **Autora:** Alla Kholmatova
- **Publicacao:** 2017
- **Categoria:** Design Systems, Pattern Language
- **Relevancia para o Squad:** Alta — fundamento para linguagem de padrões no design system
- **Ultima revisao:** 2026-03-06



## Summary

Design Systems de Kholmatova aborda design systems do ponto de vista da linguagem — não apenas como coleções de componentes, mas como sistemas de comunicação com vocabulário, gramática e regras. O livro diferencia "functional patterns" (soluções recorrentes para problemas de interface) de "perceptual patterns" (elementos que comunicam personalidade e marca).

Kholmatova argumenta que a maioria dos design systems foca demais em componentes (botões, cards, modals) e negligencia o fundamento: princípios de design, linguagem compartilhada e padrões de comportamento. Um sistema com 200 componentes mas sem princípios claros é uma biblioteca, não um sistema.

O livro é prático e metodológico — inclui exercícios para definir princípios de design, inventariar padrões existentes, nomear e documentar padrões, e criar governança para evolução do sistema. É o complemento perfeito ao Atomic Design de Frost: enquanto Frost foca na arquitetura de composição, Kholmatova foca na linguagem e nos princípios.



## Key Concepts


### 1. Functional Patterns vs. Perceptual Patterns

Functional patterns resolvem problemas de interação (navigation, data entry, feedback). Perceptual patterns comunicam personalidade (tipografia, cor, espaçamento, tom de voz, iconografia). Um design system completo precisa de ambos — functional sem perceptual é genérico; perceptual sem functional é superficial.


### 2. Design Principles as Foundation

Princípios de design são as crenças compartilhadas que guiam decisões quando não há pattern pronto. Bons princípios são específicos ao produto (não genéricos como "simples e bonito"), testáveis (pode-se avaliar se um design os segue) e acionáveis (ajudam a escolher entre alternativas).


### 3. Pattern Naming and Shared Language

Cada pattern precisa de nome descritivo e consensual. "Hero banner" é melhor que "componente-47." A linguagem compartilhada permite que designer diga "vamos usar um Stepper aqui" e dev entenda exatamente o que implementar. Kholmatova detalha como nomear, documentar e socializar patterns.


### 4. Pattern Libraries as Living Documents

A documentação de cada pattern deve incluir: nome, propósito, quando usar, quando não usar, variações, estados, acessibilidade, exemplos de uso real. A library é viva — patterns são adicionados, modificados e deprecados. O processo de evolução deve ser tão bem definido quanto o de criação.


### 5. Systematic Design Process

O processo de criação de um design system: (1) definir design principles, (2) inventariar padrões existentes, (3) identificar functional e perceptual patterns, (4) nomear e documentar, (5) criar governance model, (6) iterar baseado em feedback dos times consumidores.



## Application to Design Squad

- **Design principles workshop:** Conduzir workshop com squad para definir 4-6 princípios de design específicos ao produto. Testar cada princípio: é específico? Testável? Acionável? Ajuda a decidir?
- **Pattern audit dual:** Inventariar separadamente functional patterns e perceptual patterns. Isso revela inconsistências em ambas dimensões.
- **Naming convention:** Estabelecer convenção de nomenclatura para patterns. Socializar com engenharia para garantir alinhamento entre nome no Figma e nome no código.
- **Pattern documentation template:** Padronizar documentação de patterns com: propósito, quando usar, quando não usar, variações, estados, accessibility notes, exemplos.
- **Design principles em reviews:** Em cada design review, avaliar o trabalho contra os design principles documentados. Isso mantém os princípios vivos e relevantes.



## Key Takeaways

1. **Design system é linguagem, não biblioteca de componentes.** Sem princípios e linguagem compartilhada, uma coleção de componentes é apenas um catálogo.

2. **Functional + perceptual = sistema completo.** Componentes que funcionam mas não comunicam personalidade são genéricos demais.

3. **Princípios devem ser específicos e testáveis.** "Manter simples" não é princípio — "favorecer ação direta sobre menus hierárquicos" é.

4. **Nomenclatura é infraestrutura de comunicação.** O nome do pattern é a interface entre design e engenharia.

5. **O sistema evolui — governance é tão importante quanto criação.** Sem processo claro para adicionar, modificar e deprecar patterns, o sistema estagna ou fragmenta.



## Cross-References

- [Atomic Design — Frost](frost-atomic-design.md) — arquitetura de composição complementar
- [Design That Scales — Mall](mall-design-that-scales.md) — governança de design systems em escala
- [Design Systems Handbook — Suarez](suarez-design-systems-handbook.md) — visão prática complementar
- [Design Tokens Standard](../standards/design-tokens-standard-notes.md) — tokens como perceptual patterns codificados
- [Figma Library Governance](../tools/figma-library-governance.md) — governança na prática
