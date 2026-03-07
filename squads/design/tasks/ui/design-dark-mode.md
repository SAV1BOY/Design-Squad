# Design Dark Mode

## Metadata
- **Categoria:** UI
- **Complexidade:** Alta
- **Tempo Estimado:** 5-10 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** ui, dark-mode, theming, color-system, tokens, accessibility

## Objective
Projetar e especificar o modo escuro (dark mode) do produto, criando um sistema de cores semântico
que funcione em ambos os temas, adaptando componentes e garantindo acessibilidade. O resultado é
uma theme completa integrada ao design system e pronta para implementação.

## Prerequisites
- Design system com light mode estável e documentado
- Sistema de color tokens semânticos definido (ou necessidade de criá-lo)
- Inventário de componentes atualizado
- Ferramenta de design com suporte a modes/themes (Figma Variables)
- Referências de dark mode de produtos similares coletadas

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UI Designer | Criar paleta dark, adaptar componentes e validar visualmente |
| Design System Lead | Estruturar tokens semânticos e garantir escalabilidade |
| A11y Specialist | Validar contraste e acessibilidade em dark mode |
| Frontend Engineer | Avaliar estratégia de implementação (CSS variables, themes) |
| Design Lead | Revisar consistência e aprovar sistema de cores |

## Frameworks
- **Semantic Color Tokens** — tokens nomeados por função (background-primary, text-secondary)
- **Material Design Dark Theme** — guidelines de referência para dark mode
- **WCAG 2.2 Contrast** — 4.5:1 texto normal, 3:1 texto grande e elementos gráficos
- **Figma Variables & Modes** — para gerenciar themes de forma escalável
- **Elevation System (Dark)** — usar luminosidade ao invés de sombras para elevação

## Checklists
- [ ] Análise de referências de dark mode executada
- [ ] Sistema de color tokens semânticos definido (light + dark)
- [ ] Paleta dark mode criada com background, surface e accent colors
- [ ] Contraste verificado para todas as combinações text/background (WCAG AA)
- [ ] Componentes adaptados: botões, cards, inputs, modals, tooltips
- [ ] Imagens e ícones revisados para dark mode (sem halos, inversões incorretas)
- [ ] Elevação em dark mode definida (luminosidade, não sombra)
- [ ] Figma Variables configurados com mode light e dark
- [ ] Telas-chave renderizadas em dark mode para validação
- [ ] Specs de implementação documentados para eng

## Steps
1. **Auditar sistema de cores atual** — Mapear todas as cores usadas no light mode. Identificar
   cores hardcoded que precisam migrar para tokens semânticos antes do dark mode.

2. **Criar token layer semântica** — Definir naming convention para tokens: background-primary,
   surface-default, text-primary, border-subtle, etc. Mapear cada token para valor light.

3. **Projetar paleta dark** — Criar valores dark para cada token semântico. Regras-chave: fundo
   escuro mas não preto puro (#121212), reduzir saturação de cores, aumentar luminosidade.

4. **Adaptar sistema de elevação** — Em dark mode, elevação é expressa por aumento de
   luminosidade da superfície, não por sombras. Definir 5 níveis de surface elevation.

5. **Adaptar componentes** — Revisar cada componente do DS em dark mode: botões, cards, inputs,
   modals, tooltips, alerts. Ajustar bordas, sombras e estados.

6. **Validar contraste e acessibilidade** — Testar todas as combinações de texto/fundo contra
   WCAG AA (4.5:1). Verificar ícones, dividers e elementos gráficos (3:1).

7. **Revisar assets visuais** — Verificar: ícones com outline branco, imagens com fundo
   transparente, ilustrações, logos. Adaptar ou criar variantes dark quando necessário.

8. **Configurar Figma Variables** — Implementar sistema dual-mode no Figma usando Variables.
   Conectar tokens a componentes para switch automático entre themes.

9. **Renderizar telas-chave** — Aplicar dark mode em 5-10 telas representativas para validação
   visual completa. Verificar harmonia geral e identificar edge cases.

10. **Documentar specs** — Criar documento de implementação: token mapping, regras de elevação,
    exceções por componente e estratégia de CSS (prefers-color-scheme).

## Output
- **Dark Mode Theme** — Sistema completo de tokens e componentes em dark mode
- **Token Mapping Table** — Tabela de correspondência light/dark para cada token
- **Implementation Spec** — Documento técnico para Frontend Engineer
- **Formato:** Figma Variables + Markdown + token export (JSON/CSS)
- **Nomenclatura:** `dark-mode-[produto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UI Designer + DS Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Uma vez (setup), manutenção contínua |
| Aprovadores | Design Lead, A11y Specialist |
| Repositório | `/squads/design/tasks/ui/` |

## Cross-References
- [Create or Update Tokens](../design-system/create-or-update-tokens.md)
- [Create Component Spec](../design-system/create-component-spec.md)
- [A11y Audit](../accessibility/a11y-audit.md)
- [Publish Library](../design-system/publish-library.md)
- [UI Design High Fidelity](./ui-design-high-fidelity.md)
