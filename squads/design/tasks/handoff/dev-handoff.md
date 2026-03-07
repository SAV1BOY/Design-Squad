# Dev Handoff

## Metadata
- **Categoria:** Handoff
- **Complexidade:** Média-Alta
- **Tempo Estimado:** 2-5 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** handoff, dev, specs, engineering, implementation, figma-dev-mode

## Objective
Preparar e entregar especificações de design completas para a equipe de engenharia, garantindo
que todas as informações necessárias para implementação estão documentadas: layouts, comportamentos,
estados, tokens, assets, microcopy e critérios de aceite de design.

## Prerequisites
- Mockups high-fidelity aprovados pelo Design Lead
- Protótipo interativo disponível para referência
- Microcopy aprovado e aplicado nos mockups
- Design system components utilizados e documentados
- Figma Dev Mode configurado para o arquivo

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UI Designer | Preparar specs, organizar arquivo e conduzir walkthrough |
| UX Designer | Documentar fluxos, edge cases e regras de negócio |
| Frontend Engineer | Participar do walkthrough, tirar dúvidas e estimar |
| Design Lead | Aprovar completude do handoff antes da entrega |
| QA Engineer | Revisar critérios de aceite e planejar testes |

## Frameworks
- **Figma Dev Mode** — specs automatizadas de medidas, cores, tipografia
- **Design Spec Document** — documento suplementar com comportamentos e regras
- **Acceptance Criteria (Design)** — critérios visuais e de interação para QA
- **Asset Export Checklist** — lista de assets a serem exportados (icons, images)
- **Handoff Walkthrough** — sessão ao vivo de review spec com eng

## Checklists
- [ ] Arquivo Figma organizado com naming padronizado e páginas claras
- [ ] Dev Mode ativado e annotations adicionadas
- [ ] Todos os estados de componentes documentados em uma única página
- [ ] Fluxos de interação anotados (triggers, transições, condições)
- [ ] Edge cases e estados de erro documentados
- [ ] Breakpoints responsive incluídos com behavior notes
- [ ] Assets exportáveis marcados (icons em SVG, images em WebP/PNG)
- [ ] Microcopy final confirmado em todas as telas
- [ ] Walkthrough session agendado e conduzido com eng
- [ ] Dúvidas da eng documentadas e respondidas

## Steps
1. **Organizar arquivo Figma** — Estruturar páginas por fluxo, nomear frames consistentemente,
   agrupar variantes de estado e limpar layers desnecessários.

2. **Ativar Dev Mode e annotations** — Habilitar Dev Mode. Adicionar annotations explicativas
   em pontos que precisam de contexto adicional para implementação.

3. **Documentar estados e interações** — Criar página dedicada com todos os estados por
   componente. Anotar: trigger (click, hover), animação, condição de visibilidade.

4. **Documentar edge cases** — Listar cenários especiais: textos longos (truncation), dados
   ausentes (empty states), erros de API, offline mode, primeiro acesso.

5. **Especificar responsive behavior** — Para cada breakpoint, documentar: o que muda, como
   componentes se reorganizam e quais elementos são hidden/shown.

6. **Preparar assets** — Marcar icons para export em SVG. Preparar images em formatos adequados
   (WebP, PNG). Garantir que assets estão otimizados.

7. **Redigir design acceptance criteria** — Para cada tela, escrever critérios mensuráveis de
   aceite: alinhamento, espaçamento, cores, comportamentos e transições.

8. **Conduzir handoff walkthrough** — Sessão ao vivo de 45-60 minutos com eng. Percorrer cada
   fluxo explicando decisões, comportamentos e respondendo dúvidas.

9. **Documentar Q&A** — Registrar todas as dúvidas levantadas pela eng durante o walkthrough.
   Responder pendências em até 24h e atualizar specs se necessário.

10. **Manter suporte contínuo** — Durante a implementação, permanecer disponível para dúvidas.
    Revisar implementação no PR/staging antes de considerar o handoff concluído.

## Output
- **Figma Spec File** — Arquivo organizado com Dev Mode e annotations
- **Design Spec Document** — Documento suplementar com behaviors e edge cases
- **Acceptance Criteria** — Critérios de aceite visuais e de interação
- **Formato:** Figma file + Markdown + exported assets
- **Nomenclatura:** `handoff-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UI Designer |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por feature ou sprint |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/handoff/` |

## Cross-References
- [UI Design High Fidelity](../ui/ui-design-high-fidelity.md)
- [Build Prototype](../ui/build-prototype.md)
- [QA with Engineering](./qa-with-engineering.md)
- [Post-Release Review](./post-release-review.md)
- [Handoff Review](../review/handoff-review.md)
- [Design Responsive Layouts](../ui/design-responsive-layouts.md)
