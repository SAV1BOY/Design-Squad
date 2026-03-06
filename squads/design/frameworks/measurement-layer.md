# Measurement Layer

## Metadata
- **Autor**: Design Squad
- **Categoria**: Stack Layer, Metricas, Analytics
- **Complexidade**: Media-Alta
- **Aplicacao**: Instrumentacao, metricas e feedback loop para design
- **Ultima atualizacao**: 2026-03-06

## Concept

A Measurement Layer e a oitava camada do stack de design, responsavel por fechar o ciclo
entre design e resultado. Sem medicao, design e baseado em intuicao e opiniao; com medicao,
torna-se uma disciplina com feedback loop que se auto-corrige.

A camada engloba tres dimensoes: instrumentacao (como coletar dados), metricas (o que medir)
e feedback loop (como os dados alimentam decisoes de design futuras).

O objetivo nao e medir tudo — e medir o que importa para validar hipoteses de design e
demonstrar impacto. Metricas excessivas criam ruido; metricas insuficientes criam ponto cego.

## When to Use

- Quando se lanca qualquer mudanca de design em producao
- Quando se precisa validar se uma hipotese de design funcionou
- Quando stakeholders pedem evidencia do impacto de design
- Quando se planeja priorizacao de melhorias de UX
- Quando se quer criar cultura de design baseado em dados
- Quando metricas de produto sao insuficientes para medir experiencia

## How to Apply

### Dimensao 1 — Instrumentacao
1. **Defina eventos de tracking** para cada interacao critica:
   - Clicks em CTAs, submissoes de formularios, navegacao
   - Erros encontrados, retries, abandonos
   - Tempo em tela, scroll depth, engagement
2. **Implemente tracking plan** documentado:
   - Nome do evento, propriedades, trigger, frequencia
   - Owner (quem implementa), validador (quem testa)
3. **Ferramentas**: Google Analytics, Mixpanel, Amplitude, Heap, PostHog
4. **Visual analytics**: Hotjar, FullStory para heatmaps e session recordings
5. **Valide instrumentacao**: Teste que eventos estao disparando corretamente
   antes de analisar dados

### Dimensao 2 — Metricas de Design

**Metricas de Tarefa (por fluxo)**:
- Task success rate: % de usuarios que completam a tarefa
- Time on task: tempo medio para completar
- Error rate: % de erros cometidos durante a tarefa
- Abandonment rate: % que desiste no meio
- Steps to completion: numero de passos ate concluir

**Metricas de Satisfacao (periodicas)**:
- SUS (System Usability Scale): questionario padronizado de usabilidade
- CSAT: satisfacao pontual apos interacao
- NPS: recomendacao geral do produto
- CES (Customer Effort Score): facilidade de uso percebida

**Metricas de Adocao (continuas)**:
- Feature adoption rate: % de usuarios que usam nova feature
- Retention: % que volta apos primeira interacao
- Engagement depth: nivel de uso das funcionalidades
- Time to first value: tempo ate primeira acao significativa

**Metricas de Eficiencia Operacional**:
- Support tickets por area de UX: problemas que geram chamados
- Self-service rate: % de tarefas concluidas sem ajuda
- Documentation views: areas da docs mais consultadas

### Dimensao 3 — Feedback Loop
1. **Coleta continua**: Instrumentacao automatica sempre rodando
2. **Analise periodica**: Review semanal ou quinzenal de metricas-chave
3. **Insight generation**: Transformar dados em insights acionaveis
4. **Design iteration**: Ajustar design baseado nos insights
5. **Re-measurement**: Verificar se a mudanca teve o efeito esperado
6. **Knowledge base**: Documentar aprendizados para referencia futura

### Processo de Setup
1. Defina 3-5 metricas-chave alinhadas com objetivos de UX
2. Estabeleca baselines (valores atuais) para cada metrica
3. Defina targets realistas baseados em benchmarks
4. Implemente instrumentacao para coletar dados
5. Crie dashboard acessivel para toda a equipe
6. Estabeleca cadencia de review (semanal recomendado)
7. Documente como cada metrica e calculada e de onde vem

## Key Principles

- **Meca o que importa**: 5 metricas significativas > 50 metricas de vanidade
- **Baseline first**: Sem saber de onde voce parte, nao ha como medir progresso
- **Quanti + quali**: Numeros dizem "o que", pesquisa diz "por que"
- **Feedback loop fechado**: Dados que nao informam decisoes sao desperdicio
- **Instrumentacao e investimento**: Planejar tracking antes de lancar, nao depois
- **Transparencia de metricas**: Todos na equipe devem ter acesso aos dados
- **Humildade com dados**: Correlacao nao e causalidade. Interprete com cuidado

## Examples

### Exemplo 1 — Dashboard de UX Metrics
Metricas trackeadas para um SaaS B2B:
| Metrica                | Baseline | Target  | Atual   | Status |
|------------------------|----------|---------|---------|--------|
| Task success (onboard) | 34%      | 65%     | 58%     | Em progresso |
| Time on task (report)  | 4.2 min  | 2.5 min | 3.1 min | Em progresso |
| SUS Score              | 52       | 72      | 68      | Em progresso |
| Support tickets/semana | 45       | 25      | 31      | Em progresso |
| Feature adoption (new) | 12%      | 40%     | 37%     | Quase la |

### Exemplo 2 — Feedback Loop em Acao
1. Metrica: Abandonment rate no step 3 do checkout = 67%
2. Insight: Heatmap mostra usuarios procurando botao "pular"
3. Hipotese: Tornar step 3 opcional reduzira abandono
4. Implementacao: Step 3 com opcao "Configurar depois"
5. Re-measurement: Abandonment caiu para 23% (+44pp melhoria)
6. Learning: Steps opcionais devem ser claramente marcados como tal

### Exemplo 3 — Tracking Plan
| Evento           | Propriedades        | Trigger            | Owner |
|------------------|---------------------|--------------------|-------|
| checkout_started | cart_value, items   | Click "Checkout"   | FE Dev|
| step_completed   | step_number, time   | Step submission     | FE Dev|
| error_shown      | error_type, step    | Validation failure  | FE Dev|
| checkout_done    | total, method       | Payment confirmed   | BE Dev|
| checkout_abandon | last_step, time     | 30s inactivity     | FE Dev|

## Common Pitfalls

- **Metricas de vanidade**: Pageviews e clicks sem contexto nao medem experiencia
- **Tracking retroativo**: Instrumentar depois de lancar perde dados valiosos do lancamento
- **Data overload**: Dashboards com 30 metricas que ninguem olha
- **Sem qualitativo**: Numeros sem pesquisa qualitativa geram interpretacoes erradas
- **Metricas sem action**: Se nenhuma decisao muda baseada na metrica, nao vale medir
- **Privacy negligence**: Coletar dados sem consentimento ou compliance (LGPD, GDPR)
- **Attribution fantasiosa**: Atribuir toda melhoria de conversao ao redesign ignorando
  outros fatores (sazonalidade, pricing, marketing)

## Cross-References

- [strategy-layer.md](strategy-layer.md) — Metricas vinculadas a hipoteses estrategicas
- [discovery-layer.md](discovery-layer.md) — Dados quantitativos como discovery
- [malouf-ux-strategy-framework.md](malouf-ux-strategy-framework.md) — Metricas na estrategia de UX
- [mall-selling-design-to-stakeholders.md](mall-selling-design-to-stakeholders.md) — Metricas como argumento
- [usability-testing-framework.md](usability-testing-framework.md) — Metricas de teste de usabilidade
- [malouf-research-to-decision.md](malouf-research-to-decision.md) — Dados como evidencia
