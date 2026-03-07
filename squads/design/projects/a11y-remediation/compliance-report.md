# Compliance Report Template

## Informacoes do Relatorio

| Campo | Valor |
|-------|-------|
| **Produto** | [Nome do produto] |
| **Autor** | [Nome] |
| **Data** | [YYYY-MM-DD] |
| **Padrao** | WCAG 2.1 |
| **Nivel Alvo** | AA |
| **Versao do Produto** | [Versao] |

## Resumo Executivo

Este relatorio documenta o nivel de conformidade com WCAG 2.1
do produto [Nome] apos o projeto de remediacao de acessibilidade.

### Status de Conformidade

| Nivel | Criterios | Conformes | Parciais | Nao Conformes | % |
|-------|----------|----------|---------|-------------|---|
| A | [N] | [N] | [N] | [N] | [%] |
| AA | [N] | [N] | [N] | [N] | [%] |
| **Total** | **[N]** | **[N]** | **[N]** | **[N]** | **[%]** |

### Declaracao de Conformidade

```
O produto [Nome], versao [versao], foi avaliado quanto a
conformidade com WCAG 2.1 nivel [AA]. O resultado da avaliacao
indica [conformidade total / conformidade parcial / nao-conformidade]
com o nivel [AA], com [N] criterios totalmente conformes de um
total de [N] criterios aplicaveis.
```

## Escopo da Avaliacao

### Paginas/Fluxos Avaliados

| Pagina/Fluxo | URL | Plataforma | Incluido |
|-------------|-----|-----------|---------|
| [Pagina 1] | [url] | [Web/Mobile] | Sim |
| [Pagina 2] | [url] | [Web/Mobile] | Sim |
| [Pagina 3] | [url] | [Web/Mobile] | Sim |
| [Pagina 4] | [url] | [Web/Mobile] | Sim |
| [Pagina 5] | [url] | [Web/Mobile] | Sim |

### Tecnologias Utilizadas

| Tecnologia | Versao |
|-----------|--------|
| HTML | [5] |
| CSS | [3] |
| JavaScript | [ES2020+] |
| Framework | [React/Vue/Angular — versao] |
| WAI-ARIA | [1.1 / 1.2] |

### Ferramentas de Avaliacao

| Ferramenta | Versao | Tipo |
|-----------|--------|------|
| axe-core | [versao] | Automatizado |
| Lighthouse | [versao] | Automatizado |
| VoiceOver | [versao macOS] | Screen reader |
| NVDA | [versao] | Screen reader |
| Colour Contrast Analyser | [versao] | Manual |

## Conformidade por Principio WCAG

### 1. Perceivable (Perceptivel)

O conteudo deve ser apresentado de maneiras que os usuarios
possam perceber.

| Criterio | Nivel | Status | Observacao |
|----------|-------|--------|-----------|
| 1.1.1 Non-text Content | A | [Conforme/Parcial/Nao conforme] | [obs] |
| 1.2.1 Audio-only/Video-only | A | [Conforme/Parcial/N/A] | [obs] |
| 1.2.2 Captions | A | [Conforme/Parcial/N/A] | [obs] |
| 1.2.3 Audio Description | A | [Conforme/Parcial/N/A] | [obs] |
| 1.2.5 Audio Description (Pre) | AA | [Conforme/Parcial/N/A] | [obs] |
| 1.3.1 Info and Relationships | A | [Conforme/Parcial/Nao conforme] | [obs] |
| 1.3.2 Meaningful Sequence | A | [Conforme/Parcial/Nao conforme] | [obs] |
| 1.3.3 Sensory Characteristics | A | [Conforme/Parcial/Nao conforme] | [obs] |
| 1.3.4 Orientation | AA | [Conforme/Parcial/Nao conforme] | [obs] |
| 1.3.5 Identify Input Purpose | AA | [Conforme/Parcial/Nao conforme] | [obs] |
| 1.4.1 Use of Color | A | [Conforme/Parcial/Nao conforme] | [obs] |
| 1.4.2 Audio Control | A | [Conforme/Parcial/N/A] | [obs] |
| 1.4.3 Contrast (Minimum) | AA | [Conforme/Parcial/Nao conforme] | [obs] |
| 1.4.4 Resize Text | AA | [Conforme/Parcial/Nao conforme] | [obs] |
| 1.4.5 Images of Text | AA | [Conforme/Parcial/Nao conforme] | [obs] |
| 1.4.10 Reflow | AA | [Conforme/Parcial/Nao conforme] | [obs] |
| 1.4.11 Non-text Contrast | AA | [Conforme/Parcial/Nao conforme] | [obs] |
| 1.4.12 Text Spacing | AA | [Conforme/Parcial/Nao conforme] | [obs] |
| 1.4.13 Content on Hover/Focus | AA | [Conforme/Parcial/Nao conforme] | [obs] |

### 2. Operable (Operavel)

Os componentes de interface e navegacao devem ser operaveis.

| Criterio | Nivel | Status | Observacao |
|----------|-------|--------|-----------|
| 2.1.1 Keyboard | A | [Conforme/Parcial/Nao conforme] | [obs] |
| 2.1.2 No Keyboard Trap | A | [Conforme/Parcial/Nao conforme] | [obs] |
| 2.1.4 Character Key Shortcuts | A | [Conforme/Parcial/N/A] | [obs] |
| 2.2.1 Timing Adjustable | A | [Conforme/Parcial/N/A] | [obs] |
| 2.2.2 Pause, Stop, Hide | A | [Conforme/Parcial/N/A] | [obs] |
| 2.3.1 Three Flashes | A | [Conforme/Parcial/N/A] | [obs] |
| 2.4.1 Bypass Blocks | A | [Conforme/Parcial/Nao conforme] | [obs] |
| 2.4.2 Page Titled | A | [Conforme/Parcial/Nao conforme] | [obs] |
| 2.4.3 Focus Order | A | [Conforme/Parcial/Nao conforme] | [obs] |
| 2.4.4 Link Purpose | A | [Conforme/Parcial/Nao conforme] | [obs] |
| 2.4.5 Multiple Ways | AA | [Conforme/Parcial/Nao conforme] | [obs] |
| 2.4.6 Headings and Labels | AA | [Conforme/Parcial/Nao conforme] | [obs] |
| 2.4.7 Focus Visible | AA | [Conforme/Parcial/Nao conforme] | [obs] |
| 2.5.1 Pointer Gestures | A | [Conforme/Parcial/N/A] | [obs] |
| 2.5.2 Pointer Cancellation | A | [Conforme/Parcial/Nao conforme] | [obs] |

---
