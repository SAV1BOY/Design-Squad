# UX Cognitive Load Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | UX Psychology                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | UX Lead                        |

## Objective

Avaliar a carga cognitiva imposta ao usuario em fluxos criticos do produto, identificando
oportunidades de simplificacao. Carga cognitiva excessiva causa erros, abandono e
frustacao. Este checklist aborda as tres dimensoes: intrinseca, extrinseca e germane.

## When to Apply

- Em fluxos com alta taxa de abandono ou erro.
- Ao projetar formularios complexos ou fluxos multi-step.
- Em auditorias de usabilidade de features existentes.
- Quando dados quantitativos indicam tempo excessivo para conclusao de tarefas.

## Criteria

- [ ] O numero de opcoes por tela segue a Hick's Law (minimo necessario para a decisao).
- [ ] Informacoes sao agrupadas logicamente usando principios de Gestalt (proximity, similarity).
- [ ] Formularios utilizam progressive disclosure, revelando campos conforme necessidade.
- [ ] Labels e instrucoes sao claros, concisos e posicionados proximos aos elementos.
- [ ] Defaults inteligentes sao utilizados para reduzir decisoes do usuario.
- [ ] O numero de passos em fluxos multi-step e minimizado sem comprometer a clareza.
- [ ] Indicadores de progresso sao visiveis em fluxos com multiplas etapas.
- [ ] Informacoes previamente fornecidas nao sao solicitadas novamente.
- [ ] A hierarquia visual guia o olhar do usuario para a acao principal.
- [ ] Jargoes tecnicos e terminologia interna sao evitados ou explicados.
- [ ] Opcoes mutuamente exclusivas sao apresentadas de forma que elimine ambiguidade.
- [ ] O usuario nao precisa lembrar informacoes entre telas ou etapas.
- [ ] Feedback visual confirma acoes do usuario imediatamente (loading, success, error).
- [ ] Testes de 5-second test validam compreensao da hierarquia de informacao.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Fluxo exige memorizacao entre telas ou apresenta mais de 10 opcoes sem agrupamento. |
| Major    | Ausencia de progressive disclosure em formularios complexos.              |
| Minor    | Defaults nao otimizados ou indicador de progresso ausente.                |
| Info     | Oportunidade de simplificar texto ou melhorar agrupamento visual.         |

## Cross-References

- `ux/ux-heuristic-evaluation.md` — Avaliacao heuristica.
- `ux/ux-information-scent-audit.md` — Auditoria de information scent.
- `ux/ux-error-prevention-and-recovery.md` — Prevencao de erros.
- `ui/ui-visual-hierarchy.md` — Hierarquia visual.
