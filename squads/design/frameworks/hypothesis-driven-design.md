# Hypothesis-Driven Design

## Metadata

- **Origem:** Lean Startup (Eric Ries) + Scientific Method aplicado a design
- **Categoria:** Validation Framework
- **Complexidade:** Intermediaria
- **Aplicacao:** Validacao de decisoes de design, experimentacao, reducao de risco
- **Tags:** hypothesis, experiment, learning, validation, lean, evidence-based

## Concept

Hypothesis-Driven Design e uma abordagem que aplica o metodo cientifico ao processo de
design. Em vez de tomar decisoes baseadas em intuicao ou autoridade, a equipe formula
hipoteses explicitas sobre o comportamento dos usuarios, projeta experimentos para
testa-las e usa os resultados para tomar decisoes informadas. O ciclo fundamental e:
Hipotese, Experimento, Aprendizado.

Cada decisao de design carrega suposicoes implicitas. "Adicionar onboarding guiado vai
melhorar a retencao" e uma suposicao disfarçada de decisao. Hypothesis-Driven Design
exige que essas suposicoes sejam explicitadas e testadas antes de se investir em
implementacao completa. Isso reduz dramaticamente o risco de construir features que
ninguem precisa ou usa.

O framework nao elimina a criatividade ou a intuicao de design — ele as complementa
com rigor. Intuicao gera hipoteses. Dados validam ou invalidam. A combinacao de intuicao
criativa e validacao empirica produz resultados superiores a qualquer um dos dois
abordados isoladamente.

## When to Use

- Antes de investir recursos significativos em implementacao de features ou redesigns
- Quando ha desacordo na equipe sobre qual abordagem seguir — dados resolvem debates
- Para priorizar ideias com base em evidencias ao inves de opiniao ou hierarquia
- Em ambientes de alta incerteza onde o custo de errar e significativo
- Para construir cultura de experimentacao e aprendizado continuo na equipe

## How to Apply

1. **Identifique suposicoes criticas:** Liste todas as suposicoes implicitas na decisao de
   design. Priorize pela combinacao de risco (o que acontece se estiver errada) e incerteza
   (quao confiante estamos). Suposicoes de alto risco e alta incerteza devem ser testadas
   primeiro, antes de qualquer outra.

2. **Formule hipoteses estruturadas:** Use o formato: "Acreditamos que [acao/mudanca] para
   [usuario-alvo] vai resultar em [resultado esperado]. Saberemos que isso e verdade quando
   [metrica] [atingir valor/mudar em X%]."

3. **Projete o experimento minimo:** Determine o metodo de teste mais rapido e barato que
   pode validar ou invalidar a hipotese. Opcoes incluem: testes A/B, prototipos de baixa
   fidelidade, fake door tests, Wizard of Oz, surveys, entrevistas de usabilidade.

4. **Defina criterios de sucesso antecipadamente:** Antes de rodar o experimento, defina
   exatamente o que constitui validacao ou invalidacao. "Melhoria na retencao" e vago.
   "Aumento de 10% na retencao D7 com significancia estatistica p < 0.05" e mensuravel
   e inequivoco.

5. **Execute e colete dados:** Rode o experimento com disciplina. Nao mude variaveis no
   meio do teste. Garanta amostra suficiente para significancia estatistica (em testes
   quantitativos) ou saturacao (em testes qualitativos).

6. **Analise e decida:** Compare resultados contra os criterios pre-definidos. Documente o
   aprendizado independente do resultado. Hipoteses invalidadas sao tao valiosas quanto
   validadas — ambas geram aprendizado que informa o proximo ciclo.

7. **Itere ou pivote:** Use o aprendizado para informar o proximo ciclo. Hipotese validada:
   implemente com confianca. Hipotese invalidada: reformule a hipotese, tente abordagem
   diferente, ou abandone a ideia e mude de direcao.

## Key Principles

- **Explicitar suposicoes:** Toda decisao de design carrega suposicoes. Torna-las explicitas
  e o primeiro passo para reduzir risco. Se a equipe nao consegue articular a suposicao
  por tras de uma decisao, a decisao nao esta madura.

