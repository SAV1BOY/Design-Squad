# Feedback Component Snippets

## Purpose

Snippets para componentes de feedback ao usuario — alerts, toasts, snackbars, progress indicators, banners e inline messages. Padroes para comunicar status, sucesso, erro e informacoes.

## Snippets

### Alert / Inline Message

```html
<div class="alert alert--error" role="alert">
  <svg class="alert-icon" aria-hidden="true"><!-- error icon --></svg>
  <div class="alert-content">
    <strong class="alert-title">Erro ao salvar</strong>
    <p class="alert-description">
      Nao foi possivel salvar as alteracoes. Tente novamente em alguns instantes.
    </p>
  </div>
  <button class="alert-close" aria-label="Fechar alerta">
    <svg aria-hidden="true"><!-- close --></svg>
  </button>
</div>
```

Variantes de severidade:
- **info**: cor azul, icone de informacao
- **success**: cor verde, icone de check
- **warning**: cor amarela, icone de atencao
- **error**: cor vermelha, icone de erro

### Toast / Snackbar

```html
<div class="toast-container" aria-live="polite" aria-atomic="true">
  <div class="toast toast--success" role="status">
    <svg class="toast-icon" aria-hidden="true"><!-- check --></svg>
    <span class="toast-message">Alteracoes salvas com sucesso.</span>
    <button class="toast-action">Desfazer</button>
    <button class="toast-close" aria-label="Fechar">
      <svg aria-hidden="true"><!-- close --></svg>
    </button>
  </div>
</div>
```

Regras de toast:
- Auto-dismiss apos 5-8 segundos (exceto erros)
- Maximo 3 toasts visiveis simultaneamente
- Posicao: bottom-center (mobile) ou top-right (desktop)
- Sempre inclua acao de desfazer quando aplicavel

### Progress Bar

```html
<div class="progress" role="progressbar"
  aria-valuenow="65" aria-valuemin="0" aria-valuemax="100"
  aria-label="Progresso do upload">
  <div class="progress-fill" style="width: 65%"></div>
  <span class="progress-label">65%</span>
</div>
```

### Skeleton Loading

```html
<div class="skeleton-card" aria-busy="true" aria-label="Carregando conteudo">
  <div class="skeleton skeleton-image"></div>
  <div class="skeleton skeleton-title"></div>
  <div class="skeleton skeleton-text"></div>
  <div class="skeleton skeleton-text skeleton-text--short"></div>
</div>
```

### Banner

```html
<div class="banner banner--info" role="banner">
  <div class="banner-content">
    <strong>Manutencao programada:</strong>
    O sistema estara indisponivel no dia 15/03 das 02h as 06h.
  </div>
  <button class="banner-dismiss" aria-label="Dispensar banner">
    <svg aria-hidden="true"><!-- close --></svg>
  </button>
</div>
```

## Usage Notes

- Use `role="alert"` para mensagens urgentes que requerem atencao imediata
- Use `role="status"` com `aria-live="polite"` para feedback nao urgente
- Toasts nao devem conter informacoes criticas — use alerts inline para isso
- Progress bars devem ter labels descritivos para screen readers
- Skeletons devem refletir o layout real do conteudo que sera carregado
- Banners persistentes devem ter opcao de dismiss e nao bloquear conteudo
