# Snapchat Redesign 2018 — Reação dos Usuários

> Arquivo de lições aprendidas · Design Squad

---

## Context / Contexto

Em fevereiro de 2018, o Snapchat lançou um redesign completo do app que
reorganizou fundamentalmente a navegação. O objetivo declarado era separar
conteúdo social (amigos) de conteúdo de mídia (publishers/Discover), mas
a execução gerou uma das maiores revoltas de usuários na história de apps.

A petition on Change.org to revert the redesign gathered over 1.2 million
signatures. Celebrity backlash (notably Kylie Jenner's tweet) wiped an
estimated $1.3 billion from Snap's market value. The company eventually
rolled back several changes, but the damage to user trust and growth
trajectory was already done.

## What Went Wrong / O Que Deu Errado

### 1. Reorganização Total da Arquitetura de Informação
- Friends e Stories foram movidos para a mesma aba (esquerda), misturando
  conversas com stories de amigos em um feed algorítmico.
- A seção Discover (direita) passou a mostrar conteúdo de publishers e
  influencers, separando criadores de seus amigos.
- Usuários não conseguiam mais encontrar stories de amigos facilmente.

### 2. Algoritmo sobre Cronologia
- O feed de amigos passou a ser ordenado algoritmicamente em vez de
  cronologicamente, quebrando a previsibilidade.
- Usuários perderam o senso de "o que é novo" e "o que já vi".
- A ordenação algorítmica beneficiava power users e prejudicava criadores
  menores dentro dos círculos sociais.

### 3. Teste Insuficiente com a Base Real
- O redesign foi testado com uma amostra limitada que não representava
  a diversidade da base de usuários (predominantemente Gen Z).
- Feedback negativo durante beta foi subestimado como "resistência natural
  a mudanças" em vez de sinal de problema real.

### 4. Rollout Big-Bang
- A mudança foi lançada para toda a base de uma vez, sem rollout gradual.
- Não havia opção de voltar ao layout anterior (no opt-out).
- O volume de reclamações simultâneas sobrecarregou o suporte e amplificou
  o sentimento negativo nas redes sociais.

### 5. Desrespeito ao Modelo Mental Estabelecido
- O Snapchat construiu hábitos fortes: swipe right = chat, swipe left =
  stories/discover. O redesign inverteu e misturou essas associações.
- Muscle memory de milhões de usuários foi invalidada de uma vez.

## Design Lessons / Lições de Design

1. **Arquitetura de informação é contrato com o usuário** — Reorganizar IA
   é equivalente a mudar as ruas de uma cidade. Requer planejamento e
   sinalização extensivos.

2. **Cronologia tem valor de UX** — Feeds algorítmicos podem otimizar
   engagement metrics mas destroem a sensação de controle do usuário.

3. **Teste com a base real, não amostras convenientes** — Especialmente
   para produtos com base jovem, testes devem incluir heavy users reais.

4. **Gradual rollout é obrigatório para mudanças estruturais** — Feature
   flags, A/B testing em percentuais pequenos, e opt-out temporário.

5. **Social proof amplifica negatividade** — Em produtos sociais, um
   usuário insatisfeito recruta outros. A velocidade de contágio é brutal.

6. **Separar friends de media pode fazer sentido estratégico mas não
   para o usuário** — Business logic ≠ user mental model.

## How to Avoid / Como Evitar

- [ ] Mapear jornadas existentes antes de redesign e medir disruption score
- [ ] Implementar gradual rollout com métricas de canary (retention, session
      time, NPS) monitoradas em tempo real
- [ ] Oferecer período de transição com opção de layout anterior
- [ ] Testar com no mínimo 5% da base real antes de rollout completo
- [ ] Preparar plano de rollback antes do lançamento
- [ ] Monitorar social sentiment em tempo real durante rollout
- [ ] Validar que a nova IA corresponde ao modelo mental do usuário via
      card sorting e tree testing

## Cross-References / Referências Cruzadas

- `./redesign-disasters.md` — Catálogo geral de redesigns problemáticos
- `../../lib/patterns/confirmation-patterns.md` — Padrões de confirmação
- `../../data/research/usability-tests/.gitkeep` — Repositório de testes
- `../../lib/patterns/onboarding-patterns.md` — Re-onboarding pós-redesign
- `../../data/registries/lessons-learned-registry.yaml` — Registro de lições
- `../../data/registries/experiments-registry.yaml` — Registro de experimentos
