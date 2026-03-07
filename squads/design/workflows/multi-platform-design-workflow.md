# Multi-Platform Design Workflow

## Metadata

| Campo         | Valor                                            |
| ------------- | ------------------------------------------------ |
| squad         | Design                                           |
| versao        | 1.0.0                                            |
| criado_em     | 2026-03-06                                       |
| owner         | Design Lead                                      |
| cadencia      | Por feature multi-platform                       |
| duracao_media | 2-4 sprints (todas as plataformas)               |
| tags          | multi-platform, web, mobile, desktop, consistency|

## Trigger

Quando iniciar:

- Feature para 2+ plataformas (web, iOS, Android, desktop).
- Redesign de feature existente multi-platform.
- Nova plataforma adicionada ao produto.
- Inconsistencia entre plataformas identificada como critica.

Pre-condicoes: feature aprovada para multiplas plataformas; DS com suporte multi-platform; designer com conhecimento de HIG/Material; timeline definido.

## Phases

### Fase 1 — Platform-Agnostic Design
**Agents:** Designer, PM, Researcher.
**Inputs:** Brief da feature, pesquisa (contextos de uso por plataforma), fluxo mapeado.
**Atividades:** Definir fluxo core igual em todas as plataformas (steps, info, decisoes); identificar diferencas de contexto (web: tela grande, mouse; mobile: touch, on-the-go; desktop: keyboard shortcuts, deep workflows); documentar o que deve ser consistente (flow, terminologia, mental model, IA) vs diferente (input methods, navigation patterns, layout, density, platform features); wireframes conceituais.
**Outputs:** Fluxo core, lista de consistencias obrigatorias, lista de diferencas permitidas, wireframes.

### Fase 2 — Web Design
**Agents:** Designer.
**Inputs:** Fluxo core, DS web, web best practices.
**Atividades:** Adaptar para contexto web; design responsivo mobile-first; componentes DS web; otimizar mouse/keyboard; estados web-specific (loading, empty, error); layout tela grande (sidebar, multi-column).
**Outputs:** Mockups web (all breakpoints), specs web-specific.

### Fase 3 — Mobile Design
**Agents:** Designer.
**Inputs:** Fluxo core, DS mobile, Apple HIG, Material Design.
**Atividades:** Adaptar para mobile; patterns nativos por OS (iOS: nav controller, tab bar, sheets; Android: bottom nav, FAB, snackbar); touch targets min 44pt/48dp; gesture navigation; one-handed use; offline states; notificacoes e deep links.
**Outputs:** Mockups iOS e Android, specs mobile-specific, diferencas iOS vs Android documentadas.

### Fase 4 — Desktop App Design
**Agents:** Designer.
**Inputs:** Fluxo core, DS desktop, OS guidelines.
**Atividades:** Aproveitar real estate (multi-panel, densidade maior); keyboard shortcuts para power users; menu bar e system tray; drag and drop; window resizing behavior; offline-first; system notifications.
**Outputs:** Mockups desktop (min/default/max), keyboard shortcut map, specs desktop-specific.

### Fase 5 — Consistency Review
**Agents:** Designer, Design Lead, representante por plataforma.
**Inputs:** Mockups de todas as plataformas, listas de consistencia da Fase 1.
**Atividades:** Side-by-side comparison; verificar consistencia obrigatoria (fluxo, terminologia, mental model, brand); verificar diferencas permitidas (patterns nativos corretos, adaptacoes fazem sentido, sem inconsistencias acidentais); documentar decisoes; criar cross-platform spec sheet; ajustar onde necessario.
**Outputs:** Cross-platform spec sheet, decisoes documentadas, designs prontos para handoff por plataforma.

## Quality Gates

### Gate Agnostic -> Platform-Specific
- [ ] Fluxo core documentado.
- [ ] Consistencias e diferencas listadas.

### Gate Web
- [ ] Breakpoints cobertos.
- [ ] Componentes DS utilizados.

### Gate Mobile
- [ ] iOS e Android completos.
- [ ] Patterns nativos respeitados.
- [ ] Touch targets >= 44pt/48dp.

### Gate Desktop
- [ ] Window sizes cobertos.
- [ ] Keyboard shortcuts definidos.

### Gate Consistency Review
- [ ] Side-by-side realizado.
- [ ] Diferencas intencionais documentadas.
- [ ] Cross-platform spec sheet criado.
- [ ] Design Lead sign-off.

## Cross-References

- `feature-design-end-to-end.md` — Cada plataforma segue pipeline.
- `design-system-component-lifecycle.md` — Variantes por plataforma.
- `design-to-code-sync.md` — Tokens por plataforma.
- `handoff-and-build-loop.md` — Handoff por plataforma.
- `usability-testing-sprint.md` — Testar por plataforma.
- `cross-squad-narrative-handoff.md` — Copy pode variar.
- `accessibility-remediation-loop.md` — A11y por plataforma (VoiceOver, TalkBack).
