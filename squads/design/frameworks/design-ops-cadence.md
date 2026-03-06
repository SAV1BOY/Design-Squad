# Design Ops Cadence

## Metadata
- **Autor**: Design Squad
- **Categoria**: DesignOps, Cadencia, Rituais
- **Complexidade**: Media
- **Aplicacao**: Definir cadencias semanal e mensal, gestao de backlog e divida de design
- **Ultima atualizacao**: 2026-03-06

## Concept

Design Ops Cadence define os rituais regulares, frequencias e responsabilidades operacionais
que mantem a equipe de design funcionando de forma saudavel e produtiva. Sem cadencia
explicita, equipes oscilam entre periodos de super-atividade e estagnacao, acumulam divida
de design invisivel e perdem alinhamento progressivamente.

O framework organiza rituais em tres horizontes: semanal (execucao tatica), mensal
(revisao e ajuste) e trimestral (direcionamento estrategico). Cada ritual tem proposito,
formato, duracao e output definidos.

Alem dos rituais, o framework aborda gestao de backlog de design e monitoramento de divida,
garantindo que trabalho pendente e debitos acumulados sejam visiveis e priorizados.

## When to Use

- Quando a equipe de design nao tem rituais regulares definidos
- Quando existe sensacao de "apagar incendios" constantemente
- Quando divida de design se acumula sem visibilidade
- Quando decisoes de design nao sao comunicadas ou documentadas
- Quando novos membros da equipe nao entendem o ritmo de trabalho
- Quando se quer melhorar previsibilidade e eficiencia da equipe

## How to Apply

### Cadencia Semanal

**Segunda — Planning (30 min)**
- Revisar prioridades da semana
- Alocar designers para tarefas
- Identificar blockers e dependencias
- Output: board de tarefas atualizado para a semana

**Terca/Quarta — Design Critique (45 min)**
- 2-3 designers apresentam trabalho em andamento
- Feedback estruturado usando rubrica de qualidade
- Formato: 10 min apresentacao + 15 min feedback por trabalho
- Output: action items claros para cada trabalho revisado

**Quinta — Show and Tell (30 min, aberto para toda a org)**
- 1-2 designers mostram trabalho concluido ou em progresso
- Foco em compartilhar decisoes e aprendizados
- Aberto para perguntas de qualquer pessoa
- Output: visibilidade do trabalho de design para a organizacao

**Sexta — Housekeeping (20 min async)**
- Atualizar status das tarefas no board
- Documentar decisoes tomadas na semana
- Registrar divida de design identificada
- Preparar items para planning de segunda

### Cadencia Mensal

**Design System Review (1h, primeira semana)**
- Revisar metricas de adocao e satisfacao do DS
- Triage de issues e requests pendentes
- Priorizar backlog do DS para o mes
- Output: prioridades do DS para as proximas 4 semanas

**Design Quality Review (1h, segunda semana)**
- Avaliar 3-5 features entregues no mes anterior
- Usar rubrica de qualidade para avaliacao
- Identificar padroes de problemas recorrentes
- Output: acoes para melhorar qualidade sistematica

**Retrospectiva de Design (1h, terceira semana)**
- O que funcionou bem no processo
- O que pode melhorar
- Experimentos a tentar no proximo mes
- Output: 1-2 melhorias de processo para implementar

**Knowledge Sharing (1h, quarta semana)**
- Deep dive em um topico relevante
- Pode ser: case study, ferramenta, tecnica, artigo
- Rotacao: cada mes um membro diferente apresenta
- Output: aprendizado compartilhado e documentado

### Cadencia Trimestral

**Strategy Review (2h)**
- Revisar UX strategy e metricas
- Avaliar progresso do roadmap de design
- Ajustar prioridades para o proximo quarter
- Output: roadmap atualizado e prioridades realinhadas

**Interface Inventory (3h)**
- Auditoria visual do produto
- Identificar inconsistencias acumuladas
- Priorizar consolidacoes
- Output: lista de divida de design priorizada

**Skills Assessment (1h)**
- Revisar competencias da equipe
- Identificar gaps e oportunidades de desenvolvimento
- Planejar treinamentos e aprendizados do quarter
- Output: plano de desenvolvimento por pessoa

