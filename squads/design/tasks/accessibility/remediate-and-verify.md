# Remediate and Verify

## Metadata
- **Categoria:** Accessibility
- **Complexidade:** Média-Alta
- **Tempo Estimado:** 5-15 dias (depende do volume de issues)
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** accessibility, remediation, verification, fix, regression

## Objective
Executar o plano de remediação de acessibilidade gerado pelo A11y Audit: corrigir issues de design,
acompanhar implementação de fixes no código e verificar que as correções resolvem efetivamente
as barreiras identificadas sem introduzir regressões.

## Prerequisites
- A11y Audit Report disponível com findings priorizados
- Plano de remediação aprovado e priorizado
- Sprint(s) de remediação alocados no calendário do squad
- Ferramentas de teste de acessibilidade configuradas
- Designs corrigidos prontos no Figma (para fixes de design)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| A11y Specialist | Definir solução, validar fixes e executar verification |
| UI Designer | Corrigir issues de design (contraste, tamanho, indicadores) |
| Frontend Engineer | Implementar fixes no código (ARIA, keyboard, semântica) |
| QA Engineer | Executar testes de regressão de acessibilidade |
| Design Lead | Monitorar progresso e resolver bloqueios |

## Frameworks
- **Issue Severity Prioritization** — Critical primeiro, depois Major, Minor
- **Fix Verification Protocol** — antes/depois com mesma assistive tech
- **Regression Testing** — verificar que fixes não quebram funcionalidades existentes
- **Acceptance Criteria (A11y)** — critério específico para considerar fix aprovado
- **WCAG Technique Mapping** — técnica WCAG recomendada para cada tipo de fix

## Checklists
- [ ] Issues priorizados e atribuídos a responsáveis (design vs code)
- [ ] Fixes de design entregues no Figma para issues visuais
- [ ] Fixes de código implementados para issues técnicas
- [ ] Cada fix verificado individualmente contra o criterion WCAG original
- [ ] Teste de keyboard re-executado nos fluxos corrigidos
- [ ] Teste com screen reader re-executado nos fluxos corrigidos
- [ ] Teste de contraste re-verificado para mudanças de cor
- [ ] Testes automatizados (axe) re-executados sem novas violações
- [ ] Regressão verificada: nenhum novo issue introduzido
- [ ] Status de cada issue atualizado (fixed, verified, reopened)

## Steps
1. **Revisar e atribuir issues** — A partir do plano de remediação, atribuir cada issue ao
   responsável correto: UI Designer (visuais), Frontend (técnicos), ambos (complexos).

2. **Corrigir issues de design** — No Figma, corrigir: contraste insuficiente, targets pequenos,
   focus indicators ausentes, hierarquia de headings e indicadores não-cromáticos.

3. **Acompanhar implementação** — Monitorar progresso dos fixes de código. Oferecer suporte
   técnico de a11y ao Frontend Engineer para ARIA patterns complexos.

4. **Verificar cada fix individualmente** — Para cada issue corrigido, re-testar usando a mesma
   assistive technology e critério WCAG do finding original.

5. **Re-executar testes de keyboard** — Percorrer todos os fluxos corrigidos usando apenas
   teclado. Verificar que focus order, visibility e interactions estão corretos.

6. **Re-executar testes com screen reader** — Navegar fluxos corrigidos com NVDA e VoiceOver.
   Confirmar que a experiência é compreensível e operável via screen reader.

7. **Executar testes automatizados** — Rodar axe DevTools nas páginas corrigidas. Confirmar
   zero violações novas e que violações anteriores foram resolvidas.

8. **Verificar regressões** — Testar funcionalidades adjacentes aos fixes para garantir que
   nenhuma regressão foi introduzida (visual ou funcional).

9. **Atualizar status dos issues** — Marcar cada issue como: verified (fix confirmado), reopened
   (fix insuficiente) ou wontfix (decisão documentada com justificativa).

10. **Documentar e fechar ciclo** — Atualizar o A11y Audit Report com status final de cada
    issue. Calcular novo conformance score e comunicar progresso ao squad.

## Output
- **Verification Report** — Status de cada issue: verified, reopened, wontfix
- **Updated Conformance Score** — Nova pontuação de conformidade pós-remediação
- **Regression Test Results** — Confirmação de ausência de regressões
- **Formato:** Markdown + planilha atualizada de issues
- **Nomenclatura:** `a11y-remediation-[produto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | A11y Specialist |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Após cada A11y Audit |
| Aprovadores | Design Lead, A11y Specialist |
| Repositório | `/squads/design/tasks/accessibility/` |

## Cross-References
- [A11y Audit](./a11y-audit.md)
- [A11y Training Session](./a11y-training-session.md)
- [QA with Engineering](../handoff/qa-with-engineering.md)
- [Post-Release Review](../handoff/post-release-review.md)
- [Design Debt Prioritization](../operations/design-debt-prioritization.md)
