# Dev Handoff Checklist Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Feature / Ticket** | [PREENCHER — nome da feature e link do ticket] |
| **Designer**         | [PREENCHER — designer que fez o handoff]       |
| **Dev(s)**           | [PREENCHER — dev(s) que vai implementar]       |
| **Data do handoff**  | [PREENCHER — YYYY-MM-DD]                       |
| **Sprint / Ciclo**   | [PREENCHER — referencia do ciclo]              |
| **Status**           | [PREENCHER — Preparando / Entregue / Em implementacao / QA] |
| **Figma link**       | [PREENCHER — link principal do design]         |

## Instructions (Como Usar)

1. O designer preenche todas as secoes antes do handoff.
2. Agende uma sessao de handoff com o(s) dev(s) para walkthrough.
3. Use o checklist como referencia durante a implementacao.
4. Dev marca itens como "implementado" conforme avanca.
5. Designer valida o resultado final contra este checklist.

> **Dica:** Um bom handoff economiza horas de implementacao. Invista 30 minutos preenchendo bem para economizar dias de re-trabalho.

## Template

### 1. Resumo da Feature

[PREENCHER — breve descricao do que deve ser implementado, em 2-3 frases]

### 2. Design Assets

| Asset                      | Link                          | Status           |
|----------------------------|-------------------------------|------------------|
| Mockups finais (hi-fi)     | [PREENCHER — link Figma]      | [PREENCHER]      |
| Prototipo interativo       | [PREENCHER — link]            | [PREENCHER]      |
| Wireframes (referencia)    | [PREENCHER — link]            | [PREENCHER]      |
| Motion spec                | [PREENCHER — link]            | [PREENCHER]      |
| Assets exportados          | [PREENCHER — link/pasta]      | [PREENCHER]      |
| Redlines / Specs           | [PREENCHER — link]            | [PREENCHER]      |

### 3. Checklist de Preparacao (Designer)

**Visual & Layout:**
- [ ] Todos os estados documentados (default, hover, active, focus, disabled, loading, error, success)
- [ ] Empty states desenhados
- [ ] Breakpoints responsivos documentados — [PREENCHER — mobile/tablet/desktop]
- [ ] Espacamentos definidos com tokens do DS
- [ ] Cores usando tokens semanticos
- [ ] Tipografia usando escala do DS

**Conteudo:**
- [ ] Copy final aprovado (nao lorem ipsum)
- [ ] Mensagens de erro definidas
- [ ] Textos de loading/skeleton definidos
- [ ] Labels de formularios e placeholders definidos
- [ ] Tooltips e help text documentados

**Interacao:**
- [ ] Fluxo do usuario documentado
- [ ] Transicoes e animacoes especificadas
- [ ] Comportamento de scroll documentado
- [ ] Acoes de swipe (mobile) documentadas, se aplicavel

**Componentes:**
- [ ] Componentes do DS identificados — [PREENCHER — lista]
- [ ] Componentes customizados especificados — [PREENCHER — lista]
- [ ] Props e variantes documentadas para cada componente

**Acessibilidade:**
- [ ] Ordem de leitura (DOM order) definida
- [ ] ARIA labels e roles especificados
- [ ] Comportamento de teclado documentado
- [ ] Focus management definido (modais, drawers, etc.)
- [ ] Contraste verificado para todas as combinacoes de cor

**Edge Cases:**
- [ ] Textos longos / truncamento definido
- [ ] Estados de erro de rede / timeout
- [ ] Permissoes insuficientes
- [ ] Limites de dados (0 itens, 1 item, 1000+ itens)
- [ ] Inputs invalidos

### 4. Especificacoes Tecnicas

**Plataforma:** [PREENCHER — Web / iOS / Android]

**Componentes do Design System utilizados:**

