# Design Token Tools



## Metadata

- **Categoria:** Design Systems Tooling, Design-Dev Bridge
- **Relevancia para o Squad:** Alta — ferramentas para gerenciar e distribuir tokens
- **Ultima revisao:** 2026-03-06



## Summary

Design token tools sao o pipeline que conecta decisoes de design (no Figma) a implementacao (no codigo). Sem esse pipeline, tokens existem apenas em documentacao — nao no produto real. Este documento mapeia as ferramentas que permitem definir, transformar, distribuir e consumir tokens em escala.





## Key Concepts


### 1. Token Definition (Source of Truth)

Figma Variables + Tokens Studio: definir tokens diretamente no Figma com Tokens Studio plugin, que exporta em formato DTCG (W3C). Alternativa: definir tokens em JSON/YAML em repositorio Git como source of truth, sincronizar com Figma via plugin.


### 2. Token Transformation (Style Dictionary)

Style Dictionary (Amazon) transforma tokens de formato padrao (DTCG JSON) para formatos de cada plataforma: CSS custom properties, SCSS variables, iOS Swift/UIKit, Android XML/Compose, JSON para docs. Custom transforms permitem adaptar output a qualquer plataforma.


### 3. Token Distribution

Publicar tokens transformados como pacote (npm, CocoaPods, Maven). Cada plataforma consome o pacote como dependencia. Versionamento semantico garante que updates nao quebram consumidores. CI/CD publica automaticamente quando tokens mudam.


### 4. Token Visualization and Documentation

Storybook com addon de tokens para visualizar tokens renderizados. Zeroheight ou Supernova para documentacao de tokens com preview visual. A documentacao deve mostrar token name, value, visual preview e contexto de uso.


### 5. Token Governance

Processo para adicionar/modificar/deprecar tokens: proposta > review > implementacao > publicacao > comunicacao. Tokens deprecated devem ter replacement indicado e prazo de remocao. Governance previne token bloat (acumulo de tokens sem uso).



## Application to Design Squad

- **Tokens Studio como bridge:** Instalar e configurar Tokens Studio no Figma como bridge entre Figma Variables e formato DTCG. Definir tokens no Figma, exportar para Git.
- **Style Dictionary no pipeline:** Configurar Style Dictionary para transformar tokens em CSS, iOS e Android. Automatizar via CI — push em tokens.json trigger build e publicacao.
- **Token package publicado:** Publicar tokens como pacote npm consumido por todos os projetos. Cada projeto importa tokens, nao hardcoda valores.
- **Visual token docs:** Manter pagina de documentacao de tokens com preview visual, nome e contexto. Atualizada automaticamente quando tokens mudam.
- **Quarterly token audit:** Trimestralmente, auditar tokens: quais nao sao usados? Quais estao duplicados? Quais precisam de renomeacao? Cleanup regular previne bloat.



## Key Takeaways

1. **Tokens sem pipeline nao chegam ao codigo.** Definir tokens e metade do trabalho; transformar e distribuir e a outra metade.

2. **Figma-to-code pipeline deve ser automatizado.** Mudanca no Figma deve fluir automaticamente para codigo via CI/CD.

3. **Tokens sao pacote, nao arquivo.** Publicar como dependencia versionada garante consistencia e controlabilidade.

4. **Documentacao visual e essencial.** Tokens sao abstratos — sem preview visual, developers nao sabem o que estao usando.

5. **Governance previne token bloat.** Sem auditoria regular, tokens acumulam sem uso e perdem significado.



## Cross-References

- [Design Tokens Standard](../standards/design-tokens-standard-notes.md) — conceitos de tokens
- [W3C Design Tokens Format](../standards/w3c-design-tokens-format.md) — formato tecnico
- [Figma Library Governance](figma-library-governance.md) — tokens no Figma
- [Storybook for Design Systems](storybook-for-design-systems.md) — visualizacao de tokens
- [Design Systems Handbook — Suarez](../books/suarez-design-systems-handbook.md) — token architecture
