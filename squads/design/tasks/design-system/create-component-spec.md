# Create Component Spec

## Metadata
- **Categoria:** Design System
- **Complexidade:** Alta
- **Tempo Estimado:** 3-5 dias por componente
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** design-system, component, spec, documentation, api

## Objective
Projetar e documentar a especificação completa de um componente do design system: anatomia,
variantes, estados, propriedades (API), tokens utilizados, comportamento responsivo, acessibilidade
e guidelines de uso. A spec serve como contrato entre design e engenharia.

## Prerequisites
- Necessidade do componente validada (uso em 2+ contextos ou projeto)
- Design tokens atualizados e disponíveis
- Component inventory existente para verificar duplicações
- Padrões de acessibilidade (ARIA patterns) identificados
- Figma component library configurada e acessível

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design System Lead | Projetar componente, definir API e redigir spec |
| UI Designer | Contribuir com design visual e validar em contexto |
| Frontend Engineer | Revisar viabilidade técnica e API de props |
| A11y Specialist | Definir ARIA pattern, keyboard interaction e screen reader |
| Content Designer | Redigir guidelines de conteúdo para o componente |

## Frameworks
- **Atomic Design** — classificar componente como atom, molecule ou organism
- **Component API Design** — props, variants, slots, events
- **ARIA Authoring Practices** — padrões de acessibilidade por tipo de componente
- **Component Anatomy** — decomposição visual em partes nomeadas
- **Usage Guidelines (Do/Don't)** — exemplos de uso correto e incorreto

## Checklists
- [ ] Necessidade validada e nome do componente definido
- [ ] Anatomia documentada com partes nomeadas
- [ ] Todas as variantes definidas (size, type, style)
- [ ] Todos os estados desenhados (default, hover, active, focused, disabled, error)
- [ ] Props/API documentadas com tipo, valores e defaults
- [ ] Tokens utilizados mapeados (color, spacing, typography, elevation)
- [ ] Comportamento responsive especificado
- [ ] ARIA pattern e keyboard interactions definidos
- [ ] Guidelines de uso com Do/Don't criados
- [ ] Spec revisada por Frontend Engineer e A11y Specialist

## Steps
1. **Validar necessidade** — Verificar que o componente é necessário (usado em 2+ contextos).
   Confirmar que não existe componente similar no DS que possa ser estendido.

2. **Pesquisar padrões existentes** — Revisar como outros design systems (Material, Carbon,
   Polaris) implementam o mesmo componente. Identificar best practices e ARIA patterns.

3. **Definir anatomia** — Decompor o componente em partes nomeadas: container, label, icon,
   content, action, etc. Criar diagrama visual de anatomia.

4. **Projetar variantes** — Definir eixos de variação: size (sm, md, lg), type/kind (primary,
   secondary), style (filled, outlined). Desenhar cada combinação relevante.

5. **Desenhar estados** — Para cada variante, criar: default, hover, active/pressed, focused,
   disabled, loading, error e success (conforme aplicável ao componente).

6. **Definir API (props)** — Documentar cada prop: nome, tipo, valores possíveis, default,
   se é required. Incluir slots para conteúdo customizável e events emitidos.

7. **Especificar acessibilidade** — Definir: role ARIA, atributos (aria-label, aria-expanded),
   keyboard interactions (Tab, Enter, Escape, Arrow keys) e screen reader behavior.

8. **Criar guidelines de uso** — Redigir: quando usar, quando não usar, combinações com outros
   componentes, guidelines de conteúdo (label length, tone) e Do/Don't visuais.

9. **Construir no Figma** — Criar componente no Figma com: auto-layout, variants, component
   properties (boolean, text, instance swap) e slots. Testar com content extremes.

10. **Review e publicação** — Apresentar spec para Frontend Engineer e A11y Specialist. Incorporar
    feedback técnico e publicar spec no site de documentação do DS.

## Output
- **Component Spec Document** — Especificação completa: anatomia, API, estados, a11y, guidelines
- **Figma Component** — Componente construído com variants e properties
- **ARIA Spec** — Detalhamento de acessibilidade e keyboard interactions
- **Formato:** Figma + Markdown (spec) + site de documentação do DS
- **Nomenclatura:** `component-spec-[nome-componente]-v[X.Y]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design System Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por componente novo ou major update |
| Aprovadores | Design Lead, Frontend Lead, A11y Specialist |
| Repositório | `/squads/design/tasks/design-system/` |

## Cross-References
- [Component Inventory](./component-inventory.md)
- [Create or Update Tokens](./create-or-update-tokens.md)
- [Publish Library](./publish-library.md)
- [DS Contribution Review](./ds-contribution-review.md)
- [A11y Audit](../accessibility/a11y-audit.md)
- [Dev Handoff](../handoff/dev-handoff.md)
