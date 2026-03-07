# Agent Roles Guide

## Overview

Guia detalhado dos papéis e responsabilidades de cada agente no Design Squad. Cada
papel tem escopo definido, entregáveis esperados e interfaces com outros papéis.
O objetivo é clareza sobre quem faz o quê, evitando gaps e sobreposições.

## Content

### Product Designer (Senior e Pleno)

**Responsabilidade central:** Traduzir necessidades do usuário e do negócio em
interfaces funcionais, bonitas e acessíveis.

**Entregáveis:**
- Wireframes e fluxos de usuário
- Mockups hi-fi no Figma usando design system
- Protótipos interativos para validação
- Specs de handoff completos (todos os estados, responsivo, tokens)
- Participação em design reviews e critique sessions

**Interface com outros papéis:**
- Com PM: alinhamento de escopo, priorização, trade-offs
- Com Engenharia: handoff, QA visual, alinhamento técnico
- Com UX Researcher: definição de research questions, participação em testes
- Com UX Writer: revisão de microcopy, alinhamento de tom
- Com DS Engineer: proposta de novos componentes, feedback de API

**Diferença entre Senior e Pleno:**
- Senior lidera features complexas com autonomia total e mentorea plenos
- Pleno executa features com suporte, escala complexidade com o tempo
- Senior influencia estratégia de produto; pleno foca em execução

### UX Researcher

**Responsabilidade central:** Gerar insights acionáveis sobre comportamento,
necessidades e contextos dos usuários.

**Entregáveis:**
- Planos de pesquisa (objetivos, métodos, cronograma)
- Relatórios de pesquisa com insights priorizados
- Personas e journey maps baseados em dados
- Facilitação de testes de usabilidade
- Repository de insights searchable e atualizado

**Interface com outros papéis:**
- Com Product Designer: insights para informar design, co-análise
- Com PM: definição de research questions, priorização de estudos
- Com Data/Analytics: correlação entre quali e quanti
- Com Stakeholders: readouts de pesquisa, advocacy de UX

### UX Writer

**Responsabilidade central:** Garantir que toda comunicação textual do produto
seja clara, consistente e centrada no usuário.

**Entregáveis:**
- Microcopy para interfaces (labels, mensagens, tooltips)
- Content guidelines e voice chart
- Revisão de copy em features antes de handoff
- Biblioteca de frases reutilizáveis
- Glossário de termos do produto

**Interface com outros papéis:**
- Com Product Designer: copy integrada ao design desde o início
- Com Marketing: alinhamento de brand voice entre produto e comunicação
- Com Engenharia: strings de texto corretas no handoff
- Com Suporte: alinhamento de linguagem entre produto e SAC

### Design System Engineer

**Responsabilidade central:** Manter e evoluir o design system como produto —
componentes, tokens, documentação e tooling.

**Entregáveis:**
- Componentes Figma alinhados com componentes code
- Token architecture (primitive, semantic, component)
- Documentação de componentes (usage, API, a11y)
- Tooling de automação (token sync, linting, audits)
- Release notes e migration guides

**Interface com outros papéis:**
- Com Product Designers: suporte na criação de componentes, review de uso
- Com Front-end Engineers: component APIs, token sync, PR reviews
- Com QA: visual regression testing, a11y audit automation
- Com Design Lead: roadmap e governance do DS

### Design Ops

**Responsabilidade central:** Otimizar processos, ferramentas e métricas do
Design Squad para maximizar eficiência e qualidade.

**Entregáveis:**
- Dashboards de métricas de design
- Facilitação de rituais (critique, retros, planning)
- Gestão de ferramentas e licenças
- Processo de onboarding estruturado
- Reports de produtividade e qualidade

**Interface com outros papéis:**
- Com todos: facilitação de processos e remoção de bloqueios
- Com Finance: gestão de budget de ferramentas
- Com HR: suporte em hiring e onboarding
- Com Design Lead: métricas e insights de operação

### Design Lead

**Responsabilidade central:** Direção estratégica do design, qualidade das
entregas, desenvolvimento do time e interface com liderança.

**Entregáveis:**
- Visão e roadmap de design alinhado com produto
- Mentoria e desenvolvimento de carreira do time
- Participação em decisões estratégicas de produto
- Governance do design system
- Reports de impacto de design para liderança

## Cross-References

- `docs/squad-overview.md` — Contexto do squad
- `docs/workflow-guide.md` — Como os papéis interagem no fluxo de trabalho
- `docs/design-review-standards.md` — Papel de cada um nas reviews
- `docs/contribution-guide.md` — Como contribuir com o squad
