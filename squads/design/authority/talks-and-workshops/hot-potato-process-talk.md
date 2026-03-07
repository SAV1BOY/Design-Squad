# Hot Potato Process Talk — Dan Mall

## Speaker

**Dan Mall** e fundador e CEO da SuperFriendly, uma design collaborative que ajuda
organizacoes a construir e escalar times de design de alta performance. Ele e autor de
"Design That Scales" (2023) e um dos profissionais mais influentes na intersecao entre
design systems, processos de design e colaboracao design-engineering.

Dan e ex-diretor de design da Big Spaceship, e ja trabalhou com clientes como Google,
Entertainment Weekly, TechCrunch, Rolling Stone e Time Inc. Ele e tambem co-host do
podcast "Design System University" e professor no programa de MFA da School of Visual
Arts em Nova York.

**Credenciais relevantes:**
- Autor de "Design That Scales" (A Book Apart, 2023)
- Fundador da SuperFriendly (superfriendly.com)
- Co-criador do conceito "Hot Potato Process"
- Speaker em conferencias como An Event Apart, Smashing Conference, Design Systems Conference
- Consultor de design systems para organizacoes Fortune 500

## Topic

### The Hot Potato Process: Reimaginando a Colaboracao Design-Engineering

A talk de Dan Mall desafia fundamentalmente o modelo linear tradicional de design e
desenvolvimento, onde designers completam seu trabalho e entao "entregam" (handoff) para
engenheiros. Em vez disso, Dan propoe o "Hot Potato Process" — um modelo de colaboracao
onde o trabalho passa continuamente entre Design e Engineering, como uma batata quente
que ninguem segura por muito tempo.

A metafora e simples mas poderosa: em vez de Design trabalhar isoladamente por semanas
e depois fazer um handoff formal para Engineering, o trabalho vai e volta entre as
disciplinas em ciclos rapidos, com cada lado adicionando valor incrementalmente.

### O Problema do Modelo Linear

O modelo tradicional (waterfall de design) apresenta problemas fundamentais:

```
Tradicional:  Research → Design → Handoff → Development → QA → Launch
              [semanas]  [semanas]  [dias]    [semanas]   [dias]

Hot Potato:   Design ↔ Dev ↔ Design ↔ Dev ↔ Design ↔ Dev → Launch
              [horas]  [horas] [horas] [horas] [horas] [horas]
```

No modelo tradicional:
- Designers projetam sem entender limitacoes tecnicas reais
- Engenheiros implementam sem entender a intencao do design
- O handoff e um ponto de falha onde informacao se perde
- Feedback loops sao longos e custosos
- Rework e frequente porque decisoes sao tomadas em isolamento

## Key Takeaways

### 1. Fidelity as a Spectrum (Fidelidade como Espectro)

Dan propoe que fidelidade nao e binaria (low-fi vs. high-fi) mas um espectro continuo:

| Nivel | Design | Engineering |
|-------|--------|-------------|
| 1 | Sketch em papel | Pseudocodigo / wireframe HTML |
| 2 | Wireframe digital | HTML/CSS basico com dados mockados |
| 3 | Mockup visual | Componentes funcionais com styling basico |
| 4 | Prototipo interativo | Feature funcional com design refinado |
| 5 | Design final polished | Producao com QA visual completo |

A chave e que Design e Engineering trabalham em paralelo, incrementando a fidelidade
juntos, em vez de Design atingir nivel 5 antes de Engineering comecar no nivel 1.

### 2. O Ciclo do Hot Potato

O processo funciona em ciclos rapidos (idealmente de horas, nao dias):

**Ciclo 1 — Framing:**
- Designer cria sketch basico do conceito (15-30 min)
- Engenheiro avalia feasibility e propoe alternativas (15-30 min)
- Juntos definem a abordagem tecnica e de design

**Ciclo 2 — Structure:**
- Designer refina o wireframe com feedback tecnico (1-2h)
- Engenheiro comeca a implementar estrutura basica (1-2h)
- Review conjunto para alinhar direcao

**Ciclo 3 — Styling:**
- Designer aplica visual design no wireframe (2-4h)
- Engenheiro implementa design tokens e componentes (2-4h)
- Review conjunto com comparacao lado a lado

**Ciclo 4 — Interaction:**
- Designer define microinteracoes e transicoes (1-2h)
- Engenheiro implementa motion e interatividade (2-4h)
- Teste conjunto em dispositivo real

**Ciclo 5 — Polish:**
- Designer faz QA visual detalhado no browser (1-2h)
- Engenheiro ajusta detalhes baseado no feedback (1-2h)
- Aprovacao conjunta para producao

