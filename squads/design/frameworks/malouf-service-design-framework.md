# Malouf Service Design Framework

## Metadata
- **Autor**: Dave Malouf
- **Categoria**: Service Design, Experience Design
- **Complexidade**: Alta
- **Aplicacao**: Projetar experiencias end-to-end que envolvem multiplos touchpoints
- **Ultima atualizacao**: 2026-03-06

## Concept

O Service Design Framework de Dave Malouf expande o escopo do design de interfaces
para o design de servicos completos, mapeando a experiencia do usuario atraves de
multiplos touchpoints — digitais e fisicos, frontstage e backstage.

A premissa e que usuarios nao experimentam "telas" — experimentam servicos. Um usuario
de e-commerce interage com: busca no Google, landing page, app, email de confirmacao,
SMS de rastreamento, entrega fisica, unboxing, suporte por chat. Cada touchpoint e
parte de um servico unico, e a experiencia e a soma de todos eles.

O framework usa tres ferramentas principais: Service Blueprint (mapa tecnico do servico),
Touchpoint Map (inventario de pontos de contato) e Backstage Operations (processos
internos que suportam a experiencia). Juntos, eles revelam gaps, redundancias e
oportunidades de melhoria que nao sao visiveis quando se olha apenas para uma tela.

## When to Use

- Quando a experiencia do usuario envolve multiplos canais e touchpoints
- Quando ha gaps entre diferentes etapas da jornada do usuario
- Quando equipes diferentes sao responsaveis por partes diferentes da experiencia
- Quando se redesenha uma jornada completa (onboarding, compra, suporte)
- Quando problemas de experiencia nao sao resolvidos por mudancas em telas individuais
- Quando a organizacao quer alinhar operacoes internas com experiencia do usuario

## How to Apply

### Ferramenta 1 — Service Blueprint
**Estrutura do blueprint em 5 camadas**:

1. **Physical Evidence**: Artefatos tangiveis que o usuario ve ou toca
   (email, app, embalagem, recibo, notificacao)

2. **Customer Actions**: Acoes que o usuario realiza em cada etapa
   (buscar, clicar, pagar, ligar, avaliar)

3. **Frontstage Interactions**: Interacoes visiveis para o usuario
   (interface do app, atendente de chat, email automatico)

4. **Backstage Interactions**: Processos internos nao visiveis
   (processamento de pedido, roteamento de suporte, geracao de relatorio)

5. **Support Processes**: Sistemas e infraestrutura que sustentam tudo
   (banco de dados, sistema de logistica, CRM, analytics)

**Como construir**:
1. Defina o escopo da jornada (inicio e fim)
2. Mapeie customer actions cronologicamente
3. Para cada action, identifique frontstage interactions
4. Para cada frontstage, mapeie backstage correspondente
5. Para cada backstage, identifique support processes
6. Marque "line of visibility" (o que o usuario ve vs nao ve)
7. Marque "line of interaction" (onde usuario interage diretamente)
8. Identifique pain points, wait times e failure points

### Ferramenta 2 — Touchpoint Map
1. Liste todos os touchpoints da jornada (digitais e fisicos)
2. Classifique por canal: web, app, email, SMS, telefone, presencial
3. Classifique por ownership: qual equipe controla cada touchpoint
4. Avalie qualidade atual de cada touchpoint (1-5)
5. Identifique gaps: momentos sem touchpoint onde deveria haver
6. Identifique redundancias: multiplos touchpoints competindo
7. Priorize melhorias por impacto na experiencia e viabilidade

### Ferramenta 3 — Backstage Operations
1. Para cada touchpoint frontstage, mapeie operacoes internas necessarias
2. Identifique handoffs entre equipes (onde informacao se perde)
3. Mapeie tempos de espera internos que afetam a experiencia
4. Identifique single points of failure
5. Proponha melhorias operacionais que impactam a experiencia do usuario

## Key Principles

- **Experiencia e holistica**: Usuarios nao percebem "canais" — percebem servico unico
- **Frontstage depende de backstage**: Interface bonita com operacoes quebradas gera frustacao
- **Touchpoints sao momentos da verdade**: Cada ponto de contato pode fazer ou quebrar a experiencia
- **Gaps sao oportunidades**: Momentos sem contato sao onde ansiedade cresce
- **Cross-team alignment**: Servico bom requer alinhamento entre equipes que normalmente nao conversam
- **Tempo e dimensao critica**: Wait times percebidos impactam satisfacao enormemente
- **Mapeie antes de projetar**: Entender o servico atual e prerequisito para melhora-lo

## Examples

### Exemplo 1 — Blueprint de Onboarding SaaS
Customer Actions: Signup -> Confirm email -> First login -> Setup -> First value

Descobertas do blueprint:
- Gap de 24h entre signup e email de confirmacao (backstage: fila de email congestionada)
- Tela de setup pedia informacoes que nao eram usadas por nenhum backstage process
- "First value" dependia de integracao com API externa com 30% de falha
Acoes: Corrigir fila de email, simplificar setup, criar fallback para integracao

### Exemplo 2 — Touchpoint Map de E-commerce
Touchpoints mapeados em jornada de compra:
1. Busca Google (Marketing owns) — Qualidade 4/5
2. Landing page (Product owns) — Qualidade 3/5
3. Pagina de produto (Product owns) — Qualidade 4/5
4. Checkout (Product owns) — Qualidade 2/5
5. Email confirmacao (Engineering owns) — Qualidade 3/5
6. SMS rastreamento (Logistics owns) — Qualidade 1/5
7. Entrega (Logistics owns) — Qualidade 3/5

Insight: Os touchpoints com menor qualidade (checkout e SMS) eram os de maior
ansiedade do usuario. Priorizacao reordenada com base nesse insight.

### Exemplo 3 — Workshop de Service Blueprint
Formato: 4 horas, 10 participantes (design, eng, ops, suporte, marketing).
Cada equipe mapeou sua camada. Ao sobrepor, descobriram 7 handoffs onde
informacao se perdia entre equipes, causando 40% dos tickets de suporte.
O workshop gerou roadmap de 6 meses para eliminar os gaps mais criticos.

## Common Pitfalls

- **Mapear demais**: Tentar blueprintar toda a experiencia de uma vez. Foque em uma
  jornada critica primeiro
- **Ignorar backstage**: Focar so no frontstage bonito sem resolver operacoes quebradas
- **Nao envolver operacoes**: Blueprint feito so por designers ignora realidade operacional
- **Mapa como artefato final**: O blueprint e ferramenta de analise, nao deliverable de parede
- **Touchpoints sem owner**: Se ninguem e responsavel por um touchpoint, ninguem melhora ele
- **Esquecer o tempo**: Blueprints sem dimensao temporal ignoram wait times e urgencias
- **Nivel de detalhe errado**: Detalhe demais obscurece padroes; detalhe de menos perde insights

## Cross-References

- [malouf-ux-strategy-framework.md](malouf-ux-strategy-framework.md) — Estrategia que guia service design
- [discovery-layer.md](discovery-layer.md) — Discovery como input para blueprints
- [ux-layer.md](ux-layer.md) — Fluxos e IA como parte do servico
- [measurement-layer.md](measurement-layer.md) — Instrumentacao por touchpoint
- [cross-platform-design-framework.md](cross-platform-design-framework.md) — Consistencia entre canais
- [user-onboarding-design-framework.md](user-onboarding-design-framework.md) — Onboarding como servico
