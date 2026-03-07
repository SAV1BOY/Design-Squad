# Motion Spec Template

## Metadata

| Campo                | Valor                                           |
|----------------------|--------------------------------------------------|
| **Feature / Componente** | [PREENCHER — nome da feature ou componente]  |
| **Designer**         | [PREENCHER — motion/UI designer responsavel]     |
| **Data de criacao**  | [PREENCHER — YYYY-MM-DD]                         |
| **Versao**           | [PREENCHER — v1.0]                               |
| **Plataforma**       | [PREENCHER — Web / iOS / Android / Todas]        |
| **Status**           | [PREENCHER — Draft / Aprovado / Implementado]    |
| **Prototipo link**   | [PREENCHER — link video/prototipo interativo]    |

## Instructions (Como Usar)

1. Documente todas as animacoes e transicoes planejadas para a feature.
2. Inclua videos ou prototipos interativos como referencia visual.
3. Especifique valores exatos de duracao, easing e propriedades animadas.
4. Considere acessibilidade (prefers-reduced-motion) para cada animacao.
5. Revise com eng para validar viabilidade de implementacao.

> **Dica:** Animacoes devem servir a um proposito (feedback, orientacao, continuidade). Se nao tem proposito claro, nao anime.

## Template

### 1. Principios de Motion do Produto

| # | Principio                                          |
|---|-----------------------------------------------------|
| 1 | [PREENCHER — ex.: Funcional primeiro, decorativo depois] |
| 2 | [PREENCHER — ex.: Rapido e responsivo — nao atrasar o usuario] |
| 3 | [PREENCHER — ex.: Consistente entre plataformas] |
| 4 | [PREENCHER — ex.: Respeitar prefers-reduced-motion] |

### 2. Easing Tokens

| Token name        | Valor CSS / Cubic-bezier         | Uso                           |
|-------------------|----------------------------------|-------------------------------|
| ease-standard     | [PREENCHER — cubic-bezier()]     | [PREENCHER — interacoes gerais] |
| ease-enter        | [PREENCHER — cubic-bezier()]     | [PREENCHER — elementos entrando] |
| ease-exit         | [PREENCHER — cubic-bezier()]     | [PREENCHER — elementos saindo] |
| ease-emphasized   | [PREENCHER — cubic-bezier()]     | [PREENCHER — transicoes de destaque] |
| linear            | linear                           | [PREENCHER — progress bars, spinners] |

### 3. Duration Tokens

| Token name      | Valor     | Uso                                    |
|-----------------|-----------|----------------------------------------|
| duration-xs     | [PREENCHER — ex.: 100ms] | [PREENCHER — hover states, toggles] |
| duration-sm     | [PREENCHER — ex.: 200ms] | [PREENCHER — tooltips, small transitions] |
| duration-md     | [PREENCHER — ex.: 300ms] | [PREENCHER — page transitions, modals] |
| duration-lg     | [PREENCHER — ex.: 400ms] | [PREENCHER — complex transitions] |
| duration-xl     | [PREENCHER — ex.: 500ms] | [PREENCHER — page-level animations] |

### 4. Animacoes Detalhadas

#### Animacao 1: [PREENCHER — nome descritivo]

| Aspecto              | Valor                                          |
|----------------------|------------------------------------------------|
| **Trigger**          | [PREENCHER — o que dispara a animacao]         |
| **Elemento(s)**      | [PREENCHER — o que e animado]                  |
| **Proposito**        | [PREENCHER — por que esta animacao existe]     |
| **Propriedades**     | [PREENCHER — opacity, transform, etc.]         |
| **Estado inicial**   | [PREENCHER — valores iniciais]                 |
| **Estado final**     | [PREENCHER — valores finais]                   |
| **Duracao**          | [PREENCHER — token ou ms]                      |
| **Easing**           | [PREENCHER — token ou cubic-bezier]            |
| **Delay**            | [PREENCHER — ms, se aplicavel]                 |
| **Reduced-motion**   | [PREENCHER — alternativa sem animacao]         |

**Referencia visual:** [PREENCHER — link video/gif/prototipo]

---

#### Animacao 2: [PREENCHER — nome]

| Aspecto              | Valor                                          |
|----------------------|------------------------------------------------|
| **Trigger**          | [PREENCHER]                                    |
| **Elemento(s)**      | [PREENCHER]                                    |
| **Proposito**        | [PREENCHER]                                    |
| **Propriedades**     | [PREENCHER]                                    |
| **Estado inicial**   | [PREENCHER]                                    |
| **Estado final**     | [PREENCHER]                                    |
| **Duracao**          | [PREENCHER]                                    |
| **Easing**           | [PREENCHER]                                    |
| **Delay**            | [PREENCHER]                                    |
| **Reduced-motion**   | [PREENCHER]                                    |

---

