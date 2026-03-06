# Content Design Microcopy

## Metadata

| Campo         | Valor                                         |
| ------------- | --------------------------------------------- |
| Categoria     | Content Design                                |
| Complexidade  | Media                                         |
| Autor         | Design Squad                                  |
| Versao        | 1.0                                           |
| Ultima revisao| 2026-03-06                                    |
| Tags          | microcopy, content-design, tone, ux-writing   |

## Concept

Microcopy e o texto funcional que guia o usuario dentro de uma interface: labels de botoes,
mensagens de erro, placeholders, tooltips, empty states, confirmacoes e notificacoes. Content
design e a disciplina que trata esse texto como componente de design — com a mesma intencionalidade
de cor, tipografia e espacamento.

### Pilares do Content Design

1. **Tom (Tone)**: a personalidade da comunicacao — varia conforme contexto e emocao do usuario.
2. **Clareza**: informacao sem ambiguidade, jargao ou redundancia.
3. **Utilidade**: cada palavra deve servir a um proposito funcional.
4. **Inclusao**: linguagem acessivel, neutra e respeitosa.

### Espectro de Tom

```
Contexto de sucesso:  ----[casual]---[neutro]---[formal]----
Contexto de erro:     ----[empatico]-[neutro]---[tecnico]---
Contexto de alerta:   ----[urgente]--[neutro]---[informativo]
```

O tom se ajusta ao contexto emocional do usuario. Em momentos de frustacao (erro, bloqueio),
o tom deve ser mais empatico. Em momentos de conquista, pode ser mais casual.

## When to Use

- Em toda interface que contem texto — ou seja, todas.
- Ao criar novos componentes no design system.
- Ao projetar fluxos de erro, onboarding, empty states e confirmacoes.
- Quando metricas indicam confusao, abandono ou erros frequentes.
- Em localizacao e internacionalizacao de produtos.

## How to Apply

### 1. Botoes e CTAs

**Regra**: usar verbos de acao que descrevem o resultado, nao o processo.

```
Ruim:   [Submeter]  [OK]  [Clique aqui]
Bom:    [Salvar alteracoes]  [Criar conta]  [Enviar convite]
```

- Maximo 3-4 palavras.
- Verbo no infinitivo para acoes ("Criar projeto") ou imperativo ("Crie seu projeto").
- Ser especifico: "Excluir projeto" em vez de "Excluir".

### 2. Mensagens de Erro

**Estrutura**: O que aconteceu + Por que + O que fazer.

```
Ruim:   "Erro 422: Unprocessable Entity"
Bom:    "Nao foi possivel salvar. O campo email esta em formato invalido.
         Verifique e tente novamente."
```

- Nao culpar o usuario ("Voce errou" -> "O email precisa ter @").
- Ser especifico sobre o campo e o problema.
- Oferecer caminho de correcao.

### 3. Empty States

**Estrutura**: O que e este lugar + Por que esta vazio + O que fazer.

```
Ruim:   "Nenhum resultado"
Bom:    "Nenhum projeto encontrado. Tente ajustar os filtros ou crie um novo projeto."
```

### 4. Confirmacoes e Alertas

**Estrutura**: O que vai acontecer + Consequencia + Opcoes claras.

```
Ruim:   "Tem certeza?" [Sim] [Nao]
Bom:    "Excluir o projeto 'Landing Page'? Esta acao nao pode ser desfeita.
         Todos os arquivos serao removidos." [Cancelar] [Excluir projeto]
```

### 5. Placeholders e Hints

```
Placeholder: exemplo do formato esperado ("nome@empresa.com")
Hint text:   instrucao sobre requisitos ("Minimo 8 caracteres, incluindo 1 numero")
Nao usar placeholder como substituto de label.
```

### 6. Loading e Feedback

```
Acao rapida (<3s):  Sem texto, apenas indicador visual
Acao media (3-10s): "Salvando..." / "Processando pagamento..."
Acao longa (>10s):  "Estamos gerando seu relatorio. Isso pode levar ate 30 segundos."
Sucesso:            "Projeto criado com sucesso" (toast, auto-dismiss 5s)
```

## Key Principles

- **Front-load information**: colocar a informacao mais importante primeiro.
- **Uma ideia por frase**: frases curtas, sem subordinadas complexas.
- **Voz ativa**: "O sistema salvou seu arquivo" -> "Seu arquivo foi salvo".
- **Consistencia terminologica**: um conceito = um termo em todo o produto.
- **Scannability**: usuarios escaneiam, nao leem — facilitar a triagem visual.
- **Contexto emocional**: adaptar tom ao momento emocional do usuario.
- **Testavel**: microcopy pode e deve ser A/B testado.

## Examples

### Glossario de Consistencia

| Conceito         | Usar                | Nao usar                   |
| ---------------- | ------------------- | -------------------------- |
| Remover item     | Excluir             | Deletar, remover, apagar   |
| Desfazer acao    | Desfazer            | Reverter, voltar atras     |
| Sair da conta    | Sair                | Logout, desconectar        |
| Melhorar plano   | Fazer upgrade       | Atualizar plano            |
| Ajuda            | Central de ajuda    | FAQ, suporte, help center  |

### Fluxo de Exclusao Completo

```
Link:         "Excluir conta"
Confirmacao:  "Tem certeza que deseja excluir sua conta?"
Detalhe:      "Todos os seus dados serao removidos em 14 dias.
               Voce pode cancelar a exclusao durante esse periodo."
CTA:          [Manter conta]  [Excluir minha conta]
Feedback:     "Sua conta sera excluida em 14 dias. Enviamos um email de confirmacao."
```

## Common Pitfalls

| Erro                              | Consequencia                          | Correcao                                 |
| --------------------------------- | ------------------------------------- | ---------------------------------------- |
| Jargao tecnico                    | Usuario nao entende                   | Usar linguagem do dia a dia              |
| Tom inconsistente entre telas     | Experiencia fragmentada               | Criar voice & tone guidelines            |
| Botoes genericos ("OK", "Sim")    | Ambiguidade na acao                   | Descrever a acao no label do botao       |
| Placeholder como label            | Label desaparece, acessibilidade ruim | Usar label visivel separado              |
| Excesso de exclamacoes            | Tom parece falso ou ansioso           | Pontuar com moderacao                    |
| Texto muito longo em UI           | Ninguem le                            | Editar ate cada palavra ser essencial    |

## Cross-References

- [Error Prevention and Recovery](./error-prevention-and-recovery.md) — microcopy de erros.
- [Empty States and Loading States](./empty-states-and-loading-states.md) — copy de empty states.
- [Progressive Disclosure](./progressive-disclosure.md) — labels de expansao e revelacao.
- [Accessibility WCAG AA](./accessibility-wcag-aa.md) — linguagem clara e compreensivel.
- [Design Review and Critique](./design-review-and-critique.md) — review de microcopy no ritual.
