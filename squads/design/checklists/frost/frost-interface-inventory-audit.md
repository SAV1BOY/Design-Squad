# Frost Interface Inventory Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Frost                          |
| Domain      | Interface Audit                |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Frost Lead                     |

## Objective

Conduzir um inventario completo das interfaces existentes nos produtos, capturando
screenshots e catalogando todos os elementos visuais unicos. Este processo revela
inconsistencias, redundancias e oportunidades de padronizacao que alimentam a
evolucao do design system.

## When to Apply

- Antes de iniciar um redesign ou refactoring visual significativo.
- Ao integrar um novo produto ao ecossistema do design system.
- Em auditorias anuais de consistencia visual.
- Quando metricas indicam alta fragmentacao de componentes.

## Criteria

- [ ] Screenshots de todas as telas principais foram capturadas e catalogadas.
- [ ] Elementos unicos de tipografia foram identificados e listados com contagem de uso.
- [ ] Variacoes de cores foram mapeadas e comparadas com os tokens oficiais.
- [ ] Espacamentos e tamanhos unicos foram documentados com desvios dos tokens.
- [ ] Botoes e CTAs foram inventariados com todas as variacoes encontradas.
- [ ] Formularios e inputs foram catalogados com suas inconsistencias.
- [ ] Icones e ilustracoes foram listados com fonte e formato de cada um.
- [ ] Componentes de navegacao foram comparados entre diferentes produtos e telas.
- [ ] Cards e containers foram inventariados com suas variacoes de estilo.
- [ ] Modais, tooltips e overlays foram catalogados com comportamentos distintos.
- [ ] Elementos de feedback (alerts, toasts, banners) foram mapeados.
- [ ] O inventario foi priorizado por impacto e frequencia de uso.
- [ ] Um plano de consolidacao foi criado com timeline e responsaveis.
- [ ] Stakeholders revisaram e aprovaram o inventario final.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Mais de 5 variacoes de um mesmo tipo de componente sem justificativa.     |
| Major    | Uso de cores ou tipografia fora dos tokens sem documentacao.              |
| Minor    | Inconsistencias menores em espacamento ou border-radius.                  |
| Info     | Oportunidade de unificar componentes com baixo impacto visual.            |

## Cross-References

- `frost/frost-component-inventory-audit.md` — Inventario de componentes do sistema.
- `frost/frost-atomic-design-audit.md` — Auditoria de atomic design.
- `ui/ui-visual-hierarchy.md` — Hierarquia visual.
- `design-system/ds-audit-and-dedup.md` — Auditoria e deduplicacao.
