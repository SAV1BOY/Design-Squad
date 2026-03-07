# Storybook for Design Systems



## Metadata

- **Ferramenta:** Storybook
- **Categoria:** Design System Tooling, Component Documentation
- **Relevancia para o Squad:** Alta — documentacao viva de componentes em codigo
- **Ultima revisao:** 2026-03-06



## Summary

Storybook e a ferramenta padrao da industria para desenvolver, documentar e testar componentes de UI isoladamente. Para o design system, Storybook funciona como a "pattern library viva" — cada componente tem suas variacoes (stories), estados, props e documentacao renderizados em um ambiente interativo.

O valor do Storybook para designers e que ele serve como source of truth de implementacao — enquanto o Figma mostra a intencao de design, o Storybook mostra a realidade do codigo. Discrepancias entre Figma e Storybook sao bugs de implementacao que devem ser resolvidos.

Storybook 7+ trouxe melhorias significativas: Component Story Format 3 (CSF3), Autodocs (documentacao gerada automaticamente de props), Interaction Testing (testes de interacao dentro de stories) e Figma plugin (integração bidirecional Figma-Storybook).



## Key Concepts


### 1. Stories as Component Documentation

Cada story e um estado ou variacao do componente renderizado isoladamente. Button tem stories para: Default, Primary, Secondary, Disabled, Loading, With Icon, Small, Large. Stories servem como documentacao visual, caso de teste e especificacao de design — tudo em um artefato.


### 2. Autodocs and MDX

Autodocs gera documentacao automaticamente a partir de props e JSDoc comments do componente. MDX permite combinar Markdown com componentes interativos para documentacao rica. O resultado e documentacao que nunca diverge do codigo porque e gerada dele.


### 3. Addons Ecosystem

Addons estendem Storybook: a11y addon (verificacao de acessibilidade automatica), Design addon (embed de Figma frames), Viewport addon (testar responsiveness), Interactions addon (testes de interacao), Chromatic (visual regression testing). O ecosystem de addons transforma Storybook em plataforma de qualidade.


### 4. Visual Regression Testing (Chromatic)

Chromatic (pelo time do Storybook) captura screenshots de cada story e detecta mudancas visuais entre commits. Isso previne regressoes visuais involuntarias — se um componente mudou, alguem deve aprovar a mudanca. E como code review, mas para pixels.


### 5. Design-Dev Bridge

Storybook com Figma plugin cria ponte bidirecional: designers veem a implementacao real no Storybook linkada ao componente Figma; developers veem o design original linkado a cada story. Isso reduz o gap de handoff e torna discrepancias visiveis.



## Application to Design Squad

- **Storybook como referencia de implementacao:** Em duvida se o componente esta implementado corretamente, consultar Storybook, nao o Figma. Storybook e a realidade; Figma e a intencao.
- **a11y addon obrigatorio:** Instalar e configurar o addon de acessibilidade. Todo componente deve passar nas verificacoes automaticas antes de merge.
- **Figma links em stories:** Linkar cada story ao frame correspondente no Figma. Isso facilita comparacao e identificacao de discrepancias.
- **Visual regression no CI:** Implementar Chromatic ou similar no pipeline de CI. Mudancas visuais involuntarias sao detectadas automaticamente.
- **Designer review em Storybook:** Designers devem revisar novos componentes no Storybook (nao apenas no PR) antes de aprovar a implementacao.



## Key Takeaways

1. **Storybook e a pattern library viva.** Se nao esta no Storybook, nao existe no design system implementado.

2. **Autodocs elimina documentacao desatualizada.** Documentacao gerada do codigo nunca diverge da realidade.

3. **Visual regression testing previne surpresas.** Mudancas visuais involuntarias sao detectadas antes de chegar a producao.

4. **Acessibilidade automatizada e baseline.** O addon de a11y nao substitui testes manuais, mas catch problemas obvios automaticamente.

5. **Figma-Storybook bridge reduz handoff.** Linkar design e implementacao torna discrepancias visiveis e acionaveis.



## Cross-References

- [Figma Library Governance](figma-library-governance.md) — lado design da ponte
- [Design Tokens Standard](../standards/design-tokens-standard-notes.md) — tokens consumidos pelo Storybook
- [Handoff and Dev Collab](handoff-and-dev-collab.md) — processo de handoff
- [Accessibility Tools](accessibility-tools.md) — ferramentas complementares de a11y
- [Atomic Design — Frost](../books/frost-atomic-design.md) — estrutura de componentes
