# Accessibility Audit Findings Template

## Informacoes da Auditoria

| Campo | Valor |
|-------|-------|
| **Produto/Feature** | [Nome] |
| **Auditor** | [Nome] |
| **Data de Inicio** | [YYYY-MM-DD] |
| **Data de Conclusao** | [YYYY-MM-DD] |
| **Padrao** | WCAG 2.1 AA |
| **Escopo** | [Telas/fluxos auditados] |

## Metodologia

### Abordagem

A auditoria combina testes automatizados e manuais para maximizar
a cobertura de deteccao de issues.

| Metodo | Ferramenta | Telas Testadas |
|--------|-----------|---------------|
| Automatizado | axe DevTools | [N telas] |
| Automatizado | Lighthouse | [N telas] |
| Manual — Screen reader | VoiceOver | [N telas] |
| Manual — Screen reader | NVDA | [N telas] |
| Manual — Keyboard | Navegacao por teclado | [N telas] |
| Manual — Visual | Contraste e tamanho de texto | [N telas] |

### Escopo Auditado

| Pagina/Fluxo | URL/Rota | Plataforma | Testado |
|-------------|----------|-----------|---------|
| [Pagina 1] | [url] | [Web/Mobile] | [ ] |
| [Pagina 2] | [url] | [Web/Mobile] | [ ] |
| [Pagina 3] | [url] | [Web/Mobile] | [ ] |
| [Pagina 4] | [url] | [Web/Mobile] | [ ] |
| [Pagina 5] | [url] | [Web/Mobile] | [ ] |

## Resumo dos Findings

### Por Nivel WCAG

| Nivel | Total Issues | Criticos | Maiores | Menores |
|-------|-------------|---------|--------|---------|
| A | [N] | [N] | [N] | [N] |
| AA | [N] | [N] | [N] | [N] |
| **Total** | **[N]** | **[N]** | **[N]** | **[N]** |

### Por Categoria

| Categoria | Issues | Exemplos |
|-----------|--------|---------|
| Perceivable | [N] | Alt text, contraste, legendas |
| Operable | [N] | Teclado, timing, navegacao |
| Understandable | [N] | Linguagem, previsibilidade |
| Robust | [N] | Parsing, ARIA, compatibilidade |

### Por Tipo de Deficiencia Impactada

| Tipo | Issues | Impacto |
|------|--------|---------|
| Visual (cegueira) | [N] | [descricao] |
| Visual (baixa visao) | [N] | [descricao] |
| Auditiva | [N] | [descricao] |
| Motora | [N] | [descricao] |
| Cognitiva | [N] | [descricao] |

## Findings Detalhados

### Findings Criticos

#### FIND-001: [Titulo descritivo]

| Campo | Detalhe |
|-------|---------|
| **WCAG Criterion** | [Numero e nome — ex. 1.1.1 Non-text Content] |
| **Nivel** | [A / AA] |
| **Severidade** | Critico |
| **Pagina(s)** | [Paginas afetadas] |
| **Elemento** | [Seletor CSS ou descricao do elemento] |
| **Deficiencias Impactadas** | [Visual / Auditiva / Motora / Cognitiva] |

**Descricao do Problema**:
[Descricao clara do problema encontrado]

**Impacto no Usuario**:
[Como este problema afeta usuarios com deficiencia]

**Evidencia**:
```
[Codigo problematico ou screenshot reference]
```

**Remediacao Sugerida**:
[Descricao de como corrigir o problema]

```
[Exemplo de codigo corrigido, se aplicavel]
```

---

#### FIND-002: [Titulo descritivo]

| Campo | Detalhe |
|-------|---------|
| **WCAG Criterion** | [Numero e nome] |
| **Nivel** | [A / AA] |
| **Severidade** | Critico |
| **Pagina(s)** | [Paginas afetadas] |
| **Elemento** | [Seletor ou descricao] |
| **Deficiencias Impactadas** | [tipos] |

**Descricao do Problema**: [descricao]

**Impacto no Usuario**: [impacto]


---
