# Malouf Service Blueprint Quality

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Malouf                         |
| Domain      | Service Design                 |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Malouf Lead                    |

## Objective

Avaliar a qualidade dos service blueprints criados pelo time, verificando se eles
mapeiam adequadamente a experiencia end-to-end do usuario, incluindo frontstage,
backstage, processos de suporte e pontos de falha. Blueprints de qualidade revelam
oportunidades de melhoria sistemica que nao sao visiveis em analises pontuais.

## When to Apply

- Ao mapear novos servicos ou fluxos complexos envolvendo multiplos touchpoints.
- Em redesign de experiencias que cruzam canais (omnichannel).
- Quando reclamacoes de usuarios indicam falhas em processos internos.
- Em workshops estrategicos de melhoria de servico.

## Criteria

- [ ] O blueprint cobre a jornada completa do usuario, do gatilho inicial ao pos-servico.
- [ ] Acoes do usuario (customer actions) estao claramente documentadas em cada etapa.
- [ ] Frontstage interactions (touchpoints visiveis ao usuario) estao mapeadas.
- [ ] Backstage interactions (processos internos nao visiveis) estao documentadas.
- [ ] Support processes (sistemas, ferramentas, infraestrutura) estao identificados.
- [ ] A line of visibility separa claramente o que o usuario ve do que nao ve.
- [ ] Pontos de falha (failure points) estao sinalizados com probabilidade e impacto.
- [ ] Momentos de espera (wait points) estao identificados com duracao estimada.
- [ ] Evidencias fisicas (physical evidence) em cada touchpoint estao documentadas.
- [ ] O blueprint esta baseado em dados reais (pesquisa, analytics, entrevistas).
- [ ] Oportunidades de melhoria estao priorizadas e vinculadas a metricas de impacto.
- [ ] O blueprint foi validado com representantes de todas as areas envolvidas.
- [ ] Existe versionamento do blueprint com historico de evolucao.
- [ ] O blueprint e acessivel e compreensivel para audiencias nao-design.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Blueprint nao baseado em dados reais ou line of visibility ausente.      |
| Major    | Pontos de falha nao identificados ou backstage nao mapeado.              |
| Minor    | Evidencias fisicas ausentes ou versionamento inexistente.                |
| Info     | Oportunidade de enriquecer com dados quantitativos ou metricas.          |

## Cross-References

- `malouf/malouf-ux-strategy-audit.md` — Estrategia de UX.
- `malouf/malouf-facilitation-quality.md` — Qualidade de facilitacao.
- `ux/ux-task-completion-audit.md` — Auditoria de conclusao de tarefas.
- `research/research-triangulation-quality.md` — Triangulacao de pesquisa.
