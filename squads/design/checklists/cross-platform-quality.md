# Cross-Platform Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Platform Design
- **Version:** 1.0.0
- **Owner Agent:** Cross-Platform Agent

## Objective
Garantir que a experiencia do usuario seja coerente e otimizada em cada plataforma (web, iOS, Android), respeitando as convencoes nativas sem perder a identidade do produto.
Design cross-platform de qualidade equilibra consistencia de marca com familiaridade da plataforma.

## When to Apply
- Ao projetar funcionalidades que existem em multiplas plataformas.
- Ao expandir o produto para uma nova plataforma.
- Ao auditar a consistencia da experiencia entre plataformas.

## Criteria
- [ ] As platform guidelines (Material Design, HIG) foram consultadas e consideradas
- [ ] Os navigation patterns respeitam as convencoes nativas de cada plataforma
- [ ] Os gestos de interacao (swipe, pinch, long press) seguem os padroes da plataforma
- [ ] Os componentes nativos sao utilizados quando oferecem melhor experiencia (date pickers, share sheets)
- [ ] A tipografia utiliza as system fonts como fallback ou complemento quando adequado
- [ ] O layout respeita as safe areas e notch/punch-hole de diferentes devices
- [ ] Os icones seguem o estilo da plataforma ou possuem estilo proprio consistente
- [ ] A experiencia de notificacao respeita os patterns nativos (push, badges, alerts)
- [ ] A funcionalidade core e a mesma em todas as plataformas, sem lacunas criticas
- [ ] As diferencas intencionais entre plataformas estao documentadas com rationale
- [ ] A performance percebida e comparavel entre plataformas
- [ ] Os deep links e handoff entre plataformas funcionam corretamente
- [ ] A experiencia de onboarding esta adaptada por plataforma quando necessario
- [ ] Os padroes de input (teclado, voz, touch) estao otimizados por plataforma
- [ ] O design system possui variantes ou adaptacoes por plataforma documentadas

## Severity Guide

### Critico
- Navegacao que viola convencoes fundamentais da plataforma confundindo o usuario.
- Funcionalidade core ausente em uma plataforma sem comunicacao ao usuario.
- Layout ignorando safe areas causando conteudo cortado.

### Major
- Gestos de interacao inconsistentes com a plataforma.
- Componentes custom onde nativos seriam significativamente melhores.
- Performance perceptivelmente pior em uma plataforma.

### Minor
- Icones com estilo levemente diferente entre plataformas.
- Adaptacao de onboarding nao otimizada mas funcional.
- Deep links entre plataformas nao implementados.

## Cross-References
- [Responsive Breakpoints Quality](responsive-breakpoints-quality.md)
- [Design System Quality](design-system-quality.md)
- [Performance UX Quality](performance-ux-quality.md)
- [Motion Quality](motion-quality.md)
- [Localization Quality](localization-quality.md)
