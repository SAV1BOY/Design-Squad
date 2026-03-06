# Frost Component Inventory Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Frost                          |
| Domain      | Design System                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Frost Lead                     |

## Objective

Realizar um inventario completo de todos os componentes existentes no design system,
identificando duplicacoes, inconsistencias, componentes orfaos e lacunas de cobertura.
O objetivo e manter o catalogo enxuto, atualizado e alinhado com as necessidades do produto.

## When to Apply

- Trimestralmente como parte da auditoria do design system.
- Quando o numero de componentes cresce mais de 15% em um ciclo.
- Antes de migracoes de versao major do framework.
- Ao integrar novos squads consumidores do design system.

## Criteria

- [ ] Todos os componentes possuem entrada no catalogo central (Storybook, Figma library ou equivalente).
- [ ] Nenhum componente existe apenas em codigo sem representacao no design tool.
- [ ] Nenhum componente existe apenas no design tool sem implementacao em codigo.
- [ ] Componentes duplicados foram identificados e existe plano de consolidacao.
- [ ] Cada componente possui owner definido e contato atualizado.
- [ ] Componentes orfaos (sem uso em nenhum produto) estao sinalizados para deprecacao.
- [ ] Variantes de cada componente estao documentadas e acessiveis.
- [ ] Componentes possuem status claro: stable, beta, deprecated ou experimental.
- [ ] A cobertura de testes unitarios e de pelo menos 80% para componentes stable.
- [ ] Componentes deprecated possuem data de remocao planejada e migration guide.
- [ ] Existe mapeamento de quais produtos e telas utilizam cada componente.
- [ ] O inventario inclui metricas de uso (frequencia de importacao, numero de instancias).
- [ ] Componentes com mais de 10 props possuem revisao de API documentada.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Componente em producao sem registro no inventario.                        |
| Major    | Duplicacao de componentes sem plano de consolidacao.                      |
| Minor    | Componente sem owner definido ou status desatualizado.                    |
| Info     | Sugestao para melhorar metricas de uso ou rastreabilidade.                |

## Cross-References

- `frost/frost-atomic-design-audit.md` — Auditoria de hierarquia atomic design.
- `frost/frost-interface-inventory-audit.md` — Inventario de interfaces.
- `design-system/ds-audit-and-dedup.md` — Deduplicacao de componentes.
- `design-system/ds-adoption-playbook.md` — Playbook de adocao.
