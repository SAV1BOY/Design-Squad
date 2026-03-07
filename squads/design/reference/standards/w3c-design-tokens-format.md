# W3C Design Tokens Format — Technical Notes



## Metadata

- **Organizacao:** Design Tokens Community Group (W3C)
- **Status:** Editors' Draft (em evolucao)
- **Categoria:** Technical Standard, Design-Dev Bridge
- **Relevancia para o Squad:** Media — referencia tecnica para implementacao de tokens
- **Ultima revisao:** 2026-03-06



## Summary

O W3C Design Tokens Community Group esta desenvolvendo um formato padrao para representar design tokens de forma interoperavel. O formato usa JSON como base, com convencoes especificas para tipos de valor, aliases, grouping e metadata. O objetivo e que qualquer ferramenta (Figma, Style Dictionary, Tokens Studio, qualquer plataforma) possa importar/exportar tokens no mesmo formato.

A spec define tipos de token (color, dimension, fontFamily, fontWeight, duration, cubicBezier, shadow, strokeStyle, border, transition, gradient, typography), cada um com formato de valor especifico. Aliases permitem que tokens referenciem outros tokens, criando a hierarquia de tres niveis (reference > system > component).

Embora a spec ainda nao seja final (editors' draft), ferramentas como Tokens Studio e Style Dictionary ja suportam o formato, tornando a adocao pratica mesmo antes da finalizacao oficial. O formato esta convergindo e mudancas significativas sao improvaveis.



## Key Concepts


### 1. JSON Structure

Tokens sao definidos em JSON com propriedades prefixadas por $: $value (valor), $type (tipo), $description (descricao). Groups organizam tokens em objetos aninhados sem $ prefix. Exemplo: { "color": { "primary": { "$value": "#0066FF", "$type": "color" } } }.


### 2. Type System

Cada tipo de token tem formato de valor definido: color (hex string #RRGGBB), dimension (number + unit "16px"), duration ("200ms"), cubicBezier (array de 4 numeros), shadow (objeto com offsetX, offsetY, blur, spread, color), typography (composite com fontFamily, fontSize, fontWeight, lineHeight).


### 3. Aliases (References)

Tokens podem referenciar outros tokens usando sintaxe de chaves: { "$value": "{color.primary}" }. Isso permite a hierarquia de tres niveis: reference tokens definem valores, system tokens alias reference tokens, component tokens alias system tokens. Aliases criam dependencias rastreáveis.


### 4. Composite Tokens

Alguns tipos sao compostos de multiplos valores: typography (fontFamily + fontSize + fontWeight + lineHeight + letterSpacing), shadow (offsetX + offsetY + blur + spread + color), border (color + width + style). Composites agrupam decisoes relacionadas em um unico token.


### 5. Extensions ($extensions)

O formato suporta extensoes custom via $extensions para metadata especifico de ferramentas ou organizacoes. Exemplo: informacoes de Figma (figma-style-id), categorias custom, ou metadata de auditoria. Extensions nao afetam a interoperabilidade do formato base.



## Application to Design Squad

- **Adotar o formato DTCG:** Definir todos os tokens no formato W3C DTCG. Mesmo que a spec evolua, a base esta estavel e migracao sera incremental.
- **Type safety:** Usar $type em todos os tokens para garantir que ferramentas processem valores corretamente. Cor e sempre hex, dimensao sempre inclui unidade.
- **Alias chains:** Implementar aliases para criar hierarquia de tokens. Nunca hardcodar o mesmo valor em multiplos tokens — usar aliases para manter single source of truth.
- **Composite tokens para tipografia:** Usar o tipo typography para agrupar decisoes tipograficas. Isso garante que font-size nunca e alterado sem considerar line-height.
- **Extensions para metadata:** Usar $extensions para adicionar metadata especifico do time (categorias, ownership, deprecation date) sem quebrar interoperabilidade.



## Key Takeaways

1. **JSON com $ prefix e o formato emergente.** $value, $type, $description sao as propriedades core de cada token.

2. **Aliases criam hierarquia manutenivel.** Nunca duplique valores — use aliases para criar dependencias explicitas.

3. **Tipos garantem processamento correto.** $type permite que ferramentas validem e transformem tokens automaticamente.

4. **Composites agrupam decisoes relacionadas.** Typography como token unico e mais confiavel que font-size + line-height separados.

5. **O formato esta estavel o suficiente para adocao.** Ferramentas ja suportam; mudancas na spec serao incrementais.



## Cross-References

- [Design Tokens Standard Notes](design-tokens-standard-notes.md) — contexto conceitual
- [Design Token Tools](../tools/design-token-tools.md) — ferramentas que suportam o formato
- [Material Design Notes](material-design-notes.md) — token architecture do Material
- [Storybook for Design Systems](../tools/storybook-for-design-systems.md) — consumo de tokens
- [Figma Library Governance](../tools/figma-library-governance.md) — tokens no Figma
