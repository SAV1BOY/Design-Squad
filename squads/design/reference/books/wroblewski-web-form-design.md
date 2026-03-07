# Web Form Design — Luke Wroblewski



## Metadata

- **Autor:** Luke Wroblewski
- **Publicacao:** 2008
- **Categoria:** Form Design, UI Patterns, Conversion Optimization
- **Relevancia para o Squad:** Alta — formulários são o ponto de conversão crítico
- **Ultima revisao:** 2026-03-06



## Summary

Web Form Design é a referência definitiva sobre design de formulários — os elementos de interface que mais diretamente impactam conversão e receita. Wroblewski argumenta que formulários são frequentemente o último passo entre intenção e ação, e por isso merecem atenção desproporcional. O livro cobre cada aspecto do design de formulários: layout, labels, inputs, validação, feedback, e organização.

Baseado em extenso eye-tracking research e testes de usabilidade, Wroblewski demonstra com dados o impacto de decisões aparentemente triviais: label acima vs. ao lado do campo, validação inline vs. ao submeter, placeholder text vs. labels persistentes. Cada recomendação é fundamentada em research, não em opinião.

Embora publicado em 2008, os princípios permanecem válidos e foram confirmados por pesquisa subsequente. O livro é complementado pelos artigos contínuos de Wroblewski sobre mobile form design, que expandem as recomendações para touch interfaces.



## Key Concepts


### 1. Form Layout (Top-Aligned vs. Left-Aligned vs. Right-Aligned Labels)

Eye-tracking research mostra que labels acima dos campos (top-aligned) resultam em preenchimento mais rápido porque olho e campo estão no mesmo eixo vertical. Labels à esquerda alinhados à direita são o segundo melhor. Labels à esquerda alinhados à esquerda criam maior distância visual e são mais lentos.


### 2. Input Types and Affordances

Cada tipo de dado merece o input correto: dropdowns para listas curtas (< 7 itens), radio buttons para escolhas exclusivas visíveis, checkboxes para múltipla seleção, text inputs para dados livres. O tipo de input comunica ao usuário que tipo de resposta é esperada — affordance informacional.


### 3. Inline Validation

Validação em tempo real (enquanto o usuário preenche) é significativamente superior à validação apenas no submit. Reduz erros em até 22% e tempo de preenchimento em até 42% segundo os estudos citados. A validação deve ser positiva (confirmar o correto) tanto quanto negativa (apontar erros).


### 4. Progressive Disclosure in Forms

Mostrar apenas os campos relevantes ao contexto atual. Conditional logic (campos que aparecem baseados em respostas anteriores), smart defaults (valores pré-preenchidos quando possível) e form segmentation (dividir formulários longos em steps) reduzem perceived complexity.


### 5. Error Prevention and Recovery

Hierarquia de estratégias: prevenir erros (constraints, smart defaults) > validar inline (feedback imediato) > comunicar erros claramente (mensagem específica, próxima ao campo, com instrução de correção). Mensagens de erro genéricas ("campo inválido") são inúteis — devem dizer o que fazer ("use formato DD/MM/AAAA").



## Application to Design Squad

- **Form design guidelines:** Padronizar layout de formulários no design system: labels top-aligned como default, inline validation obrigatória, mensagens de erro específicas e acionáveis.
- **Input type matrix:** Documentar no design system qual input type usar para cada tipo de dado (email, phone, date, selection, etc.), incluindo variações mobile.
- **Conversion audit de formulários:** Auditar regularmente os formulários críticos do produto (signup, checkout, configurações) com métricas de abandono por campo e tempo de preenchimento.
- **Progressive disclosure por default:** Formulários com mais de 5 campos devem usar progressive disclosure (steps ou conditional logic) a menos que haja razão específica para não fazê-lo.
- **Error message library:** Manter biblioteca de mensagens de erro específicas e acionáveis para cada tipo de validação, reutilizável em todo o produto.



## Key Takeaways

1. **Labels acima dos campos como padrão.** Top-aligned labels são mais rápidos e funcionam melhor em mobile. Use como default no design system.

2. **Inline validation é obrigatória, não opcional.** O custo de implementação é baixo comparado ao impacto em conversão e satisfação.

3. **Cada campo a menos aumenta conversão.** Questione cada campo: é realmente necessário neste momento? Pode ser coletado depois? Pode ser inferido?
4. **Mensagens de erro devem ser instruções de correção.** "Campo inválido" não ajuda. "Use apenas números, sem espaços" resolve o problema.

5. **Progressive disclosure reduz abandono.** Formulários longos assustam. Dividir em steps com progress indicator aumenta completion rate.



## Cross-References

- [Forms and Validation Patterns](../ui-patterns/forms-and-validation-patterns.md) — padrões de implementação
- [Data Input Patterns](../ui-patterns/data-input-patterns.md) — padrões de input para diferentes tipos de dados
- [Cognitive Load Theory](../psychology/cognitive-load-theory.md) — por que progressive disclosure funciona
- [Don't Make Me Think — Krug](krug-dont-make-me-think.md) — princípios de usabilidade aplicados a forms
- [100 Things — Weinschenk](weinschenk-100-things.md) — psicologia por trás do comportamento em formulários
