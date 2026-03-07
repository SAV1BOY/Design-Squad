# Loading Patterns

## Pattern Description

Padroes para estados de carregamento em interfaces. Cobre skeletons, spinners, progress bars, optimistic UI e lazy loading. O objetivo e manter a percepcao de velocidade e informar o usuario sobre o progresso.

## Patterns

### Skeleton Screen

```
┌────────────────────────────────────┐
│ ████████████   ░░░░░░░░           │
│ ████████████████████████████       │
│ ██████████████████░░░░░░░░        │
│                                    │
│ ████████████   ░░░░░░░░           │
│ ████████████████████████████       │
│ ██████████████████░░░░░░░░        │
└────────────────────────────────────┘
```

Quando usar:
- Carregamento inicial de paginas com layout previsivel
- Listas e grids de conteudo
- Profile cards, dashboards, feeds

Regras:
- Skeleton deve espelhar o layout real do conteudo
- Use animacao pulse ou wave sutil
- Nao mostre skeleton por mais de 3-5 segundos — apos isso, mostre mensagem

### Spinner

```html
<div class="spinner" role="status" aria-label="Carregando...">
  <svg class="spinner-icon" aria-hidden="true"><!-- animated circle --></svg>
</div>
```

Quando usar:
- Acoes de curta duracao (< 3 segundos)
- Dentro de botoes durante submit
- Inline em componentes pequenos

### Progress Bar (Determinada)

```
Upload de arquivo:
[████████████████░░░░░░░░] 67% — 2 de 3 arquivos

Progresso de etapas:
Etapa 2 de 4 ━━━━━━━━━━━━░░░░░░░░░░
```

### Optimistic UI

```
Cenario: usuario curte um post
1. UI atualiza imediatamente (icone preenchido, contagem +1)
2. Request enviado ao servidor em background
3. Se falhar: reverte UI + mostra toast de erro

Beneficio: resposta instantanea percebida
Risco: inconsistencia se falhar — tenha rollback robusto
```

### Lazy Loading (Infinite Scroll)

```
[Conteudo carregado]
[Conteudo carregado]
[Conteudo carregado]
    ┌──────────────┐
    │   Loading... │ ← trigger ao scroll (Intersection Observer)
    └──────────────┘
[Novo conteudo aparece]
```

### Content Placeholder

```
Enquanto imagem carrega:
┌──────────────────┐
│                  │
│   placeholder    │ ← blur hash ou cor dominante
│   (low-res)      │
│                  │
└──────────────────┘
→ Transicao suave para imagem final
```

## Analysis

Regras de ouro para loading:
- 0-100ms: percebido como instantaneo — nao mostre nada
- 100ms-1s: mostre feedback sutil (spinner inline)
- 1s-3s: mostre skeleton ou progress
- 3s+: mostre progress bar com estimativa de tempo
- Sempre prefira skeleton sobre spinner para conteudo de pagina

## Tags

`loading`, `performance`, `skeleton`, `optimistic-ui`, `progressive-loading`
