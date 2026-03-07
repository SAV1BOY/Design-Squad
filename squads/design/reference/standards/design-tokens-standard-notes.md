# Design Tokens Standard — Notes



## Metadata

- **Organizacao:** Design Tokens Community Group (W3C)
- **Status:** Em desenvolvimento (spec editors' draft)
- **Categoria:** Design Systems, Design-Dev Bridge
- **Relevancia para o Squad:** Alta — fundamento tecnico do design system
- **Ultima revisao:** 2026-03-06



## Summary

Design tokens sao as unidades atomicas de decisao de design — valores nomeados que representam escolhas como cor, tipografia, espacamento, sombra e motion. O Design Tokens Community Group da W3C esta desenvolvendo um formato padrao (DTCG) para representar tokens de forma interoperavel entre ferramentas de design, plataformas de desenvolvimento e documentacao.

Tokens resolvem o problema de traduzir decisoes de design para codigo de forma consistente e manutenivel. Em vez de hardcodar #0066FF em CSS, Swift e Kotlin, o token color.action.primary e definido uma vez e transformado para cada plataforma. Mudancas de marca ou theming se propagam automaticamente.

A importancia de tokens cresce com a escala: para um produto pequeno, CSS variables sao suficientes. Para ecosistemas multi-plataforma (web, iOS, Android, email), tokens com formato padronizado e pipeline de transformacao (Style Dictionary, Tokens Studio) sao infraestrutura essencial.



## Key Concepts


### 1. Token Types

Color, dimension (spacing, sizing), font family, font weight, font size, line height, duration (animation timing), cubic bezier (easing), shadow, border, gradient, typography (composite). Cada tipo tem formato de valor e transformacoes especificas por plataforma.


### 2. Token Tiers (Reference, System, Component)

Reference tokens: valores primitivos sem semantica (blue-500: #0066FF). System tokens: decisoes semanticas (color-action-primary: {blue-500}). Component tokens: aplicacao especifica (button-primary-bg: {color-action-primary}). Os tres niveis permitem theming em qualquer camada.


### 3. DTCG Format (W3C Standard)

O formato padronizado usa JSON com estrutura definida: cada token tem $value (valor), $type (tipo), $description (documentacao). Groups organizam tokens hierarquicamente. Aliases referenciam outros tokens com {}. O formato permite interoperabilidade entre ferramentas.


### 4. Token Transformation Pipeline

Tokens sao definidos uma vez (source of truth) e transformados para cada plataforma: CSS custom properties, SCSS variables, Swift enums, Kotlin objects, XML resources. Style Dictionary (Amazon) e a ferramenta mais usada para essa transformacao.


### 5. Theming and Multi-Brand

Tokens permitem theming (dark mode, high contrast) e multi-brand (white-label) trocando a camada de reference tokens sem alterar system ou component tokens. Isso separa decisoes de marca de decisoes de UX — permitindo que o mesmo componente funcione para multiplas marcas.



## Application to Design Squad

- **Token-first design system:** Toda decisao de design (cor, tamanho, espaco) deve ser expressa como token antes de ser usada em componentes. Nenhum valor hardcoded no design system.
- **Three-tier adoption:** Implementar os tres niveis de tokens. Comecar com reference e system; adicionar component tokens quando componentes estiverem estabilizados.
- **Figma-to-code pipeline:** Usar Tokens Studio (plugin Figma) para definir tokens no Figma e exportar em formato DTCG para transformacao via Style Dictionary.
- **Dark mode via tokens:** Implementar dark mode como troca de reference tokens. System e component tokens permanecem identicos — apenas a base muda.
- **Token documentation:** Cada token deve ter nome semantico, valor, descricao e contexto de uso documentados. Tokens sem descricao sao debito de documentacao.



## Key Takeaways

1. **Tokens sao o contrato entre design e codigo.** Sem tokens, cada implementacao reinterpreta decisoes de design.

2. **Tres niveis de abstracão permitem flexibilidade.** Reference (branding) > System (semantica) > Component (implementacao).

3. **O formato DTCG esta se tornando padrao.** Adotar agora facilita interoperabilidade futura entre ferramentas.

4. **Theming e multi-brand sao features de tokens, nao de componentes.** Trocar tokens troca o visual sem alterar logica.

5. **Pipeline de transformacao e infraestrutura critica.** Tokens definidos sem pipeline de exportacao nao chegam ao codigo.



## Cross-References

- [W3C Design Tokens Format](w3c-design-tokens-format.md) — spec tecnica do formato
- [Design Token Tools](../tools/design-token-tools.md) — ferramentas de token management
- [Atomic Design — Frost](../books/frost-atomic-design.md) — tokens como atoms
- [Design Systems Handbook — Suarez](../books/suarez-design-systems-handbook.md) — token architecture
- [Figma Library Governance](../tools/figma-library-governance.md) — tokens no Figma
