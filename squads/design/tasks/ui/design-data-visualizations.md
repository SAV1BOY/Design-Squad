# Design Data Visualizations

## Metadata
- **Categoria:** UI
- **Complexidade:** Alta
- **Tempo Estimado:** 5-10 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** ui, data-visualization, charts, dashboards, information-design

## Objective
Projetar visualizações de dados claras, acessíveis e acionáveis que transformem dados complexos
em insights compreensíveis para o usuário. O trabalho abrange seleção de chart types, paleta de
cores para dados, interações e estados de dashboards completos.

## Prerequisites
- Requisitos de dados definidos (quais métricas, granularidade, atualização)
- Amostras de dados reais ou representativas disponíveis
- Personas e contexto de uso definidos (quem, quando, para quê)
- Design system com tokens de cores e tipografia
- Ferramenta de design e prototipação configurada (Figma, D3.js para exploração)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UI Designer | Projetar visualizações, paleta de dados e interações |
| Data Analyst | Fornecer dados reais e validar representação correta |
| UX Designer | Garantir que dashboards contam uma história acionável |
| A11y Specialist | Validar acessibilidade (contraste, não dependência de cor) |
| Frontend Engineer | Avaliar viabilidade com a library de charts escolhida |

## Frameworks
- **Data-Ink Ratio (Tufte)** — maximizar dados, minimizar elementos decorativos
- **Chart Selection Matrix** — tipo de chart por tipo de dado e comparação
- **Sequential/Diverging/Categorical Palettes** — paletas de cores para dados
- **Dashboard Information Hierarchy** — KPIs no topo, detalhes sob demanda
- **Accessible Data Viz** — padrões para visualizações acessíveis (WCAG)

## Checklists
- [ ] Tipos de dados e métricas inventariados
- [ ] Chart types selecionados e justificados por tipo de dado
- [ ] Paleta de cores para dados definida (colorblind-safe)
- [ ] Dados reais ou representativos aplicados nas visualizações
- [ ] Interações definidas: hover tooltips, drill-down, filtros, zoom
- [ ] Estados contemplados: loading (skeleton), empty, error, partial data
- [ ] Labels, legends e axis titles claros e legíveis
- [ ] Responsividade dos charts verificada em mobile e desktop
- [ ] Acessibilidade validada (contraste, alt text, keyboard navigation)
- [ ] Specs documentados para a library de charts da eng

## Steps
1. **Inventariar requisitos de dados** — Com Data Analyst e PM, listar: métricas, dimensões,
   granularidade temporal, atualização (real-time, diário, etc.) e volume de dados.

2. **Selecionar chart types** — Para cada métrica ou comparação, selecionar o tipo de chart
   mais adequado usando a Chart Selection Matrix. Justificar cada escolha.

3. **Criar paleta de cores para dados** — Definir paletas: sequential (gradiente para valores
   ordenados), diverging (centro neutro) e categorical (categorias distintas). Testar com
   simulador de daltonismo.

4. **Projetar visualizações individuais** — Desenhar cada chart com dados reais. Incluir:
   título descritivo, labels de eixo, legenda, tooltips e anotações quando relevante.

5. **Compor dashboards** — Organizar charts em layouts de dashboard com hierarquia clara:
   KPIs sumários no topo, trends no meio, detalhes e tabelas na base.

6. **Definir interações** — Especificar: hover (tooltip com valor exato), click (drill-down),
   filtros globais e locais, zoom temporal e comparação entre períodos.

7. **Projetar estados** — Para cada visualização, criar: loading (skeleton do chart), empty
   (sem dados no período), error (falha ao carregar) e partial (dados incompletos).

8. **Validar acessibilidade** — Verificar: contraste de cores em todas as séries, informação
   não dependente apenas de cor (uso de patterns, labels), alt text para charts.

9. **Documentar specs técnicos** — Criar spec por chart: tipo, library recomendada, dados
   esperados, paleta, interações e comportamento responsive.

## Output
- **Data Visualization Specs** — Especificações por chart e dashboard
- **Data Color Palette** — Paleta de cores para dados (colorblind-safe)
- **Dashboard Mockups** — Layouts completos com dados reais aplicados
- **Formato:** Figma file + Markdown specs + paleta exportada
- **Nomenclatura:** `dataviz-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UI Designer |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por projeto com componente de dados |
| Aprovadores | Design Lead, Data Analyst |
| Repositório | `/squads/design/tasks/ui/` |

## Cross-References
- [UI Design High Fidelity](./ui-design-high-fidelity.md)
- [Design Responsive Layouts](./design-responsive-layouts.md)
- [A11y Audit](../accessibility/a11y-audit.md)
- [Analyze Analytics for UX](../research/analyze-analytics-for-ux.md)
- [Create Component Spec](../design-system/create-component-spec.md)
