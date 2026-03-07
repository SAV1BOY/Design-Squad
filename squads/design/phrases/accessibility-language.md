# Accessibility Language

## Context

Frases prontas para comunicar sobre acessibilidade em diferentes contextos —
desde justificar investimento para stakeholders até especificar requisitos em
tickets. Acessibilidade é frequentemente desprioritizada por falta de argumentos
articulados; esta biblioteca resolve esse gap.

**Aplicação:** Sprint planning, design reviews, tickets, apresentações, reports
**Tom:** Accessibility Champion + Evidence-Driven

## Phrases

### Justificando investimento em a11y
- "Acessibilidade não é feature opcional — é requisito da Lei Brasileira de Inclusão (13.146/2015)."
- "45 milhões de brasileiros têm algum tipo de deficiência. Ignorar a11y é ignorar [X]% do mercado potencial."
- "O custo de corrigir a11y em produção é 3-5x maior que implementar durante o design."
- "Acessibilidade melhora a experiência para todos — captions ajudam em ambientes barulhentos, contraste ajuda sob luz solar."
- "Nosso nível atual de conformidade WCAG AA é [X]%. O target para este quarter é [Y]%."

### Especificando requisitos em tickets
- "Touch target mínimo: 44x44px (WCAG 2.5.8)."
- "Contraste mínimo texto/fundo: 4.5:1 para texto normal, 3:1 para texto grande (WCAG 1.4.3)."
- "Navegação por teclado: todos os elementos interativos acessíveis via Tab, ativação via Enter/Space."
- "Screen reader: anunciar [elemento] como [role] com [label]. Estado [expanded/collapsed] comunicado via aria-expanded."
- "Animação: respeitar prefers-reduced-motion. Duração máxima sem controle do usuário: 5 segundos."

### Feedback em design reviews
- "O contraste de [elemento] é [valor]:1 — abaixo do mínimo WCAG AA de 4.5:1. Alternativa: [cor] com [valor]:1."
- "A focus order não segue a lógica visual. Tab sequence deveria ser: [lista]."
- "O carrossel auto-play não tem controle de pausa — viola WCAG 2.2.2 (Pause, Stop, Hide)."
- "Os ícones sem label de texto precisam de aria-label descritivo."
- "O formulário precisa de error summary no topo além do inline error em cada campo."

### Em sprint planning
- "Adicionar a11y review como step do definition of done custa [N] horas e previne [N] bugs."
- "Os 3 fluxos críticos (login, checkout, cadastro) precisam ser 100% navegáveis por teclado."
- "Proponho reservar [N]% da capacidade do sprint para a11y debt — temos [N] issues abertas."
- "O audit automatizado com axe-core cobre 30-40% dos issues. O resto precisa de review manual."

### Educando o time
- "Deficiência não é binária. Inclui situacional (braço ocupado), temporária (braço engessado) e permanente (amputação)."
- "Acessibilidade não é sobre 'pessoas com deficiência' — é sobre design que funciona em todos os contextos."
- "Testar com screen reader leva 5 minutos por fluxo. VoiceOver (Mac: Cmd+F5) e NVDA (Windows, gratuito)."
- "Cada cor que não passa no contrast check exclui pessoas. Não é estética — é funcionalidade."

### Celebrando progresso
- "O score de a11y do [produto/fluxo] subiu de [X] para [Y] neste quarter."
- "100% dos novos componentes do design system foram lançados com a11y completa."
- "Zero bugs de acessibilidade em produção no último sprint."
- "O tempo de review de a11y caiu de [X] para [Y] horas graças à automação com axe."

## Variations

- Para C-level: focar em risco legal e oportunidade de mercado
- Para desenvolvedores: focar em specs técnicos (ARIA, roles, keyboard events)
- Para designers: focar em impacto visual e interação (contraste, touch targets, focus states)
- Para QA: focar em critérios testáveis e ferramentas de automação

## When to Use

- Sprint planning para incluir requisitos de a11y
- Design reviews para avaliar conformidade
- Tickets de desenvolvimento com specs de a11y
- Apresentações justificando investimento em acessibilidade
- Reports de progresso de conformidade WCAG
- Onboarding de novos membros do time
