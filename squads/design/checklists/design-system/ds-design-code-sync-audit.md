# DS Design-Code Sync Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Design-Dev Alignment           |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Design System Lead             |

## Objective

Avaliar o nivel de sincronizacao entre os artefatos de design (Figma, Sketch, etc.)
e a implementacao em codigo dos componentes do design system. Paridade entre design
e codigo e essencial para credibilidade do sistema e para que designers possam projetar
com confianca de que o resultado final sera fiel.

## When to Apply

- Em auditorias trimestrais de paridade design-code.
- Apos releases major do design system.
- Quando desenvolvedores reportam discrepancias entre design e implementacao.
- Ao automatizar pipelines de design-to-code.

## Criteria

- [ ] Tokens de cor no design tool correspondem exatamente aos tokens no codigo.
- [ ] Tokens de tipografia (family, size, weight, line-height) estao sincronizados.
- [ ] Espacamentos e dimensoes dos componentes sao identicos entre design e codigo.
- [ ] Variantes definidas no design tool possuem implementacao correspondente em codigo.
- [ ] Estados de componentes (hover, focus, disabled, error) existem em ambos os lados.
- [ ] Nomenclatura de componentes e consistente entre design tool e codebase.
- [ ] Existe processo automatizado de validacao de paridade (visual regression, overlay diff).
- [ ] Novas versoes no design tool sao acompanhadas de atualizacao no codigo e vice-versa.
- [ ] Existe responsavel definido por garantir sync apos cada mudanca significativa.
- [ ] Discrepancias sao rastreadas em backlog dedicado com prioridade definida.
- [ ] Propriedades de componentes no design tool (Figma properties) mapeiam para props no codigo.
- [ ] Breakpoints e comportamento responsivo sao consistentes entre design e codigo.
- [ ] Existe checklist de validacao de paridade executado em cada release.
- [ ] O time mede e reporta o indice de paridade regularmente.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Tokens de cor ou tipografia divergentes entre design e codigo.            |
| Major    | Variantes ou estados existem em um lado mas nao no outro.                |
| Minor    | Nomenclatura inconsistente ou breakpoints com pequenos desvios.           |
| Info     | Oportunidade de automatizar validacao ou melhorar processo de sync.       |

## Cross-References

- `design-system/ds-token-architecture.md` — Arquitetura de tokens.
- `frost/frost-frontend-style-guide-audit.md` — Style guide de frontend.
- `handoff/handoff-token-sync.md` — Sincronizacao de tokens no handoff.
- `mall/mall-hot-potato-process-audit.md` — Processo hot potato.
