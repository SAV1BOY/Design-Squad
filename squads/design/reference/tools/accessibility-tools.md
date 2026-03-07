# Accessibility Tools



## Metadata

- **Categoria:** Accessibility Testing, Inclusive Design
- **Relevancia para o Squad:** Alta — ferramentas para garantir acessibilidade
- **Ultima revisao:** 2026-03-06



## Summary

Ferramentas de acessibilidade permitem que o squad verifique, teste e melhore a acessibilidade de interfaces em diferentes etapas do processo — desde design no Figma ate producao. Nenhuma ferramenta substitui testes com usuarios reais de assistive technology, mas ferramentas automatizadas e semi-automatizadas catch a maioria dos problemas antes que cheguem a producao.

Este documento organiza ferramentas por etapa do processo: design (plugins Figma), desenvolvimento (linters, testing libraries), QA (browser extensions, screen readers) e monitoramento (auditorias automatizadas continuas).



## Key Concepts


### 1. Design Phase Tools

Figma plugins: Stark (contrast checker, color blindness simulation, focus order annotation), A11y Annotation Kit (layer annotations para developers), Color Blind (simulacao de tipos de daltonismo), Able (contrast checker). Use Stark ou Able em todo design antes de handoff.


### 2. Development Phase Tools

axe-core (engine de testing mais usada, integrada a Storybook e CI). eslint-plugin-jsx-a11y (linting de acessibilidade em JSX). Pa11y (automated testing CLI). WAVE API (testing programatico). Jest-axe (assertions de acessibilidade em unit tests).


### 3. QA and Manual Testing

Screen readers: VoiceOver (macOS/iOS, built-in), NVDA (Windows, gratuito), JAWS (Windows, pago — padrao enterprise). Browser extensions: axe DevTools, WAVE, Lighthouse. Keyboard testing: navegar o produto inteiro usando apenas teclado (Tab, Arrow, Enter, Escape).


### 4. Automated Monitoring

axe Monitor, Deque WorldSpace: scanning automatico e continuo de paginas em producao. Lighthouse CI: metricas de acessibilidade no pipeline de CI. Alertas quando score de acessibilidade cai abaixo do threshold.


### 5. Testing Protocol

Ordem recomendada: (1) automated scan com axe (catch ~30% dos problemas), (2) keyboard navigation test manual (catch ~20% adicionais), (3) screen reader test com VoiceOver/NVDA (catch ~20% adicionais), (4) teste com usuarios reais de assistive technology (catch os ~30% restantes). Automated alone e insuficiente.



## Application to Design Squad

- **Stark como mandatory plugin:** Todos designers devem ter Stark instalado no Figma e verificar contraste antes de qualquer handoff.
- **axe no Storybook:** Configurar addon de acessibilidade do Storybook (usa axe-core) como parte do definition of done para componentes.
- **Keyboard test mensal:** Uma vez por mes, navegar os fluxos principais do produto usando apenas teclado. Documentar problemas encontrados.
- **Screen reader test trimestral:** Uma vez por trimestre, testar os fluxos principais com VoiceOver. Cada designer do squad faz pelo menos um teste por trimestre.
- **Accessibility score no CI:** Implementar Lighthouse CI com threshold de accessibility score. PR que reduz o score e bloqueado.



## Key Takeaways

1. **Automated testing catch ~30% dos problemas.** E necessario mas insuficiente — combine com manual e user testing.

2. **Keyboard testing e o melhor custo-beneficio.** Rapido, sem ferramenta especial, revela problemas graves de navegacao e focus.

3. **Screen reader testing revela o que automated nao ve.** Experiencia de screen reader nao e apenas "ler alt text" — e navegacao, estrutura e anuncio.

4. **Ferramentas de design previnem problemas cedo.** Verificar contraste no Figma e 10x mais barato que corrigir em producao.

5. **Nada substitui teste com usuarios reais.** Ferramentas automatizadas sao filtro, nao validacao. Usuarios de assistive technology sao os juizes finais.



## Cross-References

- [WCAG 2.x Notes](../standards/wcag-2-x-notes.md) — criterios que as ferramentas verificam
- [ARIA Authoring Practices](../standards/aria-authoring-practices.md) — padroes de implementacao
- [Storybook for Design Systems](storybook-for-design-systems.md) — testes integrados
- [Figma Library Governance](figma-library-governance.md) — plugins no workflow
- [Design of Everyday Things — Norman](../books/norman-design-of-everyday-things.md) — design inclusivo
