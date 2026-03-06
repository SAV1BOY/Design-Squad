# DS Audit and Deduplication

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | System Hygiene                 |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Design System Lead             |

## Objective

Conduzir auditoria sistematica do design system para identificar e resolver duplicacoes
de componentes, tokens e patterns. Deduplicacao reduz confusao para consumidores,
diminui custo de manutencao e fortalece a consistencia do ecossistema visual.

## When to Apply

- Em auditorias trimestrais de saude do design system.
- Quando o numero de componentes ultrapassa threshold definido.
- Apos integracao de componentes de squads ou produtos diferentes.
- Quando consumidores reportam confusao entre componentes similares.

## Criteria

- [ ] Inventario completo de componentes foi gerado com contagem de uso por produto.
- [ ] Componentes com funcionalidade sobreposta foram identificados e listados.
- [ ] Cada par de duplicatas tem analise de diferencas (diff visual e funcional).
- [ ] Plano de consolidacao define qual componente sobrevive e qual sera deprecado.
- [ ] Migration path esta documentado para cada componente a ser removido.
- [ ] Tokens duplicados ou com valores identicos foram identificados e unificados.
- [ ] Patterns que resolvem o mesmo problema de formas diferentes estao mapeados.
- [ ] O custo de manutencao das duplicatas e quantificado para justificar a consolidacao.
- [ ] Stakeholders dos produtos afetados foram consultados antes da consolidacao.
- [ ] Timeline de deprecacao e realista e comunicada com antecedencia.
- [ ] Automacao (lint rules, import warnings) sinaliza uso de componentes deprecated.
- [ ] Testes de regressao validam que a consolidacao nao introduz bugs.
- [ ] Metricas pre e pos-deduplicacao sao comparadas para medir sucesso.
- [ ] O processo de auditoria e dedup e documentado para replicacao futura.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Mais de 3 componentes duplicados em uso ativo sem plano de consolidacao.  |
| Major    | Tokens com valores identicos sob nomes diferentes causando confusao.      |
| Minor    | Patterns duplicados de baixa frequencia ou plano de migracao incompleto.  |
| Info     | Oportunidade de automatizar deteccao de duplicatas ou melhorar lint.      |

## Cross-References

- `frost/frost-component-inventory-audit.md` — Inventario de componentes.
- `frost/frost-interface-inventory-audit.md` — Inventario de interfaces.
- `design-system/ds-token-architecture.md` — Arquitetura de tokens.
- `design-system/ds-versioning-and-changelog.md` — Versionamento.
