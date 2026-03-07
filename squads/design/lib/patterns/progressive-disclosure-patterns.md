# Progressive Disclosure Patterns

## Pattern Description

Padroes para revelacao progressiva de informacao e funcionalidades. O principio e mostrar apenas o essencial inicialmente e revelar detalhes sob demanda, reduzindo carga cognitiva e complexidade percebida.

## Patterns

### Accordion / Expandable Sections

```html
<div class="accordion">
  <div class="accordion-item">
    <button class="accordion-trigger" aria-expanded="false"
      aria-controls="content-1">
      Opcoes avancadas
      <svg class="accordion-icon" aria-hidden="true"><!-- chevron --></svg>
    </button>
    <div id="content-1" class="accordion-content" hidden>
      <!-- conteudo detalhado -->
    </div>
  </div>
</div>
```

### Show More / Read More

```
Texto curto visivel (3 linhas com line-clamp)...
[Ler mais]

→ Expande para texto completo
[Ler menos]
```

### Staged Form

```
Etapa 1: Informacoes basicas (3 campos)
    [Continuar →]

Etapa 2: Detalhes adicionais (4 campos)
    [← Voltar] [Continuar →]

Etapa 3: Revisao e confirmacao
    [← Voltar] [Enviar]
```

### Hover / Click to Reveal

```
Dashboard com KPI cards:
- Visao inicial: valor + label
- Hover: tooltip com breakdown
- Click: drawer com detalhes completos e grafico
```

### Feature Teaser

```
Plano gratuito:
┌──────────────┐
│  Relatorios  │
│  basicos     │
│              │
│  [Upgrade]   │
│  para ver    │
│  avancados   │
└──────────────┘
```

### Contextual Controls

```
Lista de itens:
- Default: apenas titulo e status
- Hover na row: revela botoes de acao (editar, excluir)
- Mobile: swipe para revelar acoes ou menu de contexto (...)
```

## Analysis

Progressive disclosure eficaz:
- Prioriza o que 80% dos usuarios precisam 80% do tempo
- Esconde sem eliminar — tudo continua acessivel
- Usa triggers claros (botoes, links, iconografia)
- Nao esconde informacoes criticas ou de seguranca
- Testa com usuarios para validar a hierarquia de importancia
- Reduz cognitive load mensuravel (NASA-TLX, SUS scores)

## Tags

`progressive-disclosure`, `complexity-management`, `cognitive-load`, `information-architecture`
