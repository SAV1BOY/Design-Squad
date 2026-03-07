# Handoff and Developer Collaboration



## Metadata

- **Categoria:** Design-Dev Workflow, Collaboration
- **Relevancia para o Squad:** Alta — processo critico de transicao design-engenharia
- **Ultima revisao:** 2026-03-06



## Summary

Handoff e o processo de transferir especificacoes de design para engenharia de forma que permita implementacao fiel e eficiente. O conceito de "handoff" esta evoluindo de entrega unidirecional para colaboracao continua — em vez de "designer entrega, dev implementa," o modelo moderno e "designer e dev trabalham juntos no componente."

Este documento cobre ferramentas, processos e best practices para minimizar o gap entre intencao de design e realidade de implementacao. O principio central e: quanto mais contexto o developer tem, melhor a implementacao.



## Key Concepts


### 1. Figma Dev Mode

Dev Mode transforma o Figma em ferramenta de spec para developers: inspect de propriedades CSS, exportacao de assets, medicoes automaticas, links para componentes do design system. Variables e tokens sao expostos como valores de desenvolvimento. Dev Mode e agora o canal primario de handoff.


### 2. Design Annotations

Alem do que Dev Mode mostra automaticamente, designers devem anotar: comportamento interativo (o que acontece ao clicar, hover, focus), responsive behavior (como adapta a breakpoints), condicoes especiais (loading, error, empty states), acessibilidade (focus order, aria labels). Annotations tornam o implicito explicito.


### 3. Component Spec Documents

Para componentes novos, criar spec document com: anatomia (partes), props (customizacoes), states (todos os estados visuais), behavior (interacao e transicoes), responsive (adaptacoes), accessibility (keyboard, screen reader). Esse documento e o contrato de implementacao.


### 4. Collaborative Design-Dev Sessions

Em vez de handoff unidirecional, conduzir sessoes onde designer e developer exploram o design juntos. O developer pergunta, o designer explica. Ambos identificam edge cases e trade-offs. Essas sessoes reduzem bugs de interpretacao e aceleram implementacao.


### 5. Design QA Process

Apos implementacao, designer revisa em staging/preview. Comparar implementacao com design — pixel-perfect nao e o objetivo, mas fidelidade a tokens, espacamento, estados e comportamento e. Feedback via ferramenta de annotation no preview (Marker.io, BugHerd) ou comments no PR.



## Application to Design Squad

- **Dev Mode como canal primario:** Todo handoff via Figma Dev Mode. Designers garantem que designs estao bem estruturados (auto layout, variables, component names) para que Dev Mode gere specs uteis.
- **Annotation checklist:** Antes de handoff, passar por checklist de annotations: interacoes, responsive, states, acessibilidade, edge cases. Spec sem annotation e spec incompleta.
- **Pairing sessions para novos componentes:** Para cada componente novo, agendar sessao de 30-60min de pairing entre designer e developer. Revisar spec juntos, identificar edge cases, alinhar expectativas.
- **Design QA sprint ritual:** Reservar tempo em cada sprint para design QA. Designer revisa implementacoes concluidas e fornece feedback antes de release.
- **Feedback loop documentado:** Usar ferramenta padrao para feedback de design QA (ex: comments no PR com screenshots comparativos). Rastrear taxa de "first-time right" como metrica de qualidade do handoff.



## Key Takeaways

1. **Handoff nao e entrega — e conversa.** Quanto mais designer e developer colaboram, menor o gap de interpretacao.

2. **Dev Mode reduziu mas nao eliminou a necessidade de annotations.** Comportamento, responsiveness e acessibilidade ainda precisam ser explicitados.

3. **Pairing sessions previnem bugs caros.** 30 minutos de conversa previnem dias de retrabalho.

4. **Design QA e responsabilidade do designer.** Se o designer nao revisou a implementacao, nao pode reclamar de infidelidade.

5. **"First-time right" e metrica de qualidade do handoff.** Se implementacoes frequentemente precisam de correcoes de design, o processo de handoff precisa melhorar.



## Cross-References

- [Figma Library Governance](figma-library-governance.md) — library bem estruturada facilita handoff
- [Storybook for Design Systems](storybook-for-design-systems.md) — verificacao de implementacao
- [Design That Scales — Mall](../books/mall-design-that-scales.md) — hot potato process
- [DesignOps Handbook — Malouf](../books/malouf-designops-handbook.md) — workflow ops
- [Design Tokens Standard](../standards/design-tokens-standard-notes.md) — tokens no handoff
