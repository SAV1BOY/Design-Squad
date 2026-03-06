# Malouf Design Quality Model

## Metadata
- **Autor**: Dave Malouf
- **Categoria**: Qualidade, Avaliacao de Design
- **Complexidade**: Media
- **Aplicacao**: Definir e medir qualidade de design de forma objetiva e compartilhada
- **Ultima atualizacao**: 2026-03-06

## Concept

O Design Quality Model de Dave Malouf propoe que qualidade de design nao e subjetiva
nem intangivel — pode e deve ser definida por criterios explicitos e avaliada por
rubricas estruturadas. O modelo estabelece dimensoes de qualidade, niveis de maturidade
para cada dimensao e processos de avaliacao que tornam feedback objetivo e acionavel.

A falta de criterios explicitos de qualidade leva a dois problemas: reviews subjetivos
onde "gostei" ou "nao gostei" sao os unicos feedbacks, e inconsistencia de padrao onde
diferentes reviewers avaliam com criterios diferentes.

O modelo cria uma linguagem compartilhada de qualidade que permite self-assessment,
peer review e avaliacao de lideranca com o mesmo vocabulario e os mesmos criterios.

## When to Use

- Quando design reviews sao subjetivos e inconsistentes
- Quando novos designers nao entendem o que "bom design" significa na organizacao
- Quando a equipe quer elevar o padrao de qualidade sistematicamente
- Quando se precisa de criterios de avaliacao para hiring e performance reviews
- Quando stakeholders questionam a qualidade do output de design
- Quando ha desalinhamento sobre o que "done" significa para um deliverable de design

## How to Apply

### Passo 1 — Defina Dimensoes de Qualidade
Selecione 5-7 dimensoes relevantes para seu contexto. Sugestoes:

1. **Usabilidade**: O design e facil de usar, aprender e eficiente para tarefas
2. **Acessibilidade**: O design funciona para pessoas com diferentes habilidades
3. **Consistencia**: O design segue patterns e guidelines do design system
4. **Clareza**: A hierarquia de informacao e comunicacao sao claras e inequivocas
5. **Completude**: Todos os estados, edge cases e cenarios estao cobertos
6. **Viabilidade**: O design e implementavel dentro das restricoes tecnicas
7. **Alinhamento estrategico**: O design avanca objetivos de negocio e usuario

### Passo 2 — Crie Rubricas por Dimensao
Para cada dimensao, defina 4 niveis (1-4):

**Exemplo — Completude**:
- **Nivel 1 (Insuficiente)**: Apenas happy path coberto. Sem estados de erro, loading ou empty
- **Nivel 2 (Basico)**: Happy path + principais estados de erro. Faltam edge cases
- **Nivel 3 (Bom)**: Todos os estados cobertos. Edge cases documentados. Responsivo
- **Nivel 4 (Excelente)**: Todos os estados + edge cases + micro-interactions + a11y
  annotations + specs completas para dev

### Passo 3 — Calibre com a Equipe
1. Selecione 3-5 exemplos de trabalho passado da equipe
2. Peca que cada pessoa avalie usando a rubrica individualmente
3. Compare resultados e discuta divergencias
4. Ajuste descricoes dos niveis ate haver consenso
5. Repita a calibracao trimestralmente com exemplos novos

### Passo 4 — Integre no Workflow
1. **Self-assessment**: Designer avalia o proprio trabalho antes de submeter para review
2. **Peer review**: Reviewer usa a rubrica como guia de avaliacao
3. **Critique sessions**: Use as dimensoes como lens de feedback
4. **Definition of Done**: Nivel minimo aceitavel definido por dimensao
5. **Retrospectivas**: Analise quais dimensoes estao consistentemente abaixo do esperado

### Passo 5 — Evolua o Modelo
1. Revise as dimensoes anualmente — estao ainda relevantes?
2. Atualize rubricas conforme o padrao da equipe evolui
3. Adicione exemplos de "benchmark" para cada nivel
4. Conecte resultados a planos de desenvolvimento individual
5. Use dados agregados para identificar gaps sistematicos de qualidade

