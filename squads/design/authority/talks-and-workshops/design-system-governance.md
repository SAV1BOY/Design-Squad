# Design System Governance Workshop

## Speaker

Este workshop reune insights de multiplos especialistas em design system governance,
incluindo Nathan Curtis (EightShapes), Jina Anne (Design Tokens Community Group Chair),
Dan Mall (SuperFriendly) e Amy Hupe (ex-GOV.UK Design System). O conteudo foi sintetizado
e adaptado a partir de talks, artigos e workshops destes profissionais.

**Perfis dos especialistas:**

- **Nathan Curtis** — Fundador da EightShapes, referencia mundial em design systems e autor
  de dezenas de artigos seminais sobre governance, contribution models e team structures
- **Jina Anne** — Criadora do conceito de Design Tokens, liderou design systems na Salesforce
  (Lightning) e ex-Senior Design Systems Advocate na Amazon
- **Dan Mall** — Fundador do SuperFriendly, especialista em hot potato process e design
  system adoption strategies
- **Amy Hupe** — Liderou o GOV.UK Design System, um dos design systems publicos mais
  reconhecidos do mundo

## Topic

### Governance de Design Systems: Modelos, Processos e Sustentabilidade

Governance e o aspecto mais subestimado e ao mesmo tempo mais critico para o sucesso de
um design system a longo prazo. Enquanto a maioria das organizacoes foca na construcao
de componentes, poucas investem adequadamente nos modelos de decisao, processos de
contribuicao e estruturas de responsabilidade que garantem a evolucao saudavel do sistema.

Este workshop aborda os tres pilares fundamentais da governance:

1. **Decision-Making** — Quem decide o que entra, sai e muda no design system?
2. **Contribution** — Como pessoas de fora do time core contribuem para o sistema?
3. **Communication** — Como mudancas sao comunicadas e adocao e promovida?

## Key Takeaways

### 1. Modelos de Governance

Nathan Curtis identifica tres modelos principais de governance para design systems:

**Modelo Centralizado (Solitary)**
- Um time dedicado constroi e mantem o design system
- Consumidores usam o sistema mas nao contribuem diretamente
- Pros: Consistencia alta, velocidade de decisao, qualidade controlada
- Contras: Gargalo no time central, desconexao com necessidades reais, falta de ownership

**Modelo Federado (Federated)**
- Representantes de diferentes times formam um comite de design system
- Decisoes sao tomadas coletivamente com representacao diversa
- Pros: Diversidade de perspectivas, maior buy-in, representacao de necessidades reais
- Contras: Decisoes mais lentas, risco de politica interna, coordenacao complexa

**Modelo Hibrido (Cyclical)**
- Time core dedicado com processo de contribuicao aberto a toda a organizacao
- Contribuicoes passam por review do time core antes de serem incorporadas
- Pros: Equilibrio entre consistencia e representatividade, escalavel
- Contras: Requer processo de contribuicao muito bem definido, overhead de review

### 2. Processo de Contribuicao

Amy Hupe compartilha o modelo do GOV.UK Design System como referencia:

**Etapas do Processo:**

1. **Proposal** — Qualquer pessoa pode propor novo componente ou mudanca
   - Template padronizado com: problema, evidencia de necessidade, proposta de solucao
   - Baixa barreira de entrada para encorajar contribuicoes

2. **Triage** — Time core avalia viabilidade e prioridade
   - Criterios claros: frequencia de uso, alinhamento com principios, impacto
   - Feedback transparente sobre decisao

3. **Design** — Solucao e projetada colaborativamente
   - Contributor trabalha com o time core
   - Revisao por peers de diferentes times

4. **Build** — Implementacao seguindo padroes do sistema
   - Code review pelo time core
   - Testes automatizados (visual regression, accessibility, unit tests)

5. **Document** — Documentacao completa antes do release
   - Usage guidelines, API docs, exemplos, do's and don'ts
   - Content review para clareza e consistencia

6. **Release** — Lancamento com versionamento semantico
   - Changelog detalhado
   - Migration guide quando necessario
   - Comunicacao proativa para consumidores

### 3. Communication e Change Management

Jina Anne enfatiza que comunicacao e tao importante quanto a construcao:

**Canais de Comunicacao:**
- **Changelog automatizado** — Publicado com cada release
- **Newsletter periodica** — Resumo mensal de mudancas e novidades
- **Office Hours** — Sessoes regulares para duvidas e feedback
- **Slack channel dedicado** — Comunicacao assincrona do dia-a-dia
- **Show & Tell** — Demonstracao de novos componentes e features

