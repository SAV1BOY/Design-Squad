# Cross-Squad Handoff Protocol

## Metadata

| Campo             | Valor                                          |
|-------------------|-------------------------------------------------|
| scope             | Todas as interacoes entre Design Squad e outros squads |
| created           | 2026-03-18                                      |
| version           | 1.0                                             |
| owner             | Design Lead                                     |
| review-cycle      | Trimestral                                      |
| status            | Ativo                                           |
## Proposito

Este protocolo define as regras universais para qualquer handoff entre o Design Squad e outro squad.
Os contratos especificos herdam estas regras e podem adicionar clausulas, mas nunca contradize-las.
## Regras Gerais

1. Todo handoff deve ter um **owner unico** no squad que envia e um **owner unico** no squad que recebe.
2. Nenhum handoff acontece verbalmente. Toda solicitacao precisa de **registro escrito** em Asana.
3. Deliverables sem **quality gate** completo nao sao aceitos. O squad receptor pode recusar.
4. Comunicacao informal no Slack **nao substitui** a task formal no Asana.
5. Prazos sao contados em **horas e dias uteis** (segunda a sexta, 9h-18h BRT).
6. Todo handoff encerrado gera um **registro de conclusao** no Asana com status e observacoes.
## Como Iniciar um Handoff

### Step 1 — Preparacao interna
- O squad solicitante prepara todos os deliverables listados no contrato especifico.
- O owner do handoff executa o quality gate on send e marca cada item como concluido.
- Se algum item obrigatorio nao pode ser entregue, documentar o motivo e alternativa proposta.

### Step 2 — Abertura da task
- Criar task no Asana usando o template `[Handoff] Design <-> [Squad]`.
- Preencher campos obrigatorios: owner, squad destino, prazo esperado, link dos deliverables.
- Adicionar tag `handoff` e tag do squad destino (ex: `copy-squad`, `brand-squad`).
- Atribuir a task ao owner do squad receptor.

### Step 3 — Notificacao
- Postar no canal Slack dedicado (ex: #design-x-copy) com link da task.
- Formato da mensagem: `[HANDOFF] {titulo} | Prazo: {data} | Task: {link}`.
- Marcar o owner do squad receptor com @mention.
## Como Executar um Handoff

### Step 4 — Acknowledgment
- O squad receptor tem **4 horas uteis** para confirmar recebimento na task do Asana.
- Acknowledgment inclui: confirmacao de que os deliverables estao acessiveis e completos.
- Se deliverables estao incompletos, o receptor lista itens faltantes na task imediatamente.

### Step 5 — Quality gate on receive
- O squad receptor executa o checklist de quality gate on receive do contrato especifico.
- Cada item e marcado como aprovado ou reprovado com comentario explicativo.
- Se todos os itens passam: task avanca para status `Em Andamento`.
- Se algum item falha: task retorna para `Rework Necessario` com detalhamento.

### Step 6 — Execucao
- O squad responsavel pela entrega trabalha nos deliverables dentro do SLA acordado.
- Updates de progresso sao postados na task do Asana a cada 2 dias uteis para tasks longas.
- Duvidas durante execucao sao resolvidas na thread do Slack, com resumo registrado no Asana.

### Step 7 — Entrega
- O squad que esta entregando posta os deliverables finais na task do Asana.
- Executa o quality gate on send antes de mudar o status para `Entregue`.
- Notifica no canal Slack com: `[ENTREGA] {titulo} | Task: {link}`.
## Como Fechar um Handoff

### Step 8 — Validacao final
- O squad receptor executa o quality gate on receive nos deliverables finais.
- Prazo para validacao: **2 dias uteis** apos a entrega.
- Se aprovado: task vai para status `Concluido` com comentario de aceitacao.

### Step 9 — Registro de conclusao
- Owner do handoff registra no Asana: data de conclusao, SLA cumprido (sim/nao), observacoes.
- Se houve rework, registrar numero de ciclos e causa raiz.
- Fechar a task com tag `handoff-concluido`.

### Step 10 — Retrospectiva (quando aplicavel)
- Handoffs com mais de 1 ciclo de rework sao incluidos na retrospectiva trimestral.
- Padroes recorrentes de rework geram acao de melhoria no processo.
## Quality Gates em Cada Etapa

| Etapa           | Gate                                                        | Responsavel    |
|-----------------|-------------------------------------------------------------|----------------|
| Preparacao      | Todos os deliverables obrigatorios estao prontos            | Squad emissor  |
| Abertura        | Task tem todos os campos preenchidos e links funcionais     | Owner do handoff|
| Acknowledgment  | Deliverables acessiveis e completos                         | Squad receptor |
| Validacao       | Checklist do contrato especifico 100% aprovado              | Squad receptor |
| Entrega         | Quality gate on send executado e documentado                | Squad emissor  |
| Fechamento      | Quality gate on receive executado e aceitacao registrada    | Squad receptor |
## Escalation Path

1. **Nivel 1 — Lembrete**: Slack com @mention do owner. Prazo: 24h uteis.
2. **Nivel 2 — Lead intervention (+24h)**: DM para ambos leads com link, impacto e opcoes.
3. **Nivel 3 — Head intervention (+48h)**: reuniao 30min com Heads. Decisao obrigatoria.
4. **Nivel 4 — Workaround**: se bloqueando release, acionar solucao temporaria como divida tecnica.
## SLA Padrao (quando contrato especifico nao define)

| Acao                         | Tempo maximo        |
|------------------------------|---------------------|
| Acknowledgment               | 4 horas uteis       |
| Primeira resposta substantiva| 1 dia util          |
| Entrega de deliverable simples| 3 dias uteis       |
| Entrega de deliverable complexo| 7 dias uteis      |
| Validacao apos entrega       | 2 dias uteis        |
| Ciclo de rework minor        | 2 dias uteis        |
| Ciclo de rework major        | 5 dias uteis        |
## Anti-patterns a Evitar

1. **Handoff fantasma**: combinar no Slack sem abrir task. Ninguem rastreia.
2. **Quality gate bypass**: enviar deliverable "quase pronto". Rework garantido.
3. **Owner difuso**: task atribuida a "todo o squad". Ninguem assume.
4. **Scope creep silencioso**: adicionar deliverables sem atualizar prazo. SLA estoura.
5. **Rework infinito**: mais de 2 ciclos sem escalar. Desgaste cronico.
## Cross-References

- `./handoff-contract-copy-squad.md` — contrato com Copy Squad.
- `./handoff-contract-brand-squad.md` — contrato com Brand Squad.
- `./handoff-contract-traffic-squad.md` — contrato com Traffic Squad.
- `./handoff-contract-storytelling-squad.md` — contrato com Storytelling Squad.
- `../workflows/handoff-and-build-loop.md` — handoff para engenharia.
