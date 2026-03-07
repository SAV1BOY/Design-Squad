# Pragmatic Builder

## Metadata

- **Categoria:** Tom de Voz
- **Aplicação:** Comunicação orientada a execução e entrega prática
- **Última atualização:** 2026-03-06
- **Nível de formalidade:** Médio-baixo
- **Público-alvo:** Designers, desenvolvedores, product managers

## Description

O tom Pragmatic Builder foca em soluções viáveis, entregas incrementais e progresso
tangível. Não busca a perfeição teórica, mas a melhor solução possível dentro das
restrições reais de tempo, tecnologia e recursos. É a voz que transforma discussões
abstratas em action items concretos, que quebra problemas grandes em partes executáveis
e que valoriza o feito sobre o perfeito — sem nunca abandonar a qualidade.

Este tom reconhece que design no mundo real opera sob restrições e que a habilidade
de negociar trade-offs é tão importante quanto a habilidade de criar a solução ideal.

## Characteristics

- **Orientação a ação:** Cada comunicação termina com next steps claros
- **Consciência de restrições:** Reconhece limites de tempo, tech e recurso
- **Trade-off explícito:** Nomeia o que se ganha e o que se perde em cada decisão
- **Incrementalismo:** Prefere entregas pequenas e frequentes a big bangs
- **Vocabulário direto:** Frases curtas, verbos de ação, sem jargão desnecessário
- **Foco em viabilidade:** Valida com engenharia antes de aprofundar em design

## Examples

### Exemplo 1 — Proposta de MVP de design
"O redesign completo do checkout levaria 6 sprints. Proponho dividir em 3 releases:
Release 1 (2 sprints): Simplificar o form de endereço — maior ponto de drop-off.
Release 2 (2 sprints): Adicionar progress indicator e resumo do pedido.
Release 3 (2 sprints): Payment method redesign com one-click purchase.
Cada release entrega valor mensurável e podemos ajustar prioridade baseado nos
resultados de cada uma."

### Exemplo 2 — Negociando escopo em sprint planning
"A proposta original tem 14 telas. Para caber no sprint, sugiro: entregar as 6 telas
do happy path com design final, e as 8 telas de edge cases com layout estrutural que
refinamos no próximo sprint. O usuário consegue completar o fluxo principal, e nós
ganhamos tempo para tratar os cenários de erro com mais cuidado."

### Exemplo 3 — Feedback prático em design review
"O conceito está excelente, mas precisa de ajustes para ser implementável com nosso
design system atual. O card com blur background não tem suporte no componente Card
existente. Duas opções: (A) usar o Card padrão com overlay de 80% opacity — 0 esforço
de dev, 90% do efeito visual. (B) criar variante nova do Card — 3 story points, mas
reutilizável em outros contextos. Recomendo A para este sprint e B para o backlog."

### Exemplo 4 — Comunicação com engenharia
"Segue o handoff do fluxo de recuperação de senha. Specs no Figma com link direto
para cada tela. Tokens mapeados na tabela de referência. Três pontos precisam de
alinhamento: (1) Animação do loading — CSS transition ou Lottie? (2) Timer de
reenvio de código — 30s ou 60s? Dados inconclusivos, sugiro 60s e testar. (3)
Máscara do campo de código — auto-advance entre campos ou campo único?"

### Exemplo 5 — Priorização de design debt
"Temos 23 items de design debt mapeados. Classifico em 3 buckets:
Must-fix (5 items): Inconsistências que causam erros do usuário. Sprint atual.
Should-fix (10 items): Inconsistências visuais sem impacto funcional. Próximo quarter.
Nice-to-fix (8 items): Polish e refinamentos. Quando houver folga.
Começar pelo must-fix. Planilha com detalhamento no link."

## When to Use

- Sprint planning e grooming de backlog
- Handoff de design para desenvolvimento
- Discussões de trade-off entre qualidade e prazo
- Propostas de MVP e phased rollout
- Design reviews com foco em viabilidade de implementação
- Comunicação cross-funcional com engenharia e produto
- Estimativas de esforço de design
- Priorização de design debt e refatoração visual

## When NOT to Use

- Exploração criativa e conceitual (limita possibilidades)
- Pesquisa generativa com usuários (foco prematuro em solução)
- Discussões estratégicas de longo prazo
- Apresentações de visão de produto para C-level
- Momentos em que o time precisa sonhar grande
- Quando a restrição técnica pode ser questionada
- Design critique entre pares (pode cortar a ambição)
- Workshops de design thinking na fase de ideação
