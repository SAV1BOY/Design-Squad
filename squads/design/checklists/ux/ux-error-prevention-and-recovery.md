# UX Error Prevention and Recovery

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | UX Error Handling              |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | UX Lead                        |

## Objective

Verificar se o produto implementa estrategias eficazes de prevencao de erros e
mecanismos de recuperacao que permitem ao usuario retomar o fluxo com minimo
impacto. Um bom tratamento de erros transforma frustracao em confianca e reduz
significativamente a carga sobre suporte ao cliente.

## When to Apply

- Ao projetar fluxos criticos (pagamento, cadastro, envio de dados).
- Em auditorias de qualidade de mensagens de erro existentes.
- Quando metricas indicam alta taxa de erros em fluxos especificos.
- Apos incidentes de suporte relacionados a erros de usuario.

## Criteria

- [ ] Validacao inline e aplicada em campos de formulario antes do envio (front-end validation).
- [ ] Mensagens de erro sao especificas, indicando o campo e o que precisa ser corrigido.
- [ ] Mensagens de erro usam linguagem humana, nao codigos tecnicos ou HTTP status.
- [ ] Erros destrutivos (deletar, cancelar) possuem confirmacao com descricao do impacto.
- [ ] Undo e disponivel para acoes reversiveis por tempo definido.
- [ ] Autosave protege dados do usuario contra perda por erro de navegacao ou falha.
- [ ] Campos com formato esperado incluem mascara, placeholder ou exemplo visivel.
- [ ] O sistema previne submissao de formularios com dados invalidos (disable button ou bloqueio).
- [ ] Erros de sistema (500, timeout) possuem tela dedicada com acao sugerida.
- [ ] O usuario e direcionado ao ponto exato do erro, nao ao inicio do formulario.
- [ ] Dados previamente preenchidos sao preservados apos erro de validacao.
- [ ] Empty states orientam o usuario sobre como proceder quando nao ha dados.
- [ ] Existe monitoramento de frequencia e tipo de erros para melhoria continua.
- [ ] Fluxos criticos possuem fallback para cenarios de falha de conectividade.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Acao destrutiva sem confirmacao ou perda de dados sem autosave.           |
| Major    | Mensagens de erro genericas ou dados perdidos apos validacao falhar.      |
| Minor    | Ausencia de validacao inline ou mascaras em campos formatados.            |
| Info     | Oportunidade de implementar undo ou melhorar copy de mensagens de erro.  |

## Cross-References

- `ux/ux-heuristic-evaluation.md` — Avaliacao heuristica (heuristica 5 e 9).
- `ux/ux-cognitive-load-audit.md` — Carga cognitiva.
- `ui/ui-states-and-feedback.md` — Estados e feedback visual.
- `handoff/handoff-edge-cases-documented.md` — Edge cases documentados.
