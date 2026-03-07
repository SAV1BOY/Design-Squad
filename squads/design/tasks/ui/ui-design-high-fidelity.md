# UI Design — High Fidelity

## Metadata
- **Categoria:** UI
- **Complexidade:** Alta
- **Tempo Estimado:** 5-15 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** ui, high-fidelity, visual-design, design-system, pixel-perfect

## Objective
Produzir interfaces de alta fidelidade que transformam wireframes aprovados em designs visuais
completos, aplicando o design system, definindo interações detalhadas e garantindo qualidade
pixel-perfect. Os mockups finais servem como referência definitiva para implementação.

## Prerequisites
- Wireframes aprovados e versionados
- Design system com tokens e componentes disponíveis
- User flows validados com estados de componentes documentados
- Content design (microcopy) definido para o fluxo
- Figma libraries do design system conectadas e atualizadas

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UI Designer | Criar mockups high-fidelity aplicando design system e visual design |
| Design Lead | Revisar qualidade visual, consistência e aderência ao DS |
| UX Designer | Validar que a intenção de UX foi preservada na tradução visual |
| Content Designer | Garantir que microcopy final está aplicado corretamente |
| Tech Lead | Antecipar questões de implementação e confirmar viabilidade |

## Frameworks
- **Design Tokens** — aplicação de cores, tipografia, espaçamento, elevação do DS
- **8pt Grid System** — grid base para alinhamento e espaçamento consistente
- **Component-Driven Design** — composição de interfaces a partir de componentes do DS
- **Visual Hierarchy** — tamanho, cor, peso e posição para guiar o olhar do usuário
- **Atomic Design** — atoms, molecules, organisms, templates, pages

## Checklists
- [ ] Todos os wireframes traduzidos para high-fidelity
- [ ] Design tokens aplicados corretamente (cores, tipo, spacing, elevation)
- [ ] Componentes do design system utilizados (sem custom desnecessário)
- [ ] Todos os estados de componentes desenhados (default, hover, active, disabled, error)
- [ ] Microcopy real aplicado em todas as telas
- [ ] Breakpoints responsive contemplados (mobile-first ou desktop-first)
- [ ] Alinhamento ao 8pt grid verificado
- [ ] Contraste de cores validado (WCAG AA mínimo)
- [ ] Review do Design Lead aprovado
- [ ] Arquivo Figma organizado com páginas, frames e layers nomeados

## Steps
1. **Setup do arquivo Figma** — Criar arquivo com estrutura padronizada: cover page, páginas
   por fluxo, componentes locais e change log. Conectar libraries do DS.

2. **Aplicar design tokens** — Configurar paleta de cores, tipografia, espaçamento e elevação
   conforme tokens do design system. Verificar versão atualizada dos tokens.

3. **Compor telas com componentes do DS** — Utilizar componentes existentes da library para
   montar cada tela. Documentar quando um novo componente é necessário.

4. **Refinar visual hierarchy** — Ajustar tamanhos, pesos e cores para estabelecer hierarquia
   clara de informação. Garantir que o olho do usuário é guiado corretamente.

5. **Desenhar todos os estados** — Para cada componente interativo e cada tela, criar variações
   para: default, hover, active, focused, disabled, loading, error, success, empty.

6. **Aplicar microcopy final** — Inserir textos definitivos fornecidos pelo Content Designer.
   Testar com textos longos e curtos para validar flexibilidade do layout.

7. **Design responsive** — Criar variações para breakpoints definidos. Documentar como componentes
   e layouts se adaptam entre mobile, tablet e desktop.

8. **Validar acessibilidade visual** — Verificar contraste de cores (4.5:1 para texto, 3:1 para
   elementos gráficos), tamanhos de toque (44x44px mínimo) e indicadores não cromáticos.

9. **Organizar arquivo e nomear layers** — Garantir que frames, layers e páginas seguem convenção
   de nomenclatura do squad. Adicionar anotações onde necessário.

10. **Conduzir review com squad** — Apresentar mockups ao Design Lead, UX Designer e Tech Lead.
    Incorporar feedback e registrar versão final aprovada.

## Output
- **High-Fidelity Mockups** — Telas completas para todos os fluxos e estados
- **Responsive Variants** — Variações para cada breakpoint
- **Spec Sheet** — Anotações de interação e comportamento por tela
- **Formato:** Figma file com estrutura padronizada
- **Nomenclatura:** `ui-hifi-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UI Designer |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por projeto ou feature |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/ui/` |

## Cross-References
- [Wireframe Pack](../ux/wireframe-pack.md)
- [Build Prototype](./build-prototype.md)
- [Design Responsive Layouts](./design-responsive-layouts.md)
- [Dev Handoff](../handoff/dev-handoff.md)
- [Design System Review](../review/design-system-review.md)
- [Create Component Spec](../design-system/create-component-spec.md)
