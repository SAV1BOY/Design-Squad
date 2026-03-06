# Interaction Design Principles

## Metadata

- **Origem:** Don Norman, Alan Cooper, Bill Moggridge e comunidade IxD
- **Categoria:** Design Principles
- **Complexidade:** Basica a Intermediaria
- **Aplicacao:** Design de interfaces interativas, micro-interactions, fluxos de usuario
- **Tags:** feedback, affordance, consistency, control, mapping, constraints, discoverability

## Concept

Interaction Design (IxD) e a disciplina que projeta como usuarios interagem com sistemas
digitais. Os principios de IxD sao fundamentos cognitivos e perceptuais que, quando
aplicados corretamente, tornam interfaces intuitivas, previsiveis e agradaveis de usar.
Diferente de guidelines especificas de plataforma, estes principios sao universais e
atemporais, aplicaveis a qualquer tipo de interface.

Don Norman, em "The Design of Everyday Things", articulou conceitos fundamentais como
affordance (o que um elemento sugere que pode fazer), signifiers (sinais que indicam como
interagir), feedback (resposta do sistema a acoes do usuario), mapping (relacao espacial
entre controle e efeito) e constraints (limitacoes que previnem erros). Esses conceitos
formam o vocabulario base de todo profissional de IxD.

Alan Cooper complementou com principios de comportamento: respeitar o modelo mental do
usuario, nao forcar o usuario a pensar como o sistema pensa, e projetar para objetivos
(goals) em vez de tarefas (tasks). A combinacao de Norman e Cooper fornece uma base
solida e duradoura para decisoes de interaction design.

## When to Use

- Em qualquer decisao de design que envolva como o usuario interage com a interface
- Para avaliar e melhorar interfaces existentes usando criterios fundamentados
- Em design reviews e criticas de design como vocabulario compartilhado pela equipe
- Ao projetar micro-interactions, transicoes, animacoes e estados de componentes
- Para treinar designers junior em fundamentos de design interativo

## How to Apply

1. **Garanta affordance e signifiers claros:** Cada elemento interativo deve comunicar
   visualmente o que faz e como interagir. Botoes devem parecer clicaveis com elevacao
   ou contraste. Links devem ser distinguiveis de texto. Arrastaveis devem ter handles
   visuais. Se o usuario precisa adivinhar, o design falhou.

2. **Implemente feedback imediato:** Toda acao do usuario deve ter resposta perceptivel do
   sistema. Cliques devem ter feedback visual (mudanca de estado). Envios devem confirmar
   sucesso ou reportar erro. Processos longos devem mostrar progresso. Silencio do sistema
   gera incerteza e ansiedade.

3. **Mantenha consistencia em tres niveis:** Consistencia interna (dentro do produto),
   consistencia externa (com padroes da plataforma e convencoes do mercado), e consistencia
   temporal (o mesmo elemento se comporta igual em diferentes momentos e contextos).
   Inconsistencia forca reaprendizado desnecessario.

4. **Projete mapping natural:** A relacao entre controle e efeito deve ser espacialmente
   e logicamente intuitiva. Slider para a direita aumenta valor. Scroll para baixo revela
   mais conteudo. Toggle para a direita ativa funcionalidade. Quando o mapping nao e
   natural, erros aumentam significativamente.

5. **Use constraints para prevenir erros:** Limite opcoes e acoes para prevenir erros ao
   inves de apenas reporta-los depois. Desabilite botoes quando a acao nao e possivel.
   Limite caracteres em campos. Use type-specific inputs (date picker em vez de campo
   de texto livre para datas).

6. **Garanta controle e liberdade ao usuario:** Permita undo, cancel e back em toda
   interacao significativa. Nunca aprisione o usuario em um fluxo sem saida clara.
   Confirmacoes antes de acoes destrutivas (deletar, enviar pagamento) sao obrigatorias.

7. **Projete para discoverability:** Features existem apenas se usuarios sabem que existem.
   Use progressive disclosure para revelar funcionalidades no momento certo. Tooltips,
   empty states educativos e onboarding contextual apoiam a descoberta gradual.

## Key Principles

- **Feedback e nao-negociavel:** Interfaces sem feedback sao como conversar com alguem que
  nao responde. Cada acao precisa de resposta — visual, sonora ou haptica. A ausencia de
  feedback e a forma mais basica de ma experiencia.

