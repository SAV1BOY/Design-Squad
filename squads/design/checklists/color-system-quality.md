# Color System Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Visual Design
- **Version:** 1.0.0
- **Owner Agent:** Color System Agent

## Objective
Assegurar que o sistema de cores seja acessivel, semanticamente estruturado e escalavel para diferentes temas e plataformas.
Um color system bem projetado garante consistencia visual e comunicacao eficaz de estados e hierarquias.

## When to Apply
- Ao definir ou reestruturar a paleta de cores do produto.
- Ao introduzir dark mode ou novos temas visuais.
- Ao auditar a acessibilidade cromatica do produto.

## Criteria
- [ ] A paleta possui cores primarias, secundarias e de acento claramente definidas
- [ ] As cores semanticas (success, warning, error, info) estao definidas e sao intuitivas
- [ ] Todas as combinacoes de foreground/background atendem WCAG AA (4.5:1 para texto)
- [ ] As cores de interacao (hover, active, focus, disabled) estao definidas
- [ ] O sistema funciona em dark mode e light mode com mapeamento documentado
- [ ] A paleta inclui escalas de neutrals suficientes para hierarquia de conteudo
- [ ] As cores nao dependem exclusivamente de matiz para comunicar informacao (colorblind-safe)
- [ ] Os color tokens estao organizados em camadas (primitive, semantic, component)
- [ ] A paleta e testada em diferentes monitores e dispositivos moveis
- [ ] Existe documentacao de uso indicando quando e onde cada cor deve ser aplicada
- [ ] As cores de overlay e surface estao definidas com opacidades documentadas
- [ ] O sistema de cores suporta data visualization com paleta dedicada
- [ ] O contraste entre elementos interativos e nao interativos e perceptivel
- [ ] As cores foram testadas com simuladores de daltonismo (protanopia, deuteranopia, tritanopia)
- [ ] A paleta e escalavel para adicao de novos temas sem reestruturacao

## Severity Guide

### Critico
- Combinacoes de cores que falham WCAG AA para texto.
- Informacao comunicada exclusivamente por cor sem indicadores alternativos.
- Cores semanticas confusas (ex: verde para erro).

### Major
- Dark mode nao planejado quando o produto requer suporte.
- Falta de escalas de neutrals para hierarquia visual.
- Color tokens nao estruturados em camadas semanticas.

### Minor
- Documentacao de uso incompleta para cores secundarias.
- Cores nao testadas em dispositivos de baixa qualidade.
- Paleta de data visualization nao definida.

## Cross-References
- [Typography Quality](typography-quality.md)
- [UI Visual Quality](ui-visual-quality.md)
- [Token Quality](token-quality.md)
- [Accessibility Quality](accessibility-quality.md)
- [Design System Quality](design-system-quality.md)
