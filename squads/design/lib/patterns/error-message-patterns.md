# Error Message Patterns

## Pattern Description

Padroes para exibicao de mensagens de erro em interfaces. Cobre erros de formulario, erros de sistema, erros de rede e erros de permissao. O objetivo e comunicar o problema de forma clara e oferecer caminhos de resolucao.

## Patterns

### Inline Field Error

```html
<div class="field field--error">
  <label for="cpf">CPF</label>
  <input id="cpf" aria-invalid="true" aria-describedby="cpf-error" />
  <span id="cpf-error" class="field-error" role="alert">
    CPF invalido. Verifique os digitos e tente novamente.
  </span>
</div>
```

Regras:
- Posicione a mensagem abaixo do campo
- Use cor vermelha (token: color-feedback-error) com icone
- Texto deve ser especifico: diga O QUE esta errado e COMO corrigir
- Evite mensagens genericas como "Campo invalido"

### Form Summary Error

```html
<div class="error-summary" role="alert" tabindex="-1">
  <h2>Corrija os seguintes erros:</h2>
  <ul>
    <li><a href="#cpf">CPF: formato invalido</a></li>
    <li><a href="#email">E-mail: campo obrigatorio</a></li>
  </ul>
</div>
```

Quando usar:
- Formularios longos (5+ campos)
- Apos tentativa de submit com erros
- Focus automatico no summary apos submit

### System Error Page

```
┌────────────────────────────────────┐
│         [Ilustracao]               │
│                                    │
│     Algo deu errado (500)          │
│                                    │
│  Estamos cientes do problema e     │
│  trabalhando para resolve-lo.      │
│                                    │
│  [Tentar novamente] [Ir ao inicio] │
└────────────────────────────────────┘
```

### Network Error Toast

```
Cenario: perda de conexao durante acao
- Exiba toast persistente (nao auto-dismiss)
- Texto: "Sem conexao. Suas alteracoes serao salvas quando reconectar."
- Acao: "Tentar novamente"
- Icone: wifi-off
```

### Permission Error

```
Cenario: usuario sem permissao para recurso
- Exiba pagina ou modal com explicacao
- Texto: "Voce nao tem permissao para acessar este recurso."
- Acao: "Solicitar acesso" ou "Voltar"
- Nunca exponha detalhes tecnicos (403, 401)
```

## Analysis

Mensagens de erro eficazes seguem o padrao:
1. **Identifique** o problema de forma clara
2. **Explique** o que aconteceu em linguagem simples
3. **Oriente** com proximo passo ou acao de recuperacao

Erros tecnicos (stack traces, codigos HTTP) nunca devem ser exibidos ao usuario final.

## Tags

`error-handling`, `feedback`, `forms`, `validation`, `ux-writing`, `a11y`
