# Multi-Brand Design System

## Metadata
- **Autor**: Design Squad
- **Categoria**: Design Systems, Theming, Multi-Brand
- **Complexidade**: Alta
- **Aplicacao**: Design systems que precisam servir multiplas marcas com tokens semanticos
- **Ultima atualizacao**: 2026-03-06

## Concept

Multi-Brand Design System e a arquitetura que permite que um unico conjunto de componentes
sirva multiplas marcas visuais atraves de theming e tokens semanticos. Em vez de manter
N design systems para N marcas, a organizacao mantém 1 sistema de componentes com N temas
que expressam identidades visuais distintas.

A chave e a separacao entre estrutura (componentes com layout, comportamento e logica) e
aparencia (cores, tipografia, espacamento, border radius que definem a identidade visual).
Componentes sao brand-agnostic; tokens sao brand-specific.

A arquitetura usa tres camadas de tokens (global, alias, component) onde a camada de
alias tokens e onde as marcas se diferenciam. Cada marca tem seu conjunto de alias tokens
que mapeia para os mesmos component tokens, garantindo que o switch de marca nao requer
mudanca em nenhum componente.

## When to Use

- Quando a organizacao tem multiplos produtos com marcas distintas
- Quando se quer consolidar design systems fragmentados por marca
- Quando uma marca precisa de white-labeling ou customizacao por cliente
- Quando se planeja dark mode e outros temas visuais
- Quando o custo de manter multiplos design systems e insustentavel
- Quando se quer consistencia de UX entre marcas com identidades visuais diferentes

## How to Apply

### Arquitetura de Tokens para Multi-Brand

**Camada 1 — Global Tokens (compartilhados)**
Paleta universal disponivel para todas as marcas:
```
colors/
  blue-500: #3B82F6
  purple-500: #8B5CF6
  green-500: #22C55E
  ...
spacing/
  1: 4px
  2: 8px
  ...
```

**Camada 2 — Alias Tokens (por marca)**
Cada marca mapeia semantica para globais diferentes:

Brand A (corporativo):
```
color-action-primary: {blue-600}
color-action-secondary: {gray-700}
font-family-heading: "Inter"
border-radius-md: 8px
```

Brand B (jovem):
```
color-action-primary: {purple-500}
color-action-secondary: {pink-500}
font-family-heading: "Space Grotesk"
border-radius-md: 16px
```

**Camada 3 — Component Tokens (compartilhados)**
Componentes referenciam alias tokens (mesmos nomes para todas as marcas):
```
button-bg: {color-action-primary}
button-text: {color-text-on-primary}
button-radius: {border-radius-md}
button-font: {font-family-heading}
```

### Processo de Implementacao
1. **Audit de marcas**: Identifique o que e comum e o que e diferente entre marcas
2. **Defina global tokens**: Paleta universal que cobre todas as marcas
3. **Defina alias tokens por marca**: Mapeie semantica para cada marca
4. **Construa componentes brand-agnostic**: Referencie apenas alias/component tokens
5. **Implemente theme switching**: Mecanismo para trocar alias tokens em runtime
6. **Valide cada marca**: Teste todos os componentes com cada tema aplicado
7. **Documente por marca**: Guidelines de uso especificas por identidade visual

### Mecanismo de Override
Para casos onde um componente precisa de ajuste especifico por marca:
1. Priorize ajuste via tokens (99% dos casos)
2. Se tokens nao bastam, use component variants brand-specific
3. Se variant nao basta, crie componente brand-specific (ultimo recurso)
4. Documente todo override com justificativa

### Gestao de Complexidade
1. Mantenha uma "compatibility matrix": quais componentes sao testados com quais marcas
2. Visual regression tests rodam para TODAS as marcas a cada PR
3. Defina um "reference brand" que e o padrao de desenvolvimento
4. Outras marcas sao validadas via testes automatizados e spot checks
5. Cada marca tem um owner que valida identidade visual

## Key Principles

- **Estrutura compartilhada, aparencia diferenciada**: Componentes sao os mesmos, tokens mudam
- **Alias layer e o ponto de articulacao**: Toda diferenciacao entre marcas vive nos alias tokens
- **Componentes nunca referenciam globais diretamente**: Indirection e obrigatoria
- **Teste em todas as marcas**: Um PR que funciona em Brand A pode quebrar em Brand B
- **Override como excecao**: Ajustes brand-specific devem ser raros e documentados
- **Custo-beneficio**: Multi-brand so vale se ha 2+ marcas com volume significativo
- **Identidade preservada**: Cada marca deve parecer unica, nao "a mesma coisa com cores diferentes"

## Examples

### Exemplo 1 — White-Label SaaS
Uma plataforma SaaS serve 50 clientes, cada um com sua marca:
- Global tokens: 200 valores primitivos
- Alias tokens: 80 tokens semanticos, 50 conjuntos (1 por cliente)
- Componentes: 45 componentes brand-agnostic
- Override: 3 componentes com variantes client-specific (header, footer, login)
- Resultado: 50 marcas visuais distintas com 1 codebase de componentes

### Exemplo 2 — Holding com 3 Marcas
Uma holding com 3 produtos (premium, mid-market, budget):
- Componentes compartilhados: 100% dos componentes base
- Diferenciacao: cores, tipografia, border-radius, spacing scale
- Premium: tipografia serif, cores dark, border-radius sutil, spacing amplo
- Budget: tipografia sans bold, cores vibrantes, border-radius arredondado, spacing compact
- Build time: 1 design system vs 3 = economia de 60% em manutencao

### Exemplo 3 — Dark Mode como "Marca"
Dark mode tratado como um tema adicional:
- Light theme: alias tokens com cores claras de fundo, escuras de texto
- Dark theme: alias tokens com cores escuras de fundo, claras de texto
- Componentes: zero mudancas, apenas swap de alias tokens
- Implementacao: CSS custom properties com media query `prefers-color-scheme`

## Common Pitfalls

- **Lowest common denominator**: Simplificar componentes demais para funcionar em todas
  as marcas perde a identidade de cada uma
- **Token explosion**: Criar alias tokens demais "por via das dudas" gera complexidade
  sem uso. Comece com o minimo e expanda conforme necessidade
- **Testar so uma marca**: Bug que so aparece com o tema de Brand B vai para producao
- **Override sem documentacao**: Excepcoes nao documentadas viram pontos cegos
- **Identidade diluida**: Se todas as marcas parecem iguais "com cores diferentes",
  o theming esta superficial demais
- **Complexity creep**: Cada nova marca adiciona complexidade. Avalie se realmente precisa
  de multi-brand ou se marcas separadas sao mais simples
- **Sem reference brand**: Sem uma marca "padrao", devs nao sabem em qual contexto testar

## Cross-References

- [design-token-architecture.md](design-token-architecture.md) — Arquitetura de tokens em detalhe
- [design-system-layer.md](design-system-layer.md) — DS como infraestrutura compartilhada
- [ui-layer.md](ui-layer.md) — Decisoes visuais por marca
- [cross-platform-design-framework.md](cross-platform-design-framework.md) — Multi-brand + multi-platform
- [component-spec-framework.md](component-spec-framework.md) — Specs brand-agnostic
- [frost-atomic-design-methodology.md](frost-atomic-design-methodology.md) — Componentes como building blocks
