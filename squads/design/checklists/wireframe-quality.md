# Wireframe Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Interaction Design
- **Version:** 1.0.0
- **Owner Agent:** Wireframe Agent

## Objective
Garantir que wireframes comuniquem de forma clara a estrutura, hierarquia e comportamento das interfaces sem ambiguidades.
Wireframes de qualidade aceleram a convergencia do time sobre decisoes de layout e interacao.

## When to Apply
- Ao criar wireframes de baixa ou media fidelidade para novas features.
- Ao revisar wireframes antes de avancar para design visual.
- Ao utilizar wireframes como base de discussao com stakeholders.

## Criteria
- [ ] A hierarquia visual de conteudo esta clara e guia o olhar do usuario corretamente
- [ ] Todos os elementos interativos estao identificados e diferenciados de conteudo estatico
- [ ] As anotacoes de comportamento (interactions, transitions) estao presentes e claras
- [ ] O conteudo utiliza texto real ou representativo, nao apenas lorem ipsum
- [ ] Os estados de cada componente estao representados (default, hover, active, disabled, error)
- [ ] A responsividade esta indicada ou existe wireframe por breakpoint principal
- [ ] O grid system utilizado esta definido e consistente
- [ ] Os espacamentos seguem um sistema coerente e documentado
- [ ] Empty states estao representados para listas, busca e conteudo dinamico
- [ ] Os CTAs primarios e secundarios estao claramente hierarquizados
- [ ] A acessibilidade basica esta considerada (tab order, areas de toque)
- [ ] O wireframe cobre todos os steps do user flow correspondente
- [ ] Modais, tooltips e overlays estao documentados com trigger e conteudo
- [ ] O wireframe indica de onde vem os dados dinamicos (data sources)
- [ ] Existe um inventario de componentes utilizados com referencia ao design system

## Severity Guide

### Critico
- Hierarquia visual confusa que nao guia o usuario adequadamente.
- Elementos interativos indistinguiveis de conteudo estatico.
- Steps do user flow nao cobertos pelo wireframe.

### Major
- Ausencia de representacao de error states e empty states.
- Uso exclusivo de lorem ipsum sem indicacao de conteudo real necessario.
- Responsividade nao considerada para produto multi-device.

### Minor
- Grid system nao explicitamente documentado mas consistente visualmente.
- Falta de indicacao de data sources para conteudo dinamico.
- Anotacoes de comportamento poderiam ser mais detalhadas.

## Cross-References
- [User Flow Quality](user-flow-quality.md)
- [UI Visual Quality](ui-visual-quality.md)
- [Component Spec Quality](component-spec-quality.md)
- [Responsive Breakpoints Quality](responsive-breakpoints-quality.md)
- [Prototyping Quality](prototyping-quality.md)
