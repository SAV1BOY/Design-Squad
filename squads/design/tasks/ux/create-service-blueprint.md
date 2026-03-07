# Create Service Blueprint

## Metadata
- **Categoria:** UX
- **Complexidade:** Alta
- **Tempo Estimado:** 5-8 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** ux, service-blueprint, service-design, systems-thinking, backstage

## Objective
Criar um service blueprint que visualize a experiência do usuário em conjunto com os processos
de backstage, sistemas de suporte e pontos de interação entre front-stage e back-stage. O artefato
revela dependências ocultas, gargalos operacionais e oportunidades de melhoria sistêmica.

## Prerequisites
- Journey map do usuário disponível como referência
- Acesso a stakeholders de operações, engenharia e suporte
- Mapeamento de sistemas e integrações do produto
- Ferramenta de diagramação configurada (Miro, FigJam, Smaply)
- Entendimento dos processos internos que sustentam a experiência

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UX Designer | Facilitar mapeamento e criar blueprint visual |
| Tech Lead | Detalhar processos de backstage e dependências técnicas |
| Product Manager | Contextualizar regras de negócio e priorizar oportunidades |
| Customer Support Lead | Mapear processos de atendimento e escalação |
| Ops/Backend Engineer | Detalhar sistemas de suporte e integrações |
| Design Lead | Revisar e garantir actionability do blueprint |

## Frameworks
- **Service Blueprint (Shostack)** — modelo de 5 lanes padrão
- **Line of Interaction** — fronteira entre usuário e front-stage
- **Line of Visibility** — fronteira entre front-stage e back-stage
- **Line of Internal Interaction** — fronteira entre back-stage e suporte
- **Failure Point Analysis** — identificação de pontos de falha no serviço

## Checklists
- [ ] Journey map existente utilizado como base para as ações do usuário
- [ ] Physical evidence mapeada por touchpoint
- [ ] Front-stage actions documentadas (o que o usuário vê e interage)
- [ ] Back-stage actions mapeadas (processos invisíveis ao usuário)
- [ ] Support processes identificados (sistemas, databases, third-parties)
- [ ] Lines of interaction, visibility e internal interaction desenhadas
- [ ] Failure points identificados e classificados por risco
- [ ] Oportunidades de melhoria sistêmica documentadas
- [ ] Blueprint revisado por Tech Lead e Ops

## Steps
1. **Definir escopo** — Selecionar o serviço ou fluxo a ser mapeado. Delimitar início e fim do
   blueprint. Pode cobrir toda a jornada ou focar em um momento crítico.

2. **Mapear customer actions** — Usando o journey map como base, listar todas as ações do
   usuário em sequência cronológica na lane superior do blueprint.

3. **Documentar physical evidence** — Para cada touchpoint, registrar evidências físicas ou
   digitais que o usuário encontra: telas, emails, notificações, documentos.

4. **Mapear front-stage actions** — Documentar tudo que é visível ao usuário: interfaces,
   mensagens, interações com suporte humano, feedback do sistema.

5. **Mapear back-stage actions** — Com Tech Lead e Ops, documentar processos invisíveis ao
   usuário que sustentam cada front-stage action: processamento, validações, workflows.

6. **Identificar support processes** — Listar sistemas, databases, APIs, serviços terceiros e
   processos manuais que suportam as ações de back-stage.

7. **Desenhar linhas de separação** — Posicionar as três linhas horizontais que separam as lanes:
   interaction, visibility e internal interaction. Garantir coerência.

8. **Identificar failure points** — Analisar cada conexão entre lanes buscando: pontos de falha,
   gargalos, dependências frágeis e handoffs problemáticos.

9. **Mapear oportunidades** — Para cada failure point e gargalo, propor melhorias. Categorizar
   por: automação possível, melhoria de processo, nova feature, treinamento.

10. **Publicar e socializar** — Criar versão visual final do blueprint. Apresentar para
    stakeholders cross-funcionais e integrar oportunidades ao roadmap.

## Output
- **Service Blueprint** — Diagrama visual com 5+ lanes completas
- **Failure Point Analysis** — Lista de pontos de falha com risco e impacto
- **Improvement Opportunities** — Oportunidades categorizadas e priorizadas
- **Formato:** Miro/FigJam board + Markdown para documentação de findings
- **Nomenclatura:** `service-blueprint-[serviço]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UX Designer |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por serviço, revisão anual |
| Aprovadores | Design Lead, PM, Tech Lead |
| Repositório | `/squads/design/tasks/ux/` |

## Cross-References
- [Create Journey Map](./create-journey-map.md)
- [Design User Flows](./design-user-flows.md)
- [Create Personas or JTBD](./create-personas-or-jtbd.md)
- [Problem Definition](../discovery/problem-definition.md)
- [Cross-Squad Sync](../operations/cross-squad-sync.md)
