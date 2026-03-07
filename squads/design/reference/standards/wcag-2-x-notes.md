# WCAG 2.x — Web Content Accessibility Guidelines



## Metadata

- **Organizacao:** W3C (Web Accessibility Initiative)
- **Versao atual:** 2.2 (2023), 2.1 (2018)
- **Categoria:** Accessibility Standards
- **Relevancia para o Squad:** Alta — compliance obrigatorio de acessibilidade
- **Ultima revisao:** 2026-03-06



## Summary

As Web Content Accessibility Guidelines (WCAG) sao o padrao internacional para acessibilidade de conteudo web. Organizadas em quatro principios (Perceivable, Operable, Understandable, Robust — POUR), as guidelines definem criterios de sucesso em tres niveis de conformidade: A (minimo), AA (recomendado) e AAA (ideal).

WCAG 2.1 adicionou criterios para mobile, low vision e cognitive disabilities. WCAG 2.2 expandiu com foco em cognitive accessibility, dragging movements e consistent help. O padrao e referenciado por legislacoes em dezenas de paises, incluindo o Brasil (LBI — Lei Brasileira de Inclusao) e a UE (European Accessibility Act).

Para o squad de design, WCAG nao e apenas compliance legal — e framework de qualidade que beneficia todos os usuarios. Contraste adequado ajuda quem usa o produto ao sol; labels claros ajudam quem esta com pressa; navegacao por teclado ajuda power users tanto quanto usuarios de assistive technology.



## Key Concepts


### 1. POUR Principles

Perceivable: conteudo deve ser apresentavel em formas que o usuario possa perceber (alt text, captions, contraste). Operable: interface deve ser operavel por todos (teclado, tempo suficiente, sem seizure triggers). Understandable: conteudo e operacao devem ser compreensíveis (linguagem clara, previsibilidade). Robust: conteudo deve ser interpretavel por assistive technologies.


### 2. Conformance Levels (A, AA, AAA)

Level A: barreiras mais severas removidas (alt text, keyboard access). Level AA: a maioria dos usuarios com deficiencia pode usar (contraste 4.5:1, resize text, focus visible). Level AAA: acessibilidade maxima (contraste 7:1, sign language, reading level). AA e o target padrao da industria e da legislacao.


### 3. Key Criteria for Designers

1.4.3 Contrast Minimum (AA): texto normal 4.5:1, texto grande 3:1. 1.4.11 Non-text Contrast (AA): componentes de UI e graficos 3:1. 2.4.7 Focus Visible (AA): indicador de foco visivel para navegacao por teclado. 2.5.8 Target Size Minimum (AA - 2.2): alvos de toque minimo 24x24px.


### 4. Color Independence

Informacao nao deve ser transmitida apenas por cor. Links devem ter indicador alem de cor (underline). Erros em formularios devem ter icone ou texto alem de borda vermelha. Graficos devem ser legiveis em escala de cinza.


### 5. Cognitive Accessibility (WCAG 2.2)

Novos criterios focados em usuarios com dificuldades cognitivas: Consistent Help (3.2.6 — ajuda em posicao consistente), Redundant Entry (3.3.7 — nao pedir informacao ja fornecida), Accessible Authentication (3.3.8 — nao depender de memoria para autenticacao).



## Application to Design Squad

- **AA como baseline:** Estabelecer WCAG 2.2 Level AA como requisito minimo para todo design. Incluir criterios de acessibilidade em definition of done.
- **Contrast checker integrado:** Usar plugin de verificacao de contraste no Figma para todo design. Nenhum texto ou componente de UI deve ser publicado abaixo dos ratios minimos.
- **Focus state no design system:** Todo componente interativo deve ter focus state documentado no design system. Nao depender apenas do default do browser.
- **Color-independent design:** Em todo uso de cor para comunicar status (erro, sucesso, alerta), adicionar segundo indicador (icone, texto, forma). Validar com simulacao de daltonismo.
- **Accessibility checklist em reviews:** Incluir checklist de acessibilidade em cada design review: contraste, keyboard access, alt text, focus order, target size.



## Key Takeaways

1. **AA e o padrao, nao o objetivo aspiracional.** Legislacao global e a industria convergem para AA como minimo.

2. **Acessibilidade beneficia todos os usuarios.** Contraste adequado ajuda ao sol, labels claros ajudam com pressa, keyboard nav ajuda power users.

3. **Cor nunca e o unico indicador.** Sempre fornecer segundo canal de informacao alem de cor.

4. **Focus states sao design, nao afterthought.** Todo componente interativo precisa de focus state documentado e implementado.

5. **Acessibilidade no inicio, nao no final.** Retrofitar acessibilidade custa 10x mais que projetar acessivel desde o inicio.



## Cross-References

- [ARIA Authoring Practices](aria-authoring-practices.md) — como implementar ARIA corretamente
- [Accessibility Tools](../tools/accessibility-tools.md) — ferramentas de verificacao
- [Forms and Validation Patterns](../ui-patterns/forms-and-validation-patterns.md) — formularios acessiveis
- [Color Psychology in UI](../psychology/color-psychology-in-ui.md) — uso de cor alem de decoracao
- [Design of Everyday Things — Norman](../books/norman-design-of-everyday-things.md) — constraints como acessibilidade
