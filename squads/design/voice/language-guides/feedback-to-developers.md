# Feedback to Developers

## Context

Guia de linguagem para comunicação do Design Squad com desenvolvedores — code reviews
de UI, apontamentos de QA visual, discussões de implementação e negociações de
viabilidade técnica. O objetivo é construir parceria produtiva, não relação adversarial.

Desenvolvedores são aliados na materialização do design. A comunicação deve ser
específica, reproduzível e respeitosa com as restrições técnicas. Dizer "está
diferente do Figma" sem especificar o que, onde e por que importa não ajuda ninguém.

**Aplicação:** Code reviews, QA visual, discussions em PRs, Slack com devs.
**Tom predominante:** Pragmatic Builder + System Thinker
**Frequência:** Contínua — durante todo o ciclo de desenvolvimento

## Do's

### Ser específico e mensurável
- "O padding do card está 12px, deveria ser 16px (token spacing-md)"
- "O border-radius do button está 4px, o token usa 8px (border-radius-md)"
- "A fonte do heading está 18px/24px, o spec é 20px/28px (heading-sm)"

### Referenciar tokens e specs
- "Token correto: color-text-primary (#1A1A1A), implementado: #333333"
- "Componente no Figma: [link direto para o frame]"
- "Spec completo na tabela de handoff: [link]"

### Classificar severidade
- **Blocker:** Impede a funcionalidade ou é inacessível (contraste, touch target)
- **Major:** Visivelmente diferente do spec e afeta a experiência
- **Minor:** Diferença sutil, perceptível em comparação direta
- **Polish:** Refinamento desejável, não bloqueia release

### Contextualizar por que importa
- "O touch target de 32px está abaixo do mínimo de 44px — difícil de tocar em mobile"
- "O truncate sem tooltip esconde informação crítica (nome do produto)"
- "A animação de 500ms causa lag perceptível em devices low-end"

### Oferecer flexibilidade na implementação
- "O efeito desejado é [X]. Se não for possível com CSS puro, aceito [alternativa]"
- "O ideal é lazy loading. Se o bundle ficar complexo, podemos simplificar para..."
- "A interação no Figma é aspiracional — qual a melhor forma de implementar isso?"

## Don'ts

### Linguagem vaga ou emocional
- "Tá feio" — não é acionável
- "Não é assim que eu desenhei" — pessoaliza demais
- "O feeling está errado" — não é mensurável

### Desconsiderar restrições técnicas
- Insistir em solução impossível sem ouvir alternativas
- Ignorar impacto de performance por purismo visual
- Exigir pixel-perfect em cenários dinâmicos (conteúdo variável)

### Apontar problemas sem propor solução
- "Está errado" — sem dizer o que e como corrigir
- "Refaz" — sem explicar o que precisa mudar
- "Olha o Figma" — sem identificar a discrepância específica

### Tom hierárquico ou condescendente
- "Isso é design básico" — desrespeita o conhecimento do dev
- "Eu sei que vocês não entendem de design, mas..." — arrogante
- "É só mudar isso aqui" — minimiza o esforço de implementação

### Feedback público desnecessário
- Criticar implementação em canal público quando DM resolvia
- Escalar antes de tentar resolver diretamente
- Usar screenshot de bug em apresentação sem contexto

## Templates

### Template de QA visual report
```
## QA Visual — [Feature/Tela] — [Data]

### Ambiente testado
- Browser: [Chrome 120 / Safari 17 / etc.]
- Viewport: [1440px / 768px / 375px]
- OS: [macOS / Windows / iOS / Android]

### Findings

#### [Blocker/Major/Minor/Polish] — [Descrição curta]
- **Esperado:** [valor/comportamento do spec]
- **Encontrado:** [valor/comportamento atual]
- **Token/Referência:** [token ou link do Figma]
- **Screenshot:** [comparação side-by-side]
```

### Template de comment em PR
```
[SEVERITY: Blocker | Major | Minor | Polish]
[ÁREA: Spacing | Color | Typography | Layout | Interaction | A11y]

Esperado: [spec]
Encontrado: [implementação atual]
Referência: [link Figma / token name]
Sugestão: [como resolver — se souber]
```

### Template de pedido de alinhamento técnico
```
Preciso de ajuda para entender a viabilidade de [interação/visual].
O comportamento desejado é: [descrição]
No Figma: [link]
Restrições que conheço: [se houver]
Alternativas que considerei: [se houver]
Podemos alinhar em [horário]?
```
