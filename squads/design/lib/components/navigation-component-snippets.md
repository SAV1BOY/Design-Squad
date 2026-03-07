# Navigation Component Snippets

## Purpose

Snippets para componentes de navegacao — tabs, breadcrumbs, side nav, bottom nav, pagination e menus. Padroes estruturais e de interacao para orientacao do usuario.

## Snippets

### Tab Navigation

```html
<div class="tabs" role="tablist" aria-label="Secoes do perfil">
  <button role="tab" aria-selected="true" aria-controls="panel-info"
    id="tab-info" tabindex="0">
    Informacoes
  </button>
  <button role="tab" aria-selected="false" aria-controls="panel-security"
    id="tab-security" tabindex="-1">
    Seguranca
  </button>
  <button role="tab" aria-selected="false" aria-controls="panel-billing"
    id="tab-billing" tabindex="-1">
    Cobranca
  </button>
</div>

<div role="tabpanel" id="panel-info" aria-labelledby="tab-info">
  <!-- conteudo -->
</div>
```

### Breadcrumb

```html
<nav aria-label="Breadcrumb">
  <ol class="breadcrumb">
    <li><a href="/">Inicio</a></li>
    <li aria-hidden="true" class="separator">/</li>
    <li><a href="/produtos">Produtos</a></li>
    <li aria-hidden="true" class="separator">/</li>
    <li aria-current="page">Detalhes do Produto</li>
  </ol>
</nav>
```

### Side Navigation

```html
<nav class="side-nav" aria-label="Menu lateral">
  <ul class="nav-list">
    <li class="nav-section">
      <span class="nav-section-title">Principal</span>
      <ul>
        <li><a href="/dashboard" class="nav-item active" aria-current="page">Dashboard</a></li>
        <li><a href="/projects" class="nav-item">Projetos</a></li>
        <li><a href="/team" class="nav-item">Equipe</a></li>
      </ul>
    </li>
    <li class="nav-section">
      <span class="nav-section-title">Configuracoes</span>
      <ul>
        <li><a href="/settings" class="nav-item">Geral</a></li>
        <li><a href="/billing" class="nav-item">Cobranca</a></li>
      </ul>
    </li>
  </ul>
</nav>
```

### Bottom Navigation (Mobile)

```html
<nav class="bottom-nav" aria-label="Navegacao principal">
  <a href="/home" class="bottom-nav-item active" aria-current="page">
    <svg class="icon" aria-hidden="true"><!-- home --></svg>
    <span>Inicio</span>
  </a>
  <a href="/search" class="bottom-nav-item">
    <svg class="icon" aria-hidden="true"><!-- search --></svg>
    <span>Buscar</span>
  </a>
  <a href="/profile" class="bottom-nav-item">
    <svg class="icon" aria-hidden="true"><!-- profile --></svg>
    <span>Perfil</span>
  </a>
</nav>
```

### Pagination

```html
<nav aria-label="Paginacao">
  <ul class="pagination">
    <li><button aria-label="Pagina anterior" disabled>&laquo;</button></li>
    <li><button aria-current="page" class="active">1</button></li>
    <li><button>2</button></li>
    <li><button>3</button></li>
    <li><span class="ellipsis">...</span></li>
    <li><button>10</button></li>
    <li><button aria-label="Proxima pagina">&raquo;</button></li>
  </ul>
</nav>
```

## Usage Notes

- Limite bottom nav a 3-5 itens no mobile
- Breadcrumbs sao essenciais para hierarquias com 3+ niveis
- Use `aria-current="page"` para indicar a pagina atual
- Tabs devem usar Arrow keys para navegacao, nao Tab key
- Side nav deve colapsar em telas pequenas com toggle acessivel
- Mantenha consistencia no padrao de navegacao em todo o produto
