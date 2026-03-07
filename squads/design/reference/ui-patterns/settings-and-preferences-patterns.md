# Settings and Preferences Patterns



## Metadata

- **Categoria:** UI Patterns, Personalization, Configuration
- **Relevancia para o Squad:** Media — patterns de configuracao e personalizacao
- **Ultima revisao:** 2026-03-06



## Summary

Settings e preferences permitem que usuarios personalizem a experiencia do produto. Bem projetadas, empoderam o usuario e aumentam satisfacao. Mal projetadas, confundem com opcoes excessivas e criam ansiedade de decisao. O principio guia: smart defaults que funcionam para a maioria, com opcoes de personalizacao para quem precisa.



## Key Concepts


### 1. Settings Organization

Agrupar por dominio (Account, Notifications, Privacy, Appearance, Integrations), nao por tipo (Toggles, Dropdowns, Text fields). Busca dentro de settings para produtos com muitas opcoes. Hierarquia: categorias > subcategorias > individual settings.


### 2. Smart Defaults

Todo setting deve ter default que funciona para a maioria dos usuarios. Pesquisa de uso informa quais defaults servem a maioria. Defaults nao sao arbitrarios — sao a decisao de design mais impactante de cada setting.


### 3. Progressive Disclosure in Settings

Mostrar settings comuns por default, esconder avancados sob "Advanced" ou "More options". Nao sobrecarregar novatos com opcoes de power user. Settings avancados podem usar linguagem mais tecnica.


### 4. Immediate vs. Explicit Save

Settings que tomam efeito imediatamente (toggle on/off com visual feedback) vs. settings que requerem "Save" explicito (formularios com multiplos campos). Feedback imediato para toggles; confirmacao explicita para mudancas de maior impacto.


### 5. Dangerous Settings

Settings com consequencias significativas (delete account, export data, change email) devem ter: warning explicito, confirmacao adicional (re-type, password), e path de reversal quando possivel. A dificuldade de execucao deve ser proporcional a irreversibilidade.



## Application to Design Squad

- **Settings audit:** Mapear todos os settings do produto. Quais sao usados? Quais nunca sao alterados? Settings nao usados sao candidatos a remocao ou defaults melhores.
- **Default policy:** Documentar o racional de cada default. "O default e X porque Y% dos usuarios usam esse valor, baseado em dados de uso."
- **Progressive disclosure:** Organizar settings em common (visivel por default) e advanced (expandivel). Reduzir carga cognitiva para a maioria.
- **Danger zone design:** Para settings destrutivos, criar padrao visual consistente: zona visual distinta (borda vermelha), warning, confirmacao com friction intencional.
- **Search in settings:** Para produtos com muitos settings, implementar busca. O usuario nao deveria navegar menus para encontrar uma opcao.



## Key Takeaways

1. **Defaults sao a feature mais impactante.** A maioria nao altera settings — o default e a experiencia deles.

2. **Organize por dominio, nao por UI type.** O usuario pensa em "notificacoes," nao em "toggles."

3. **Progressive disclosure reduz overwhelm.** Common upfront, advanced on demand.

4. **Friction intencional para acoes destrutivas.** A dificuldade deve ser proporcional a consequencia.

5. **Busca em settings e necessaria apos ~20 opcoes.** Nao dependa de navegacao hierarquica quando o volume e alto.



## Cross-References

- [Nudge — Thaler](../books/thaler-nudge.md) — defaults como choice architecture
- [Progressive Disclosure Psychology](../psychology/progressive-disclosure-psychology.md) — revelar gradualmente
- [Forms and Validation Patterns](forms-and-validation-patterns.md) — formularios de settings
- [Notifications and Alerts Patterns](notifications-and-alerts-patterns.md) — settings de notificacao
- [Don't Make Me Think — Krug](../books/krug-dont-make-me-think.md) — simplicidade
