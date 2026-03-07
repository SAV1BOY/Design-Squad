# Handoff Communication

## Context

Frases prontas para comunicar entregas de design para desenvolvimento. O handoff é o
momento de maior risco de perda de informação — o que é óbvio para o designer pode ser
ambíguo para o desenvolvedor. Comunicação precisa, completa e estruturada no handoff
reduz retrabalho e builds trust entre as disciplinas.

**Aplicação:** Tickets, Slack, meetings de handoff, comments no Figma
**Tom:** Pragmatic Builder + System Thinker

## Phrases

### Anunciando handoff
- "Handoff pronto para [feature/tela]. Link do Figma: [link]. Specs detalhados no frame 'Handoff Notes'."
- "O design de [feature] está aprovado e pronto para desenvolvimento. Todos os estados estão especificados."
- "Compartilho o handoff de [feature]. Destaco [N] pontos que precisam de alinhamento técnico."
- "Specs finais após incorporar feedback da última design review. Changelog no comment fixado do Figma."

### Descrevendo o escopo
- "Esse handoff cobre: [lista de telas/componentes]. Não cobre: [o que não está incluído]."
- "São [N] telas novas + [M] alterações em telas existentes. Prioridade: [ordem sugerida]."
- "O fluxo completo tem [N] estados. Os críticos são: [lista]. Os edge cases são: [lista]."
- "Componentes novos necessários: [lista]. Componentes existentes reutilizados: [lista]."

### Especificando comportamento interativo
- "A transição entre telas é [tipo] com duração de [ms]. Respeitar prefers-reduced-motion."
- "O dropdown abre com click, não com hover. Fecha com click fora, Escape, ou seleção de item."
- "O scroll é infinito com loading trigger a [N]px do bottom. Skeleton loader durante fetch."
- "A validação do form é on-blur (campo a campo), não on-submit. Error summary no topo ao submeter."
- "O toast de feedback aparece no bottom-center, persiste por [N] segundos, dismiss com swipe ou click no X."

### Indicando tokens e referências
- "Todos os valores estão mapeados para tokens do design system. Tabela de referência no frame 'Tokens'."
- "A cor de fundo usa color-surface-primary, não hex direto. Consultar token list atualizada."
- "Spacing segue a escala padrão: 4/8/16/24/32/48/64. Nenhum valor custom neste handoff."
- "Tipografia: heading-lg para título, body-md para texto, caption-sm para metadata."

### Apontando áreas de atenção
- "Atenção especial para [área]: o comportamento muda entre desktop e mobile."
- "O truncate de texto neste card precisa de tooltip on hover/focus com o texto completo."
- "A imagem tem aspect-ratio fixo de 16:9. Usar object-fit: cover para imagens fora de proporção."
- "Este componente precisa funcionar com conteúdo dinâmico — testar com texto de 1 palavra e de 200 caracteres."

### Pedindo alinhamento técnico
- "Antes de implementar, preciso alinhar: (1) [questão técnica]. Podemos conversar em [horário]?"
- "Não tenho certeza se [interação] é viável com [tecnologia]. Qual a melhor abordagem?"
- "O protótipo mostra a interação ideal. Se não for possível, aceito [alternativa simplificada]."
- "Tenho dúvida sobre [aspecto técnico]. Prefiro alinhar antes do sprint planning para não estimar errado."

### Respondendo dúvidas de implementação
- "Boa pergunta. A intenção é [comportamento]. Se tecnicamente for melhor [alternativa], aceito."
- "O spec não cobre esse cenário. Minha recomendação é [sugestão]. Mas se vocês têm pattern melhor, sigam."
- "Atualizei o Figma com o cenário que faltava. Link direto: [link]."
- "Esse edge case não foi considerado. Vou adicionar o estado no Figma e atualizo até [horário]."

## Variations

- Em Slack: formato conciso com links diretos e bullets
- Em ticket: formato completo com todos os campos preenchidos
- Em reunião: walkthrough visual pelo Figma com Q&A ao vivo
- Em Figma comment: formato "[HANDOFF] [área]: [instrução]"

## When to Use

- Entrega formal de specs de design para o sprint
- Comunicação de novos componentes para o time de front-end
- Esclarecimento de dúvidas durante implementação
- QA visual — apontar discrepâncias entre spec e implementação
