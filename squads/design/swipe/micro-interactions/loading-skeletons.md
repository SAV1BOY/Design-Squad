# Loading Skeleton Patterns

## Pattern Description

Padroes para skeleton screens que indicam carregamento mantendo o layout esperado do conteudo. Skeletons reduzem percepcao de tempo de espera comparado a spinners.

## Examples

### Example 1: Facebook — Content-Shaped Skeletons
Facebook popularizou skeletons no feed:
- Formas que espelham o layout real (avatar circular, texto retangular)
- Animacao pulse (opacity 1 → 0.4 → 1) com duracao de 1.5s
- Gradiente da esquerda para direita (wave) como alternativa
- Placeholder para imagem com aspect-ratio correto
- Transicao fade do skeleton para conteudo real

### Example 2: LinkedIn — Progressive Skeleton
LinkedIn carrega progressivamente:
- Header carrega primeiro (skeleton removido)
- Feed carrega em blocos (2-3 cards por vez)
- Skeleton dos proximos cards visivel durante scroll
- Shimmer effect (gradiente em movimento)
- `aria-busy="true"` no container durante loading

### Example 3: Notion — Page Skeleton
Notion mostra skeleton de pagina:
- Sidebar carrega independentemente do conteudo
- Breadcrumb skeleton com largura variavel
- Content blocks com alturas proporcionais ao tipo
- Transicao suave (fade 300ms) ao carregar conteudo
- Skeleton persiste max 5s, depois mostra error state

## Analysis

Skeletons eficazes:
- **Fidelidade**: forme que espelha o layout real do conteudo
- **Animacao**: pulse ou shimmer sutil (nao estático)
- **Performance**: CSS puro (evite imagens ou JS pesado)
- **Timeout**: apos 5s, mostre mensagem ou error state
- **A11y**: `aria-busy="true"` + `aria-label="Carregando"`
- **Transicao**: fade suave do skeleton para conteudo real

## Tags

`skeleton`, `loading`, `perceived-performance`, `animation`, `progressive-loading`
