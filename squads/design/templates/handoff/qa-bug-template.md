# QA Bug Report Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Bug ID**           | [PREENCHER — ID do ticket, ex.: BUG-1234]      |
| **Feature / Tela**   | [PREENCHER — onde o bug ocorre]                |
| **Reportado por**    | [PREENCHER — designer / QA / usuario]          |
| **Data**             | [PREENCHER — YYYY-MM-DD]                       |
| **Severidade**       | [PREENCHER — Critico / Alto / Medio / Baixo]   |
| **Tipo**             | [PREENCHER — Visual / Funcional / A11y / Performance] |
| **Plataforma**       | [PREENCHER — Web / iOS / Android]              |
| **Browser / Device** | [PREENCHER — Chrome 120 / iPhone 15 / etc.]    |
| **Ambiente**         | [PREENCHER — Staging / Producao / Local]       |
| **Status**           | [PREENCHER — Aberto / Em fix / Resolvido / Nao reproduzivel] |
| **Assigned to**      | [PREENCHER — dev responsavel]                  |

## Instructions (Como Usar)

1. Preencha todos os campos com o maximo de detalhe possivel.
2. Inclua sempre screenshots e/ou videos — sao essenciais para reproducao.
3. Descreva os steps para reproduzir de forma precisa e sequencial.
4. Indique claramente o comportamento esperado vs. o encontrado.
5. Se for um bug visual, inclua referencia do mockup original do Figma.

> **Dica:** Quanto mais facil for reproduzir o bug, mais rapido ele sera corrigido. Steps claros sao a chave.

## Template

### 1. Resumo do Bug

[PREENCHER — descricao concisa do bug em 1-2 frases. O que esta errado?]

### 2. Steps para Reproduzir

1. [PREENCHER — passo 1, ex.: Acessar a pagina /dashboard]
2. [PREENCHER — passo 2, ex.: Clicar no botao "Criar projeto"]
3. [PREENCHER — passo 3, ex.: Preencher o campo "Nome" com texto longo (100+ caracteres)]
4. [PREENCHER — passo 4, ex.: Clicar em "Salvar"]
5. [PREENCHER — passo 5, ex.: Observar o resultado]

**URL onde ocorre:** [PREENCHER — URL exata]
**Credenciais de teste:** [PREENCHER — ou link para vault]

### 3. Comportamento Esperado

[PREENCHER — o que DEVERIA acontecer de acordo com o design / spec]

**Referencia do design:** [PREENCHER — link Figma para o estado correto]

### 4. Comportamento Atual

[PREENCHER — o que REALMENTE acontece]

### 5. Evidencias Visuais

**Screenshot do bug:**
[PREENCHER — anexar imagem ou link]

**Screenshot do design esperado (Figma):**
[PREENCHER — anexar imagem ou link]

**Video de reproducao (se aplicavel):**
[PREENCHER — link para video/gif mostrando o bug]

**Comparacao lado a lado:**
| Esperado (design)          | Encontrado (implementacao)  |
|----------------------------|-----------------------------|
| [PREENCHER — screenshot]   | [PREENCHER — screenshot]    |

### 6. Detalhes do Ambiente

| Aspecto         | Valor                                      |
|-----------------|--------------------------------------------|
| Browser         | [PREENCHER — nome e versao]                |
| OS              | [PREENCHER — ex.: macOS 14.2 / Windows 11] |
| Device          | [PREENCHER — ex.: iPhone 15 Pro / Pixel 8] |
| Resolucao       | [PREENCHER — ex.: 1920x1080 / 390x844]    |
| Viewport        | [PREENCHER — se diferente da resolucao]    |
| Zoom level      | [PREENCHER — ex.: 100% / 150%]            |
| Conexao         | [PREENCHER — Wi-Fi / 4G / Simulada lenta] |
| Conta de teste  | [PREENCHER — tipo de conta / role]         |

### 7. Classificacao do Bug

**Tipo detalhado:**
- [ ] Spacing / Padding incorreto
- [ ] Cor / Token errado
- [ ] Tipografia incorreta (font, size, weight)
- [ ] Componente errado ou variante incorreta
- [ ] Comportamento de estado incorreto (hover, focus, disabled)
- [ ] Responsividade / Breakpoint incorreto
- [ ] Animacao / Transicao incorreta ou ausente
- [ ] Acessibilidade (keyboard, screen reader, contraste)
- [ ] Funcionalidade (acao nao funciona como esperado)
- [ ] Conteudo / Copy incorreto
- [ ] [PREENCHER — outro]

**Frequencia:** [PREENCHER — Sempre / As vezes / Raramente / Uma vez]
**Reproduzivel:** [PREENCHER — Sim, sempre / Sim, intermitente / Nao consegui reproduzir de novo]

### 8. Impacto

**Usuarios afetados:** [PREENCHER — todos / segmento especifico / edge case]
**Workaround disponivel:** [PREENCHER — Sim (descreva) / Nao]
**Bloqueador de release:** [PREENCHER — Sim / Nao]

### 9. Contexto Adicional

[PREENCHER — qualquer informacao adicional que ajude a entender ou resolver o bug]

- Console errors: [PREENCHER — erros no console, se aplicavel]
- Network errors: [PREENCHER — falhas de rede, se aplicavel]
- Dados de teste usados: [PREENCHER — dados especificos que trigaram o bug]
- Relacao com outros bugs: [PREENCHER — links para bugs relacionados]

### 10. Fix e Validacao

**Fix implementado:** [PREENCHER — apos o fix, descreva o que foi feito]
**Validado por:** [PREENCHER — designer/QA que validou]
**Data da validacao:** [PREENCHER — YYYY-MM-DD]
**Status final:** [PREENCHER — Resolvido / Reaberto / Won't fix]

## Example (Parcialmente Preenchido)

**Bug:** Botao "Salvar" fica cortado em tela mobile quando o teclado virtual esta aberto
**Steps:** 1. Abrir /settings no iPhone SE 2. Tocar no campo "Nome" 3. Teclado abre 4. Botao "Salvar" fica parcialmente oculto pelo teclado, sem scroll
**Esperado:** Tela faz scroll automatico para manter o botao visivel acima do teclado
**Severidade:** Alto — impede completar acao principal
**Frequencia:** Sempre, em todos os iPhones testados

## Notes

- Bugs visuais devem sempre incluir comparacao com o mockup original.
- Classifique severidade baseado no impacto para o usuario, nao na dificuldade do fix.
- Um bug bem documentado pode ser corrigido 3-5x mais rapido que um mal documentado.
- Evite agrupar multiplos bugs em um unico ticket — um bug por ticket.
- Re-teste o fix no mesmo ambiente e condicoes do bug original.
