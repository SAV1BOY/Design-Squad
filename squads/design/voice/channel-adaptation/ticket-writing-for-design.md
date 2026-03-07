# Ticket Writing for Design

## Context

Adaptação de voz para escrita de tickets (Jira, Linear, Asana) relacionados a design.
Tickets são a moeda de troca entre design e desenvolvimento — um ticket bem escrito
reduz perguntas, evita retrabalho e acelera o ciclo de entrega. Um ticket mal escrito
gera ambiguidade, implementação incorreta e frustração bilateral.

**Canal:** Ferramentas de project management (Jira, Linear, Asana)
**Audiência:** Desenvolvedores, QA, PMs
**Formalidade:** Nível 3 (Profissional)
**Tom:** Pragmatic Builder + System Thinker

## Ticket Structure

### Campos obrigatórios para tickets de design

1. **Título:** Verbo de ação + componente/tela + contexto
   - "Implementar novo card de produto na página de busca"
   - "Corrigir spacing do header em viewport mobile"
   - "Adicionar estado de empty state na lista de favoritos"

2. **Descrição:** O que e por que (2-4 frases)
   - Contextualizar o problema ou a feature
   - Conectar à user story ou objetivo de negócio
   - Referenciar decisão de design review se aplicável

3. **Design Specs:**
   - Link direto para o frame no Figma (não para o arquivo genérico)
   - Tabela de tokens utilizados
   - Lista de estados (default, hover, active, disabled, loading, error, empty)
   - Breakpoints e comportamento responsivo

4. **Critérios de aceite:**
   - Lista verificável de condições para considerar o ticket "done"
   - Incluir critérios de acessibilidade (keyboard nav, screen reader, contraste)
   - Incluir critérios de responsividade (breakpoints a testar)

5. **Assets:** Links para ícones, ilustrações, imagens que precisam ser exportados

## Writing Rules

### Títulos de ticket
- Máximo 80 caracteres
- Começar com verbo no infinitivo: Implementar, Corrigir, Adicionar, Remover, Atualizar
- Incluir contexto de localização: "...na página de checkout"
- Não usar termos vagos: "Melhorar UX do form" (melhorar como?)

### Descrição
- Primeira frase responde: O que precisa ser feito?
- Segunda frase responde: Por que isso importa?
- Terceira frase: Contexto adicional se necessário
- Quarta frase: Referências e links

### Critérios de aceite
- Formato checklist: "[ ] O botão tem min-height de 48px"
- Mensuráveis e verificáveis: "[ ] Contraste mínimo de 4.5:1 em todos os textos"
- Cobrir happy path e edge cases: "[ ] Truncate com ellipsis em nomes > 30 caracteres"
- Incluir dispositivos: "[ ] Funciona em Chrome, Safari, Firefox (últimas 2 versões)"

## Templates

### Template de ticket — Nova Feature
```
**Título:** Implementar [componente/feature] na [localização]

**Descrição:**
Adicionar [o que] para permitir que o usuário [objetivo].
Essa feature endereça [problema/métrica]. Specs validados na
design review de [data].

**Design Specs:**
- Figma: [link direto para o frame]
- Protótipo: [link para interação]
- Tokens: [tabela ou link para spec de tokens]

**Estados:**
- [ ] Default
- [ ] Hover / Focus
- [ ] Active / Pressed
- [ ] Disabled
- [ ] Loading
- [ ] Error
- [ ] Empty

**Responsivo:**
- Desktop (1440px+): [comportamento]
- Tablet (768px-1439px): [comportamento]
- Mobile (< 768px): [comportamento]

**Critérios de aceite:**
- [ ] [Critério funcional 1]
- [ ] [Critério funcional 2]
- [ ] Navegação por teclado funcional
- [ ] Screen reader anuncia [o que]
- [ ] Contraste mínimo WCAG AA
- [ ] Touch target mínimo 44x44px em mobile

**Assets:**
- [Lista de ícones/imagens com link de export]
```

### Template de ticket — Bug Visual
```
**Título:** Corrigir [o que está errado] em [localização]

**Descrição:**
[Componente] está renderizando diferente do spec de design.
Impacto: [funcional / visual / acessibilidade].

**Esperado:** [descrição + screenshot do Figma]
**Encontrado:** [descrição + screenshot da implementação]
**Ambiente:** [Browser, viewport, OS]

**Fix proposto:**
- [Token/valor que precisa mudar]

**Critérios de aceite:**
- [ ] Visual match com spec do Figma
- [ ] Não causa regressão em [componentes relacionados]
```

## Cross-References

- `voice/language-guides/feedback-to-developers.md` — Linguagem para devs
- `docs/handoff-standards.md` — Padrões de entrega
- `phrases/handoff-communication.md` — Frases para comunicar entrega
