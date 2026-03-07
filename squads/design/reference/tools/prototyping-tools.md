# Prototyping Tools



## Metadata

- **Categoria:** Prototyping, Testing, Validation
- **Relevancia para o Squad:** Media-Alta — ferramentas para diferentes niveis de fidelidade
- **Ultima revisao:** 2026-03-06



## Summary

Prototyping tools permitem simular experiencias de uso antes da implementacao — desde sketches em papel ate prototipos interativos quase indistinguiveis do produto final. A escolha da ferramenta depende do nivel de fidelidade necessario, do publico do prototipo e do tempo disponivel.

Este documento mapeia ferramentas por nivel de fidelidade e caso de uso, ajudando o squad a escolher a ferramenta certa para cada situacao. O principio guia e: use a menor fidelidade que responde a pergunta de design.



## Key Concepts


### 1. Low-Fidelity (Paper, Whiteboard, FigJam)

Para explorar direcoes e testar conceitos basicos. Custo: minutos. Quando usar: inicio de projeto, design sprint, ideacao. Paper prototyping e surpreendentemente eficaz para testar fluxos e IA. FigJam para sketching digital colaborativo.


### 2. Mid-Fidelity (Figma Wireframes with Prototyping)

Wireframes clicaveis no Figma para testar fluxos, navegacao e arquitetura de informacao sem distracao visual. Custo: horas. Quando usar: validacao de fluxo antes de investir em visual design. Figma prototyping cobre a maioria dos casos.


### 3. High-Fidelity (Figma Full Prototype)

Mockups completos com interacao no Figma. Smart Animate para transicoes, Component interaction para estados, Variables para prototipagem condicional. Custo: dias. Quando usar: user testing final, apresentacao para stakeholders, validacao de microinteracoes.


### 4. Code Prototypes (React/HTML)

Para interacoes que Figma nao simula: animacoes complexas, data-driven interfaces, real API integration. Custo: dias a semanas. Quando usar: quando a fidelidade da interacao e critica para o teste e Figma nao e suficiente.


### 5. Specialized Tools

ProtoPie: microinteracoes complexas, hardware integration (gyroscope, sound). Principle: animacoes e transicoes detalhadas. Origami Studio: prototipos complexos com logica condicional. Framer: prototipos com codigo real.



## Application to Design Squad

- **Fidelity decision tree:** Antes de prototipar, perguntar: "Que pergunta preciso responder?" Se e sobre direcao, use low-fi. Se e sobre fluxo, use mid-fi. Se e sobre experiencia, use hi-fi.
- **Figma como default:** Para a maioria dos casos, Figma prototyping e suficiente. So escalar para outras ferramentas quando Figma nao consegue simular a interacao necessaria.
- **Prototipo descartavel:** Prototipos existem para aprender, nao para entregar. Nao invista em "perfeicao" de prototipo — invista em perfeição do que foi aprendido.
- **Test-ready prototypes:** Todo prototipo criado para teste deve ter: cenario de uso definido, tarefas para o participante, happy path completo e pelo menos um error state.
- **Prototype library:** Manter biblioteca de prototipos ja criados como referencia para novos projetos. Componentes de prototipo (flows, patterns) podem ser reutilizados.



## Key Takeaways

1. **Use a menor fidelidade que responde a pergunta.** Low-fi e rapido e suficiente para a maioria das validacoes iniciais.

2. **Figma cobre 80% dos casos.** So escale para ferramentas especializadas quando necessario.

3. **Prototipos sao descartaveis por design.** O valor e o aprendizado, nao o artefato.

4. **Fidelidade comunica estagio.** Low-fi convida feedback estrategico; hi-fi convida feedback tatico.

5. **Sem cenario de uso, o prototipo nao serve para teste.** Defina o que testar antes de como prototipar.



## Cross-References

- [Sprint — Knapp](../books/knapp-sprint.md) — prototipagem em um dia
- [Sketching UX — Buxton](../books/buxton-sketching-ux.md) — sketch como prototipagem
- [FigJam Workshops](figjam-workshops.md) — low-fi colaborativo
- [Figma Library Governance](figma-library-governance.md) — componentes para prototipagem
- [Research Tools](research-tools.md) — ferramentas de teste
