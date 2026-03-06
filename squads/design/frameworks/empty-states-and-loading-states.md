# Empty States and Loading States

## Metadata

| Campo         | Valor                                          |
| ------------- | ---------------------------------------------- |
| Categoria     | UI Pattern                                     |
| Complexidade  | Media                                          |
| Autor         | Design Squad                                   |
| Versao        | 1.0                                            |
| Ultima revisao| 2026-03-06                                     |
| Tags          | empty-state, loading, skeleton, spinner, zero-data |

## Concept

Empty states e loading states representam momentos criticos na experiencia do usuario — sao as
lacunas entre a intencao e o conteudo. Um design consciente desses estados transforma momentos de
espera ou ausencia em oportunidades de orientacao, educacao e engajamento.

### Tipos de Empty States

1. **Zero data** — O usuario ainda nao criou nenhum conteudo. Primeiro uso.
2. **No results** — Uma busca ou filtro nao retornou resultados.
3. **Error state** — O conteudo nao pode ser carregado por falha tecnica.
4. **Permission state** — O usuario nao tem acesso ao conteudo.
5. **Cleared state** — O usuario completou todas as tarefas (inbox zero).

### Tipos de Loading States

1. **Skeleton screen** — Placeholder estrutural que imita o layout final.
2. **Spinner / loader** — Indicador generico de processamento.
3. **Progress bar** — Para operacoes com duracao estimavel.
4. **Optimistic UI** — Mostrar resultado esperado antes da confirmacao do servidor.
5. **Stale-while-revalidate** — Mostrar dados em cache enquanto busca atualizacao.

## When to Use

- **Empty states**: toda tela que pode existir sem conteudo deve ter um estado vazio projetado.
- **Loading states**: toda operacao que leva mais de 300ms deve ter feedback visual.
- Usar skeleton quando o layout final e previsivel e a espera e curta (< 3s).
- Usar spinner quando o layout nao e previsivel ou a espera e indeterminada.
- Usar progress bar para uploads, downloads, importacoes.
- Usar optimistic UI para acoes de baixo risco (like, bookmark, mark as read).

## How to Apply

### Empty States

1. **Auditar todas as telas** e listar onde cada tipo de empty state pode ocorrer.
2. **Para zero data**: incluir ilustracao, titulo orientador, descricao breve e CTA primario.
3. **Para no results**: sugerir ajustes na busca, mostrar termos alternativos.
4. **Para error state**: explicar o problema e oferecer retry ou caminho alternativo.
5. **Para permission state**: explicar o que o usuario veria e como obter acesso.
6. **Para cleared state**: celebrar a conquista e sugerir proximo passo.

### Loading States

1. **Definir threshold de loading**: 0-300ms = nada, 300ms-1s = skeleton, >1s = skeleton + msg.
2. **Criar skeleton components** no design system para cada tipo de card/list/table.
3. **Animar skeletons** com shimmer effect sutil (pulse ou wave).
4. **Implementar optimistic UI** para acoes onde rollback e raro.
5. **Adicionar mensagens de espera** para operacoes longas ("Isso pode levar alguns segundos...").
6. **Testar em conexoes lentas** usando throttling do DevTools.

## Key Principles

- **Nunca mostrar tela em branco**: todo estado vazio e uma oportunidade de comunicacao.
- **Feedback imediato**: o usuario deve saber que algo esta acontecendo em ate 300ms.
- **Perceived performance**: skeletons fazem a espera parecer menor que spinners.
- **Orientar, nao apenas informar**: empty states devem guiar o proximo passo.
- **Consistencia**: usar os mesmos patterns de loading em toda a aplicacao.
- **Acessibilidade**: `aria-busy="true"`, `role="status"`, `aria-live="polite"` para loading.
- **Gracefulness**: transicao suave do skeleton para o conteudo real.

## Examples

### Zero Data — Pagina de Projetos

```
[Ilustracao de pasta vazia]
Titulo: "Nenhum projeto ainda"
Descricao: "Crie seu primeiro projeto para comecar a organizar seu trabalho."
CTA: [+ Criar projeto]
Link secundario: "Saiba mais sobre projetos"
```

### Skeleton — Lista de Cards

```
+---------------------------+
| [===] [================]  |    <- avatar skeleton + title skeleton
| [========================]|    <- description skeleton line 1
| [==================]      |    <- description skeleton line 2
| [====]        [===] [===] |    <- tag skeleton + action skeletons
+---------------------------+
Animacao: shimmer da esquerda para direita, 1.5s loop
```

### Error State — Feed de Notificacoes

```
[Ilustracao de nuvem com raio]
Titulo: "Nao foi possivel carregar suas notificacoes"
Descricao: "Houve um problema de conexao. Verifique sua internet e tente novamente."
CTA: [Tentar novamente]
```

### Optimistic UI — Like Button

```
1. Usuario clica no coracao
2. UI atualiza imediatamente (coracao cheio, contador +1)
3. Request enviado ao servidor em background
4. Se falhar: rollback visual + toast "Nao foi possivel salvar"
```

## Common Pitfalls

| Erro                                  | Consequencia                         | Correcao                                |
| ------------------------------------- | ------------------------------------ | --------------------------------------- |
| Tela completamente em branco          | Usuario acha que algo quebrou        | Projetar empty state para cada tela     |
| Skeleton que nao corresponde ao layout| Estranheza na transicao              | Skeleton deve espelhar o layout real    |
| Spinner para operacoes < 300ms        | Flash de loading desnecessario       | Adicionar delay minimo antes de mostrar |
| Empty state sem CTA                   | Usuario sem direcao                  | Sempre incluir acao primaria            |
| Optimistic UI sem rollback            | Estado inconsistente em caso de erro | Implementar mecanismo de undo           |
| Loading sem timeout                   | Espera infinita                      | Definir timeout e mostrar erro apos     |

## Cross-References

- [Progressive Disclosure](./progressive-disclosure.md) — loading como revelacao gradual de conteudo.
- [Error Prevention and Recovery](./error-prevention-and-recovery.md) — error states detalhados.
- [Motion Design System](./motion-design-system.md) — animacoes de skeleton e transicoes.
- [Content Design Microcopy](./content-design-microcopy.md) — copy para empty states.
- [Accessibility WCAG AA](./accessibility-wcag-aa.md) — aria attributes para estados dinamicos.
