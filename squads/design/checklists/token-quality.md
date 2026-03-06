# Design Token Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Design Systems
- **Version:** 1.0.0
- **Owner Agent:** Token Management Agent

## Objective
Garantir que design tokens sejam bem estruturados, nomeados de forma semantica e sincronizados entre design e codigo.
Tokens bem gerenciados sao a base para temas, consistencia cross-platform e escalabilidade do design system.

## When to Apply
- Ao criar ou reestruturar a arquitetura de design tokens.
- Ao adicionar novos tokens para componentes ou features.
- Ao implementar suporte a temas (dark mode, brand themes, white-labeling).

## Criteria
- [ ] Os tokens estao organizados em camadas: primitive (global), semantic (alias) e component-specific
- [ ] A naming convention segue um padrao consistente e legivel (ex: color-background-primary)
- [ ] Os valores primitivos estao definidos em formatos padrao (HEX, RGB, rem, px)
- [ ] Os tokens semanticos abstraem o proposito, nao o valor (ex: color-error, nao color-red)
- [ ] Cada token possui descricao documentada sobre seu proposito e contexto de uso
- [ ] Os tokens de spacing seguem uma escala matematica consistente (4px base ou similar)
- [ ] Os tokens de tipografia cobrem font-family, font-size, font-weight, line-height e letter-spacing
- [ ] Os tokens de cor suportam tema claro e escuro com mapeamento documentado
- [ ] Os tokens de elevacao (shadow) estao definidos em niveis hierarquicos
- [ ] Os tokens de border-radius seguem uma escala consistente
- [ ] Os tokens de motion (duration, easing) estao definidos e documentados
- [ ] A fonte de verdade (source of truth) dos tokens esta claramente definida (Figma, JSON, YAML)
- [ ] O processo de sincronizacao entre design e codigo esta automatizado ou documentado
- [ ] Tokens deprecated possuem alternativas documentadas e timeline de remocao
- [ ] Os tokens sao validados em diferentes plataformas (web, iOS, Android) quando aplicavel
- [ ] Existe tooling para transformacao de tokens entre formatos (Style Dictionary ou similar)

## Severity Guide

### Critico
- Tokens nao sincronizados entre design e codigo gerando inconsistencias visuais.
- Naming convention inconsistente dificultando adocao.
- Ausencia de tokens semanticos, usando apenas valores hard-coded.

### Major
- Tokens de cor nao suportam temas quando o produto requer.
- Escala de spacing inconsistente entre componentes.
- Source of truth ambigua com valores conflitantes.

### Minor
- Descricoes de tokens ausentes mas nomes sao auto-explicativos.
- Tooling de transformacao nao automatizado mas funcional.
- Tokens de motion nao definidos em produto com pouca animacao.

## Cross-References
- [Design System Quality](design-system-quality.md)
- [Color System Quality](color-system-quality.md)
- [Typography Quality](typography-quality.md)
- [Component Spec Quality](component-spec-quality.md)
- [Motion Quality](motion-quality.md)
