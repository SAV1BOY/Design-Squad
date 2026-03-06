# Performance UX Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Performance & UX
- **Version:** 1.0.0
- **Owner Agent:** Performance UX Agent

## Objective
Garantir que as decisoes de design considerem o impacto na performance percebida e real do produto.
Uma experiencia rapida e fluida e tao importante quanto uma experiencia bonita — velocidade e uma feature de UX.

## When to Apply
- Ao projetar interfaces com conteudo dinamico ou listas extensas.
- Ao definir estrategias de carregamento e feedback visual.
- Ao avaliar a experiencia em conexoes lentas ou devices de baixa performance.

## Criteria
- [ ] Os loading patterns estao definidos (skeleton screens, spinners, progress bars) por contexto
- [ ] O skeleton screen reflete a estrutura real do conteudo que sera carregado
- [ ] O feedback visual para acoes do usuario e imediato (menos de 100ms)
- [ ] A estrategia de lazy loading esta definida para imagens e conteudo below-the-fold
- [ ] Os assets de imagem possuem tamanhos otimizados e formatos modernos (WebP, AVIF)
- [ ] As fontes possuem estrategia de carregamento (font-display, preload) definida
- [ ] O conteudo acima da dobra (above-the-fold) carrega prioritariamente
- [ ] A paginacao ou infinite scroll esta planejada para listas extensas
- [ ] Os estados de erro de rede possuem tratamento visual e opcao de retry
- [ ] A experiencia offline ou em conexao instavel esta considerada quando aplicavel
- [ ] As animacoes utilizam propriedades GPU-friendly (transform, opacity)
- [ ] O perceived performance e otimizado com progressive disclosure e optimistic UI
- [ ] Os Core Web Vitals (LCP, FID, CLS) foram considerados nas decisoes de design
- [ ] A experiencia em devices de baixa performance foi validada
- [ ] O peso total da pagina (page weight) e monitorado e tem budget definido
- [ ] Existe estrategia de caching visual para conteudo frequentemente acessado

## Severity Guide

### Critico
- Ausencia de qualquer feedback visual durante operacoes longas.
- Layout shift significativo (CLS alto) apos carregamento de conteudo.
- Pagina completamente inutilizavel em conexoes 3G.

### Major
- Skeleton screens nao refletem a estrutura real do conteudo.
- Imagens nao otimizadas impactando significativamente o tempo de carregamento.
- Ausencia de tratamento para erros de rede.

### Minor
- Estrategia de font-display nao definida mas impacto visual minimo.
- Caching visual nao implementado para conteudo de baixa frequencia.
- Page weight budget nao formalizado.

## Cross-References
- [Motion Quality](motion-quality.md)
- [Responsive Breakpoints Quality](responsive-breakpoints-quality.md)
- [Cross-Platform Quality](cross-platform-quality.md)
- [UX Audit Quality](ux-audit-quality.md)
- [Design Debt Quality](design-debt-quality.md)
