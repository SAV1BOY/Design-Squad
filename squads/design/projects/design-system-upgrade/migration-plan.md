# Migration Plan Template

## Informacoes do Projeto

| Campo | Valor |
|-------|-------|
| **Versao Origem** | [ex. v3.x] |
| **Versao Destino** | [ex. v4.x] |
| **Migration Lead** | [Nome] |
| **Data de Inicio** | [YYYY-MM-DD] |
| **Data Prevista de Conclusao** | [YYYY-MM-DD] |
| **Produtos Afetados** | [Lista de produtos] |

## Escopo da Migracao

### O que Muda

Resumo das principais mudancas entre versoes que impactam
os times consumidores do Design System.

#### Breaking Changes

| Componente | Mudanca | Impacto | Migration Path |
|-----------|---------|---------|---------------|
| [comp] | [descricao] | [alto/medio/baixo] | [como migrar] |
| [comp] | [descricao] | [alto/medio/baixo] | [como migrar] |
| [comp] | [descricao] | [alto/medio/baixo] | [como migrar] |

#### Non-Breaking Changes

| Componente | Mudanca | Acao Necessaria |
|-----------|---------|----------------|
| [comp] | [descricao] | [nenhuma / atualizar import] |
| [comp] | [descricao] | [nenhuma / atualizar import] |

#### Deprecated Components

| Componente | Substituto | Deadline para Migracao |
|-----------|-----------|----------------------|
| [comp antigo] | [comp novo] | [data] |
| [comp antigo] | [comp novo] | [data] |

### Token Changes

| Token Antigo | Token Novo | Tipo de Mudanca |
|-------------|-----------|----------------|
| `color-primary-500` | `color-brand-primary` | Rename |
| `spacing-4` | `spacing-md` | Rename + valor |
| `font-size-14` | `font-size-body` | Semantic naming |

## Estrategia de Migracao

### Abordagem

Escolha uma das abordagens abaixo e justifique:

- [ ] **Big Bang**: todos os produtos migram simultaneamente
- [ ] **Incremental**: produtos migram individualmente em ondas
- [ ] **Parallel Run**: versao antiga e nova coexistem temporariamente

**Justificativa**: [Por que esta abordagem foi escolhida]

### Ondas de Migracao (se incremental)

| Onda | Produtos | Inicio | Fim | Responsavel |
|------|----------|--------|-----|-------------|
| 1 | [produto piloto] | [data] | [data] | [nome] |
| 2 | [produtos] | [data] | [data] | [nome] |
| 3 | [produtos] | [data] | [data] | [nome] |

## Ferramentas de Suporte

### Codemods Disponiveis

Scripts automatizados para facilitar a migracao de codigo.

| Codemod | Descricao | Comando |
|---------|-----------|---------|
| `rename-tokens` | Renomeia tokens deprecated | `npx ds-migrate rename-tokens` |
| `update-imports` | Atualiza import paths | `npx ds-migrate update-imports` |
| `replace-components` | Substitui componentes deprecated | `npx ds-migrate replace-components` |

### Compatibility Layer

Se aplicavel, descreva o compatibility layer que permite uso
temporario da API antiga sobre a implementacao nova.

```
[Descricao do compatibility layer e como ativa-lo]
```

## Guia de Migracao por Componente

### [Componente 1]

**Antes (v3)**:
```jsx
// Exemplo de uso antigo
<OldComponent prop="value" />
```

**Depois (v4)**:
```jsx
// Exemplo de uso novo
<NewComponent newProp="value" />
```

**Notas**: [Observacoes especificas sobre esta migracao]

### [Componente 2]

**Antes (v3)**:
```jsx
// Exemplo de uso antigo
```

**Depois (v4)**:
```jsx

---
