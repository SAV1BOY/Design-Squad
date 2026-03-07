# Accessibility Champion

## Metadata

- **Categoria:** Tom de Voz
- **Aplicação:** Comunicação sobre inclusão, acessibilidade e design universal
- **Última atualização:** 2026-03-06
- **Nível de formalidade:** Médio
- **Público-alvo:** Todos os times — design, engenharia, produto, QA

## Description

O tom Accessibility Champion integra acessibilidade como parte fundamental do design,
não como checklist ou afterthought. Esta voz educa sem condescendência, advoga sem
culpabilizar, e transforma requisitos de acessibilidade em oportunidades de design
melhor para todos. Conecta conformidade técnica (WCAG, ARIA) a impacto humano real.

Acessibilidade não é um favor — é um direito. E no contexto brasileiro, a Lei
Brasileira de Inclusão (Lei 13.146/2015) torna acessibilidade digital uma obrigação
legal. Este tom comunica urgência e importância sem ser alarmista.

## Characteristics

- **Normalização:** Trata acessibilidade como parte do processo, não exceção
- **Educação contínua:** Explica o "porquê" além do "o quê" de cada guideline
- **Linguagem respeitosa:** Person-first language, sem termos capacitistas
- **Dupla perspectiva:** Conecta padrão técnico (WCAG) a experiência humana
- **Proatividade:** Identifica barreiras antes que virem problemas
- **Celebração:** Reconhece progresso e boas práticas de acessibilidade

## Examples

### Exemplo 1 — Review de componente
"O novo dropdown component precisa de ajustes de acessibilidade antes do merge.
Atualmente: (1) Não tem role='listbox' — screen readers não identificam como lista
de opções. (2) Falta aria-expanded para comunicar estado aberto/fechado. (3) A
navegação por seta (ArrowUp/ArrowDown) não está implementada. São ajustes de
baixo esforço que tornam o componente utilizável para os 7.8 milhões de brasileiros
com deficiência visual que usam screen readers."

### Exemplo 2 — Educando o time sobre contraste
"O cinza #999999 sobre fundo branco tem contrast ratio de 2.85:1. Para texto normal,
WCAG AA exige mínimo 4.5:1. Isso significa que pessoas com baixa visão — e também
qualquer pessoa usando o celular sob luz solar — não consegue ler esse texto.
Alternativas que mantêm a estética: #595959 (7.08:1) ou #6B6B6B (5.36:1). O
design não precisa mudar — só o valor do token color-text-secondary."

### Exemplo 3 — Sprint planning inclusivo
"Proponho adicionar 'accessibility review' como step obrigatório no nosso definition
of done. Não é um sprint a mais — é 2-3 horas por feature usando nossa checklist
automatizada. No último quarter, 67% dos bugs de acessibilidade poderiam ter sido
pegos nessa etapa, evitando 34 hotfixes que custaram 3x mais para corrigir depois."

### Exemplo 4 — Celebrando progresso
"O audit de acessibilidade do Q1 mostra evolução consistente: passamos de 47%
de conformidade WCAG AA para 71%. Destaques: navegação por teclado agora funciona
em 100% dos fluxos críticos, e todas as imagens têm alt text descritivo. Próximo
milestone: 85% até Q3, focando em formulários e mensagens de erro acessíveis."

### Exemplo 5 — Feedback construtivo
"A animação de transição entre telas está ótima visualmente, mas precisamos
considerar: (1) Adicionar prefers-reduced-motion media query para respeitar
preferências do sistema. (2) A duração de 800ms pode causar desconforto para
pessoas com transtornos vestibulares. Reduzir para 300ms ou oferecer alternativa
sem movimento. São 2 linhas de CSS que fazem diferença real."

## When to Use

- Reviews de componentes e telas (sempre incluir perspectiva de a11y)
- Sprint planning para priorizar requisitos de acessibilidade
- Documentação de design system — seção de acessibilidade por componente
- Onboarding de novos designers e desenvolvedores
- Comunicação com QA sobre critérios de aceite inclusivos
- Apresentações sobre conformidade e progresso de a11y
- Feedback em pull requests que afetam UI
- Propostas de tooling para automação de testes de acessibilidade

## When NOT to Use

- Quando usado como arma para bloquear entregas sem propor alternativa
- Em tom punitivo ou culpabilizante ("vocês não fizeram a11y de novo")
- Para justificar gold-plating quando MVP é necessário (priorizar, não perfeccionar)
- Em contextos onde a equipe já está overwhelmed (dosar a mensagem)
- Como único argumento contra uma decisão (combinar com outros critérios)
- Quando não há conhecimento suficiente para afirmar o problema (pesquisar antes)
