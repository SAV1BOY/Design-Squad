# New Designer Onboarding

## Metadata

| Campo         | Valor                                     |
| ------------- | ----------------------------------------- |
| squad         | Design                                    |
| versao        | 1.0.0                                     |
| criado_em     | 2026-03-06                                |
| owner         | Design Lead                               |
| cadencia      | A cada nova contratacao                   |
| duracao_media | 4-6 semanas (ramp-up completo)            |
| tags          | onboarding, ferramentas, DS, rituais      |

## Trigger

Quando iniciar:

- Novo designer contratado (full-time ou contrato).
- Designer transferido de outro squad.
- Estagiario inicia no squad.

Pre-condicoes: contratacao aprovada e data definida; buddy designado (designer senior); acessos solicitados ao IT; onboarding checklist preparado.

## Phases

### Fase 1 — Semana 1: Ferramentas e Ambiente
**Agents:** Novo designer, Buddy, Design Ops/IT.
**Inputs:** Lista de ferramentas, credenciais, welcome kit.
**Atividades:** **Dia 1:** reuniao com Design Lead (30 min, boas-vindas, visao, expectativas); reuniao com Buddy (30 min, quem eh quem, dia-a-dia); tour de ferramentas. **Dias 1-3:** configurar Figma (org, libraries DS); acessar tracker (Jira/Linear/Notion); entrar em canais Slack; acessar repositorio de pesquisa. **Dias 3-5:** clonar templates Figma; revisar folder structure; familiarizar-se com board de tracking.
**Outputs:** Ferramentas configuradas, canais acessados, templates clonados, navegacao autonoma no Figma.

### Fase 2 — Semana 1-2: Design System Deep-Dive
**Agents:** Novo designer, Buddy, DS Lead.
**Inputs:** Documentacao DS, Figma library, Storybook.
**Atividades:** **Sessao com DS Lead (60 min):** visao geral, foundations, componentes core, como buscar/usar, como propor novos. **Exercicio pratico (2-3h):** recriar tela existente usando apenas DS; identificar gaps; Buddy revisa. **Review de tokens:** naming convention, onde encontrar valores, fluxo Figma -> codigo.
**Outputs:** Exercicio concluido e revisado, designer confortavel com DS, gaps identificados.

### Fase 3 — Semana 2-3: Rituais e Processos
**Agents:** Novo designer, Buddy, Design Lead.
**Inputs:** Calendario de rituais, docs de workflows, projetos anteriores.
**Atividades:** Participar de cada ritual como observador (backlog monday, critique, handoff, housekeeping); Buddy walkthrough dos workflows principais (`feature-design-end-to-end.md`, `handoff-and-build-loop.md`, `design-critique-loop.md`); shadow de projeto ativo do Buddy (3-5 dias); 1:1 com PM e Tech Lead (30 min cada).
**Outputs:** Todos rituais observados (min 1x), workflows entendidos, shadow concluido, relacoes com PM e Tech Lead.

### Fase 4 — Semana 3-6: Primeiros Projetos
**Agents:** Novo designer, Buddy (mentor), Design Lead (check-ins).
**Inputs:** Projeto de entrada (escopo pequeno), conhecimento acumulado.
**Atividades:** **Semana 3-4:** projeto de entrada (melhoria ou divida), execucao com autonomia crescente, apresentar em critique. **Semana 4-6:** segundo projeto (parte de feature), maior autonomia, participar de handoff. **Check-ins:** semana 2 (como esta indo?), semana 4 (progresso, feedback), semana 6 (onboarding completo?). **Feedback 360:** coletar feedback do novo designer sobre o processo; Buddy e Lead avaliam ramp-up.
**Outputs:** Projetos entregues, check-ins documentados, feedback coletado, designer operando com autonomia.

## Quality Gates

### Gate Ferramentas (Semana 1)
- [ ] Todas as ferramentas configuradas.
- [ ] Acesso a Figma org e libraries.
- [ ] Canais acessados.

### Gate DS (Semana 1-2)
- [ ] Sessao com DS Lead realizada.
- [ ] Exercicio pratico revisado.

### Gate Rituais (Semana 2-3)
- [ ] Cada ritual observado min 1x.
- [ ] Shadow concluido.
- [ ] 1:1 com PM e Tech Lead.

### Gate Projetos (Semana 3-6)
- [ ] Projeto de entrada concluido.
- [ ] Apresentou em critique.
- [ ] Participou de handoff.
- [ ] Check-in semana 6 realizado.
- [ ] Feedback coletado.

## Cross-References

- `weekly-design-ops-cadence.md` — Rituais semanais.
- `design-critique-loop.md` — Formato de critique.
- `design-system-bootstrap.md` — Contexto do DS.
- `design-system-component-lifecycle.md` — Como propor componentes.
- `feature-design-end-to-end.md` — Pipeline de features.
- `handoff-and-build-loop.md` — Processo de handoff.
- `design-to-code-sync.md` — Fluxo de tokens.
