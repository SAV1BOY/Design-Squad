# Atlassian Design System Journey

## Overview

A jornada do Atlassian Design System, um dos mais complexos DS enterprise, unificando produtos diversos como Jira, Confluence, Trello e Bitbucket.

## Timeline

### 2015: ADG (Atlassian Design Guidelines) v1
```
Primeiro passo:
- Guidelines visuais para produtos Atlassian
- Foco em consistencia entre Jira e Confluence
- Componentes em Atlaskit (React)
- 30+ componentes basicos
- Desafio: cada produto tinha cultura de design propria
```

### 2017-2018: Atlaskit e Unificacao
```
Evolucao tecnica:
- Atlaskit como monorepo de componentes
- Migracoes de produtos para componentes compartilhados
- Design tokens introduzidos
- Aquisicao do Trello — mais um produto para unificar
- Metricas de adocao: 40% coverage
```

### 2019-2020: Design System Team
```
Investimento em time:
- Equipe dedicada de 15+ pessoas
- Contribution model formalizado (RFC)
- Office hours semanais
- Migration guides para cada release
- Metricas de adocao: 65% coverage
```

### 2021-presente: Token-Centric Architecture
```
Estado atual:
- Tokens como camada de abstracao entre design e codigo
- Theming system (light, dark, high-contrast)
- Componentes maduros (100+) com a11y integrada
- Design System Council para governanca
- Metricas de adocao: 85%+ coverage
```

## Desafios Unicos

```
Desafio                        | Abordagem
-------------------------------|------------------------------------------
Multiplos produtos (Jira, Conf)| Tokens compartilhados, componentes compostos
Aquisicoes (Trello)            | Migracao gradual com migration guides
Scale (4000+ engineers)        | Inner source model + quality gates
Legacy code                    | Codemods automatizados para migracao
```

## Governance Model

```
Nivel         | Responsavel            | Scope
--------------|------------------------|--------------------------
Foundation    | DS Core Team           | Tokens, core components
Patterns      | DS + Product Designers | Cross-product patterns
Product-level | Product Teams          | Product-specific extensions
```

## Lessons

- DS para multiplos produtos exige governanca forte mas flexivel
- Migracao de legacy code precisa de tooling (codemods)
- Office hours reduzem tickets de suporte em 40%
- Metricas de adocao devem ser automatizadas (AST analysis)
- Contribution model aberto acelera coverage mas requer quality gates

## Tags

`atlassian`, `design-system`, `enterprise`, `governance`, `multi-product`, `migration`
