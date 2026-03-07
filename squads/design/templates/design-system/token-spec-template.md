# Token Spec Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Token category**   | [PREENCHER — Color / Spacing / Typography / Shadow / Border] |
| **Autor(a)**         | [PREENCHER — DS designer responsavel]          |
| **Data de criacao**  | [PREENCHER — YYYY-MM-DD]                       |
| **DS Version**       | [PREENCHER — versao do design system]          |
| **Status**           | [PREENCHER — Proposta / Aprovado / Implementado] |
| **Breaking change**  | [PREENCHER — Sim / Nao]                        |
| **Impacto**          | [PREENCHER — numero de componentes afetados]   |

## Instructions (Como Usar)

1. Documente cada novo token ou alteracao de token existente usando este template.
2. Siga a convencao de nomenclatura definida pelo time de DS.
3. Inclua o valor para todos os temas (light/dark) quando aplicavel.
4. Valide que novos tokens nao conflitam com existentes.
5. Obtenha aprovacao do DS lead antes de implementar.

> **Dica:** Tokens semanticos (ex.: `color-text-primary`) sao preferidos sobre tokens primitivos (ex.: `gray-900`) em componentes.

## Template

### 1. Contexto e Justificativa

[PREENCHER — por que estes tokens estao sendo criados ou alterados? Qual problema resolvem?]

### 2. Convencao de Nomenclatura

**Formato:** `[PREENCHER — namespace]-[PREENCHER — category]-[PREENCHER — property]-[PREENCHER — variant]-[PREENCHER — state]`

**Exemplos do formato:**
- [PREENCHER — ex.: `ds-color-bg-primary-default`]
- [PREENCHER — ex.: `ds-spacing-component-padding-md`]

### 3. Tokens Primitivos (Global)

| Token name              | Valor              | Tipo        | Descricao                     |
|-------------------------|--------------------|-------------|-------------------------------|
| [PREENCHER — nome]      | [PREENCHER — valor]| [PREENCHER] | [PREENCHER — descricao]       |
| [PREENCHER — nome]      | [PREENCHER]        | [PREENCHER] | [PREENCHER]                   |
| [PREENCHER — nome]      | [PREENCHER]        | [PREENCHER] | [PREENCHER]                   |
| [PREENCHER — nome]      | [PREENCHER]        | [PREENCHER] | [PREENCHER]                   |
| [PREENCHER — nome]      | [PREENCHER]        | [PREENCHER] | [PREENCHER]                   |
| [PREENCHER — nome]      | [PREENCHER]        | [PREENCHER] | [PREENCHER]                   |
| [PREENCHER — nome]      | [PREENCHER]        | [PREENCHER] | [PREENCHER]                   |
| [PREENCHER — nome]      | [PREENCHER]        | [PREENCHER] | [PREENCHER]                   |

### 4. Tokens Semanticos

| Token name              | Referencia (primitive) | Light theme      | Dark theme       | Uso                         |
|-------------------------|------------------------|------------------|------------------|-----------------------------|
| [PREENCHER — nome]      | [PREENCHER — ref]      | [PREENCHER]      | [PREENCHER]      | [PREENCHER — onde usar]     |
| [PREENCHER — nome]      | [PREENCHER]            | [PREENCHER]      | [PREENCHER]      | [PREENCHER]                 |
| [PREENCHER — nome]      | [PREENCHER]            | [PREENCHER]      | [PREENCHER]      | [PREENCHER]                 |
| [PREENCHER — nome]      | [PREENCHER]            | [PREENCHER]      | [PREENCHER]      | [PREENCHER]                 |
| [PREENCHER — nome]      | [PREENCHER]            | [PREENCHER]      | [PREENCHER]      | [PREENCHER]                 |
| [PREENCHER — nome]      | [PREENCHER]            | [PREENCHER]      | [PREENCHER]      | [PREENCHER]                 |

### 5. Tokens de Componente (Component-specific)

| Token name              | Referencia (semantic)   | Valor resolvido  | Componente       |
|-------------------------|-------------------------|------------------|------------------|
| [PREENCHER — nome]      | [PREENCHER — ref]       | [PREENCHER]      | [PREENCHER]      |
| [PREENCHER — nome]      | [PREENCHER]             | [PREENCHER]      | [PREENCHER]      |
| [PREENCHER — nome]      | [PREENCHER]             | [PREENCHER]      | [PREENCHER]      |

### 6. Hierarquia de Referencia

```
Primitive Token          Semantic Token              Component Token
[PREENCHER] ---------> [PREENCHER] -------------> [PREENCHER]
[PREENCHER] ---------> [PREENCHER] -------------> [PREENCHER]
[PREENCHER] ---------> [PREENCHER]
```

### 7. Uso e Exemplos

**Onde usar:**
- [PREENCHER — contexto 1 de uso do token]
- [PREENCHER — contexto 2]
- [PREENCHER — contexto 3]

**Onde NAO usar:**
- [PREENCHER — anti-pattern 1]
- [PREENCHER — anti-pattern 2]

### 8. Acessibilidade

| Token pair (foreground / background)  | Contrast ratio | WCAG Level    |
|---------------------------------------|----------------|---------------|
| [PREENCHER — text] / [PREENCHER — bg] | [PREENCHER]   | [PREENCHER — AA/AAA/Fail] |
| [PREENCHER] / [PREENCHER]            | [PREENCHER]    | [PREENCHER]   |
| [PREENCHER] / [PREENCHER]            | [PREENCHER]    | [PREENCHER]   |

### 9. Migracao (se alterando tokens existentes)

| Token antigo             | Token novo               | Acao necessaria          |
|--------------------------|--------------------------|--------------------------|
| [PREENCHER — deprecated] | [PREENCHER — substituto] | [PREENCHER — rename/update] |
| [PREENCHER]              | [PREENCHER]              | [PREENCHER]              |

**Deprecation timeline:** [PREENCHER — quando o token antigo sera removido]

### 10. Implementacao

**Formato de output:**

| Plataforma   | Formato                            | Arquivo                    |
|--------------|------------------------------------|----------------------------|
| Web (CSS)    | [PREENCHER — CSS custom properties]| [PREENCHER — path]         |
| Web (JS)     | [PREENCHER — JS object/ES module] | [PREENCHER — path]         |
| iOS          | [PREENCHER — Swift/Asset Catalog] | [PREENCHER — path]         |
| Android      | [PREENCHER — XML resources]       | [PREENCHER — path]         |

**Ferramenta de build:** [PREENCHER — Style Dictionary / Tokens Studio / Custom]

## Example (Parcialmente Preenchido)

**Primitivo:** `blue-500` = #2563EB
**Semantico:** `color-action-primary-default` -> referencia `blue-500` (light) / `blue-400` (dark)
**Componente:** `button-primary-bg-default` -> referencia `color-action-primary-default`
**Contraste:** `color-action-primary-default` (#2563EB) sobre `color-bg-surface` (#FFFFFF) = 4.56:1 (AA pass)

## Notes

- Tokens primitivos nunca devem ser usados diretamente em componentes — sempre use semanticos.
- Verifique contraste de acessibilidade para TODOS os pares de cores criados.
- Mantenha a hierarquia primitive -> semantic -> component consistente.
- Documente breaking changes claramente e comunique com antecedencia aos squads.
- Use ferramentas como Style Dictionary para gerar tokens em multiplos formatos automaticamente.
