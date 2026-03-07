# Workshop Kit: Design Tokens

## Objective

Kit completo para facilitar um workshop pratico sobre design tokens. Objetivo: alinhar designers e developers sobre o conceito, beneficios e implementacao pratica de tokens.

## Workshop Overview

```
Duracao: 3 horas
Participantes: 4-8 (mix de designers e developers)
Materiais: Figma file preparado, VS Code, token files de exemplo
Pre-work: ler artigo introdutorio sobre tokens (15 min)
```

## Agenda

### 1. Concept Introduction (30 min)
```
O que sao design tokens:
- "Design decisions stored as data"
- Camada de abstracao entre design e codigo
- Source of truth para valores visuais

Analogia:
- Variaveis em programacao = tokens em design
- CSS custom properties = tokens na web

Exemplos visuais:
- Sem tokens: color: #2563EB → espalhado em 47 arquivos
- Com tokens: color: var(--color-action-primary) → 1 definicao
```

### 2. Token Architecture (30 min)
```
Exercicio guiado: mapear 3 camadas

Global tokens:
  color-blue-600: #2563EB
  ↓
Alias tokens:
  color-action-primary: {color-blue-600}
  ↓
Component tokens:
  button-bg-primary: {color-action-primary}

Atividade: participantes mapeiam 5 valores visuais de um
componente real para as 3 camadas usando post-its/FigJam.
```

### 3. Hands-On: Tokenizing a Component (45 min)
```
Exercicio pratico:

1. Grupo recebe um componente (Card) em Figma e codigo
2. Identificar todos os valores visuais (cor, spacing, tipo, radius, shadow)
3. Criar nomenclatura para cada token
4. Mapear nas 3 camadas
5. Implementar como CSS custom properties

Formato: 2 sub-grupos trabalhando no mesmo componente
Resultado: comparar abordagens e discutir diferencas
```

### 4. Theming Demo (30 min)
```
Demonstracao ao vivo:
- Mesmos componentes em light e dark mode
- Trocar tema mudando apenas alias tokens
- Demonstrar brand theming (white-label)
- Mostrar como tokens habilitam esses cenarios

Discussao:
- Quais cenarios de theming sao relevantes para nos?
- Quais tokens precisamos ter para suportar nossos cenarios?
```

### 5. Naming Convention Workshop (20 min)
```
Exercicio colaborativo:
- Grupo define naming convention para o time
- Template: {category}-{property}-{variant}-{state}
- Testar com 10 exemplos reais do produto
- Documentar convencao acordada
```

### 6. Debrief e Next Steps (15 min)
```
- O que aprendemos?
- Quais sao os proximos passos concretos?
  1. Audit de valores hard-coded no codebase
  2. Definir token file structure
  3. Implementar tokens em 1 componente piloto
  4. Expandir gradualmente
- Quem e owner de cada next step?
```

## Materials Needed

```
Preparacao:
- Figma file com componentes do produto (sem tokens)
- Arquivo CSS com valores hard-coded
- Template de token file (JSON)
- Exemplos de token files de DS publicos (Carbon, Polaris)
- FigJam board com templates de exercicios
```

## Facilitator Notes

- Adapte a profundidade tecnica ao grupo (mais designers → mais visual, mais devs → mais codigo)
- O exercicio de naming convention geralmente gera debate — timebox para nao dominar
- Tenha backup de exercicio se um grupo terminar mais rapido
- Resultado tangivel: token file para 1 componente real do produto

## Notes

- Workshop funciona melhor presencial (whiteboard + pair programming)
- Follow-up em 2 semanas para revisar progresso
- Considere workshop avancado futuro: multi-theme tokens, token pipelines
