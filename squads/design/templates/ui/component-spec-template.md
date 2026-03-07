# Component Spec Template

## Metadata

| Campo                | Valor                                            |
|----------------------|--------------------------------------------------|
| **Componente**       | [PREENCHER — nome do componente]                 |
| **Designer**         | [PREENCHER — designer responsavel]               |
| **Eng counterpart**  | [PREENCHER — dev que vai implementar]            |
| **Data de criacao**  | [PREENCHER — YYYY-MM-DD]                         |
| **Versao**           | [PREENCHER — v1.0]                               |
| **Design System**    | [PREENCHER — DS existente ou standalone]         |
| **Status**           | [PREENCHER — Draft / Review / Approved / Shipped]|
| **Figma link**       | [PREENCHER — link para component page]           |

## Instructions (Como Usar)

1. Crie este spec apos finalizar o design do componente no Figma.
2. Detalhe todos os estados, variantes e propriedades.
3. Revise com o dev responsavel antes de iniciar implementacao.
4. Use como referencia durante QA para validar fidelidade.
5. Atualize quando o componente receber alteracoes.

> **Dica:** Quanto mais detalhado o spec, menos idas e vindas durante a implementacao. Invista tempo aqui.

## Template

### 1. Descricao do Componente

[PREENCHER — o que e este componente? Para que serve? Onde e usado?]

**Anatomia:**
```
+--------------------------------------------------+
| [PREENCHER — Leading icon/element] (opcional)     |
| [PREENCHER — Label / Content area]               |
| [PREENCHER — Trailing icon/action] (opcional)     |
| [PREENCHER — Helper text / Description] (opcional)|
+--------------------------------------------------+
```

### 2. Propriedades (Props)

| Prop           | Tipo                    | Default         | Obrigatoria | Descricao                      |
|----------------|-------------------------|-----------------|-------------|--------------------------------|
| [PREENCHER]    | [PREENCHER — string/boolean/enum] | [PREENCHER] | Sim/Nao | [PREENCHER — o que faz]    |
| [PREENCHER]    | [PREENCHER]             | [PREENCHER]     | [PREENCHER] | [PREENCHER]                    |
| [PREENCHER]    | [PREENCHER]             | [PREENCHER]     | [PREENCHER] | [PREENCHER]                    |
| [PREENCHER]    | [PREENCHER]             | [PREENCHER]     | [PREENCHER] | [PREENCHER]                    |
| [PREENCHER]    | [PREENCHER]             | [PREENCHER]     | [PREENCHER] | [PREENCHER]                    |

### 3. Variantes

| Variante       | Descricao                          | Quando usar                       |
|----------------|------------------------------------|-----------------------------------|
| [PREENCHER]    | [PREENCHER — descricao visual]     | [PREENCHER — contexto de uso]     |
| [PREENCHER]    | [PREENCHER]                        | [PREENCHER]                       |
| [PREENCHER]    | [PREENCHER]                        | [PREENCHER]                       |
| [PREENCHER]    | [PREENCHER]                        | [PREENCHER]                       |

### 4. Estados

| Estado          | Visual                            | Comportamento                     |
|-----------------|-----------------------------------|-----------------------------------|
| Default         | [PREENCHER — descricao visual]    | [PREENCHER — interacao]           |
| Hover           | [PREENCHER — mudancas visuais]    | [PREENCHER — cursor, feedback]    |
| Active/Pressed  | [PREENCHER — mudancas visuais]    | [PREENCHER — feedback]            |
| Focus           | [PREENCHER — focus ring style]    | [PREENCHER — teclado behavior]    |
| Disabled        | [PREENCHER — opacity, cor]        | [PREENCHER — nao clicavel]        |
| Loading         | [PREENCHER — skeleton/spinner]    | [PREENCHER — interacao bloqueada] |
| Error           | [PREENCHER — cor, icone]          | [PREENCHER — mensagem]            |
| Success         | [PREENCHER — cor, icone]          | [PREENCHER — feedback]            |

