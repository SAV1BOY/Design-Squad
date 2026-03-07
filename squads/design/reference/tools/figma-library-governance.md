# Figma Library Governance



## Metadata

- **Ferramenta:** Figma
- **Categoria:** Design System Tooling, Library Management
- **Relevancia para o Squad:** Alta — governanca da principal ferramenta de design
- **Ultima revisao:** 2026-03-06



## Summary

A governanca da library do Figma e o processo que garante que a biblioteca de componentes permaneca consistente, atualizada e adotada pelo time. Sem governanca, libraries se fragmentam — cada designer cria variantes locais, componentes ficam desatualizados e a promessa de consistencia do design system se dissolve.

Este documento cobre estrategias para estruturacao de arquivos, naming conventions, versionamento de componentes, processo de contribuicao, auditoria de adocao e manutencao continua. A governanca nao e sobre controle — e sobre tornar facil usar o sistema corretamente e dificil usa-lo incorretamente.

O Figma evoluiu significativamente com Dev Mode, Variables (tokens), Component Properties e Auto Layout, tornando possible uma library que serve tanto designers quanto developers. A governanca deve acompanhar essas capabilities — nao faz sentido governar uma library de 2020 com ferramentas de 2024.



## Key Concepts


### 1. File Structure and Organization

Estrutura recomendada: arquivo de Foundations (tokens/variables — cores, tipografia, espacamento, sombras), arquivo de Components (atomos, moleculas, organismos), arquivo de Icons, arquivo de Patterns (composicoes de componentes para cenarios comuns). Cada arquivo e uma library publicada separadamente.


### 2. Naming Conventions

Componentes: Category/Component/Variant (ex: Forms/Input/Default, Forms/Input/Error). Variables: tier/category/name (ex: ref/color/blue-500, sys/color/primary). Layers internas: descritivas e consistentes (Container, Label, Icon, Slot). Naming e o contrato entre Figma e codigo.


### 3. Component Properties and Variants

Usar Component Properties para expor customizacoes sem criar variantes excessivas: boolean properties (show icon: true/false), text properties (label: "Button"), instance swap properties (icon: Arrow/Check/Close). Variants para diferenciacoes visuais significativas (size: sm/md/lg, state: default/hover/active).


### 4. Variables for Tokens

Figma Variables como implementacao de design tokens: Color variables para temas (light/dark), Number variables para espacamento e sizing, String variables para feature flags. Modes para theming (Light Mode, Dark Mode) aplicados a frames.


### 5. Contribution and Publishing Process

Processo de contribuicao: proposta (brief com problema e solucao) > design review (conformidade com guidelines) > QA (naming, properties, auto layout) > publicacao (publish com release notes) > comunicacao (changelog no canal do squad). Cada etapa tem dono e checklist.



## Application to Design Squad

- **Library audit trimestral:** Revisar toda a library a cada trimestre: componentes desatualizados, variantes nao usadas, inconsistencias de naming. Usar Figma analytics para identificar componentes mais e menos usados.
- **Contribution guide documentado:** Publicar guia de contribuicao com templates, checklists e exemplos. Todo designer deve poder propor novo componente seguindo o guia.
- **Naming enforcement:** Usar plugin de linting para verificar naming conventions em novos componentes antes de publicacao.
- **Variables como single source:** Migrar todos os tokens para Figma Variables. Nenhum valor hardcoded em componentes — tudo via variables.
- **Changelog por release:** Cada publicacao de library deve ter release notes com: novos componentes, mudancas em existentes, deprecacoes e migration notes.



## Key Takeaways

1. **Naming e o contrato mais importante.** Se o nome no Figma nao corresponde ao nome no codigo, o sistema esta quebrado.

2. **Component Properties reduzem complexidade.** Menos variantes, mais properties configuráveis resulta em library mais manutenivel.

3. **Variables sao tokens no Figma.** Adotar Variables para todos os valores de design conecta Figma ao pipeline de tokens.

4. **Governanca e processo, nao restricao.** O objetivo e tornar facil fazer certo, nao difícil fazer qualquer coisa.

5. **Audit regular previne degradacao.** Sem auditoria, a library degrada silenciosamente ate perder confianca do time.



## Cross-References

- [Design Tokens Standard](../standards/design-tokens-standard-notes.md) — tokens que as Variables implementam
- [Design Token Tools](design-token-tools.md) — pipeline de tokens Figma-to-code
- [Storybook for Design Systems](storybook-for-design-systems.md) — espelho da library no codigo
- [Atomic Design — Frost](../books/frost-atomic-design.md) — hierarquia de componentes
- [Design That Scales — Mall](../books/mall-design-that-scales.md) — governanca organizacional
