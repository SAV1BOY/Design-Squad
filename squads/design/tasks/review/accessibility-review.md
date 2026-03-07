# Accessibility Review

## Metadata
- **Categoria:** Review
- **Complexidade:** Média
- **Tempo Estimado:** 1-2 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** review, accessibility, wcag, inclusive-design, shift-left

## Objective
Revisar designs em andamento (wireframes ou mockups) para identificar problemas de acessibilidade
antes da implementação (shift-left). O review antecipa barreiras que seriam mais custosas de
corrigir depois do código, garantindo que a11y é considerada desde o design.

## Prerequisites
- Design em estágio de wireframe ou mockup
- WCAG 2.2 Level AA como referência de conformidade
- Checklist de a11y para design preparado
- Conhecimento dos fluxos e interações planejadas
- Reviewer com expertise em acessibilidade

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| A11y Specialist | Conduzir review e documentar findings |
| UX/UI Designer | Apresentar design e iterar com feedback |
| Content Designer | Validar clareza de texto e mensagens de erro |
| Design Lead | Arbitrar trade-offs entre a11y e outros requisitos |

## Frameworks
- **WCAG 2.2 (Design-Phase Criteria)** — critérios aplicáveis antes da implementação
- **POUR Principles** — Perceivable, Operable, Understandable, Robust
- **A11y Annotation Kit** — anotações de a11y para adicionar ao design
- **Inclusive Design Principles** — projetar para diversidade de capacidades
- **Color Contrast Analyzer** — verificação de contraste em tempo de design

## Checklists
- [ ] Contraste de texto verificado (4.5:1 normal, 3:1 grande)
- [ ] Contraste de elementos UI verificado (3:1 para borders, icons)
- [ ] Hierarquia de headings lógica (h1 > h2 > h3)
- [ ] Focus order planejado e documentado
- [ ] Touch targets dimensionados (44x44px mínimo)
- [ ] Informação não depende apenas de cor (uso de ícones, texto, pattern)
- [ ] Mensagens de erro claras e vinculadas ao campo
- [ ] Empty states e loading states acessíveis
- [ ] Alternative text planejado para imagens e ícones
- [ ] Keyboard interactions especificadas para componentes custom

## Steps
1. **Verificar contraste de cores** — Usar Color Contrast Analyzer para testar todas as
   combinações de texto/fundo e elementos UI contra WCAG AA mínimo.

2. **Avaliar hierarquia visual e semântica** — Confirmar que heading levels formam hierarquia
   lógica (sem saltar níveis) e que a visual hierarchy corresponde à semântica.

3. **Verificar independência de cor** — Garantir que nenhuma informação depende exclusivamente
   de cor: status, erros, links, gráficos. Verificar alternativas: ícone, texto, pattern.

4. **Avaliar touch targets** — Medir áreas de toque de todos os elementos interativos. Garantir
   mínimo de 44x44px (inclusive spacing entre targets adjacentes).

5. **Planejar focus order** — Verificar que a ordem de focus segue a lógica visual e de leitura.
   Anotar order quando diferente do DOM natural.

6. **Revisar formulários** — Confirmar: labels visíveis, associação label-input, feedback de
   validação inline, mensagens de erro descritivas e estados de error acessíveis.

7. **Verificar content accessibility** — Com Content Designer, avaliar: linguagem simples,
   instruções claras, mensagens de erro acionáveis e alternative text adequado.

8. **Adicionar a11y annotations** — No Figma, adicionar annotations de: heading level, landmark
   regions, focus order, ARIA labels e keyboard interactions.

9. **Documentar findings** — Listar issues por WCAG criterion e prioridade. Incluir sugestão
   de solução e referência ao guideline violado.

## Output
- **A11y Review Report** — Findings com criterion, prioridade e solução sugerida
- **Annotated Design** — Figma com a11y annotations adicionadas
- **Formato:** Markdown + Figma annotations
- **Nomenclatura:** `a11y-review-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | A11y Specialist |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por feature antes do handoff |
| Aprovadores | A11y Specialist |
| Repositório | `/squads/design/tasks/review/` |

## Cross-References
- [A11y Audit](../accessibility/a11y-audit.md)
- [Remediate and Verify](../accessibility/remediate-and-verify.md)
- [Design Critique Session](./design-critique-session.md)
- [Handoff Review](./handoff-review.md)
- [UI Design High Fidelity](../ui/ui-design-high-fidelity.md)