- **Affordance percebida e o que importa:** Nao importa o que o elemento tecnicamente pode
  fazer — importa o que o usuario percebe que pode fazer. Um botao flat sem borda pode
  parecer texto comum. A affordance percebida deve coincidir com a funcao real.

- **Consistencia reduz carga cognitiva:** Quando padroes se repetem, usuarios transferem
  aprendizado de uma parte do produto para outra automaticamente. Cada inconsistencia
  forca o cerebro a processar algo novo, consumindo recursos cognitivos limitados.

- **Controle gera confianca:** Usuarios que sentem controle sobre a interface confiam mais
  no produto e na marca. Undo, cancel, voltar, desfazer — essas opcoes nao sao features
  opcionais, sao direitos fundamentais do usuario.

- **Constraints sao gentileza:** Prevenir um erro e sempre melhor que reporta-lo depois.
  Constraints bem projetadas nao limitam o usuario — elas protegem de consequencias
  indesejadas e reduzem a carga de decisao.

- **Visibilidade do estado do sistema:** O usuario deve sempre saber onde esta, o que esta
  acontecendo, e o que pode fazer em seguida. Incerteza sobre o estado atual gera
  ansiedade, erros e abandono.

## Examples

### Micro-interactions em Form de Cadastro
Feedback: campos validam em tempo real com indicadores visuais de sucesso (verde) e erro
(vermelho + mensagem especifica dizendo o que corrigir). Constraints: campo de email
bloqueia espacos, campo de telefone aceita apenas numeros e formata automaticamente.
Mapping: tab move para o proximo campo na ordem visual. Affordance: botao de submit fica
desabilitado ate todos os campos obrigatorios serem validamente preenchidos. Resultado:
taxa de erro no submit caiu de 35% para 4%.

### Editor de Texto Colaborativo
Consistencia: atalhos de teclado seguem convencoes do OS (Ctrl+B para bold, Ctrl+Z para
undo). Feedback: cursor de outros colaboradores e visivel em tempo real com nome e cor
distintas. Controle: historico de versoes permite reverter qualquer mudanca a qualquer
momento. Constraints: formatacao limitada a estilos predefinidos mantendo consistencia
do documento final.

### App de Navegacao GPS
Mapping natural: mapa gira conforme usuario gira fisicamente (quando em modo pedestrian).
Feedback: vibracoes hapticas ao se aproximar de uma curva importante. Affordance: botao
de zoom com icone de + e - universalmente compreensivel. Visibilidade de estado: barra
de progresso mostra distancia restante e tempo estimado de chegada em tempo real.

## Common Pitfalls

- **Feedback atrasado ou ausente:** A causa mais frequente de cliques duplos acidentais e
  submissoes duplicadas e a falta de feedback imediato. Se o sistema demora para responder,
  pelo menos mostre um estado de loading imediato.

- **Consistencia com a plataforma errada:** Um app iOS que se comporta como Android (ou
  vice-versa) viola expectativas do usuario e gera confusao. Respeite convencoes da
  plataforma especifica onde o produto roda.

- **Affordance falsa:** Elementos que parecem clicaveis mas nao sao (ou vice-versa) geram
  frustacao e desconfianca no produto. Cada affordance visual deve corresponder a uma
  acao real e funcional.

- **Excesso de constraints:** Constraints que bloqueiam acoes legitimas do usuario sao tao
  ruins quanto a falta delas. Se o constraint impede o usuario de completar seu objetivo
  real, e restritivo e frustrante — nao protetor.

## Cross-References

- [Nielsen Heuristics](nielsen-heuristics.md) — As 10 heuristicas incluem e expandem
  varios principios fundamentais de IxD
- [Gestalt Principles](gestalt-principles.md) — Principios visuais que fundamentam decisoes
  de layout, agrupamento e hierarquia visual
- [Fitts's Law](fitts-law.md) — Fundamenta decisoes sobre tamanho e posicionamento de
  alvos interativos na interface
- [Hick's Law](hick-law.md) — Informa decisoes sobre numero de opcoes apresentadas e
  progressive disclosure de funcionalidades
- [Atomic Design](atomic-design.md) — Principios de IxD devem ser aplicados consistentemente
  em cada nivel do design system
