# Empty State Patterns

## Pattern Description

Padroes para estados vazios em interfaces — quando nao ha dados para exibir. Cobre zero-data, resultados de busca vazios, estados de erro e estados de permissao. Empty states sao oportunidades de orientar e engajar o usuario.

## Patterns

### Zero Data (First Use)

```
┌────────────────────────────────────┐
│         [Ilustracao]               │
│                                    │
│    Nenhum projeto ainda            │
│                                    │
│  Crie seu primeiro projeto para    │
│  comecar a organizar seu trabalho. │
│                                    │
│      [+ Criar projeto]             │
└────────────────────────────────────┘
```

Regras:
- Tom amigavel e encorajador
- CTA claro e unico
- Ilustracao contextual (nao generica)

### Search No Results

```
┌────────────────────────────────────┐
│         [Ilustracao busca]         │
│                                    │
│  Nenhum resultado para "xpto"      │
│                                    │
│  Sugestoes:                        │
│  - Verifique a ortografia          │
│  - Use termos mais gerais          │
│  - Remova alguns filtros           │
│                                    │
│  [Limpar busca]                    │
└────────────────────────────────────┘
```

### Filtered No Results

```
Nenhum item corresponde aos filtros selecionados.
[Limpar filtros]
```

Diferenca do search empty state: aqui o usuario aplicou filtros, nao digitou uma busca. A acao e limpar filtros, nao corrigir texto.

### Error State

```
┌────────────────────────────────────┐
│         [Ilustracao erro]          │
│                                    │
│  Nao conseguimos carregar os dados │
│                                    │
│  Isso pode ser um problema         │
│  temporario. Tente novamente.      │
│                                    │
│  [Tentar novamente]                │
└────────────────────────────────────┘
```

### Permission Denied

```
┌────────────────────────────────────┐
│         [Ilustracao cadeado]       │
│                                    │
│  Acesso restrito                   │
│                                    │
│  Voce precisa de permissao para    │
│  visualizar este conteudo.         │
│                                    │
│  [Solicitar acesso]                │
└────────────────────────────────────┘
```

## Analysis

Empty states eficazes compartilham estas caracteristicas:
- **Ilustracao**: reforca visualmente o contexto
- **Titulo claro**: descreve a situacao em poucas palavras
- **Descricao**: explica o porque e orienta o proximo passo
- **CTA unico**: uma acao principal clara

Empty states sao uma das maiores oportunidades de onboarding negligenciadas.

## Tags

`empty-states`, `onboarding`, `ux-writing`, `illustration`, `first-use`
