# Responsive Breakpoints Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Responsive Design
- **Version:** 1.0.0
- **Owner Agent:** Responsive Design Agent

## Objective
Garantir que o design responsivo funcione de forma fluida em todos os breakpoints, mantendo usabilidade e hierarquia visual em qualquer tamanho de tela.
Um sistema de breakpoints bem definido evita experiencias quebradas e garante acessibilidade universal.

## When to Apply
- Ao definir a estrategia de breakpoints para um novo produto.
- Ao projetar layouts para features que devem funcionar em multiplos devices.
- Ao revisar a implementacao responsiva antes do lancamento.

## Criteria
- [ ] Os breakpoints estao definidos com base em conteudo e uso, nao apenas em devices populares
- [ ] O approach (mobile-first ou desktop-first) esta definido e documentado
- [ ] O layout se adapta de forma fluida entre breakpoints, nao apenas em pontos fixos
- [ ] A hierarquia visual e de conteudo e mantida em todos os breakpoints
- [ ] Os touch targets atendem o minimo de 44x44px em breakpoints mobile e tablet
- [ ] A navegacao se adapta adequadamente (ex: hamburger menu em mobile, full nav em desktop)
- [ ] As imagens e media sao responsivas com srcset ou art direction quando necessario
- [ ] Os formularios sao usaveis em todos os breakpoints (teclado virtual considerado)
- [ ] O grid system se adapta com colunas adequadas por breakpoint
- [ ] Os componentes que mudam de layout entre breakpoints estao documentados
- [ ] O conteudo nao e ocultado em breakpoints menores sem alternativa de acesso
- [ ] A tipografia se adapta com font-sizes apropriados por breakpoint
- [ ] As tabelas e conteudo tabulado possuem estrategia de adaptacao (scroll, stack, collapse)
- [ ] O design foi testado em orientacao portrait e landscape
- [ ] Os modais e overlays sao usaveis em telas pequenas

## Severity Guide

### Critico
- Layout quebrado em algum breakpoint impedindo uso da funcionalidade.
- Touch targets inacessiveis em mobile.
- Conteudo critico ocultado sem alternativa de acesso.

### Major
- Navegacao nao adaptada para mobile.
- Formularios inutilizaveis em telas pequenas.
- Imagens nao responsivas causando scroll horizontal.

### Minor
- Pequenas inconsistencias de espacamento entre breakpoints.
- Orientacao landscape nao otimizada mas funcional.
- Tipografia nao totalmente adaptada entre breakpoints.

## Cross-References
- [Wireframe Quality](wireframe-quality.md)
- [UI Visual Quality](ui-visual-quality.md)
- [Handoff Quality](handoff-quality.md)
- [Cross-Platform Quality](cross-platform-quality.md)
- [Accessibility Quality](accessibility-quality.md)
