# UX Heuristic Evaluation

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | UX Evaluation                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | UX Lead                        |

## Objective

Conduzir avaliacao heuristica estruturada dos fluxos do produto, utilizando as
heuristicas de Nielsen como base e complementando com heuristicas especificas do
dominio. A avaliacao heuristica identifica problemas de usabilidade de forma rapida
e economica, sem necessidade de recrutamento de participantes.

## When to Apply

- Antes de testes de usabilidade para identificar problemas obvios.
- Em auditorias trimestrais de qualidade UX do produto.
- Ao avaliar concorrentes ou referencias (benchmarking).
- Em revisoes de design antes do handoff para engenharia.

## Criteria

- [ ] Visibilidade do status do sistema: o usuario sempre sabe o que esta acontecendo.
- [ ] Correspondencia entre sistema e mundo real: linguagem e convencoes sao familiares.
- [ ] Controle e liberdade do usuario: saidas de emergencia e undo sao claros e acessiveis.
- [ ] Consistencia e padroes: elementos similares se comportam de forma identica.
- [ ] Prevencao de erros: o design previne erros antes que eles ocorram.
- [ ] Reconhecimento em vez de memorizacao: informacoes necessarias sao visiveis ou facilmente recuperaveis.
- [ ] Flexibilidade e eficiencia de uso: atalhos e aceleradores estao disponiveis para usuarios experientes.
- [ ] Design estetico e minimalista: nenhuma informacao irrelevante compete com informacao relevante.
- [ ] Ajuda para reconhecer, diagnosticar e recuperar erros: mensagens de erro sao claras e acionaveis.
- [ ] Ajuda e documentacao: informacao de ajuda e facil de encontrar e orientada a tarefa.
- [ ] Cada problema encontrado esta classificado por severidade (0-4 escala de Nielsen).
- [ ] Avaliacao foi conduzida por pelo menos 3 avaliadores independentes.
- [ ] Resultados foram consolidados, deduplicados e priorizados para acao.
- [ ] Recomendacoes de melhoria acompanham cada problema identificado.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Violacao de heuristica que impede conclusao de tarefa critica.            |
| Major    | Violacao que causa confusao significativa ou desvio de fluxo.             |
| Minor    | Violacao cosmetica ou que causa leve desconforto ao usuario.              |
| Info     | Sugestao de melhoria que elevaria a experiencia sem resolver problema.    |

## Cross-References

- `ux/ux-cognitive-load-audit.md` — Auditoria de carga cognitiva.
- `ux/ux-error-prevention-and-recovery.md` — Prevencao e recuperacao de erros.
- `ux/ux-task-completion-audit.md` — Auditoria de conclusao de tarefas.
- `malouf/malouf-design-quality-principles-audit.md` — Principios de qualidade.
