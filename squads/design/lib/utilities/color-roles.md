# Color Roles

## Purpose

Mapeamento de roles semanticos de cor para uso consistente na interface. Define como cores sao aplicadas por funcao (nao por valor), facilitando temas e acessibilidade.

## Role Definitions

### Surface Colors
```
Token                        | Role                    | Light          | Dark
-----------------------------|-------------------------|----------------|----------------
--color-surface-default      | Fundo principal         | white          | gray-900
--color-surface-subtle       | Fundo secundario        | gray-50        | gray-800
--color-surface-muted        | Fundo terciario         | gray-100       | gray-700
--color-surface-elevated     | Cards e elementos       | white          | gray-800
--color-surface-overlay      | Modais, scrim           | black/50%      | black/70%
```

### Text Colors
```
Token                        | Role                    | Light          | Dark
-----------------------------|-------------------------|----------------|----------------
--color-text-default         | Texto principal         | gray-900       | gray-50
--color-text-subtle          | Texto secundario        | gray-600       | gray-400
--color-text-muted           | Texto desabilitado      | gray-400       | gray-600
--color-text-on-action       | Texto sobre botao       | white          | white
--color-text-link            | Links                   | blue-600       | blue-400
```

### Action Colors
```
Token                        | Role                    | Default        | Hover
-----------------------------|-------------------------|----------------|----------------
--color-action-primary       | CTA principal           | blue-600       | blue-700
--color-action-secondary     | Acao secundaria         | gray-100       | gray-200
--color-action-danger        | Acao destrutiva         | red-600        | red-700
--color-action-disabled      | Acao desabilitada       | gray-200       | gray-700
```

### Feedback Colors
```
Token                        | Role                    | Background     | Text/Icon
-----------------------------|-------------------------|----------------|----------------
--color-feedback-success     | Sucesso                 | green-50       | green-700
--color-feedback-warning     | Atencao                 | yellow-50      | yellow-800
--color-feedback-error       | Erro                    | red-50         | red-700
--color-feedback-info        | Informacao              | blue-50        | blue-700
```

### Border Colors
```
Token                        | Role                    | Light          | Dark
-----------------------------|-------------------------|----------------|----------------
--color-border-default       | Borda padrao            | gray-200       | gray-700
--color-border-subtle        | Borda sutil             | gray-100       | gray-800
--color-border-strong        | Borda enfatizada        | gray-400       | gray-500
--color-border-focus         | Focus ring              | blue-500       | blue-400
```

## Contrast Requirements

```
Combinacao                    | Ratio Minimo | Nivel
------------------------------|-------------|--------
text-default / surface        | 4.5:1       | AA
text-subtle / surface         | 4.5:1       | AA
text-on-action / action       | 4.5:1       | AA
feedback-text / feedback-bg   | 4.5:1       | AA
border-default / surface      | 3:1         | AA (non-text)
```

## Usage Notes

- Nunca use cores por nome (blue-600) — sempre use o role (action-primary)
- Roles facilitam troca de tema sem alterar componentes
- Teste todas as combinacoes de cor com ferramenta de contraste
- Documente novos roles antes de adicionar a paleta
- Mantenha o numero de roles minimo — menos e mais consistente
