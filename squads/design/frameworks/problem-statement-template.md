# Problem Statement Template

## Metadata

- **Origem:** Multiplas tradicoes de design (d.school, IDEO, Google Ventures)
- **Categoria:** Problem Framing Tool
- **Complexidade:** Basica a Intermediaria
- **Aplicacao:** Definicao de problemas, alinhamento de equipe, scoping de projetos
- **Tags:** how-might-we, constraints, problem-framing, POV, design-brief

## Concept

Um problem statement e a articulacao clara e concisa do problema que a equipe esta tentando
resolver. O formato mais utilizado em design e o "How Might We" (HMW) — "Como poderiamos...?"
— que transforma desafios em oportunidades de design. Um bom problem statement e amplo o
suficiente para permitir multiplas solucoes, mas especifico o suficiente para ser acionavel.

O problem statement funciona como um contrato entre a equipe e os stakeholders. Ele define
o que esta dentro e fora do escopo, quem sao os usuarios-alvo, e quais constraints devem
ser respeitadas. Sem um problem statement claro, equipes frequentemente divergem em direcoes
conflitantes, resolvem problemas diferentes uns dos outros, ou criam solucoes para problemas
que nao existem.

A formulacao do problem statement e iterativa. Comeca-se com uma versao ampla baseada em
suposicoes iniciais e refina-se progressivamente conforme pesquisa com usuarios revela o
problema real. O erro mais comum e tratar o primeiro rascunho como definitivo e imutavel.

## When to Use

- No inicio de qualquer projeto de design, apos pesquisa inicial com usuarios
- Quando a equipe percebe que esta trabalhando sem direcao clara ou alinhamento
- Para alinhar stakeholders com expectativas diferentes sobre o que o projeto deve resolver
- Em workshops de discovery para transicionar de insights de pesquisa para direcao de design
- Quando multiplas oportunidades foram identificadas e e necessario priorizar foco

## How to Apply

1. **Reuna insights de pesquisa:** Antes de escrever qualquer statement, revise os dados de
   pesquisa — entrevistas, observacoes, analytics, feedback. Identifique padroes, dores
   recorrentes e necessidades nao atendidas. Sem base em evidencias, o statement sera
   baseado em suposicoes que podem estar erradas.

2. **Escreva o Point of View (POV):** Use o formato: "[Usuario-alvo] precisa de [necessidade]
   porque [insight]". Exemplo: "Gestores de projeto junior precisam visualizar dependencias
   entre tarefas porque perdem prazos quando nao enxergam impactos em cascata."

