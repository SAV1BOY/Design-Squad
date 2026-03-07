# Healthcare.gov Launch — Lições de UX e Design

> Arquivo de lições aprendidas · Design Squad

---

## Context / Contexto

O Healthcare.gov foi lançado em 1 de outubro de 2013 como o marketplace
federal de seguros de saúde do Affordable Care Act (Obamacare). O site
deveria permitir que milhões de americanos comparassem e adquirissem planos
de saúde. O lançamento foi um desastre técnico e de experiência do usuário
que se tornou referência mundial em como não lançar um produto digital.

During the first week, only 1% of visitors were able to successfully create
an account and enroll. The site crashed repeatedly, displayed cryptic error
messages, and required users to complete a lengthy registration before even
browsing available plans. The estimated cost exceeded $500 million, making
it one of the most expensive website failures in history.

## What Went Wrong / O Que Deu Errado

### 1. Registration Wall antes de Valor
- O site exigia criação de conta completa (com verificação de identidade)
  antes de permitir que usuários vissem planos disponíveis.
- Isso violava o princípio fundamental de "mostrar valor antes de pedir
  investimento" — users had no motivation to endure a painful signup.
- Comparação: sites de e-commerce permitem browsing antes de checkout.

### 2. Formulários Monumentais sem Progressive Disclosure
- O processo de inscrição tinha dezenas de campos obrigatórios apresentados
  em sequência, sem indicação clara de progresso ou tempo estimado.
- Não havia salvamento de progresso — se o sistema falhasse (e falhava
  frequentemente), o usuário perdia tudo e precisava recomeçar.
- Campos pediam informações que os usuários não tinham à mão (números de
  documentos, dados fiscais específicos).

### 3. Mensagens de Erro Inúteis
- Erros técnicos eram exibidos como códigos genéricos sem orientação.
- "An error has occurred" sem explicar o que aconteceu nem o que fazer.
- Nenhuma diferenciação entre erro do usuário e erro do sistema.
- Sem sugestão de próximos passos ou canais alternativos de atendimento.

### 4. Falta de Testes de Carga e Stress Testing
- O sistema não foi testado para o volume real de acessos simultâneos.
- Estimativas de tráfego foram subestimadas por ordens de magnitude.
- Não havia degradação graceful — o sistema falhava completamente em vez
  de oferecer experiência reduzida.

### 5. Ausência de Design System e Consistência
- Múltiplas equipes e contractors desenvolveram partes diferentes do site
  sem design system unificado.
- Padrões de interação variavam entre seções, aumentando carga cognitiva.
- Não havia componentes reutilizáveis — cada equipe reinventava soluções.

### 6. Acessibilidade como Afterthought
- O site inicial não atendia WCAG guidelines adequadamente.
- Screen readers tinham dificuldade com formulários dinâmicos.
- Contraste de cores e tamanho de fonte insuficientes para público idoso
  (um dos principais grupos-alvo do programa).

## Design Lessons / Lições de Design

1. **Value first, registration second** — Permita que usuários explorem e
   entendam o valor antes de exigir qualquer compromisso.

2. **Progressive disclosure em formulários complexos** — Quebre processos
   longos em etapas gerenciáveis com progresso visível e salvamento.

3. **Error messages são interface, não log** — Mensagens de erro devem
   ser humanas, específicas e acionáveis. Sempre incluir próximo passo.

4. **Graceful degradation > hard failure** — Quando o sistema está sob
   stress, ofereça experiência reduzida em vez de falha total.

5. **Design system é infraestrutura, não luxo** — Projetos multi-equipe
   precisam de componentes e padrões compartilhados desde o início.

6. **Acessibilidade desde o dia zero** — Especialmente quando o público-
   alvo inclui populações vulneráveis (idosos, baixa literacia digital).

7. **Teste com volume real** — Load testing com dados realistas é tão
   importante quanto usability testing.

## How to Avoid / Como Evitar

- [ ] Permitir browsing anônimo para exploração antes de exigir registro
- [ ] Implementar save-and-resume em qualquer formulário com mais de 5 campos
- [ ] Criar biblioteca de mensagens de erro com tom humano e próximos passos
- [ ] Realizar load testing com 2-3x o volume esperado de pico
- [ ] Estabelecer design system compartilhado antes do desenvolvimento
- [ ] Incluir auditoria de acessibilidade (WCAG AA) no definition of done
- [ ] Planejar graceful degradation para cenários de alta carga
- [ ] Testar com usuários do público-alvo real (não apenas tech-savvy testers)

## Cross-References / Referências Cruzadas

- `../../lib/patterns/error-message-patterns.md` — Padrões de erro
- `../../lib/patterns/loading-patterns.md` — Padrões de loading e fallback
- `../../lib/patterns/progressive-disclosure-patterns.md` — Disclosure gradual
- `../../lib/components/form-component-snippets.md` — Componentes de form
- `../../lib/utilities/a11y-compliance-rubric.md` — Rubrica de acessibilidade
- `../../lib/taxonomies/a11y-issue-taxonomy.md` — Taxonomia de issues a11y
- `../../data/registries/lessons-learned-registry.yaml` — Registro de lições
- `./a11y-lawsuits-cases.md` — Casos de processos por acessibilidade
