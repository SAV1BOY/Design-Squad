# Edge Cases Documentation Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Feature / Fluxo**  | [PREENCHER — nome da feature]                  |
| **Designer**         | [PREENCHER — responsavel]                      |
| **Data de criacao**  | [PREENCHER — YYYY-MM-DD]                       |
| **Versao**           | [PREENCHER — v1.0]                             |
| **Status**           | [PREENCHER — Em mapeamento / Completo / Validado com eng] |
| **Link do design**   | [PREENCHER — link Figma com estados]           |

## Instructions (Como Usar)

1. Mapeie edge cases durante o processo de design, nao no handoff.
2. Categorize por tipo para facilitar revisao com eng.
3. Para cada edge case, defina o comportamento esperado e o design correspondente.
4. Revise com eng e QA para identificar cases que voce pode ter perdido.
5. Use como referencia durante QA para validar cobertura.

> **Dica:** Edge cases sao onde a maioria dos bugs mora. Documentar cedo previne surpresas tardias.

## Template

### 1. Overview do Fluxo

[PREENCHER — breve descricao do fluxo e seus limites/boundaries]

**Happy path resumido:** [PREENCHER — steps do caminho feliz]

### 2. Edge Cases — Dados e Conteudo

| # | Cenario                                | Comportamento esperado               | Design link          |
|---|----------------------------------------|--------------------------------------|----------------------|
| 1 | [PREENCHER — texto vazio]              | [PREENCHER — placeholder ou msg]     | [PREENCHER — frame]  |
| 2 | [PREENCHER — texto muito longo]        | [PREENCHER — truncar com ellipsis?]  | [PREENCHER]          |
| 3 | [PREENCHER — caracteres especiais]     | [PREENCHER — sanitizar / exibir]     | [PREENCHER]          |
| 4 | [PREENCHER — emojis no input]          | [PREENCHER — permitir / bloquear]    | [PREENCHER]          |
| 5 | [PREENCHER — numeros negativos]        | [PREENCHER — validacao]              | [PREENCHER]          |
| 6 | [PREENCHER — valor zero]               | [PREENCHER — exibicao]               | [PREENCHER]          |
| 7 | [PREENCHER — campo obrigatorio vazio]  | [PREENCHER — mensagem de erro]       | [PREENCHER]          |

### 3. Edge Cases — Limites e Quantidades

| # | Cenario                                | Comportamento esperado               | Design link          |
|---|----------------------------------------|--------------------------------------|----------------------|
| 1 | [PREENCHER — 0 itens na lista]         | [PREENCHER — empty state]            | [PREENCHER]          |
| 2 | [PREENCHER — 1 item na lista]          | [PREENCHER — singular vs plural]     | [PREENCHER]          |
| 3 | [PREENCHER — maximo de itens]          | [PREENCHER — limite / paginacao]     | [PREENCHER]          |
| 4 | [PREENCHER — excede limite de upload]  | [PREENCHER — mensagem de limite]     | [PREENCHER]          |
| 5 | [PREENCHER — arquivo muito grande]     | [PREENCHER — mensagem]               | [PREENCHER]          |

### 4. Edge Cases — Estado e Conectividade

| # | Cenario                                | Comportamento esperado               | Design link          |
|---|----------------------------------------|--------------------------------------|----------------------|
| 1 | [PREENCHER — sem conexao internet]     | [PREENCHER — offline state]          | [PREENCHER]          |
| 2 | [PREENCHER — conexao lenta]            | [PREENCHER — loading prolongado]     | [PREENCHER]          |
| 3 | [PREENCHER — timeout de API]           | [PREENCHER — retry / mensagem]       | [PREENCHER]          |
| 4 | [PREENCHER — erro 500 do servidor]     | [PREENCHER — error state generico]   | [PREENCHER]          |
| 5 | [PREENCHER — sessao expirada]          | [PREENCHER — redirect login]         | [PREENCHER]          |
| 6 | [PREENCHER — acao duplicada (double click)] | [PREENCHER — debounce / disable] | [PREENCHER]          |

### 5. Edge Cases — Permissoes e Acesso

| # | Cenario                                | Comportamento esperado               | Design link          |
|---|----------------------------------------|--------------------------------------|----------------------|
| 1 | [PREENCHER — sem permissao de leitura] | [PREENCHER — 403 / mensagem]        | [PREENCHER]          |
| 2 | [PREENCHER — sem permissao de edicao]  | [PREENCHER — view-only mode]        | [PREENCHER]          |
| 3 | [PREENCHER — conta trial/free]         | [PREENCHER — upgrade prompt]         | [PREENCHER]          |
| 4 | [PREENCHER — link compartilhado invalido] | [PREENCHER — error page]         | [PREENCHER]          |

