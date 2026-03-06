# Progressive Disclosure

## Metadata

| Campo         | Valor                                      |
| ------------- | ------------------------------------------ |
| Categoria     | UI Pattern                                 |
| Complexidade  | Media                                      |
| Autor         | Design Squad                               |
| Versao        | 1.0                                        |
| Ultima revisao| 2026-03-06                                 |
| Tags          | progressive-disclosure, complexity, layered-ui |

## Concept

Progressive disclosure e uma estrategia de design de interface que organiza informacoes e funcionalidades
em camadas de complexidade crescente. O objetivo e reduzir a carga cognitiva do usuario, apresentando
apenas o essencial no primeiro momento e revelando detalhes adicionais sob demanda.

O principio central: **mostrar o que e necessario agora e esconder o que pode ser necessario depois**.

A tecnica se baseia na Lei de Hick — quanto mais opcoes visiveis, maior o tempo de decisao. Ao reduzir
o numero de elementos simultaneos, aceleramos a tomada de decisao e diminuimos a percepcao de complexidade.

Niveis tipicos de disclosure:

1. **Level 0 — Overview**: informacao minima para orientacao e triagem.
2. **Level 1 — Summary**: detalhes suficientes para a maioria das tarefas.
3. **Level 2 — Detail**: configuracoes avancadas, dados brutos, opcoes de poder.
4. **Level 3 — Expert**: APIs, bulk actions, customizacoes profundas.

## When to Use

- Interfaces com muitos campos de formulario (cadastro, configuracoes).
- Dashboards com metricas de diferentes niveis de profundidade.
- Onboarding flows onde o usuario ainda nao conhece o sistema.
- Ferramentas com funcionalidades basicas e avancadas distintas.
- Quando a pesquisa de usabilidade mostra que usuarios se sentem sobrecarregados.
- Quando ha personas com niveis de expertise diferentes usando a mesma interface.

## How to Apply

1. **Mapear todas as informacoes e acoes** disponiveis na interface.
2. **Classificar por frequencia de uso** — analytics de uso real sao a melhor fonte.
3. **Definir os niveis de disclosure** usando a hierarquia Level 0-3.
4. **Escolher o pattern de revelacao adequado**:
   - Expandable sections (accordions).
   - Tooltips e popovers para detalhes contextuais.
   - "Show more" / "Advanced options" links.
   - Steppers e wizards para fluxos multi-etapa.
   - Drawers e modais para informacao complementar.
5. **Sinalizar a existencia de conteudo oculto** — o usuario precisa saber que ha mais.
6. **Testar com usuarios** de diferentes niveis de expertise.
7. **Medir** task completion rate, time on task e error rate antes e depois.

## Key Principles

- **Relevancia temporal**: mostre informacao quando ela e util, nao antes.
- **Affordance de expansao**: deixe claro que ha conteudo adicional disponivel.
- **Reversibilidade**: o usuario deve poder colapsar o que expandiu.
- **Persistencia de estado**: lembre da preferencia do usuario entre sessoes quando possivel.
- **Escalabilidade**: o pattern deve funcionar conforme o conteudo cresce.
- **Acessibilidade**: uso correto de `aria-expanded`, `aria-controls` e `aria-hidden`.
- **Zero surpresas**: a revelacao nao deve causar reflow inesperado ou perda de contexto.

## Examples

### Formulario de Cadastro

```
Level 0: Nome, Email, Senha (campos obrigatorios)
Level 1: "Mais opcoes" -> Telefone, Empresa, Cargo
Level 2: "Configuracoes avancadas" -> Preferencias de notificacao, Integracao API
```

### Dashboard de Metricas

```
Level 0: KPIs principais em cards (receita, usuarios ativos, churn)
Level 1: Click no card -> grafico de tendencia + breakdown
Level 2: "Ver detalhes" -> tabela completa com filtros
Level 3: "Exportar" / "Abrir no analytics" -> dados brutos
```

### Settings Page

```
Level 0: Categorias com resumo (Perfil: "Joao Silva, joao@email.com")
Level 1: Expandir categoria -> campos editaveis comuns
Level 2: "Opcoes avancadas" -> configuracoes de seguranca, tokens
```

## Common Pitfalls

| Erro                              | Consequencia                              | Correcao                                   |
| --------------------------------- | ----------------------------------------- | ------------------------------------------ |
| Esconder funcoes criticas         | Usuario nao encontra o que precisa         | Testar com card sorting e tree testing      |
| Nenhuma indicacao de mais conteudo| Usuario acha que viu tudo                  | Adicionar affordances claras de expansao    |
| Muitos niveis de profundidade     | Navegacao se torna labirintica             | Limitar a 3 niveis maximo                   |
| Disclosure inconsistente          | Modelo mental quebrado                     | Padronizar patterns no design system        |
| Ignorar reduced motion            | Animacao de revelacao causa desconforto    | Respeitar `prefers-reduced-motion`          |
| Reflow agressivo                  | Usuario perde o contexto visual            | Revelar conteudo abaixo, nunca deslocar     |

## Cross-References

- [Empty States and Loading States](./empty-states-and-loading-states.md) — estados intermediarios durante disclosure.
- [Accessibility WCAG AA](./accessibility-wcag-aa.md) — aria attributes para elementos expansiveis.
- [Motion Design System](./motion-design-system.md) — animacoes de revelacao e transicao.
- [Content Design Microcopy](./content-design-microcopy.md) — microcopy para labels de expansao.
- [Responsive Design System](./responsive-design-system.md) — disclosure pode variar por breakpoint.