3. **Transforme em How Might We:** Converta o POV em pergunta HMW: "Como poderiamos ajudar
   gestores junior a visualizar dependencias entre tarefas para evitar atrasos em cascata?"
   Ajuste o nivel de abrangencia — nem amplo demais ("Como poderiamos melhorar gestao de
   projetos?") nem restrito demais ("Como poderiamos adicionar um grafico Gantt?").

4. **Defina constraints explicitas:** Liste restricoes reais do projeto: tecnologicas
   ("deve funcionar no app mobile existente"), temporais ("MVP em 6 semanas"), de recursos
   ("sem backend novo"), de negocio ("nao pode canibalizar produto X"), regulatorias
   ("conformidade LGPD").

5. **Defina anti-goals:** Explicite o que o projeto NAO vai resolver. Isso e tao importante
   quanto definir o escopo positivo. Anti-goals evitam scope creep e alinham expectativas
   de todos os envolvidos.

6. **Valide com stakeholders e usuarios:** Apresente o problem statement para stakeholders
   e, se possivel, para usuarios. Pergunte: "Isso representa o problema que voce enfrenta?"
   Ajuste conforme o feedback recebido.

7. **Itere conforme o projeto evolui:** O problem statement pode ser refinado apos fases de
   ideacao e teste. Se testes revelam que o problema real e diferente do assumido, reescreva
   o statement sem hesitar.

## Key Principles

- **Problema, nao solucao:** O statement deve descrever o problema e a necessidade do
  usuario, nunca prescrever uma solucao. "Como poderiamos adicionar notificacoes push?"
  contem solucao. "Como poderiamos manter usuarios informados em tempo real?" e
  problem-focused.

- **Baseado em evidencia:** Cada elemento do statement deve ser rastreavel a dados de
  pesquisa — citacoes de usuarios, metricas, observacoes. Statements baseados em
  suposicoes levam a solucoes irrelevantes.

- **Nivel certo de abrangencia:** Um HMW muito amplo nao guia decisoes. Um muito restrito
  limita a criatividade. Teste: se o statement admite pelo menos 3 abordagens diferentes
  de solucao, a abrangencia esta adequada.

- **Centrado no usuario:** O statement deve nomear o usuario-alvo e sua necessidade real,
  nao objetivos de negocio disfarçados de necessidades do usuario. "Como poderiamos
  aumentar conversao?" nao e centrado no usuario.

- **Constraints como aliadas:** Restricoes nao sao inimigas da criatividade — sao
  estimulantes. Constraints claras focam a exploracao e tornam ideias mais realizaveis
  dentro do contexto real do projeto.

## Examples

### Plataforma de Telemedicina
POV: "Pacientes idosos em areas rurais precisam de acesso facilitado a consultas medicas
porque deslocamento ate a cidade mais proxima e fisicamente desgastante e financeiramente
proibitivo." HMW: "Como poderiamos permitir que pacientes idosos em areas rurais consultem
medicos sem precisar se deslocar?" Constraints: deve funcionar em conexoes 3G lentas;
interface acessivel para baixa alfabetizacao digital; conformidade com regulacao de saude.
Anti-goals: nao substitui emergencias presenciais; nao inclui farmacia delivery.

### Ferramenta de Colaboracao para Times Remotos
POV: "Designers em equipes distribuidas precisam de feedback contextual assincrono porque
fusos horarios diferentes impedem sessoes sincronas frequentes." HMW: "Como poderiamos
facilitar feedback de design contextualizado em equipes distribuidas sem depender de
reunioes sincronas?" Constraints: integracao com Figma; latencia maxima de 2s; suporte
a anotacoes visuais. Anti-goals: nao substituir ferramentas de video-call existentes.

### Onboarding de App Financeiro
POV: "Usuarios millennials de primeira viagem em investimentos precisam entender risco
de forma intuitiva porque terminologia financeira tradicional gera inseguranca e abandono."
HMW: "Como poderiamos tornar o conceito de risco financeiro compreensivel e nao-intimidante
para investidores iniciantes?" Constraints: compliance regulatoria impede simplificacao
excessiva; onboarding maximo de 5 telas; deve funcionar sem suporte humano.

## Common Pitfalls

- **Solution-first framing:** "Como poderiamos criar um chatbot para atendimento?" ja
  contem a solucao. Reescreva para focar no problema: "Como poderiamos resolver duvidas
  frequentes de forma instantanea e sem espera?"

- **Problema do stakeholder, nao do usuario:** "Como poderiamos aumentar o LTV?" e um
  objetivo de negocio, nao um problema de usuario. Encontre a necessidade do usuario
  que, quando atendida, gera o resultado de negocio desejado.

- **Falta de constraints:** Um HMW sem restricoes gera ideias irrealizaveis que frustram
  a equipe na hora da implementacao. Constraints nao limitam criatividade — elas a
  direcionam produtivamente.

- **Statement fossilizado:** Tratar o problem statement como imutavel apos ser escrito
  impede a equipe de incorporar novos aprendizados. Revise o statement regularmente
  ao longo do projeto e ajuste quando necessario.

## Cross-References

- [Design Thinking](design-thinking.md) — Problem statements sao o output principal da
  fase Define do processo
- [Double Diamond](double-diamond.md) — O statement e o ponto de convergencia do primeiro
  diamante, conectando problema a solucao
- [Jobs to Be Done](jobs-to-be-done.md) — Job statements e outcomes alimentam a formulacao
  de HMWs mais precisos e fundamentados
- [Hypothesis-Driven Design](hypothesis-driven-design.md) — Problem statements se desdobram
  em hipoteses testaveis para validacao
- [North Star and Success Metrics](north-star-and-success-metrics.md) — Metricas de sucesso
  devem ser derivadas do problem statement definido
