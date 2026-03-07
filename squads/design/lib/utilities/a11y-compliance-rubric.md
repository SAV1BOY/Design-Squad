# Accessibility Compliance Rubric

## Purpose

Rubrica detalhada para avaliacao de conformidade com acessibilidade (WCAG 2.2). Usada em auditorias de a11y, design reviews e QA para garantir que interfaces sao acessiveis a todos os usuarios.

## WCAG Compliance Levels

```
Nivel  | Descricao                          | Requisito
-------|------------------------------------|--------------------------
A      | Requisitos minimos essenciais      | Obrigatorio
AA     | Padrao recomendado (nosso target)  | Obrigatorio
AAA    | Nivel maximo de acessibilidade     | Desejavel onde possivel
```

## Rubric Dimensions

### 1. Perceivable (Perceptivel)

```
Criterio                           | Peso | Check
-----------------------------------|------|----------------------------------
Alt text em todas as imagens       | Alto | Ferramenta automatizada + review
Contraste de cor (AA: 4.5:1 texto) | Alto | Contrast checker em cada tela
Contraste de cor (AA: 3:1 UI)      | Alto | Bordas, icones, controles
Captions em video                  | Med  | Review manual
Nao depender apenas de cor         | Alto | Review manual (color-blind test)
Responsive text (zoom 200%)        | Med  | Teste manual em browser
```

### 2. Operable (Operavel)

```
Criterio                           | Peso | Check
-----------------------------------|------|----------------------------------
Keyboard navigation completa       | Alto | Tab through em cada tela
Focus visible em todos elementos   | Alto | Teste manual + CSS audit
Nenhum keyboard trap               | Alto | Teste manual (modais, dropdowns)
Skip navigation link               | Med  | Inspecao de codigo
Target size (min 24x24, ideal 44)  | Alto | Medicao em ferramentas
Motion: respeita reduced-motion    | Med  | Teste com prefers-reduced-motion
Timeout: usuario pode estender     | Med  | Teste funcional
```

### 3. Understandable (Compreensivel)

```
Criterio                           | Peso | Check
-----------------------------------|------|----------------------------------
Linguagem clara e consistente      | Med  | Review de UX writing
Erros identificados claramente     | Alto | Teste de formularios
Sugestoes de correcao em erros     | Med  | Teste de formularios
Labels em todos os inputs          | Alto | Ferramenta automatizada
Navegacao consistente              | Med  | Review de IA
```

### 4. Robust (Robusto)

```
Criterio                           | Peso | Check
-----------------------------------|------|----------------------------------
HTML semantico                     | Alto | Validador + inspecao
ARIA roles corretos                | Alto | axe-core + review manual
ARIA states atualizados            | Alto | Teste com screen reader
Compativel com assistive tech      | Alto | Teste com NVDA/VoiceOver
```

## Scoring

```
Score por criterio:
  Pass (1.0): criterio atendido completamente
  Partial (0.5): atendido parcialmente, com issues menores
  Fail (0.0): nao atendido

Compliance Score = soma dos scores / total de criterios * 100

Classificacao:
  95-100%: Excelente — AA completo
  85-94%:  Bom — maioria AA, issues menores
  70-84%:  Regular — precisa correcoes antes de release
  < 70%:   Critico — bloqueador de release
```

## Testing Tools

```
Automatizado:  axe-core, Lighthouse, WAVE, pa11y
Semi-auto:     Accessibility Insights, Stark (Figma)
Manual:        Screen reader (NVDA, VoiceOver, JAWS)
               Keyboard-only navigation
               Zoom 200% + reflow test
               High contrast mode
```

## Usage Notes

- Score minimo para producao: 85% (Bom)
- Issues de contraste e keyboard sao bloqueadores
- Teste com pelo menos 1 screen reader antes de release
- Inclua testes de a11y no CI/CD (axe-core)
- Re-audite apos mudancas significativas de UI
