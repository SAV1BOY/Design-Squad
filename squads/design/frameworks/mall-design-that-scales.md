# Mall Design That Scales

## Metadata
- **Autor**: Dan Mall
- **Categoria**: Design Operations, Escalabilidade
- **Complexidade**: Alta
- **Aplicacao**: Organizacoes crescendo que precisam escalar praticas de design
- **Ultima atualizacao**: 2026-03-06

## Concept

Design That Scales e a abordagem de Dan Mall para fazer design funcionar em organizacoes
grandes e crescentes. O problema central e que praticas de design que funcionam para uma
equipe de 5 pessoas colapsam quando a organizacao cresce para 50 ou 500.

A solucao nao e simplesmente "contratar mais designers" — e criar sistemas, processos e
cultura que permitam que o output de design mantenha qualidade e consistencia independente
do numero de pessoas envolvidas. Isso envolve padronizar decisoes, codificar principios
em artefatos actionables e criar mecanismos de coordenacao que nao dependam de comunicacao
individual.

Mall argumenta que escalar design e fundamentalmente sobre escalar decisoes: como garantir
que 100 designers tomem decisoes consistentes sem precisar consultar uns aos outros a cada
escolha.

## When to Use

- Quando a equipe de design cresce e a consistencia diminui
- Quando novos designers demoram meses para se alinhar ao padrao de qualidade
- Quando diferentes produtos da mesma empresa parecem ser de empresas diferentes
- Quando designers gastam tempo excessivo em decisoes que ja foram tomadas antes
- Quando a lideranca de design nao consegue mais revisar todo o output
- Quando o design system sozinho nao resolve inconsistencias de experiencia

## How to Apply

### Estrategia 1 — Codifique Decisoes
1. Identifique decisoes que se repetem: cores, espacamentos, layout, tom de voz
2. Transforme cada decisao recorrente em um artefato consultavel:
   - Design tokens para decisoes visuais
   - Guidelines escritas para decisoes de UX
   - Templates de fluxo para decisoes de IA (Information Architecture)
   - Checklists para decisoes de acessibilidade
3. Mantenha um decision log publico para decisoes nao triviais
4. Revise e atualize decisoes codificadas trimestralmente

### Estrategia 2 — Escale Atraves de Padroes
1. Identifique patterns de design que se repetem entre produtos
2. Documente cada pattern com: quando usar, quando nao usar, variantes permitidas
3. Crie uma biblioteca de patterns acessivel e pesquisavel
4. Estabeleca processo para propor novos patterns e deprecar existentes
5. Vincule patterns a componentes implementados no design system

### Estrategia 3 — Crie Mecanismos de Coordenacao
1. **Design critiques**: Sessoes regulares de review entre pares
2. **Office hours**: Tempo dedicado para duvidas e alinhamento
3. **Show and tell**: Compartilhamento semanal de trabalho em andamento
4. **Design principles**: Heuristicas compartilhadas para decisoes rapidas
5. **Quality rubrics**: Criterios explicitos de qualidade para self-assessment

### Estrategia 4 — Estruture o Onboarding
1. Crie um "design starter kit" com tudo que um novo designer precisa
2. Defina um buddy system para os primeiros 30 dias
3. Crie exercicios praticos que ensinam o sistema de design e patterns
4. Estabeleca checkpoints de 30/60/90 dias para validar alinhamento
5. Documente tribal knowledge que normalmente so existe na cabeca das pessoas

### Estrategia 5 — Distribua Lideranca
1. Identifique design leads por area/produto que garantam qualidade local
2. Crie um forum de leads para alinhamento cross-produto
3. Delegue decisoes rotineiras para leads, reserve decisoes estrategicas
4. Faca design leads responsaveis por coaching de designers juniores
5. Rotacione responsabilidades para evitar silos e single points of failure

## Key Principles

- **Decisoes codificadas escalam, pessoas nao**: Documente e sistematize para reduzir dependencia
- **Consistencia suficiente**: 100% de consistencia e impossivel e indesejavel. Busque 80%
- **Autonomia com alinhamento**: Designers devem ter liberdade dentro de guardrails claros
- **Onboarding como investimento**: Tempo investido em onboarding se paga em meses
- **Coordenacao leve**: Prefira mecanismos asincronos a reunioes excessivas
- **Feedback como norma cultural**: Critique o trabalho, nao a pessoa
- **Evolucao continua**: O modelo de escala precisa evoluir conforme a organizacao muda

## Examples

### Exemplo 1 — Decision Library
Uma organizacao com 40 designers criou uma "Decision Library" no Notion com 200+
decisoes documentadas. Cada entrada tinha: contexto, decisao, alternativas consideradas,
racional e data. Novos designers consultavam a library antes de tomar decisoes.
Resultado: tempo de onboarding reduziu de 3 meses para 6 semanas.

### Exemplo 2 — Design Quality Rubric
Uma equipe criou uma rubrica com 5 dimensoes (usabilidade, acessibilidade, consistencia,
clareza, elegancia) cada uma com 4 niveis (1-4). Designers faziam self-assessment antes
de submeter para review. Resultado: 40% menos rounds de revisao e criticas mais objetivas.

### Exemplo 3 — Federated Design Leads
Uma empresa com 8 produtos designou 1 design lead por produto. Leads se reuniam
quinzenalmente para: compartilhar decisoes tomadas, alinhar patterns cross-produto
e escalar conflitos. O modelo manteve consistencia entre produtos sem centralizar
todas as decisoes em uma unica pessoa.

## Common Pitfalls

- **Over-process**: Criar processos demais paralisa a equipe. Comece leve e adicione
  conforme necessario
- **Documentacao morta**: Decisoes documentadas que ninguem consulta sao inutils.
  Integre a consulta no workflow diario
- **Centralizar demais**: Uma pessoa revisando tudo nao escala. Distribua responsabilidade
- **Ignorar cultura**: Processos sem cultura de feedback e colaboracao sao cascas vazias
- **Copiar modelos de big tech**: O que funciona para 200 designers nao e necessario para 20.
  Adapte ao tamanho real da equipe
- **Esquecer do onboarding**: Cada novo membro que entra desalinhado degrada a consistencia
- **Nao medir**: Sem metricas de consistencia e satisfacao, nao ha como saber se o modelo funciona

## Cross-References

- [mall-design-system-team-models.md](mall-design-system-team-models.md) — Modelos de equipe para escala
- [mall-superfriendly-model.md](mall-superfriendly-model.md) — Modelo de colaboracao
- [malouf-designops-framework.md](malouf-designops-framework.md) — DesignOps como enabler de escala
- [malouf-design-quality-model.md](malouf-design-quality-model.md) — Rubricas de qualidade
- [governance-layer.md](governance-layer.md) — Processos de governanca
- [design-ops-cadence.md](design-ops-cadence.md) — Cadencias operacionais
