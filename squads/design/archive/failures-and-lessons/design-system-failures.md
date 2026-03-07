# Design System Failures

## Overview

Analise de falhas comuns em iniciativas de design system. Documentar fracassos e tao valioso quanto documentar sucessos — evita repetir os mesmos erros.

## Common Failure Patterns

### 1. The Ivory Tower DS
```
Sintomas:
- Time de DS isolado dos times de produto
- Componentes projetados sem input de consumidores
- Documentacao academica, nao pratica
- Ninguem usa porque nao resolve problemas reais

Causa raiz: falta de colaboracao com consumidores
Resultado: DS abandonado apos 6-12 meses
Licao: DS deve ser co-criado com os times que o usam
```

### 2. The Never-Shipped DS
```
Sintomas:
- Planejamento perfeito sem delivery
- Escopo sempre crescente ("precisamos de mais componentes antes de lancar")
- V1 nunca lancada
- Time frustrado com falta de impacto

Causa raiz: perfeccionismo e falta de pragmatismo
Resultado: investimento perdido, credibilidade do DS comprometida
Licao: lance com 10-15 componentes, itere baseado em uso real
```

### 3. The Zombie DS
```
Sintomas:
- DS lancado mas sem manutencao
- Bugs nao corrigidos
- Issues abertas sem resposta
- Docs desatualizadas
- Times criam workarounds em vez de contribuir

Causa raiz: DS sem equipe dedicada ou ownership claro
Resultado: fragmentation progressiva, pior que nao ter DS
Licao: DS precisa de investment continuo (1-3 FTEs minimo)
```

### 4. The Copy-Paste DS
```
Sintomas:
- Design system copiado de Material/Ant sem adaptacao
- Nao reflete a identidade ou necessidades do produto
- Componentes genericos que nao resolvem casos especificos
- Times ainda criam componentes custom para 80% dos casos

Causa raiz: pressa para ter um DS sem entender as necessidades
Resultado: dois sistemas paralelos (DS + custom)
Licao: baseie-se em auditoria real dos componentes existentes
```

### 5. The Dictatorial DS
```
Sintomas:
- DS team impoe regras sem flexibilidade
- Nenhum caminho para excecoes ou extensoes
- Times de produto sentem-se bloqueados
- Contribuicoes rejeitadas sem feedback construtivo

Causa raiz: governanca rigida demais
Resultado: resistencia e subversao (shadow components)
Licao: governanca deve ser firme nos principios, flexivel na execucao
```

## Recovery Strategies

```
Falha               | Recuperacao
--------------------|------------------------------------------
Ivory Tower         | Embedded designer no time de produto
Never-Shipped       | Ship v0.1 em 2 semanas, itere
Zombie              | Atribuir ownership, resolver top 5 issues
Copy-Paste          | Component audit + redesign incremental
Dictatorial         | Open contribution model + office hours
```

## Lessons

- Design systems falham por razoes organizacionais, nao tecnicas
- Adocao voluntaria e mais sustentavel que adocao forcada
- Comece pequeno, prove valor, escale com dados
- Communication e governanca sao mais importantes que pixels perfeitos
- Trate DS como produto com roadmap, backlog, stakeholders e metricas

## Tags

`design-systems`, `failures`, `lessons-learned`, `governance`, `adoption`
