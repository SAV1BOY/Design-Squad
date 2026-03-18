# Interview Framework

## Metadata

- **Autor**: Design Squad
- **Categoria**: Research, Discovery, Qualitativo
- **Complexidade**: Media
- **Aplicacao**: Planejar, conduzir e sintetizar entrevistas de usuario com rigor metodologico
- **Ultima atualizacao**: 2026-03-18
- **Tags**: user-interview, screener, probing, rapport, synthesis, ethics

## Concept

O Interview Framework estrutura o processo completo de entrevistas com usuarios — do recrutamento
a sintese. Entrevistas sao a ferramenta qualitativa mais versatil do design research, mas sua
qualidade depende diretamente de preparacao rigorosa, tecnicas de probing eficazes e sintese
disciplinada. Um guia mal construido ou rapport fraco gera dados superficiais que levam a decisoes
erradas.

Este framework cobre screener design, construcao do guia, tecnicas de conduzir a conversa,
etica de pesquisa e metodos de sintese que transformam transcricoes em insights acionaveis.

## When to Use

- No discovery para entender problemas, comportamentos e contextos dos usuarios
- Para validar hipoteses qualitativas antes de investir em solucoes
- Quando dados quantitativos mostram "o que" mas nao explicam "por que"
- Para explorar necessidades latentes que usuarios nao articulam espontaneamente
- Apos lancamento para entender percepcao real do produto
- Quando personas precisam ser criadas ou atualizadas com dados reais

## How to Apply

### Step 1 — Definir Objetivo e Research Questions
1. Defina o objetivo da pesquisa em 1 frase: "Entender como [perfil] [comportamento] no contexto de [situacao]"
2. Liste 3-5 research questions (o que voce quer descobrir, nao o que vai perguntar)
3. Defina criterios de sucesso: que tipo de insight tornaria esta pesquisa valiosa?
4. Alinhe com PM e stakeholders para garantir que os outputs sao acionaveis

### Step 2 — Criar Screener de Recrutamento
1. Defina criterios de inclusao (quem voce quer) e exclusao (quem distorceria os dados)
2. Monte questionario de triagem com 5-8 perguntas objetivas
3. Inclua perguntas de disfarce para evitar auto-selecao enviesada
4. Defina tamanho da amostra: 5-8 participantes por segmento para saturacao tematica
5. Inclua criterios de diversidade (genero, idade, experiencia com o produto)

### Step 3 — Construir Guia de Entrevista
1. **Abertura (5 min)**: Apresentacao, consentimento, explicacao do formato, quebra-gelo
2. **Contexto (10 min)**: Perguntas amplas sobre rotina, comportamento geral, relacao com o dominio
3. **Exploracao profunda (20-25 min)**: Perguntas sobre o tema central, cenarios especificos, ultimas experiencias
4. **Reacao a estimulos (10 min)**: Mostrar prototipos, screenshots ou conceitos (opcional)
5. **Fechamento (5 min)**: Perguntas finais, espaco para o participante adicionar algo, agradecimento
6. Escreva perguntas abertas — evite sim/nao e perguntas direcionadoras

### Step 4 — Tecnicas de Probing durante a Entrevista
- **Echo probing**: Repita a ultima frase do participante com entonacao de pergunta
- **Silent probing**: Faca uma pausa de 5-7 segundos — o silencio convida elaboracao
- **Laddering (why chain)**: "Por que isso e importante pra voce?" repetido 3-5 vezes
- **Critical incident**: "Me conta a ultima vez que isso aconteceu — o que voce fez?"
- **Contraste**: "Como seria se fosse diferente? O que mudaria pra voce?"
- **Projecao**: "Se voce pudesse mudar uma coisa, o que seria?"

### Step 5 — Rapport e Etica
1. Obtenha consentimento informado por escrito antes da sessao
2. Explique gravacao, uso dos dados e anonimizacao
3. Deixe claro que nao ha respostas certas ou erradas
4. Nao corrija o participante — observe, nao eduque
5. Oferca opcao de parar a qualquer momento
6. Pague incentivo justo pelo tempo do participante
7. Nunca compartilhe dados individuais identificaveis

### Step 6 — Sintese
1. Faca debrief de 10 min imediatamente apos cada sessao (top 3 insights, surpresas)
2. Transcreva ou revise gravacoes com notas timestamped
3. Use affinity mapping para agrupar observacoes em temas
4. Escreva insight statements: "[Perfil] precisa [necessidade] porque [motivacao]"
5. Identifique padroes (recorrentes em 3+ participantes) vs. outliers
6. Documente citacoes representativas para cada insight

## Examples

### Exemplo 1 — Discovery de Feature de Notificacoes
Objetivo: entender como usuarios gerenciam notificacoes. 6 entrevistas, 45 min cada.
Finding principal: usuarios nao desativam notificacoes — eles ignoram o app inteiro.
O problema real nao era excesso de notificacoes, era irrelevancia. Insight redirecionou
a solucao de "settings de notificacao" para "personalizacao por relevancia".

### Exemplo 2 — Validacao de Conceito de Onboarding
8 entrevistas com novos usuarios. Probing revelou que o bloqueio nao era complexidade
do setup, mas medo de "configurar errado e perder dados". Solucao: setup reversivel
com preview antes de confirmar. Conceito validado com 7/8 participantes.

## Common Pitfalls

- **Perguntas direcionadoras**: "Voce nao acha que seria melhor se..." invalida a resposta
- **Pular screener**: Entrevistar o perfil errado gera dados inuteis
- **Guia rigido demais**: O guia e mapa, nao trilho — siga o participante quando ele revela algo rico
- **Nao gravar**: Confiar na memoria gera dados filtrados pelo bias do pesquisador
- **Sintese individual**: Sintetize em dupla ou trio para reduzir bias interpretativo
- **Entrevistar so "power users"**: Diversidade de perfis revela diversidade de necessidades

## Cross-References

- [UX Design Expert](../agents/ux-design-expert.md) — Agente especialista em research qualitativo
- [Interview Guide Quality Checklist](../checklists/interview-guide-quality.md) — Checklist de qualidade do guia
- [Interview Script Template](../templates/research/interview-script-template.md) — Template do guia semi-estruturado
- [insight-synthesis-framework.md](insight-synthesis-framework.md) — Framework de sintese pos-entrevista
- [discovery-layer.md](discovery-layer.md) — Entrevistas como atividade central de discovery
- [hypothesis-driven-design.md](hypothesis-driven-design.md) — Hipoteses informam research questions
- [jobs-to-be-done.md](jobs-to-be-done.md) — JTBD como lente para guia de entrevista
