# Product Design Debt Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Design Quality                 |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Product Design Lead            |

## Objective

Identificar, catalogar e priorizar dividas de design (design debt) acumuladas no
produto ao longo do tempo. Design debt sao decisoes de design sub-otimas feitas por
restricoes de tempo, escopo ou conhecimento que impactam negativamente a experiencia
do usuario e a consistencia do produto.

## When to Apply

- Em auditorias trimestrais de qualidade do produto.
- Ao planejar sprints de melhoria ou polish.
- Quando metricas de UX indicam degradacao da experiencia.
- Em planejamentos de quarter para alocar capacidade de reducao de debt.

## Criteria

- [ ] Existe inventario centralizado de design debt catalogado e priorizado.
- [ ] Cada item de debt possui descricao, impacto estimado e esforco de correcao.
- [ ] Design debt e categorizado por tipo: visual, interacao, conteudo, fluxo, acessibilidade.
- [ ] O impacto e quantificado quando possivel (metricas, feedback, tickets de suporte).
- [ ] Existe priorizacao clara usando framework (ex.: impact vs. effort matrix).
- [ ] Capacidade dedicada para reducao de design debt esta alocada (ex.: 20% do sprint).
- [ ] Novo design debt introduzido conscientemente e registrado com justificativa.
- [ ] Existe processo para prevenir acumulo descontrolado de design debt.
- [ ] Stakeholders entendem o conceito de design debt e seu impacto no negocio.
- [ ] Metricas de reducao de debt sao rastreadas ao longo do tempo.
- [ ] Design debt de acessibilidade e priorizado com severidade elevada.
- [ ] Revisoes periodicas atualizam a lista removendo items resolvidos.
- [ ] O inventario e visivel para toda a equipe de produto e engenharia.
- [ ] Design debt critico possui timeline de resolucao definido.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Design debt de acessibilidade nao rastreado ou nenhum inventario existe.  |
| Major    | Nenhuma capacidade alocada para reducao ou debt crescendo descontrolado.  |
| Minor    | Priorizacao nao estruturada ou metricas de reducao nao rastreadas.       |
| Info     | Oportunidade de melhorar visibilidade ou implementar prevencao proativa.  |

## Cross-References

- `malouf/malouf-ux-strategy-audit.md` — Estrategia de UX.
- `product/product-roadmap-alignment.md` — Alinhamento de roadmap.
- `frost/frost-interface-inventory-audit.md` — Inventario de interfaces.
- `ux/ux-heuristic-evaluation.md` — Avaliacao heuristica.
