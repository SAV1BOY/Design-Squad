# Component Inventory

## Metadata
- **Categoria:** Design System
- **Complexidade:** Média
- **Tempo Estimado:** 3-5 dias
- **Squad:** Design
- **Status:** Gold Standard
- **Última Atualização:** 2026-03-06
- **Tags:** design-system, inventory, components, audit, consistency

## Objective
Realizar um inventário completo de todos os componentes de UI utilizados no produto, identificando
variações, duplicações e inconsistências. O inventário serve como baseline para consolidação do
design system e priorização de componentização.

## Prerequisites
- Acesso ao produto em produção e ao repositório de código
- Acesso aos arquivos Figma de design do produto
- Ferramenta de captura e catalogação configurada
- Design system atual documentado (se existente)
- Stakeholder alignment sobre escopo do inventário

## Agents
| Papel | Responsabilidade |
|-------|-----------------|
| Design System Lead | Coordenar inventário, definir taxonomia e priorizar |
| UI Designer | Capturar componentes das interfaces e catalogar variações |
| Frontend Engineer | Mapear componentes implementados e suas variantes no código |
| Design Lead | Revisar inventário e aprovar plano de consolidação |

## Frameworks
- **Interface Inventory (Brad Frost)** — método de coleta e catalogação sistemática
- **Atomic Design** — classificação: atoms, molecules, organisms, templates
- **Component Maturity Model** — nível de maturidade: ad-hoc, managed, defined, measured
- **Duplication Score** — métrica de duplicação por categoria de componente

## Checklists
- [ ] Escopo do inventário definido (plataformas, módulos, páginas)
- [ ] Screenshots de todos os componentes capturados do produto
- [ ] Componentes agrupados por tipo (botões, inputs, cards, modals, etc.)
- [ ] Variações por componente identificadas e documentadas
- [ ] Duplicações e inconsistências catalogadas
- [ ] Componentes do Figma mapeados vs componentes em código
- [ ] Gap analysis entre design e implementação executado
- [ ] Priorização de consolidação definida (por frequência e impacto)
- [ ] Inventário publicado e acessível ao squad
- [ ] Plano de ação para consolidação redigido

## Steps
1. **Definir escopo** — Delimitar quais plataformas (web, mobile, desktop), módulos e páginas
   serão inventariados. Priorizar por impacto e volume de uso.

2. **Capturar componentes visuais** — Percorrer o produto sistematicamente capturando screenshots
   de cada componente único. Incluir todos os estados visíveis.

3. **Catalogar por tipo** — Organizar screenshots em categorias: typography, buttons, inputs,
   cards, navigation, modals, alerts, tables, icons, etc.

4. **Identificar variações** — Para cada tipo, documentar todas as variações encontradas.
   Registrar: onde aparece, visual, comportamento e se é intencional ou acidental.

5. **Mapear componentes em código** — Com Frontend Engineer, levantar componentes implementados
   no codebase. Verificar: nomes, props, variantes e usage count.

6. **Executar gap analysis** — Cruzar inventário visual com inventário de código. Identificar:
   componentes em design sem código, em código sem design, e divergências.

7. **Calcular duplication score** — Para cada categoria, quantificar o nível de duplicação.
   Exemplo: 7 variantes de botão quando o DS define 3 = score de duplicação alto.

8. **Priorizar consolidação** — Classificar componentes por: frequência de uso x nível de
   inconsistência. Componentes usados frequentemente com alta inconsistência são prioridade.

9. **Documentar e planejar** — Redigir relatório com inventário completo, scores de duplicação,
   gap analysis e plano de consolidação com timeline sugerida.

## Output
- **Component Inventory** — Catálogo visual de todos os componentes com variações
- **Gap Analysis** — Mapa de divergências entre design e código
- **Consolidation Plan** — Plano priorizado de ações para reduzir duplicação
- **Formato:** Figma file (galeria) + planilha + Markdown
- **Nomenclatura:** `component-inventory-[produto]-[YYYY-MM-DD]`

## Registry
| Campo | Valor |
|-------|-------|
| Criado por | Design System Lead |
| Data de criação | 2026-03-06 |
| Versão | 1.0 |
| Frequência | Semestral ou antes de major DS update |
| Aprovadores | Design Lead |
| Repositório | `/squads/design/tasks/design-system/` |

## Cross-References
- [Design Audit Existing Product](../discovery/design-audit-existing-product.md)
- [Create Component Spec](./create-component-spec.md)
- [DS Health Check](./ds-health-check.md)
- [Adoption and Migration](./adoption-and-migration.md)
- [Publish Library](./publish-library.md)
