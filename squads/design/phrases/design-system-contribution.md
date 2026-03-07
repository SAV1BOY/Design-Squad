# Design System Contribution

## Context

Frases prontas para comunicar sobre contribuições ao design system — propostas de
novos componentes, updates de tokens, breaking changes, deprecations e governance.
O design system é um produto compartilhado; comunicar mudanças com clareza e
antecedência é essencial para manter a confiança dos consumidores.

**Aplicação:** PRs, release notes, announcements, RFC docs
**Tom:** System Thinker + Pragmatic Builder

## Phrases

### Propondo novo componente
- "Proponho adicionar [componente] ao design system. Justificativa: é usado em [N] squads com [N] variações inconsistentes."
- "Este componente foi extraído do [squad/produto] e generalizado. Cobre [N] use cases identificados."
- "RFC aberta para o componente [nome]. Feedback até [data]. Specs no Figma: [link]. API proposta: [link]."
- "O componente resolve [problema]. Sem ele, cada squad implementa sua versão — hoje temos [N] variações incompatíveis."

### Anunciando release
- "DS Release v[X.Y.Z] disponível. [N] novos componentes, [M] updates, [K] bug fixes."
- "Novo componente: [nome]. Documentação: [link]. Storybook: [link]. Figma: [link]."
- "Update de tokens: [lista de mudanças]. Sem breaking changes — atualizar sem risco."
- "Bug fix: [componente] — [descrição do fix]. Atualizar para v[X.Y.Z] para receber a correção."

### Comunicando breaking changes
- "BREAKING CHANGE na v[X.0.0]: [descrição]. Migration guide: [link]. Deadline para migração: [data]."
- "O componente [nome] foi renomeado de [antigo] para [novo]. Alias de compatibilidade disponível até [data]."
- "Token [antigo] foi deprecado em favor de [novo]. Codemod disponível: `npx ds-migrate [comando]`."
- "A API do [componente] mudou: prop [antiga] substituída por [nova]. Razão: [justificativa]."
- "Prazo para migração: [N] sprints. Suporte durante a migração no canal #design-system."

### Deprecating componentes
- "O componente [nome] será deprecado na v[X]. Substituir por [alternativa]. Razão: [justificativa]."
- "Timeline de deprecation: v[X] — warning no console. v[Y] — remoção do bundle. v[Z] — remoção do Figma."
- "[Componente] não receberá mais updates. Recomendação: migrar para [alternativa] que tem [vantagem]."

### Respondendo pedidos de componente
- "Esse use case é coberto pelo [componente existente] com a prop [prop]. Exemplo: [link]."
- "Avaliamos o pedido. Não será adicionado ao DS porque [razão]. Recomendação: implementar no squad."
- "Boa sugestão. Adicionei ao backlog do DS com prioridade [P]. Previsão: [quarter]."
- "O pedido faz sentido, mas precisa de mais contexto. Quantos squads precisam? Quais variações?"

### Governança e contribuição
- "Para contribuir com o design system, siga o guia em [link]. O processo é: proposal → RFC → review → merge."
- "Contribuições de qualquer squad são bem-vindas. O requisito mínimo é: documentação, testes, a11y review."
- "O design system tem office hours toda [dia] às [hora]. Traga dúvidas, propostas ou feedback."
- "O comitê de design system se reúne [frequência] para avaliar proposals. Submeta até [prazo]."

## Variations

- Para desenvolvedores: foco em API changes, migration paths, codemods
- Para designers: foco em Figma updates, novos patterns, guidelines
- Para PMs: foco em impacto do DS na velocidade de entrega e consistência
- Para release notes públicas: formato conciso com categorias (New, Changed, Fixed, Deprecated)

## When to Use

- Anúncios de release do design system
- RFCs para novos componentes ou mudanças significativas
- Comunicação de breaking changes com timeline de migração
- Respostas a pedidos de componentes ou features do DS
- Documentação de governança e processo de contribuição
