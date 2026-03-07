# Interaction Taxonomy

## Purpose

Taxonomia de tipos de interacao em interfaces digitais. Classifica como usuarios interagem com elementos, incluindo gestos, estados e padroes de feedback.

## Interaction Types

### 1. Click / Tap Interactions
```
click/
├── single-click
│   ├── primary-action (button click)
│   ├── selection (checkbox, radio)
│   ├── toggle (switch, expand/collapse)
│   └── navigation (link, menu item)
├── double-click
│   └── inline-edit activation
├── long-press
│   ├── context-menu (mobile)
│   └── drag-initiation
└── right-click
    └── context-menu (desktop)
```

### 2. Pointer Interactions
```
pointer/
├── hover
│   ├── tooltip-reveal
│   ├── preview (card hover)
│   └── action-reveal (row actions)
├── drag-and-drop
│   ├── reorder (list items)
│   ├── move (kanban cards)
│   ├── upload (file drop zone)
│   └── resize (panels, columns)
└── cursor-feedback
    ├── pointer (clickable)
    ├── grab/grabbing (draggable)
    ├── not-allowed (disabled)
    └── resize (resizable borders)
```

### 3. Keyboard Interactions
```
keyboard/
├── tab-navigation
│   ├── sequential (Tab/Shift+Tab)
│   └── skip-links
├── arrow-navigation
│   ├── menu items (Up/Down)
│   ├── tabs (Left/Right)
│   └── grid cells (all directions)
├── activation
│   ├── enter (links, buttons)
│   └── space (buttons, checkboxes)
├── dismissal
│   └── escape (modals, popovers)
└── shortcuts
    ├── global (Cmd+K search)
    └── contextual (Cmd+S save)
```

### 4. Touch Gestures (Mobile)
```
touch/
├── tap (equivalent to click)
├── swipe
│   ├── horizontal (dismiss, reveal actions)
│   ├── vertical (scroll, pull-to-refresh)
│   └── directional-nav (carousel, onboarding)
├── pinch
│   ├── zoom-in
│   └── zoom-out
├── pan
│   └── map/canvas navigation
└── multi-touch
    └── rotate (images, canvas)
```

### 5. Voice / Input Interactions
```
voice/
├── voice-command
├── dictation
└── voice-search
```

## Interaction States

```
State       | Visual Cue                  | Trigger
------------|-----------------------------|-----------------------
Default     | Aparencia base              | Nenhum
Hover       | Mudanca sutil de cor/shadow | Mouse over
Focus       | Focus ring (outline)        | Tab / click
Active      | Pressed appearance          | Mouse down / touch
Selected    | Checked/highlighted         | Click + state change
Disabled    | Opacity reduzida            | Condicional
Loading     | Spinner / skeleton          | Async operation
Dragging    | Elevated + cursor change    | Drag start
```

## Feedback Types

```
Tipo        | Exemplo                     | Timing
------------|-----------------------------|-----------------------
Visual      | Color change, animation     | Imediato (< 100ms)
Haptic      | Vibration (mobile)          | Imediato
Audio       | Click sound, notification   | Imediato
Progress    | Bar, spinner, percentage    | Ongoing
Confirmation| Toast, modal               | After completion
```

## Usage Notes

- Toda interacao deve ter feedback visual imediato
- Touch targets: minimo 44x44px, com 8px de espacamento entre alvos
- Keyboard deve poder replicar todas as acoes do mouse
- Gestos mobile devem ter alternativa de botao visivel
- Documente shortcuts em menu acessivel ao usuario
