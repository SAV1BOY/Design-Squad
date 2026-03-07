# Design Motion Specs

## Metadata
- **Categoria:** UI
- **Complexidade:** Média-Alta
- **Tempo Estimado:** 3-5 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** ui, motion, animation, micro-interactions, transitions, easing

## Objective
Definir e documentar especificações de motion design para o produto: transições entre telas,
micro-interactions de componentes, easing curves e timing. As specs garantem consistência nas
animações, melhoram a percepção de performance e comunicam hierarquia e estado ao usuário.

## Prerequisites
- Mockups high-fidelity aprovados com estados de componentes
- Design system com tokens de motion definidos (ou necessidade de criá-los)
- Protótipos interativos como referência de intenção de interação
- Ferramenta de motion design configurada (Figma, ProtoPie, After Effects, Lottie)
- Conhecimento das capacidades de animação do framework frontend (CSS, Framer Motion, GSAP)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UI Designer / Motion Designer | Criar animações, definir timing e documentar specs |
| Design System Lead | Integrar motion tokens ao design system |
| Frontend Engineer | Validar viabilidade e performance das animações |
| A11y Specialist | Garantir que motion respeita prefers-reduced-motion |
| Design Lead | Revisar consistência e aprovar motion language |

## Frameworks
- **Motion Principles** — purposeful, quick, natural (não decorativo)
- **Easing Curves** — ease-in-out, ease-out, spring physics
- **Duration Scale** — micro (100-200ms), small (200-300ms), medium (300-500ms), large (500ms+)
- **Material Motion** — container transform, shared axis, fade through, cross-fade
- **prefers-reduced-motion** — respeitar preferência de acessibilidade do usuário

## Checklists
- [ ] Princípios de motion do produto documentados
- [ ] Duration scale definida com valores para cada categoria
- [ ] Easing curves padrão definidas e nomeadas
- [ ] Micro-interactions de componentes especificadas (hover, click, toggle)
- [ ] Transições entre telas definidas (navigation, modal, drawer)
- [ ] Loading animations e skeleton screens especificados
- [ ] Feedback animations documentados (success, error, progress)
- [ ] prefers-reduced-motion alternativas definidas
- [ ] Motion specs revisados por Frontend Engineer
- [ ] Exemplos exportados (vídeo, Lottie, ou protótipo)

## Steps
1. **Definir motion principles** — Articular 3-5 princípios que guiam todas as animações do
   produto. Exemplo: "Toda animação serve a um propósito funcional, nunca apenas decorativo."

2. **Criar duration scale** — Definir categorias de duração com valores específicos: micro
   (150ms), small (250ms), medium (400ms), large (600ms). Contextualizar uso de cada.

3. **Definir easing curves** — Selecionar 3-4 curvas padrão: ease-out (entradas), ease-in-out
   (transições), spring (elementos interativos). Fornecer valores cubic-bezier.

4. **Especificar micro-interactions** — Para cada componente interativo, documentar: trigger,
   propriedade animada, duração, easing e valor inicial/final.

5. **Projetar transições de navegação** — Definir como telas transicionam: push, fade, shared
   element. Documentar por tipo de navegação (forward, back, modal, drawer).

6. **Criar loading animations** — Especificar skeleton screens, spinners e progress indicators.
   Garantir que comunicam progresso e reduzem percepção de espera.

7. **Definir alternativas reduced-motion** — Para cada animação, documentar a alternativa quando
   prefers-reduced-motion está ativada: fade instantâneo, sem animação ou versão simplificada.

8. **Produzir exemplos visuais** — Criar protótipos em ProtoPie, vídeos de referência ou
   exports Lottie que demonstrem cada animação especificada.

9. **Revisar com eng** — Apresentar specs para Frontend Engineer. Validar performance,
   viabilidade no framework e impacto em bundle size.

## Output
- **Motion Spec Document** — Documento com principles, tokens, specs por componente e transição
- **Motion Token Set** — Valores de duration e easing exportáveis (JSON/CSS)
- **Reference Videos/Prototypes** — Exemplos visuais de cada animação
- **Formato:** Markdown + Figma/ProtoPie + vídeo/Lottie exports
- **Nomenclatura:** `motion-specs-[produto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UI Designer / Motion Designer |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Uma vez (foundation), atualizações por componente |
| Aprovadores | Design Lead, DS Lead |
| Repositório | `/squads/design/tasks/ui/` |

## Cross-References
- [Build Prototype](./build-prototype.md)
- [Create or Update Tokens](../design-system/create-or-update-tokens.md)
- [Create Component Spec](../design-system/create-component-spec.md)
- [Dev Handoff](../handoff/dev-handoff.md)
- [A11y Audit](../accessibility/a11y-audit.md)
