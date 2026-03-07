# Design Critique Language

## Context

Linguagem para sessões de design critique — momentos formais onde o time avalia
trabalho de design com o objetivo de melhorar a qualidade final. O critique não é
sobre gosto pessoal, mas sobre eficácia do design em resolver o problema proposto.

Uma boa critique é específica, acionável e respeitosa. Separa o trabalho da pessoa,
foca em critérios objetivos e sempre propõe direções alternativas ao apontar problemas.

**Aplicação:** Design reviews, critique sessions, feedback assíncrono no Figma.
**Tom predominante:** Evidence-Driven + Pragmatic Builder
**Frequência:** Semanal (critique sessions) e contínuo (comments no Figma)

## Do's

### Ser específico sobre o que está sendo avaliado
- "A hierarquia visual do header não está guiando o olho para o CTA principal"
- "O spacing entre os cards está inconsistente — 16px no topo e 24px embaixo"
- "O contraste do texto secundário (#999) contra o fundo (#F5F5F5) é de 2.8:1"

### Fundamentar em critérios objetivos
- "Segundo as heurísticas de Nielsen, o sistema não está dando feedback suficiente"
- "O pattern de navigation tabs viola nosso guideline de máximo 5 items"
- "Os dados do teste mostram que 60% dos usuários não encontraram esse botão"

### Propor alternativas junto com a crítica
- "O layout em grid de 3 colunas pode ficar apertado em tablet. Já considerou 2 colunas com card maior?"
- "Se movermos o CTA para acima do fold e aumentarmos para 48px de height, ganhamos visibilidade"
- "Uma alternativa ao modal seria um inline expansion — menos intrusivo e mantém contexto"

### Reconhecer o que funciona bem
- "A paleta de cores está excelente — comunica confiança sem ser corporativa demais"
- "O microinteraction do toggle é polida e dá feedback claro de estado"
- "A estrutura de informação do form segue uma lógica natural e progressiva"

### Fazer perguntas antes de assumir
- "Qual foi o racional para usar accordion ao invés de tabs nessa seção?"
- "Esse espaço em branco é intencional ou é placeholder para conteúdo futuro?"
- "O usuário chega nessa tela vindo de onde? Isso muda minha leitura do contexto"

## Don'ts

### Feedback vago ou subjetivo sem fundamentação
- "Não gostei dessa tela" — sem explicar o que e por que
- "Está estranho" — sem especificar o que causa a estranheza
- "Precisa de mais pop" — não é critério de design acionável

### Misturar pessoa com trabalho
- "Você sempre faz headers grandes demais" — personaliza o feedback
- "Isso é básico, qualquer junior faria melhor" — ataca competência
- "De novo esse problema?" — tom acusatório e não construtivo

### Reescrever ao invés de orientar
- Refazer o design da pessoa sem explicar o porquê
- Impor sua preferência estética como "o jeito certo"
- Ditar solução pixel a pixel sem dar espaço para interpretação

### Ignorar restrições conhecidas
- Criticar responsividade quando o brief era só desktop
- Pedir animações complexas quando o sprint tem 3 dias
- Sugerir componentes que não existem no design system sem propor criação

## Templates

### Template de feedback estruturado
```
**Componente/Área:** [Nome ou localização na tela]
**Observação:** [O que foi identificado — factual]
**Impacto:** [Por que isso importa — para o usuário ou para o sistema]
**Sugestão:** [Alternativa proposta — acionável]
**Prioridade:** [Crítico / Importante / Nice-to-have]
```

### Template de comment no Figma
```
[TIPO: Visual | Interação | Conteúdo | A11y | Consistência]
Observação: [descrição específica]
Referência: [link para guideline, componente ou dado]
Sugestão: [alternativa proposta]
```

### Template de resumo de critique session
```
# Critique Summary — [Nome da Feature] — [Data]

## Participantes
- [Lista]

## Consensos
- [Pontos onde o grupo convergiu]

## Pontos de discussão
- [Pontos que precisam de mais exploração]

## Action items
- [ ] [Ação] — Responsável — Prazo
```
