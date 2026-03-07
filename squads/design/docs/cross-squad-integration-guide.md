# Cross-Squad Integration Guide

## Overview

Guia para integração do Design Squad com outros squads da organização. O design
opera como serviço compartilhado — atende múltiplos squads de produto mantendo
consistência e qualidade. Este guia define como essa interface funciona.

## Content

### Modelo de Atendimento

O Design Squad opera em modelo **embedded + centralized**:
- Designers são alocados a squads de produto (embedded) para proximidade
- Mas pertencem ao Design Squad (centralized) para consistência e desenvolvimento

**Proporção:** 1 designer para cada 1-2 squads de produto (dependendo da complexidade)

### Interface com Squads de Produto

#### Como solicitar design
1. PM cria request no board compartilhado com template preenchido
2. Design Lead avalia prioridade e aloca designer em até 2 dias úteis
3. Kickoff de alinhamento (30 min) entre PM, designer e dev lead
4. Designer segue o workflow padrão (ver `workflow-guide.md`)

#### Template de Request
```
## Design Request — [Nome da Feature]

**Squad:** [Nome do squad]
**PM:** [Nome]
**Prioridade:** [P0/P1/P2/P3]
**Deadline desejado:** [Data]

**Problema:** [O que precisa ser resolvido]
**Contexto:** [Dados, pesquisas, feedback que motivam]
**Escopo:** [O que está incluído e excluído]
**Métrica de sucesso:** [Como vamos medir]
**Dependências:** [Outros times, APIs, conteúdo]
```

#### SLAs de Atendimento

| Prioridade | Início do trabalho | Entrega estimada |
|-----------|-------------------|-----------------|
| P0 (Crítico) | Mesmo dia | 1-2 dias |
| P1 (Urgente) | 1-2 dias | 3-5 dias |
| P2 (Normal) | 3-5 dias | 1-2 sprints |
| P3 (Nice-to-have) | Próximo sprint | 2-3 sprints |

### Interface com Engineering

#### Rituais compartilhados
- **Sprint Planning:** Designer participa para alinhar escopo e estimar design
- **Daily:** Designer participa para acompanhar implementação e tirar dúvidas
- **Sprint Review:** Designer apresenta resultado visual
- **Retro:** Designer participa para feedback bidirecional

#### Protocolo de handoff
- Ver `handoff-standards.md` para detalhamento completo
- Designer disponível para dúvidas durante todo o sprint de implementação
- QA visual pelo designer antes de merge

### Interface com QA

- Designer define critérios visuais de aceite nos tickets
- QA usa screenshots do Figma como referência
- Designer disponível para esclarecer ambiguidades durante teste
- Bugs visuais retornam ao designer para avaliação de severidade

### Interface com Marketing e Brand

- Alinhamento trimestral sobre brand guidelines
- UX Writer participa de reviews de brand voice
- Design system compartilha tokens de cor e tipografia com brand
- Campanhas que impactam produto passam por review do Design Squad

### Interface com Suporte/CS

- Design Squad recebe relatório mensal de issues UX reportadas pelo suporte
- Suporte é convidado para readouts de pesquisa relevantes
- Mudanças de UX significativas são comunicadas ao suporte antes do lançamento
- Feedback de suporte alimenta backlog de design debt

### Resolução de Conflitos

| Conflito | Quem resolve |
|----------|-------------|
| Prioridade entre squads | Design Lead + PM Lead |
| Escopo de design vs. prazo | PM do squad + Designer |
| Padrão de DS vs. necessidade do squad | DS Committee |
| Qualidade vs. velocidade | Design Lead tem última palavra em qualidade |

### Communication Channels

| Tipo de comunicação | Canal |
|--------------------|-------|
| Request de design | Board compartilhado (Jira/Linear) |
| Updates de progresso | Slack canal do squad |
| Feedback de implementação | Slack + Figma comments |
| Escalação | DM com Design Lead |
| Design system questions | #design-system |

## Cross-References

- `docs/squad-overview.md` — Estrutura do Design Squad
- `docs/workflow-guide.md` — Fluxo de trabalho
- `docs/handoff-standards.md` — Padrões de entrega
- `voice/language-guides/stakeholder-communication.md` — Comunicação com stakeholders