### 3. Prerequisites para o Hot Potato Funcionar

Dan e honesto sobre os pre-requisitos:

**Design System como Fundacao:**
- Sem um design system compartilhado, o hot potato gera mais caos do que valor
- Componentes compartilhados criam a "lingua comum" necessaria
- Design tokens garantem que Design e Engineering falam da mesma cor, fonte, espacamento

**Ferramentas Compartilhadas:**
- Designers precisam ter acesso basico ao ambiente de desenvolvimento (staging, preview)
- Engenheiros precisam ter acesso basico ao ambiente de design (Figma view)
- Ferramentas de comunicacao rapida (Slack, pair programming tools)

**Cultura de Confianca e Proximidade:**
- Ambos os lados precisam confiar um no outro e estar confortaveis mostrando trabalho incompleto
- Em ambientes remotos, requer sessoes regulares de pair design/development

### 4. Design Systems Aceleram o Hot Potato

Dan conecta o hot potato process diretamente a design systems:

- **Componentes compartilhados** eliminam a necessidade de especificar detalhes visuais basicos
- **Design tokens** criam a ponte entre o Figma e o codigo
- **Documentacao de componentes** serve como contrato entre Design e Engineering
- **Storybook/equivalente** permite que designers vejam componentes reais em isolamento
- O design system e o "vocabulario compartilhado" que torna o hot potato possivel

### 5. Measuring Collaboration Quality

Dan propoe metricas para avaliar a qualidade da colaboracao:

| Metrica | O que Mede | Target |
|---------|-----------|--------|
| Handoff Iterations | Numero de idas e vindas no "handoff" tradicional | 0 (eliminado) |
| Design-to-Browser Time | Tempo do primeiro conceito ate ver no browser | < 1 dia |
| Visual QA Issues | Discrepancias entre design e implementacao | < 5 por feature |
| Rework Rate | % de trabalho que precisa ser refeito | < 5% |
| Joint Session Frequency | Frequencia de sessoes colaborativas Design+Eng | > 3x/semana |
| Satisfaction Score | Satisfacao mutua de designers e engenheiros | > 8/10 |

### 6. Scaling Hot Potato

Para times maiores, Dan sugere adaptacoes:

- **Pair Rotation** — Designers e engenheiros formam pares que rotacionam a cada projeto
- **Design System as Buffer** — O design system absorve a necessidade de especificacao detalhada
- **Async Hot Potato** — Para times distribuidos, usar PRs de design e code reviews conjuntos
- **Hot Potato Sprints** — Dedicar sprints especificos para trabalho colaborativo intensivo

## Application

### Implementando Hot Potato na MMOS

**Fase 1 — Piloto (1 sprint)**
- Selecionar 1 feature de complexidade media
- Formar 1 par designer-engenheiro para experimentar o processo
- Documentar o fluxo, os desafios e os resultados
- Comparar metricas (tempo, qualidade, satisfacao) com o processo tradicional

**Fase 2 — Expansao (2-3 sprints)**
- Aplicar em 2-3 features com pares diferentes
- Refinar o processo baseado nos aprendizados do piloto
- Estabelecer cadencia de pair sessions (3x/semana, 2h cada)
- Integrar feedback no processo de design critique

**Fase 3 — Padronizacao (ongoing)**
- Hot potato como processo padrao para features com complexidade de UI
- Documentar best practices e anti-patterns especificos para a MMOS
- Treinar novos membros do time no processo
- Medir e otimizar continuamente

### Rituais de Suporte

- **Daily Design-Eng Sync (15 min)** — Alinhamento rapido, bloqueios e dependencias
- **Weekly Pair Review (1h)** — Demo no browser, feedback visual e funcional em tempo real
- **Sprint Retro Item** — Item fixo sobre qualidade da colaboracao Design-Eng

## Resources

### Leitura Essencial
- **"Design That Scales"** por Dan Mall (A Book Apart, 2023)
- **"Hot Potato Process"** — danmall.com/hot-potato-process/
- **SuperFriendly Blog** — superfriendly.com/blog/
- **"The Handoff Myth"** — Dan Mall article on design-engineering collaboration

### Videos, Ferramentas e Workshops
- "Hot Potato Process" — Dan Mall @ An Event Apart (YouTube)
- "Design That Scales" — Dan Mall @ Figma Config
- **Figma Dev Mode** + **Storybook** + **Tuple/Pop** para pair sessions remotas
- Dan Mall oferece workshops customizados (2 dias, hands-on, projetos reais)

---

**Referencia original:** danmall.com, "Design That Scales" (A Book Apart, 2023)
**Ultima atualizacao:** Marco 2026
**Responsavel:** Design Squad — MMOS
