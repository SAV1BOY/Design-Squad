# Design to Code Handoff

## Metadata
- **Autor**: Design Squad
- **Categoria**: Handoff, Colaboracao, Specs
- **Complexidade**: Media
- **Aplicacao**: Garantir transicao fiel de design para implementacao com specs, tokens, QA e feedback
- **Ultima atualizacao**: 2026-03-06

## Concept

Design to Code Handoff e o framework detalhado para a transicao entre design e implementacao,
cobrindo quatro pilares: Specs (o que construir), Tokens (como referenciar decisoes visuais),
QA (como validar fidelidade) e Feedback (como iterar pos-implementacao).

Diferente de um handoff discreto ("aqui esta o Figma, boa sorte"), este framework propoe
um processo continuo de colaboracao onde handoff e uma fase, nao um momento. O designer
permanece envolvido durante toda a implementacao, e o dev tem acesso ao racional por tras
das decisoes de design.

O objetivo final e zero divergencia entre design e implementacao — ou pelo menos divergencia
consciente e documentada.

## When to Use

- Para cada feature ou componente que transita de design para implementacao
- Quando divergencias entre design e codigo sao frequentes
- Quando devs reclamam de specs incompletas ou ambiguas
- Quando designers reclamam que a implementacao nao corresponde ao design
- Quando se quer reduzir ciclos de QA visual
- Quando se estrutura o processo de colaboracao design-dev

## How to Apply

### Pilar 1 — Specs Completas
**Checklist de spec por feature**:
1. Layout e estrutura:
   - Grid e posicionamento de elementos
   - Espacamentos entre componentes (margins, paddings)
   - Alinhamentos e hierarquia visual
   - Comportamento responsivo em 3 breakpoints
2. Componentes e variantes:
   - Quais componentes do DS sao usados
   - Quais props/variantes de cada componente
   - Quais componentes precisam ser criados (com spec)
3. Estados completos:
   - Default, loading, error, empty, success
   - Hover, focus, active, disabled
   - Edge cases: texto longo, imagem ausente, lista vazia
4. Interacoes:
   - Click/tap behaviors e destinos
   - Transicoes e animacoes (duration, easing)
   - Keyboard interactions
   - Validacoes e feedback

**Formato de entrega**:
- Figma com frames organizados por estado e breakpoint
- Annotations com notas explicativas
- Video walkthrough de 5-10 min explicando decisoes-chave

### Pilar 2 — Token Mapping
1. Para cada propriedade visual, indique o token correspondente:
   - Background: `--color-surface-primary` (nao `#FFFFFF`)
   - Text: `--color-text-primary` (nao `#111827`)
   - Spacing: `--spacing-4` (nao `16px`)
   - Font: `--font-body-md` (nao `16px/24px Inter`)
2. Documente tokens novos que precisam ser criados
3. Valide que todos os tokens referenciados existem no DS
4. Forneca mapeamento em formato tabular ou como layer no Figma

### Pilar 3 — QA Visual
**Pre-QA (dev self-check)**:
1. Dev compara implementacao com design em split-screen
2. Verifica todos os estados (nao so default)
3. Testa em 3 breakpoints (mobile, tablet, desktop)
4. Verifica que tokens corretos estao sendo usados (inspecionar CSS)

**QA pelo designer**:
1. Revisar em staging/preview (nao em screenshot)
2. Interagir com o produto (nao so olhar)
3. Registrar divergencias com screenshot + anotacao
4. Classificar severidade: critico (funcional) vs minor (cosmetico)
5. Priorizar: criticos antes do merge, minor no backlog

**Visual regression automatizado**:
1. Configurar Chromatic, Percy ou similar no CI
2. Aprovar baselines para cada componente
3. Flags automaticas quando diff > threshold
4. Designer revisa diffs como parte do code review

