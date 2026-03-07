# A11y Training Session

## Metadata
- **Categoria:** Accessibility
- **Complexidade:** Média
- **Tempo Estimado:** 2-3 dias (preparação) + 2-4h (sessão)
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** accessibility, training, education, wcag, inclusive-design, enablement

## Objective
Conduzir sessões de treinamento sobre acessibilidade digital para designers e engineers do squad,
elevando o nível de conhecimento e capacitando o time a projetar e implementar experiências
acessíveis desde o início (shift-left a11y), reduzindo custos de remediação.

## Prerequisites
- Tópicos de treinamento priorizados com base nos gaps identificados
- Exemplos reais do próprio produto para contextualizar aprendizados
- Ferramentas de teste de a11y disponíveis para exercícios hands-on
- Assistive technologies configuradas para demonstração (screen reader, switch)
- Sala ou videoconferência reservada com capacidade adequada

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| A11y Specialist | Preparar conteúdo, facilitar sessão e conduzir exercícios |
| Design Lead | Apoiar na priorização de tópicos e garantir participação |
| Design Ops | Logística, agendamento e materiais de suporte |
| Participantes | Designers, engineers, PMs do squad |

## Frameworks
- **WCAG 2.2 Overview** — princípios POUR: Perceivable, Operable, Understandable, Robust
- **Shift-Left Accessibility** — integrar a11y desde design, não apenas QA
- **Persona Spectrum (Microsoft)** — deficiências permanentes, temporárias e situacionais
- **Assistive Technology Demo** — experiência prática com screen readers e switch control
- **Empathy Exercises** — simulação de restrições para construir empatia

## Checklists
- [ ] Tópicos selecionados e priorizados por relevância para o squad
- [ ] Material de treinamento preparado (slides, exemplos, exercícios)
- [ ] Exemplos reais do produto coletados para contextualização
- [ ] Exercícios hands-on estruturados e testados
- [ ] Assistive technologies configuradas e funcionando para demo
- [ ] Sessão agendada com confirmação de todos os participantes
- [ ] Material de referência (cheat sheets, checklists) preparado para distribuição
- [ ] Sessão conduzida e feedback coletado
- [ ] Gravação disponibilizada para ausentes
- [ ] Quiz ou assessment pós-treinamento aplicado (opcional)

## Steps
1. **Identificar gaps de conhecimento** — Com base em audit findings e feedback do squad,
   identificar os tópicos de a11y com maior gap de conhecimento e impacto.

2. **Selecionar formato** — Definir: workshop hands-on (2-4h), lightning talk (30min), série
   de micro-sessions (4x 30min) ou bootcamp (dia inteiro). Adaptar ao público.

3. **Preparar material** — Criar slides com: conceitos fundamentais, exemplos reais do produto,
   demonstrações de assistive tech e exercícios práticos.

4. **Criar exercícios hands-on** — Preparar 2-3 exercícios práticos: navegar com screen reader,
   avaliar tela com checklist, redesenhar componente inacessível.

5. **Configurar assistive tech** — Testar screen readers (NVDA, VoiceOver), ferramentas de teste
   (axe, WAVE) e simuladores de restrição visual em todas as máquinas.

6. **Conduzir sessão** — Apresentar conteúdo alternando entre teoria e prática. Usar exemplos
   do próprio produto para manter relevância. Incluir empathy exercise.

7. **Facilitar exercícios** — Guiar participantes nos exercícios hands-on. Oferecer suporte
   individual e promover discussão sobre dificuldades encontradas.

8. **Distribuir material de referência** — Entregar: cheat sheet de WCAG, checklist de design
   acessível, guia de teste com keyboard e links para recursos de aprofundamento.

9. **Coletar feedback** — Aplicar survey rápido (5 perguntas) sobre: relevância, clareza,
   aplicabilidade e sugestões para próximas sessões.

## Output
- **Training Materials** — Slides, exercícios e gravação da sessão
- **Reference Materials** — Cheat sheets e checklists distribuídos
- **Feedback Summary** — Resultado do survey de feedback dos participantes
- **Formato:** Slides (PDF/Google Slides) + Markdown + gravação de vídeo
- **Nomenclatura:** `a11y-training-[topico]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | A11y Specialist |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Trimestral ou por onboarding de novos membros |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/accessibility/` |

## Cross-References
- [A11y Audit](./a11y-audit.md)
- [Remediate and Verify](./remediate-and-verify.md)
- [Onboard New Designer](../operations/onboard-new-designer.md)
- [DS Health Check](../design-system/ds-health-check.md)
- [Accessibility Review](../review/accessibility-review.md)
