# Fitts's Law

## Metadata

- **Origem:** Paul Fitts (1954), aplicado a HCI por Card, Moran & Newell (1983)
- **Categoria:** Cognitive/Motor Performance Principle
- **Complexidade:** Basica
- **Aplicacao:** Dimensionamento de alvos, layout de interfaces, design mobile e touch
- **Tags:** target-size, distance, touch-targets, motor-performance, pointing, accessibility

## Concept

Fitts's Law e um modelo preditivo do movimento humano que estabelece: o tempo para
alcançar um alvo e uma funcao do tamanho do alvo e da distancia ate ele. Quanto menor o
alvo e maior a distancia, mais tempo e esforco sao necessarios para acerta-lo.
Matematicamente: T = a + b * log2(D/W + 1), onde T e o tempo, D e a distancia ao alvo
e W e a largura do alvo.

Para designers de interface, a implicacao pratica e direta: elementos interativos
importantes devem ser grandes o suficiente para serem clicados ou tocados facilmente e
posicionados de forma que minimizem a distancia de deslocamento do cursor ou dedo. Isso
e especialmente critico em interfaces touch, onde a imprecisao do toque com o dedo e
significativamente maior que a precisao de um cursor de mouse.

Fitts's Law tambem explica por que certas posicoes de tela sao mais valiosas que outras.
Cantos e bordas de tela em desktop sao alvos "infinitamente grandes" na direcao da borda
(o cursor para na borda e nao passa). Em mobile, a zona do polegar (thumb zone) determina
quais areas sao facilmente alcançaveis com uma mao. Decisoes de layout que ignoram esses
principios criam interfaces fisicamente desconfortaveis de usar.

## When to Use

- Ao dimensionar botoes, links e alvos interativos — especialmente em interfaces touch
- Para posicionar acoes primarias e CTAs em layouts de pagina e telas mobile
- Ao projetar interfaces mobile, considerando a zona do polegar e alcance
- Em decisoes de layout de toolbars, menus e barras de navegacao
- Para avaliar a ergonomia de interfaces existentes e identificar alvos problematicos

## How to Apply

1. **Dimensione alvos adequadamente:** Siga tamanhos minimos recomendados por plataforma.
   Para touch: minimo 44x44pt (Apple HIG) ou 48x48dp (Material Design). Para desktop
   com mouse: minimo 24x24px, recomendado 32x32px ou maior. Alvos menores que esses
   minimos geram erros de clique e frustracao.

2. **Aumente a area clicavel, nao apenas a visual:** A area de toque/clique pode ser maior
   que o elemento visivel usando padding transparente. Um icone de 24px pode ter area
   clicavel de 48px com padding ao redor. O usuario nao precisa ver a area de toque
   inteira para acertar o alvo.

3. **Reduza distancia entre acoes relacionadas:** Acoes frequentemente usadas em sequencia
   devem estar proximas espacialmente. "Compor" e "Enviar" em um email. "Adicionar ao
   carrinho" e "Ir para checkout". Distancia grande entre acoes sequenciais desperdiça
   tempo e aumenta a carga motora do usuario.

4. **Posicione acoes primarias na thumb zone:** Em mobile, a area inferior central da tela
   e a mais acessivel ao polegar em uso com uma mao. Posicione acoes primarias e
   frequentes nesta zona privilegiada. Acoes destrutivas ou raras podem ficar em areas
   menos acessiveis como o canto superior.

5. **Use bordas e cantos estrategicamente (desktop):** Em desktop, o cursor para nas bordas
   da tela, tornando-as alvos infinitamente grandes na direcao da borda. Menus na borda
   superior e botoes nos cantos sao mais faceis de acertar que elementos flutuando
   isolados no centro da tela.

6. **Agrupe acoes relacionadas em toolbars:** Toolbars e action bars agrupam acoes para
   minimizar distancia de deslocamento entre acoes relacionadas. Agrupe por contexto de
   uso e frequencia, nao por funcao tecnica abstrata.

7. **Considere a Lei para acoes destrutivas:** Para acoes irreversiveis (deletar conta,
   enviar pagamento), tamanho menor e distancia maior de outras acoes podem ser
   deliberados para prevenir acionamento acidental. Fitts's Law pode ser usada a favor
   da seguranca do usuario.

## Key Principles

- **Tamanho importa exponencialmente:** A relacao entre tamanho e dificuldade nao e linear.
  Reduzir um alvo de 48px para 24px mais que dobra o tempo e os erros. Cada pixel a
  menos no alvo conta proporcionalmente mais que o anterior.

