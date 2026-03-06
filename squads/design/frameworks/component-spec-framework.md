# Component Spec Framework

## Metadata
- **Autor**: Design Squad
- **Categoria**: Design Systems, Documentacao de Componentes
- **Complexidade**: Media
- **Aplicacao**: Especificar componentes com anatomy, states, props e guidelines
- **Ultima atualizacao**: 2026-03-06

## Concept

O Component Spec Framework define a estrutura padrao para especificar qualquer componente
de um design system. Uma spec completa cobre quatro dimensoes: Anatomy (partes que compoem
o componente), States (todos os estados visuais e interativos), Props (propriedades
configuráveis) e Guidelines (quando e como usar).

A premissa e que componentes mal especificados geram interpretacoes diferentes entre
designers, devs e QA. Uma spec completa funciona como contrato compartilhado que elimina
ambiguidade e reduz retrabalho.

O framework e aplicavel a qualquer componente, independente do nivel de complexidade
(atom, molecule, organism) ou da tecnologia de implementacao.

## When to Use

- Quando se adiciona um novo componente ao design system
- Quando se documenta componentes existentes que nao tem spec formal
- Quando designers e devs interpretam o mesmo componente de formas diferentes
- Quando se faz review de qualidade de componentes do sistema
- Quando novos membros precisam entender como componentes funcionam
- Quando se planeja a API publica de um componente

## How to Apply

### Secao 1 — Overview
1. **Nome**: Nome unico e consistente (mesmo no design e no codigo)
2. **Descricao**: 1-2 frases sobre o que o componente faz e quando usar
3. **Categoria**: Posicao na hierarquia (atom, molecule, organism)
4. **Status**: Draft, Beta, Stable, Deprecated

### Secao 2 — Anatomy
1. Decomponha o componente em partes nomeadas:
   - Container, Label, Icon, Badge, Divider, etc.
2. Indique quais partes sao obrigatorias e quais opcionais
3. Mostre a estrutura visual com anotacoes
4. Documente a hierarquia de partes (DOM structure)
5. Exemplo — Button anatomy:
   - Container (obrigatorio): superficie clicavel
   - Leading icon (opcional): icone antes do label
   - Label (obrigatorio): texto do botao
   - Trailing icon (opcional): icone apos o label

### Secao 3 — States
Documente cada estado com visual e descricao:
1. **Default**: Estado base sem interacao
2. **Hover**: Mouse sobre o componente (desktop)
3. **Active/Pressed**: Durante click ou tap
4. **Focus**: Foco via teclado (outline visivel obrigatorio)
5. **Disabled**: Componente desabilitado (opaco, nao interativo)
6. **Loading**: Aguardando processamento
7. **Error**: Estado de erro com mensagem
8. **Success**: Confirmacao de acao bem-sucedida
9. **Empty**: Sem dados para exibir
10. **Read-only**: Visivel mas nao editavel

Para cada estado, especifique:
- Visual: como se parece (cores, opacidade, icones)
- Behavior: como reage a interacao neste estado
- Transitions: como entra e sai deste estado

### Secao 4 — Props (API)
Documente cada propriedade configuravel:
| Prop       | Type          | Default    | Required | Description                |
|------------|---------------|------------|----------|----------------------------|
| variant    | primary/secondary/ghost | primary | no  | Estilo visual do botao    |
| size       | sm/md/lg      | md         | no       | Tamanho do componente      |
| disabled   | boolean       | false      | no       | Desabilita interacao       |
| loading    | boolean       | false      | no       | Mostra estado de loading   |
| icon       | IconName      | undefined  | no       | Icone opcional             |
| onClick    | function      | undefined  | yes      | Handler de click           |
| children   | ReactNode     | undefined  | yes      | Conteudo do botao          |

### Secao 5 — Guidelines
**Quando usar**:
- Use Button primary para a acao principal de uma pagina ou secao
- Use Button secondary para acoes alternativas
- Use Button ghost para acoes terciarias ou dentro de componentes

**Quando NAO usar**:
- Nao use Button para navegacao — use Link
- Nao use mais de 1 primary button por secao
- Nao use Button disabled sem explicar por que esta desabilitado

