# Design Decision Phrases

## Context

Frases prontas para articular e documentar decisões de design. Cada decisão precisa
de rationale claro — não apenas "o que" foi decidido, mas "por que". Decisões bem
documentadas evitam revisitas desnecessárias e constroem a memória institucional
do Design Squad.

**Aplicação:** ADRs, design docs, reviews, comunicação com stakeholders
**Tom:** Evidence-Driven + System Thinker

## Phrases

### Documentando a decisão
- "Decidimos usar [abordagem] porque [razão baseada em dados/pesquisa/princípio]."
- "A escolha de [componente/pattern] foi baseada em: (1) [critério], (2) [critério], (3) [critério]."
- "Entre [opção A] e [opção B], escolhemos [A] porque resolve [requisito prioritário] com menor custo de implementação."
- "Essa decisão é reversível / irreversível. Se os dados pós-lançamento mostrarem [sinal], revisamos em [prazo]."
- "Essa decisão se alinha com o princípio de design '[nome do princípio]': [como se aplica]."

### Justificando com dados
- "Os testes de usabilidade com [N] participantes mostraram que [abordagem] teve task completion rate de [X]% vs. [Y]% da alternativa."
- "O benchmarking com [N] concorrentes revelou que [pattern] é o padrão do mercado — desviar teria custo de aprendizado para o usuário."
- "A análise de heatmap mostra que [X]% dos clicks acontecem em [área], validando a hierarquia visual proposta."
- "O custo de implementação de [abordagem A] é [N] story points vs. [M] de [abordagem B], com benefício similar."

### Justificando sem dados (hipótese fundamentada)
- "Não temos dados específicos para este caso, mas a literatura de UX (NNGroup / Baymard / Laws of UX) sugere [princípio]."
- "Baseado na experiência com features similares ([exemplo]), esperamos [resultado]. Validaremos com [método] pós-lançamento."
- "Esta é uma decisão de design informed by heuristics — especificamente [heurística]. Marcar para validação em [prazo]."
- "A hipótese é que [abordagem] performará melhor porque [lógica]. A/B test planejado para o primeiro mês."

### Comunicando trade-offs
- "Ao escolher [A], abrimos mão de [B]. O trade-off é aceitável porque [razão]."
- "Sabemos que [limitação] é uma consequência desta decisão. O plano para mitigar é [ação]."
- "Essa decisão prioriza [critério 1] sobre [critério 2]. Em contextos onde [critério 2] é mais importante, a abordagem deveria ser [alternativa]."
- "Simplicidade para o usuário vs. flexibilidade do sistema: priorizamos simplicidade porque [dados]."

### Revisando decisões anteriores
- "A decisão de [data] sobre [tema] precisa ser revisitada porque [novo dado/contexto]."
- "Os dados pós-lançamento invalidam a hipótese original. [Métrica] ficou em [valor] vs. [esperado]."
- "O contexto mudou desde a decisão original: [o que mudou]. Proponho reavaliar com base em [novos dados]."
- "Mantemos a decisão de [tema]. Os dados de [período] confirmam: [métrica] está em [valor], alinhado com o esperado."

### Comunicando para não-designers
- "Escolhemos [abordagem] para tornar a experiência mais simples para o usuário — menos etapas, menos atrito."
- "Essa decisão reduz risco de erros do usuário em [X]%, baseado nos testes realizados."
- "O padrão escolhido é familiar para o usuário — é o mesmo usado por [apps conhecidos]."
- "Em termos de impacto: essa decisão pode melhorar [métrica de negócio] em [estimativa]."

## Variations

- Para ADR: formato completo com contexto, decisão, alternativas, consequências
- Para Slack: "Decisão: [o quê]. Razão: [1 frase]. Trade-off: [1 frase]."
- Para sprint review: visual before/after + métrica de impacto
- Para documentação: incluir links para dados, specs e discussões anteriores

## When to Use

- Documentação formal de decisões (ADRs)
- Design reviews quando questionado sobre escolhas
- Sprint reviews para explicar direção do design
- Retrospectivas para avaliar decisões passadas
- Onboarding para explicar "por que as coisas são assim"
