# Handoff Review

## Metadata
- **Categoria:** Review
- **Complexidade:** Média
- **Tempo Estimado:** 1 dia
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** review, handoff, completeness, specs, engineering-readiness

## Objective
Revisar a completude e qualidade das especificações de design antes da entrega formal para
engenharia. O review garante que o pacote de handoff contém todas as informações necessárias
para implementação, reduzindo idas e vindas e acelerando o ciclo de desenvolvimento.

## Prerequisites
- Pacote de handoff preparado pelo designer (Figma + specs)
- Design system review e accessibility review concluídos
- Protótipo interativo disponível como referência
- Checklist de completude de handoff preparado
- Reviewer designado (Design Lead ou peer senior)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design Lead | Conduzir review de completude e qualidade |
| UI Designer | Apresentar handoff e completar lacunas identificadas |
| UX Designer | Validar cobertura de fluxos e edge cases |
| Frontend Engineer (optional) | Preview para identificar gaps técnicos |

## Frameworks
- **Handoff Completeness Checklist** — itens obrigatórios para aprovação
- **Quality Gate** — gate de qualidade que deve ser passado antes do handoff
- **Spec Coverage Matrix** — mapa de o que está especificado vs o que falta
- **Red/Yellow/Green Status** — classificação de readiness por área

## Checklists
- [ ] Arquivo Figma organizado com estrutura e naming padronizados
- [ ] Todas as telas dos fluxos aprovados presentes
- [ ] Todos os estados de componentes documentados (default, hover, etc.)
- [ ] Responsive variants para todos os breakpoints definidos
- [ ] Edge cases documentados (empty, error, loading, long text, first time)
- [ ] Annotations de comportamento e interação adicionadas
- [ ] Microcopy final aplicado em todas as telas
- [ ] Assets exportáveis preparados (SVG, PNG, WebP)
- [ ] A11y annotations incluídas (headings, focus order, ARIA)
- [ ] Design acceptance criteria redigidos

## Steps
1. **Verificar organização do arquivo** — Confirmar: structure de páginas, naming de frames,
   layers limpas, cover page atualizada e Dev Mode ativado.

2. **Verificar cobertura de telas** — Cruzar user flows com telas no Figma. Garantir que cada
   etapa do fluxo tem uma tela correspondente, incluindo bifurcações.

3. **Verificar estados de componentes** — Confirmar que para cada componente interativo existem
   variações para todos os estados relevantes em uma página dedicada.

4. **Verificar responsive** — Confirmar que existem variações para todos os breakpoints
   definidos com behavior notes sobre o que muda entre eles.

5. **Verificar edge cases** — Confirmar documentação de: textos extremamente longos, estados
   sem dados, erros de API, timeout, conexão lenta e primeiro acesso.

6. **Verificar annotations** — Confirmar que existem notas explicativas para: interações não
   óbvias, regras de negócio, condições de visibilidade e animações.

7. **Verificar a11y annotations** — Confirmar presença de: heading levels, landmark regions,
   focus order, alt texts e ARIA labels nos designs.

8. **Verificar assets** — Confirmar que ícones estão marcados para export em SVG e imagens
   em formatos otimizados. Verificar qualidade dos exports.

9. **Emitir parecer** — Classificar readiness como Green (pronto), Yellow (lacunas menores,
   prosseguir com follow-up) ou Red (lacunas críticas, não entregar ainda).

## Output
- **Handoff Review Report** — Parecer de readiness com findings por área
- **Approval/Block** — Decisão formal: aprovado, aprovado com condições ou bloqueado
- **Formato:** Markdown + Figma comments
- **Nomenclatura:** `handoff-review-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por handoff (antes de cada entrega para eng) |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/review/` |

## Cross-References
- [Dev Handoff](../handoff/dev-handoff.md)
- [Design System Review](./design-system-review.md)
- [Accessibility Review](./accessibility-review.md)
- [Design Critique Session](./design-critique-session.md)
- [QA with Engineering](../handoff/qa-with-engineering.md)
