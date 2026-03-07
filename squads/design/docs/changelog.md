# Changelog

## Overview

Registro de mudanças significativas nos processos, ferramentas, padrões e artefatos
do Design Squad. Organizado em ordem cronológica reversa (mais recente primeiro).
Cada entrada registra o que mudou, por que mudou e quem é o ponto de contato.

## Content

### Formato de Entrada

Cada mudança segue o formato:
```
### [AAAA-MM-DD] — [Título da Mudança]
**Tipo:** [Processo | Ferramenta | Padrão | Documento | Design System]
**Impacto:** [Alto | Médio | Baixo]
**Owner:** [Nome]

[Descrição da mudança — o que mudou e por que]

**Ação necessária:** [O que os membros precisam fazer, se algo]
```

### 2026

### [2026-03-06] — Criação da Base Documental do Design Squad
**Tipo:** Documento
**Impacto:** Alto
**Owner:** Design Lead

Criação do conjunto completo de documentação do Design Squad incluindo:
- 22 arquivos de voice (tone profiles, language guides, calibration, channel adaptation)
- 18 arquivos de phrases (bibliotecas de frases e microcopy)
- 18 arquivos de docs (guias, padrões, políticas)
- 15 arquivos de scripts (automação e processos)

Esta é a versão 1.0 da base documental. Todos os membros devem ler os documentos
relevantes ao seu papel (ver `getting-started.md` para guia).

**Ação necessária:** Todos — ler `getting-started.md` e documentos do seu papel

### [2026-03-01] — Adoção do Gold Standard
**Tipo:** Padrão
**Impacto:** Alto
**Owner:** Design Lead

Definição formal do Gold Standard para todas as dimensões de qualidade do squad.
Métricas e targets documentados em `gold-standard-and-sota.md`. Audit trimestral
a partir de Q2 2026.

**Ação necessária:** Todos — familiarizar-se com métricas e targets

### [2026-02-15] — Atualização da Política de Acessibilidade
**Tipo:** Padrão
**Impacto:** Alto
**Owner:** Design Lead

Target de WCAG 2.2 AA atualizado: 80% até Q2 2026, 95% até Q4 2026. Checklist de
a11y integrado ao Definition of Done. Scripts de automação disponíveis.

**Ação necessária:** Designers — incluir a11y checklist em todo handoff

### [2026-02-01] — Novo Workflow de Design Review
**Tipo:** Processo
**Impacto:** Médio
**Owner:** Design Lead

Introdução de 4 tipos de review (Peer Critique, Stakeholder, A11y, DS Consistency)
com critérios e templates específicos. Design critique semanal às terças.

**Ação necessária:** Designers — seguir novo processo de review

### [2026-01-15] — Migração de Token Architecture
**Tipo:** Design System
**Impacto:** Alto
**Owner:** DS Engineer

Migração de flat token namespace para 3-layer architecture (primitive, semantic,
component). Migration guide disponível. Breaking change na v3.0.0 do DS.

**Ação necessária:** Todos os consumers — migrar tokens até 2026-03-31

### [2026-01-01] — Início do Design Squad v2
**Tipo:** Processo
**Impacto:** Alto
**Owner:** Design Lead

Reestruturação do Design Squad com modelo embedded + centralized. Novos rituais,
cadências e métricas implementados. Documentação inicial criada.

**Ação necessária:** Todos — participar do kickoff e ler docs iniciais

### Como Adicionar Entradas

- Qualquer membro pode adicionar entradas para mudanças no seu escopo
- Mudanças de impacto Alto devem ser comunicadas no #design-squad
- Manter ordem cronológica reversa
- Incluir sempre: data, tipo, impacto, owner, descrição, ação necessária

## Cross-References

- `docs/gold-standard-and-sota.md` — Padrões de qualidade
- `docs/operating-system.md` — Sistema operacional do squad
- `docs/design-system-governance.md` — Governança do DS
