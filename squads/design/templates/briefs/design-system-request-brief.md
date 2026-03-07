# Design System Request Brief

## Metadata

| Campo                | Valor                                           |
|----------------------|--------------------------------------------------|
| **Componente / Token** | [PREENCHER — nome do componente ou token]      |
| **Solicitante**      | [PREENCHER — nome e squad]                       |
| **Tipo de request**  | [PREENCHER — Novo / Modificacao / Deprecacao]    |
| **Data de criacao**  | [PREENCHER — YYYY-MM-DD]                         |
| **Status**           | [PREENCHER — Submetido / Em analise / Aprovado / Rejeitado] |
| **Prioridade**       | [PREENCHER — Critica / Alta / Media / Baixa]     |
| **DS Version alvo**  | [PREENCHER — versao do design system]            |

## Instructions (Como Usar)

1. Preencha este brief ao solicitar qualquer mudanca no design system.
2. Envie o brief preenchido ao time de Design System pelo canal designado (Slack / Jira).
3. O time de DS fara a triagem e retornara com perguntas ou aprovacao.
4. Apos aprovacao, o componente entra no backlog de desenvolvimento do DS.
5. Acompanhe o status no board do Design System.

> **Dica:** Inclua prints ou links de Figma para facilitar a analise. Quanto mais visual, melhor.

## Template

### 1. Descricao da Solicitacao

[PREENCHER — descreva o que voce precisa. Se e um novo componente, descreva o comportamento esperado. Se e uma modificacao, descreva o que precisa mudar e por que.]

### 2. Justificativa / Problema

[PREENCHER — por que esta mudanca e necessaria? Que problema ela resolve? Quantos squads/produtos se beneficiariam?]

**Impacto estimado:**
- Squads afetados: [PREENCHER — numero e nomes]
- Paginas/telas afetadas: [PREENCHER — estimativa]
- Usuarios impactados: [PREENCHER — estimativa]

### 3. Casos de Uso

| # | Caso de uso                                    | Squad / Contexto        |
|---|------------------------------------------------|-------------------------|
| 1 | [PREENCHER — onde/como o componente sera usado]| [PREENCHER]             |
| 2 | [PREENCHER — caso de uso alternativo]          | [PREENCHER]             |
| 3 | [PREENCHER — edge case]                        | [PREENCHER]             |

### 4. Comportamento Esperado

**Estados do componente:**
- Default: [PREENCHER — descricao do estado]
- Hover: [PREENCHER — descricao do estado]
- Active/Pressed: [PREENCHER — descricao do estado]
- Disabled: [PREENCHER — descricao do estado]
- Error: [PREENCHER — descricao do estado]
- Loading: [PREENCHER — descricao ou N/A]

**Variantes necessarias:**
- [PREENCHER — variante 1, ex.: size small / medium / large]
- [PREENCHER — variante 2, ex.: filled / outlined / ghost]

### 5. Requisitos de Acessibilidade

- [ ] Navegacao por teclado: [PREENCHER — comportamento esperado]
- [ ] Screen reader: [PREENCHER — labels e anuncios]
- [ ] Contraste minimo: [PREENCHER — ratio WCAG AA / AAA]
- [ ] Focus indicator: [PREENCHER — estilo de foco]
- [ ] Reducao de motion: [PREENCHER — comportamento sem animacao]

### 6. Referencias Visuais

| Referencia                 | Link                              |
|----------------------------|-----------------------------------|
| Mockup / Proposta visual   | [PREENCHER — link Figma]          |
| Componente similar no DS   | [PREENCHER — nome e link]         |
| Referencia externa         | [PREENCHER — link Material/Ant/etc.] |
| Print do contexto de uso   | [PREENCHER — link imagem]         |

### 7. Compatibilidade

- **Plataformas:** [PREENCHER — Web / iOS / Android / Todas]
- **Frameworks:** [PREENCHER — React / Vue / Swift / Kotlin / Todos]
- **Breakpoints:** [PREENCHER — comportamento responsivo esperado]
- **Themes:** [PREENCHER — Light / Dark / Ambos]

### 8. Timeline Desejada

| Marco                  | Data desejada     | Flexibilidade       |
|------------------------|-------------------|----------------------|
| Aprovacao do request   | [PREENCHER]       | [PREENCHER]          |
| Design spec pronta     | [PREENCHER]       | [PREENCHER]          |
| Implementacao          | [PREENCHER]       | [PREENCHER]          |
| Release                | [PREENCHER]       | [PREENCHER]          |

## Example (Parcialmente Preenchido)

**Componente:** DateRangePicker
**Tipo:** Novo componente
**Solicitante:** Marina Costa — Squad Analytics

**Justificativa:** 4 squads diferentes implementaram date pickers customizados com comportamentos inconsistentes. Um componente padrao reduziria re-trabalho e melhoraria a consistencia.

**Caso de uso 1:** Filtro de periodo em dashboards de analytics.
**Variantes:** Single date / Date range / Preset ranges (7d, 30d, 90d).

## Notes

- Requests sem justificativa clara podem ser devolvidos para complementacao.
- O time de DS prioriza requests com maior impacto cross-squad.
- Se o componente ja existe mas nao atende seu caso de uso, descreva exatamente o gap.
- Para urgencias, contate o DS lead diretamente alem de submeter o brief.
- Consulte o catalogo atual do DS antes de submeter para evitar duplicacoes.