## Key Principles

- **Qualidade e definivel**: O que nao e definido nao pode ser medido nem melhorado
- **Criterios compartilhados**: Todos avaliam com os mesmos criterios
- **Niveis incrementais**: Qualidade nao e binario (bom/ruim) — e um espectro
- **Calibracao continua**: Rubricas precisam ser calibradas regularmente
- **Self-assessment primeiro**: Designers devem ser capazes de avaliar o proprio trabalho
- **Feedback acionavel**: "Nivel 2 em completude porque faltam estados de erro" e
  infinitamente mais util que "precisa melhorar"
- **Contexto importa**: O nivel aceitavel pode variar por tipo de projeto

## Examples

### Exemplo 1 — Rubrica Completa
| Dimensao       | Nivel 1         | Nivel 2         | Nivel 3         | Nivel 4         |
|----------------|-----------------|-----------------|-----------------|-----------------|
| Usabilidade    | Fluxo confuso   | Fluxo funcional | Fluxo otimizado | Testado c/ users|
| Acessibilidade | Sem consideracao| Contraste ok    | WCAG AA         | WCAG AAA + SR   |
| Consistencia   | Ad-hoc          | Usa alguns tokens| Segue DS        | Contribui pro DS|
| Clareza        | Hierarquia pobre| Hierarquia ok   | Hierarquia clara| Copy otimizado  |
| Completude     | Happy path only | + estados erro  | + edge cases    | + micro-int     |
| Viabilidade    | Nao verificado  | Conversou c/ dev| Spec tecnica    | Prototipo c/ dev|

### Exemplo 2 — Self-Assessment em Acao
Um designer junior avaliou seu mockup de dashboard:
- Usabilidade: 3 (fluxo otimizado baseado em benchmark)
- Acessibilidade: 2 (contraste ok, falta keyboard nav)
- Consistencia: 3 (segue DS completamente)
- Completude: 2 (faltam empty states)
O self-assessment direcionou 2 horas adicionais de trabalho para fechar gaps
em acessibilidade e completude antes do review.

### Exemplo 3 — Gap Analysis de Equipe
Apos 3 meses usando a rubrica, um design lead agregou resultados:
- Media mais alta: Consistencia (3.4/4) — equipe segue bem o DS
- Media mais baixa: Acessibilidade (1.8/4) — gap sistematico
- Acao: Investimento em treinamento de a11y para toda a equipe,
  adocao de plugins de checagem automatica, e inclusao de a11y
  review como obrigatorio no Definition of Done

## Common Pitfalls

- **Rubrica como punicao**: Se usada punitivamente, gera medo e gaming. Use para
  desenvolvimento, nao para ranking
- **Dimensoes demais**: Mais de 7 dimensoes torna a avaliacao exaustiva. Foque nas
  mais relevantes
- **Niveis vagos**: "Design bom" vs "design otimo" nao e rubrica util. Seja especifico
  e concreto em cada nivel
- **Nao calibrar**: Sem calibracao, cada pessoa interpreta niveis de forma diferente
- **Aplicar uniformemente**: Um prototipo rapido nao precisa de nivel 4 em todas as
  dimensoes. Adapte ao contexto
- **Ignorar evolucao**: A rubrica que servia ha 1 ano pode nao refletir o padrao atual
- **Focar em output sobre outcome**: Qualidade de design inclui se o design resolveu
  o problema do usuario, nao so se ficou "bonito"

## Cross-References

- [malouf-designops-framework.md](malouf-designops-framework.md) — Qualidade como pilar operacional
- [malouf-research-to-decision.md](malouf-research-to-decision.md) — Evidencia como input de qualidade
- [mall-design-that-scales.md](mall-design-that-scales.md) — Qualidade em escala
- [governance-layer.md](governance-layer.md) — Quality gates no processo
- [measurement-layer.md](measurement-layer.md) — Metricas de qualidade
- [usability-testing-framework.md](usability-testing-framework.md) — Validacao de qualidade com usuarios
