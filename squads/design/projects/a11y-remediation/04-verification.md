# Phase: Verification & Validation

## Objective

Verificar que correcoes de acessibilidade sao eficazes e que o produto atingiu o nivel de compliance target (WCAG AA).

## Inputs

- Issues corrigidos (03-remediation.md)
- Original findings para comparacao
- Testing tools e screen readers
- Target compliance score (85%+ para AA-)

## Activities

### 1. Automated Re-Scan
Rodar axe-core completo em todas as paginas. Comparar com scan original: issues resolvidos, issues remanescentes, novos issues introduzidos. Gerar compliance score atualizado.

### 2. Manual Re-Test
Re-testar keyboard navigation em todos os fluxos. Re-testar screen reader nos fluxos principais. Re-verificar contraste em combinacoes alteradas. Verificar fixes de issues especificos reportados.

### 3. Assistive Technology Testing
Teste com usuarios reais de assistive technology (se possivel). Ou teste com tester experiente em AT: VoiceOver (Mac/iOS), NVDA (Windows), TalkBack (Android), keyboard-only, zoom 400%.

### 4. Compliance Report
Gerar VPAT (Voluntary Product Accessibility Template) ou equivalente. Documentar nivel de conformidade por WCAG criterion. Listar issues remanescentes com timeline de resolucao. Preparar documentacao para stakeholders e legal.

### 5. Ongoing Monitoring Plan
Definir cadencia de re-audit: automated (cada PR), manual (trimestral), full audit (anual). Definir processo para novos issues. Definir ownership de a11y por area.

## Output

- Compliance report final com score
- VPAT ou equivalente documentado
- Issues remanescentes com timeline
- Monitoring plan aprovado
- Celebracao do progresso com o time

## Next Phase

→ Monitoring continuo conforme plan + proximo ciclo de audit (trimestral/anual)
