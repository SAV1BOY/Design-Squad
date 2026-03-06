# UX Audit Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** UX Evaluation
- **Version:** 1.0.0
- **Owner Agent:** UX Audit Agent

## Objective
Assegurar que auditorias de UX sejam conduzidas de forma sistematica, cobrindo todos os aspectos relevantes da experiencia do usuario.
O checklist garante consistencia entre diferentes auditorias e auditores.

## When to Apply
- Ao iniciar uma auditoria de UX em produto existente.
- Durante revisoes periodicas de qualidade de experiencia.
- Antes de grandes redesigns para estabelecer baseline.

## Criteria
- [ ] O escopo da auditoria esta claramente definido com as areas e flows a serem avaliados
- [ ] Os heuristic principles utilizados estao documentados (ex: Nielsen, Shneiderman)
- [ ] Cada problema encontrado possui screenshot ou recording como evidencia
- [ ] Os problemas estao classificados por severity (critico, major, minor)
- [ ] Cada finding possui descricao do impacto no usuario
- [ ] As recomendacoes de melhoria sao actionable e especificas
- [ ] Os competitive benchmarks relevantes foram consultados
- [ ] A auditoria cobre os principais user flows end-to-end
- [ ] Aspectos de accessibility foram avaliados conforme WCAG guidelines
- [ ] Performance percebida (perceived performance) foi considerada
- [ ] A consistencia visual e de interacao entre telas foi verificada
- [ ] O estado de error handling e empty states foi avaliado
- [ ] A experiencia em diferentes devices e breakpoints foi testada
- [ ] Um executive summary com principais findings esta presente
- [ ] As metricas quantitativas disponiveis (analytics, NPS) foram correlacionadas
- [ ] O plano de priorizacao de fixes esta documentado com effort vs impact

## Severity Guide

### Critico
- Auditoria sem evidencias visuais dos problemas encontrados.
- Findings sem classificacao de severidade.
- Escopo da auditoria nao definido.

### Major
- Ausencia de recomendacoes actionable para os problemas.
- Falta de avaliacao de accessibility.
- Nenhum competitive benchmark consultado.

### Minor
- Executive summary ausente mas findings bem documentados.
- Formatacao inconsistente entre findings.
- Falta de correlacao com metricas quantitativas.

## Cross-References
- [Accessibility Quality](accessibility-quality.md)
- [Usability Test Quality](usability-test-quality.md)
- [Performance UX Quality](performance-ux-quality.md)
- [Responsive Breakpoints Quality](responsive-breakpoints-quality.md)
- [Design Critique Quality](design-critique-quality.md)
