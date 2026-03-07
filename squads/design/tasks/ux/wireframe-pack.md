# Wireframe Pack

## Metadata
- **Categoria:** UX
- **Complexidade:** Média-Alta
- **Tempo Estimado:** 5-10 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** ux, wireframes, low-fidelity, layout, structure

## Objective
Produzir um conjunto completo de wireframes de baixa a média fidelidade que traduzem user flows
e IA em layouts estruturais. Os wireframes priorizam hierarquia de informação, posicionamento de
elementos e lógica de interação, sem foco em estética visual.

## Prerequisites
- User flows aprovados e versionados
- Information Architecture e sitemap definidos
- Personas ou JTBD disponíveis para referência de contexto
- Design system component inventory (se existente)
- Ferramenta de wireframing configurada (Figma, Balsamiq, Whimsical)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UX Designer | Criar wireframes, iterar com feedback e documentar decisões |
| Design Lead | Revisar hierarquia de informação e consistência entre telas |
| Product Manager | Validar conteúdo, priorização e requisitos funcionais |
| Content Designer | Fornecer texto real ou próximo do real para cada tela |
| Tech Lead | Confirmar viabilidade de layouts e componentes propostos |

## Frameworks
- **Content-First Design** — priorizar conteúdo real sobre lorem ipsum
- **Progressive Disclosure** — revelar informação gradualmente conforme necessidade
- **Gestalt Principles** — proximidade, similaridade, continuidade para agrupamento visual
- **Responsive Wireframing** — considerar breakpoints desde o wireframe
- **Annotation Standards** — padrão de anotações para especificar comportamentos

## Checklists
- [ ] Todas as telas dos user flows aprovados contempladas
- [ ] Conteúdo real ou próximo do real utilizado (não lorem ipsum)
- [ ] Hierarquia de informação clara e consistente entre telas
- [ ] Progressive disclosure aplicado em telas complexas
- [ ] Estados de cada componente contemplados (default, hover, active, disabled, error)
- [ ] Breakpoints mobile e desktop considerados
- [ ] Anotações de comportamento incluídas em cada tela
- [ ] Review com Design Lead executado
- [ ] Feedback de PM e Tech Lead incorporado
- [ ] Wireframes versionados e organizados no Figma

## Steps
1. **Mapear inventário de telas** — A partir dos user flows, listar todas as telas necessárias.
   Agrupar por fluxo e identificar telas compartilhadas entre fluxos.

2. **Definir grid e estrutura base** — Estabelecer grid system, breakpoints e estrutura de
   página base (header, content area, sidebar, footer) para garantir consistência.

3. **Wireframar telas-chave primeiro** — Começar pelas telas de maior complexidade ou impacto.
   Focar em hierarquia de informação e posicionamento de elementos-chave.

4. **Inserir conteúdo real** — Substituir placeholders por conteúdo real ou próximo do real.
   Testar com textos longos e curtos para validar flexibilidade do layout.

5. **Contemplar estados de componentes** — Para cada componente interativo, documentar estados:
   default, hover, active, focused, disabled, loading, error e success.

6. **Adicionar anotações** — Incluir notas explicativas sobre: comportamentos de interação,
   regras de negócio, condições de visibilidade e lógica de componentes.

7. **Considerar responsive** — Criar variações para os breakpoints críticos (mobile, tablet,
   desktop). Documentar como elementos se reorganizam entre breakpoints.

8. **Revisar com squad** — Conduzir sessão de review com Design Lead, PM e Tech Lead. Coletar
   feedback sobre viabilidade, conteúdo e priorização.

9. **Iterar e finalizar** — Incorporar feedback, ajustar wireframes e versionar. Organizar
   arquivo Figma com nomenclatura padronizada e navegação clara.

## Output
- **Wireframe Pack** — Conjunto completo de wireframes organizados por fluxo
- **Annotation Document** — Anotações de comportamento e regras por tela
- **Responsive Specs** — Variações de layout para breakpoints críticos
- **Formato:** Figma file + Markdown para anotações detalhadas
- **Nomenclatura:** `wireframes-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UX Designer |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por projeto ou feature |
| Aprovadores | Design Lead, PM |
| Repositório | `/squads/design/tasks/ux/` |

## Cross-References
- [Design User Flows](./design-user-flows.md)
- [Build IA and Sitemap](./build-ia-and-sitemap.md)
- [UI Design High Fidelity](../ui/ui-design-high-fidelity.md)
- [Build Prototype](../ui/build-prototype.md)
- [Design Responsive Layouts](../ui/design-responsive-layouts.md)
- [Run Usability Test](../research/run-usability-test.md)
