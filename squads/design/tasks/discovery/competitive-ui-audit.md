# Competitive UI Audit

## Metadata
- **Categoria:** Discovery
- **Complexidade:** Média
- **Tempo Estimado:** 3-5 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** discovery, competitive-analysis, benchmarking, ui-patterns

## Objective
Realizar uma análise sistemática das interfaces de concorrentes diretos e indiretos para identificar
padrões de UI, oportunidades de diferenciação e best practices do mercado. O audit gera um
repositório visual comparativo que informa decisões de design durante todo o projeto.

## Prerequisites
- Lista de concorrentes diretos e indiretos definida com PM
- Acesso às plataformas concorrentes (contas de teste quando necessário)
- Ferramenta de captura de tela e anotação (Markup Hero, CleanShot ou equivalente)
- Template de análise competitiva padronizado pelo squad
- Critérios de avaliação definidos (heurísticas ou dimensões de comparação)

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| UI Designer | Capturar interfaces, catalogar padrões e elaborar análise visual |
| UX Designer | Avaliar fluxos e decisões de interação dos concorrentes |
| Design Lead | Definir critérios de avaliação e revisar documento final |
| Product Manager | Validar lista de concorrentes e fornecer contexto competitivo |

## Frameworks
- **Heuristic Evaluation (Nielsen)** — para avaliar usabilidade de cada concorrente
- **Feature Matrix** — para comparar funcionalidades e padrões entre concorrentes
- **SWOT por Concorrente** — para mapear forças, fraquezas, oportunidades e ameaças
- **UI Pattern Library** — para catalogar padrões recorrentes identificados

## Checklists
- [ ] Lista de concorrentes aprovada pelo PM (mínimo 5, máximo 12)
- [ ] Critérios de avaliação definidos e documentados
- [ ] Screenshots capturados de todos os fluxos relevantes por concorrente
- [ ] Feature Matrix preenchida com todas as dimensões comparativas
- [ ] Análise heurística resumida por concorrente
- [ ] Padrões de UI recorrentes catalogados com exemplos visuais
- [ ] Oportunidades de diferenciação identificadas e priorizadas
- [ ] Documento final revisado pelo Design Lead
- [ ] Apresentação de findings para o squad realizada

## Steps
1. **Definir escopo e concorrentes** — Com o PM, selecionar 5-12 concorrentes (diretos e
   indiretos). Definir quais fluxos e funcionalidades serão analisados por concorrente.

2. **Estabelecer critérios de avaliação** — Selecionar 6-10 dimensões de análise como:
   onboarding, navegação, density de informação, feedback visual, acessibilidade percebida.

3. **Capturar interfaces sistematicamente** — Para cada concorrente, percorrer os fluxos
   definidos capturando screenshots anotados. Organizar por concorrente e fluxo.

4. **Preencher Feature Matrix** — Criar matriz comparativa com concorrentes nas colunas e
   features/padrões nas linhas. Usar escala de 1-5 ou indicadores visuais.

5. **Avaliar com heurísticas** — Aplicar as 10 heurísticas de Nielsen de forma resumida para
   cada concorrente. Registrar violações notáveis e boas práticas.

6. **Catalogar padrões de UI** — Identificar padrões recorrentes entre concorrentes (ex: card
   layouts, navigation patterns, empty states). Criar galeria visual categorizada.

7. **Identificar oportunidades de diferenciação** — Com base nas lacunas e fraquezas dos
   concorrentes, listar oportunidades onde nosso produto pode se destacar.

8. **Elaborar documento de findings** — Consolidar análise em documento estruturado com:
   resumo executivo, matrix comparativa, padrões catalogados e recomendações.

9. **Apresentar para o squad** — Conduzir sessão de 30-45 minutos apresentando os principais
   findings e facilitando discussão sobre implicações para o projeto.

## Output
- **Competitive UI Audit Report** — Documento com análise comparativa completa, galeria de
  padrões e recomendações de diferenciação
- **Feature Matrix** — Planilha ou tabela comparativa detalhada
- **Pattern Gallery** — Coleção organizada de screenshots anotados
- **Formato:** Markdown + FigJam/Miro board para assets visuais
- **Nomenclatura:** `competitive-audit-[nome-do-projeto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | UI Designer |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Por projeto ou trimestral para produtos maduros |
| Aprovadores | Design Lead, PM |
| Repositório | `/squads/design/tasks/discovery/` |

## Cross-References
- [Problem Definition](./problem-definition.md)
- [Design Audit Existing Product](./design-audit-existing-product.md)
- [Create Visual Explorations](../ui/create-visual-explorations.md)
- [UI Design High Fidelity](../ui/ui-design-high-fidelity.md)
- [Maintain Swipe File](../operations/maintain-swipe-file.md)
