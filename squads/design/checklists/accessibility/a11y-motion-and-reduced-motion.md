# A11Y Motion and Reduced Motion

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Accessibility                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Accessibility Lead             |

## Objective

Verificar se animacoes e transicoes respeitam as preferencias do usuario por movimento
reduzido, prevenindo desconforto, nausea ou risco de convulsoes em usuarios com
vestibular disorders ou fotossensibilidade. Design de motion responsavel equilibra
experiencia visual rica com acessibilidade.

## When to Apply

- Ao projetar animacoes, transicoes ou micro-interacoes.
- Em auditorias de acessibilidade focadas em motion.
- Quando usuarios reportam desconforto com animacoes.
- Ao definir motion guidelines do design system.

## Criteria

- [ ] prefers-reduced-motion media query e respeitada em todas as animacoes.
- [ ] Animacoes essenciais (loading, progress) possuem alternativa sem motion.
- [ ] Nenhuma animacao pisca mais de 3 vezes por segundo (risco de convulsao).
- [ ] Parallax scrolling possui alternativa estatica para reduced motion.
- [ ] Auto-playing animations possuem controle de pause/stop acessivel.
- [ ] Videos com autoplay podem ser pausados e nao reiniciam automaticamente.
- [ ] Transicoes de tela usam fade ou corte simples quando reduced motion esta ativo.
- [ ] Animacoes de scroll (scroll-triggered) sao desabilitadas em reduced motion.
- [ ] Background animations (particulas, gradientes animados) respeitam a preferencia.
- [ ] Duracoes de animacao sao razoaveis (200-500ms para micro-interacoes).
- [ ] Existe documentacao de motion guidelines com principios e restricoes.
- [ ] Testes de animacao sao realizados com reduced motion habilitado no OS.
- [ ] Carousel e slider possuem controles manuais e pausa automatica.
- [ ] Motion e utilizado com proposito (feedback, orientacao, transicao), nao decorativamente.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Animacao com mais de 3 flashes/s ou prefers-reduced-motion ignorada.     |
| Major    | Auto-play sem controle de pausa ou parallax sem alternativa.              |
| Minor    | Duracoes excessivas ou animacoes puramente decorativas sem desabilitacao.  |
| Info     | Oportunidade de enriquecer motion guidelines ou adicionar alternativas.   |

## Cross-References

- `accessibility/a11y-wcag-audit.md` — Auditoria WCAG (criterio 2.3.1).
- `ui/ui-states-and-feedback.md` — Estados e feedback visual.
- `design-system/ds-token-architecture.md` — Tokens de motion.
- `frost/frost-frontend-style-guide-audit.md` — Style guide de frontend.
