# Frost Atomic Design Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Frost                          |
| Domain      | Design System                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Frost Lead                     |

## Objective

Garantir que a arquitetura de componentes segue rigorosamente os principios do Atomic Design,
mantendo a separacao clara entre atoms, molecules, organisms, templates e pages. Este checklist
avalia a integridade estrutural, a reutilizacao e a composicao correta de cada nivel hierarquico.

## When to Apply

- Durante auditorias trimestrais do design system.
- Ao adicionar novos componentes ao repositorio.
- Em revisoes de pull requests que alteram a hierarquia de componentes.
- Antes de releases major do design system.

## Criteria

- [ ] Cada atom e autossuficiente e nao depende de outros atoms para renderizar corretamente.
- [ ] Molecules sao compostas exclusivamente por atoms, sem logica de negocio embutida.
- [ ] Organisms combinam molecules e atoms de forma coerente com o dominio do produto.
- [ ] Templates definem layout sem conteudo real, usando placeholders apropriados.
- [ ] Pages sao instancias de templates com dados reais ou realistas.
- [ ] Nenhum componente pula niveis na hierarquia (ex.: page usando atom diretamente sem molecule).
- [ ] Tokens de design (spacing, color, typography) sao aplicados de forma consistente em todos os niveis.
- [ ] Cada componente possui documentacao de props e variantes no Storybook ou ferramenta equivalente.
- [ ] Testes visuais (snapshot ou visual regression) cobrem pelo menos 90% dos atoms e molecules.
- [ ] Nomenclatura segue convencao padronizada (kebab-case, prefixo por nivel).
- [ ] Componentes deprecados estao marcados e possuem alternativa documentada.
- [ ] Nao existem componentes duplicados em niveis diferentes da hierarquia.
- [ ] A arvore de dependencias nao possui ciclos entre niveis.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Componente pula niveis hierarquicos ou possui dependencias ciclicas.      |
| Major    | Molecule contendo logica de negocio ou atom com dependencia externa.      |
| Minor    | Nomenclatura fora do padrao ou documentacao incompleta.                   |
| Info     | Sugestao de melhoria na composicao ou organizacao de pastas.              |

## Cross-References

- `frost/frost-component-inventory-audit.md` — Inventario completo de componentes.
- `frost/frost-pattern-library-quality.md` — Qualidade da pattern library.
- `design-system/ds-component-anatomy.md` — Anatomia padrao de componentes.
- `design-system/ds-token-architecture.md` — Arquitetura de tokens.
