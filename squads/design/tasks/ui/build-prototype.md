# Build Prototype

## Metadata
- **Categoria:** UI
- **Complexidade:** Média-Alta
- **Tempo Estimado:** 3-8 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** ui, prototype, interaction-design, figma-prototype, testing

## Objective
Construir protótipos interativos que simulem a experiência real do produto para fins de teste com
usuários, validação com stakeholders e comunicação de design intent para engenharia. O nível de
fidelidade deve ser adequado ao objetivo: desde click-through básico até protótipos com micro-interactions.

## Prerequisites
- Mockups high-fidelity aprovados (para protótipos de alta fidelidade)
- Wireframes aprovados (para protótipos de baixa fidelidade)
- User flows documentados com todos os caminhos e edge cases
- Ferramenta de prototipação configurada (Figma, ProtoPie, Framer)
- Cenários de teste definidos (se o protótipo será usado em usability test)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UI Designer | Criar protótipo, definir transições e micro-interactions |
| UX Designer | Validar fluxos e garantir cobertura de cenários |
| UX Researcher | Definir cenários de teste e validar prototypability |
| Design Lead | Revisar qualidade e fidelidade do protótipo |
| Tech Lead | Avaliar viabilidade das animações e interações propostas |

## Frameworks
- **Fidelity Spectrum** — low (wireframe clickável) a high (pixel-perfect interativo)
- **Smart Animate (Figma)** — para transições suaves entre estados
- **Component Variants** — para simular interações com componentes do DS
- **Conditional Logic (ProtoPie)** — para protótipos com lógica condicional
- **Prototype Coverage Matrix** — para garantir cobertura de cenários

## Checklists
- [ ] Nível de fidelidade definido e justificado pelo objetivo
- [ ] Happy path completo e funcional
- [ ] Fluxos alternativos cobertos (mínimo 80% dos edge cases)
- [ ] Transições entre telas consistentes e realistas
- [ ] Estados de erro e feedback prototipados
- [ ] Loading states e skeleton screens incluídos
- [ ] Hotspots claramente definidos e sem dead ends
- [ ] Protótipo testado internamente antes de compartilhar
- [ ] Link de compartilhamento gerado e funcional
- [ ] Cenários de teste documentados (se para usability test)

## Steps
1. **Definir fidelidade e escopo** — Com base no objetivo (teste, stakeholder review, handoff),
   definir nível de fidelidade e quais fluxos serão prototipados.

2. **Preparar frames** — Duplicar mockups para o arquivo de protótipo. Garantir que todos os
   estados necessários estão como frames independentes.

3. **Conectar happy path** — Ligar telas do fluxo principal com interações e transições
   adequadas. Definir triggers (click, hover, drag) e animações.

4. **Prototipar estados interativos** — Usar component variants e interactive components para
   simular: toggles, dropdowns, modals, tooltips e form validation.

5. **Adicionar fluxos alternativos** — Prototipar caminhos de erro, estados vazios e fluxos
   secundários. Garantir que o usuário nunca chega a um dead end.

6. **Criar transições e micro-interactions** — Aplicar smart animate para transições suaves.
   Adicionar micro-interactions relevantes: loading, success, hover effects.

7. **Testar internamente** — Percorrer o protótipo completo simulando cada cenário de teste.
   Verificar: links quebrados, dead ends, transições estranhas e performance.

8. **Documentar cenários** — Se o protótipo será usado em usability test, documentar: cenário
   de contexto, tarefas, caminhos esperados e pontos de observação.

9. **Gerar link e compartilhar** — Criar link de compartilhamento com configurações adequadas
   (device frame, starting point, flow name). Testar em diferentes dispositivos.

## Output
- **Interactive Prototype** — Protótipo funcional cobrindo fluxos definidos
- **Prototype Map** — Diagrama mostrando telas e conexões do protótipo
- **Test Scenarios** — Cenários documentados (se para testing)
- **Formato:** Figma prototype link + documentação em Markdown
- **Nomenclatura:** `prototype-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UI Designer |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por ciclo de design/iteração |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/ui/` |

## Cross-References
- [UI Design High Fidelity](./ui-design-high-fidelity.md)
- [Wireframe Pack](../ux/wireframe-pack.md)
- [Run Usability Test](../research/run-usability-test.md)
- [Design Motion Specs](./design-motion-specs.md)
- [Dev Handoff](../handoff/dev-handoff.md)