| Componente DS      | Variante          | Props especificas             |
|--------------------|--------------------|-------------------------------|
| [PREENCHER]        | [PREENCHER]        | [PREENCHER]                   |
| [PREENCHER]        | [PREENCHER]        | [PREENCHER]                   |
| [PREENCHER]        | [PREENCHER]        | [PREENCHER]                   |

**Tokens utilizados:**

| Categoria    | Token name                | Valor             |
|--------------|---------------------------|--------------------|
| Color        | [PREENCHER]               | [PREENCHER]        |
| Spacing      | [PREENCHER]               | [PREENCHER]        |
| Typography   | [PREENCHER]               | [PREENCHER]        |
| Shadow       | [PREENCHER]               | [PREENCHER]        |

### 5. Comportamento por Breakpoint

| Elemento / Secao     | Mobile (<768px)        | Tablet (768-1024px)    | Desktop (>1024px)      |
|----------------------|------------------------|------------------------|------------------------|
| [PREENCHER]          | [PREENCHER]            | [PREENCHER]            | [PREENCHER]            |
| [PREENCHER]          | [PREENCHER]            | [PREENCHER]            | [PREENCHER]            |
| [PREENCHER]          | [PREENCHER]            | [PREENCHER]            | [PREENCHER]            |

### 6. Assets para Exportar

| Asset              | Formato      | Tamanho(s)        | Nome do arquivo          |
|--------------------|--------------|--------------------|--------------------------|
| [PREENCHER]        | [PREENCHER — SVG/PNG] | [PREENCHER — 1x, 2x, 3x] | [PREENCHER]     |
| [PREENCHER]        | [PREENCHER]  | [PREENCHER]        | [PREENCHER]              |

### 7. Analytics Events

| Evento                    | Trigger                     | Dados enviados               |
|---------------------------|-----------------------------|------------------------------|
| [PREENCHER — event name]  | [PREENCHER — acao do user]  | [PREENCHER — payload]        |
| [PREENCHER]               | [PREENCHER]                 | [PREENCHER]                  |
| [PREENCHER]               | [PREENCHER]                 | [PREENCHER]                  |

### 8. Checklist de Validacao (Pos-implementacao)

**Designer verifica:**
- [ ] Layout fiel ao mockup em todos os breakpoints
- [ ] Espacamentos corretos
- [ ] Cores e tipografia corretas
- [ ] Todos os estados implementados
- [ ] Animacoes/transicoes implementadas
- [ ] Empty states implementados
- [ ] Mensagens de erro corretas
- [ ] Navegacao por teclado funcional
- [ ] Screen reader anuncia corretamente

### 9. Notas para Implementacao

[PREENCHER — informacoes adicionais, decisoes de design, contexto que ajude o dev]

- [PREENCHER — nota 1]
- [PREENCHER — nota 2]
- [PREENCHER — nota 3]

### 10. Perguntas e Respostas (Handoff Session)

| Pergunta do dev                  | Resposta do designer              |
|----------------------------------|-----------------------------------|
| [PREENCHER — pergunta]           | [PREENCHER — resposta]            |
| [PREENCHER — pergunta]           | [PREENCHER — resposta]            |
| [PREENCHER — pergunta]           | [PREENCHER — resposta]            |

## Example (Parcialmente Preenchido)

**Feature:** Modal de confirmacao de exclusao
**Componentes DS:** Modal (variant: confirmation), Button (Primary danger + Secondary), Icon (warning)
**Edge case:** Se usuario clica "Excluir" e perde conexao, exibir toast de erro com opcao de retry.
**A11y:** Focus vai para o botao "Cancelar" ao abrir. Esc fecha o modal. aria-labelledby no titulo.

## Notes

- Handoff nao e um momento, e um processo. Mantenha-se disponivel para duvidas.
- Prefira handoff sincrono (reuniao) seguido do doc como referencia.
- Atualize o Figma se decisoes forem tomadas durante a implementacao.
- O checklist pos-implementacao e responsabilidade do designer — nao delegue para QA apenas.
- Documente decisoes tomadas durante implementacao que divergem do design original.
