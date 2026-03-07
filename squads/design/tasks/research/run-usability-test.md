# Run Usability Test

## Metadata
- **Categoria:** Research
- **Complexidade:** Alta
- **Tempo Estimado:** 5-8 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** research, usability-testing, evaluative, task-analysis, prototype-testing

## Objective
Planejar e executar testes de usabilidade moderados ou não-moderados para avaliar a eficácia,
eficiência e satisfação de um design (protótipo ou produto em produção). Os resultados identificam
problemas de usabilidade e geram recomendações acionáveis para iteração.

## Prerequisites
- Protótipo funcional ou acesso ao produto em staging/produção
- Objetivo do teste claramente definido (o que será avaliado)
- Tarefas-alvo mapeadas com critérios de sucesso
- Ferramenta de teste configurada (Maze, UserTesting, Lookback ou presencial)
- Perfil de participante definido e recrutamento iniciado

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UX Researcher | Planejar protocolo, moderar sessões e sintetizar findings |
| UX/UI Designer | Preparar protótipo, observar sessões e iterar com base nos achados |
| Note-taker | Registrar comportamentos, erros e verbalizações em tempo real |
| Product Manager | Definir tarefas críticas e participar como observer |
| Design Lead | Revisar plano de teste e priorizar findings para ação |

## Frameworks
- **Think-Aloud Protocol** — para capturar raciocínio do participante durante tarefas
- **Task Success Rate** — métrica de eficácia (completion rate)
- **Time on Task** — métrica de eficiência
- **SUS (System Usability Scale)** — questionário pós-teste padronizado
- **Severity Rating (Nielsen)** — classificação de problemas: 0-4
- **Rainbow Spreadsheet** — visualização de padrões entre participantes

## Checklists
- [ ] Plano de teste documentado com objetivo, tarefas e métricas
- [ ] Protótipo testável e sem bugs bloqueantes
- [ ] Roteiro de moderação criado com tarefas e probes
- [ ] Piloto realizado e protocolo ajustado
- [ ] 5-8 participantes recrutados e agendados
- [ ] Ambiente de teste preparado (ferramenta, links, gravação)
- [ ] Todas as sessões executadas e gravadas
- [ ] Rainbow Spreadsheet preenchida com dados de todas as sessões
- [ ] Problemas classificados por severidade
- [ ] Relatório com recomendações entregue ao squad

## Steps
1. **Definir objetivo e tarefas** — Especificar quais aspectos do design serão avaliados e criar
   3-5 tarefas representativas com cenários realistas e critérios de sucesso mensuráveis.

2. **Preparar protocolo de teste** — Documentar: introdução, script de moderação, sequência de
   tarefas, probes, questionário pós-teste (SUS) e roteiro de debrief.

3. **Preparar protótipo** — Garantir que o protótipo cobre todos os fluxos das tarefas definidas.
   Testar internamente para eliminar bugs de prototipação que enviesar resultados.

4. **Recrutar participantes** — Selecionar 5-8 participantes representativos do público-alvo.
   Confirmar agendamento e enviar instruções prévias.

5. **Conduzir piloto** — Executar 1 sessão-piloto completa para calibrar timing, identificar
   ambiguidades no script e verificar a configuração técnica.

6. **Executar sessões de teste** — Moderar sessões de 45-60 minutos usando think-aloud protocol.
   Manter postura neutra, não ajudar o participante e registrar todas as observações.

7. **Preencher Rainbow Spreadsheet** — Após cada sessão, registrar: sucesso/falha por tarefa,
   tempo, erros, verbalizações-chave e score SUS. Consolidar em visão comparativa.

8. **Classificar problemas por severidade** — Listar todos os problemas encontrados e aplicar
   severity rating de Nielsen (0=cosmético a 4=catástrofe de usabilidade).

9. **Elaborar relatório de findings** — Documentar: metodologia, perfil, métricas consolidadas,
   top problemas com evidências (clips, quotes) e recomendações de design.

10. **Facilitar sessão de priorização** — Apresentar findings ao squad e priorizar correções
    por severidade x esforço. Definir itens para próxima iteração de design.

## Output
- **Usability Test Report** — Relatório com métricas, problemas e recomendações
- **Rainbow Spreadsheet** — Dados tabulados por participante e tarefa
- **Highlight Reel** — Compilação de clips dos momentos mais relevantes
- **Formato:** Markdown + planilha + clips de vídeo
- **Nomenclatura:** `usability-test-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UX Researcher |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por ciclo de iteração de design |
| Aprovadores | Design Lead, PM |
| Repositório | `/squads/design/tasks/research/` |

## Cross-References
- [Build Prototype](../ui/build-prototype.md)
- [Synthesize Insights](./synthesize-insights.md)
- [Build Research Repository](./build-research-repository.md)
- [Wireframe Pack](../ux/wireframe-pack.md)
- [UI Design High Fidelity](../ui/ui-design-high-fidelity.md)
- [Accessibility Review](../review/accessibility-review.md)
