# Design System Review

## Metadata
- **Categoria:** Review
- **Complexidade:** Média
- **Tempo Estimado:** 1-2 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** review, design-system, consistency, tokens, components, governance

## Objective
Revisar trabalho de design em andamento para garantir aderência ao design system: uso correto de
tokens, componentes, patterns e guidelines. O review previne drift do DS, identifica necessidades
de novos componentes e mantém consistência visual entre squads.

## Prerequisites
- Design em estágio de mockup high-fidelity ou posterior
- Design system documentation acessível como referência
- Figma library conectada ao arquivo sendo revisado
- Checklist de DS compliance preparado
- Reviewer com domínio do design system

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design System Lead | Conduzir review e documentar findings |
| UI Designer | Apresentar design e ajustar com base no feedback |
| Design Lead | Arbitrar exceções e aprovar desvios justificados |

## Frameworks
- **DS Compliance Checklist** — itens de verificação por categoria (tokens, components, patterns)
- **Deviation Request** — processo formal para desvios justificados do DS
- **Component Coverage** — % de elementos que utilizam componentes do DS
- **Token Coverage** — % de valores de cor, tipo e spacing que usam tokens
- **New Component Proposal** — trigger para solicitar novo componente ao DS

## Checklists
- [ ] Todos os valores de cor utilizam color tokens do DS
- [ ] Tipografia segue type scale e text styles do DS
- [ ] Espaçamento segue spacing tokens (sem valores custom)
- [ ] Componentes do DS utilizados quando disponíveis
- [ ] Variantes corretas de componentes selecionadas
- [ ] Elevação e border radius seguem tokens do DS
- [ ] Patterns de layout consistentes com guidelines
- [ ] Iconografia utiliza icon library do DS
- [ ] Desvios identificados e justificados formalmente
- [ ] Necessidades de novos componentes registradas

## Steps
1. **Verificar token coverage** — Inspecionar todas as cores, tamanhos de texto e espaçamentos
   no design. Identificar valores hardcoded que deveriam usar tokens do DS.

2. **Verificar component usage** — Para cada elemento interativo, confirmar que utiliza
   componente da library do DS. Listar instâncias de custom components desnecessários.

3. **Verificar variantes corretas** — Garantir que as variantes de componentes selecionadas são
   as adequadas: size, type, state conforme o contexto de uso.

4. **Verificar patterns e layout** — Confirmar que patterns de página (header, content, sidebar),
   grid system e breakpoints seguem guidelines do DS.

5. **Verificar iconografia** — Garantir que ícones são da library oficial, no tamanho correto
   e com as cores de token apropriadas.

6. **Identificar desvios** — Listar todos os pontos onde o design diverge do DS. Classificar
   como: não intencional (corrigir) ou intencional (justificar via Deviation Request).

7. **Identificar gaps no DS** — Se o design precisa de componentes ou variantes não existentes
   no DS, registrar como proposta de novo componente para avaliação.

8. **Consolidar feedback** — Documentar findings por categoria: must fix (compliance), should
   fix (consistency), e proposals (novos componentes/variantes).

9. **Comunicar ao designer** — Compartilhar feedback com UI Designer. Apoiar na resolução de
   issues e na submissão de Deviation Requests quando justificado.

## Output
- **DS Review Report** — Findings por categoria com status e ações
- **Deviation Requests** — Pedidos formais de desvio justificado
- **New Component Proposals** — Propostas de componentes/variantes para o DS
- **Formato:** Markdown + Figma comments
- **Nomenclatura:** `ds-review-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design System Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por projeto antes do handoff |
| Aprovadores | Design System Lead |
| Repositório | `/squads/design/tasks/review/` |

## Cross-References
- [DS Health Check](../design-system/ds-health-check.md)
- [DS Contribution Review](../design-system/ds-contribution-review.md)
- [Create Component Spec](../design-system/create-component-spec.md)
- [UI Design High Fidelity](../ui/ui-design-high-fidelity.md)
- [Handoff Review](./handoff-review.md)
