# Create or Update Tokens

## Metadata
- **Categoria:** Design System
- **Complexidade:** Alta
- **Tempo Estimado:** 3-8 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** design-system, tokens, variables, theming, foundations

## Objective
Criar ou atualizar design tokens que formam a base do design system: cores, tipografia,
espaçamento, elevação, border radius, motion e breakpoints. Os tokens garantem consistência
visual cross-platform e habilitam theming (light/dark mode, white-labeling).

## Prerequisites
- Decisões de visual design aprovadas (paleta, tipografia, escala)
- Ferramenta de design com suporte a variables (Figma Variables)
- Pipeline de token export configurado (Style Dictionary, Tokens Studio ou equivalente)
- Nomenclatura de tokens definida ou a definir nesta task
- Inventário de valores atuais em uso no produto (se update)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design System Lead | Definir arquitetura de tokens, naming e governança |
| UI Designer | Contribuir com decisões de valor e testar aplicação visual |
| Frontend Engineer | Configurar pipeline de export e validar consumo no código |
| Design Lead | Aprovar arquitetura e naming convention |
| A11y Specialist | Validar tokens de cor e tipografia contra WCAG |

## Frameworks
- **Token Architecture (3 tiers)** — global/primitive, alias/semantic, component-specific
- **Naming Convention** — `category-property-variant-state` (ex: color-text-primary-default)
- **Style Dictionary** — pipeline de transformação de tokens para múltiplas plataformas
- **Figma Variables** — gerenciamento de tokens no Figma com collections e modes
- **Token Taxonomy** — classificação por: color, typography, spacing, sizing, elevation, motion

## Checklists
- [ ] Arquitetura de 3 tiers definida (global, alias, component)
- [ ] Naming convention documentada e aprovada
- [ ] Color tokens criados: primitive + semantic (background, text, border, surface)
- [ ] Typography tokens definidos: font-family, size scale, weight, line-height
- [ ] Spacing tokens definidos com escala consistente (4px ou 8px base)
- [ ] Elevation tokens definidos (shadow values por nível)
- [ ] Border radius tokens criados com escala
- [ ] Motion tokens incluídos (duration, easing)
- [ ] Figma Variables configurados com collections e modes
- [ ] Pipeline de export testado e gerando output correto (CSS, JSON, iOS, Android)

## Steps
1. **Auditar valores atuais** — Se update, inventariar todos os valores de cor, tipo, spacing
   atualmente em uso. Identificar valores hardcoded que precisam migrar para tokens.

2. **Definir arquitetura de tiers** — Estabelecer 3 níveis: primitives (valores raw),
   semantic/alias (significado contextual), component-specific (uso em componente).

3. **Criar naming convention** — Definir padrão de nomenclatura: `category.property.variant.state`.
   Documentar com exemplos para cada categoria de token.

4. **Definir color tokens** — Criar: primitives (blue-500, gray-100), semantics (color-bg-primary,
   color-text-secondary), component (button-bg-default, input-border-error).

5. **Definir typography tokens** — Estabelecer: font families, type scale (8-10 sizes), weights,
   line-heights e letter-spacing. Agrupar em text styles compostos.

6. **Definir spacing e sizing** — Criar escala de spacing (4, 8, 12, 16, 24, 32, 48, 64, 96)
   e sizing tokens para componentes (icon sizes, avatar sizes, etc.).

7. **Definir elevation e outros** — Criar tokens de: shadow (5 níveis), border-radius (4-5
   valores), border-width e opacity. Incluir motion tokens (duration, easing).

8. **Configurar Figma Variables** — Implementar tokens como Figma Variables organizados em
   collections (primitives, semantics). Configurar modes para light/dark.

9. **Configurar pipeline de export** — Montar pipeline com Style Dictionary ou Tokens Studio
   para gerar output em CSS custom properties, JSON, iOS (Swift) e Android (Kotlin).

10. **Validar e documentar** — Testar tokens aplicados em componentes reais. Validar acessibilidade
    de cores. Documentar catálogo completo de tokens com valores e uso.

## Output
- **Token Catalog** — Documentação completa de todos os tokens com valores e uso
- **Figma Variables** — Collections configuradas no Figma com modes
- **Token Export Files** — CSS, JSON, Swift, Kotlin outputs via pipeline
- **Formato:** Figma + JSON/CSS exports + Markdown documentation
- **Nomenclatura:** `design-tokens-[produto]-v[X.Y]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design System Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Setup + atualização por ciclo de release do DS |
| Aprovadores | Design Lead, Frontend Lead |
| Repositório | `/squads/design/tasks/design-system/` |

## Cross-References
- [Design Dark Mode](../ui/design-dark-mode.md)
- [Create Component Spec](./create-component-spec.md)
- [Publish Library](./publish-library.md)
- [Design Motion Specs](../ui/design-motion-specs.md)
- [Component Inventory](./component-inventory.md)
- [DS Health Check](./ds-health-check.md)
