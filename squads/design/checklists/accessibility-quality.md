# Accessibility Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Accessibility
- **Version:** 1.0.0
- **Owner Agent:** Accessibility Agent

## Objective
Garantir que o produto seja utilizavel por pessoas com diferentes habilidades e necessidades, atendendo no minimo WCAG 2.1 nivel AA.
Acessibilidade nao e um extra opcional — e um requisito de qualidade e, em muitos contextos, uma obrigacao legal.

## When to Apply
- Em todas as fases do design, desde wireframes ate alta fidelidade.
- Ao revisar entregas antes do handoff para desenvolvimento.
- Em auditorias periodicas de acessibilidade do produto.

## Criteria
- [ ] Todo conteudo nao textual possui alternative text descritivo e contextual
- [ ] A hierarquia de headings (H1-H6) e semantica e sequencial
- [ ] O contraste de texto atende WCAG AA: 4.5:1 (normal) e 3:1 (large text)
- [ ] O contraste de elementos graficos e controles de UI atende 3:1
- [ ] Todos os elementos interativos sao acessiveis via keyboard (Tab, Enter, Space, Escape)
- [ ] O focus indicator e visivel e tem contraste adequado em todos os elementos interativos
- [ ] Os formularios possuem labels associados, instrucoes claras e mensagens de erro acessiveis
- [ ] As ARIA roles, states e properties estao especificadas para componentes custom
- [ ] O conteudo nao depende exclusivamente de cor para comunicar informacao
- [ ] As animacoes respeitam prefers-reduced-motion e nao causam seizures (max 3 flashes/segundo)
- [ ] O touch target minimo e de 44x44px para elementos interativos em mobile
- [ ] A ordem de leitura (reading order) faz sentido quando linearizada
- [ ] Os time-based media possuem alternativas (captions, transcripts)
- [ ] O zoom ate 200% nao causa perda de conteudo ou funcionalidade
- [ ] Os error messages sao claros, especificos e sugerem correcao
- [ ] O skip navigation esta disponivel para conteudo repetitivo
- [ ] O produto foi testado com screen readers principais (VoiceOver, NVDA, TalkBack)
- [ ] Existe documentacao de accessibility requirements para cada componente

## Severity Guide

### Critico
- Contraste de texto abaixo dos niveis WCAG AA.
- Elementos interativos inacessiveis via keyboard.
- Ausencia de alternative text em conteudo nao textual critico.
- Formularios sem labels ou mensagens de erro.

### Major
- Focus indicator nao visivel ou com contraste insuficiente.
- ARIA roles nao especificadas para componentes custom.
- Animacoes que nao respeitam prefers-reduced-motion.

### Minor
- Skip navigation ausente em paginas com pouca repeticao.
- Touch targets ligeiramente abaixo de 44px em elementos nao criticos.
- Documentacao de accessibility requirements incompleta.

## Cross-References
- [UI Visual Quality](ui-visual-quality.md)
- [Color System Quality](color-system-quality.md)
- [Typography Quality](typography-quality.md)
- [Component Spec Quality](component-spec-quality.md)
- [Content Design Quality](content-design-quality.md)
