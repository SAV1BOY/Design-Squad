# Mall Hot Potato Process Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Mall                           |
| Domain      | Design-Dev Workflow            |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Mall Lead                      |

## Objective

Avaliar a implementacao do processo Hot Potato entre design e engenharia, onde o
trabalho alterna rapidamente entre as disciplinas em ciclos curtos de iteracao.
Este processo substitui o handoff linear tradicional por colaboracao continua,
resultando em maior fidelidade e menos retrabalho.

## When to Apply

- Ao adotar o processo Hot Potato pela primeira vez no squad.
- Em retrospectivas de projetos que utilizam este modelo.
- Quando o ciclo de iteracao entre design e codigo esta lento.
- Em avaliacoes trimestrais da eficacia do workflow design-dev.

## Criteria

- [ ] O conceito de Hot Potato foi apresentado e aceito por design e engenharia.
- [ ] Ciclos de iteracao entre design e codigo acontecem em intervalos curtos (1-3 dias).
- [ ] Designer e desenvolvedor trabalham no mesmo componente simultaneamente ou em sequencia rapida.
- [ ] Existe ambiente de preview (staging, Storybook) para validacao continua.
- [ ] Feedback de design sobre implementacao e dado diretamente no componente renderizado.
- [ ] Ajustes visuais menores sao feitos diretamente no codigo pelo desenvolvedor.
- [ ] O designer revisa o componente implementado antes de considerar a tarefa concluida.
- [ ] Existe definicao clara de quando o componente esta "done" para ambas as disciplinas.
- [ ] O processo reduz o numero de ciclos de revisao comparado ao handoff tradicional.
- [ ] Ferramentas de comparacao visual (overlay, pixel diff) sao utilizadas na validacao.
- [ ] O squad mede e compara cycle time antes e depois de adotar Hot Potato.
- [ ] Existe documentacao do processo adaptada ao contexto do squad.
- [ ] Sessoes de pair programming/design sao parte regular do workflow.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Processo Hot Potato declarado mas nao praticado (handoff linear disfarc.). |
| Major    | Ciclos de iteracao maiores que uma semana ou sem validacao visual.         |
| Minor    | Ferramentas de comparacao visual nao utilizadas ou metricas ausentes.     |
| Info     | Oportunidade de refinar o processo com novas ferramentas ou rituais.      |

## Cross-References

- `mall/mall-cross-functional-collab.md` — Colaboracao cross-functional.
- `handoff/handoff-qa-with-dev.md` — QA com desenvolvimento.
- `handoff/handoff-specs-and-redlines.md` — Especificacoes e redlines.
- `design-system/ds-design-code-sync-audit.md` — Sincronizacao design-code.
