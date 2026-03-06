# Accessibility by Default

## Metadata
- **Autor**: Design Squad
- **Categoria**: Acessibilidade, Processo, Qualidade
- **Complexidade**: Media-Alta
- **Aplicacao**: Integrar acessibilidade no processo de design desde o inicio
- **Ultima atualizacao**: 2026-03-06

## Concept

Accessibility by Default e o principio de que acessibilidade nao e uma feature a ser
adicionada depois, nem um checklist a ser verificado antes do lancamento — e uma
propriedade fundamental embutida em cada etapa do processo de design e desenvolvimento.

A abordagem shift-left de acessibilidade significa considerar a11y desde a discovery
(pesquisa com usuarios com deficiencia), passando por UX (fluxos acessiveis), UI (contraste,
foco, tipografia), design system (componentes acessiveis por padrao), handoff (a11y specs),
ate QA (testes de acessibilidade automatizados e manuais).

O custo de corrigir problemas de acessibilidade cresce exponencialmente quanto mais tarde
sao identificados: 1x na fase de design, 10x na implementacao, 100x apos lancamento.

## When to Use

- Sempre — acessibilidade nao e opcional ou situacional
- Quando se estabelece ou evolui o processo de design de uma equipe
- Quando se constroi ou refatora componentes do design system
- Quando se planeja testes e quality assurance
- Quando se treina novos membros da equipe de design
- Quando se avalia compliance com WCAG e legislacao aplicavel

## How to Apply

### Etapa 1 — Discovery Acessivel
1. Inclua pessoas com deficiencia na pesquisa de usuarios
2. Mapeie assistive technologies usadas pelo publico-alvo
3. Identifique barreiras de acessibilidade nos fluxos atuais
4. Considere cenarios de uso: baixa visao, motor, cognitivo, auditivo
5. Documente requisitos de acessibilidade como parte do brief

### Etapa 2 — UX Acessivel
1. **Fluxos lineares**: Garanta que toda tarefa pode ser completada sequencialmente
2. **Alternativas**: Para cada interacao visual, tenha alternativa nao-visual
3. **Cognitivo**: Simplifique linguagem, reduza carga cognitiva
4. **Erro recovery**: Facilite identificacao, prevencao e correcao de erros
5. **Consistencia**: Padroes previsíveis reduzem carga de aprendizado
6. **Focus management**: Planeje para onde o foco vai apos cada acao

### Etapa 3 — UI Acessivel
1. **Contraste**: WCAG AA minimo (4.5:1 texto normal, 3:1 texto grande)
2. **Tipografia**: Minimo 16px body, line-height 1.5, nao justificado
3. **Touch targets**: Minimo 44x44px para interacoes touch
4. **Color independence**: Nunca dependa apenas de cor para comunicar informacao
5. **Focus indicators**: Foco visivel e distinguivel em todos os componentes
6. **Motion**: Respeite `prefers-reduced-motion`, evite motion excessivo
7. **Responsive text**: Suporte zoom ate 200% sem perda de funcionalidade

### Etapa 4 — Design System Acessivel
1. Componentes acessiveis por padrao (ARIA built-in, keyboard nav, contraste)
2. Tokens de cor validados para contraste em todas as combinacoes
3. Documentacao de a11y em cada component spec
4. Testes automatizados de a11y em cada componente (axe-core, Storybook a11y addon)
5. Guidelines de uso acessivel para cada componente

### Etapa 5 — Handoff com A11y Specs
1. Anote tab order em cada tela
2. Especifique ARIA roles e attributes por componente
3. Documente screen reader announcements para acoes dinamicas
4. Especifique keyboard shortcuts e interactions
5. Inclua alt text para imagens e aria-label para icones

### Etapa 6 — Teste e QA de Acessibilidade
1. **Automatizado**: axe-core, Lighthouse, pa11y em CI/CD
2. **Manual — Keyboard**: Navegue toda a interface usando apenas teclado
3. **Manual — Screen reader**: Teste com VoiceOver (Mac), NVDA (Windows), TalkBack (Android)
4. **Manual — Zoom**: Teste com 200% zoom
5. **Com usuarios**: Testes de usabilidade com pessoas com deficiencia
6. **Audit periodico**: Auditoria completa WCAG a cada 6 meses

## Key Principles

- **A11y e responsabilidade de todos**: Nao so do "especialista em acessibilidade"
- **Shift-left**: Quanto mais cedo considerar, mais barato corrigir
- **Built-in > bolt-on**: Componentes acessiveis por padrao > fixes retroativos
- **WCAG como baseline**: AA e o minimo, AAA e o ideal para conteudo critico
- **Test with users**: Testes automatizados pegam ~30% dos problemas. Usuarios reais pegam o resto
- **Color independence**: Cor e um hint, nao o unico canal de informacao
- **Progressive enhancement**: Funciona sem JS, sem CSS, sem imagens como fallback

## Examples

### Exemplo 1 — Componente de Form Acessivel
Input com a11y built-in:
- `<label>` associado via `for` attribute
- `aria-describedby` vinculando helper text e error message
- `aria-invalid="true"` quando em estado de erro
- `aria-required="true"` para campos obrigatorios
- Focus ring visivel com `outline` (nao `outline: none`)
- Error message inclui icone + cor + texto (nao so cor)

### Exemplo 2 — Audit de Acessibilidade
Uma equipe rodou audit WCAG 2.1 AA e encontrou:
- 23 falhas de contraste (principalmente texto cinza em fundo branco)
- 12 componentes sem keyboard access (dropdowns, tooltips, modals)
- 8 imagens sem alt text
- 5 formularios sem labels programáticos
- 3 videos sem captions
Priorizaram: contraste (impacto alto, esforco baixo) como primeiro fix.

### Exemplo 3 — Integracao no CI/CD
Pipeline configurado com:
1. `axe-core` roda em todos os componentes do Storybook — bloqueia merge se critico
2. Lighthouse a11y score > 90 — warning se < 90, bloqueia se < 70
3. Teste de contraste automatizado em todas as combinacoes de tokens
Resultado: 0 novas falhas de a11y automatizaveis introduzidas em 6 meses.

## Common Pitfalls

- **"Vamos resolver a11y depois"**: Retrofit e 10-100x mais caro. Nunca e "depois"
- **Depender so de ferramentas**: Testes automatizados pegam ~30% dos problemas.
  Teste manual e com usuarios sao essenciais
- **Overlay solutions**: Widgets de acessibilidade que se sobrepoem a interface nao resolvem
  problemas estruturais e frequentemente pioram a experiencia
- **A11y = screen readers**: Acessibilidade inclui motor, cognitivo, baixa visao, auditivo,
  situacional. Nao e so screen reader
- **Compliance sem usabilidade**: Um site pode passar em todos os criterios WCAG e ainda
  ser inutilizavel para pessoas com deficiencia. Teste com usuarios reais
- **Focus invisible**: `outline: none` sem alternativa visivel e uma das falhas mais comuns
- **Assumir que "ninguem com deficiencia usa nosso produto"**: 15-20% da populacao mundial
  tem alguma forma de deficiencia

## Cross-References

- [component-spec-framework.md](component-spec-framework.md) — A11y section na spec
- [design-system-layer.md](design-system-layer.md) — Componentes acessiveis por padrao
- [ui-layer.md](ui-layer.md) — Decisoes visuais acessiveis
- [handoff-layer.md](handoff-layer.md) — A11y specs no handoff
- [usability-testing-framework.md](usability-testing-framework.md) — Testes com usuarios com deficiencia
- [malouf-design-quality-model.md](malouf-design-quality-model.md) — A11y como dimensao de qualidade
