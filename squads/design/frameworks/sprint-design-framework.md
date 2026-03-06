# Sprint Design Framework

## Metadata

| Campo         | Valor                                         |
| ------------- | --------------------------------------------- |
| Categoria     | Metodologia                                   |
| Complexidade  | Alta                                          |
| Autor         | Design Squad                                  |
| Versao        | 1.0                                           |
| Ultima revisao| 2026-03-06                                    |
| Tags          | design-sprint, google-ventures, prototype, test |

## Concept

O Design Sprint e um processo de 5 dias criado pela Google Ventures para responder questoes
criticas de negocio por meio de design, prototipacao e teste com usuarios. Comprime meses de
debate e desenvolvimento em uma semana intensiva e estruturada.

### Estrutura dos 5 Dias

```
Segunda:  Map      — Mapear o problema e escolher um foco
Terca:    Sketch   — Gerar solucoes individuais
Quarta:   Decide   — Escolher a melhor solucao e criar storyboard
Quinta:   Prototype— Construir prototipo de alta fidelidade
Sexta:    Test     — Testar com 5 usuarios reais
```

### Premissas Fundamentais

- **Time-boxed**: a restricao de tempo forca decisoes e elimina perfeccionismo.
- **Cross-functional**: participantes de design, produto, engenharia, negocios.
- **Facilitado**: um facilitador dedicado que nao participa do conteudo.
- **Baseado em evidencia**: a sexta-feira produz dados reais, nao opinioes.

## When to Use

- No inicio de um novo produto ou feature com alta incerteza.
- Quando o time esta preso em debate sem convergencia.
- Para validar uma direcao estrategica antes de investir em desenvolvimento.
- Quando ha uma deadline critica e o time precisa acelerar.
- Para alinhar stakeholders com visoes divergentes sobre a solucao.
- Quando uma feature existente tem metricas problematicas e precisa de redesign.

## How to Apply

### Segunda — Map

**Objetivo**: entender o problema e definir o foco do sprint.

1. **Long-term goal** (10 min): definir o objetivo de longo prazo do projeto.
2. **Sprint questions** (15 min): listar perguntas que o sprint deve responder.
3. **Map** (30 min): criar mapa simplificado da jornada do usuario.
4. **Expert interviews** (60 min): entrevistar stakeholders e especialistas.
5. **How Might We** (30 min): transformar insights em oportunidades (post-its).
6. **Target** (15 min): escolher um momento especifico do mapa para focar.

### Terca — Sketch

**Objetivo**: gerar solucoes diversas individualmente.

1. **Lightning demos** (40 min): cada participante mostra 3 referencias inspiradoras.
2. **4-part sketch**:
   - Notes (20 min): anotar ideias livremente.
   - Ideas (20 min): esbocar conceitos rapidos.
   - Crazy 8s (8 min): 8 variacoes em 8 minutos.
   - Solution sketch (45 min): esbocar uma solucao detalhada em 3 paineis.
3. Todos os sketches sao anonimos ate a votacao.

### Quarta — Decide

**Objetivo**: escolher a solucao e planejar o prototipo.

1. **Art museum** (10 min): fixar todos os sketches na parede.
2. **Heat map** (15 min): cada pessoa vota com dots nas partes que gosta.
3. **Speed critique** (30 min): facilitador narra cada sketch, time discute.
4. **Supervote** (5 min): decider (decisor final) escolhe com 3 votos.
5. **Storyboard** (60 min): criar storyboard detalhado do prototipo.

### Quinta — Prototype

**Objetivo**: construir prototipo testavel em um dia.

Principios:
- **Goldilocks quality**: realista o suficiente para gerar reacoes genuinas.
- **Fachada funcional**: parece real por fora, nao precisa funcionar por dentro.
- **Dividir e conquistar**: cada pessoa responsavel por uma parte.

```
Ferramentas recomendadas:
  UI:        Figma (prototipo interativo)
  Landing:   Webflow / Framer
  Dados:     Conteudo real, nunca lorem ipsum
  Review:    Trial run no final do dia com alguem de fora
```

### Sexta — Test

**Objetivo**: testar com 5 usuarios e aprender.

1. **Recrutar 5 participantes** que representem a persona target.
2. **Entrevista de 60 min cada**: introducao (5), tarefas (40), debrief (15).
3. **Observadores em sala separada**: time assiste ao vivo, anota em post-its.
4. **Sintese em tempo real**: apos cada entrevista, consolidar patterns.
5. **Resultado final**: padroes de comportamento, validacoes e invalidacoes.

## Key Principles

- **Juntos, sozinhos**: gerar ideias individualmente, decidir coletivamente.
- **Tangibilidade**: prototipar em vez de debater abstratamente.
- **Dados reais de usuarios**: a opiniao que importa e a do usuario.
- **Facilitacao rigorosa**: timeboxing e a alma do sprint.
- **Decisor presente**: alguem com autoridade para decidir deve participar.
- **Foco implacavel**: um problema, uma semana, uma resposta.

## Examples

### Sprint Questions

```
- "Os usuarios vao entender o modelo de pricing em menos de 30 segundos?"
- "Conseguimos guiar um novo usuario ate o primeiro valor em 5 minutos?"
- "O fluxo de checkout em 2 etapas reduz abandono comparado ao atual?"
```

### Storyboard — Checkout Redesign

```
Quadro 1: Usuario no carrinho com 3 itens
Quadro 2: Click em "Finalizar compra"
Quadro 3: Etapa 1 — Endereco (pre-preenchido se logado)
Quadro 4: Etapa 2 — Pagamento + resumo do pedido
Quadro 5: Confirmacao com tracking number
Quadro 6: Email de confirmacao na caixa de entrada
```

### Resultado da Sexta-Feira

```
5 usuarios testados:
  Patterns positivos (4/5 usuarios):
    - Entenderam o fluxo de 2 etapas sem ajuda
    - Elogiaram o pre-preenchimento de endereco
  Patterns negativos (3/5 usuarios):
    - Nao encontraram opcao de cupom de desconto
    - Esperavam ver prazo de entrega antes do pagamento
  Decisao: implementar com ajuste de cupom e prazo visivel
```

## Common Pitfalls

| Erro                               | Consequencia                        | Correcao                                |
| ---------------------------------- | ----------------------------------- | --------------------------------------- |
| Sem decisor presente               | Decisoes reabertas depois           | Exigir presenca do decisor              |
| Prototipo com lorem ipsum          | Reacoes nao-realistas nos testes    | Usar conteudo real sempre               |
| Pular a sexta-feira                | Sprint sem validacao = brainstorm   | Sexta e o dia mais importante           |
| Time muito grande (>7 pessoas)     | Discussoes improdutivas             | Limitar a 4-7 participantes             |
| Facilitador que opina              | Facilitar e participar sao conflito | Facilitador dedicado e neutro           |
| Nao recrutar usuarios com antecedencia | Sexta sem participantes         | Recrutar na semana anterior             |

## Cross-References

- [Lean UX Framework](./lean-ux-framework.md) — design sprint como formato intensivo de Lean UX.
- [Design Review and Critique](./design-review-and-critique.md) — critique integrada na quarta-feira.
- [SUS System Usability Scale](./sus-system-usability-scale.md) — SUS como metrica pos-sprint.
- [Content Design Microcopy](./content-design-microcopy.md) — microcopy real no prototipo.
- [Kano Model](./kano-model.md) — priorizar features antes do sprint.
