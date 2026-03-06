# Handoff Layer

## Metadata
- **Autor**: Design Squad
- **Categoria**: Stack Layer, Handoff, Colaboracao Design-Dev
- **Complexidade**: Media
- **Aplicacao**: Processo de transicao de design para implementacao
- **Ultima atualizacao**: 2026-03-06

## Concept

A Handoff Layer e a setima camada do stack de design, responsavel por garantir que o
trabalho de design seja traduzido fielmente em codigo. Engloba specs, assets, tokens,
documentacao tecnica e processo de QA visual.

O handoff perfeito seria desnecessario — designers e devs trabalhariam tao proximos que
nao haveria "entrega". Na realidade, algum grau de formalizacao e necessario, mesmo em
equipes altamente colaborativas, para garantir completude e rastreabilidade.

A camada endereca o gap historico entre "o que foi projetado" e "o que foi implementado",
fornecendo artefatos, processos e mecanismos de validacao que minimizam esse gap.

## When to Use

- Quando o design esta pronto para ser implementado por desenvolvedores
- Quando ha historico de divergencia entre design e implementacao
- Quando designers e devs nao conseguem trabalhar em pair o tempo todo
- Quando novos devs precisam implementar features sem acesso direto ao designer
- Quando se quer garantir qualidade visual em producao
- Quando QA precisa de referencia para validar implementacao

## How to Apply

### Artefato 1 — Design Specs
1. Para cada tela/componente, documente:
   - Espacamentos exatos (margins, paddings) em relacao ao grid
   - Tamanhos de tipografia, peso, line-height
   - Cores com referencia a tokens do design system
   - Tamanhos e proporcoes de elementos
   - Breakpoints e comportamento responsivo
2. Use ferramentas de inspect automatico (Figma Dev Mode)
3. Complemente com notas manuais onde automatico nao e suficiente
4. Inclua specs de interacao: o que acontece no click, hover, focus

### Artefato 2 — Assets
1. Exporte icones em SVG (vetorial, escalavel)
2. Exporte imagens em formatos otimizados (WebP, AVIF com fallback)
3. Forneca assets em multiplas resolucoes para telas retina (@2x, @3x)
4. Organize assets com nomenclatura consistente e previsivel
5. Mantenha assets versionados (nao sobrescreva, versione)

### Artefato 3 — Token Mapping
1. Para cada elemento visual, indique qual token usar (nao o valor bruto)
2. Exemplo: "background: var(--color-surface-primary)" nao "background: #FFFFFF"
3. Documente tokens que ainda nao existem e precisam ser criados
4. Valide que todos os tokens usados existem no design system atual

### Artefato 4 — Behavior Specs
1. Documente cada interacao:
   - Trigger: o que inicia a interacao (click, hover, scroll)
   - Action: o que acontece visualmente
   - Duration e easing: timing de animacoes
   - State changes: o que muda no estado do componente
2. Documente loading states, skeleton screens, transitions
3. Documente keyboard interactions e focus management
4. Use videos curtos ou GIFs para comportamentos complexos

### Processo de QA Visual
1. Dev implementa baseado nas specs
2. Dev faz self-review comparando implementacao com design
3. Designer faz QA visual em staging/preview environment
4. Feedback e registrado com screenshots comparativos (expected vs actual)
5. Ajustes sao feitos e re-verificados
6. Sign-off formal do designer antes de merge para producao

## Key Principles

- **Tokens sobre valores**: Sempre referencie tokens, nao valores brutos
- **Specs completas**: Cada estado, breakpoint e interacao deve estar documentado
- **QA e parte do handoff**: Handoff nao termina na entrega — termina na validacao
- **Colaboracao continua**: Specs nao substituem conversas. Mantenha canal aberto
- **Automacao onde possivel**: Use ferramentas de inspect, visual regression, diff
- **Definition of Done inclui fidelidade**: Feature nao esta "done" se o visual diverge
- **Feedback rapido**: QA visual deve acontecer em horas, nao em sprints

## Examples

### Exemplo 1 — Checklist de Handoff
Para cada feature, o designer completa:
- [ ] Todas as telas em estado default (mobile + desktop)
- [ ] Todos os estados de componentes (hover, focus, disabled, error, loading, empty)
- [ ] Specs de espacamento e tipografia documentadas
- [ ] Tokens mapeados para cada propriedade visual
- [ ] Assets exportados e organizados
- [ ] Behavior specs com duracoes e easings
- [ ] Edge cases documentados (texto longo, dados vazios, erro de rede)
- [ ] A11y annotations (tab order, ARIA roles, contraste)

### Exemplo 2 — QA Visual Eficiente
Uma equipe implementou QA visual em 3 passos:
1. Visual regression automatizada (Chromatic) detecta diferencas > 0.1%
2. Designer revisa diffs flagrados automaticamente (10 min/feature)
3. Ajustes sao feitos pelo dev e re-verificados no proximo build
Tempo medio de QA por feature: 20 minutos (antes era 2+ horas).

### Exemplo 3 — Handoff de Componente Complexo
Para um data table com sorting, filtering e pagination:
- Figma: 18 frames cobrindo todos os estados e combinacoes
- Notas: 12 annotations explicando comportamento condicional
- Video: 2 min de screencast mostrando interacoes esperadas
- Token map: 23 tokens referenciados com nomes e valores
- Edge cases: tabela vazia, 1 item, 1000 items, coluna com texto longo

## Common Pitfalls

- **Handoff como muro**: "Jogar por cima do muro" sem contexto gera retrabalho.
  Inclua uma sessao de walkthrough verbal
- **Specs incompletas**: Faltou o estado de erro? Dev vai inventar ou perguntar dias depois
- **Valores hardcoded**: Usar "#2563EB" em vez de "var(--color-primary-500)" cria
  divergencia quando tokens mudam
- **QA visual como afterthought**: Se QA so acontece depois do merge, corrigir e mais caro
- **Assets desorganizados**: Icones sem nomenclatura, imagens sem otimizacao, versoes
  misturadas criam confusao
- **Assumir que Figma e suficiente**: Figma Dev Mode ajuda mas nao substitui notas
  explicativas e walkthrough
- **Nao documentar o "por que"**: Specs dizem "o que", mas sem o "por que", devs nao
  conseguem tomar decisoes quando encontram restricoes tecnicas

## Cross-References

- [design-to-code-handoff.md](design-to-code-handoff.md) — Framework detalhado de handoff
- [component-spec-framework.md](component-spec-framework.md) — Spec por componente
- [design-token-architecture.md](design-token-architecture.md) — Tokens como lingua do handoff
- [prototyping-layer.md](prototyping-layer.md) — Prototipos que complementam specs
- [frost-frontend-style-guide.md](frost-frontend-style-guide.md) — Docs vivas como referencia
- [mall-hot-potato-process.md](mall-hot-potato-process.md) — Alternativa ao handoff discreto
