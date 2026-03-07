# DS Contribution Review

## Metadata
- **Categoria:** Design System
- **Complexidade:** Média
- **Tempo Estimado:** 1-2 dias por contribuição
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** design-system, contribution, review, governance, quality

## Objective
Revisar e avaliar contribuições ao design system vindas de squads consumidores, garantindo que
novos componentes, variantes e atualizações atendem aos padrões de qualidade, consistência e
acessibilidade do DS antes de serem integrados à library oficial.

## Prerequisites
- Contribution guidelines publicadas e acessíveis
- Contribuição submetida conforme template padronizado
- Critérios de aceitação documentados (qualidade, a11y, naming, tokens)
- Reviewers disponíveis (DS Lead + A11y + Frontend)
- Processo de feedback e iteração definido

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design System Lead | Revisar design, naming e consistência com o DS |
| A11y Specialist | Validar conformidade com ARIA patterns e WCAG |
| Frontend Engineer (DS) | Revisar viabilidade técnica e code quality |
| Contributor (Designer) | Submeter contribuição e iterar com feedback |
| Design Lead | Desempatar decisões e aprovar exceções |

## Frameworks
- **Contribution Checklist** — critérios obrigatórios para aceitação
- **Component Maturity Ladder** — nível mínimo de maturidade para entrada no DS
- **Review Rubric** — scorecard com dimensões de avaliação ponderadas
- **RFC (Request for Comments)** — para contribuições que propõem mudanças significativas
- **Feedback Loop** — estrutura para comunicação construtiva entre reviewer e contributor

## Checklists
- [ ] Contribuição submetida com template completo preenchido
- [ ] Necessidade do componente validada (uso em 2+ contextos)
- [ ] Naming convention do DS seguida corretamente
- [ ] Design tokens utilizados (sem valores hardcoded)
- [ ] Todas as variantes e estados desenhados
- [ ] Anatomia e props/API documentadas
- [ ] ARIA pattern identificado e implementado
- [ ] Keyboard interactions especificadas
- [ ] Guidelines de uso (Do/Don't) incluídos
- [ ] Feedback comunicado ao contributor de forma construtiva

## Steps
1. **Receber contribuição** — Verificar que a submissão está completa conforme template. Se
   incompleta, retornar ao contributor com checklist de itens faltantes.

2. **Validar necessidade** — Confirmar que o componente é necessário: usado em 2+ contextos,
   não duplica componente existente e não pode ser resolvido com variante do atual.

3. **Revisar design** — Avaliar: consistência visual com o DS, uso correto de tokens, qualidade
   dos estados e variantes, e aderência à visual language do produto.

4. **Revisar naming** — Verificar que nomes de componente, variantes e props seguem a naming
   convention do DS. Sugerir ajustes quando necessário.

5. **Revisar acessibilidade** — Validar ARIA pattern, keyboard interactions, contraste de cores,
   focus indicators e screen reader behavior contra WCAG 2.2 AA.

6. **Revisar viabilidade técnica** — Com Frontend Engineer, avaliar: implementabilidade, API de
   props, performance e compatibilidade com a stack técnica atual.

7. **Consolidar feedback** — Reunir feedback de todos os reviewers em um documento único.
   Classificar em: obrigatório (must fix), recomendado (should fix) e sugestão (nice to have).

8. **Comunicar ao contributor** — Enviar feedback de forma construtiva com: pontos positivos,
   itens obrigatórios, sugestões e prazo para re-submissão.

9. **Revisar iteração** — Avaliar re-submissão contra feedback anterior. Se todos os itens
   obrigatórios foram atendidos, aprovar para integração.

10. **Integrar à library** — Aprovar merge na library principal. Incluir na próxima release
    com crédito ao contributor nas release notes.

## Output
- **Review Report** — Feedback consolidado por contribuição
- **Approval/Rejection** — Decisão formal com justificativa
- **Formato:** Markdown template de review + comentários no Figma
- **Nomenclatura:** `ds-review-[nome-componente]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design System Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por contribuição recebida |
| Aprovadores | DS Lead + A11y Specialist |
| Repositório | `/squads/design/tasks/design-system/` |

## Cross-References
- [Create Component Spec](./create-component-spec.md)
- [Publish Library](./publish-library.md)
- [Adoption and Migration](./adoption-and-migration.md)
- [Accessibility Review](../review/accessibility-review.md)
- [Design System Review](../review/design-system-review.md)
