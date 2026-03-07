# Accessibility Snippets

## Purpose

Colecao de snippets e padroes para garantir acessibilidade (a11y) em componentes de interface. Cobre ARIA attributes, keyboard navigation, focus management e semantic HTML.

## Snippets

### ARIA Roles e Labels

```html
<!-- Botao com descricao acessivel -->
<button aria-label="Fechar modal de confirmacao" aria-describedby="modal-desc">
  <svg aria-hidden="true"><!-- icon --></svg>
</button>

<!-- Live region para feedback dinamico -->
<div role="status" aria-live="polite" aria-atomic="true">
  Formulario enviado com sucesso.
</div>

<!-- Navegacao com landmark -->
<nav aria-label="Menu principal">
  <ul role="menubar">
    <li role="menuitem"><a href="/home">Inicio</a></li>
    <li role="menuitem"><a href="/about">Sobre</a></li>
  </ul>
</nav>
```

### Focus Management

```javascript
// Trap focus dentro do modal
function trapFocus(modalElement) {
  const focusable = modalElement.querySelectorAll(
    'button, [href], input, select, textarea, [tabindex]:not([tabindex="-1"])'
  );
  const first = focusable[0];
  const last = focusable[focusable.length - 1];

  modalElement.addEventListener('keydown', (e) => {
    if (e.key === 'Tab') {
      if (e.shiftKey && document.activeElement === first) {
        e.preventDefault();
        last.focus();
      } else if (!e.shiftKey && document.activeElement === last) {
        e.preventDefault();
        first.focus();
      }
    }
  });

  first.focus();
}
```

### Keyboard Navigation Patterns

```
Component         | Keys                      | Behavior
------------------|---------------------------|---------------------------
Tabs              | Arrow Left/Right          | Move entre tabs
Menu              | Arrow Up/Down             | Navegar itens
Dialog            | Escape                    | Fechar dialog
Combobox          | Arrow Down, Enter         | Abrir lista, selecionar
Accordion         | Enter/Space               | Expandir/colapsar
```

### Skip Navigation

```html
<body>
  <a href="#main-content" class="skip-link">
    Pular para conteudo principal
  </a>
  <header><!-- nav --></header>
  <main id="main-content" tabindex="-1">
    <!-- conteudo -->
  </main>
</body>
```

### Color Contrast Tokens

```
Nivel      | Ratio Minimo | Uso
-----------|-------------|---------------------------
AA Normal  | 4.5:1       | Texto body (< 18px)
AA Large   | 3:1         | Texto grande (>= 18px bold)
AAA Normal | 7:1         | Texto critico / legal
AAA Large  | 4.5:1       | Headings grandes
```

## Usage Notes

- Teste todos os componentes apenas com teclado antes de aprovar
- Use `aria-live` regions para conteudo dinamico (toasts, contadores)
- Mantenha a ordem de tab logica — evite tabindex positivo
- Sempre forneca alternativas textuais para conteudo visual
- Valide com ferramentas automatizadas (axe, Lighthouse) E teste manual
- Inclua testes de a11y no CI/CD pipeline do design system
