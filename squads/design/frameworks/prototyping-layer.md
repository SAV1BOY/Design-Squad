# Prototyping Layer

## Metadata
- **Autor**: Design Squad
- **Categoria**: Stack Layer, Prototipagem, Validacao
- **Complexidade**: Media
- **Aplicacao**: Construir prototipos para validar design antes da implementacao
- **Ultima atualizacao**: 2026-03-06

## Concept

A Prototyping Layer e a sexta camada do stack de design, responsavel por transformar
conceitos de design em artefatos interativos que permitem validacao antes da implementacao
completa. Prototipos sao hipoteses de experiencia que podem ser testados com usuarios
reais a um custo significativamente menor que implementacao em codigo.

O principio central e: quanto mais cedo e barato voce falha, melhor. Prototipos existem
para revelar problemas enquanto corrigi-los ainda e barato. Cada nivel de fidelidade
(baixa, media, alta) responde a tipos diferentes de perguntas.

A camada aborda tres dimensoes: fidelidade (nivel de realismo), cenarios (o que testar)
e validacao (como avaliar resultados).

## When to Use

- Quando conceitos de design precisam ser validados antes de investir em desenvolvimento
- Quando stakeholders precisam ver e interagir com a ideia antes de aprovar
- Quando decisoes de fluxo ou interacao precisam ser testadas com usuarios
- Quando ha incerteza sobre a viabilidade de uma abordagem de design
- Quando a equipe de dev precisa entender comportamento esperado alem de specs estaticas
- Quando se comparam duas ou mais abordagens de design concorrentes

## How to Apply

### Dimensao 1 — Fidelidade
**Baixa fidelidade (Lo-fi)**
- Formato: Sketches em papel, wireframes clicaveis basicos
- Tempo: 1-4 horas
- Ferramentas: Papel, Figma lo-fi, Balsamiq
- Responde: "O fluxo faz sentido? A estrutura esta correta?"
- Quando: Fase inicial, multiplas opcoes para comparar

**Media fidelidade (Mid-fi)**
- Formato: Wireframes interativos com conteudo real
- Tempo: 1-3 dias
- Ferramentas: Figma prototyping, Axure
- Responde: "A experiencia funciona end-to-end? O conteudo e claro?"
- Quando: Apos validacao de conceito, antes de visual design

**Alta fidelidade (Hi-fi)**
- Formato: Prototipo com visual final, micro-interactions, dados reais
- Tempo: 3-7 dias
- Ferramentas: Figma avancado, ProtoPie, Framer, codigo (HTML/CSS/JS)
- Responde: "A experiencia final e satisfatoria? Os detalhes funcionam?"
- Quando: Validacao final pre-dev, demos para stakeholders

### Dimensao 2 — Cenarios de Teste
1. **Happy path**: O cenario ideal de uso — funciona como esperado?
2. **Error scenarios**: O que acontece quando algo da errado?
3. **Edge cases**: Dados extremos (muito longos, vazios, especiais)
4. **First-time use**: Experiencia sem contexto previo
5. **Expert use**: Experiencia de usuario frequente com atalhos
6. **Accessibility**: Experiencia com assistive technologies
7. **Cross-device**: Experiencia em diferentes tamanhos de tela

### Dimensao 3 — Validacao
1. **Teste de usabilidade moderado**: 5 usuarios, tarefas definidas, observacao
2. **Teste nao moderado**: Plataformas como Maze ou UserTesting, escala maior
3. **Guerilla testing**: Teste rapido com colegas ou pessoas disponiveis
4. **A/B prototyping**: Compare 2 versoes para determinar qual funciona melhor
5. **Expert review**: Heuristic evaluation por designers experientes
6. **Stakeholder walkthrough**: Demonstracao guiada para aprovadores

### Processo Recomendado
1. Defina a pergunta que o prototipo deve responder
2. Escolha o nivel de fidelidade minimo necessario para responder
3. Construa o prototipo focando apenas no que sera testado
4. Defina cenarios e tarefas de teste
5. Teste com 5 usuarios (suficiente para encontrar ~85% dos problemas)
6. Sintetize findings e itere no design
7. Repita se necessario com fidelidade maior

## Key Principles

- **Fidelidade minima viavel**: Use o menor nivel de fidelidade que responda sua pergunta
- **Descartabilidade**: Prototipos sao descartaveis por natureza. Nao se apegue
- **Cenarios sobre telas**: Teste cenarios completos, nao telas isoladas
- **Fail fast**: O objetivo e encontrar problemas, nao confirmar que "esta tudo certo"
- **5 usuarios sao suficientes**: Para testes qualitativos, 5 usuarios revelam a maioria dos problemas
- **Prototipo nao e spec**: Prototipos validam experiencia, specs documentam para dev
- **Itere rapidamente**: Teste -> findings -> ajuste -> re-teste em ciclos curtos

## Examples

### Exemplo 1 — Escada de Fidelidade
Projeto de redesign de checkout em 3 rodadas:
- Rodada 1 (lo-fi, 3h): 3 conceitos de fluxo em papel testados com 5 usuarios.
  Resultado: conceito B melhor, mas step 2 confuso. Descartados A e C.
- Rodada 2 (mid-fi, 2 dias): Conceito B refinado com conteudo real.
  Resultado: fluxo funciona, campo de CEP precisa de auto-complete.
- Rodada 3 (hi-fi, 4 dias): Visual final com micro-interactions.
  Resultado: aprovado com ajustes menores em copy.
Total: 7 dias de prototipagem preveniram semanas de retrabalho em dev.

### Exemplo 2 — A/B Prototyping
Duas abordagens para navegacao de dashboard:
- Versao A: Sidebar fixa com menu colapsavel
- Versao B: Top navigation com mega menu
Teste com 10 usuarios (5 por versao): Versao A foi 30% mais rapida para
encontrar itens do segundo nivel. Versao B foi preferida esteticamente.
Decisao: Sidebar (performance > preferencia estetica).

### Exemplo 3 — Prototipo em Codigo
Para testar drag-and-drop de reordenacao de itens (impossivel em Figma),
um dev construiu prototipo funcional em React em 1 dia.
Teste revelou que usuarios esperavam feedback visual durante o drag que
nao estava planejado. Ajuste adicionado ao spec antes da implementacao real.

## Common Pitfalls

- **Over-prototyping**: Prototipos de alta fidelidade para tudo e desperdicio.
  Reserve hi-fi para decisoes criticas e incertas
- **Prototipos como produto final**: Se o prototipo vira codigo de producao, qualidade sofre
- **Testar com a equipe, nao com usuarios**: Colegas sabem demais. Teste com usuarios reais
- **Sem pergunta definida**: Prototipo sem pergunta a responder e exercicio sem proposito
- **Apego ao prototipo**: Designers que se apegam ao prototipo resistem a findings negativos
- **Cenario unico**: Testar apenas o happy path esconde problemas reais
- **Nao documentar findings**: Insights de teste que nao sao documentados sao perdidos

## Cross-References

- [ux-layer.md](ux-layer.md) — Fluxos e wireframes como input para prototipos
- [ui-layer.md](ui-layer.md) — Visual aplicado em prototipos hi-fi
- [usability-testing-framework.md](usability-testing-framework.md) — Framework de teste de usabilidade
- [handoff-layer.md](handoff-layer.md) — Prototipos que informam handoff
- [mall-hot-potato-process.md](mall-hot-potato-process.md) — Prototipagem rapida em pares
- [frost-pattern-lab.md](frost-pattern-lab.md) — Componentes como blocos de prototipagem
