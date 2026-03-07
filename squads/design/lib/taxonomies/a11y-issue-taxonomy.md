# Accessibility Issue Taxonomy

## Purpose

Taxonomia de problemas de acessibilidade organizados por principio WCAG, severidade e impacto. Usada para classificar, priorizar e rastrear issues de a11y.

## WCAG Principle Categories

### 1. Perceivable Issues
```
perceivable/
├── color-contrast
│   ├── text-contrast-below-aa (4.5:1)
│   ├── large-text-contrast-below-aa (3:1)
│   └── ui-component-contrast-below-aa (3:1)
├── text-alternatives
│   ├── missing-alt-text
│   ├── decorative-image-not-hidden
│   ├── complex-image-missing-long-desc
│   └── icon-button-missing-label
├── multimedia
│   ├── video-missing-captions
│   ├── audio-missing-transcript
│   └── auto-playing-media
├── adaptability
│   ├── content-not-reflow-at-200-zoom
│   ├── text-spacing-broken
│   └── orientation-locked
└── distinguishable
    ├── info-conveyed-by-color-only
    ├── audio-control-missing
    └── text-over-image-unreadable
```

### 2. Operable Issues
```
operable/
├── keyboard
│   ├── element-not-keyboard-accessible
│   ├── keyboard-trap
│   ├── focus-not-visible
│   ├── focus-order-illogical
│   └── missing-skip-link
├── timing
│   ├── timeout-without-warning
│   ├── no-pause-for-auto-content
│   └── session-timeout-too-short
├── seizures
│   ├── flashing-content (> 3 per second)
│   └── animation-without-reduced-motion
├── navigation
│   ├── inconsistent-navigation
│   ├── page-title-missing-or-generic
│   ├── link-purpose-unclear
│   └── multiple-ways-missing
└── input-modalities
    ├── target-size-too-small (< 24x24)
    ├── drag-without-alternative
    └── motion-activation-without-alternative
```

### 3. Understandable Issues
```
understandable/
├── readable
│   ├── language-not-specified
│   ├── language-of-parts-missing
│   └── jargon-without-definition
├── predictable
│   ├── unexpected-context-change-on-focus
│   ├── unexpected-context-change-on-input
│   └── inconsistent-labeling
└── input-assistance
    ├── error-not-identified
    ├── label-missing
    ├── error-suggestion-missing
    └── error-prevention-missing
```

### 4. Robust Issues
```
robust/
├── parsing
│   ├── duplicate-ids
│   ├── invalid-html
│   └── incomplete-start-end-tags
├── name-role-value
│   ├── missing-aria-role
│   ├── incorrect-aria-role
│   ├── aria-state-not-updated
│   └── custom-widget-missing-semantics
└── status-messages
    ├── dynamic-content-not-announced
    └── status-missing-aria-live
```

## Severity Classification

```
Severity   | Descricao                                    | SLA
-----------|----------------------------------------------|----------
Critical   | Bloqueia acesso completo para algum grupo    | 1 sprint
High       | Dificulta significativamente o uso           | 2 sprints
Medium     | Causa inconveniencia mas tem workaround      | 3 sprints
Low        | Melhoria de experiencia, nao bloqueia acesso | Backlog
```

## Impact Groups

```
Grupo                  | Issues que mais afetam
-----------------------|----------------------------------
Cegos (screen reader)  | Alt text, ARIA, semantics, focus
Baixa visao            | Contraste, zoom, text spacing
Motores               | Keyboard, target size, drag
Cognitivos            | Linguagem, consistencia, erros
Surdos                | Captions, transcripts
Vestibulares          | Motion, flashing, parallax
```

## Usage Notes

- Classifique cada issue encontrada usando esta taxonomia
- Use severity para priorizar o backlog de a11y
- Rastreie issues no accessibility-issues-registry.yaml
- Re-teste apos correcao para confirmar resolucao
- Inclua o grupo de impacto para comunicar urgencia ao time