- **Distancia importa logaritmicamente:** Dobrar a distancia nao dobra o tempo — o aumento
  e logaritmico. Ainda assim, minimizar distancia entre acoes sequenciais melhora a
  eficiencia de forma notavel na experiencia.

- **Touch e inerentemente impreciso:** O dedo humano tem area de contato de aproximadamente
  7mm, sem a precisao de pixel de um cursor de mouse. Interfaces touch exigem alvos
  significativamente maiores e espacamento generoso entre alvos para evitar toques
  acidentais no vizinho.

- **Posicao e tao importante quanto tamanho:** Um botao grande no lugar errado (topo direito
  do mobile, fora da thumb zone) pode ser menos acessivel que um botao medio na posicao
  certa (centro inferior da tela).

- **Velocidade versus precisao e um tradeoff:** Fitts's Law descreve um tradeoff
  fundamental: usuarios podem ser rapidos ou precisos, mas nao ambos simultaneamente
  com alvos pequenos. Alvos maiores permitem que sejam ambos.

## Examples

### Redesign de Toolbar Mobile
Problema: toolbar no topo da tela com icones de 32x32dp e spacing de 4dp entre eles.
Usuarios de telas grandes (6.5"+) nao alcançavam acoes sem reposicionar a mao, quebrando
o fluxo de uso. Solucao: toolbar movida para a parte inferior da tela, icones aumentados
para 48x48dp com spacing de 12dp, acao primaria ("criar") em FAB de 56dp no canto
inferior direito. Erros de toque cairam 45% e velocidade de interacao melhorou 30%.

### Checkout E-commerce Desktop
Problema: botao "Finalizar compra" era 120x32px em azul claro, posicionado no canto
inferior direito. Botao "Continuar comprando" era 120x32px em azul escuro, imediatamente
ao lado. Usuarios frequentemente clicavam no botao errado pela proximidade e similaridade.
Solucao: "Finalizar compra" aumentado para 240x48px em verde, posicionado isoladamente
com espaco generoso. "Continuar comprando" transformado em link textual distante.
Conversao subiu 8%.

### App de Controle Industrial
Alvos de 24x24px em um app usado com luvas de protecao em ambiente de fabrica com vibracao.
Taxa de erro de toque: 35% — inaceitavel para controles industriais. Apos redesign com
alvos de 64x64dp e spacing minimo de 16dp entre alvos, taxa de erro caiu para 3%. O
contexto de uso (luvas grossas, vibracao, iluminacao variavel) exigia alvos muito maiores
que os minimos padroes de interfaces consumer.

## Common Pitfalls

- **Otimizar apenas para estetica:** Botoes pequenos e elegantes podem ser visualmente
  agradaveis mas funcionalmente inacessiveis para o usuario. Acessibilidade e usabilidade
  devem prevalecer sobre preferencia estetica em alvos interativos.

- **Ignorar contexto de uso real:** Os minimos recomendados (44pt, 48dp) assumem condicoes
  ideais de uso. Usuarios com mobilidade reduzida, em movimento no transporte publico,
  ou usando luvas precisam de alvos consideravelmente maiores.

- **Spacing insuficiente entre alvos adjacentes:** Alvos grandes sem espacamento adequado
  entre eles geram toques acidentais no alvo vizinho. O espaco entre alvos e tao
  importante quanto o tamanho dos proprios alvos.

- **Tratamento uniforme de todas as acoes:** Nem todas as acoes precisam do mesmo tamanho.
  Acoes primarias e frequentes devem ser maiores e melhor posicionadas. Acoes secundarias
  e destrutivas podem ser menores e mais distantes.

## Cross-References

- [Interaction Design Principles](interaction-design-principles.md) — Fitts's Law
  fundamenta decisoes sobre affordance e controle de elementos interativos
- [Hick's Law](hick-law.md) — Complementa Fitts: Hick trata do tempo de decisao cognitiva,
  Fitts trata do tempo de execucao motora
- [Nielsen Heuristics](nielsen-heuristics.md) — Heuristicas 5 (error prevention) e 7
  (flexibility/efficiency) se conectam diretamente a Fitts
- [Gestalt Principles](gestalt-principles.md) — Agrupamento visual (proximidade) deve
  coincidir com agrupamento funcional para eficiencia motora
- [Atomic Design](atomic-design.md) — Tamanhos minimos de touch targets devem ser definidos
  no nivel de atoms do design system como fundacao
