# Accessibility WCAG AA

## Metadata

| Campo         | Valor                                         |
| ------------- | --------------------------------------------- |
| Categoria     | Acessibilidade                                |
| Complexidade  | Alta                                          |
| Autor         | Design Squad                                  |
| Versao        | 1.0                                           |
| Ultima revisao| 2026-03-06                                    |
| Tags          | accessibility, wcag, a11y, perceivable, operable |

## Concept

WCAG (Web Content Accessibility Guidelines) AA e o nivel de conformidade alvo para a maioria dos
produtos digitais. Organizado em quatro principios — POUR — que garantem que o conteudo seja
acessivel ao maior numero possivel de pessoas, incluindo aquelas com deficiencias visuais,
auditivas, motoras e cognitivas.

### Os Quatro Principios (POUR)

1. **Perceivable** — Informacao e componentes de UI devem ser apresentaveis de formas que os
   usuarios possam perceber.
2. **Operable** — Componentes de UI e navegacao devem ser operaveis por todos.
3. **Understandable** — Informacao e operacao da UI devem ser compreensiveis.
4. **Robust** — Conteudo deve ser robusto o suficiente para ser interpretado por tecnologias
   assistivas, incluindo screen readers.

### Criterios Chave por Principio

**Perceivable:**
- 1.1.1 Non-text Content: todo conteudo nao-textual tem alternativa textual.
- 1.3.1 Info and Relationships: estrutura semantica conveyed programmatically.
- 1.4.3 Contrast (Minimum): 4.5:1 texto normal, 3:1 texto grande.
- 1.4.11 Non-text Contrast: 3:1 para componentes UI e graficos.

**Operable:**
- 2.1.1 Keyboard: toda funcionalidade acessivel via teclado.
- 2.4.3 Focus Order: ordem de foco logica e previsivel.
- 2.4.7 Focus Visible: indicador de foco visivel em todos os elementos interativos.
- 2.5.5 Target Size: area de toque minimo 44x44 CSS pixels.

**Understandable:**
- 3.1.1 Language of Page: idioma definido no atributo `lang`.
- 3.2.1 On Focus: foco nao causa mudanca inesperada de contexto.
- 3.3.1 Error Identification: erros identificados e descritos ao usuario.
- 3.3.2 Labels or Instructions: inputs tem labels descritivos.

**Robust:**
- 4.1.2 Name, Role, Value: todos os componentes tem name e role acessiveis.
- 4.1.3 Status Messages: mensagens de status anunciadas sem mover foco.

## When to Use

- Em todo produto digital — acessibilidade nao e opcional.
- Desde o inicio do projeto, nao como remediacao posterior.
- Em cada componente do design system.
- Em todo review de design e code review.
- Quando atendendo requisitos legais (Lei Brasileira de Inclusao, ADA, EAA).

## How to Apply

### No Design

1. **Contraste**: verificar todos os pares de cor com ferramentas automatizadas.
2. **Hierarquia semantica**: definir heading levels (h1-h6) no wireframe.
3. **Focus states**: projetar focus ring visivel (minimo 2px, contraste 3:1).
4. **Touch targets**: garantir minimo 44x44px para elementos interativos.
5. **Alternativas textuais**: escrever alt text para imagens no design.
6. **Ordem de leitura**: anotar a reading order no layout.

### No Desenvolvimento

1. **HTML semantico**: usar elementos corretos (`button`, `nav`, `main`, `header`).
2. **ARIA quando necessario**: `aria-label`, `aria-describedby`, `aria-live`, `role`.
3. **Keyboard navigation**: garantir tab order logica, skip links, focus trap em modais.
4. **Screen reader testing**: testar com VoiceOver, NVDA ou JAWS regularmente.
5. **Automated testing**: integrar axe-core ou pa11y no CI/CD.
6. **Manual testing**: checklist de acessibilidade em cada sprint.

### No QA

1. **Tab through**: navegar toda a pagina usando apenas teclado.
2. **Screen reader walkthrough**: ouvir a pagina inteira com screen reader.
3. **Zoom 200%**: verificar que conteudo nao quebra em zoom ate 200%.
4. **High contrast mode**: testar em Windows High Contrast Mode.
5. **Color blindness simulation**: verificar com Sim Daltonism ou similar.

## Key Principles

- **Acessibilidade e design, nao remediacacao**: incorporar desde o primeiro wireframe.
- **Nada sobre nos sem nos**: envolver pessoas com deficiencia em pesquisa e testes.
- **Semantica antes de ARIA**: HTML semantico correto resolve 80% dos problemas.
- **Progressivo**: nao esperar perfeicao — melhorar iterativamente.
- **Automatizar o que for possivel**: CI checks para contraste, alt text, labels.
- **Documentar decisoes**: registrar decisoes de acessibilidade no design system.

## Examples

### Focus Management em Modal

```html
<!-- Ao abrir modal: mover foco para o primeiro elemento focavel -->
<!-- Implementar focus trap: Tab e Shift+Tab cicam dentro do modal -->
<!-- Ao fechar: retornar foco ao elemento que abriu o modal -->
<div role="dialog" aria-modal="true" aria-labelledby="modal-title">
  <h2 id="modal-title">Confirmar exclusao</h2>
  <p>Esta acao nao pode ser desfeita.</p>
  <button>Cancelar</button>
  <button>Excluir</button>
</div>
```

### Live Region para Notificacoes

```html
<div aria-live="polite" aria-atomic="true" class="sr-only">
  <!-- Conteudo injetado dinamicamente sera anunciado pelo screen reader -->
</div>
```

### Formulario Acessivel

```html
<label for="email">Email</label>
<input id="email" type="email" aria-describedby="email-hint email-error"
       aria-invalid="true" required />
<span id="email-hint">Use seu email corporativo</span>
<span id="email-error" role="alert">Formato de email invalido</span>
```

## Common Pitfalls

| Erro                                | Consequencia                        | Correcao                                |
| ----------------------------------- | ----------------------------------- | --------------------------------------- |
| div com onClick em vez de button    | Nao focavel, sem keyboard support   | Usar elementos semanticos nativos       |
| Placeholder como unico label       | Label desaparece ao digitar         | Usar label visivel + placeholder        |
| Cor como unico indicador           | Daltonicos nao percebem o estado    | Combinar cor + icone + texto            |
| Focus outline removido com CSS     | Usuarios de teclado sem orientacao  | Customizar, nunca remover outline       |
| Imagens sem alt text               | Conteudo invisivel para screen readers| Escrever alt descritivo ou alt=""       |
| ARIA overuse                       | Confusao no screen reader           | Usar ARIA apenas quando HTML nao basta  |

## Cross-References

- [Dark Mode System](./dark-mode-system.md) — contraste em ambos os temas.
- [Motion Design System](./motion-design-system.md) — prefers-reduced-motion.
- [Error Prevention and Recovery](./error-prevention-and-recovery.md) — erros acessiveis.
- [Responsive Design System](./responsive-design-system.md) — touch targets e reflow.
- [Content Design Microcopy](./content-design-microcopy.md) — linguagem clara e inclusiva.