### Pilar 4 — Feedback Loop
1. **Imediato**: Canal Slack/Teams para duvidas durante implementacao
2. **Sessao de walkthrough**: 15-30 min com designer antes do merge
3. **Post-launch review**: Verificar em producao 1 semana apos lancamento
4. **Retro de handoff**: A cada 2-4 semanas, avaliar o processo
   - O que deu certo? O que ficou ambiguo? O que faltou na spec?
5. **Melhorias de processo**: Incorporar aprendizados no processo

### Workflow Completo
```
Designer                          Dev
   |                                |
   |-- Spec + tokens + walkthrough-->|
   |                                |-- Implementa
   |<--- Duvidas durante impl ------|
   |--- Respostas + ajustes ------->|
   |                                |-- PR pronto
   |<--- QA visual em staging ------|
   |--- Feedback com screenshots -->|
   |                                |-- Fixes
   |<--- Re-review ------------------|
   |--- Sign-off ------------------>|
   |                                |-- Merge
   |<--- Post-launch review --------|
```

## Key Principles

- **Handoff como fase, nao momento**: Colaboracao continua, nao "entrega e esquece"
- **Specs eliminam adivinhacao**: Quanto mais explicita a spec, menos retrabalho
- **Tokens sao a lingua comum**: Designer e dev referenciam os mesmos tokens
- **QA e responsabilidade compartilhada**: Dev faz self-check, designer valida
- **Feedback rapido**: Dias entre implementacao e review geram context switch
- **Documentar divergencias**: Se algo nao pode ser implementado fielmente, documente por que
- **Processo evoluivel**: Cada retro de handoff melhora o processo

## Examples

### Exemplo 1 — Handoff de Feature Complexa
Feature: novo dashboard com 5 widgets interativos
- Spec: 42 frames no Figma (estados x breakpoints x edge cases)
- Tokens: planilha com 67 token mappings
- Walkthrough: video de 12 min + sessao ao vivo de 20 min
- QA: 2 rodadas — 8 feedbacks na primeira, 2 na segunda
- Timeline: spec (2 dias) + implementacao (5 dias) + QA (1 dia)
Divergencia final: 1 animacao ajustada por limitacao de performance (documentada)

### Exemplo 2 — Handoff Leve
Feature: ajuste de copy em 3 telas
- Spec: link para 3 frames no Figma com texto novo destacado
- Tokens: nenhum novo necessario
- QA: quick check de 5 min em staging
- Timeline: spec (15 min) + implementacao (30 min) + QA (5 min)

### Exemplo 3 — Metricas de Handoff
Uma equipe rastreou qualidade do handoff por 3 meses:
- Tempo medio de spec: 3.2h por feature (caiu para 2.1h com templates)
- Rodadas de QA: media 1.8 (caiu para 1.3 com self-check do dev)
- Divergencias criticas: media 0.4 por feature (caiu para 0.1)
- Satisfacao dev com specs: 7.2/10 (subiu para 8.6/10)

## Common Pitfalls

- **Spec incompleta**: Faltou um estado? Dev inventa ou espera — ambos ruins
- **Handoff sem walkthrough**: Figma sozinho nao comunica contexto e racional
- **QA tardio**: Revisar depois do merge multiplica custo de correcao
- **Feedback vago**: "Nao esta certo" nao e feedback. Especifique o que esta diferente
- **Perfeccionismo visual**: 1px off em elemento nao-critico nao justifica re-implementacao
- **Valores hardcoded**: Dev usa `#2563EB` em vez de `var(--color-primary)` — token drift
- **Nao fazer retro**: Repetir os mesmos problemas de handoff sprint apos sprint

## Cross-References

- [handoff-layer.md](handoff-layer.md) — Camada de handoff no stack
- [component-spec-framework.md](component-spec-framework.md) — Spec detalhada de componentes
- [design-token-architecture.md](design-token-architecture.md) — Tokens como base do handoff
- [mall-hot-potato-process.md](mall-hot-potato-process.md) — Alternativa de colaboracao continua
- [frost-frontend-style-guide.md](frost-frontend-style-guide.md) — Docs como referencia compartilhada
- [measurement-layer.md](measurement-layer.md) — Metricas de qualidade de handoff
