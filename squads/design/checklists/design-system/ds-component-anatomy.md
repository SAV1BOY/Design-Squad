# DS Component Anatomy

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Component Design               |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Design System Lead             |

## Objective

Verificar se os componentes do design system seguem uma anatomia padronizada, com
estrutura, props, variantes, estados e API bem definidos. Componentes com anatomia
consistente sao mais faceis de aprender, usar, compor e manter.

## When to Apply

- Ao criar novos componentes para o design system.
- Em revisoes de API de componentes existentes.
- Quando componentes sao refatorados ou recebem novas variantes.
- Em auditorias de qualidade do catalogo de componentes.

## Criteria

- [ ] Cada componente possui nome unico seguindo convencao de nomenclatura do sistema.
- [ ] A API de props e minima, expressiva e consistente com outros componentes.
- [ ] Variantes sao definidas por prop enum, nao por componentes separados.
- [ ] Tamanhos seguem escala padronizada (sm, md, lg) alinhada com o sistema.
- [ ] Slots ou children permitem composicao flexivel sem quebrar o layout.
- [ ] Valores default de props sao definidos para o caso de uso mais comum.
- [ ] Cada componente suporta className/style override para customizacao controlada.
- [ ] Componentes implementam forwardRef e suportam data-attributes para testes.
- [ ] Props de acessibilidade (aria-label, role) sao suportadas nativamente.
- [ ] Eventos (onClick, onChange, onFocus) seguem convencao consistente de naming.
- [ ] Componentes sao renderizaveis server-side (SSR) sem erros.
- [ ] Tipos (TypeScript) ou PropTypes sao definidos e exportados para consumidores.
- [ ] Documentacao inclui anatomia visual com labels para cada parte do componente.
- [ ] Cada componente possui testes unitarios, de acessibilidade e visual regression.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | API inconsistente com outros componentes ou sem tipos definidos.          |
| Major    | Componente nao suporta composicao ou nao implementa acessibilidade.      |
| Minor    | Defaults nao otimizados ou documentacao de anatomia incompleta.           |
| Info     | Oportunidade de adicionar data-attributes ou melhorar SSR support.       |

## Cross-References

- `frost/frost-atomic-design-audit.md` — Auditoria de atomic design.
- `design-system/ds-token-architecture.md` — Arquitetura de tokens.
- `ui/ui-states-and-feedback.md` — Estados e feedback visual.
- `accessibility/a11y-aria-and-semantics.md` — ARIA e semantica.
