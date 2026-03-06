# Information Architecture & Navigation Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Information Architecture
- **Version:** 1.0.0
- **Owner Agent:** IA Agent

## Objective
Garantir que a arquitetura de informacao e a navegacao do produto sejam intuitivas, escalaveis e baseadas em modelos mentais reais dos usuarios.
Uma IA bem estruturada e a fundacao para uma experiencia de uso eficiente.

## When to Apply
- Ao definir ou reestruturar a arquitetura de informacao de um produto.
- Ao adicionar novas secoes ou funcionalidades que impactam a navegacao.
- Ao avaliar resultados de tree testing ou card sorting.

## Criteria
- [ ] A estrutura de informacao foi validada com usuarios atraves de card sorting ou tree testing
- [ ] A hierarquia de conteudo reflete os modelos mentais dos usuarios, nao a estrutura organizacional
- [ ] Os labels de navegacao sao claros, concisos e utilizam vocabulario do usuario
- [ ] A profundidade da hierarquia nao excede 3-4 niveis para tarefas frequentes
- [ ] Os caminhos de navegacao para tarefas principais (primary tasks) sao curtos e diretos
- [ ] Existe navegacao secundaria (breadcrumbs, search) para apoiar diferentes estrategias de busca
- [ ] A navegacao global e consistente em todas as paginas e secoes
- [ ] O sitemap ou mapa de navegacao esta documentado e atualizado
- [ ] A taxonomia utilizada e consistente e escalavel para crescimento futuro
- [ ] Os search patterns (search, filter, sort) estao definidos para conteudo extenso
- [ ] A navegacao mobile foi planejada com prioridades diferentes do desktop quando necessario
- [ ] Os estados de wayfinding (onde estou, onde posso ir) estao claros em cada ponto
- [ ] Cross-links entre conteudos relacionados estao planejados
- [ ] A acessibilidade da navegacao (keyboard navigation, screen readers) esta considerada
- [ ] Existe documentacao de decisoes de IA com rationale

## Severity Guide

### Critico
- Hierarquia de informacao nao validada com usuarios.
- Labels de navegacao ambiguos ou incompreensiveis para o publico-alvo.
- Tarefas principais requerem mais de 5 cliques para conclusao.

### Major
- Navegacao inconsistente entre secoes do produto.
- Ausencia de mecanismos de busca e filtragem em conteudo extenso.
- Estrutura nao escalavel para crescimento planejado.

### Minor
- Breadcrumbs ausentes em hierarquias profundas.
- Cross-links nao planejados entre conteudos relacionados.
- Documentacao de decisoes de IA incompleta.

## Cross-References
- [User Flow Quality](user-flow-quality.md)
- [Wireframe Quality](wireframe-quality.md)
- [Content Design Quality](content-design-quality.md)
- [Accessibility Quality](accessibility-quality.md)
- [Responsive Breakpoints Quality](responsive-breakpoints-quality.md)
