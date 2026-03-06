# Gestalt Principles

## Metadata

- **Origem:** Psicologia Gestalt (Max Wertheimer, Kurt Koffka, Wolfgang Kohler, 1920s)
- **Categoria:** Visual Perception Principles
- **Complexidade:** Basica
- **Aplicacao:** Layout, agrupamento visual, hierarquia, design de interfaces
- **Tags:** proximity, similarity, continuity, closure, figure-ground, common-region, perception

## Concept

Os principios de Gestalt descrevem como o cerebro humano organiza informacao visual em
padroes significativos. A premissa central e que "o todo e diferente da soma das partes"
— o cerebro nao processa elementos visuais isoladamente, mas os agrupa automaticamente em
estruturas coerentes segundo regras perceptuais previsíveis. Esses principios sao leis da
percepcao neurologica, nao sugestoes de design.

Para designers de interface, Gestalt e fundamental porque determina como usuarios percebem
relacoes entre elementos antes mesmo de ler qualquer texto. Proximidade, similaridade,
continuidade, closure e figure-ground sao os mecanismos que o cerebro usa para criar
ordem visual. Quando o design respeita esses principios, a interface parece "intuitiva".
Quando viola, parece "confusa" — mesmo que o usuario nao consiga articular o motivo da
confusao.

Entender Gestalt permite projetar comunicacao visual sem depender exclusivamente de rotulos
e instrucoes textuais. A estrutura visual em si comunica relacoes, hierarquia e agrupamento.
Isso e especialmente critico em interfaces mobile, onde espaco de tela e limitado e cada
pixel deve comunicar com maxima eficiencia.

## When to Use

- Em qualquer decisao de layout e composicao visual de interface
- Para comunicar relacoes entre elementos sem depender apenas de texto explicativo
- Ao projetar formularios, tabelas, cards, dashboards e paginas de conteudo
- Para diagnosticar por que um layout parece "desorganizado" ou "confuso" para os usuarios
- Em design reviews para fundamentar feedback visual com principios objetivos e universais

## How to Apply

1. **Aplique Proximidade para agrupar:** Elementos relacionados devem estar fisicamente
   proximos. Elementos nao relacionados devem estar separados por espaco maior. Em um
   formulario, label e input devem estar mais proximos entre si do que do proximo par
   label-input. Isso elimina ambiguidade sobre qual label pertence a qual campo.

2. **Use Similaridade para categorizar:** Elementos com funcao similar devem ter aparencia
   similar (cor, forma, tamanho, estilo tipografico). Todos os botoes primarios devem ter
   o mesmo estilo visual. Todos os links devem ter o mesmo tratamento. Quando um elemento
   se parece com outro, o usuario assume que se comporta como o outro.

3. **Mantenha Continuidade em fluxos:** O olho segue linhas e curvas naturalmente, sem
   esforco consciente. Use alinhamento e fluxo direcional para guiar o olhar do usuario
   pela interface na ordem desejada. Elementos alinhados em uma linha sao percebidos
   como parte do mesmo grupo ou sequencia logica.

4. **Explore Closure para simplificar:** O cerebro completa formas incompletas
   automaticamente. Isso permite usar icones simplificados, bordas parciais e formas
   sugeridas que comunicam sem ocupar espaco visual excessivo. Cards nao precisam de
   bordas em todos os lados se sombra e background ja criam separacao suficiente.

5. **Gerencie Figure-Ground com cuidado:** A relacao entre elemento de foco (figure) e
   fundo (ground) deve ser inequivoca em todos os contextos. Use contraste, elevacao
   (sombras) e cor para garantir que o usuario identifique claramente o que e conteudo
   principal e o que e background de suporte.

6. **Aplique Common Region para containers:** Elementos dentro de uma mesma area delimitada
   (borda, background diferente, card com sombra) sao percebidos como um grupo funcional.
   Use common region para criar containers logicos que organizam conteudo relacionado
   visualmente.

7. **Valide com squint test:** Olhe para o layout com olhos semi-cerrados (ou desfocando
   a visao). Se os agrupamentos visuais correspondem aos agrupamentos logicos, a Gestalt
   esta funcionando corretamente. Se nao, ajuste espacamento, cor ou bordas.

## Key Principles

- **Proximidade e o principio mais poderoso:** Espacamento e a ferramenta mais eficaz para
  comunicar relacao entre elementos. Antes de adicionar bordas, linhas ou cores para
  separar conteudo, tente simplesmente ajustar o espacamento.

