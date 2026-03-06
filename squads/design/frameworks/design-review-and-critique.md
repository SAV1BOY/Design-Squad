# Design Review and Critique

## Metadata

| Campo         | Valor                                         |
| ------------- | --------------------------------------------- |
| Categoria     | Process                                       |
| Complexidade  | Media                                         |
| Autor         | Design Squad                                  |
| Versao        | 1.0                                           |
| Ultima revisao| 2026-03-06                                    |
| Tags          | critique, review, ritual, decision, feedback  |

## Concept

Design review and critique e um ritual estruturado para avaliar decisoes de design, gerar
feedback acionavel e documentar aprendizados. Diferente de uma opiniao casual, a critique segue
um formato que separa observacao de julgamento, foca nos objetivos do projeto e produz
decisoes claras.

### Diferenca entre Review e Critique

- **Review**: avaliacao formal de deliverable contra criterios objetivos (checklist, specs,
  guidelines). Resultado: aprovado, aprovado com ajustes, ou reprovado.
- **Critique**: exploracao colaborativa de alternativas e trade-offs. Resultado: insights,
  direcoes e decisoes de design.

Ambos sao necessarios em momentos diferentes do processo.

### Anatomia de uma Critique Session

```
1. Contexto     (5 min)  — Apresentador explica problema, restricoes e objetivos
2. Apresentacao (10 min) — Walk-through do design sem interrupcoes
3. Perguntas    (5 min)  — Clarificacao, nao julgamento
4. Feedback     (20 min) — Observacoes estruturadas dos participantes
5. Sintese      (5 min)  — Facilitador resume decisoes e proximos passos
6. Registro     (5 min)  — Documentacao formal no repositorio de decisoes
```

## When to Use

- **Critique semanal**: ritual recorrente para trabalho em andamento (WIP).
- **Review de milestone**: antes de handoff para engenharia.
- **Review de design system**: antes de adicionar ou alterar componentes.
- **Post-launch review**: apos lancamento, analisando metricas vs expectativas.
- Quando ha divergencia no time sobre a direcao de design.
- Quando um designer precisa de perspectiva externa.

## How to Apply

### 1. Preparacao (antes da sessao)

- **Apresentador**: compartilhar contexto antecipadamente (brief, user stories, restricoes).
- **Facilitador**: definir escopo e tipo de feedback desejado.
- **Participantes**: revisar material compartilhado previamente.
- **Setup**: tela compartilhada, Figma/FigJam pronto, documento de registro aberto.

### 2. Framework de Feedback Estruturado

Usar o modelo **I Like / I Wish / What If**:

| Tipo       | Proposito                              | Exemplo                                     |
| ---------- | -------------------------------------- | ------------------------------------------- |
| I Like     | Reforcar o que funciona                | "Gosto da hierarquia visual do dashboard"   |
| I Wish     | Apontar preocupacoes                   | "Gostaria de mais contraste no CTA"         |
| What If    | Sugerir alternativas                   | "E se usassemos um stepper em vez de tabs?" |

### 3. Niveis de Feedback

Classificar cada feedback por impacto para priorizar acoes:

```
P1 — Bloqueante:    impede o lancamento (acessibilidade, usabilidade critica)
P2 — Importante:    deve ser resolvido antes do handoff
P3 — Nice-to-have:  melhoria para iteracao futura
P4 — Divergencia:   opiniao pessoal sem consenso — registrar e seguir
```

### 4. Tomada de Decisao

Quando ha divergencia, usar o framework de decisao:

```
1. O designer owner tem a decisao final dentro do escopo do projeto.
2. O design lead arbitra quando afeta design system ou padrao cross-product.
3. Divergencias registradas para reavaliacao futura com dados.
4. "Disagree and commit" — apos decisao, todos alinham.
```

### 5. Registro de Decisoes

Cada sessao produz um registro com:

```markdown
## Design Decision Record — [Data]

**Projeto:** [Nome]
**Participantes:** [Lista]
**Decisao:** [Resumo da decisao tomada]
**Contexto:** [Por que essa decisao foi tomada]
**Alternativas descartadas:** [O que foi considerado]
**Proximos passos:** [Acoes com owners e deadlines]
**Status:** [Decidido / Em aberto / Revisitar em X]
```

## Key Principles

- **Separar observacao de julgamento**: descrever antes de avaliar.
- **Focar no problema, nao na pessoa**: "O contraste esta baixo" vs "Voce errou o contraste".
- **Feedback especifico e acionavel**: "Aumentar contraste do texto para 4.5:1" vs "Melhorar o visual".
- **Escopo claro**: definir que tipo de feedback e desejado antes de comecar.
- **Tempo protegido**: critique funciona com timeboxing rigoroso.
- **Seguranca psicologica**: ambiente onde errar e parte do processo.
- **Documentar, sempre**: decisoes nao registradas sao decisoes perdidas.

## Examples

### Critique Semanal (60 min)

```
Agenda:
  00-05  Check-in e agenda
  05-25  Critique 1: redesign da pagina de settings (designer A)
  25-45  Critique 2: novo componente de filtro (designer B)
  45-55  Critique 3: exploracao de onboarding (designer C)
  55-60  Wrap-up e registro de decisoes
```

### Review de Handoff (Checklist)

```
[ ] Design segue o design system (tokens, componentes, spacing)
[ ] Todos os estados projetados (default, hover, active, focus, disabled, error, loading, empty)
[ ] Responsividade definida para xs, md, lg
[ ] Acessibilidade verificada (contraste, focus, alt text, reading order)
[ ] Microcopy revisado com content designer
[ ] Specs e redlines documentados
[ ] Prototipo de interacao disponivel
[ ] Edge cases documentados
```

### Decision Record Exemplo

```
Projeto: Checkout redesign
Decisao: Usar stepper com 3 etapas em vez de single-page
Contexto: Taxa de abandono de 42% no formulario single-page
Alternativas: Accordion (descartado por complexidade mobile),
              tabs (descartado por falta de senso de progresso)
Proximos passos: Designer A prototipa stepper ate sexta-feira
```

## Common Pitfalls

| Erro                               | Consequencia                         | Correcao                                |
| ---------------------------------- | ------------------------------------ | --------------------------------------- |
| Critique sem escopo definido       | Feedback disperso e improdutivo      | Definir perguntas especificas antes     |
| Opiniao pessoal travestida de regra| Decisoes arbitrarias                 | Embasar em principios e dados           |
| Nao documentar decisoes            | Mesmas discussoes se repetem         | Registro obrigatorio apos cada sessao   |
| Feedback vago ("nao gostei")       | Designer sem direcao                 | Exigir estrutura I Like / I Wish        |
| Hierarquia dominando a conversa    | Juniors nao falam                    | Facilitador garante rotacao de fala     |
| Critique como gatekeeping          | Designers evitam mostrar WIP         | Reforcar que critique e para crescimento|

## Cross-References

- [Design System Governance](./design-system-governance.md) — review como parte do RFC process.
- [Lean UX Framework](./lean-ux-framework.md) — critique alinhada a ciclos de aprendizado.
- [Sprint Design Framework](./sprint-design-framework.md) — critique dentro do design sprint.
- [Design Maturity Model](./design-maturity-model.md) — rituais como indicador de maturidade.
- [SUS System Usability Scale](./sus-system-usability-scale.md) — dados de usabilidade na critique.
