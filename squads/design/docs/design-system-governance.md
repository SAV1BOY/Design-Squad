# Design System Governance

## Overview

Modelo de governança do Design System — como componentes são propostos, avaliados,
aprovados, versionados e deprecados. A governança equilibra velocidade de evolução
com estabilidade para os consumidores.

## Content

### Princípios de Governança

1. **O DS é um produto** — Tem roadmap, backlog, releases e consumers
2. **Contribuição aberta, merge controlado** — Qualquer squad pode propor, o DS committee aprova
3. **Estabilidade é prioridade** — Breaking changes são planejados e comunicados com antecedência
4. **Documentação é parte da entrega** — Componente sem doc não é componente publicado
5. **Acessibilidade é requisito** — Componente sem a11y review não passa para stable

### Ciclo de Vida de Componente

```
Proposal → RFC → Design Review → Build → A11y Review → Beta → Stable → Deprecated → Removed
```

#### 1. Proposal
- Qualquer membro pode propor via template no canal #design-system
- Incluir: problema que resolve, use cases, alternativas existentes
- Avaliação em até 5 dias úteis pelo DS committee

#### 2. RFC (Request for Comments)
- Documento detalhado com specs, API proposta e trade-offs
- Período de feedback aberto: 1 semana
- Feedback de consumers é obrigatório (mínimo 2 squads)

#### 3. Design Review
- Review do componente no Figma pelo DS committee
- Critérios: consistência, flexibilidade, naming, documentação
- Aprovação necessária para prosseguir para build

#### 4. Build
- Implementação em Figma (design) e código (engineering)
- Figma e code devem estar sincronizados antes de avançar
- Testes unitários e visual regression tests obrigatórios

#### 5. A11y Review
- Audit de acessibilidade com checklist específico do componente
- Keyboard navigation, screen reader, contrast, focus management
- Aprovação do a11y reviewer necessária

#### 6. Beta
- Disponível para uso com flag de "beta" — API pode mudar
- Período mínimo de 2 sprints em beta
- Feedback de consumers reais coletado e incorporado

#### 7. Stable
- API congelada — breaking changes apenas em major version
- Documentação completa publicada (Storybook + Figma)
- Anúncio em #design-system com exemplos de uso

#### 8. Deprecated → Removed
- Aviso com 2 major versions de antecedência
- Migration guide publicada antes da deprecation
- Codemod fornecido quando possível
- Remoção do bundle após período de grace de 1 quarter

### DS Committee

**Composição:**
- Design Lead (chair)
- DS Engineer
- 1 Product Designer representando consumers
- Rotação trimestral do representante de consumers

**Responsabilidades:**
- Avaliar proposals e RFCs
- Aprovar breaking changes
- Definir roadmap trimestral do DS
- Resolver conflitos de prioridade

**Reuniões:**
- Sync quinzenal: review de proposals e roadmap
- Ad-hoc: decisões urgentes via Slack async

### Versionamento

Seguimos Semantic Versioning (SemVer):
- **Major (X.0.0):** Breaking changes — APIs removidas ou alteradas
- **Minor (0.X.0):** Novas features — novos componentes ou props
- **Patch (0.0.X):** Bug fixes — correções sem mudança de API

### Critérios para Inclusão no DS

Um componente deve atender TODOS os critérios:
- [ ] Usado por 2+ squads ou 3+ contextos diferentes
- [ ] Não é específico de domínio (não é "ProductCard" se só 1 produto tem products)
- [ ] Tem design e code sincronizados
- [ ] Documentação completa (usage, API, a11y, examples)
- [ ] A11y review aprovada
- [ ] Visual regression tests implementados

## Cross-References

- `docs/accessibility-policy.md` — Política de acessibilidade
- `docs/naming-conventions.md` — Convenções de nomenclatura
- `docs/contribution-guide.md` — Como contribuir
- `phrases/design-system-contribution.md` — Frases para comunicação sobre DS
