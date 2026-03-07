# Testing Plan Template

## Informacoes do Projeto

| Campo | Valor |
|-------|-------|
| **Design System Version** | [ex. v4.0.0] |
| **QA Lead** | [Nome] |
| **Data de Inicio** | [YYYY-MM-DD] |
| **Data de Conclusao** | [YYYY-MM-DD] |
| **Ambiente de Teste** | [Staging / Preview] |

## Objetivo do Plano de Testes

Garantir que o upgrade do Design System nao introduza regressoes
visuais, funcionais ou de acessibilidade, e que todos os componentes
novos ou atualizados funcionem conforme especificado.

## Escopo de Testes

### Em Escopo

- [ ] Testes de regressao visual de todos os componentes
- [ ] Testes funcionais de componentes atualizados
- [ ] Testes de acessibilidade (WCAG 2.1 AA)
- [ ] Testes de responsividade em todos os breakpoints
- [ ] Testes cross-browser
- [ ] Testes de performance (bundle size, render time)
- [ ] Testes de migracao (codemods e compatibility layer)

### Fora do Escopo

- [Item 1 — justificativa]
- [Item 2 — justificativa]

## Estrategia de Testes

### Piramide de Testes

```
        /  E2E  \          ← Testes end-to-end em produtos piloto
       / Integr.  \        ← Testes de integracao entre componentes
      / Componente  \      ← Testes unitarios por componente
     /  Visual Regr.  \    ← Testes de regressao visual automatizados
    /____a11y Audit_____\  ← Auditoria de acessibilidade
```

### Tipos de Teste

| Tipo | Ferramenta | Responsavel | Automatizado |
|------|-----------|-------------|-------------|
| Visual Regression | Chromatic | QA Team | Sim |
| Unit Tests | Jest + Testing Library | Dev Team | Sim |
| a11y Testing | axe-core + manual | QA + Design | Hibrido |
| Cross-browser | BrowserStack | QA Team | Parcial |
| Performance | Lighthouse + bundlesize | Dev Team | Sim |
| Integration | Cypress | QA Team | Sim |
| Usability | Manual | Design Team | Nao |

## Matriz de Testes por Componente

### Componentes Atualizados

| Componente | Visual | Funcional | a11y | Responsive | Performance |
|-----------|--------|----------|------|-----------|-------------|
| Button | [ ] | [ ] | [ ] | [ ] | [ ] |
| Input | [ ] | [ ] | [ ] | [ ] | [ ] |
| Select | [ ] | [ ] | [ ] | [ ] | [ ] |
| Modal | [ ] | [ ] | [ ] | [ ] | [ ] |
| Table | [ ] | [ ] | [ ] | [ ] | [ ] |
| Toast | [ ] | [ ] | [ ] | [ ] | [ ] |
| Tabs | [ ] | [ ] | [ ] | [ ] | [ ] |

### Componentes Novos

| Componente | Visual | Funcional | a11y | Responsive | Performance |
|-----------|--------|----------|------|-----------|-------------|
| [Comp] | [ ] | [ ] | [ ] | [ ] | [ ] |

## Testes de Acessibilidade

### Checklist por Componente

Para cada componente, verificar:

- [ ] Keyboard navigation funcional
- [ ] Focus management correto
- [ ] Screen reader compatibility (VoiceOver + NVDA)
- [ ] Color contrast (4.5:1 texto normal, 3:1 texto grande)
- [ ] ARIA attributes corretos
- [ ] Reduced motion respeitado
- [ ] High contrast mode suportado

### Ferramentas de a11y Testing

| Ferramenta | Tipo | Cobertura |
|-----------|------|-----------|
| axe-core | Automatizado | ~30% dos issues |
| Lighthouse a11y | Automatizado | ~20% dos issues |
| VoiceOver (macOS) | Manual | Screen reader |
| NVDA (Windows) | Manual | Screen reader |
| Keyboard only | Manual | Navegacao |

## Testes Cross-Browser

### Matriz de Browsers

| Browser | Versao | Desktop | Mobile | Prioridade |
|---------|--------|---------|--------|-----------|
| Chrome | Latest + 1 | [ ] | [ ] | P0 |
| Firefox | Latest + 1 | [ ] | [ ] | P0 |
| Safari | Latest + 1 | [ ] | [ ] | P0 |
| Edge | Latest + 1 | [ ] | [ ] | P1 |
| Samsung Internet | Latest | - | [ ] | P2 |

## Testes de Performance

### Metricas e Thresholds

---
