# Pattern Taxonomy

## Purpose

Taxonomia de padroes de UX organizados por contexto de uso. Diferente de componentes (blocos de construcao), padroes sao solucoes recorrentes para problemas de design.

## Taxonomy Tree

### 1. Data Entry Patterns
```
data-entry/
├── form-validation
│   ├── inline-validation
│   ├── on-submit-validation
│   └── real-time-validation
├── multi-step-form
├── inline-editing
├── auto-save
├── address-autocomplete
└── file-upload-flow
```

### 2. Navigation Patterns
```
navigation/
├── global-navigation
├── local-navigation
├── contextual-navigation
├── wizard / stepper
├── search-and-filter
├── deep-linking
└── back-navigation
```

### 3. Content Patterns
```
content/
├── empty-states
├── loading-states
├── error-states
├── infinite-scroll
├── pagination
├── content-preview
├── expandable-content
└── master-detail
```

### 4. Communication Patterns
```
communication/
├── notifications
│   ├── push
│   ├── in-app
│   └── email-digest
├── confirmation
│   ├── modal-confirmation
│   ├── undo
│   └── inline-confirmation
├── onboarding
│   ├── welcome-tour
│   ├── progressive-profiling
│   └── contextual-tips
└── feedback
    ├── success-feedback
    ├── error-feedback
    └── progress-feedback
```

### 5. Data Management Patterns
```
data-management/
├── crud-operations
├── bulk-actions
├── sort-and-filter
├── search
│   ├── basic-search
│   ├── faceted-search
│   └── command-palette
├── export
└── import
```

### 6. Layout Patterns
```
layout/
├── responsive-adaptation
├── dashboard-layout
├── settings-layout
├── list-detail (master-detail)
├── modal-workflow
└── split-view
```

## Pattern vs Component

```
Aspecto      | Componente              | Padrao
-------------|-------------------------|---------------------------
Nivel        | Elemento de UI          | Solucao de UX
Escopo       | Unico elemento          | Fluxo ou comportamento
Exemplo      | Button, Input           | Form validation, Onboarding
Reutilizacao | Identico em cada uso    | Adaptado ao contexto
```

## Usage Notes

- Padroes podem usar multiplos componentes
- Documente quando usar cada padrao e suas variacoes
- Referencie padroes em specs de design para consistencia
- Revise com base em dados de usabilidade
