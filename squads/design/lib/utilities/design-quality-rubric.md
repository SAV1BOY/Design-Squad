# Design Quality Rubric

## Purpose

Rubrica para avaliacao objetiva da qualidade de design de interfaces. Usada em design reviews, QA visual e auditorias de qualidade para garantir padrao Gold Standard.

## Rubric Dimensions

### 1. Visual Consistency (Peso: 25%)

```
Score | Criterio
------|------------------------------------------------------------------
5     | 100% dos elementos usam tokens do design system
4     | 95%+ aderencia a tokens, desvios documentados
3     | 80-94% aderencia, alguns valores hard-coded
2     | 50-79% aderencia, inconsistencias visiveis
1     | < 50% aderencia, aparencia fragmentada
```

### 2. Typography & Hierarchy (Peso: 20%)

```
Score | Criterio
------|------------------------------------------------------------------
5     | Hierarquia clara, escala tipografica consistente, ritmo perfeito
4     | Hierarquia boa, pequenos ajustes necessarios
3     | Hierarquia funcional mas com inconsistencias
2     | Hierarquia confusa em algumas areas
1     | Sem hierarquia clara, tipografia inconsistente
```

### 3. Spacing & Layout (Peso: 15%)

```
Score | Criterio
------|------------------------------------------------------------------
5     | Grid perfeito, spacing tokens em 100% dos casos
4     | Grid consistente, 1-2 desvios menores
3     | Grid funcional, alguns espacamentos arbitrarios
2     | Layout irregular, espacamentos visivelmente inconsistentes
1     | Sem sistema de grid ou spacing
```

### 4. Interaction Design (Peso: 15%)

```
Score | Criterio
------|------------------------------------------------------------------
5     | Todos os estados cobertos, feedback claro, transicoes suaves
4     | Estados principais cobertos, bom feedback
3     | Estados basicos presentes, feedback inconsistente
2     | Faltam estados importantes (hover, focus, error)
1     | Sem estados interativos definidos
```

### 5. Accessibility (Peso: 15%)

```
Score | Criterio
------|------------------------------------------------------------------
5     | WCAG AA completo, testado com assistive tech
4     | WCAG AA quase completo, issues menores
3     | Contraste OK, mas faltam ARIA labels ou keyboard nav
2     | Problemas de contraste ou navegacao por teclado
1     | Acessibilidade nao considerada
```

### 6. Responsiveness (Peso: 10%)

```
Score | Criterio
------|------------------------------------------------------------------
5     | Perfeito em todos os breakpoints, conteudo adaptado
4     | Funcional em todos os breakpoints, ajustes menores
3     | Funcional no desktop e mobile, tablet parcial
2     | Funcional apenas no desktop
1     | Nao responsivo
```

## Scoring Formula

```
Quality Score = (Visual * 0.25) + (Typography * 0.20) + (Spacing * 0.15) +
               (Interaction * 0.15) + (Accessibility * 0.15) + (Responsive * 0.10)

Classificacao:
  4.5 - 5.0: Gold Standard
  3.5 - 4.4: Production Ready
  2.5 - 3.4: Needs Improvement
  1.5 - 2.4: Significant Issues
  1.0 - 1.4: Not Acceptable
```

## Usage Notes

- Aplique a rubrica em design reviews antes do handoff
- Use como checklist durante QA visual
- Score minimo para producao: 3.5 (Production Ready)
- Documente issues encontradas com screenshot e sugestao de correcao
- Revise a rubrica semestralmente para alinhar com evolucao do DS
