# UI Layer

## Metadata
- **Autor**: Design Squad
- **Categoria**: Stack Layer, UI Design, Visual Design
- **Complexidade**: Media
- **Aplicacao**: Definicao de UI system, identidade visual e componentes de interface
- **Ultima atualizacao**: 2026-03-06

## Concept

A UI Layer e a quarta camada do stack de design, onde a estrutura de UX recebe tratamento
visual. Aqui sao definidos o sistema visual, a identidade de interface, componentes de UI
e a linguagem estetica do produto.

Esta camada transforma wireframes em interfaces concretas, aplicando cores, tipografia,
iconografia, espacamentos, sombras, animacoes e todo o vocabulario visual que da
personalidade e usabilidade ao produto.

O trabalho de UI nao e decoracao — e comunicacao. Cada decisao visual (cor, peso, tamanho,
contraste) comunica hierarquia, importancia, estado e relacao. Um botao primario e visualmente
distinto de um secundario nao por estetica, mas porque o usuario precisa distingui-los
instantaneamente.

## When to Use

- Apos a definicao de fluxos, IA e wireframes na camada de UX
- Quando se estabelece ou evolui a identidade visual do produto
- Quando se constroi o visual do design system
- Quando se precisa traduzir brand guidelines para interface
- Quando inconsistencias visuais precisam ser resolvidas
- Quando novos componentes precisam de tratamento visual

## How to Apply

### Dimensao 1 — UI System Foundations
1. **Color system**: Primarias, secundarias, neutras, semanticas (success, error, warning, info)
   - Defina paleta com pelo menos 5 tonalidades por cor
   - Garanta contraste WCAG AA em todas as combinacoes texto/fundo
   - Crie color tokens semanticos (background, surface, text, border)
2. **Typography system**: Familias, pesos, tamanhos, line-heights
   - Defina escala tipografica (6-8 tamanhos e suficiente)
   - Garanta legibilidade minima de 16px para body text
   - Defina headings, body, caption, label, code
3. **Spacing system**: Grid e escala de espacamentos
   - Use base consistente (4px ou 8px)
   - Defina escala: 4, 8, 12, 16, 24, 32, 48, 64, 96
   - Aplique para paddings, margins, gaps
4. **Elevation system**: Sombras e profundidade
   - 3-5 niveis de elevacao e suficiente
   - Use para comunicar hierarquia e sobreposicao
5. **Border radius, opacity, transitions**: Defina tokens para consistencia

### Dimensao 2 — Componentes Visuais
1. Aplique foundations em cada componente do sistema
2. Defina visual para todos os estados: default, hover, active, focus, disabled
3. Garanta que estados focados sejam visiveis para keyboard navigation
4. Crie variantes de density: compact, default, comfortable
5. Documente specs visuais: cores usadas, espacamentos, tamanhos

### Dimensao 3 — Iconografia e Ilustracoes
1. Escolha ou crie um icon set consistente
2. Defina grid de icones (24x24, 20x20, 16x16)
3. Defina estilo: outlined, filled, rounded
4. Garanta que icones tenham labels de texto associados (a11y)
5. Para ilustracoes: defina estilo e nivel de detalhe consistente

### Dimensao 4 — Motion e Micro-interactions
1. Defina principios de motion: duration, easing, purpose
2. Categorize: transitions (navegacao), feedback (acoes), decorative
3. Duracao sugerida: micro (100-200ms), medium (200-400ms), macro (400-700ms)
4. Easing: ease-out para entradas, ease-in para saidas
5. Respeite `prefers-reduced-motion` para acessibilidade

### Dimensao 5 — Responsive e Adaptive
1. Defina breakpoints: mobile (< 768px), tablet (768-1024px), desktop (> 1024px)
2. Decida o que adapta: layout, tamanho, visibilidade, interacao
3. Mobile-first: projete a partir da menor tela
4. Teste em dispositivos reais, nao apenas em resize de browser

## Key Principles

- **Visual e comunicacao**: Cada decisao visual comunica algo para o usuario
- **Sistema sobre estilo individual**: Decisoes visuais sistematicas escalam
- **Acessibilidade e baseline**: Contraste, foco visivel e reduced motion nao sao opcionais
- **Tokens sao a lingua**: Design tokens codificam decisoes visuais em formato reutilizavel
- **Consistencia gera confianca**: Interfaces consistentes parecem mais confiaveis
- **Performance visual**: Menos variacao visual = menos carga cognitiva
- **Responsive e default**: Toda interface deve funcionar em multiplos tamanhos

## Examples

### Exemplo 1 — Color Token System
```
--color-primary-500: #2563EB    (cor principal)
--color-primary-600: #1D4ED8    (hover)
--color-primary-700: #1E40AF    (active)

Semanticos:
--color-bg-primary: var(--color-primary-500)
--color-text-on-primary: #FFFFFF
--color-border-default: var(--neutral-200)
```

### Exemplo 2 — Typography Scale
| Token        | Size  | Weight | Line-height | Uso               |
|--------------|-------|--------|-------------|-------------------|
| heading-xl   | 32px  | 700    | 40px        | Titulos de pagina |
| heading-lg   | 24px  | 700    | 32px        | Secoes            |
| heading-md   | 20px  | 600    | 28px        | Sub-secoes        |
| body-lg      | 18px  | 400    | 28px        | Texto destaque    |
| body-md      | 16px  | 400    | 24px        | Texto padrao      |
| body-sm      | 14px  | 400    | 20px        | Texto secundario  |
| caption      | 12px  | 400    | 16px        | Labels, metadata  |

### Exemplo 3 — UI Audit Resultado
Uma auditoria revelou no produto: 14 tons de cinza, 6 tamanhos de botao,
3 familias tipograficas. Apos sistematizacao: 5 tons de cinza (com tokens),
3 tamanhos de botao (sm, md, lg), 1 familia tipografica com 4 pesos.
Carga cognitiva visual reduziu mensuravel em testes A/B.

## Common Pitfalls

- **Estilo sem sistema**: Decisoes visuais ad-hoc criam inconsistencia invisivel
- **Ignorar acessibilidade**: Cores bonitas que falham em contraste excluem usuarios
- **Desktop-first**: Projetar para desktop e "adaptar" para mobile gera UX inferior
- **Over-design**: Mais sombras, gradientes e animacoes nao significam melhor UI
- **Tokens abstratos demais**: Se ninguem entende o nome do token, ninguem usa corretamente
- **Esquecer dark mode**: Retroencaixar dark mode e 10x mais custoso que projetar junto
- **Motion sem proposito**: Animacoes decorativas que nao comunicam nada sao distracao

## Cross-References

- [ux-layer.md](ux-layer.md) — Estrutura sobre a qual o visual se aplica
- [design-system-layer.md](design-system-layer.md) — Sistema que codifica decisoes de UI
- [design-token-architecture.md](design-token-architecture.md) — Arquitetura de tokens
- [frost-atomic-design-methodology.md](frost-atomic-design-methodology.md) — Componentes hierarquicos
- [accessibility-by-default.md](accessibility-by-default.md) — A11y nas decisoes visuais
- [multi-brand-design-system.md](multi-brand-design-system.md) — Theming visual multi-marca
