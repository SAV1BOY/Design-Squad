# Apple Human Interface Guidelines (HIG)



## Metadata

- **Organizacao:** Apple
- **Plataformas:** iOS, iPadOS, macOS, watchOS, tvOS, visionOS
- **Categoria:** Platform Guidelines, Design System
- **Relevancia para o Squad:** Media — referencia para design multiplataforma
- **Ultima revisao:** 2026-03-06



## Summary

As Human Interface Guidelines (HIG) da Apple sao o guia oficial para design de apps nas plataformas Apple. Diferente de Material Design (sistema de design com componentes), o HIG e um conjunto de principios, padroes e best practices que orientam como criar experiencias nativas e consistentes em cada plataforma Apple.

O HIG e organizado por principio (clarity, deference, depth), por plataforma (iOS, macOS, visionOS) e por componente/pattern. A Apple enfatiza que bons apps se sentem nativos — respeitam os paradigmas da plataforma enquanto expressam personalidade propria. Apps que ignoram o HIG parecem "estranhos" para usuarios Apple, mesmo que sejam tecnicamente funcionais.

A adicao de visionOS guidelines em 2023 trouxe principios de spatial design ineditos — como projetar para realidade mista, onde elementos existem em espaco 3D ao redor do usuario. Embora especifico para Vision Pro, os principios de spatial hierarchy e contextual depth sao aplicaveis a outras plataformas.



## Key Concepts


### 1. Design Principles (Clarity, Deference, Depth)

Clarity: texto e todo tamanho legivel, icones precisos, affordances obvias. Deference: a interface serve o conteudo, nao compete com ele; UI elements sao translucidos e leves. Depth: camadas e transicoes comunicam hierarquia e contexto; motion e physics reforçam relacoes espaciais.


### 2. Platform Conventions

Cada plataforma tem convencoes proprias: iOS usa tab bars e navigation controllers; macOS usa sidebars e toolbars; watchOS usa listas scrollaveis e complicacoes; visionOS usa volumes e windows flutuantes. Respeitar convencoes de plataforma e pre-requisito para experiencia nativa.


### 3. SF Symbols and System Components

Apple oferece 5000+ SF Symbols (icones consistentes com tipografia SF) e componentes nativos que se adaptam a accessibility settings (Dynamic Type, Bold Text, Reduce Motion). Usar componentes nativos garante acessibilidade automatica e consistencia com o ecossistema.


### 4. Typography System (Dynamic Type)

O sistema tipografico da Apple se adapta as preferencias de acessibilidade do usuario. Designers devem projetar com Dynamic Type em mente — layouts que funcionam com texto 2x maior que o default. Isso requer layouts flexiveis e prioridades de conteudo claras.


### 5. Privacy by Design

Apple enfatiza privacidade como principio de design: pedir permissoes no momento de uso (nao no onboarding), explicar por que cada dado e necessario, oferecer alternativas quando permissao e negada, respeitar o principio de data minimization.



## Application to Design Squad

- **Platform-aware design:** Quando o produto tem versao mobile, respeitar convencoes de plataforma. Tab bar em iOS, navigation drawer em Android. Nao forcar um modelo cross-platform que parece estranho em ambos.
- **Dynamic Type testing:** Testar todos os designs com texto 2x maior para garantir que layouts nao quebram. Isso beneficia acessibilidade em todas as plataformas, nao apenas Apple.
- **Privacy-first patterns:** Adotar o principio de pedir permissoes contextualmente (no momento de uso) e explicar o motivo. Aplicavel a qualquer plataforma.
- **Iconografia consistente:** Usar sistema de icones coerente (como SF Symbols e para Apple). Garantir que icones do design system sao consistentes em estilo, peso e metafora.
- **Content-first layouts:** Seguir o principio de deference — a UI serve o conteudo. Avaliar se elementos de interface competem com ou suportam o conteudo principal.



## Key Takeaways

1. **Plataformas tem convencoes — respeita-las e design.** Usuarios esperam comportamento nativo; desviar sem motivo e confusao.

2. **Acessibilidade tipografica requer layouts flexiveis.** Se o design quebra com texto maior, o layout e fragil.

3. **Privacidade e decisao de design.** Quando e como pedir permissoes impacta confianca e conversao.

4. **Content-first, UI-second.** A interface existe para servir conteudo, nao para se exibir.

5. **Design para o ecossistema, nao para a tela.** Usuarios transitam entre dispositivos — a experiencia deve ser coerente no ecossistema.



## Cross-References

- [Material Design Notes](material-design-notes.md) — design system alternativo
- [Microsoft Fluent Notes](microsoft-fluent-notes.md) — terceiro grande design system
- [Mobile-First Design Playbook](../industries/mobile-first-design-playbook.md) — design mobile
- [Navigation Patterns](../ui-patterns/navigation-patterns.md) — padroes de navegacao cross-platform
- [Accessibility Tools](../tools/accessibility-tools.md) — ferramentas de teste
