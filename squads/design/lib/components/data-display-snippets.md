# Data Display Snippets

## Purpose

Snippets para componentes de exibicao de dados — tabelas, listas, cards de metricas, badges, tags e avatares. Padroes para apresentar informacoes de forma clara e escaneavel.

## Snippets

### Data Table

```html
<div class="table-container" role="region" aria-label="Lista de usuarios" tabindex="0">
  <table class="data-table">
    <thead>
      <tr>
        <th scope="col" aria-sort="ascending">
          <button class="sort-btn">Nome <span aria-hidden="true">▲</span></button>
        </th>
        <th scope="col">E-mail</th>
        <th scope="col">Status</th>
        <th scope="col">Acoes</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Ana Silva</td>
        <td>ana@empresa.com</td>
        <td><span class="badge badge--success">Ativo</span></td>
        <td>
          <button aria-label="Editar Ana Silva">Editar</button>
        </td>
      </tr>
    </tbody>
  </table>
</div>
```

### Metric Card / KPI

```html
<div class="metric-card">
  <span class="metric-label">Usuarios Ativos</span>
  <span class="metric-value">12.847</span>
  <span class="metric-trend metric-trend--up">
    <svg aria-hidden="true"><!-- arrow up --></svg>
    +8,3% vs. mes anterior
  </span>
</div>
```

### Badge / Tag

```html
<!-- Status badge -->
<span class="badge badge--success">Ativo</span>
<span class="badge badge--warning">Pendente</span>
<span class="badge badge--error">Bloqueado</span>

<!-- Removable tag -->
<span class="tag">
  Design System
  <button class="tag-remove" aria-label="Remover tag Design System">
    <svg aria-hidden="true"><!-- close --></svg>
  </button>
</span>
```

### Avatar Group

```html
<div class="avatar-group" aria-label="5 membros da equipe">
  <img class="avatar" src="/avatar1.jpg" alt="Ana Silva" />
  <img class="avatar" src="/avatar2.jpg" alt="Carlos Lima" />
  <img class="avatar" src="/avatar3.jpg" alt="Maria Santos" />
  <span class="avatar avatar--count" aria-label="mais 2 membros">+2</span>
</div>
```

### Description List

```html
<dl class="detail-list">
  <div class="detail-item">
    <dt>Criado em</dt>
    <dd>15 de janeiro de 2026</dd>
  </div>
  <div class="detail-item">
    <dt>Responsavel</dt>
    <dd>Ana Silva</dd>
  </div>
  <div class="detail-item">
    <dt>Status</dt>
    <dd><span class="badge badge--info">Em andamento</span></dd>
  </div>
</dl>
```

### Empty Table State

```html
<div class="empty-state">
  <svg class="empty-state-illustration" aria-hidden="true"><!-- illustration --></svg>
  <h3 class="empty-state-title">Nenhum resultado encontrado</h3>
  <p class="empty-state-description">
    Tente ajustar os filtros ou termos de busca.
  </p>
  <button class="btn btn--secondary">Limpar filtros</button>
</div>
```

## Usage Notes

- Tabelas devem ter scroll horizontal em telas pequenas com indicacao visual
- Use `scope="col"` e `scope="row"` para headers de tabela acessiveis
- Metric cards devem mostrar tendencia (trend) quando dados historicos existem
- Badges devem ter contraste suficiente mesmo em tamanho pequeno
- Avatares precisam de alt text descritivo ou aria-label
- Listas de descricao sao ideais para dados chave-valor em detalhes
