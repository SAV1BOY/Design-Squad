# Design System Audit Template

## Informacoes da Auditoria

| Campo | Valor |
|-------|-------|
| **Versao Atual do DS** | [ex. v3.2.1] |
| **Auditor** | [Nome] |
| **Data de Inicio** | [YYYY-MM-DD] |
| **Data de Conclusao** | [YYYY-MM-DD] |
| **Escopo** | [Completo / Parcial — especificar] |

## Objetivo da Auditoria

Avaliar o estado atual do Design System para identificar gaps,
inconsistencias e oportunidades de melhoria que devem ser
enderecados no proximo upgrade.

## Metodologia

### Fontes de Dados

- [ ] Repositorio do Design System (GitHub)
- [ ] Biblioteca Figma
- [ ] Storybook
- [ ] Documentacao existente
- [ ] Feedback de usuarios (designers e devs)
- [ ] Analytics de uso de componentes

### Criterios de Avaliacao

| Criterio | Peso | Descricao |
|----------|------|-----------|
| Consistencia visual | Alto | Aderencia aos tokens e padroes |
| Acessibilidade | Alto | Conformidade WCAG 2.1 AA |
| Completude de API | Medio | Props e variantes disponíveis |
| Documentacao | Medio | Qualidade e atualidade da docs |
| Performance | Medio | Bundle size e render performance |
| Adocao | Alto | Percentual de uso em produtos |

## Auditoria de Tokens

### Design Tokens

| Categoria | Total | Consistentes | Inconsistentes | Sem Uso |
|-----------|-------|-------------|---------------|---------|
| Colors | [N] | [N] | [N] | [N] |
| Typography | [N] | [N] | [N] | [N] |
| Spacing | [N] | [N] | [N] | [N] |
| Shadows | [N] | [N] | [N] | [N] |
| Border Radius | [N] | [N] | [N] | [N] |
| Breakpoints | [N] | [N] | [N] | [N] |

### Problemas Encontrados em Tokens

| Token | Problema | Severidade | Recomendacao |
|-------|---------|-----------|-------------|
| [token] | [descricao] | [Alta/Media/Baixa] | [recomendacao] |

## Auditoria de Componentes

### Resumo por Categoria

| Categoria | Total | Atualizados | Desatualizados | Deprecated |
|-----------|-------|------------|---------------|-----------|
| Forms | [N] | [N] | [N] | [N] |
| Navigation | [N] | [N] | [N] | [N] |
| Data Display | [N] | [N] | [N] | [N] |
| Feedback | [N] | [N] | [N] | [N] |
| Layout | [N] | [N] | [N] | [N] |
| Overlay | [N] | [N] | [N] | [N] |

### Avaliacao Individual de Componentes

| Componente | Versao | a11y | Docs | Adocao | Score |
|-----------|--------|------|------|--------|-------|
| Button | [ver] | [1-5] | [1-5] | [%] | [media] |
| Input | [ver] | [1-5] | [1-5] | [%] | [media] |
| Select | [ver] | [1-5] | [1-5] | [%] | [media] |
| Modal | [ver] | [1-5] | [1-5] | [%] | [media] |
| Toast | [ver] | [1-5] | [1-5] | [%] | [media] |
| Card | [ver] | [1-5] | [1-5] | [%] | [media] |
| Table | [ver] | [1-5] | [1-5] | [%] | [media] |

## Auditoria de Acessibilidade

### Resumo

| Nivel WCAG | Total Issues | Critico | Major | Minor |
|------------|-------------|---------|-------|-------|
| A | [N] | [N] | [N] | [N] |
| AA | [N] | [N] | [N] | [N] |
| AAA | [N] | [N] | [N] | [N] |

### Issues Encontrados

| Componente | Issue | WCAG Criteria | Severidade |
|-----------|-------|--------------|-----------|
| [comp] | [descricao] | [criterio] | [sev] |

## Auditoria de Documentacao

| Aspecto | Status | Observacao |
|---------|--------|-----------|
| Getting started guide | [Atualizado/Desatualizado/Ausente] | [obs] |
| Component API docs | [Atualizado/Desatualizado/Ausente] | [obs] |
| Design guidelines | [Atualizado/Desatualizado/Ausente] | [obs] |
| Migration guides | [Atualizado/Desatualizado/Ausente] | [obs] |
| Changelog | [Atualizado/Desatualizado/Ausente] | [obs] |
| Contributing guide | [Atualizado/Desatualizado/Ausente] | [obs] |

## Gap Analysis

### Componentes Faltantes

Componentes frequentemente solicitados ou custom-built pelos times.

| Componente | Solicitacoes | Times Afetados | Prioridade |

---