**Do's and Don'ts**:
- Do: Use verbos de acao no label ("Salvar", "Enviar", "Criar")
- Don't: Use labels vagos ("Ok", "Sim", "Clique aqui")
- Do: Mantenha labels curtos (1-3 palavras)
- Don't: Use labels com mais de 5 palavras

### Secao 6 — Acessibilidade
1. ARIA roles e attributes necessarios
2. Keyboard interactions (Tab, Enter, Space, Escape)
3. Screen reader announcements
4. Requisitos de contraste por estado
5. Focus management (onde o foco vai apos interacao)

### Secao 7 — Design Tokens
Liste todos os tokens usados pelo componente:
- `--button-bg-primary`: cor de fundo primary
- `--button-text-primary`: cor do texto primary
- `--button-padding-x`: padding horizontal
- `--button-border-radius`: border radius
- `--button-font-size-md`: tamanho da fonte md

## Key Principles

- **Completude**: Uma spec incompleta gera ambiguidade. Cubra todos os aspectos
- **Consistencia de formato**: Todos os componentes seguem a mesma estrutura de spec
- **Exemplos visuais**: Cada estado e variante tem representacao visual
- **API explicita**: Props documentadas com tipos, defaults e constraints
- **Guidelines opinionadas**: "Quando nao usar" e tao importante quanto "quando usar"
- **A11y como secao obrigatoria**: Acessibilidade nao e opcional
- **Versionamento**: Specs evoluem com o componente — mantenha historico

## Examples

### Exemplo 1 — Spec Completa de Input
Anatomy: Container, Label, Helper text, Input field, Leading icon, Trailing icon, Error message
States: Default, Focused, Filled, Error, Disabled, Read-only, Loading
Props: 12 props documentadas (value, onChange, label, placeholder, error, disabled, etc.)
Guidelines: 8 do's, 6 don'ts, 3 exemplos de uso correto, 3 de uso incorreto
A11y: aria-label, aria-describedby para helper/error, focus ring visivel
Tokens: 15 tokens especificos do componente

### Exemplo 2 — Spec Minima Viavel
Para um componente em status Beta, a spec minima inclui:
- Nome e descricao (2 linhas)
- Anatomy (diagrama simples)
- States: Default, Hover, Focus, Disabled (4 estados basicos)
- Props: apenas as essenciais com tipos
- 1 guideline de uso e 1 de nao-uso
Expanda para spec completa ao promover para Stable.

### Exemplo 3 — Spec Review Checklist
Antes de aprovar um componente para o DS, verifique:
- [ ] Anatomy documentada com partes nomeadas
- [ ] Pelo menos 6 estados cobertos (default, hover, focus, active, disabled, error)
- [ ] Props com tipos, defaults e descricoes
- [ ] Guidelines com pelo menos 3 do's e 3 don'ts
- [ ] A11y section com ARIA e keyboard specs
- [ ] Tokens listados e existentes no sistema
- [ ] Exemplos visuais para cada variante e estado

## Common Pitfalls

- **Spec sem estados**: Documentar so o default e cobrir 20% da experiencia real
- **Props sem tipos**: `size: any` nao e documentacao — defina tipos exatos
- **Guidelines genericas**: "Use com moderacao" nao ajuda. Seja especifico
- **A11y como afterthought**: Se a11y nao esta na spec, nao sera implementada
- **Spec desatualizada**: Spec que nao acompanha evolucao do componente e enganosa
- **Over-specification**: Especificar cada pixel em vez de referenciar tokens
- **Sem exemplos negativos**: Mostrar apenas uso correto nao previne uso incorreto

## Cross-References

- [design-system-layer.md](design-system-layer.md) — Componentes como parte do DS
- [design-token-architecture.md](design-token-architecture.md) — Tokens referenciados na spec
- [frost-atomic-design-methodology.md](frost-atomic-design-methodology.md) — Categorias de componentes
- [handoff-layer.md](handoff-layer.md) — Spec como artefato de handoff
- [accessibility-by-default.md](accessibility-by-default.md) — A11y na spec
- [frost-frontend-style-guide.md](frost-frontend-style-guide.md) — Docs vivas dos componentes
