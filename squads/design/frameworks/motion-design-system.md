# Motion Design System

## Metadata

| Campo         | Valor                                         |
| ------------- | --------------------------------------------- |
| Categoria     | Design System                                 |
| Complexidade  | Alta                                          |
| Autor         | Design Squad                                  |
| Versao        | 1.0                                           |
| Ultima revisao| 2026-03-06                                    |
| Tags          | motion, animation, easing, duration, a11y     |

## Concept

Um motion design system define os principios, tokens e padroes de animacao de uma interface de forma
sistematica. Motion e uma ferramenta funcional — comunica relacoes espaciais, fornece feedback,
direciona atencao e suaviza transicoes de estado. Quando mal aplicada, distrai e irrita.

### Motion Tokens

Motion tokens sao valores padronizados que garantem consistencia e eficiencia na aplicacao de animacoes.

**Duration tokens:**

| Token              | Valor   | Uso                                          |
| ------------------ | ------- | -------------------------------------------- |
| `duration-instant` | 100ms   | Micro-interacoes (hover, focus ring)          |
| `duration-fast`    | 200ms   | Feedback de acao (click, toggle)              |
| `duration-normal`  | 300ms   | Transicoes de componente (expand, collapse)   |
| `duration-slow`    | 500ms   | Transicoes de layout (page, modal)            |
| `duration-slower`  | 700ms   | Animacoes decorativas (onboarding, empty)     |

**Easing tokens:**

| Token               | Valor                        | Uso                                  |
| -------------------- | ---------------------------- | ------------------------------------ |
| `ease-default`       | cubic-bezier(0.4, 0, 0.2, 1)| Movimentos padrao                    |
| `ease-in`            | cubic-bezier(0.4, 0, 1, 1)  | Elementos saindo da tela             |
| `ease-out`           | cubic-bezier(0, 0, 0.2, 1)  | Elementos entrando na tela           |
| `ease-in-out`        | cubic-bezier(0.4, 0, 0.2, 1)| Elementos que mudam de posicao       |
| `ease-spring`        | cubic-bezier(0.175, 0.885, 0.32, 1.275) | Interacoes ludicas      |

## When to Use

- Para dar feedback visual a acoes do usuario (click, hover, drag).
- Para comunicar mudancas de estado (loading, success, error).
- Para orientar atencao para novos elementos ou mudancas na interface.
- Para suavizar transicoes de layout que seriam abruptas.
- Para criar sensacao de profundidade e espacialidade.
- Nunca para decoracao pura sem funcao comunicativa.

## How to Apply

### 1. Categorizar o Tipo de Motion

- **Feedback motion**: resposta imediata a interacao (button press, switch toggle).
- **Transition motion**: mudanca de um estado para outro (page transition, accordion).
- **Choreography motion**: multiplos elementos se movendo em sequencia coordenada.
- **Ambient motion**: animacao sutil continua (skeleton shimmer, pulse).
- **Illustrative motion**: animacao decorativa com proposito educativo (onboarding).

### 2. Aplicar Duration Correta

Regra geral: **quanto menor o elemento, menor a duration.**

```
Icone de 16px mudando de cor:       100ms (instant)
Botao respondendo a click:          200ms (fast)
Card expandindo com detalhes:       300ms (normal)
Modal abrindo com overlay:          300-500ms (normal-slow)
Transicao de pagina inteira:        500ms (slow)
```

### 3. Escolher Easing Adequado

```
Elemento entrando na tela:   ease-out (comeca rapido, desacelera)
Elemento saindo da tela:     ease-in (comeca lento, acelera)
Elemento mudando de posicao: ease-in-out (suave nas duas pontas)
Feedback de interacao:       ease-default (natural)
```

### 4. prefers-reduced-motion

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

Alternativa melhor — reduzir em vez de eliminar:

```css
@media (prefers-reduced-motion: reduce) {
  .card-expand {
    transition-duration: 0.01ms; /* elimina animacao de movimento */
    /* mantem mudanca de opacidade como alternativa */
    opacity: 1;
  }
}
```

## Key Principles

- **Funcional, nao decorativo**: toda animacao deve servir a um proposito de UX.
- **Rapido por padrao**: duracao curta e quase sempre melhor que longa.
- **Consistente**: usar tokens, nunca valores magic number.
- **Respeitoso**: honrar `prefers-reduced-motion` sem degradar a experiencia.
- **Performatico**: animar apenas `transform` e `opacity` para 60fps.
- **Hierarquico**: motion mais pronunciado para mudancas mais importantes.
- **Testavel**: motion deve ser testavel em storybook com controles de playback.

## Examples

### Button Click Feedback

```css
.button {
  transition: transform var(--duration-instant) var(--ease-default),
              box-shadow var(--duration-instant) var(--ease-default);
}
.button:active {
  transform: scale(0.97);
  box-shadow: none;
}
```

### Modal Opening

```css
.modal-overlay {
  animation: fadeIn var(--duration-normal) var(--ease-out);
}
.modal-content {
  animation: slideUp var(--duration-normal) var(--ease-out);
}
```

### Staggered List Entry

```
Item 1: delay 0ms,   duration 300ms, ease-out
Item 2: delay 50ms,  duration 300ms, ease-out
Item 3: delay 100ms, duration 300ms, ease-out
Item 4: delay 150ms, duration 300ms, ease-out
Max stagger: 8 items (400ms total delay). Apos isso, todos entram juntos.
```

## Common Pitfalls

| Erro                               | Consequencia                        | Correcao                                |
| ---------------------------------- | ----------------------------------- | --------------------------------------- |
| Animacoes longas demais            | Interface parece lenta              | Manter duracoes abaixo de 500ms         |
| Ignorar reduced motion             | Desconforto ou nausea em usuarios   | Implementar media query obrigatoriamente|
| Animar width/height/top/left       | Jank e queda de FPS                 | Usar transform e opacity apenas         |
| Motion inconsistente entre telas   | Experiencia fragmentada             | Usar motion tokens do design system     |
| Stagger infinito em listas longas  | Espera frustrante                   | Limitar stagger a 8 itens               |
| Animacao sem proposito funcional   | Distracao e irritacao               | Questionar: "que informacao isso comunica?" |

## Cross-References

- [Dark Mode System](./dark-mode-system.md) — transicoes de tema com motion tokens.
- [Empty States and Loading States](./empty-states-and-loading-states.md) — skeleton shimmer e loading animations.
- [Progressive Disclosure](./progressive-disclosure.md) — animacao de revelacao de conteudo.
- [Accessibility WCAG AA](./accessibility-wcag-aa.md) — WCAG 2.3.3 Animation from Interactions.
- [Design System Governance](./design-system-governance.md) — versionamento de motion tokens.
