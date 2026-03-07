# Animation Tokens Map

## Purpose

Mapa de tokens de animacao para motion design consistente. Define duracoes, easing curves, propriedades animaveis e padroes de transicao padronizados.

## Duration Tokens

```
Token                  | Value  | Uso
-----------------------|--------|------------------------------------------
--duration-instant     | 0ms    | Sem animacao (reduced motion)
--duration-fast        | 100ms  | Micro-interactions (hover, focus)
--duration-normal      | 200ms  | Transicoes de estado (expand, color)
--duration-slow        | 300ms  | Transicoes de layout (slide, fade)
--duration-slower      | 500ms  | Animacoes complexas (page transitions)
--duration-slowest     | 800ms  | Animacoes de entrada dramaticas
```

## Easing Tokens

```
Token                    | Value                        | Uso
-------------------------|------------------------------|----------------------------
--ease-default           | cubic-bezier(0.25, 0.1, 0.25, 1) | Padrao para maioria
--ease-in                | cubic-bezier(0.42, 0, 1, 1)      | Elementos saindo da tela
--ease-out               | cubic-bezier(0, 0, 0.58, 1)      | Elementos entrando na tela
--ease-in-out            | cubic-bezier(0.42, 0, 0.58, 1)   | Transicoes bidirecionais
--ease-spring            | cubic-bezier(0.34, 1.56, 0.64, 1)| Bounce sutil (delight)
--ease-linear            | linear                            | Progress bars, timers
```

## Common Transition Patterns

```css
/* Hover state */
.button {
  transition: background-color var(--duration-fast) var(--ease-default),
              box-shadow var(--duration-fast) var(--ease-default);
}

/* Expand/collapse */
.accordion-content {
  transition: height var(--duration-normal) var(--ease-out),
              opacity var(--duration-normal) var(--ease-out);
}

/* Slide in */
.drawer {
  transition: transform var(--duration-slow) var(--ease-out);
}

/* Fade */
.toast {
  transition: opacity var(--duration-normal) var(--ease-in-out),
              transform var(--duration-normal) var(--ease-out);
}
```

## Animation Patterns

```css
/* Skeleton pulse */
@keyframes skeleton-pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.4; }
}
.skeleton { animation: skeleton-pulse 1.5s var(--ease-in-out) infinite; }

/* Spin (loading) */
@keyframes spin {
  to { transform: rotate(360deg); }
}
.spinner { animation: spin 0.8s var(--ease-linear) infinite; }

/* Entrance */
@keyframes fade-in-up {
  from { opacity: 0; transform: translateY(8px); }
  to { opacity: 1; transform: translateY(0); }
}
.card-enter { animation: fade-in-up var(--duration-slow) var(--ease-out); }
```

## Reduced Motion

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: var(--duration-instant) !important;
    transition-duration: var(--duration-instant) !important;
  }
}
```

## Principles

- Motion deve ter proposito: guiar atencao, dar feedback, mostrar relacao
- Menos e mais — animacoes excessivas causam fadiga
- Sempre respeite `prefers-reduced-motion`
- Elementos maiores devem ter duracao maior
- Stagger animations para listas (delay incremental de 50ms por item)

## Usage Notes

- Use `will-change` com moderacao para performance
- Anime apenas `transform` e `opacity` para 60fps
- Evite animar `width`, `height`, `top`, `left` — prefira `transform`
- Teste em dispositivos de baixa performance
