# Design System Layer

## Metadata
- **Autor**: Design Squad
- **Categoria**: Stack Layer, Design Systems
- **Complexidade**: Alta
- **Aplicacao**: Camada de tokens, componentes, padroes e documentacao do design system
- **Ultima atualizacao**: 2026-03-06

## Concept

A Design System Layer e a quinta camada do stack de design, onde decisoes visuais e de UX
sao codificadas em artefatos reutilizaveis: tokens, componentes, padroes compostos e
documentacao. Esta camada e o que normalmente se chama de "design system" — a infraestrutura
compartilhada que permite que multiplas equipes construam interfaces consistentes.

O design system nao e um projeto — e um produto que serve outros produtos. Ele precisa de
estrategia, roadmap, governanca e manutencao continua, assim como qualquer produto.

A camada funciona em tres niveis: tokens (decisoes atomicas de design), componentes
(elementos de UI reutilizaveis) e patterns (combinacoes de componentes que resolvem
problemas recorrentes).

## When to Use

- Quando multiplas equipes constroem interfaces no mesmo ecossistema de produto
- Quando inconsistencias visuais e funcionais sao frequentes
- Quando o tempo de desenvolvimento de UI e desproporcionalmente alto
- Quando se precisa de linguagem compartilhada entre design e desenvolvimento
- Quando a organizacao escala e precisa manter qualidade de interface
- Quando se planeja suportar multiplas plataformas com mesma experiencia

## How to Apply

### Nivel 1 — Design Tokens
1. **Global tokens**: Valores primitivos (cores hex, tamanhos em px, font families)
2. **Alias tokens**: Significado atribuido (primary-color, body-font-size)
3. **Component tokens**: Especificos de componente (button-bg, input-border-color)
4. Implemente tokens em formato consumivel (JSON, CSS custom properties, etc.)
5. Sincronize tokens entre design tool (Figma) e codigo

### Nivel 2 — Componentes
1. Defina a biblioteca core: os 15-25 componentes mais usados
   - Button, Input, Select, Checkbox, Radio, Toggle
   - Card, Modal, Toast, Tooltip, Popover
   - Table, Tabs, Accordion, Breadcrumb, Pagination
   - Badge, Avatar, Tag, Skeleton, Spinner
2. Para cada componente, defina:
   - Anatomy: partes que compoem o componente
   - Props: propriedades configuráveis
   - States: default, hover, active, focus, disabled, loading, error
   - Variants: tamanhos, estilos, densidades
   - Behavior: como reage a interacao e resize
3. Implemente em codigo com testes (unit + visual regression + a11y)
4. Documente com exemplos vivos (Storybook ou equivalente)

### Nivel 3 — Patterns (Padroes Compostos)
1. Identifique combinacoes recorrentes de componentes:
   - Form patterns: login, signup, search, filters
   - Layout patterns: sidebar, header/content/footer, dashboard grid
   - Data patterns: table with filters, list with pagination, detail view
   - Feedback patterns: empty state, error state, loading state, success
2. Documente cada pattern com: quando usar, composicao, variantes
3. Nao crie componentes para patterns — documente a composicao correta

### Nivel 4 — Documentacao
1. **Getting started**: Como instalar e configurar o design system
2. **Foundations**: Tokens, cores, tipografia, espacamento, grid
3. **Components**: Cada componente com API, exemplos e guidelines
4. **Patterns**: Composicoes recomendadas com codigo
5. **Contributing**: Como propor e implementar novos componentes
6. **Changelog**: Historico de mudancas por versao
7. **Migration guides**: Como migrar entre versoes major

## Key Principles

- **Single source of truth**: Uma unica fonte de verdade para cada decisao de design
- **Consumo facil**: Se e dificil de usar, nao sera usado. DX e prioridade
- **Documentacao como feature**: Componente sem documentacao nao existe
- **Versionamento semantico**: Consumidores precisam confiar na estabilidade
- **Tokens como fundacao**: Tudo começa nos tokens — mudou o token, mudou tudo
- **Acessibilidade built-in**: Componentes devem ser acessiveis por padrao
- **Evolucao governada**: Mudancas seguem processo claro e comunicado

## Examples

### Exemplo 1 — Estrutura de Design System
```
design-system/
  tokens/
    global.json          # cores hex, sizes px
    alias.json           # semanticos (primary, bg)
    component.json       # por componente
  components/
    Button/
      Button.tsx
      Button.styles.ts
      Button.test.tsx
      Button.stories.tsx
      Button.docs.mdx
    Input/
      ...
  patterns/
    LoginForm.docs.mdx
    EmptyState.docs.mdx
  docs/
    getting-started.md
    contributing.md
    changelog.md
```

### Exemplo 2 — Metricas de Sucesso
Um design system maduro media:
- 87% de cobertura (% de componentes em producao vindos do DS)
- 234 componentes totais, 12 deprecated, 8 em beta
- NPS 72 com consumidores (survey trimestral)
- 11 dias de RFC a release para novos componentes
- 0 breaking changes nao comunicadas nos ultimos 6 meses

### Exemplo 3 — Adocao Incremental
Uma equipe lancou o DS com foco em 3 componentes: Button, Input, Card.
Esses 3 cobriam 40% do uso de UI no produto principal. Em 3 meses,
expandiram para 15 componentes cobrindo 75%. Em 6 meses, 25 componentes
cobrindo 90%. A estrategia de foco nos mais usados maximizou ROI precoce.

## Common Pitfalls

- **Construir sem consumidor**: DS criado em abstrato sem equipes consumidoras validando
- **Documentacao como afterthought**: Sem docs, equipes nao adotam. Docs e parte do componente
- **Excesso de abstração**: Componentes genéricos demais sao dificeis de usar. Equilibre
  flexibilidade com opiniao
- **Token hell**: Tokens demais com nomes crípticos confundem. Mantenha simples
- **Ignorar DX**: API confusa, instalacao complicada, types ruins = baixa adocao
- **One-size-fits-all**: Nem todo produto precisa de todos os componentes. Permita tree-shaking
- **Nao medir**: Sem metricas de cobertura e satisfacao, nao ha como priorizar

## Cross-References

- [design-token-architecture.md](design-token-architecture.md) — Arquitetura detalhada de tokens
- [component-spec-framework.md](component-spec-framework.md) — Spec detalhada de componentes
- [frost-atomic-design-methodology.md](frost-atomic-design-methodology.md) — Hierarquia de componentes
- [frost-maintaining-design-systems.md](frost-maintaining-design-systems.md) — Manutencao do sistema
- [mall-design-system-strategy.md](mall-design-system-strategy.md) — Estrategia do sistema
- [ui-layer.md](ui-layer.md) — Decisoes visuais que alimentam o sistema
