# QA Review Framework

## Metadata

- **Autor**: Design Squad
- **Categoria**: Quality Assurance, Handoff, Validacao
- **Complexidade**: Media
- **Aplicacao**: Comparar specs de design com implementacao, reportar bugs visuais/funcionais com severidade
- **Ultima atualizacao**: 2026-03-18
- **Tags**: qa, visual-review, spec-comparison, bug-reporting, severity, prioritization, pixel-perfect

## Concept

O QA Review Framework estrutura o processo de validacao visual e funcional — a comparacao
sistematica entre o que foi especificado no design e o que foi implementado no codigo. O
objetivo nao e "pixel-perfect" obsessivo, mas garantir que a intencao de design (hierarquia,
usabilidade, acessibilidade, consistencia) foi preservada na implementacao.

O framework define como inspecionar, como reportar discrepancias com severidade objetiva, e
como priorizar correcoes para que bugs criticos de UX nao fiquem atras de detalhes cosmeticos.
O QA de design e complementar ao QA funcional de engenharia — foca na experiencia percebida
pelo usuario, nao apenas em "funciona vs. nao funciona".

## When to Use

- Antes de cada release que inclui mudancas visuais ou de interacao
- Apos implementacao de novos componentes do design system
- Quando engenharia sinaliza "pronto para review de design"
- Em ciclos de QA regulares para features em desenvolvimento
- Apos hotfixes que tocaram camada de UI
- Para validar responsive behavior em breakpoints criticos

## How to Apply

### Step 1 — Preparar Review
1. Obtenha acesso ao ambiente de staging/preview com a implementacao
2. Abra os specs de design correspondentes (Figma, Zeplin, ou ferramenta de handoff)
3. Prepare checklist de review baseado nas dimensoes abaixo
4. Defina devices/browsers a testar: minimo desktop + mobile principal
5. Garanta que dados de teste sao representativos (nomes reais, textos longos, edge cases)

### Step 2 — Inspecao Visual
Compare specs vs. implementacao em cada dimensao:

| Dimensao | O que verificar |
|---|---|
| **Layout & Spacing** | Margins, paddings, gaps, alinhamentos, grid compliance |
| **Tipografia** | Font family, size, weight, line-height, letter-spacing, truncation |
| **Cores** | Background, text, borders, estados (hover, active, disabled, focus) |
| **Componentes** | Variantes corretas, props aplicadas, estados visuais |
| **Icones & Imagens** | Tamanho, cor, alinhamento, resolucao, alt text |
| **Responsive** | Breakpoints, reflow, stacking order, touch targets (min 44x44px) |
| **Motion** | Timing, easing, transicoes entre estados, loading states |

### Step 3 — Inspecao Funcional de UX
Alem do visual, valide comportamentos de experiencia:

1. **Fluxo completo**: Execute o happy path e verifique cada etapa
2. **Estados**: Empty state, loading, error, success — todos implementados?
3. **Edge cases**: Textos longos, listas vazias, conexao lenta, timeout
4. **Interacoes**: Hover, focus, active, disabled funcionam como especificado?
5. **Navegacao**: Back button, deep links, breadcrumbs funcionam corretamente?
6. **Acessibilidade basica**: Tab order, focus visible, contraste, screen reader labels

### Step 4 — Reportar Discrepancias (Bug Reporting)
Para cada discrepancia encontrada, documente:

1. **Titulo**: Descricao concisa do problema
2. **Severidade**: S1-S4 (veja classificacao abaixo)
3. **Dimensao**: Qual aspecto esta incorreto (layout, cor, typography, etc.)
4. **Onde**: Tela, componente, estado, device/browser
5. **Esperado**: Screenshot ou link do spec de design
6. **Atual**: Screenshot da implementacao
7. **Impacto**: Como afeta o usuario final

Classificacao de severidade:

