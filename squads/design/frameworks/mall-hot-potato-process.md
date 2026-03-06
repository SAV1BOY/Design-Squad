# Mall Hot Potato Process

## Metadata
- **Autor**: Dan Mall
- **Categoria**: Processo, Colaboracao Design-Dev
- **Complexidade**: Media
- **Aplicacao**: Equipes de design e desenvolvimento trabalhando em ciclos rapidos
- **Ultima atualizacao**: 2026-03-06

## Concept

O Hot Potato Process e uma abordagem de colaboracao entre designers e desenvolvedores
proposta por Dan Mall onde o trabalho e passado rapidamente entre as disciplinas em
ciclos muito curtos, como uma batata quente. Em vez do modelo tradicional waterfall
(designer finaliza -> entrega para dev -> dev implementa -> designer revisa), o hot
potato propoe que o artefato mude de maos multiplas vezes ao dia.

A metafora e intencional: ninguem fica segurando o trabalho por muito tempo. O designer
faz um sketch rapido, passa para o dev que implementa um prototipo basico, passa de
volta para o designer que refina, volta para o dev que ajusta — e assim por diante
ate a solucao convergir.

Esse modelo elimina o "big reveal" onde o designer apresenta um mockup finalizado e o
dev descobre que e tecnicamente inviavel ou extremamente custoso. Problemas sao
identificados e resolvidos em minutos, nao em dias.

## When to Use

- Quando o handoff tradicional esta causando retrabalho significativo
- Quando designers projetam coisas que devs nao conseguem implementar fielmente
- Quando devs implementam coisas que designers nao aprovam
- Quando o ciclo design -> dev -> review e longo demais (mais de 1 sprint)
- Quando a equipe quer adotar pair design-dev
- Quando componentes novos precisam ser criados rapidamente com alta qualidade

## How to Apply

### Setup Inicial
1. Forme pares ou trios (1 designer + 1-2 devs) que trabalham juntos
2. Garanta que ambos tem acesso as ferramentas do outro:
   - Designer tem acesso ao repositorio/Storybook
   - Dev tem acesso ao Figma/design tool
3. Defina sessoes dedicadas de hot potato (blocos de 2-4 horas)
4. Escolha um componente ou feature como escopo da sessao
5. Prepare o ambiente: mesma sala fisica ou call continua

### Ciclo Hot Potato
**Passe 1 — Designer (10-15 min)**
Sketch rapido do conceito no papel ou Figma em baixa fidelidade.
Foco em estrutura e hierarquia, nao em polish visual.
Passa para o dev.

**Passe 2 — Dev (15-20 min)**
Implementa um prototipo funcional basico com HTML/CSS.
Identifica restricoes tecnicas e oportunidades.
Passa de volta para o designer.

**Passe 3 — Designer (10-15 min)**
Refina baseado no que viu implementado. Ajusta espacamentos,
tipografia, estados interativos. Passa para o dev.

**Passe 4 — Dev (15-20 min)**
Implementa refinamentos. Adiciona responsividade e estados.
Mostra resultado no browser. Passa para o designer.

**Passe 5+ — Repeticao**
Continua ate ambos estarem satisfeitos com o resultado.
Tipicamente 4-8 passes por componente.

### Finalizacao
1. Revisar o resultado juntos no browser em diferentes viewports
2. Documentar decisoes tomadas durante o processo
3. Criar spec final baseada no que foi implementado (nao no mockup original)
4. Adicionar ao design system se o componente for reutilizavel
5. Retro rapida: o que funcionou, o que melhorar no proximo ciclo

## Key Principles

- **Velocidade sobre perfeicao**: Cada passe deve ser rapido e imperfeiito
- **Co-autoria**: O resultado final e de ambos, nao "design do designer" ou "codigo do dev"
- **Browser como canvas**: O browser e o ambiente real, mockups sao rascunhos temporarios
- **Restricoes como input**: Limitacoes tecnicas informam decisoes de design em tempo real
- **Confianca mutua**: Cada pessoa confia que a outra vai melhorar o que recebeu
- **Ego reduzido**: Ninguem e dono do artefato — e um trabalho compartilhado
- **Convergencia natural**: A solucao converge organicamente em vez de ser "entregue pronta"

## Examples

### Exemplo 1 — Componente de Navigation
Um designer e um dev usaram hot potato para criar uma navegacao responsiva:
- Passe 1: Designer sketcha nav horizontal com dropdown no desktop
- Passe 2: Dev implementa com flexbox, percebe que items nao cabem em tablet
- Passe 3: Designer propoe priority+ pattern (overflow menu)
- Passe 4: Dev implementa priority+ com resize observer
- Passe 5: Designer refina transicoes e espacamentos
- Passe 6: Dev adiciona keyboard navigation e ARIA

Total: 2.5 horas. Estimativa anterior no modelo waterfall: 2 sprints.

### Exemplo 2 — Hot Potato Remoto
Uma equipe distribuida adaptou o processo para remoto:
- Usaram VS Code Live Share para co-editar codigo em tempo real
- Figma para sketches rapidos compartilhados
- Call continua no Google Meet durante os blocos de hot potato
- Commits frequentes com mensagens descritivas do passe
Funcionalidade identica ao presencial, com 10-15% mais tempo por passe.

### Exemplo 3 — Escala do Processo
Uma equipe de 12 pessoas (4 designers, 8 devs) adotou hot potato:
- Formaram 4 pares fixos (1 designer + 2 devs alternando)
- Blocos de hot potato toda terca e quinta, 14h-17h
- Em 2 meses, criaram 28 componentes novos para o design system
- Retrabalho pos-handoff reduziu de 35% para 8%
- Satisfacao da equipe com o processo de colaboracao subiu de 5.2/10 para 8.7/10

## Common Pitfalls

- **Passes muito longos**: Se alguem fica mais de 30 minutos com a "batata", o processo
  perde eficacia. Mantenha passes curtos e frequentes
- **Falta de dedicacao**: Hot potato requer atencao total. Nao funciona se as pessoas
  estao fazendo outras coisas em paralelo
- **Assimetria de skills**: Se o designer nao entende nada de codigo ou o dev nada de
  design, os passes sao ineficientes. Invista em cross-skilling minimo
- **Querer polish no passe 1**: O primeiro sketch deve ser crude. Perfecionismo no inicio
  mata a velocidade
- **Nao documentar decisoes**: No calor do processo, decisoes sao tomadas rapidamente.
  Se nao documentadas, serao esquecidas e questionadas depois
- **Forcar em todo tipo de trabalho**: Hot potato funciona melhor para componentes e features
  de UI. Nao e ideal para research, estrategia ou arquitetura
- **Egos no caminho**: Se designer ou dev se sentem "donos" do resultado e resistem
  a mudancas do outro, o processo nao funciona

## Cross-References

- [frost-death-of-the-page.md](frost-death-of-the-page.md) — Trabalho component-centric que viabiliza hot potato
- [frost-pattern-lab.md](frost-pattern-lab.md) — Ambiente compartilhado para os passes
- [mall-design-that-scales.md](mall-design-that-scales.md) — Hot potato como pratica que escala
- [handoff-layer.md](handoff-layer.md) — Hot potato como alternativa ao handoff tradicional
- [design-to-code-handoff.md](design-to-code-handoff.md) — Handoff continuo vs discreto
- [prototyping-layer.md](prototyping-layer.md) — Browser como ambiente de prototipagem
