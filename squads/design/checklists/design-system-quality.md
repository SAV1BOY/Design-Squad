# Design System Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Design Systems
- **Version:** 1.0.0
- **Owner Agent:** Design System Lead Agent

## Objective
Assegurar que o design system seja consistente, escalavel, bem documentado e efetivamente adotado pelas equipes de design e desenvolvimento.
Um design system de qualidade e uma fonte unica de verdade que acelera a entrega com consistencia.

## When to Apply
- Ao criar ou reestruturar um design system.
- Em auditorias periodicas de saude e adocao do design system.
- Ao avaliar a inclusao de novos componentes ou patterns no sistema.

## Criteria
- [ ] Os principios de design (design principles) que guiam o sistema estao documentados
- [ ] A estrutura de tokens (primitives, semantics, component) esta definida e implementada
- [ ] Todos os componentes possuem documentacao completa com specs e exemplos
- [ ] Os componentes sao consistentes entre as plataformas suportadas (web, iOS, Android)
- [ ] O sistema de versionamento (semantic versioning) esta implementado
- [ ] Existe um processo claro para contribuicao e proposta de novos componentes
- [ ] O changelog e mantido atualizado a cada release
- [ ] Os componentes foram testados em contextos reais de uso antes da publicacao
- [ ] A cobertura de accessibility esta verificada para todos os componentes (WCAG AA)
- [ ] A documentacao inclui guidelines de uso com exemplos de do e don't
- [ ] O design system possui metricas de adocao e satisfacao dos usuarios internos
- [ ] Os assets de design (Figma libraries) estao sincronizados com o codigo
- [ ] Existe um deprecation process definido para componentes descontinuados
- [ ] O sistema de nomenclatura (naming convention) e consistente e intuitivo
- [ ] A governanca do design system (ownership, decisoes, roadmap) esta definida
- [ ] O onboarding para novos membros do time esta documentado

## Severity Guide

### Critico
- Componentes inconsistentes entre design e codigo implementado.
- Ausencia de sistema de versionamento causando breaking changes silenciosas.
- Componentes sem cobertura minima de accessibility.

### Major
- Documentacao de componentes incompleta ou desatualizada.
- Processo de contribuicao inexistente gerando componentes nao governados.
- Assets de design desincronizados do codigo.

### Minor
- Metricas de adocao nao coletadas.
- Onboarding de novos membros nao documentado formalmente.
- Changelog atrasado mas versionamento funcional.

## Cross-References
- [Component Spec Quality](component-spec-quality.md)
- [Token Quality](token-quality.md)
- [Color System Quality](color-system-quality.md)
- [Typography Quality](typography-quality.md)
- [Accessibility Quality](accessibility-quality.md)
