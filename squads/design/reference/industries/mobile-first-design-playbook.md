# Mobile-First Design Playbook



## Metadata

- **Categoria:** Industry Playbook, Mobile Design, Responsive
- **Relevancia para o Squad:** Alta — design para a plataforma dominante
- **Ultima revisao:** 2026-03-06



## Summary

Mobile-first design e a abordagem de projetar primeiramente para a menor tela e expandir para telas maiores. No Brasil, onde a maioria do acesso a internet e via mobile e frequentemente em dispositivos de entrada, mobile-first nao e preferencia — e necessidade. Este playbook cobre padroes e restricoes especificas de design mobile.



## Key Concepts


### 1. Touch-First Interaction

Thumb zone: area acessivel pelo polegar (parte inferior da tela). CTAs primarios na thumb zone. Touch targets minimos: 44x44px (Apple) / 48x48dp (Android). Gestures: swipe, pull-to-refresh, long-press. Evitar interacoes que dependem de hover (nao existe em touch).


### 2. Performance as UX

Em mercados emergentes (Brasil incluso), muitos usuarios tem conexao lenta e dispositivos limitados. Performance e UX: imagens otimizadas, lazy loading, skeleton screens, offline-first para dados criticos. Core Web Vitals como metricas de UX, nao apenas de engenharia.


### 3. Progressive Enhancement

Comecar com a experiencia mobile basica funcional e adicionar features conforme a plataforma permite: desktop ganha sidebar, tablet ganha split view, dispositivos rapidos ganham animacoes. A experiencia core funciona em qualquer dispositivo.


### 4. Mobile Navigation Patterns

Bottom tab bar (3-5 destinos), hamburger menu (controverso — esconde navegacao), segmented control (para sub-navegacao), swipeable tabs. Bottom sheet para acoes contextuais. Evitar dropdown menus em mobile — dificeis de usar com touch.


### 5. Mobile Form Optimization

Inputs adaptados: type="email" para teclado com @, type="tel" para numerico, autocomplete para endereco. Minimal fields (cada campo custa mais em mobile). Camera-based input: scan de documentos, QR code, OCR. Biometric para autenticacao.



## Application to Design Squad

- **Mobile-first como default:** Todo design comeca em 375px (iPhone) e expande para tablet e desktop. Nao o contrario.
- **Thumb zone awareness:** CTAs primarios sempre acessiveis pelo polegar. Testar reach em diferentes tamanhos de device.
- **Performance budget:** Definir performance budget: LCP < 2.5s, FID < 100ms, CLS < 0.1. Incluir como criterio de design (imagens, animacoes, complexidade de layout).
- **Gesture documentation:** Documentar gestures suportados no design system: swipe directions, long-press actions, pull-to-refresh contexts. Garantir discoverability (gestures sem signifier sao escondidos).
- **Offline-first consideration:** Para features criticas, projetar comportamento offline: dados cacheados, queue de acoes, sync quando reconectar. Comunicar estado offline claramente.



## Key Takeaways

1. **Mobile-first e necessidade no Brasil.** Maioria do acesso e mobile, frequentemente em dispositivos de entrada com conexao limitada.

2. **Thumb zone determina layout.** CTAs na area acessivel pelo polegar, nao no topo da tela.

3. **Performance e UX.** Pagina que demora 5 segundos para carregar em 3G nao e usavel, independente de quao bonita e.

4. **Gestures precisam de signifiers.** Gestures que o usuario nao descobre sao features escondidas.

5. **Offline e realidade de muitos usuarios.** Projetar para offline-first e inclusivo e resiliente.



## Cross-References

- [Apple HIG](../standards/apple-human-interface-guidelines.md) — iOS design
- [Material Design Notes](../standards/material-design-notes.md) — Android design
- [Navigation Patterns](../ui-patterns/navigation-patterns.md) — mobile navigation
- [Forms and Validation Patterns](../ui-patterns/forms-and-validation-patterns.md) — mobile forms
- [Brazil LATAM Design Context](brazil-latam-design-context.md) — contexto mobile BR