- **Similaridade cria expectativa comportamental:** Quando dois elementos parecem iguais,
  o usuario assume que se comportam igualmente. Quebrar essa expectativa (botao que parece
  link, link que parece texto) gera confusao e erros de interacao.

- **Figure-ground deve ser inequivoco:** Ambiguidade na relacao figure-ground forca o
  cerebro a processar continuamente sem resolucao, gerando fadiga visual. Modais,
  dropdowns e tooltips dependem de figure-ground claro para funcionar.

- **Menos elementos, mais percepcao:** Gestalt permite comunicar mais com menos elementos
  visuais. Em vez de adicionar labels, bordas e separadores, use espacamento e
  similaridade. Interfaces limpas sao possiveis porque Gestalt faz o trabalho pesado
  de organizacao perceptual.

- **Contexto cultural e limitado:** Principios de Gestalt sao baseados em percepcao
  neurologica, nao cultural. Proximidade funciona igualmente em interfaces em portugues,
  arabe ou japones. Isso os torna universalmente aplicaveis sem adaptacao cultural.

## Examples

### Design de Formulario
Problema: usuarios associavam labels ao campo errado em um formulario longo com muitos
campos. Causa: espacamento igual entre label e campo acima e label e campo abaixo, criando
ambiguidade perceptual. Solucao com Proximidade: reduzir espaco entre label e seu campo
para 4px e aumentar espaco entre grupos de campos para 24px. Taxa de erro de
preenchimento caiu de 12% para 2%.

### Dashboard de Analytics
Problema: dashboard com 15 metricas parecia caotico e desestruturado. Solucao combinando
multiplos principios: Common Region agrupou metricas relacionadas em cards (financeiro,
engajamento, performance). Similaridade fez metricas positivas verdes e negativas
vermelhas. Proximidade aproximou titulo e valor de cada metrica individual. Continuidade
alinhou cards em grid consistente. Resultado: tempo para encontrar uma metrica especifica
caiu de 15s para 4s.

### Navegacao Mobile
Problema: tab bar com 5 icones onde usuarios nao distinguiam item ativo de inativo de
forma clara. Solucao com Figure-Ground e Similaridade: icone ativo em cor primaria com
label visivel (figure claro), icones inativos em cinza sem label (ground). Closure:
icone ativo dentro de pill shape sugerida sem borda completa. Taxa de navegacao acidental
entre tabs caiu em 60%.

## Common Pitfalls

- **Proximidade ambigua:** Espacamento uniforme entre todos os elementos impede o cerebro
  de identificar grupos significativos. Crie hierarquia de espacamento clara e consistente:
  dentro de grupo < entre grupos < entre secoes.

- **Similaridade excessiva sem diferenciacao:** Se todos os elementos parecem iguais, nada
  se destaca e nao ha hierarquia. Hierarquia visual requer diferenca deliberada — use
  contraste de tamanho, peso e cor para criar niveis claros de importancia.

- **Ignorar figure-ground em overlays:** Modais sem overlay escuro no background, dropdowns
  sem sombra, e tooltips sem contraste adequado com o fundo criam ambiguidade figure-ground
  que confunde o usuario sobre o que e acionavel.

- **Confiar apenas em cor para comunicar:** Cor e uma ferramenta de Similaridade poderosa,
  mas insuficiente isoladamente. Usuarios daltonicos (8% dos homens) nao distinguem verde
  de vermelho. Combine cor com forma, icone ou texto sempre.

## Cross-References

- [Interaction Design Principles](interaction-design-principles.md) — Gestalt fundamenta
  decisoes visuais que suportam principios interativos de IxD
- [Nielsen Heuristics](nielsen-heuristics.md) — Heuristicas como "aesthetic and minimalist
  design" e "recognition over recall" dependem de Gestalt
- [Atomic Design](atomic-design.md) — Composicao de atomos em moleculas e organismos usa
  principios de agrupamento Gestalt para criar coerencia
- [Information Architecture Toolkit](information-architecture-toolkit.md) — Estrutura logica
  de IA deve ser reforçada por agrupamento visual Gestalt
- [Fitts's Law](fitts-law.md) — Tamanho visual dos alvos e relacao figure-ground afetam
  a aplicacao pratica de Fitts's Law
