# Handoff QA with Dev

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Quality Assurance              |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Handoff Lead                   |

## Objective

Garantir que o processo de QA visual entre design e desenvolvimento e realizado de
forma sistematica, verificando se a implementacao corresponde fielmente ao design
aprovado. QA visual eficaz detecta desvios antes do lancamento e mantem a barra de
qualidade visual do produto.

## When to Apply

- Apos cada implementacao de feature ou componente novo.
- Em sprints de QA visual antes de releases.
- Quando o time adota processo de review visual formal.
- Ao estabelecer workflow de QA entre design e engenharia.

## Criteria

- [ ] O designer revisa a implementacao em ambiente de staging ou preview.
- [ ] A revisao cobre todos os breakpoints definidos (mobile, tablet, desktop).
- [ ] Cada estado de componente (default, hover, active, disabled, error) e verificado.
- [ ] Espacamentos sao comparados com o design usando ferramenta de overlay ou medicao.
- [ ] Tipografia (family, size, weight, color, line-height) e verificada pixel a pixel.
- [ ] Cores implementadas correspondem aos tokens referenciados no design.
- [ ] Animacoes e transicoes correspondem as especificacoes (duracao, easing, trigger).
- [ ] Edge cases visuais sao testados (texto longo, dados vazios, listas extensas).
- [ ] Acessibilidade basica e verificada (foco, contraste, alt text).
- [ ] Bugs visuais encontrados sao documentados com screenshot e descricao precisa.
- [ ] Existe escala de severidade para bugs visuais (blocker, major, minor, cosmetic).
- [ ] Follow-up de bugs visuais e rastreado ate resolucao e re-verificacao.
- [ ] O processo de QA visual tem SLA definido para nao bloquear releases.
- [ ] Ferramentas de visual regression testing complementam a revisao manual.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Implementacao funcional mas visualmente irreconhecivel em relacao ao design.|
| Major    | Desvios significativos de cor, tipografia ou layout em fluxos criticos.   |
| Minor    | Desvios menores de espacamento ou animacoes nao implementadas.            |
| Info     | Oportunidade de implementar visual regression testing automatizado.      |

## Cross-References

- `mall/mall-hot-potato-process-audit.md` — Processo hot potato.
- `mall/mall-cross-functional-collab.md` — Colaboracao cross-functional.
- `handoff/handoff-specs-and-redlines.md` — Especificacoes de handoff.
- `design-system/ds-design-code-sync-audit.md` — Sincronizacao design-code.