### 6. Edge Cases — Multi-usuario e Concorrencia

| # | Cenario                                | Comportamento esperado               | Design link          |
|---|----------------------------------------|--------------------------------------|----------------------|
| 1 | [PREENCHER — 2 usuarios editando simultaneamente] | [PREENCHER — conflict resolution] | [PREENCHER] |
| 2 | [PREENCHER — item deletado por outro usuario] | [PREENCHER — notificacao/refresh] | [PREENCHER]       |
| 3 | [PREENCHER — dados desatualizados]     | [PREENCHER — stale data handling]    | [PREENCHER]          |

### 7. Edge Cases — Dispositivos e Plataforma

| # | Cenario                                | Comportamento esperado               | Design link          |
|---|----------------------------------------|--------------------------------------|----------------------|
| 1 | [PREENCHER — viewport muito pequeno]   | [PREENCHER — min-width / scroll]     | [PREENCHER]          |
| 2 | [PREENCHER — zoom 200%]               | [PREENCHER — layout adaptado]        | [PREENCHER]          |
| 3 | [PREENCHER — landscape mobile]         | [PREENCHER — layout adaptado]        | [PREENCHER]          |
| 4 | [PREENCHER — dark mode]                | [PREENCHER — cores adaptadas]        | [PREENCHER]          |
| 5 | [PREENCHER — navegador sem JS]         | [PREENCHER — degradacao graceful]    | [PREENCHER]          |

### 8. Edge Cases — Acessibilidade

| # | Cenario                                | Comportamento esperado               |
|---|----------------------------------------|--------------------------------------|
| 1 | [PREENCHER — navegacao por teclado apenas] | [PREENCHER — todos elementos acessiveis] |
| 2 | [PREENCHER — screen reader ativo]      | [PREENCHER — anuncios corretos]      |
| 3 | [PREENCHER — prefers-reduced-motion]   | [PREENCHER — animacoes desativadas]  |
| 4 | [PREENCHER — alto contraste]           | [PREENCHER — legibilidade mantida]   |
| 5 | [PREENCHER — font-size aumentado pelo usuario] | [PREENCHER — layout nao quebra] |

### 9. Decisoes e Trade-offs

| Edge case                       | Decisao tomada                    | Justificativa                    |
|---------------------------------|-----------------------------------|----------------------------------|
| [PREENCHER — case]              | [PREENCHER — como tratamos]       | [PREENCHER — por que]            |
| [PREENCHER — case]              | [PREENCHER]                       | [PREENCHER]                      |
| [PREENCHER — case]              | [PREENCHER]                       | [PREENCHER]                      |

### 10. Cobertura e Status

| Categoria              | Total de cases | Documentados | Com design     | Implementados  |
|------------------------|----------------|--------------|----------------|----------------|
| Dados e conteudo       | [PREENCHER]    | [PREENCHER]  | [PREENCHER]    | [PREENCHER]    |
| Limites e quantidades  | [PREENCHER]    | [PREENCHER]  | [PREENCHER]    | [PREENCHER]    |
| Estado e conectividade | [PREENCHER]    | [PREENCHER]  | [PREENCHER]    | [PREENCHER]    |
| Permissoes e acesso    | [PREENCHER]    | [PREENCHER]  | [PREENCHER]    | [PREENCHER]    |
| Multi-usuario          | [PREENCHER]    | [PREENCHER]  | [PREENCHER]    | [PREENCHER]    |
| Dispositivos           | [PREENCHER]    | [PREENCHER]  | [PREENCHER]    | [PREENCHER]    |
| Acessibilidade         | [PREENCHER]    | [PREENCHER]  | [PREENCHER]    | [PREENCHER]    |

## Example (Parcialmente Preenchido)

**Feature:** Formulario de criacao de projeto
**Edge case — Texto longo:** Nome do projeto com 200+ caracteres -> Truncar com ellipsis apos 80 caracteres na listagem, exibir completo na pagina do projeto. Tooltip no hover mostra nome completo.
**Edge case — Double click:** Botao "Criar" desabilitado apos primeiro click + loading spinner. Reabilita apos timeout de 5s se nao receber resposta.

## Notes

- Comece mapeando os edge cases mais provaveis, depois cubra os mais raros.
- Envolva eng e QA no mapeamento — eles pensam em cenarios que designers podem nao considerar.
- Nem todo edge case precisa de design custom — as vezes um comportamento generico e suficiente.
- Documente decisoes de "nao tratar agora" com justificativa para revisao futura.
- Use esta documentacao como base para test cases do QA.