### 5. Tamanhos

| Size    | Height  | Padding (h/v)   | Font size | Icon size | Uso                   |
|---------|---------|------------------|-----------|-----------|------------------------|
| Small   | [PREENCHER] | [PREENCHER]  | [PREENCHER] | [PREENCHER] | [PREENCHER]        |
| Medium  | [PREENCHER] | [PREENCHER]  | [PREENCHER] | [PREENCHER] | [PREENCHER]        |
| Large   | [PREENCHER] | [PREENCHER]  | [PREENCHER] | [PREENCHER] | [PREENCHER]        |

### 6. Spacing e Layout

**Espacamento interno:**
- Padding horizontal: [PREENCHER — token]
- Padding vertical: [PREENCHER — token]
- Gap entre elementos: [PREENCHER — token]

**Espacamento externo (recomendado):**
- Margin-bottom: [PREENCHER — token]
- Distancia de outros componentes: [PREENCHER — token]

**Largura:** [PREENCHER — fixed / fluid / hug content]
**Alinhamento:** [PREENCHER — left / center / stretch]

### 7. Tokens Visuais

| Propriedade      | Token / Valor                      | Estado         |
|------------------|------------------------------------|----------------|
| Background       | [PREENCHER — token ou hex]         | Default        |
| Background       | [PREENCHER]                        | Hover          |
| Text color       | [PREENCHER]                        | Default        |
| Border           | [PREENCHER — width, style, color]  | Default        |
| Border           | [PREENCHER]                        | Focus          |
| Border-radius    | [PREENCHER]                        | Todos          |
| Shadow           | [PREENCHER]                        | [PREENCHER]    |

### 8. Acessibilidade

- **Role ARIA:** [PREENCHER — ex.: button, checkbox, dialog]
- **Keyboard interaction:**
  - [PREENCHER — tecla]: [PREENCHER — comportamento]
  - [PREENCHER — tecla]: [PREENCHER — comportamento]
- **Screen reader:** [PREENCHER — como deve ser anunciado]
- **Focus management:** [PREENCHER — ordem e comportamento de foco]
- **Contraste minimo:** [PREENCHER — ratio verificado]

### 9. Animacao / Motion

| Propriedade animada  | Duracao      | Easing                | Trigger              |
|----------------------|--------------|-----------------------|----------------------|
| [PREENCHER]          | [PREENCHER]  | [PREENCHER — ease-in-out/etc.] | [PREENCHER — hover/click] |
| [PREENCHER]          | [PREENCHER]  | [PREENCHER]           | [PREENCHER]          |

**prefers-reduced-motion:** [PREENCHER — comportamento sem animacao]

### 10. Do's and Don'ts

**Do (Usar assim):**
- [PREENCHER — uso correto 1]
- [PREENCHER — uso correto 2]
- [PREENCHER — uso correto 3]

**Don't (Nao usar assim):**
- [PREENCHER — uso incorreto 1]
- [PREENCHER — uso incorreto 2]
- [PREENCHER — uso incorreto 3]

## Example (Parcialmente Preenchido)

**Componente:** Button
**Variantes:** Primary (filled), Secondary (outlined), Ghost (text-only)
**Tamanhos:** Small (32px), Medium (40px), Large (48px)
**Prop `loading`:** boolean, default false — quando true, substitui o label por spinner e desabilita interacao.
**A11y:** role="button", Enter/Space para ativar, focus ring 2px offset com cor `focus-ring`.

## Notes

- Mantenha o spec sincronizado com o componente no Figma.
- Inclua exemplos de uso (do) e anti-patterns (don't) para guiar outros designers.
- Specs devem ser revisados por eng ANTES da implementacao comecar.
- Documente breaking changes quando atualizar versoes do componente.
- Considere criar Storybook stories que espelhem os estados documentados aqui.
