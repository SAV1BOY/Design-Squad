# Visual Exploration Framework

## Metadata

- **Autor**: Design Squad
- **Categoria**: UI Design, Exploracao Visual, Direcionamento Estetico
- **Complexidade**: Media
- **Aplicacao**: Estruturar exploracoes visuais desde moodboards ate convergencia em direcao final
- **Ultima atualizacao**: 2026-03-18
- **Tags**: moodboard, style-tiles, design-direction, visual-language, convergence, branding

## Concept

O Visual Exploration Framework estrutura o processo de explorar e definir a linguagem visual
de um produto ou feature — desde a divergencia ampla (moodboards e referencias) ate a
convergencia em uma direcao final aprovada. O objetivo e separar decisoes esteticas de decisoes
funcionais, permitindo que o time explore opcoes visuais de forma sistematica antes de
comprometer-se com uma direcao.

O processo usa artefatos progressivamente mais concretos: moodboards (emocao e atmosfera),
style tiles (aplicacao de atributos visuais), design directions (aplicacao em contexto do
produto) e convergencia (selecao e refinamento final). Cada etapa filtra opcoes e aumenta
fidelidade, evitando o salto direto de briefing para mockup final.

## When to Use

- No inicio de projetos que envolvem nova identidade visual ou redesign significativo
- Quando stakeholders tem visoes divergentes sobre "como deve parecer"
- Para definir linguagem visual de novas features que diferem do padrao existente
- Ao expandir o design system para novos contextos (dark mode, novo produto, nova marca)
- Quando o time precisa alinhar sensibilidade estetica antes de produzir telas

## How to Apply

### Step 1 — Definir Atributos de Marca / Produto
1. Identifique 3-5 atributos que a experiencia visual deve comunicar (ex.: "confiavel", "moderno", "acessivel")
2. Para cada atributo, defina o que ele significa no contexto do produto
3. Defina anti-atributos: o que a experiencia visual NAO deve ser (ex.: "nao e infantil", "nao e frio")
4. Alinhe atributos com stakeholders antes de comecar a explorar
5. Use esses atributos como criterio de avaliacao em todas as etapas seguintes

### Step 2 — Moodboards (Divergencia Maxima)
1. Crie 2-3 moodboards distintos, cada um enfatizando combinacoes diferentes dos atributos
2. Inclua: fotografias, tipografia, paletas de cor, texturas, icones, referencias de UI
3. Fontes de referencia: Dribbble, Behance, Mobbin, competidores, fora do digital (arquitetura, moda, editorial)
4. Cada moodboard deve contar uma "historia visual" coerente, nao ser colagem aleatoria
5. Apresente aos stakeholders com narrativa: "Este moodboard comunica [atributo] atraves de [elementos]"
6. Colete feedback: quais atributos ressoam, quais nao funcionam, quais devem ser combinados

### Step 3 — Style Tiles (Convergencia Inicial)
1. Baseado no feedback dos moodboards, crie 2-3 style tiles
2. Cada style tile inclui: paleta de cores, tipografia (headings, body, caption), botoes, icones, espacamento, tratamento de imagens
3. Style tiles NAO sao layouts — sao amostras de atributos visuais aplicados a elementos de UI
4. Mantenha consistencia com design tokens existentes quando possivel
5. Apresente lado a lado para comparacao direta
6. Colete feedback especifico: "Prefiro a tipografia do tile A com as cores do tile B"

### Step 4 — Design Directions (Aplicacao em Contexto)
1. Selecione 2 direcoes finais baseadas nos style tiles aprovados
2. Aplique cada direcao em 2-3 telas-chave do produto (hero screen, tela de tarefa, tela de detalhe)
3. Mantenha o conteudo e a estrutura identicos — so mude a camada visual
4. Garanta que cada direcao funciona em light e dark mode (se aplicavel)
5. Teste acessibilidade basica: contraste, legibilidade, tamanhos minimos
6. Apresente com contexto de uso: device mockups, cenarios reais

### Step 5 — Convergencia e Decisao
1. Avalie cada direcao contra os atributos definidos no Step 1
2. Use rubrica objetiva: para cada atributo, qual direcao melhor o comunica? (escala 1-5)
3. Colete input de: design team, stakeholders, e idealmente 3-5 usuarios representativos
4. Tome a decisao com base em: aderencia aos atributos > preferencia pessoal
5. Documente a direcao escolhida e o racional da decisao
6. Identifique elementos das direcoes nao escolhidas que podem ser incorporados

### Step 6 — Documentar Linguagem Visual
1. Traduza a direcao final em especificacoes de design tokens
2. Documente principios visuais do produto (3-5 regras que guiam decisoes futuras)
3. Crie exemplos de "do" e "don't" para cada principio
4. Integre ao design system como foundation layer
5. Arquive moodboards, style tiles e direcoes descartadas como referencia historica

## Examples

### Exemplo 1 — Redesign Visual de App Financeiro
Atributos: confiavel, moderno, acessivel. Anti-atributos: nao e frio, nao e complicado.
3 moodboards: "Banco Digital" (tech-forward), "Consultor Pessoal" (humano, caloroso),
"Swiss Precision" (minimalista, neutro). Stakeholders preferiram mix de 1 + 2. Style tiles
convergiram para tipografia humanista, paleta azul-quente com acentos coral, icones com
stroke arredondado. Direcao final: aprovada com 4.2/5 nos atributos-alvo.

### Exemplo 2 — Nova Linha Visual para Feature de Analytics
Produto existente com DS consolidado. Exploracao focada em data visualization: 2 style tiles
(colorido vs. monocromatico com acentos). User testing rapido com 5 usuarios revelou que
versao monocromatica era percebida como "mais profissional" mas "dificil de distinguir dados".
Direcao final: paleta sequencial com alta diferenciacao + labels explicitos.

## Common Pitfalls

- **Pular direto para mockup**: Sem exploracao, a primeira ideia vira a unica opcao
- **Moodboard como decoracao**: Moodboard sem atributos definidos e colecao de "coisas bonitas" sem criterio
- **Stakeholder design-by-committee**: Muitas opinioes sem criterio geram Frankenstein visual
- **Ignorar acessibilidade na exploracao**: Direcao linda que reprova em contraste e retrabalho garantido
- **Uma unica direcao**: Apresentar so uma opcao nao e explorar — e pedir aprovacao
- **Nao documentar o descartado**: Direcoes rejeitadas sao referencia valiosa para futuras decisoes

## Cross-References

- [Nano Banana Generator](../agents/nano-banana-generator.md) — Agente para geracao rapida de variacoes visuais
- [Jessica UX/UI](../agents/jessica-ux-ui.md) — Agente especialista em UI e linguagem visual
- [Moodboard Template](../templates/ui/moodboard-template.md) — Template para construcao de moodboards
- [Style Tile Template](../templates/ui/style-tile-template.md) — Template para style tiles
- [design-token-architecture.md](design-token-architecture.md) — Tokens como output da exploracao visual
- [ui-layer.md](ui-layer.md) — Camada de UI onde a linguagem visual se materializa
- [design-system-governance.md](design-system-governance.md) — Governanca de decisoes visuais no DS
- [dark-mode-system.md](dark-mode-system.md) — Dark mode como variante da linguagem visual
