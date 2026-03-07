# Table Filter Patterns

## Pattern Description

Padroes para filtragem e busca em tabelas de dados. Cobre filtros por coluna, filtros globais, filtros avancados, chips de filtro ativo e estados de resultado vazio.

## Patterns

### Search + Filter Bar

```
┌──────────────────────────────────────────┐
│ [🔍 Buscar...]  [Status ▼] [Data ▼] [+] │
│                                          │
│ Filtros ativos: [Ativo ×] [Jan 2026 ×]  │
├──────────────────────────────────────────┤
│ Nome       | Status  | Data     | Acoes  │
│ Ana Silva  | Ativo   | 15/01    | ...    │
│ Carlos L.  | Ativo   | 20/01    | ...    │
├──────────────────────────────────────────┤
│ Mostrando 2 de 150 resultados            │
└──────────────────────────────────────────┘
```

### Filter Dropdown

```html
<div class="filter-dropdown">
  <button class="filter-trigger" aria-expanded="false" aria-haspopup="listbox">
    Status <span class="filter-count">2</span>
  </button>
  <div class="filter-panel" role="listbox" aria-multiselectable="true">
    <label><input type="checkbox" checked /> Ativo</label>
    <label><input type="checkbox" checked /> Pendente</label>
    <label><input type="checkbox" /> Inativo</label>
    <div class="filter-actions">
      <button>Limpar</button>
      <button class="btn-primary">Aplicar</button>
    </div>
  </div>
</div>
```

### Active Filter Chips

```html
<div class="filter-chips" aria-label="Filtros ativos">
  <span class="chip">
    Status: Ativo
    <button aria-label="Remover filtro Status: Ativo">×</button>
  </span>
  <span class="chip">
    Periodo: Jan 2026
    <button aria-label="Remover filtro Periodo: Jan 2026">×</button>
  </span>
  <button class="chip-clear">Limpar todos</button>
</div>
```

### Advanced Filter Panel

```
Para tabelas complexas com 5+ dimensoes de filtro:
- Painel lateral (drawer) com todos os filtros
- Agrupados por categoria
- Preview do numero de resultados antes de aplicar
- Botoes "Aplicar" e "Redefinir"
```

### Column Sort

```
Interacao:
1. Click no header: ordena ascendente
2. Segundo click: ordena descendente
3. Terceiro click: remove ordenacao
- Indicador visual (seta) no header ativo
- aria-sort="ascending" | "descending" | "none"
```

## Analysis

Filtros eficazes equilibram poder e simplicidade:
- Comece com filtros mais usados visiveis (1-3)
- Esconda filtros avancados atras de um expandir/painel
- Sempre mostre o estado atual dos filtros (chips)
- Atualize a contagem de resultados em tempo real
- Preserve filtros na URL para compartilhamento

## Tags

`tables`, `filters`, `search`, `data-display`, `responsive`, `a11y`
