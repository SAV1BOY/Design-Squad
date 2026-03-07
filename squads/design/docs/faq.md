# FAQ

## Overview

Perguntas frequentes sobre o Design Squad, seus processos, ferramentas e padrões.
Organizado por categoria para facilitar busca. Se sua pergunta não está aqui,
pergunte no #design-squad e adicionaremos a resposta.

## Content

### Geral

**Q: Qual é a missão do Design Squad?**
A: Criar experiências digitais úteis, utilizáveis e acessíveis, sustentadas por um
design system robusto e processos de qualidade. Detalhes em `squad-overview.md`.

**Q: Como solicito trabalho de design para meu squad?**
A: Crie uma request no board compartilhado usando o template em
`cross-squad-integration-guide.md`. O Design Lead aloca um designer em até 2 dias.

**Q: Qual é o SLA de entrega de design?**
A: Depende da prioridade: P0 (1-2 dias), P1 (3-5 dias), P2 (1-2 sprints), P3 (2-3
sprints). Detalhes em `cross-squad-integration-guide.md`.

**Q: Posso dar feedback sobre o design do produto?**
A: Sim. Qualquer pessoa na organização pode postar sugestões no #design-reviews com
screenshot e descrição do problema. Respondemos em até 48h.

### Design System

**Q: Posso criar componente custom no meu squad?**
A: Sim, se o componente é específico do seu domínio. Se é potencialmente reutilizável
(2+ squads), proponha para o DS via `contribution-guide.md`.

**Q: Como sei se um componente existe no design system?**
A: Consulte o Storybook (link no bookmark do #design-system) ou a library no Figma.
Se não encontrar, pergunte no #design-system antes de criar do zero.

**Q: Quando acontecem breaking changes no DS?**
A: Apenas em major versions. Comunicadas com 2 major versions de antecedência, com
migration guide e codemod quando possível. Detalhes em `design-system-governance.md`.

**Q: Como proponho um novo componente?**
A: Post no #design-system com: nome, problema que resolve, use cases, e referências.
Se aprovado, segue para RFC. Processo completo em `contribution-guide.md`.

### Processos

**Q: Quando acontecem design reviews?**
A: Critique semanal às terças (1h). Reviews com stakeholders são por demanda. A11y
reviews e DS consistency reviews são antes de cada handoff.

**Q: O que precisa estar no handoff?**
A: Todos os estados, 3 breakpoints, token reference table, a11y specs, microcopy
aprovada. Checklist completa em `handoff-standards.md`.

**Q: Preciso esperar o design ficar "perfeito" para mostrar ao time?**
A: Não. Compartilhe cedo e frequentemente. O estágio do trabalho deve ser comunicado:
"Isto é exploração, busco feedback direcional" vs. "Isto é spec final, busco aprovação."

**Q: Como funciona a priorização do backlog de design?**
A: Design Lead prioriza com input de PMs usando critérios de impacto (NPS, conversão),
urgência (deadline, blocker) e esforço. Metodologia RICE quando aplicável.

### Acessibilidade

**Q: Qual é nosso nível de conformidade atual?**
A: Consultar `accessibility-policy.md` para o número atualizado. O target é WCAG 2.2
AA com evolução trimestral documentada.

**Q: Preciso testar com screen reader toda feature?**
A: Fluxos críticos (login, checkout, cadastro) sim, obrigatoriamente. Outras features
passam por audit automatizado (axe-core) + checklist manual.

**Q: Onde encontro as ferramentas de a11y?**
A: Figma: Plugin Stark. Browser: axe DevTools. CI: Pa11y. Screen readers: VoiceOver
(Mac: Cmd+F5), NVDA (Windows, gratuito). Scripts em `scripts/a11y/`.

**Q: O que fazer quando a11y e deadline conflitam?**
A: A11y crítica (bloqueio de uso) nunca é cortada. A11y séria pode ser lançada com
ticket de fix no próximo sprint. A11y menor entra como polish. Design Lead decide.

### Ferramentas

**Q: Quais plugins do Figma são obrigatórios?**
A: Figma Tokens, Stark (a11y) e Content Reel. Recomendados: Autoflow, Contrast.

**Q: Posso usar outra ferramenta além do Figma?**
A: Para deliverables, Figma é obrigatório (source of truth). Para exploração pessoal,
use o que preferir (Sketch, papel, Illustrator). Resultado final vai para Figma.

**Q: Onde documento decisões de design?**
A: ADRs na wiki (Confluence/Notion). Template em `documentation-style.md`. Link no
Figma quando a decisão afeta um arquivo específico.

### Carreira e Desenvolvimento

**Q: Como é a avaliação de performance de designers?**
A: Baseada em: qualidade de entregas (Gold Standard), contribuição ao time (critique,
mentoria), evolução técnica e impacto no produto. Ciclo semestral.

**Q: Que recursos de desenvolvimento o squad oferece?**
A: Budget anual para cursos/conferências, pair design com seniors, design critique
como ferramenta de aprendizado, acesso a ferramentas de referência.

**Q: Como evoluo de pleno para sênior?**
A: Autonomia completa em features complexas, mentoria ativa de juniors/plenos,
contribuição para processos e padrões do squad, influência em decisões de produto.
Conversar com Design Lead sobre plano individual.

## Cross-References

- `docs/getting-started.md` — Guia de primeiros passos
- `docs/squad-overview.md` — Visão geral do squad
- `docs/contribution-guide.md` — Como contribuir
- `docs/glossary.md` — Glossário de termos
