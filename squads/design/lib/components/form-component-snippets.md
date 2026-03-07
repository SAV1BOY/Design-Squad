# Form Component Snippets

## Purpose

Biblioteca de snippets para componentes de formulario — inputs, selects, checkboxes, radios, toggles e grupos de campos. Foco em UX de preenchimento, validacao e estados.

## Snippets

### Text Input com Validacao

```html
<div class="field" data-state="error">
  <label for="email" class="field-label">
    E-mail <span class="required" aria-hidden="true">*</span>
  </label>
  <input
    id="email"
    type="email"
    class="field-input"
    aria-required="true"
    aria-invalid="true"
    aria-describedby="email-error"
    placeholder="voce@empresa.com"
  />
  <span id="email-error" class="field-error" role="alert">
    Insira um endereco de e-mail valido.
  </span>
</div>
```

Estados do campo:
- **Default**: borda neutra, label visivel
- **Focus**: borda primaria, ring de foco
- **Filled**: borda neutra, valor visivel
- **Error**: borda vermelha, mensagem de erro
- **Disabled**: opacidade reduzida, cursor not-allowed

### Select / Dropdown

```html
<div class="field">
  <label for="country">Pais</label>
  <select id="country" class="field-select">
    <option value="" disabled selected>Selecione um pais</option>
    <option value="BR">Brasil</option>
    <option value="PT">Portugal</option>
    <option value="US">Estados Unidos</option>
  </select>
</div>
```

### Checkbox Group

```html
<fieldset>
  <legend>Interesses</legend>
  <label class="checkbox-item">
    <input type="checkbox" name="interests" value="design" />
    <span class="checkbox-label">Design de Interface</span>
  </label>
  <label class="checkbox-item">
    <input type="checkbox" name="interests" value="research" />
    <span class="checkbox-label">Pesquisa com Usuarios</span>
  </label>
  <label class="checkbox-item">
    <input type="checkbox" name="interests" value="code" />
    <span class="checkbox-label">Front-end Development</span>
  </label>
</fieldset>
```

### Toggle Switch

```html
<label class="toggle">
  <input type="checkbox" role="switch" aria-checked="false" />
  <span class="toggle-track">
    <span class="toggle-thumb"></span>
  </span>
  <span class="toggle-label">Notificacoes por e-mail</span>
</label>
```

### Form Layout Pattern

```
Vertical Stack (recomendado):
┌──────────────────┐
│ Label             │
│ [Input         ]  │
│ Helper text       │
│                   │
│ Label             │
│ [Input         ]  │
│ Helper text       │
└──────────────────┘

Inline (apenas para campos curtos relacionados):
┌──────────────────────────┐
│ [Nome     ] [Sobrenome ] │
│ [Cidade   ] [Estado ] [CEP] │
└──────────────────────────┘
```

## Usage Notes

- Labels devem ser sempre visiveis — nao use apenas placeholder como label
- Agrupe campos relacionados com `<fieldset>` e `<legend>`
- Mostre erros inline proximo ao campo, nao apenas no topo do form
- Use `autocomplete` attributes para campos comuns (name, email, address)
- Desabilite o botao de submit enquanto o form estiver invalido OU mostre erros on submit
- Valide no blur para feedback imediato, mas permita correcao sem pressao