| Nivel | Descricao | Exemplos | SLA sugerido |
|---|---|---|---|
| **S1 — Critico** | Impede uso ou viola requisito legal | Botao de acao invisivel, contraste abaixo de WCAG AA, fluxo bloqueado | Fix antes da release |
| **S2 — Major** | Prejudica experiencia significativamente | Hierarquia invertida, touch target muito pequeno, estado de erro ausente | Fix no sprint atual |
| **S3 — Minor** | Discrepancia notavel mas nao impede uso | Spacing 4px off, cor levemente diferente, animacao ausente | Fix no proximo sprint |
| **S4 — Cosmetic** | Detalhe menor, polish | Arredondamento 2px diferente, sombra sutil ausente | Backlog / nice-to-have |

### Step 5 — Priorizar Correcoes
1. Agrupe bugs por severidade e por tela/fluxo
2. Identifique padroes: problemas sistemicos (ex.: todos os spacings estao 4px maiores)
3. Bugs sistematicos devem ser resolvidos na raiz (token, componente base), nao caso a caso
4. Priorize: S1 > S2 > bugs sistemicos S3 > S3 pontual > S4
5. Defina com engenharia quais serao fixados antes da release vs. pos-release
6. Registre decisoes de "aceitar como esta" com racional (nao ignore silenciosamente)

### Step 6 — Re-review e Sign-off
1. Apos fixes, re-verifique cada bug reportado como corrigido
2. Mantenha status atualizado: aberto > em fix > re-review > fechado
3. Quando todos os S1 e S2 estao fechados: design sign-off para release
4. Documente S3/S4 aceitos para sprint futuro como design debt
5. Comunique sign-off (ou bloqueio) formalmente no canal do squad

## Examples

### Exemplo 1 — QA de Feature de Checkout
22 bugs reportados: 2 S1 (botao CTA sem contraste acessivel + empty state de carrinho ausente),
5 S2 (touch targets < 44px em mobile, hierarquia de preco incorreta), 10 S3, 5 S4.
S1 fixados em 1 dia. S2 fixados no sprint. Release aprovada com 3 S3 aceitos como debt.

### Exemplo 2 — QA Sistemico pos-Migration de DS
Apos migracao de DS v2 para v3, QA em 8 telas revelou padrao: todos os spacings de 16px
viraram 12px por erro no token mapping. Fix unico no token resolveu 34 dos 41 bugs reportados.
Restantes 7 eram bugs pontuais de implementacao. Sem o QA sistematico, cada bug teria sido
reportado e fixado individualmente.

## Common Pitfalls

- **QA so no final**: Revisar so antes da release gera pressao para "aceitar como esta"
- **Tudo e S1**: Inflar severidade destrói priorizacao e credibilidade do design
- **Screenshots sem contexto**: Bug report sem spec de referencia forca engenharia a adivinhar
- **Ignorar responsive**: Testar so desktop quando 60%+ do trafego e mobile
- **QA sem dados reais**: Testar com "Lorem ipsum" nao revela problemas de truncation e layout
- **Nao fechar o loop**: Reportar bugs sem re-verificar fixes cria backlog fantasma

## Cross-References

- [design-to-code-handoff.md](design-to-code-handoff.md) — Specs como referencia para QA
- [handoff-layer.md](handoff-layer.md) — Processo de handoff que precede o QA
- [design-audit-framework.md](design-audit-framework.md) — Audit abrangente vs. QA pontual
- [accessibility-wcag-aa.md](accessibility-wcag-aa.md) — Criterios de a11y no QA
- [design-debt-management.md](design-debt-management.md) — Bugs S3/S4 aceitos viram design debt
- [design-system-governance.md](design-system-governance.md) — DS consistency como dimensao de QA
- [Design Review Report Template](../templates/reports/design-review-report-template.md) — Template para documentar review
- [Design Critique Quality Checklist](../checklists/design-critique-quality.md) — Checklist de qualidade
- [Design Chief](../agents/design-chief.md) — Sign-off authority
- [Jessica UX/UI](../agents/jessica-ux-ui.md) — Agente para suporte em QA visual
