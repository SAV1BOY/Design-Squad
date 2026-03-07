# Cross-Squad Narrative Handoff

## Metadata

| Campo         | Valor                                       |
| ------------- | ------------------------------------------- |
| squad         | Design + Story/Copy Squad                   |
| versao        | 1.0.0                                       |
| criado_em     | 2026-03-06                                  |
| owner         | Design Lead + Content Lead                  |
| cadencia      | Por projeto com narrativa significativa     |
| duracao_media | 1-2 semanas (colaboracao ativa)             |
| tags          | cross-squad, narrative, copy, storytelling  |

## Trigger

Quando iniciar:

- Landing page ou campanha com storytelling central.
- Onboarding com narrativa de usuario.
- Feature com copy extenso (wizards, walkthroughs).
- Rebranding que impacta tom de voz nas interfaces.

Pre-condicoes: Writer do Story/Copy Squad alocado; brief com objetivos de comunicacao; tom de voz definido; Designer alocado.

## Phases

### Fase 1 — Briefing Conjunto (60 min)
**Agents:** Designer, Writer, PM.
**Inputs:** Brief (objetivo, audiencia, KPIs), brand guidelines, tom de voz, pesquisa de usuario.
**Atividades:** Revisar brief e objetivos; alinhar entendimento da audiencia; definir narrativa central (core message, arco); acordar tom visual e verbal; mapear touchpoints da narrativa no fluxo; identificar momentos onde copy e visual se reforcam; definir cadencia de trabalho; criar shared workspace.
**Outputs:** Narrativa central documentada, mapa de touchpoints, cadencia definida, workspace criado.

### Fase 2 — Co-Criacao (Copy + Visual)
**Agents:** Designer, Writer, PM (check-ins).
**Inputs:** Narrativa central, mapa de touchpoints, DS, brand guidelines.
**Atividades:** Trabalho paralelo com sync diario (15-20 min): Writer cria drafts de copy, Designer cria wireframes; garantir que hierarquia visual reforca copy; imagens complementam (nao repetem) texto; micro-copy (CTAs, labels, tooltips) alinhados; testar legibilidade no contexto visual; revisar a11y do copy (linguagem clara, alt text).
**Outputs:** Wireframes com copy real (nao placeholder), copy deck por touchpoint, alternativas visuais.

### Fase 3 — Refinamento e Review
**Agents:** Designer, Writer, Design Lead, Content Lead.
**Inputs:** Wireframes com copy, brand guidelines, feedback de stakeholders.
**Atividades:** Design review (Design Lead); copy review (Content Lead); review conjunta de harmonia; iterar; criar high-fi mockups com copy final; validar responsividade (copy pode quebrar em mobile); review de localizacao se aplicavel.
**Outputs:** Mockups high-fi com copy final, copy deck aprovado, sign-off de Design Lead e Content Lead.

### Fase 4 — Handoff para Engenharia
**Agents:** Designer, Writer, Frontend Engineer.
**Inputs:** Mockups finais, copy deck versionado, specs.
**Atividades:** Sessao de handoff conjunta (Designer + Writer + Engineer); copy em formato consumivel (JSON, CMS, strings file); heading hierarchy e semantics para a11y; comportamento de copy dinamico (pluralizacao, variaveis, fallbacks); mapeamento de localizacao.
**Outputs:** Copy em formato tecnico, specs com anotacoes de copy, handoff realizado.

### Fase 5 — QA de Narrativa
**Agents:** Writer, Designer, QA.
**Inputs:** Build em staging, copy deck, mockups.
**Atividades:** Writer revisa copy (typos, truncamento, overflow); Designer revisa integracao visual + copy; testar breakpoints (copy em mobile?); copy dinamico com dados reais; screen reader test (narrativa sequencial?); registrar e corrigir bugs.
**Outputs:** Bugs corrigidos, sign-off conjunto (Writer + Designer), projeto pronto.

## Quality Gates

### Gate Briefing -> Co-Criacao
- [ ] Narrativa central documentada.
- [ ] Mapa de touchpoints criado.

### Gate Co-Criacao -> Refinamento
- [ ] Wireframes com copy real.
- [ ] Syncs diarios realizados.

### Gate Refinamento -> Handoff
- [ ] Sign-off de Design Lead e Content Lead.
- [ ] Responsividade do copy validada.

### Gate Handoff -> QA
- [ ] Copy em formato tecnico entregue.
- [ ] Sessao conjunta realizada.

### Gate QA -> Release
- [ ] Copy sem typos/truncamento.
- [ ] Screen reader review concluido.
- [ ] Sign-off conjunto.

## Cross-References

- `feature-design-end-to-end.md` — Narrativa integra-se ao pipeline.
- `handoff-and-build-loop.md` — Handoff padrao com adicao de copy.
- `usability-testing-sprint.md` — Testar narrativa com usuarios.
- `design-critique-loop.md` — Critique conjunta copy + visual.
- `a11y-integration-workflow.md` — Copy acessivel no processo.
- `multi-platform-design-workflow.md` — Copy pode variar por plataforma.
