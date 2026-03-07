# UI Style Sheet Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Produto / Feature**| [PREENCHER — nome do produto ou feature]       |
| **Designer**         | [PREENCHER — designer responsavel]             |
| **Data de criacao**  | [PREENCHER — YYYY-MM-DD]                       |
| **Versao**           | [PREENCHER — v1.0]                             |
| **Baseado em DS**    | [PREENCHER — nome do design system / N/A]      |
| **Status**           | [PREENCHER — Draft / Aprovado / Implementado]  |
| **Link Figma**       | [PREENCHER — link para style sheet no Figma]   |

## Instructions (Como Usar)

1. Defina os estilos visuais que serao usados na feature ou produto.
2. Se existe design system, referencie tokens e componentes existentes.
3. Use como guia de referencia rapida durante a implementacao.
4. Compartilhe com eng para garantir fidelidade visual no codigo.
5. Atualize quando estilos forem alterados durante o processo.

> **Dica:** Este template e para documentar decisoes visuais especificas de um projeto. Para estilos globais, use o design system.

## Template

### 1. Paleta de Cores

**Cores primarias:**

| Nome do token       | Hex         | Uso                                 |
|---------------------|-------------|--------------------------------------|
| [PREENCHER — nome]  | [PREENCHER] | [PREENCHER — onde e como usar]       |
| [PREENCHER — nome]  | [PREENCHER] | [PREENCHER]                          |
| [PREENCHER — nome]  | [PREENCHER] | [PREENCHER]                          |

**Cores secundarias:**

| Nome do token       | Hex         | Uso                                 |
|---------------------|-------------|--------------------------------------|
| [PREENCHER]         | [PREENCHER] | [PREENCHER]                          |
| [PREENCHER]         | [PREENCHER] | [PREENCHER]                          |

**Cores semanticas:**

| Nome               | Hex         | Uso                                 |
|--------------------|-------------|--------------------------------------|
| Success            | [PREENCHER] | [PREENCHER — feedback positivo]      |
| Warning            | [PREENCHER] | [PREENCHER — alertas]                |
| Error              | [PREENCHER] | [PREENCHER — erros e validacoes]     |
| Info               | [PREENCHER] | [PREENCHER — informacoes neutras]    |

**Cores neutras:**

| Nome               | Hex         | Uso                                 |
|--------------------|-------------|--------------------------------------|
| Background         | [PREENCHER] | [PREENCHER — fundo principal]        |
| Surface            | [PREENCHER] | [PREENCHER — cards, modais]          |
| Border             | [PREENCHER] | [PREENCHER — divisores, bordas]      |
| Text primary       | [PREENCHER] | [PREENCHER — corpo de texto]         |
| Text secondary     | [PREENCHER] | [PREENCHER — textos auxiliares]      |
| Text disabled      | [PREENCHER] | [PREENCHER — textos inativos]        |

### 2. Tipografia

| Nivel           | Font family   | Size  | Weight     | Line-height | Letter-spacing | Uso                    |
|-----------------|---------------|-------|------------|-------------|----------------|------------------------|
| Display         | [PREENCHER]   | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER — heroes] |
| H1              | [PREENCHER]   | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER]          |
| H2              | [PREENCHER]   | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER]          |
| H3              | [PREENCHER]   | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER]          |
| Body            | [PREENCHER]   | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER — paragrafos] |
| Body small      | [PREENCHER]   | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER]          |
| Caption         | [PREENCHER]   | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER — labels]  |
| Button          | [PREENCHER]   | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER]          |

### 3. Espacamento e Grid

**Grid system:**
- Colunas: [PREENCHER — ex.: 12 colunas]
- Gutter: [PREENCHER — ex.: 24px]
- Margin: [PREENCHER — ex.: 32px]
- Max-width: [PREENCHER — ex.: 1200px]

**Spacing scale:**

| Token       | Valor      | Uso                                    |
|-------------|------------|----------------------------------------|
| space-xs    | [PREENCHER]| [PREENCHER — ex.: inline elements]     |
| space-sm    | [PREENCHER]| [PREENCHER — ex.: dentro de cards]     |
| space-md    | [PREENCHER]| [PREENCHER — ex.: entre secoes]        |
| space-lg    | [PREENCHER]| [PREENCHER — ex.: entre blocos]        |
| space-xl    | [PREENCHER]| [PREENCHER — ex.: hero sections]       |

### 4. Bordas e Sombras

**Border radius:**

| Token          | Valor       | Uso                                  |
|----------------|-------------|--------------------------------------|
| radius-sm      | [PREENCHER] | [PREENCHER — ex.: buttons, inputs]   |
| radius-md      | [PREENCHER] | [PREENCHER — ex.: cards]             |
| radius-lg      | [PREENCHER] | [PREENCHER — ex.: modais]            |
| radius-full    | [PREENCHER] | [PREENCHER — ex.: avatars, pills]    |

**Sombras (elevation):**

| Token          | Valor (CSS)                              | Uso                     |
|----------------|------------------------------------------|-------------------------|
| shadow-sm      | [PREENCHER — box-shadow value]           | [PREENCHER — cards]     |
| shadow-md      | [PREENCHER]                              | [PREENCHER — dropdowns] |
| shadow-lg      | [PREENCHER]                              | [PREENCHER — modais]    |

### 5. Iconografia

- **Estilo:** [PREENCHER — line / filled / duotone]
- **Tamanhos:** [PREENCHER — 16px / 20px / 24px / 32px]
- **Stroke width:** [PREENCHER — ex.: 1.5px]
- **Biblioteca:** [PREENCHER — nome e link]
- **Cor padrao:** [PREENCHER — token de cor]

### 6. Componentes Utilizados

| Componente        | Fonte (DS/Custom) | Variantes usadas             | Link             |
|-------------------|--------------------|------------------------------|------------------|
| [PREENCHER]       | [PREENCHER]        | [PREENCHER — variantes]      | [PREENCHER]      |
| [PREENCHER]       | [PREENCHER]        | [PREENCHER]                  | [PREENCHER]      |
| [PREENCHER]       | [PREENCHER]        | [PREENCHER]                  | [PREENCHER]      |
| [PREENCHER]       | [PREENCHER]        | [PREENCHER]                  | [PREENCHER]      |
| [PREENCHER]       | [PREENCHER]        | [PREENCHER]                  | [PREENCHER]      |

### 7. Breakpoints

| Nome           | Min-width    | Layout changes                       |
|----------------|--------------|--------------------------------------|
| Mobile         | [PREENCHER]  | [PREENCHER — descricao]              |
| Tablet         | [PREENCHER]  | [PREENCHER — descricao]              |
| Desktop        | [PREENCHER]  | [PREENCHER — descricao]              |
| Wide           | [PREENCHER]  | [PREENCHER — descricao]              |

## Example (Parcialmente Preenchido)

**Produto:** App de gestao de tarefas
**Cor primaria:** Brand Blue #2563EB — usada em CTAs principais e links
**Tipografia:** Inter (body), Poppins (headings)
**Grid:** 12 colunas, gutter 16px (mobile) / 24px (desktop), max-width 1280px
**Spacing scale:** xs=4px, sm=8px, md=16px, lg=24px, xl=48px

## Notes

- Mantenha consistencia com o design system sempre que possivel.
- Documente excecoes e justifique desvios do DS.
- Use nomes de tokens semanticos (ex.: `text-primary`) em vez de valores literais.
- Compartilhe este sheet com eng no kick-off de implementacao.
- Verifique contraste de todas as combinacoes de cor para acessibilidade (WCAG AA minimo).
