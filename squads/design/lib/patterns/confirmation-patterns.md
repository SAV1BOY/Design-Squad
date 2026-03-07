# Confirmation Patterns

## Pattern Description

Padroes para confirmacao de acoes destrutivas ou irreversiveis. Cobre modais de confirmacao, confirmacao inline, undo patterns e double-confirmation para acoes criticas.

## Patterns

### Modal de Confirmacao Simples

```
┌────────────────────────────────────┐
│  Excluir projeto?                  │
│                                    │
│  O projeto "Dashboard v2" e todos  │
│  os seus arquivos serao excluidos  │
│  permanentemente.                  │
│                                    │
│  [Cancelar]  [Excluir projeto]     │
└────────────────────────────────────┘
```

Regras:
- Titulo como pergunta direta
- Descricao especifica (nome do item, consequencia)
- Botao destrutivo com label especifico (nao "OK" ou "Sim")
- Botao destrutivo em vermelho (token: color-feedback-error)
- Cancelar como opcao secundaria

### Confirmacao com Input

```
┌────────────────────────────────────┐
│  Excluir organizacao               │
│                                    │
│  Esta acao e irreversivel. Todos   │
│  os dados serao perdidos.          │
│                                    │
│  Digite "excluir minha org" para   │
│  confirmar:                        │
│                                    │
│  [                              ]  │
│                                    │
│  [Cancelar] [Excluir] (disabled)   │
└────────────────────────────────────┘
```

Quando usar:
- Acoes com impacto organizacional (deletar conta, org, projeto)
- Acoes que afetam outros usuarios
- Acoes sem possibilidade de undo

### Undo Pattern (Preferivel)

```
Acao executada imediatamente:
┌──────────────────────────────────────┐
│ ✓ Item movido para lixeira. [Desfazer] │
└──────────────────────────────────────┘
```

Vantagens sobre confirmacao:
- Nao interrompe o fluxo do usuario
- Mais rapido para acoes frequentes
- Reduz "confirmation fatigue"
- Permite exploracao sem medo

### Confirmacao Inline

```
Botao "Excluir" clicado →
Botao muda para: [Tem certeza? Clique novamente]
Apos 3 segundos sem acao, reverte ao estado original.
```

### Bulk Action Confirmation

```
┌────────────────────────────────────┐
│  Arquivar 15 itens?                │
│                                    │
│  Os itens selecionados serao       │
│  movidos para o arquivo.           │
│  Voce podera restaura-los depois.  │
│                                    │
│  [Cancelar]  [Arquivar 15 itens]   │
└────────────────────────────────────┘
```

## Analysis

Hierarquia de confirmacao por severidade:
1. **Baixa** (reversivel): undo pattern — sem interrupcao
2. **Media** (consequencia moderada): modal simples
3. **Alta** (irreversivel, afeta outros): modal com input de confirmacao
4. **Critica** (dados permanentes): modal + input + cooldown timer

Nunca use confirmacao para acoes rotineiras — causa "alert fatigue".

## Tags

`confirmation`, `destructive-actions`, `undo`, `modal`, `safety-patterns`
