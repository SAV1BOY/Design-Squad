# Design Responsive Layouts

## Metadata
- **Categoria:** UI
- **Complexidade:** Média-Alta
- **Tempo Estimado:** 3-5 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** ui, responsive, layout, breakpoints, mobile-first, adaptive

## Objective
Projetar layouts responsivos que garantam experiência consistente e otimizada em todos os
dispositivos e tamanhos de tela. O trabalho define como componentes, grids e conteúdo se adaptam
entre breakpoints, documentando regras claras para implementação.

## Prerequisites
- Mockups high-fidelity aprovados para pelo menos um breakpoint
- Grid system e breakpoints definidos no design system
- Inventário de componentes responsivos do DS
- Dados de analytics sobre dispositivos e resoluções dos usuários
- Ferramenta de design com suporte a auto-layout (Figma)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UI Designer | Criar variações responsive e documentar comportamentos |
| Design Lead | Revisar consistência e aderência aos padrões do DS |
| Frontend Engineer | Validar viabilidade CSS/layout e anteciprar edge cases |
| UX Designer | Garantir que a experiência é preservada em todos os breakpoints |

## Frameworks
- **Mobile-First Design** — projetar para mobile e expandir para desktop
- **Fluid Grid System** — colunas flexíveis com gutters proporcionais
- **Container Queries** — adaptação baseada no container, não apenas viewport
- **Breakpoint Strategy** — mobile (360px), tablet (768px), desktop (1280px), wide (1440px+)
- **Content Priority Guide** — priorização de conteúdo por breakpoint

## Checklists
- [ ] Breakpoints oficiais definidos e documentados
- [ ] Grid system configurado para cada breakpoint (colunas, gutters, margens)
- [ ] Layout mobile projetado com priorização de conteúdo
- [ ] Transições entre breakpoints documentadas (o que muda e como)
- [ ] Componentes responsive validados (stack, reflow, hide/show)
- [ ] Imagens e media com estratégia de adaptação definida
- [ ] Touch targets mínimos verificados em mobile (44x44px)
- [ ] Tipografia responsiva configurada (fluid type ou scale por breakpoint)
- [ ] Review com Frontend Engineer executado
- [ ] Documentação de responsive behavior publicada

## Steps
1. **Definir breakpoints e grid** — Confirmar breakpoints oficiais com o DS. Configurar grid
   system para cada: número de colunas, gutter, margens laterais e max-width.

2. **Analisar dados de dispositivo** — Revisar analytics para entender distribuição de
   dispositivos e resoluções. Priorizar breakpoints com maior volume de uso.

3. **Projetar mobile-first** — Começar pelo breakpoint mobile, priorizando conteúdo essencial.
   Definir hierarquia e sequência de elementos para viewport estreita.

4. **Expandir para tablet** — Adaptar layout para tablet: reorganizar colunas, expandir
   componentes colapsados e ajustar espaçamento. Manter touch-friendly.

5. **Expandir para desktop** — Projetar layout completo para desktop: múltiplas colunas, sidebars,
   navegação expandida e aproveitamento de espaço horizontal.

6. **Documentar comportamento de componentes** — Para cada componente, especificar como se adapta:
   stack (empilhar), reflow (redistribuir), scale (redimensionar) ou hide/show.

7. **Configurar tipografia responsiva** — Definir escala tipográfica por breakpoint ou implementar
   fluid typography com clamp(). Testar legibilidade em todos os tamanhos.

8. **Validar com Frontend Engineer** — Apresentar layouts e comportamentos para eng. Confirmar
   viabilidade com CSS Grid, Flexbox e media queries disponíveis.

9. **Criar documentação de responsive specs** — Consolidar todas as regras em documento de
   referência: grid por breakpoint, comportamentos, exceções e exemplos visuais.

## Output
- **Responsive Mockups** — Variações completas para cada breakpoint oficial
- **Responsive Spec Document** — Regras de adaptação por componente e layout
- **Grid Spec** — Especificação detalhada do grid system por breakpoint
- **Formato:** Figma file + Markdown para specs
- **Nomenclatura:** `responsive-layouts-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UI Designer |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por projeto ou feature |
| Aprovadores | Design Lead, Frontend Engineer |
| Repositório | `/squads/design/tasks/ui/` |

## Cross-References
- [UI Design High Fidelity](./ui-design-high-fidelity.md)
- [Wireframe Pack](../ux/wireframe-pack.md)
- [Create Component Spec](../design-system/create-component-spec.md)
- [Dev Handoff](../handoff/dev-handoff.md)
- [Create or Update Tokens](../design-system/create-or-update-tokens.md)
