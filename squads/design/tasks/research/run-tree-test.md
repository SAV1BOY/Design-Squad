# Run Tree Test

## Metadata
- **Categoria:** Research
- **Complexidade:** Média
- **Tempo Estimado:** 3-5 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** research, tree-test, information-architecture, findability, navigation

## Objective
Executar tree tests para validar a eficácia da information architecture proposta ou existente,
medindo a capacidade dos usuários de encontrar itens na estrutura de navegação. Os dados de
findability e directness orientam ajustes na IA antes do design visual.

## Prerequisites
- Estrutura de IA (tree) definida e pronta para teste
- Tarefas de findability redigidas (mínimo 8, ideal 10-15)
- Ferramenta de tree test configurada (Optimal Workshop Treejack ou equivalente)
- Perfil de participante definido e base de recrutamento disponível
- Resultados de card sort prévio (se disponíveis) como referência

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UX Researcher | Planejar estudo, definir tarefas e analisar resultados |
| UX Designer | Construir árvore de IA e iterar com base nos achados |
| Content Designer | Revisar labels de navegação e nomenclatura da árvore |
| Product Manager | Validar tarefas prioritárias e escopo de conteúdo |

## Frameworks
- **Treejack (Optimal Workshop)** — ferramenta padrão para tree testing remoto
- **Findability Rate** — % de participantes que encontraram o item correto
- **Directness Score** — % que navegou direto ao destino sem backtracking
- **First Click Analysis** — onde os participantes clicam primeiro por tarefa
- **Path Analysis** — visualização dos caminhos percorridos até o destino

## Checklists
- [ ] Árvore de navegação montada na ferramenta de teste
- [ ] 10-15 tarefas de findability redigidas com resposta correta definida
- [ ] Piloto executado com 3-5 participantes internos
- [ ] 30-50 participantes recrutados e estudo distribuído
- [ ] Taxa de completude monitorada (mínimo 80%)
- [ ] Dados de findability e directness analisados por tarefa
- [ ] First click e path analysis revisados para tarefas problemáticas
- [ ] Recomendações de ajuste na IA documentadas
- [ ] Relatório final compartilhado com squad

## Steps
1. **Construir árvore de teste** — Transferir a estrutura de IA proposta para a ferramenta de
   tree test. Incluir todos os níveis de navegação relevantes (tipicamente 2-4 níveis).

2. **Redigir tarefas de findability** — Criar 10-15 tarefas no formato: "Onde você iria para
   [objetivo do usuário]?". Evitar palavras que apareçam nos labels da árvore.

3. **Definir respostas corretas** — Para cada tarefa, marcar o(s) destino(s) correto(s) na
   árvore. Permitir múltiplas respostas corretas quando aplicável.

4. **Executar piloto** — Rodar com 3-5 colegas para verificar clareza das tarefas, tempo total
   e funcionamento técnico. Revisar tarefas ambíguas.

5. **Recrutar e distribuir** — Enviar para 30-50 participantes representativos. Tempo médio
   esperado: 5-10 minutos por participante.

6. **Monitorar coleta** — Acompanhar taxa de completude e qualidade das respostas. Encerrar
   após atingir amostra mínima (30 participantes completos).

7. **Analisar métricas por tarefa** — Calcular findability rate e directness score para cada
   tarefa. Identificar tarefas com findability abaixo de 70% como problemáticas.

8. **Investigar caminhos** — Para tarefas problemáticas, analisar first click e paths mais
   comuns. Identificar onde os participantes se perdem na árvore.

9. **Documentar recomendações** — Propor ajustes na IA baseados nos dados: renomear categorias,
   mover itens, criar atalhos ou reestruturar níveis problemáticos.

10. **Iterar e re-testar** — Se ajustes significativos forem feitos, considerar um segundo round
    de tree test para validar as melhorias antes de avançar para design visual.

## Output
- **Tree Test Report** — Relatório com métricas por tarefa, análise de paths e recomendações
- **IA Refinements** — Proposta de ajustes na estrutura de navegação
- **Formato:** Markdown + exports da ferramenta (pietrees, heatmaps)
- **Nomenclatura:** `tree-test-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UX Researcher |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Após card sort ou mudança significativa na IA |
| Aprovadores | Design Lead, UX Designer |
| Repositório | `/squads/design/tasks/research/` |

## Cross-References
- [Run Card Sort](./run-card-sort.md)
- [Build IA and Sitemap](../ux/build-ia-and-sitemap.md)
- [Synthesize Insights](./synthesize-insights.md)
- [Design User Flows](../ux/design-user-flows.md)
- [Build Research Repository](./build-research-repository.md)
