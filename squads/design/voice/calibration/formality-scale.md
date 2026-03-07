# Formality Scale

## Metadata

- **Categoria:** Calibração de Voz
- **Aplicação:** Ajustar formalidade da comunicação conforme contexto e canal
- **Última atualização:** 2026-03-06

## Description

A Formality Scale define 5 níveis de formalidade para a comunicação do Design Squad.
O nível correto depende do canal, da audiência e do propósito. Ser formal demais em
Slack cria distância desnecessária; ser informal demais em apresentação para C-level
compromete credibilidade.

No contexto brasileiro, a comunicação profissional tende a ser mais relacional que
em culturas anglo-saxãs. Isso significa que mesmo em contextos formais, um tom
humano e acessível é valorizado — sem perder profissionalismo.

## Scale

### Nível 1 — Casual
- **Registro:** Conversacional, direto, com humor pontual
- **Tratamento:** Primeiro nome, "você"
- **Canais:** Slack interno do time, DMs, daily standup
- **Pontuação:** Informal — emojis de reação aceitos, frases curtas
- **Exemplo:**
  - "Ficou massa o novo card. Só ajusta o spacing do footer que tá 12px, deveria ser 16."
  - "Quem tá livre pra pair na tela de settings? 30min resolve"
  - "Review pronta no Figma, link no thread"

### Nível 2 — Profissional Relaxado
- **Registro:** Claro e direto, mas com estrutura
- **Tratamento:** Primeiro nome, "você", eventualmente "pessoal"
- **Canais:** Slack com outros times, emails internos, retros
- **Pontuação:** Standard — frases completas, bullets para clareza
- **Exemplo:**
  - "Pessoal, compartilho o update da sprint de design. Entregamos 3 das 5 telas
    planejadas. As 2 restantes dependem do alinhamento de copy com marketing —
    reunião marcada para amanhã."
  - "O componente novo tá no Figma. Principais decisões documentadas no thread."

### Nível 3 — Profissional
- **Registro:** Estruturado, preciso, respeitoso
- **Tratamento:** Primeiro nome em conversa, cargo em apresentação formal
- **Canais:** Emails cross-team, documentação, design reviews formais
- **Pontuação:** Formal — parágrafos estruturados, sem abreviações
- **Exemplo:**
  - "Conforme alinhado na reunião de sprint planning, o time de design priorizou
    os 3 fluxos de maior impacto no NPS. O cronograma detalhado e as dependências
    estão documentados no link abaixo."
  - "Solicito revisão do documento de specs até sexta-feira para que possamos
    iniciar o desenvolvimento na sprint seguinte."

### Nível 4 — Formal
- **Registro:** Institucional, documentado, preciso
- **Tratamento:** Nome completo ou cargo quando apropriado
- **Canais:** Apresentações para liderança, reports trimestrais, propostas
- **Pontuação:** Alta formalidade — linguagem cuidada, dados precisos
- **Exemplo:**
  - "Apresentamos os resultados do Q1 do programa de Design System. A adoção
    atingiu 89% dos squads ativos, com redução mensurável de 34% no tempo de
    desenvolvimento de interfaces. O investimento planejado para Q2 foca em
    acessibilidade e internacionalização."

### Nível 5 — Institucional
- **Registro:** Oficial, representando a organização
- **Tratamento:** Formal, impessoal quando necessário
- **Canais:** Release notes públicas, blog posts, comunicação externa
- **Pontuação:** Máxima formalidade — revisão editorial obrigatória
- **Exemplo:**
  - "A versão 3.0 do Design System introduz suporte completo a WCAG 2.2 AA,
    dark mode nativo e tokens multi-plataforma. Consulte o guia de migração
    para atualizar seus projetos."

## Channel-Formality Matrix

| Canal                    | Nível Padrão | Range Aceitável |
|--------------------------|-------------|----------------|
| Slack — canal do time    | 1           | 1-2            |
| Slack — canal cross-team | 2           | 2-3            |
| Email interno            | 3           | 2-4            |
| Design review            | 3           | 2-3            |
| Apresentação para VP+    | 4           | 3-4            |
| Documentação pública     | 4           | 4-5            |
| Blog/Release notes       | 5           | 4-5            |

## Signals to Adjust

**Suba a formalidade quando:**
- O público inclui alguém 2+ níveis acima na hierarquia
- A comunicação será encaminhada ou referenciada futuramente
- O assunto é sensível (budget, headcount, performance)
- Há audiência externa (clientes, parceiros, imprensa)

**Desça a formalidade quando:**
- O grupo é pequeno e se conhece bem
- O objetivo é brainstorm ou exploração
- Velocidade importa mais que polish
- O tom formal está criando barreira de comunicação

## Cross-References

- `voice/calibration/audience-depth-scale.md` — Profundidade por audiência
- `voice/channel-adaptation/slack-design-comms.md` — Adaptação para Slack
- `voice/channel-adaptation/design-review-presentation.md` — Adaptação para reviews
