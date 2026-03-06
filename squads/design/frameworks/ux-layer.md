# UX Layer

## Metadata
- **Autor**: Design Squad
- **Categoria**: Stack Layer, UX Design
- **Complexidade**: Media
- **Aplicacao**: Definicao de fluxos, information architecture, wireframes e conteudo
- **Ultima atualizacao**: 2026-03-06

## Concept

A UX Layer e a terceira camada do stack de design, onde a estrategia se materializa em
estrutura de experiencia. Aqui sao definidos os fluxos de usuario, a information
architecture (IA), wireframes e a estrategia de conteudo.

Esta camada resolve o "como funciona" antes do "como se parece". O foco e em logica,
estrutura e fluxo — nao em estetica. Um wireframe bem feito comunica hierarquia,
prioridades e relacoes entre elementos sem influencia de cores, tipografia ou estilo visual.

A separacao entre UX e UI (proxima camada) nao e dogmatica — em muitos contextos,
trabalham em paralelo. Mas a distincao conceitual e importante: decisoes de estrutura
e fluxo sao fundamentalmente diferentes de decisoes visuais.

## When to Use

- Apos definicao estrategica, quando se precisa dar forma a experiencia
- Quando a equipe precisa alinhar sobre fluxos e estrutura antes do visual
- Quando se projeta novos fluxos ou reestrutura fluxos existentes
- Quando problemas de usabilidade indicam falhas de estrutura, nao de visual
- Quando se precisa validar a logica de experiencia com stakeholders ou usuarios
- Quando a IA do produto precisa ser definida ou reestruturada

## How to Apply

### Dimensao 1 — Fluxos de Usuario
1. Mapeie os fluxos criticos do usuario (task flows):
   - Entry points: de onde o usuario vem
   - Steps: acoes sequenciais necessarias
   - Decision points: onde o usuario escolhe caminhos
   - End states: sucesso, erro, abandono
2. Identifique happy paths e exception paths
3. Mapeie edge cases: o que acontece quando dados faltam, erros ocorrem,
   conexao cai, permissoes sao insuficientes
4. Minimize steps sem sacrificar clareza
5. Valide fluxos com walkthrough antes de wireframes

### Dimensao 2 — Information Architecture
1. **Card sorting**: Descubra como usuarios agrupam informacoes mentalmente
2. **Tree testing**: Valide se a estrutura permite encontrar informacao
3. Defina hierarquia de navegacao: primaria, secundaria, contextual
4. Mapeie relacoes entre conteudos (links, referencias, dependencias)
5. Crie sitemap ou app map documentando a estrutura completa
6. Defina taxonomia consistente (naming de secoes, categorias, acoes)

### Dimensao 3 — Wireframes
1. Comece com sketches de baixa fidelidade (papel ou Figma lo-fi)
2. Foque em: hierarquia de conteudo, posicao relativa, prioridade visual
3. Nao use cores (grayscale), nao use tipografia final, nao use imagens reais
4. Documente decisoes de layout com notas explicativas
5. Crie wireframes para todos os estados: default, loading, empty, error, success
6. Inclua responsive breakpoints: mobile, tablet, desktop
7. Use conteudo real ou realista (nao "Lorem ipsum" em wireframes)

### Dimensao 4 — Estrategia de Conteudo
1. Defina tom de voz para cada contexto (onboarding vs erro vs sucesso)
2. Escreva microcopy para acoes criticas (labels, CTAs, mensagens de erro)
3. Priorize clareza sobre criatividade em conteudo funcional
4. Crie glossario de termos do produto (consistencia terminologica)
5. Defina hierarquia de conteudo: titulo > descricao > detalhe > meta
6. Teste conteudo com usuarios (o que entendem, o que confunde)

## Key Principles

- **Estrutura antes de estetica**: Resolva o "como funciona" antes do "como se parece"
- **Fluxos sao a experiencia**: Usuarios experimentam sequencias, nao telas isoladas
- **IA e invisivel quando bem feita**: Boa arquitetura de informacao e transparente
- **Conteudo e interface**: Copy e tao importante quanto layout
- **Wireframes comunicam intencao**: Nao sao mockups — sao documentos de decisao
- **Edge cases sao experiencia real**: Usuarios reais encontram erros, dados faltantes, timeout
- **Validacao precoce**: Testar fluxos e IA cedo e barato; testar depois e custoso

## Examples

### Exemplo 1 — Fluxo de Onboarding
```
[Landing Page] -> [Signup Form] -> [Email Verification]
    -> [Profile Setup] -> [First Action] -> [Dashboard]
         |                    |
         v                    v
    [Skip to Dashboard]  [Help Tooltip]
```
Edge cases mapeados: email ja cadastrado, verificacao expirada, setup
interrompido e retomado, primeiro acesso via deep link.

### Exemplo 2 — IA Validation
Tree test com 15 usuarios para validar navegacao de SaaS:
- Tarefa: "Encontre a fatura do mes passado" — 80% sucesso (ok)
- Tarefa: "Mude sua senha" — 45% sucesso (problema: estava em "Perfil",
  usuarios procuravam em "Configuracoes")
- Acao: Mover seguranca de Perfil para Configuracoes, ou criar shortcut

### Exemplo 3 — Wireframe com Conteudo Real
Em vez de "Lorem ipsum dolor sit amet" no wireframe de pagina de produto:
- Titulo: "Fone de ouvido Bluetooth com cancelamento de ruido"
- Preco: "R$ 459,90 ou 12x R$ 38,32"
- CTA: "Adicionar ao carrinho"
Conteudo real revelou que titulos longos quebravam o layout mobile —
problema invisivel com placeholder text.

## Common Pitfalls

- **Pular para visual**: Ir direto para UI bonita sem resolver fluxo e IA resulta
  em interfaces atraentes mas confusas
- **Wireframes como mockups**: Wireframes com cor, tipografia final e imagens confundem
  stakeholders que focam no visual em vez da estrutura
- **Happy path only**: Projetar apenas o caminho feliz e garantir frustacao em producao
- **IA baseada em org chart**: Estruturar a navegacao pela estrutura interna da empresa
  em vez de pelo modelo mental do usuario
- **Lorem ipsum**: Placeholder text esconde problemas de conteudo. Use conteudo real
- **Fluxos sem contexto**: Projetar o fluxo sem considerar de onde o usuario vem e
  para onde vai depois
- **Validacao tardia**: Descobrir que a IA esta errada apos o visual estar pronto e
  exponencialmente mais caro

## Cross-References

- [strategy-layer.md](strategy-layer.md) — Estrategia que guia decisoes de UX
- [ui-layer.md](ui-layer.md) — Visual que se aplica sobre a estrutura de UX
- [prototyping-layer.md](prototyping-layer.md) — Prototipagem para validar fluxos
- [discovery-layer.md](discovery-layer.md) — Pesquisa que informa fluxos
- [usability-testing-framework.md](usability-testing-framework.md) — Validacao de fluxos com usuarios
- [malouf-service-design-framework.md](malouf-service-design-framework.md) — Fluxos no contexto de servico
