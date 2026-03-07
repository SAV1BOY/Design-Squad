# Design That Scales — Dan Mall



## Metadata

- **Autor:** Dan Mall
- **Publicacao:** 2022
- **Categoria:** Design Systems, Design Operations
- **Relevancia para o Squad:** Alta — governança e escalabilidade de design systems
- **Ultima revisao:** 2026-03-06



## Summary

Design That Scales aborda o desafio de criar e manter design systems em organizações reais. Dan Mall parte da premissa de que o problema principal não é técnico, mas organizacional — como conseguir adoção, manter qualidade e escalar sem criar burocracia paralisante. O livro apresenta frameworks práticos para governança, contribuição distribuída e mensuração de valor de design systems.

Mall argumenta que design systems falham não por falta de componentes, mas por falta de modelo operacional claro. Ele propõe uma abordagem onde o design system é tratado como produto interno, com roadmap, stakeholders e métricas de sucesso próprias. O livro detalha como estruturar equipes (centralized, federated, hybrid), como gerenciar contribuições de múltiplos times e como medir o impacto real do sistema na velocidade e qualidade do produto.

A obra também explora a relação entre design system e brand, mostrando como manter flexibilidade criativa dentro de um sistema estruturado, e como negociar com stakeholders que veem o sistema como limitação em vez de habilitador.



## Key Concepts


### 1. Design System as Product

O design system deve ser tratado como um produto interno com seu próprio product owner, backlog, roadmap e métricas. Isso significa ter uma equipe dedicada (mesmo que parcial), ciclos de release, changelog e canais de feedback dos "clientes" internos — os squads que consomem o sistema.


### 2. Governance Models (Centralized, Federated, Hybrid)

Mall detalha três modelos de governança: centralizado (uma equipe controla tudo), federado (cada squad contribui livremente) e híbrido (equipe core define padrões, squads contribuem seguindo guidelines). O modelo híbrido é recomendado para a maioria das organizações, equilibrando consistência e velocidade.


### 3. Contribution Model

Um framework claro para como novos componentes entram no sistema: proposta, revisão, implementação, documentação e publicação. Mall propõe um "contribution agreement" que define responsabilidades de quem propõe e de quem aprova.


### 4. Measuring Design System Value

Métricas de adoção (% de componentes do sistema usados vs. custom), velocidade (tempo para entregar features com vs. sem sistema), consistência (variações não-intencionais detectadas) e satisfação dos times consumidores. Mall alerta contra métricas de vaidade como "número de componentes na library."


### 5. Hot Potato Process

Em vez do handoff linear (designer entrega para dev), Mall propõe um processo onde o artefato vai e volta entre designer e dev em iterações rápidas — como uma batata quente. Isso reduz gaps de interpretação e acelera a convergência entre design e código.



## Application to Design Squad

- **Modelo de governança:** Implementar o modelo híbrido — squad de design system define tokens, componentes core e guidelines; squads de produto propõem extensões seguindo o contribution model.
- **Design System como produto:** Manter backlog dedicado para o design system, com priorização baseada no impacto nos squads consumidores. Conduzir "office hours" semanais para suporte.
- **Métricas de adoção:** Rastrear mensalmente a taxa de adoção do sistema por squad e a redução de componentes custom. Usar esses dados para justificar investimento contínuo.
- **Hot Potato com engenharia:** Adotar ciclos rápidos de ida-e-volta com developers durante a criação de novos componentes, em vez de entregar specs finalizados.
- **Contribution agreement:** Documentar critérios claros para novos componentes (quando cria novo vs. quando compõe a partir de existentes).



## Key Takeaways

1. **Governança clara é mais importante que componentes bonitos.** Um sistema com poucos componentes mas modelo operacional sólido supera uma library enorme sem processo de manutenção.

2. **Trate o design system como produto, não como projeto.** Projetos terminam; produtos evoluem. O design system precisa de investimento contínuo e dono claro.

3. **Meça impacto, não output.** O número de componentes na library é irrelevante se os squads não os adotam. Foque em métricas de adoção e velocidade.

4. **O modelo híbrido equilibra controle e autonomia.** Nem tudo centralizado (burocracia) nem tudo federado (caos). Core team define guardrails, squads contribuem dentro deles.

5. **Flexibilidade intencional preserva criatividade.** O sistema deve ter pontos de extensão claros onde variação é esperada e bem-vinda.



## Cross-References

- [Atomic Design — Frost](frost-atomic-design.md) — fundamento teórico para a arquitetura de componentes
- [Design Systems — Kholmatova](kholmatova-design-systems.md) — linguagem de padrões como complemento
- [Design Systems Handbook — Suarez](suarez-design-systems-handbook.md) — visão prática da implementação
- [DesignOps Handbook — Malouf](malouf-designops-handbook.md) — operação de design como disciplina
- [Figma Library Governance](../tools/figma-library-governance.md) — governança aplicada ao Figma