#### Animacao 3: [PREENCHER — nome]

| Aspecto              | Valor                                          |
|----------------------|------------------------------------------------|
| **Trigger**          | [PREENCHER]                                    |
| **Elemento(s)**      | [PREENCHER]                                    |
| **Proposito**        | [PREENCHER]                                    |
| **Propriedades**     | [PREENCHER]                                    |
| **Estado inicial**   | [PREENCHER]                                    |
| **Estado final**     | [PREENCHER]                                    |
| **Duracao**          | [PREENCHER]                                    |
| **Easing**           | [PREENCHER]                                    |
| **Reduced-motion**   | [PREENCHER]                                    |

### 5. Transicoes de Pagina / Tela

| De (tela)        | Para (tela)       | Tipo                    | Duracao     | Detalhes              |
|------------------|-------------------|-------------------------|-------------|-----------------------|
| [PREENCHER]      | [PREENCHER]       | [PREENCHER — push/fade/slide] | [PREENCHER] | [PREENCHER]      |
| [PREENCHER]      | [PREENCHER]       | [PREENCHER]             | [PREENCHER] | [PREENCHER]           |

### 6. Micro-interacoes

| Elemento        | Trigger        | Animacao                          | Duracao     | Easing       |
|-----------------|----------------|-----------------------------------|-------------|--------------|
| Button hover    | mouseenter     | [PREENCHER — background-color]    | [PREENCHER] | [PREENCHER]  |
| Button press    | mousedown      | [PREENCHER — scale(0.98)]         | [PREENCHER] | [PREENCHER]  |
| Toggle switch   | click          | [PREENCHER — translateX + bg]     | [PREENCHER] | [PREENCHER]  |
| [PREENCHER]     | [PREENCHER]    | [PREENCHER]                       | [PREENCHER] | [PREENCHER]  |
| [PREENCHER]     | [PREENCHER]    | [PREENCHER]                       | [PREENCHER] | [PREENCHER]  |

### 7. Loading e Skeleton Animations

| Tipo            | Elemento                  | Animacao                      | Duracao / Loop |
|-----------------|---------------------------|-------------------------------|----------------|
| Skeleton        | [PREENCHER — cards/text]  | [PREENCHER — shimmer/pulse]   | [PREENCHER]    |
| Spinner         | [PREENCHER — onde aparece] | [PREENCHER — rotate]         | [PREENCHER]    |
| Progress bar    | [PREENCHER]               | [PREENCHER — width + ease]    | [PREENCHER]    |

### 8. Staggered Animations (Sequenciais)

| Grupo de elementos     | Delay entre itens | Propriedade animada  | Duracao individual |
|------------------------|--------------------|----------------------|--------------------|
| [PREENCHER — ex.: list items] | [PREENCHER — ex.: 50ms] | [PREENCHER — opacity + translateY] | [PREENCHER] |
| [PREENCHER]            | [PREENCHER]        | [PREENCHER]          | [PREENCHER]        |

### 9. Acessibilidade (prefers-reduced-motion)

**Estrategia geral:** [PREENCHER — remove all motion / reduce to opacity-only / instant transitions]

| Animacao original              | Alternativa reduced-motion           |
|--------------------------------|--------------------------------------|
| [PREENCHER — slide + fade]     | [PREENCHER — fade only / instant]    |
| [PREENCHER — scale bounce]     | [PREENCHER — opacity / instant]      |
| [PREENCHER — stagger list]     | [PREENCHER — all items appear at once] |

### 10. Implementacao

**Tecnologia recomendada:**
- CSS Transitions: [PREENCHER — quais animacoes]
- CSS Animations: [PREENCHER — quais animacoes]
- JS (Framer Motion / GSAP / Web Animations API): [PREENCHER — quais]
- Lottie: [PREENCHER — quais, se aplicavel]

**Performance:**
- [ ] Apenas propriedades composited (transform, opacity) animadas
- [ ] Nao anima layout properties (width, height, top, left)
- [ ] will-change aplicado seletivamente
- [ ] Testado a 60fps em dispositivos de referencia

## Example (Parcialmente Preenchido)

**Animacao: Modal Open**
- Trigger: Click em botao "Abrir"
- Overlay: opacity 0->0.5, duracao 200ms, ease-enter
- Modal container: opacity 0->1, translateY(16px)->0, duracao 300ms, ease-enter
- Reduced-motion: Apenas opacity, sem translateY, duracao 150ms

## Notes

- Animacoes acima de 300ms para interacoes diretas parecem lentas — seja breve.
- Sempre implemente prefers-reduced-motion — e um requisito de acessibilidade.
- Teste performance em dispositivos de baixo desempenho, nao apenas no seu Mac.
- Evite animar propriedades que causam reflow (width, height, padding, margin).
- Videos de referencia sao essenciais — texto sozinho nao comunica motion adequadamente.
