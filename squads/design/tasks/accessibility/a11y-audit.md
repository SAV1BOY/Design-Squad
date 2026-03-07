# A11y Audit

## Metadata
- **Categoria:** Accessibility
- **Complexidade:** Alta
- **Tempo Estimado:** 5-10 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** accessibility, audit, wcag, compliance, inclusive-design

## Objective
Realizar um audit completo de acessibilidade do produto ou feature avaliando conformidade com
WCAG 2.2 Level AA. O audit identifica barreiras de acesso, classifica por severidade e gera um
plano de remediação priorizado para garantir que o produto é utilizável por todos.

## Prerequisites
- Produto ou feature disponível em staging ou produção para avaliação
- Escopo do audit definido (fluxos, páginas, plataformas)
- Ferramentas de teste configuradas: axe DevTools, WAVE, screen reader (NVDA/VoiceOver)
- Checklist WCAG 2.2 Level AA preparado
- Assistive technologies disponíveis para teste manual

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| A11y Specialist | Conduzir audit, classificar findings e redigir relatório |
| UX Designer | Contextualizar fluxos e participar da análise de impacto |
| Frontend Engineer | Apoiar investigação técnica e validar viabilidade de fixes |
| Design Lead | Priorizar remediações e alocar recursos |
| QA Engineer | Apoiar testes automatizados de acessibilidade |

## Frameworks
- **WCAG 2.2 (Level AA)** — critérios de conformidade (A + AA)
- **ARIA Authoring Practices** — padrões de implementação por componente
- **axe-core Rules** — regras automatizáveis de acessibilidade
- **Severity Scale (A11y)** — Critical (blocker), Major, Minor, Enhancement
- **Testing Matrix** — combinação de assistive tech x browser x device

## Checklists
- [ ] Escopo do audit definido e documentado
- [ ] Teste automatizado executado (axe DevTools, Lighthouse)
- [ ] Teste de contraste executado para todas as combinações text/bg
- [ ] Teste de keyboard navigation executado em todos os fluxos
- [ ] Teste com screen reader executado (NVDA no Windows, VoiceOver no macOS)
- [ ] Teste de zoom (200% e 400%) executado
- [ ] Teste de motion (prefers-reduced-motion) verificado
- [ ] Findings classificados por WCAG criterion e severidade
- [ ] Relatório com evidências (screenshots, recordings) redigido
- [ ] Plano de remediação priorizado e entregue ao squad

## Steps
1. **Definir escopo e matriz de testes** — Delimitar fluxos, páginas e plataformas. Definir
   combinações de assistive tech x browser x device a serem testadas.

2. **Executar testes automatizados** — Rodar axe DevTools, Lighthouse e WAVE em todas as
   páginas do escopo. Exportar resultados e classificar findings únicos.

3. **Testar contraste de cores** — Verificar todas as combinações de text/background contra
   WCAG: 4.5:1 para texto normal, 3:1 para texto grande e elementos gráficos.

4. **Testar keyboard navigation** — Percorrer cada fluxo usando apenas Tab, Shift+Tab, Enter,
   Space, Escape e Arrow keys. Verificar: focus visible, focus order, no keyboard traps.

5. **Testar com screen reader** — Navegar fluxos com NVDA (Windows) e VoiceOver (macOS).
   Verificar: headings structure, landmark regions, alt texts, form labels, live regions.

6. **Testar zoom e reflow** — Ampliar para 200% e 400%. Verificar: no horizontal scroll,
   conteúdo acessível, touch targets mantidos, text readable.

7. **Testar media e motion** — Verificar: vídeos com captions, áudio com transcrição, animações
   pausáveis e respeito a prefers-reduced-motion.

8. **Classificar findings** — Para cada issue, registrar: WCAG criterion violado, severidade
   (critical/major/minor), evidência (screenshot/recording) e recomendação de fix.

9. **Redigir relatório** — Consolidar em documento: resumo executivo, score de conformidade,
   findings por categoria, evidências e plano de remediação priorizado.

10. **Apresentar e planejar remediação** — Compartilhar relatório com squad. Priorizar fixes
    por severidade. Agendar sprint(s) de remediação conforme capacidade.

## Output
- **A11y Audit Report** — Relatório completo com findings, evidências e recomendações
- **Remediation Plan** — Plano priorizado de correções com timeline
- **Conformance Score** — % de critérios WCAG 2.2 AA atendidos
- **Formato:** Markdown + planilha de findings + screenshots/recordings
- **Nomenclatura:** `a11y-audit-[produto/feature]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | A11y Specialist |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Trimestral ou por major release |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/accessibility/` |

## Cross-References
- [Remediate and Verify](./remediate-and-verify.md)
- [A11y Training Session](./a11y-training-session.md)
- [Accessibility Review](../review/accessibility-review.md)
- [Design Audit Existing Product](../discovery/design-audit-existing-product.md)
- [DS Health Check](../design-system/ds-health-check.md)
- [QA with Engineering](../handoff/qa-with-engineering.md)
