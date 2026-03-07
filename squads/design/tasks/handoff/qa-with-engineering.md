# QA with Engineering

## Metadata
- **Categoria:** Handoff
- **Complexidade:** Média
- **Tempo Estimado:** 1-3 dias por feature
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** handoff, qa, engineering, review, pixel-perfect, implementation

## Objective
Realizar quality assurance de design sobre a implementação desenvolvida pela engenharia, comparando
o resultado com as specs de design e documentando divergências. O processo garante fidelidade visual
e comportamental antes do release para produção.

## Prerequisites
- Feature implementada disponível em staging/preview environment
- Design specs (Figma) acessíveis para comparação lado a lado
- Design acceptance criteria documentados
- Ferramenta de comparação visual configurada (overlay tools, screenshots)
- Acesso a múltiplos dispositivos e browsers para teste

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UI Designer | Executar QA visual, documentar discrepâncias |
| UX Designer | Validar fluxos, comportamentos e edge cases |
| Frontend Engineer | Corrigir issues identificados e esclarecer limitações |
| QA Engineer | Testar funcionalidade e acessibilidade em paralelo |
| A11y Specialist | Verificar implementação de requisitos de acessibilidade |

## Frameworks
- **Visual QA Checklist** — itens de verificação visual padronizados
- **Design Overlay Method** — sobreposição de screenshot vs mockup para comparação
- **Device/Browser Matrix** — combinações de teste priorizadas
- **Bug Severity Scale** — critical (blocker), major (visual break), minor (polish)
- **Design QA Sign-off** — aprovação formal de design sobre a implementação

## Checklists
- [ ] Staging environment acessível e atualizado com a feature
- [ ] Comparação visual executada para cada tela principal
- [ ] Espaçamento e alinhamento verificados (8pt grid)
- [ ] Tipografia verificada (font, size, weight, line-height, color)
- [ ] Cores verificadas contra design tokens
- [ ] Componentes interativos testados em todos os estados
- [ ] Responsividade verificada nos breakpoints definidos
- [ ] Animações e transições comparadas com motion specs
- [ ] Edge cases testados (empty, error, loading, long text)
- [ ] Issues documentados com screenshot e severity

## Steps
1. **Acessar staging** — Confirmar que a feature está deployada no ambiente de staging com dados
   representativos. Verificar que é a versão correta para review.

2. **Comparar layout visual** — Para cada tela, fazer screenshot da implementação e comparar
   com mockup do Figma. Usar overlay tool para identificar divergências de alinhamento.

3. **Verificar tipografia** — Confirmar: font-family, font-size, font-weight, line-height,
   letter-spacing e color para cada elemento de texto. Comparar com tokens do DS.

4. **Verificar cores e espaçamento** — Inspecionar cores de background, borders, ícones e texto
   contra tokens. Medir espaçamentos e verificar aderência ao grid.

5. **Testar componentes interativos** — Verificar todos os estados: hover, active, focused,
   disabled, loading, error. Comparar com specs de estados do handoff.

6. **Testar responsividade** — Redimensionar browser e testar em dispositivos reais. Verificar
   que os comportamentos responsive estão conforme spec.

7. **Testar edge cases** — Verificar: textos longos (truncation, wrap), empty states, estados
   de erro, loading states e first-time experience.

8. **Documentar issues** — Para cada discrepância, registrar: localização, expected (screenshot
   do mockup), actual (screenshot da implementação), severity e sugestão de fix.

9. **Revisar com engineer** — Conduzir sessão de 30 minutos com Frontend Engineer para percorrer
   issues. Alinhar prioridade e timeline de correção.

10. **Verificar fixes e sign-off** — Após correções, re-verificar cada issue. Quando todas as
    issues critical e major estão resolvidas, emitir design QA sign-off.

## Output
- **QA Report** — Lista de issues com screenshots, severity e status
- **Design Sign-off** — Aprovação formal de design sobre a implementação
- **Formato:** Markdown ou ticket tracker + screenshots
- **Nomenclatura:** `design-qa-[nome-da-feature]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UI Designer |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por feature antes do release |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/handoff/` |

## Cross-References
- [Dev Handoff](./dev-handoff.md)
- [Post-Release Review](./post-release-review.md)
- [A11y Audit](../accessibility/a11y-audit.md)
- [Handoff Review](../review/handoff-review.md)
- [UI Design High Fidelity](../ui/ui-design-high-fidelity.md)
