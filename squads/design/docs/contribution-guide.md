# Contribution Guide

## Overview

Guia para contribuições ao Design Squad — seja por membros internos, designers de
outros squads ou qualquer pessoa na organização. Contribuições podem ser propostas
de componentes, correções de documentação, feedback de processos ou novas ideias.

## Content

### Tipos de Contribuição

| Tipo | Quem pode | Processo |
|------|-----------|----------|
| Bug report (visual) | Qualquer pessoa | Abrir ticket com screenshot |
| Sugestão de melhoria UX | Qualquer pessoa | Post no #design-reviews |
| Proposta de componente DS | Designers | RFC via template |
| Fix de documentação | Qualquer pessoa | PR direto ou post no Slack |
| Novo documento/guide | Membros do squad | Proposta ao design lead |
| Melhoria de processo | Membros do squad | Discussão na retro |
| Contribuição de pesquisa | Designers + Researchers | Seguir research-standards.md |

### Como Contribuir com o Design System

#### 1. Identificar a necessidade
- O componente é usado por 2+ squads ou 3+ contextos?
- Não é coberto por componente existente (verificar Storybook)?
- Não é específico de domínio?

#### 2. Abrir uma Proposal
Postar no #design-system com:
```
**Proposta:** [Nome do componente]
**Problema:** [O que não é coberto hoje]
**Use cases:** [Onde seria usado — squads e contextos]
**Alternativa atual:** [Como está sendo resolvido hoje]
**Referências:** [Exemplos em outros DS ou produtos]
```

#### 3. Escrever RFC (se aprovado)
Documento detalhado seguindo template:
```
# RFC: [Nome do Componente]

## Problema
[Descrição detalhada]

## Proposta
[Design + API proposta]

## Variantes
[Quais variantes são necessárias]

## Acessibilidade
[Requisitos de a11y]

## Tokens
[Tokens novos necessários]

## Trade-offs
[Prós e contras]

## Alternativas consideradas
[O que mais foi avaliado]
```

#### 4. Review e Aprovação
- Período de feedback: 1 semana
- Aprovação do DS Committee necessária
- Feedback de consumers (mínimo 2 squads)

#### 5. Implementação
- Design no Figma seguindo naming conventions
- Code implementation com testes
- Documentação completa
- A11y review

### Como Reportar Bugs Visuais

Template de bug report:
```
**Componente/Tela:** [Nome]
**Ambiente:** [Browser, viewport, OS]
**Esperado:** [O que deveria ser — screenshot do Figma]
**Encontrado:** [O que está — screenshot da implementação]
**Severidade:** [Blocker / Major / Minor / Polish]
**Passos para reproduzir:** [Se aplicável]
```

### Como Sugerir Melhorias de UX

Qualquer pessoa na organização pode sugerir melhorias:

1. Postar no #design-reviews com:
   - Screenshot ou gravação do problema
   - Descrição do impacto no usuário
   - Sugestão de melhoria (opcional)
2. Designer alocado avalia e responde em até 48h
3. Se aprovado, entra no backlog com prioridade definida

### Como Contribuir com Documentação

- **Erros e typos:** Corrigir direto (PR ou edição na wiki)
- **Conteúdo desatualizado:** Notificar o owner do documento
- **Novo conteúdo:** Propor ao design lead com outline do que seria escrito
- **Templates:** Sugerir via #design-squad com exemplo de uso

### Código de Conduta para Contribuições

1. **Respeito:** Toda contribuição é valorizada, mesmo se não for aceita
2. **Construtividade:** Feedback sobre contribuições deve ser específico e acionável
3. **Paciência:** O processo de review leva tempo — é para garantir qualidade
4. **Documentação:** Se contribuiu, documente. Código sem doc não é contribuição
5. **Acessibilidade:** Toda contribuição visual deve considerar a11y

### Reconhecimento

- Contribuidores são creditados nas release notes
- Top contribuidores reconhecidos no all-hands trimestral
- Contribuições significativas contam para avaliação de performance

## Cross-References

- `docs/design-system-governance.md` — Processo detalhado do DS
- `docs/naming-conventions.md` — Convenções a seguir
- `docs/accessibility-policy.md` — Requisitos de a11y
- `phrases/design-system-contribution.md` — Frases para comunicação
