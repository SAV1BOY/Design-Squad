# Color Psychology in UI



## Metadata

- **Categoria:** Visual Design, Psychology, Brand
- **Relevancia para o Squad:** Media — como cor influencia percepcao e comportamento
- **Ultima revisao:** 2026-03-06



## Summary

Cor e um dos elementos mais poderosos de comunicacao visual — transmite emocao, hierarquia, significado e identidade de marca. Mas a psicologia das cores e mais nuanceada que tabelas simplistas ("azul = confianca, vermelho = urgencia"). Contexto cultural, contexto de uso e combinacao de cores importam mais que significado isolado de uma cor.



## Key Concepts


### 1. Functional Color in UI

Vermelho para erro/destructivo, verde para sucesso/confirmacao, amarelo para warning, azul para informacao/links. Essas associacoes sao convencoes fortes no digital. Desviar dessas convencoes (verde para erro) causa confusao. Funcional > estetico para estados de sistema.


### 2. Cultural Context

Significados variam entre culturas: branco e luto na Asia e pureza no Ocidente; vermelho e sorte na China e perigo no Ocidente. Para produtos globais (ou Brasil com diversidade cultural), depender de cor como unico comunicador e arriscado.


### 3. Color and Accessibility

8% dos homens e 0.5% das mulheres tem daltonismo. Nunca usar cor como unico diferenciador de informacao. Combinacoes problematicas: vermelho/verde (deuteranopia), azul/amarelo (tritanopia). Sempre adicionar segundo indicador (icone, texto, forma).


### 4. Color Hierarchy and Emphasis

Cor primaria de marca como accent para CTAs e acoes principais. Neutrals (cinzas) para conteudo e estrutura. Semantic colors (vermelho, verde, amarelo) para estados. A hierarquia de cor guia atencao: quanto mais cor, mais atencao — usar com moderacao.


### 5. Dark Mode Considerations

Em dark mode, cores claras sobre fundo escuro. Cores vibrantes precisam ser dessaturadas para evitar vibração visual. Superficies usam cinza (nao preto puro #000) para profundidade. Semantic colors (erro, sucesso) podem precisar de ajuste para manter contraste em dark mode.



## Application to Design Squad

- **Color system documentado:** Definir e documentar no design system: cor primaria (brand), secundaria, neutrals (escala de cinza), semantic colors (error, success, warning, info). Cada cor com variantes (50-900) para flexibilidade.
- **Color accessibility check:** Todo uso de cor deve ter segundo indicador. Verificar com simulador de daltonismo. Contraste minimo WCAG 2.2 AA para texto (4.5:1) e UI components (3:1).
- **Dark mode tokens:** Se o produto tem dark mode, definir token layer separado com cores ajustadas para contraste e legibilidade em fundo escuro.
- **Color sparingly:** Usar cor de marca como accent, nao como background dominante. Interfaces com excesso de cor saturada causam fadiga visual.
- **Cultural sensitivity:** Para produtos no Brasil e LATAM, validar que associacoes de cor funcionam para a base de usuarios diversa.



## Key Takeaways

1. **Cor funcional segue convencoes.** Vermelho = erro, verde = sucesso. Nao reinvente.

2. **Cor nunca e o unico indicador.** Acessibilidade exige sempre segundo canal (icone, texto, forma).

3. **Menos cor = mais impacto.** Interfaces com poucas cores de accent se destacam mais que as vibrantes.

4. **Contexto cultural importa.** Significados de cor variam entre culturas e gerações.

5. **Dark mode nao e inversao.** Requer paleta ajustada para contraste, dessaturacao e profundidade.



## Cross-References

- [WCAG 2.x Notes](../standards/wcag-2-x-notes.md) — contraste de cor
- [Accessibility Tools](../tools/accessibility-tools.md) — ferramentas de verificacao
- [Gestalt Principles](gestalt-principles-deep-dive.md) — similarity por cor
- [Elements of Typographic Style — Bringhurst](../books/bringhurst-elements-of-typographic-style.md) — cor e tipografia
- [Design Tokens Standard](../standards/design-tokens-standard-notes.md) — tokens de cor
