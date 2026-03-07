# Accessibility Remediation Project Template

## Overview

Template para projetos de remediacao de acessibilidade (a11y).
Este conjunto de documentos guia o time desde a identificacao de
problemas ate a conformidade com os padroes WCAG 2.1.

## Estrutura do Template

| Arquivo | Descricao | Fase |
|---------|-----------|------|
| `audit-findings.md` | Findings da auditoria de a11y | Assessment |
| `prioritization-matrix.md` | Matriz de priorizacao | Planejamento |
| `remediation-tracker.md` | Tracker de remediacao | Execucao |
| `compliance-report.md` | Relatorio de compliance | Verificacao |

## Como Usar

1. Conduza a auditoria de acessibilidade e registre findings
2. Priorize os issues usando a matriz de priorizacao
3. Acompanhe a remediacao usando o tracker
4. Documente o nivel de conformidade no relatorio final

## Fluxo do Projeto

```
Audit → Prioritization → Remediation → Verification → Compliance Report
```

## Padroes de Referencia

### WCAG 2.1

O Web Content Accessibility Guidelines e o padrao principal.
Os niveis de conformidade sao:

| Nivel | Descricao | Obrigatorio? |
|-------|-----------|-------------|
| **A** | Requisitos basicos de acessibilidade | Sim |
| **AA** | Requisitos recomendados (padrao do mercado) | Sim |
| **AAA** | Requisitos avancados | Recomendado |

### Legislacao Relevante

| Legislacao | Ambito | Requisito |
|-----------|--------|----------|
| LBI (Lei 13.146/2015) | Brasil | Acessibilidade digital obrigatoria |
| ADA | EUA | Section 508 compliance |
| EN 301 549 | Europa | Conformidade WCAG 2.1 AA |

## Ferramentas Recomendadas

### Testes Automatizados

| Ferramenta | Tipo | Cobertura |
|-----------|------|-----------|
| axe DevTools | Browser extension | ~30% dos issues |
| Lighthouse | Chrome DevTools | ~20% dos issues |
| WAVE | Browser extension | ~25% dos issues |
| Pa11y | CLI / CI | ~25% dos issues |
| jest-axe | Unit test | Per-component |

### Testes Manuais

| Ferramenta | Tipo | Uso |
|-----------|------|-----|
| VoiceOver | Screen reader (macOS/iOS) | Teste de leitura de tela |
| NVDA | Screen reader (Windows) | Teste de leitura de tela |
| TalkBack | Screen reader (Android) | Teste mobile |
| Colour Contrast Analyser | Desktop app | Verificacao de contraste |
| Keyboard only | Navegacao | Teste de acessibilidade por teclado |

## Metricas de Sucesso

| Metrica | Definicao | Meta |
|---------|----------|------|
| WCAG A compliance | % de criterios A atendidos | 100% |
| WCAG AA compliance | % de criterios AA atendidos | 100% |
| Automated test pass rate | % de testes automatizados passando | > 95% |
| Manual audit score | Score da auditoria manual (0-100) | > 90 |
| Remediation velocity | Issues resolvidos por sprint | Crescente |

## Time e Papeis

| Papel | Responsabilidade |
|-------|-----------------|
| a11y Lead | Coordenacao e auditoria |
| Product Designer | Correcao de design issues |
| Frontend Engineer | Implementacao de fixes |
| QA Engineer | Verificacao de fixes |
| Content Designer | Correcao de texto alternativo |

---

**Ultima atualizacao**: 2026-Q1
**Responsavel**: Accessibility Team