**Estrategia de Deprecacao:**
- Anuncio antecipado de deprecacao com timeline clara
- Migration guides detalhados com exemplos antes/depois
- Periodo de transicao com ambas versoes disponiveis
- Tooling para detectar uso de componentes deprecated (linting)
- Suporte ativo durante o periodo de migracao

### 4. Metricas de Saude do Design System

Dan Mall propoe metricas especificas para avaliar a saude da governance:

| Metrica | O que Mede | Target |
|---------|-----------|--------|
| Adoption Rate | % de componentes do DS em uso vs. custom | > 90% |
| Contribution Rate | Contribuicoes externas ao time core por trimestre | > 5 |
| Time to Contribution | Tempo medio de proposal a release | < 4 semanas |
| Breaking Change Frequency | Numero de breaking changes por trimestre | < 2 |
| Documentation Coverage | % de componentes com docs completa | 100% |
| Consumer Satisfaction | NPS dos consumidores do DS | > 60 |
| Bug Resolution Time | Tempo medio para resolver bugs reportados | < 1 semana |

### 5. Sustentabilidade a Longo Prazo

Todos os speakers concordam que sustentabilidade e o maior desafio:

- **Funding dedicado** — Design systems precisam de budget proprio, nao dependente de projetos
- **Roadmap proprio** — O design system tem seu proprio roadmap, nao apenas reage a demandas
- **Career growth** — Trabalhar no design system deve ser valorizado na carreira
- **Executive sponsorship** — Suporte visivel da lideranca executiva
- **Community building** — Cultivar senso de comunidade entre os consumidores

## Application

### Modelo de Governance na MMOS

Adotamos o **modelo hibrido (cyclical)** com as seguintes adaptacoes:

**Time Core do Design System:**
- 1 Design System Lead (dedicado 100%)
- 1 Design System Engineer (dedicado 100%)
- 1 Designer rotativo (dedicado 50%, rotacao trimestral)

**Comite de Review:**
- Design System Lead (permanente)
- 1 representante de Product Design
- 1 representante de Engineering
- 1 representante de Product Management
- Reuniao quinzenal para review de proposals e decisoes

**Processo de Contribuicao MMOS:**

| Etapa | Responsavel | SLA | Artefato |
|-------|------------|-----|----------|
| Proposal | Qualquer membro | N/A | Issue no GitHub |
| Triage | DS Lead | 3 dias uteis | Label + comentario |
| Design | Contributor + DS team | 2 semanas | Figma specs |
| Review | Comite | 1 semana | Aprovacao/feedback |
| Build | Contributor + DS engineer | 2 semanas | PR no GitHub |
| Document | Contributor + DS Lead | 1 semana | Docs atualizadas |
| Release | DS Lead | 2 dias uteis | Version bump + changelog |

**Comunicacao:**
- Slack #design-system para comunicacao diaria
- Newsletter mensal do design system
- Office hours quinzenais (30min)
- Show & Tell mensal no Design All-Hands

### Criterios de Decisao para Novos Componentes

Utilizamos a seguinte rubrica para avaliar proposals:

1. **Frequencia de Uso** (peso 3) — Quantos times/features utilizariam?
2. **Alinhamento com Principios** (peso 3) — Esta alinhado com os principios do sistema?
3. **Complexidade de Implementacao** (peso 2) — Qual o esforco de build e manutencao?
4. **Impacto na Consistencia** (peso 2) — Quanto melhora a consistencia da experiencia?
5. **Acessibilidade** (peso 2) — Pode ser implementado de forma acessivel?

Score minimo para aprovacao: 30/60 (50%)

## Resources

### Artigos Essenciais
- Nathan Curtis — "Designing a Systems Team" (medium.com/eightshapes-llc)
- Nathan Curtis — "Team Models for Scaling a Design System" (medium.com/eightshapes-llc)
- Amy Hupe — "Building the GOV.UK Design System" (amyhupe.co.uk)
- Jina Anne — "Design Tokens: Scaling Design with a Single Source of Truth"

### Livros e Ferramentas
- "Design Systems" por Alla Kholmatova (Smashing Magazine)
- **GitHub Projects** — Para tracking de proposals e roadmap
- **Chromatic** — Para visual regression testing
- **Style Dictionary** — Para gestao de design tokens

---

**Ultima atualizacao:** Marco 2026
**Responsavel:** Design Squad — MMOS
