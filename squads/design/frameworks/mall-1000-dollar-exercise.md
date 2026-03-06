# Mall $1000 Dollar Exercise

## Metadata
- **Autor**: Dan Mall
- **Categoria**: Priorizacao, Alinhamento de Stakeholders
- **Complexidade**: Baixa
- **Aplicacao**: Workshops de priorizacao e alinhamento entre equipe e stakeholders
- **Ultima atualizacao**: 2026-03-06

## Concept

O $1000 Dollar Exercise e uma tecnica de priorizacao criada por Dan Mall onde participantes
recebem um orcamento ficticio de $1000 para distribuir entre diferentes opcoes, features
ou areas de investimento. A mecanica de soma-zero forca tradeoffs explicitos: investir
mais em uma area significa investir menos em outra.

A genialidade do exercicio esta na simplicidade. Em vez de pedir que pessoas classifiquem
prioridades de 1 a 5 (onde tudo vira "alta prioridade"), o orcamento limitado forca
diferenciacoes reais. Se alguem coloca $400 em performance e $100 em animacoes, a
mensagem e clara sobre o que importa mais.

O exercicio funciona como ferramenta de alinhamento: quando todos os participantes fazem
o exercicio individualmente e depois compartilham resultados, divergencias ficam visiveis
e podem ser discutidas produtivamente.

## When to Use

- No inicio de um projeto para alinhar prioridades entre stakeholders
- Quando a equipe precisa decidir onde investir tempo limitado
- Quando ha desacordo sobre o que e mais importante
- Durante planning de trimestre ou sprint para priorizar backlog
- Quando stakeholders dizem que "tudo e prioridade"
- Para alinhar expectativas sobre escopo e investimento em design system

## How to Apply

### Preparacao (15 min)
1. Defina as categorias de investimento (5-10 opcoes e ideal)
   - Exemplos para design system: componentes, documentacao, tokens, tooling,
     acessibilidade, performance, onboarding, governanca
   - Exemplos para produto: features, UX, performance, seguranca, design,
     divida tecnica, testes, analytics
2. Prepare um template simples (planilha, post-its ou formulario)
3. Reuna os participantes: inclua designers, devs, PMs e stakeholders

### Execucao Individual (10 min)
1. Distribua o template para cada participante
2. Instrua: "Voce tem $1000 para distribuir entre essas categorias"
3. Regras:
   - Cada categoria deve receber pelo menos $0 (pode ser zero)
   - O total deve somar exatamente $1000
   - Sem frações — increments de $50 funcionam bem
   - Nao discuta com outros durante esta fase
4. Cada pessoa preenche individualmente e em silencio

### Revelacao e Discussao (30-45 min)
1. Colete todos os resultados e mostre lado a lado
2. Calcule a media de investimento por categoria
3. Identifique areas de consenso (todos investiram alto ou baixo)
4. Identifique areas de divergencia (investimentos muito diferentes)
5. Discuta as divergencias:
   - "Por que voce colocou $300 em documentacao e voce colocou $50?"
   - "O que te fez priorizar performance acima de tudo?"
6. Nao busque consenso forcado — entenda as perspectivas

### Sintese (15 min)
1. Apos discussao, permita uma segunda rodada de alocacao (opcional)
2. Consolide os resultados em uma distribuicao acordada pela equipe
3. Traduza a distribuicao em proporcoes de esforco reais:
   - $300/1000 em componentes = ~30% do tempo do sprint em componentes
4. Documente o resultado e as justificativas
5. Revise a alocacao periodicamente (a cada quarter)

## Key Principles

- **Soma-zero forca tradeoffs**: Orcamento limitado impede que tudo seja "prioridade 1"
- **Individual antes de coletivo**: Cada pessoa decide sozinha antes de ver os outros
- **Divergencias sao dados**: Desacordos revelam premissas e valores diferentes
- **Simplicidade da mecanica**: Qualquer pessoa entende "$1000 para distribuir"
- **Numeros concretos**: $300 vs $100 e mais claro que "alta" vs "media" prioridade
- **Democracia ponderada**: Todos os participantes tem voz igual no exercicio
- **Repetibilidade**: O exercicio pode ser repetido para recalibrar ao longo do tempo

## Examples

### Exemplo 1 — Priorizacao de Design System
Categorias: Componentes, Tokens, Documentacao, Tooling, A11y, Performance, Governance.

Resultados:
| Categoria     | Designer 1 | Designer 2 | Dev 1 | Dev 2 | PM    | Media |
|---------------|-----------|-----------|-------|-------|-------|-------|
| Componentes   | $300      | $250      | $200  | $300  | $200  | $250  |
| Tokens        | $100      | $200      | $150  | $100  | $50   | $120  |
| Documentacao  | $150      | $100      | $200  | $150  | $150  | $150  |
| Tooling       | $50       | $50       | $200  | $200  | $100  | $120  |
| A11y          | $200      | $200      | $100  | $100  | $200  | $160  |
| Performance   | $100      | $100      | $100  | $100  | $100  | $100  |
| Governance    | $100      | $100      | $50   | $50   | $200  | $100  |

Insight: Consenso forte em componentes como prioridade. Divergencia significativa
em tooling (devs investem mais) e governance (PM investe mais).

### Exemplo 2 — Priorizacao de Feature
Uma equipe usou o exercicio para priorizar o backlog do trimestre entre 8 features.
O resultado revelou que PM e stakeholders priorizavam features de growth enquanto
designers e devs priorizavam refatoracao de UX. A discussao subsequente levou a um
compromisso: 60% growth features, 40% refatoracao de UX existente.

### Exemplo 3 — Variacao com Rounds
Uma equipe fez 3 rounds do exercicio:
- Round 1: Prioridades individuais sem discussao
- Round 2: Apos 20 min de discussao sobre divergencias, nova alocacao
- Round 3: Alocacao final de consenso

A variacao entre rounds mostrou que a discussao moveu $200 de "novas features" para
"melhorar features existentes", indicando que a conversa mudou perspectivas reais.

## Common Pitfalls

- **Categorias demais**: Mais de 10 categorias dilui as alocacoes e dificulta tradeoffs.
  Mantenha entre 5 e 8
- **Categorias vagas**: "Melhorar a UX" e vago demais. Use categorias especificas e
  concretas que todos entendam
- **Influencia do grupo**: Se a alocacao nao for individual primeiro, vozes dominantes
  influenciam o resultado. Sempre comece em silencio
- **Ignorar divergencias**: As divergencias sao a parte mais valiosa do exercicio.
  Nao as apague calculando medias sem discutir
- **Tratar como votacao definitiva**: O exercicio e input para decisao, nao a decisao final.
  Lideranca pode ajustar baseada em fatores adicionais
- **Nao revisitar**: Prioridades mudam. Repita o exercicio a cada trimestre
- **Participantes homogeneos**: Se so designers participam, o resultado e enviesado.
  Inclua todas as disciplinas e stakeholders relevantes

## Cross-References

- [mall-selling-design-to-stakeholders.md](mall-selling-design-to-stakeholders.md) — Comunicacao de prioridades
- [mall-design-system-strategy.md](mall-design-system-strategy.md) — Estrategia informada por priorizacao
- [strategy-layer.md](strategy-layer.md) — Priorizacao como parte da camada estrategica
- [malouf-ux-strategy-framework.md](malouf-ux-strategy-framework.md) — Roadmap baseado em prioridades
- [design-debt-management.md](design-debt-management.md) — Priorizacao de divida de design
- [design-ops-cadence.md](design-ops-cadence.md) — Exercicio como ritual periodico
