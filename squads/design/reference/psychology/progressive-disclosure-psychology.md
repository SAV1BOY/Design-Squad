# Progressive Disclosure Psychology



## Metadata

- **Categoria:** Cognitive Psychology, Interaction Design
- **Relevancia para o Squad:** Alta — principio fundamental de gerenciamento de complexidade
- **Ultima revisao:** 2026-03-06



## Summary

Progressive disclosure e a estrategia de apresentar informacao em camadas, revelando complexidade gradualmente conforme o usuario precisa. Fundamentada em cognitive load theory, progressive disclosure reduz sobrecarga inicial e permite que novatos e experts usem a mesma interface com niveis diferentes de profundidade.



## Key Concepts


### 1. Cognitive Basis

Working memory limitada significa que apresentar tudo de uma vez sobrecarrega. Progressive disclosure permite que o usuario processe informacao em chunks gerenciaveis. Cada nivel revelado e processado antes do proximo.


### 2. Implementation Patterns

Accordions (expand/collapse), "Show more" / "Advanced options" buttons, tooltips e popovers, wizards/steppers, tabs e panels, contextual menus. Cada pattern tem contexto adequado — accordion para listas FAQ, wizard para fluxos sequenciais, tabs para conteudo paralelo.


### 3. Novice vs. Expert Paths

Novatos precisam de orientacao e simplicidade; experts precisam de acesso rapido a features avancadas. Progressive disclosure atende ambos: superficie simples para novatos, profundidade disponivel para experts. A chave e nao esconder tao profundo que experts nao encontrem.


### 4. Information Scent

Para que o usuario clique em "Show more," precisa acreditar que conteudo util esta la (information scent). Labels como "3 opcoes avancadas" sao mais tentadores que "Mais." O custo percebido de expandir deve ser menor que o beneficio esperado.


### 5. Progressive Disclosure vs. Hidden Features

Disclosure progressivo e intencional — o usuario sabe que mais existe e pode acessar. Features escondidas sao acidentais — o usuario nao sabe que existem. Progressive disclosure requer signifiers claros de que ha mais a descobrir.



## Application to Design Squad

- **Default to progressive disclosure:** Para qualquer feature com mais de 5 opcoes ou configuracoes, usar progressive disclosure como default. Mostrar essencial, revelar avancado sob demanda.
- **Information scent auditing:** Verificar se labels de "expandir" comunicam o que sera revelado. "Opcoes avancadas (3)" e melhor que "Mais."
- **Novice/expert testing:** Testar fluxos com usuarios novatos (encontram o essencial?) e experts (encontram o avancado rapidamente?). Ambos devem ser atendidos.
- **Disclosure depth limit:** Maximo 2 niveis de disclosure (surface > expanded). Se precisa de 3+ niveis, a information architecture precisa ser repensada.
- **Consistent disclosure patterns:** Padronizar como disclosure funciona no design system: mesmo icone (chevron), mesma animacao, mesmo comportamento.



## Key Takeaways

1. **Moste o necessario, revele o resto.** Superficie simples com profundidade acessivel atende novatos e experts.

2. **Information scent e essencial.** O usuario precisa saber que mais existe e querer clicar.

3. **Maximo 2 niveis de profundidade.** Se precisa de mais, reorganize a informacao.

4. **Consistencia de pattern importa.** O usuario deve reconhecer "aqui tem mais" pelo padrao visual.

5. **Escondido nao e disclosure.** Se o usuario nao sabe que existe, nao e progressive disclosure — e feature oculta.



## Cross-References

- [Cognitive Load Theory](cognitive-load-theory.md) — base teorica
- [Don't Make Me Think — Krug](../books/krug-dont-make-me-think.md) — menos e mais
- [Settings and Preferences Patterns](../ui-patterns/settings-and-preferences-patterns.md) — disclosure em settings
- [Forms and Validation Patterns](../ui-patterns/forms-and-validation-patterns.md) — disclosure em forms
- [Designing Interfaces — Tidwell](../books/tidwell-designing-interfaces.md) — collapsible patterns
