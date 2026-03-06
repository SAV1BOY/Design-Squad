# Atomic Design

## Metadata

- **Origem:** Brad Frost (2013)
- **Categoria:** Design System Architecture
- **Complexidade:** Intermediaria a Avancada
- **Aplicacao:** Construcao de design systems, component libraries e interfaces escalaveis
- **Tags:** atoms, molecules, organisms, templates, pages, design-systems, components

## Concept

Atomic Design e uma metodologia para criar design systems de forma hierarquica e modular,
inspirada na quimica. Brad Frost propoe cinco niveis de composicao: Atoms, Molecules,
Organisms, Templates e Pages. Cada nivel combina elementos do nivel anterior para criar
componentes progressivamente mais complexos e contextualizados.

A metafora quimica e poderosa: assim como atomos se combinam em moleculas que formam
organismos, elementos basicos de interface (cores, tipografia, botoes) se combinam em
componentes (campo de busca) que formam secoes (header) e, eventualmente, paginas
completas. Essa abordagem bottom-up garante consistencia e reusabilidade em escala.

O valor real do Atomic Design nao esta apenas na taxonomia, mas na mudanca de mentalidade.
Em vez de projetar paginas isoladas, equipes passam a projetar sistemas de componentes.
Isso acelera o desenvolvimento, facilita manutencao e garante coerencia visual e funcional
em todo o produto, independente de quantas telas existam.

## When to Use

- Ao construir ou reestruturar um design system do zero
- Quando multiplas equipes precisam compartilhar componentes de forma consistente
- Em projetos de grande escala com muitas telas e variacoes de interface
- Para documentar e organizar component libraries existentes
- Quando ha necessidade de escalar design e desenvolvimento simultaneamente

## How to Apply

1. **Defina os Atoms:** Identifique os elementos mais basicos e indivisiveis da interface —
   cores, tipografia, espacamento, icones, botoes basicos, inputs, labels. Documente cada
   atomo com suas variacoes e estados (hover, active, disabled, error).

2. **Combine em Molecules:** Agrupe atomos em componentes funcionais simples. Um campo de
   busca (input + botao + label) e uma molecula. Um card basico (imagem + titulo +
   descricao) e outra. Cada molecula deve ter uma unica responsabilidade clara.

3. **Monte Organisms:** Combine moleculas e atomos em secoes de interface distintas. Um
   header (logo + navegacao + campo de busca + avatar) e um organismo. Um product listing
   (grid de cards + filtros + paginacao) e outro. Organismos sao os blocos que compoem
   layouts completos.

4. **Estruture Templates:** Crie layouts que posicionam organismos na pagina usando
   placeholder content. Templates definem a estrutura e hierarquia da informacao sem
   conteudo real. Sao o esqueleto da pagina, mostrando proporcoes e relacoes espaciais.

5. **Instancie Pages:** Aplique conteudo real aos templates para criar instancias
   especificas. Pages revelam como o design se comporta com dados reais — textos longos,
   imagens variadas, estados vazios, edge cases e conteudo em diferentes idiomas.

6. **Mantenha documentacao viva:** Use ferramentas como Storybook ou ZeroHeight para
   documentar cada nivel com exemplos interativos, guidelines de uso, props aceitas
   e variacoes documentadas com codigo.

## Key Principles

- **Composicao hierarquica:** Cada nivel e construido a partir do anterior. Mudancas em
  atomos propagam automaticamente para moleculas, organismos, templates e pages.

- **Responsabilidade unica:** Cada componente deve fazer uma coisa bem feita. Moleculas
  nao devem tentar ser organismos. Mantenha componentes focados e reutilizaveis.

- **Context-agnostic na base:** Atoms e molecules devem ser genericos o suficiente para
  funcionar em diferentes contextos. Contexto especifico e adicionado nos niveis de
  organism e acima.

- **Conteudo real valida o design:** Somente no nivel de pages, com conteudo real, e
  possivel validar se o sistema funciona. Nao confie apenas em lorem ipsum e imagens
  perfeitas que escondem problemas de layout.

- **Sistema sobre paginas:** Pense em sistemas de componentes, nao em paginas isoladas.
  Um botao bem projetado serve centenas de contextos. Uma pagina bem projetada serve
  apenas um unico cenario.

## Examples

### Design System de E-commerce
Atoms: cores da marca, tipografia (headings, body, captions), botoes (primary, secondary,
ghost), inputs, badges, icones. Molecules: product card (imagem + titulo + preco + rating),
search bar (input + botao + icone), breadcrumb. Organisms: product grid (cards + filtros +
sort + paginacao), checkout form (dados pessoais + endereco + pagamento). Templates: PDP
layout, PLP layout, checkout layout. Pages: instancias com produtos reais, incluindo
edge cases como nomes longos e imagens verticais.

### App de Gestao de Projetos
Atoms: avatares, status badges (to-do, in-progress, done), timestamps, priority tags.
Molecules: task card (titulo + assignee + status + due date), comment block (avatar +
nome + texto + timestamp). Organisms: task board column (header + lista de task cards +
add button), activity feed (lista de comment blocks). A estrutura permitiu que tres squads
diferentes construissem features usando o mesmo vocabulario visual e os mesmos componentes.

### Plataforma Educacional
Atoms incluiam elementos especificos do dominio: progress indicators, difficulty badges,
duration labels. Molecules como lesson card e quiz question combinavam atomos de forma
padronizada. O sistema permitiu escalar de 50 para 500 cursos mantendo consistencia
visual completa sem redesign manual de cada pagina.

## Common Pitfalls

- **Over-engineering na base:** Criar atomos excessivamente configuraveis com dezenas de
  props gera complexidade desnecessaria. Comece simples e adicione variacoes conforme a
  demanda real aparece no produto.

- **Nomenclatura inconsistente:** Se a equipe de design chama "card" e a engenharia chama
  "tile", o sistema quebra na comunicacao. Alinhe vocabulario entre design e desenvolvimento
  desde o inicio do projeto.

- **Ignorar estados e edge cases:** Documentar apenas o happy path (estado default) e
  insuficiente. Cada componente precisa de estados: loading, empty, error, disabled,
  hover, focus, e variacoes de conteudo (texto longo, texto curto, sem imagem).

- **Rigidez excessiva na hierarquia:** A metafora quimica e util, mas nao deve ser uma
  camisa de forca. Alguns componentes nao se encaixam perfeitamente em um unico nivel.
  Pragmatismo sobre purismo taxonomico.

## Cross-References

- [Gestalt Principles](gestalt-principles.md) — Fundamentam decisoes de agrupamento e
  hierarquia visual na composicao de componentes
- [Interaction Design Principles](interaction-design-principles.md) — Guiam o comportamento
  interativo de cada componente em todos os niveis
- [Information Architecture Toolkit](information-architecture-toolkit.md) — Informa a
  estrutura de templates e organizacao de organismos na pagina
- [Nielsen Heuristics](nielsen-heuristics.md) — Criterios de avaliacao aplicaveis a
  componentes em todos os niveis do sistema
- [Design Thinking](design-thinking.md) — Processo para identificar necessidades dos
  usuarios que o design system deve atender