### Gestao de Backlog
1. Mantenha um board unico e priorizado de tarefas de design
2. Categorize: Discovery, Design, Handoff, Design System, Divida
3. Priorize semanalmente usando criterios: impacto, urgencia, esforco
4. Limite WIP (work in progress): maximo 2 itens por designer
5. Revise items sem progresso ha mais de 2 semanas

### Gestao de Divida de Design
1. **Inventario**: Mantenha lista visivel de divida identificada
2. **Classificacao**: Cosmetica, Funcional, Estrutural, de Acessibilidade
3. **Priorizacao**: Severidade x Frequencia x Custo de correcao
4. **Alocacao**: Reserve 20% da capacidade semanal para reduzir divida
5. **Tracking**: Monitore volume de divida mensalmente (crescendo ou diminuindo?)

## Key Principles

- **Ritmo cria previsibilidade**: Cadencia regular reduz ansiedade e melhora planning
- **Rituais com proposito**: Cada ritual tem output definido. Sem output, cancele
- **Cadencia adaptavel**: Comece com o minimo e adicione conforme necessidade
- **Divida visivel**: Divida de design escondida cresce exponencialmente
- **Capacity para divida**: Sem tempo alocado explicitamente, divida nunca e paga
- **Async quando possivel**: Nem tudo precisa de reuniao. Prefira async para status updates
- **Documentacao leve**: Decisions devem ser registradas, mas sem overhead excessivo

## Examples

### Exemplo 1 — Calendario Semanal
| Dia     | Ritual           | Duracao | Participantes    |
|---------|------------------|---------|------------------|
| Segunda | Planning         | 30 min  | Design team      |
| Terca   | Critique         | 45 min  | Design team      |
| Quarta  | Office Hours DS  | 30 min  | Design + devs    |
| Quinta  | Show and Tell    | 30 min  | Aberto           |
| Sexta   | Housekeeping     | 20 min  | Async individual |

Total: 2h25 de rituais por semana (menos de 6% do tempo disponivel).

### Exemplo 2 — Dashboard de Divida
Uma equipe trackava divida de design no Notion:
| Item                      | Tipo        | Severidade | Sprints Pendente |
|---------------------------|-------------|------------|------------------|
| Modals inconsistentes     | Estrutural  | Alta       | 6                |
| Contraste em textos sec.  | A11y        | Alta       | 4                |
| Spacing inconsistente     | Cosmetica   | Media      | 8                |
| Empty states faltando     | Funcional   | Media      | 3                |

Alocaram 1 dia/semana por designer para reduzir divida. Em 2 meses,
resolveram os 2 itens de alta severidade.

### Exemplo 3 — Evolucao de Cadencia
- Equipe de 3 designers: Planning + Critique semanal, Retro mensal
- Equipe de 8 designers: + Show and Tell, + DS Review, + Quality Review
- Equipe de 15 designers: + Office Hours, + Knowledge Sharing, + Strategy quarterly

## Common Pitfalls

- **Rituais demais**: Designers em reunioes o dia todo nao projetam. Mantenha leve
- **Rituais sem enforcement**: Rituais opcionais morrem em 2 semanas. Comprometa-se
- **Critique sem estrutura**: Feedback desestruturado e improdutivo. Use rubrica
- **Divida invisivel**: Se nao esta no board, nao existe para efeitos de priorizacao
- **Zero tempo para divida**: "Vamos pagar divida quando der" = nunca
- **Cadencia rigida**: Se um ritual nao esta gerando valor, mude ou cancele
- **Documentacao excessiva**: Registre decisoes, nao atas detalhadas de reuniao

## Cross-References

- [malouf-designops-framework.md](malouf-designops-framework.md) — DesignOps completo
- [design-debt-management.md](design-debt-management.md) — Gestao detalhada de divida
- [malouf-design-quality-model.md](malouf-design-quality-model.md) — Rubrica para critiques
- [frost-maintaining-design-systems.md](frost-maintaining-design-systems.md) — Cadencia do DS
- [governance-layer.md](governance-layer.md) — Processos de governanca
- [mall-design-that-scales.md](mall-design-that-scales.md) — Cadencia em escala
