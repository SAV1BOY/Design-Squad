# Design Systems Handbook — Marco Suarez et al.



## Metadata

- **Autores:** Marco Suarez, Jina Anne, Katie Sylor-Miller, Diana Mounter, Roy Stanfield
- **Publicacao:** 2017 (DesignBetter by InVision)
- **Categoria:** Design Systems, Implementation
- **Relevancia para o Squad:** Alta — guia prático de implementação de design systems
- **Ultima revisao:** 2026-03-06



## Summary

O Design Systems Handbook é um guia colaborativo escrito por practitioners de empresas como Salesforce, GitHub e Etsy. Diferente dos textos mais teóricos, este handbook foca na implementação real — como iniciar, construir, manter e escalar um design system em organizações com diferentes níveis de maturidade.

O livro aborda a realidade de design systems que incluem não apenas componentes visuais, mas design tokens, guidelines de voz e tom, padrões de acessibilidade, e processos de contribuição. Cada autor contribui com perspectiva de sua experiência, resultando em um guia diversificado que reconhece que não existe modelo único.

Jina Anne contribui especificamente sobre design tokens como camada de abstração entre decisões de design e implementação. Katie Sylor-Miller detalha a infraestrutura técnica necessária. Diana Mounter compartilha lições do Primer (design system do GitHub). O resultado é um guia completo e pragmático.



## Key Concepts


### 1. Design System Layers (Tokens, Components, Patterns, Guidelines)

Quatro camadas de abstração: tokens (valores atômicos — cores, espaçamentos, tipografia), components (elementos reutilizáveis construídos com tokens), patterns (combinações de componentes para resolver problemas), guidelines (documentação de quando e como usar tudo). Cada camada depende da inferior.


### 2. Starting Small and Iterating

Não tente construir o sistema completo de uma vez. Comece com um "starter kit" — tokens fundamentais, 5-10 componentes mais usados e uma página de documentação. Expanda baseado na demanda dos times consumidores, não em completude teórica. Suarez chama isso de "minimum viable design system."


### 3. Design Tokens Architecture

Tokens como camada de abstração que separa decisão de design (cor primária é #0066FF) de implementação (CSS variable, Swift color, Android resource). Permitem theming, dark mode e white-labeling sem alterar componentes. Jina Anne detalha a taxonomia: global tokens > alias tokens > component tokens.


### 4. Versioning and Change Management

Design systems precisam de versionamento semântico (semver): major (breaking changes), minor (novas features), patch (bug fixes). Times consumidores devem poder atualizar com confiança. Changelog detalhado, migration guides e deprecation notices são essenciais.


### 5. Measuring Adoption and Health

Métricas de health do sistema: adoption rate (% de componentes do sistema vs. custom), coverage (% de telas usando o sistema), freshness (versão do sistema em uso pelos times), contribution rate (novos componentes propostos por times consumidores), satisfaction (NPS interno do design system).



## Application to Design Squad

- **Minimum viable design system:** Se não existe sistema formal, começar com tokens + 10 componentes core + 1 página de docs. Expandir iterativamente baseado em demanda.
- **Token architecture:** Implementar três níveis de tokens: global (primitivos), alias (semânticos — ex: color-action-primary) e component (específicos — ex: button-color-primary). Documentar no design system.
- **Semver para o design system:** Adotar versionamento semântico. Publicar changelog a cada release. Nunca fazer breaking changes sem major version bump e migration guide.
- **Adoption dashboard:** Criar dashboard que rastreie adoção do sistema por squad/feature. Usar dados para priorizar gaps no sistema.
- **Contribution pipeline:** Documentar como um time consumidor pode propor novos componentes: template de proposta > review > aprovação > implementação > documentação > release.



## Key Takeaways

1. **Comece mínimo, itere baseado em demanda.** Um sistema pequeno usado é infinitamente mais valioso que um completo ignorado.

2. **Tokens são o fundamento invisível.** Sem token architecture, mudanças de marca ou theming requerem refatoração de cada componente.

3. **Versionamento semântico constrói confiança.** Times adotam o sistema quando confiam que updates não quebram suas interfaces.

4. **Meça adoção, não completude.** O sistema é saudável quando times o usam voluntariamente, não quando tem muitos componentes.

5. **O sistema é produto, precisa de roadmap.** Sem direção clara de evolução, o sistema estagna e os times criam workarounds.



## Cross-References

- [Atomic Design — Frost](frost-atomic-design.md) — arquitetura de componentes
- [Design Systems — Kholmatova](kholmatova-design-systems.md) — linguagem de padrões
- [Design That Scales — Mall](mall-design-that-scales.md) — governança organizacional
- [Design Tokens Standard](../standards/design-tokens-standard-notes.md) — standard de tokens
- [Storybook for Design Systems](../tools/storybook-for-design-systems.md) — implementação técnica
