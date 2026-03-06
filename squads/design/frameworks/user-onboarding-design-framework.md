# User Onboarding Design Framework

## Metadata
- squad: design
- category: application-specific
- version: 1.0.0

## Concept

O User Onboarding Design Framework e uma abordagem sistematica para projetar a experiencia de primeiro uso de um produto digital. O onboarding nao e apenas um "tutorial" — e o processo pelo qual o usuario descobre valor, atinge o "Aha Moment" e forma o habito de uso.

O framework cobre desde o first-run experience (primeira abertura) ate a ativacao completa (usuario atingiu o valor core). Baseia-se em conceitos de behavioral design (Nir Eyal - Hooked), progressive profiling, e reducao de friccao (Krug - Don't Make Me Think).

Um onboarding bem projetado reduz churn nos primeiros 7 dias, aumenta activation rate e acelera time-to-value. Um onboarding mal projetado gera abandono, confusao e suporte desnecessario.

## When to Use

- Ao projetar o first-run experience de um novo produto ou feature
- Ao redesenhar o onboarding existente (metricas de ativacao baixas)
- Ao adicionar nova funcionalidade complexa que requer orientacao
- Ao projetar upgrade flows (free -> paid, basic -> pro)
- Ao avaliar drop-off no funil de ativacao

## How to Apply

1. **Defina o "Aha Moment"** — Qual e o momento em que o usuario percebe o valor do produto?
2. **Mapeie o funil de ativacao** — Sign-up -> Setup -> First action -> Aha moment -> Habit formation
3. **Identifique friccoes** — Em cada etapa, o que pode causar abandono?
4. **Reduza steps ao minimo** — Cada step adicional perde ~20% dos usuarios
5. **Progressive profiling** — Colete informacoes ao longo do tempo, nao tudo no sign-up
6. **Guie sem bloquear** — Tooltips, empty states com CTAs, checklists de progresso
7. **Celebre marcos** — Feedback positivo ao completar setup, primeira acao
8. **Personalize quando possivel** — Pergunte o objetivo do usuario e adapte
9. **Meca e itere** — Funil de ativacao, time-to-value, completion rate por step

## Key Principles

1. **Value first, features later** — Mostre o valor antes de explicar features
2. **Do, don't show** — Usuarios aprendem fazendo, nao lendo
3. **Progressive disclosure** — Revele complexidade gradualmente
4. **Reduce friction ruthlessly** — Cada campo, step, decisao e ponto de abandono
5. **Empty states are onboarding** — O estado vazio e a primeira impressao
6. **Personalization increases activation** — Onboarding relevante ativa mais rapido

## Examples

### Exemplo 1: SaaS Dashboard
- **Aha Moment:** Usuario ve seu primeiro dashboard com dados reais
- **Funil:** Sign-up -> Conectar data source -> Ver dashboard -> Personalizar
- **Otimizacao:** Pre-popular com dados de exemplo antes de conectar data source

### Exemplo 2: E-commerce App
- **Aha Moment:** Usuario encontra produto relevante
- **Funil:** Download -> Browse -> First search -> Add to cart -> Purchase
- **Otimizacao:** Perguntar categorias de interesse, personalizar home

### Exemplo 3: Collaboration Tool
- **Aha Moment:** Usuario recebe resposta de colega
- **Funil:** Sign-up -> Invite team -> Create project -> First comment
- **Otimizacao:** Facilitar invite (link), pre-criar projeto de exemplo

## Common Pitfalls

1. **Tutorial overload** — 10 slides de "bem-vindo" que o usuario pula
2. **Feature tour sem contexto** — Explicar features antes do usuario precisar
3. **Sign-up form longo** — Pedir tudo upfront
4. **Ignorar empty states** — Tela vazia sem orientacao
5. **Nao medir funil** — Sem metricas, nao sabe onde usuarios abandonam

## Cross-References

- **Agents:** `ux-design-expert`, `jessica-ux-ui`, `design-chief`
- **Frameworks:** `progressive-disclosure.md`, `empty-states-and-loading-states.md`, `heart-metrics-framework.md`
- **Checklists:** `checklists/ux/ux-onboarding-quality.md`
- **Reference:** `reference/ui-patterns/onboarding-patterns.md`, `reference/psychology/habit-formation-design.md`
