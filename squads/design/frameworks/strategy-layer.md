# Strategy Layer

## Metadata
- **Autor**: Design Squad
- **Categoria**: Stack Layer, Estrategia
- **Complexidade**: Alta
- **Aplicacao**: Definir hipoteses, trade-offs, metricas e plano de acao de design
- **Ultima atualizacao**: 2026-03-06

## Concept

A Strategy Layer e a segunda camada do stack de design, onde insights da discovery sao
transformados em direcao estrategica. Aqui a equipe formula hipoteses, define metricas
de sucesso, explicita trade-offs e cria um plano para atingir objetivos.

A estrategia de design nao e separada da estrategia de produto — e a dimensao de experiencia
da estrategia de produto. Enquanto a estrategia de produto define "o que construir e por que",
a estrategia de design define "como a experiencia vai se manifestar e como saberemos se
funciona".

O output desta camada sao decisoes fundamentadas que guiam todo o trabalho de design
subsequente, evitando que a equipe opere sem direcao ou mude de rumo constantemente.

## When to Use

- Apos a fase de discovery, quando se tem insights suficientes para direcionar
- Quando a equipe precisa decidir entre abordagens de design concorrentes
- Quando se planeja investimento de UX para o proximo quarter
- Quando stakeholders precisam entender e aprovar a direcao de design
- Quando ha restricoes significativas que exigem trade-offs explicitos
- Quando multiplas equipes precisam alinhar em uma direcao comum

## How to Apply

### Elemento 1 — Hipoteses de Design
1. Transforme insights da discovery em hipoteses testaveis:
   - Template: "Acreditamos que [mudanca de design] vai [impacto esperado]
     para [segmento de usuario] porque [racional baseado em insight]"
2. Priorize hipoteses por: confianca no racional, impacto esperado, custo de teste
3. Defina como cada hipotese sera validada (A/B test, usability test, analytics)
4. Documente hipoteses nao priorizadas para futuro
5. Aceite que hipoteses podem ser invalidadas — isso e sucesso, nao fracasso

### Elemento 2 — Trade-offs Explicitos
1. Para cada decisao estrategica, documente o que esta sendo privilegiado
   e o que esta sendo sacrificado:
   - "Privilegiamos simplicidade sobre completude no v1"
   - "Privilegiamos mobile-first sobre paridade desktop"
   - "Privilegiamos velocidade de lancamento sobre polish visual"
2. Valide trade-offs com stakeholders antes de prosseguir
3. Use os trade-offs como criterio de decisao durante a execucao
4. Revise trade-offs se o contexto mudar significativamente

### Elemento 3 — Metricas de Sucesso
1. Para cada hipotese, defina 1-2 metricas primarias
2. Defina baseline (valor atual) e target (valor esperado apos mudanca)
3. Defina timeline para medir (quando verificaremos se funcionou)
4. Inclua guardrail metrics (metricas que nao podem piorar):
   - "Task success rate deve subir de 65% para 80%, sem aumentar
     time-on-task em mais de 10%"
5. Documente como as metricas serao instrumentadas e coletadas

### Elemento 4 — Plano de Acao
1. Quebre a estrategia em iniciativas concretas
2. Para cada iniciativa: escopo, owner, timeline, dependencias
3. Defina milestones com deliverables claros:
   - M1 (semana 2): Wireframes validados
   - M2 (semana 4): Prototipo testado com 5 usuarios
   - M3 (semana 6): Design specs entregues para dev
   - M4 (semana 10): Feature em producao
4. Identifique riscos e planos de mitigacao
5. Defina cadencia de review do plano (quinzenal recomendado)

## Key Principles

- **Hipoteses sao apostas informadas**: Nao precisam estar certas, precisam ser testaveis
- **Trade-offs sao inevitaveis**: Explicita-los e melhor que fingir que nao existem
- **Metricas criam accountability**: Sem metricas, sucesso e subjetivo
- **Plano e vivo**: Estrategia que nao se adapta a realidade e dogma, nao plano
- **Alinhamento e prerequisito**: Estrategia desalinhada com stakeholders gera conflito
- **Simplicidade estrategica**: Estrategia complexa demais nao e seguida. 3-5 prioridades
- **Conexao com discovery**: Toda decisao estrategica deve ser rastreavel a um insight

## Examples

### Exemplo 1 — Estrategia para Redesign de Checkout
**Hipotese**: Simplificar checkout de 5 passos para 2 aumentara conversao em 20%
porque pesquisa mostrou que usuarios abandonam por fadiga de formulario.

**Trade-offs**: Privilegiamos velocidade de conclusao sobre coleta de dados de marketing.
Campos opcionais serao removidos do checkout e movidos para pos-compra.

**Metricas**: Conversao de 3.2% para 3.8% (+20%) em 8 semanas. Guardrail: ticket
medio nao cai mais que 5%.

**Plano**: Sprint 1-2 wireframes + teste, Sprint 3-4 UI + dev, Sprint 5 lancamento.

### Exemplo 2 — Trade-off Matrix
| Decisao        | Privilegiamos          | Sacrificamos           |
|----------------|------------------------|------------------------|
| V1 Scope       | Core features          | Nice-to-haves          |
| Platform       | Mobile-first           | Desktop feature parity |
| Componentes    | Flexibilidade          | Consistencia estrita   |
| Timeline       | Rapido em producao     | Polish visual          |

### Exemplo 3 — Hipoteses em Cascata
Hipotese primaria invalidada: "onboarding mais curto melhora retention."
Teste mostrou que retention nao mudou. Hipotese secundaria ativada:
"Onboarding com quick win (primeira acao de valor) melhora retention."
A estrategia pivotou de "menos steps" para "steps mais significativos".

## Common Pitfalls

- **Estrategia sem discovery**: Hipoteses sem pesquisa sao adivinhacao
- **Trade-offs implicitos**: Nao explicitar trade-offs gera desalinhamento quando conflitos surgem
- **Metricas de vanidade**: Pageviews nao medem sucesso de UX. Escolha metricas de impacto
- **Plano rigido**: Estrategia que nao muda com novos aprendizados e dogma
- **Excesso de hipoteses**: Testar 10 coisas ao mesmo tempo nao testa nenhuma. Foque em 2-3
- **Desconexao produto-design**: Estrategia de design que conflita com produto gera paralisia
- **Nao revisitar**: Estrategia definida em janeiro e nunca revisada esta obsoleta em marco

## Cross-References

- [discovery-layer.md](discovery-layer.md) — Discovery como input estrategico
- [ux-layer.md](ux-layer.md) — Execucao da estrategia em UX
- [measurement-layer.md](measurement-layer.md) — Instrumentacao de metricas
- [malouf-ux-strategy-framework.md](malouf-ux-strategy-framework.md) — Framework completo de estrategia
- [mall-1000-dollar-exercise.md](mall-1000-dollar-exercise.md) — Priorizacao de investimento
- [mall-selling-design-to-stakeholders.md](mall-selling-design-to-stakeholders.md) — Comunicar estrategia
