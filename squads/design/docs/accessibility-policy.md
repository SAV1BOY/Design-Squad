# Accessibility Policy

## Overview

Política de acessibilidade do Design Squad — define o nível de conformidade target,
responsabilidades, processos de verificação e roadmap de evolução. Acessibilidade
é requisito fundamental, não feature opcional.

## Content

### Conformance Target

**Nível atual:** WCAG 2.2 AA parcial — [X]% de conformidade
**Target Q2 2026:** 80% de conformidade WCAG 2.2 AA
**Target Q4 2026:** 95% de conformidade WCAG 2.2 AA
**Long-term:** WCAG 2.2 AA completo + items selecionados de AAA

### Marco Legal

- **Lei Brasileira de Inclusão (13.146/2015):** Art. 63 — acessibilidade em
  sites e aplicativos de empresas com sede no Brasil é obrigação legal.
- **Decreto 5.296/2004:** Regulamenta acessibilidade digital em serviços públicos.
- **eMAG (Modelo de Acessibilidade em Governo Eletrônico):** Referência complementar
  para padrões brasileiros.

### Responsabilidades

| Papel | Responsabilidade de A11y |
|-------|--------------------------|
| Product Designer | Cores com contraste adequado, touch targets, focus states, estados completos |
| UX Writer | Microcopy clara, alt text, labels descritivos, linguagem simples |
| UX Researcher | Incluir PcD em pesquisas, testes com tecnologias assistivas |
| DS Engineer | Componentes com ARIA correto, keyboard nav, focus management |
| Front-end Dev | Implementar specs de a11y, testar com screen reader |
| QA | Testar a11y com checklist, rodar axe-core, reportar findings |
| Design Lead | Priorizar a11y no roadmap, garantir resources |

### Checklist por Fase

#### Design
- [ ] Contraste de texto: 4.5:1 (normal) / 3:1 (grande) — WCAG 1.4.3
- [ ] Contraste de UI: 3:1 para elementos interativos — WCAG 1.4.11
- [ ] Touch targets: mínimo 44x44px — WCAG 2.5.8
- [ ] Focus states visíveis para todos os elementos interativos
- [ ] Hierarquia de headings lógica (H1 > H2 > H3)
- [ ] Informação não depende apenas de cor
- [ ] Alt text definido para imagens informativas
- [ ] Animações com opção de redução ou prefers-reduced-motion

#### Handoff
- [ ] ARIA roles e labels especificados
- [ ] Tab order definido
- [ ] Keyboard interactions especificadas por componente
- [ ] Screen reader announcements definidos para estados dinâmicos
- [ ] Error handling com aria-live para mensagens

#### QA
- [ ] axe-core scan com 0 violations de severity "critical" e "serious"
- [ ] Navegação completa por teclado (Tab, Enter, Space, Escape, Arrows)
- [ ] VoiceOver (macOS/iOS) ou NVDA (Windows) walkthrough
- [ ] Zoom a 200% sem perda de funcionalidade
- [ ] prefers-reduced-motion respeitado
- [ ] Testes em alto contraste do sistema

### Processo de Audit

**Frequência:** Trimestral para produto completo, por feature em cada sprint

**Ferramentas:**
- axe DevTools (automação — cobre ~40% dos issues)
- Stark Figma Plugin (design time — contraste e simulação)
- Pa11y CI (automação em pipeline)
- Manual testing com screen reader (cobre issues de contexto e semântica)

**Escala de severidade:**
- **Crítico:** Bloqueio completo — usuário não consegue completar tarefa
- **Sério:** Barreira significativa — workaround possível mas difícil
- **Moderado:** Inconveniente — funciona mas com dificuldade extra
- **Menor:** Não conforme com WCAG mas impacto baixo no uso

### Roadmap de A11y

| Quarter | Foco | Target |
|---------|------|--------|
| Q1 2026 | Audit baseline + fix de críticos | 70% compliance |
| Q2 2026 | Navegação por teclado + focus management | 80% compliance |
| Q3 2026 | Forms + error handling acessível | 90% compliance |
| Q4 2026 | Polish + AAA items selecionados | 95% compliance |

## Cross-References

- `phrases/accessibility-language.md` — Frases para comunicar sobre a11y
- `voice/tone-profiles/accessibility-champion.md` — Tom de voz para a11y
- `scripts/a11y/run-axe-audit.md` — Script de audit automatizado
- `scripts/a11y/contrast-scan.md` — Verificação de contraste
- `scripts/a11y/focus-order-validator.md` — Validação de focus order
