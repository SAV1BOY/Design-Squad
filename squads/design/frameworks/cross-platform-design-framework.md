# Cross-Platform Design Framework

## Metadata
- **Autor**: Design Squad
- **Categoria**: Multi-Platform, Consistencia, Design Systems
- **Complexidade**: Alta
- **Aplicacao**: Manter consistencia de experiencia entre Web, iOS e Android
- **Ultima atualizacao**: 2026-03-06

## Concept

O Cross-Platform Design Framework define principios e praticas para manter consistencia
de experiencia entre Web, iOS e Android, equilibrando identidade de produto com convencoes
nativas de cada plataforma.

O dilema central e: ate que ponto o produto deve parecer "o mesmo" em todas as plataformas
vs seguir os padroes nativos (Material Design no Android, Human Interface Guidelines no iOS,
convencoes web)? A resposta nao e binaria — e um espectro que deve ser navegado
deliberadamente para cada tipo de componente e interacao.

O framework propoe uma classificacao em tres categorias: Brand-consistent (igual em todas
as plataformas), Platform-adaptive (mesmo conceito, adaptado a convencao nativa) e
Platform-native (usa componente nativo da plataforma).

## When to Use

- Quando o produto existe em Web, iOS e Android simultaneamente
- Quando usuarios transitam entre plataformas e esperam experiencia coerente
- Quando inconsistencias entre plataformas geram confusao ou tickets de suporte
- Quando se constroi design system que serve multiplas plataformas
- Quando se toma decisoes de design que afetam mais de uma plataforma
- Quando se planeja lancamento de produto em nova plataforma

## How to Apply

### Classificacao de Componentes por Estrategia

**Brand-Consistent (Identico em todas as plataformas)**
Componentes cuja identidade de marca e mais importante que convencao nativa:
- Color system e tokens visuais
- Tipografia do produto (font family, scale)
- Iconografia custom do produto
- Logo, branding elements
- Ilustracoes e estilo visual
- Componentes core diferenciadores (feature unica do produto)

**Platform-Adaptive (Mesmo conceito, execucao nativa)**
Componentes que seguem o conceito do produto mas respeitam padroes nativos:
- Navegacao: Tab bar (iOS) vs Bottom navigation (Android) vs Sidebar (Web)
- Formularios: Picker nativo vs dropdown custom
- Gestos: Swipe behaviors conforme plataforma
- Feedback: Toast vs Snackbar vs Alert
- Tipografia base: SF Pro (iOS), Roboto (Android), System (Web)
- Espacamento: Seguir grid de cada plataforma quando apropriado

**Platform-Native (Usa componente nativo)**
Componentes onde a convencao nativa deve prevalecer:
- Date/time pickers
- Alertas de sistema (permissions, errors)
- Share sheets
- Notifications
- Status bar, system chrome
- Keyboard behavior, text selection

### Processo de Decisao
Para cada componente, pergunte:
1. Este componente e parte da identidade de marca? -> Brand-consistent
2. Usuarios esperam comportamento nativo? -> Platform-native
3. E algo entre os dois? -> Platform-adaptive

### Tokens Cross-Platform
1. Defina tokens em formato abstrato (JSON) como source of truth
2. Transforme para cada plataforma:
   - Web: CSS Custom Properties
   - iOS: Swift UIColor / SwiftUI modifiers
   - Android: XML resources / Compose theme
3. Use mesmos nomes semanticos em todas as plataformas
4. Valide consistencia de valores entre plataformas
5. Sincronize updates via pipeline automatizado

### Design File Organization
1. Mantenha um Figma file por plataforma + 1 shared foundations file
2. Foundations file: tokens, cores, tipografia (source of truth)
3. Platform files: componentes adaptados com specs nativas
4. Cross-reference entre files para manter sincronizacao
5. Review cross-platform a cada 2 semanas

### QA Cross-Platform
1. Defina "parity matrix": qual feature existe em qual plataforma
2. Para features paritarias, defina nivel de consistencia esperado
3. Teste fluxos criticos em todas as plataformas simultaneamente
4. Compare screenshots cross-platform para detectar drift
5. Priorize consistencia de funcionalidade sobre consistencia visual

## Key Principles

- **Experiencia coerente, nao identica**: O produto deve ser reconhecivel, nao clonado
- **Respeite convencoes nativas**: Usuarios de iOS esperam comportamento iOS
- **Tokens como fundacao compartilhada**: Mesmos tokens, diferentes implementacoes
- **Feature parity e estrategia**: Nem tudo precisa existir em todas as plataformas
- **Consistencia de conceito**: O modelo mental do usuario deve ser o mesmo
- **Teste cross-platform**: Bugs de plataforma so aparecem testando naquela plataforma
- **Progressive rollout**: Lance em uma plataforma, aprenda, adapte para as outras

## Examples

### Exemplo 1 — Navegacao Cross-Platform
Conceito: Navegacao principal com 5 secoes
- **iOS**: Tab bar na parte inferior com icones e labels, swipe entre tabs
- **Android**: Bottom navigation bar, sem swipe (Material Design)
- **Web**: Sidebar persistente no desktop, bottom nav no mobile web
Consistencia: Mesmas 5 secoes, mesmos icones, mesmas cores. Diferenca: posicao,
animacao de transicao e gestos seguem convencao nativa.

### Exemplo 2 — Token Cross-Platform
Token `color-action-primary: #2563EB` implementado:
- Web: `--color-action-primary: #2563EB` (CSS custom property)
- iOS: `Color.actionPrimary` (UIColor extension / SwiftUI)
- Android: `colorActionPrimary` (#2563EB em themes.xml / Compose)
Mesmo nome semantico, mesma cor, formato nativo de cada plataforma.

### Exemplo 3 — Parity Matrix
| Feature          | Web | iOS | Android | Consistencia |
|------------------|-----|-----|---------|--------------|
| Login/Signup     | Yes | Yes | Yes     | Brand-consistent |
| Dashboard        | Yes | Yes | Yes     | Platform-adaptive|
| Push notifications| No | Yes | Yes     | Platform-native |
| Keyboard shortcuts| Yes | No  | No     | Platform-specific|
| Biometric auth   | No  | Yes | Yes     | Platform-native |
| Drag and drop    | Yes | No  | No      | Platform-specific|

## Common Pitfalls

- **Clone web para mobile**: Replicar UI web em app mobile ignora padroes nativos e
  gera experiencia estranha
- **Ignorar convencoes nativas**: Usuarios esperam back button no Android, swipe-back no iOS
- **Feature parity forcada**: Nem toda feature web faz sentido em mobile e vice-versa
- **Tokens desincronizados**: Atualizar token no web e esquecer de atualizar no iOS cria drift
- **Testar so em uma plataforma**: "Funciona no web" nao significa "funciona no iOS"
- **Over-customization**: Customizar tudo ignora que usuarios ja sabem usar componentes nativos
- **Design em silos**: Designers de iOS e web que nao conversam criam experiencias divergentes

## Cross-References

- [design-token-architecture.md](design-token-architecture.md) — Tokens como base cross-platform
- [multi-brand-design-system.md](multi-brand-design-system.md) — Multi-brand + multi-platform
- [design-system-layer.md](design-system-layer.md) — DS como infraestrutura compartilhada
- [malouf-service-design-framework.md](malouf-service-design-framework.md) — Experiencia cross-channel
- [frost-death-of-the-page.md](frost-death-of-the-page.md) — Componentes context-agnostic
- [handoff-layer.md](handoff-layer.md) — Specs por plataforma
