# Content Design — Microcopy

## Metadata
- **Categoria:** UX
- **Complexidade:** Média
- **Tempo Estimado:** 3-5 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** ux, content-design, microcopy, ux-writing, voice-and-tone

## Objective
Projetar e redigir microcopy para interfaces do produto garantindo clareza, consistência e tom
adequado em todos os touchpoints textuais. O content design transforma interações complexas em
experiências compreensíveis através de palavras estrategicamente escolhidas.

## Prerequisites
- User flows e wireframes disponíveis como referência estrutural
- Voice and tone guidelines do produto (ou necessidade de criá-los)
- Glossário de termos do produto (se existente)
- Contextos de uso e personas documentados
- Acesso ao design system para verificar padrões de texto existentes

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Content Designer | Redigir microcopy, definir voice and tone e manter glossário |
| UX Designer | Fornecer contexto de interação e integrar texto ao design |
| Product Manager | Validar terminologia de negócio e mensagens-chave |
| A11y Specialist | Revisar clareza e inclusividade do conteúdo |
| Localization Lead | Avaliar adaptabilidade para múltiplos idiomas (se aplicável) |

## Frameworks
- **Voice and Tone Guidelines** — personalidade da marca em diferentes contextos
- **Content Patterns** — padrões reutilizáveis: CTAs, errors, empty states, tooltips
- **Readability Standards** — Flesch-Kincaid ou equivalente para clareza
- **Inclusive Language Guidelines** — linguagem acessível e não discriminatória
- **Content-First Design** — texto como elemento primário, não decorativo

## Checklists
- [ ] Voice and tone guidelines definidos ou revisados
- [ ] Glossário de termos do produto atualizado
- [ ] Microcopy redigido para todos os estados: default, loading, success, error, empty
- [ ] CTAs claros e orientados à ação (verbo + complemento)
- [ ] Mensagens de erro seguem padrão: o que aconteceu + como resolver
- [ ] Empty states informativos e guiam o próximo passo
- [ ] Tooltips e help text escritos em linguagem simples
- [ ] Revisão de inclusividade e acessibilidade executada
- [ ] Consistência verificada entre todas as telas do fluxo
- [ ] Microcopy validado com usuários (se possível via teste)

## Steps
1. **Auditar conteúdo existente** — Revisar textos atuais do produto identificando inconsistências,
   jargão técnico, ambiguidades e lacunas. Criar inventário de microcopy.

2. **Definir voice and tone** — Documentar a personalidade verbal do produto: atributos de voz
   (ex: profissional, amigável, direto) e variações de tom por contexto (sucesso vs erro).

3. **Criar glossário** — Definir termos-chave do produto com definição, uso correto e variações
   a evitar. Garantir alinhamento entre produto, marketing e suporte.

4. **Mapear touchpoints textuais** — Listar todos os pontos onde o usuário encontra texto na
   interface: headers, labels, CTAs, placeholders, errors, confirmações, tooltips.

5. **Redigir microcopy por categoria** — Criar texto para cada categoria de touchpoint seguindo
   padrões definidos. Priorizar fluxos críticos identificados nos user flows.

6. **Aplicar padrão de mensagens de erro** — Para cada erro possível, redigir seguindo o formato:
   "O que aconteceu" + "Por que aconteceu" (se relevante) + "Como resolver".

7. **Projetar empty states** — Criar conteúdo para estados vazios que: explique o que deveria
   estar ali, guie o próximo passo e mantenha o tom adequado ao contexto.

8. **Revisar inclusividade** — Verificar: uso de linguagem neutra, ausência de jargão excludente,
   clareza para diferentes níveis de letramento digital, alt texts adequados.

9. **Validar com squad e usuários** — Revisar todo o microcopy com UX Designer e PM. Se possível,
   testar compreensão com 3-5 usuários em sessões rápidas de 15 minutos.

## Output
- **Microcopy Spec** — Documento com todo o texto da interface organizado por tela/componente
- **Voice and Tone Guide** — Diretrizes de voz e tom do produto
- **Glossary** — Glossário de termos com uso correto e variações
- **Formato:** Markdown + Figma annotations
- **Nomenclatura:** `microcopy-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Content Designer |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por projeto, atualização contínua |
| Aprovadores | Design Lead, PM |
| Repositório | `/squads/design/tasks/ux/` |

## Cross-References
- [Design User Flows](./design-user-flows.md)
- [Wireframe Pack](./wireframe-pack.md)
- [Build IA and Sitemap](./build-ia-and-sitemap.md)
- [A11y Audit](../accessibility/a11y-audit.md)
- [Dev Handoff](../handoff/dev-handoff.md)
- [Update Design System Docs](../operations/update-design-system-docs.md)