- **Menor experimento viavel:** O objetivo e aprender o maximo possivel com o menor
  investimento possivel. Um prototipo em papel testado com 5 usuarios pode invalidar
  uma ideia que custaria meses de desenvolvimento.

- **Criterios antes dos dados:** Definir o que constitui sucesso antes de ver os resultados
  previne vieses de confirmacao. Se o criterio e definido depois, a equipe inconscientemente
  ajusta para validar sua preferencia.

- **Falhar e aprender, nao falhar e desperdicar:** O valor do framework esta no aprendizado.
  Cada experimento, independente do resultado, deve gerar insight documentado que informa
  decisoes futuras da equipe.

- **Velocidade sobre perfeicao:** Um experimento imperfeito rodado em uma semana gera mais
  valor que um experimento perfeito planejado por tres meses. Bias toward action com
  rigor suficiente, nao rigor paralisante.

## Examples

### Redesign de Checkout
Hipotese: "Acreditamos que reduzir o checkout de 4 etapas para 1 pagina unica vai
aumentar a taxa de conversao em 15% para usuarios mobile." Experimento: prototipo
interativo testado com 200 usuarios via teste A/B remoto. Resultado: conversao aumentou
8% mas erros de preenchimento subiram 25%. Aprendizado: o problema nao era o numero de
etapas, mas a falta de feedback em tempo real nos campos de formulario.

### Feature de Compartilhamento Social
Hipotese: "Acreditamos que adicionar compartilhamento social vai aumentar a aquisicao
organica em 20%." Experimento: fake door test — botao de compartilhamento adicionado sem
funcionalidade completa, medindo apenas cliques de intencao. Resultado: menos de 2% dos
usuarios clicaram. Aprendizado: compartilhamento social nao era uma necessidade real dos
usuarios. A equipe economizou 6 semanas de desenvolvimento.

### Sistema de Notificacoes Personalizadas
Hipotese: "Acreditamos que notificacoes personalizadas baseadas em comportamento vao
aumentar re-engajamento D7 em 12%." Experimento: Wizard of Oz — notificacoes enviadas
manualmente simulando algoritmo, para 500 usuarios durante 2 semanas. Resultado:
re-engajamento subiu 18%. A equipe validou o conceito antes de investir em infraestrutura
de machine learning.

## Common Pitfalls

- **Hipoteses vagas:** "Acreditamos que a mudanca vai melhorar a experiencia" nao e testavel.
  Especifique usuario, acao, resultado e metrica. Se nao da para medir, nao e hipotese
  — e desejo ou opiniao.

- **Vies de confirmacao:** A equipe inconscientemente interpreta dados ambiguos como
  validacao. Mitigue definindo criterios de sucesso antes do experimento e envolvendo
  pessoas sem apego emocional a hipotese na analise dos resultados.

- **Testar tudo, decidir nada:** Experimentacao excessiva sem acao gera paralisia. Nem toda
  decisao precisa de teste formal. Reserve experimentos para suposicoes de alto risco.
  Decisoes de baixo risco podem ser tomadas com base em heuristicas e experiencia.

- **Amostra insuficiente:** Tomar decisoes com base em 10 respostas de survey ou 3 dias de
  teste A/B gera conclusoes estatisticamente invalidas. Calcule sample size adequado antes
  de rodar o experimento para ter confianca nos resultados.

## Cross-References

- [Problem Statement Template](problem-statement-template.md) — Problem statements se
  desdobram em hipoteses testaveis e estruturadas
- [HEART Metrics Framework](heart-metrics-framework.md) — Fornece metricas estruturadas
  para definir criterios de sucesso de experimentos
- [North Star and Success Metrics](north-star-and-success-metrics.md) — Metricas de sucesso
  orientam quais hipoteses sao prioritarias para testar
- [Design Thinking](design-thinking.md) — Hypothesis-Driven Design adiciona rigor cientifico
  a fase de Test do processo
- [Double Diamond](double-diamond.md) — Experimentos sao centrais na fase Develop/Deliver
  do segundo diamante
