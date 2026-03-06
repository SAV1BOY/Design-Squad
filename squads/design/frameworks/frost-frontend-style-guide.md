# Frost Frontend Style Guide

## Metadata
- **Autor**: Brad Frost
- **Categoria**: Documentacao, Design Systems
- **Complexidade**: Media-Alta
- **Aplicacao**: Produtos com design system que precisam de docs vivas
- **Ultima atualizacao**: 2026-03-06

## Concept

Frontend Style Guide e o conceito de Brad Frost de documentacao viva (living documentation)
que esta diretamente sincronizada com o codigo de producao. Diferente de style guides
estaticos em PDF ou paginas de wiki que rapidamente ficam desatualizados, um frontend
style guide e gerado a partir dos proprios componentes implementados, garantindo que
a documentacao sempre reflete o estado real do sistema.

A premissa fundamental e que documentacao desatualizada e pior que nenhuma documentacao,
pois gera falsa confianca e decisoes baseadas em informacao incorreta. A solucao e
eliminar a separacao entre codigo e documentacao, fazendo com que um seja derivado do outro.

O style guide funciona como a "single source of truth" para designers, desenvolvedores,
QA e qualquer pessoa que precise entender como a interface do produto funciona.

## When to Use

- Quando a documentacao do design system fica desatualizada frequentemente
- Quando designers e devs trabalham com versoes diferentes dos componentes
- Quando novos membros da equipe precisam de onboarding no sistema visual
- Quando ha necessidade de review automatizado de consistencia
- Quando stakeholders precisam acompanhar a evolucao do design system
- Quando QA precisa de referencia confiavel para testes visuais

## How to Apply

### Passo 1 — Escolha a Abordagem de Geracao
Existem duas estrategias principais:
- **Code-first**: Documentacao gerada automaticamente a partir do codigo dos componentes
  (ex: Storybook, Docusaurus com MDX). O componente e a fonte da verdade.
- **Design-first com sync**: Documentacao criada no design tool (Figma) com mecanismos
  de sincronizacao automatica com o codigo.

A abordagem code-first e mais robusta para manter sincronizacao.

### Passo 2 — Estruture o Conteudo
Para cada componente, documente:
- Nome e descricao de uso
- Variantes visuais com preview renderizado ao vivo
- Props/parametros com tipos e valores default
- Estados interativos (hover, focus, disabled, loading, error)
- Guidelines de uso: quando usar e quando nao usar
- Codigo de exemplo copiavel
- Tokens de design utilizados (cores, espacamentos, tipografia)

### Passo 3 — Automatize a Sincronizacao
1. Integre a geracao do style guide no pipeline de CI/CD
2. Configure deploy automatico a cada merge na branch principal
3. Adicione testes visuais (visual regression) vinculados ao style guide
4. Crie alertas para quando componentes mudarem sem atualizacao de docs
5. Versione o style guide junto com o codigo

### Passo 4 — Promova a Adocao
1. Torne o style guide o ponto de entrada para qualquer trabalho de UI
2. Integre links do style guide nos design reviews e code reviews
3. Inclua o style guide no onboarding de novos membros
4. Colete feedback continuamente e itere na experiencia de uso
5. Celebre contribuicoes e melhorias na documentacao

### Passo 5 — Mantenha Vivo
1. Defina owners para cada secao do style guide
2. Revise mensalmente se ha componentes sem documentacao
3. Monitore metricas de uso (page views, buscas, feedback)
4. Atualize guidelines conforme padroes de uso evoluem
5. Retire componentes deprecated com comunicacao clara

## Key Principles

- **Sincronizacao automatica**: Documentacao deve ser gerada ou validada pelo codigo
- **Exemplos ao vivo**: Componentes devem ser renderizados, nao screenshots estaticos
- **Copiabilidade**: Codigo de exemplo deve ser facilmente copiavel e funcional
- **Busca eficiente**: O style guide deve ter search robusto e navegacao intuitiva
- **Versionamento**: Cada versao do sistema deve ter seu style guide correspondente
- **Acessibilidade da docs**: O proprio style guide deve ser acessivel e bem organizado
- **Feedback loop**: Usuarios da docs devem poder reportar problemas facilmente

## Examples

### Exemplo 1 — Storybook como Style Guide
Uma equipe configurou Storybook com addons de docs, a11y e design tokens. Cada componente
React tinha stories que serviam simultaneamente como testes visuais e documentacao.
O deploy era automatico via CI a cada merge. Resultado: zero divergencia entre docs
e codigo por 18 meses consecutivos.

### Exemplo 2 — Style Guide com Metricas
Uma equipe adicionou analytics ao style guide e descobriu que:
- 78% dos acessos eram para copiar codigo de exemplo
- A pagina de tokens era a mais visitada
- Componentes de formulario tinham 3x mais pageviews que outros
Essas metricas guiaram investimento em melhorar docs de forms e tokens primeiro.

### Exemplo 3 — Migrating from Static to Living
Uma empresa tinha um PDF de 200 paginas como style guide. Migraram para Storybook
em 4 sprints: Sprint 1 — setup e 10 componentes core. Sprint 2 — mais 25 componentes.
Sprint 3 — tokens e guidelines. Sprint 4 — search, analytics e feedback mechanism.
Adocao subiu de 23% para 89% da equipe em 2 meses apos lancamento.

## Common Pitfalls

- **Style guide como projeto separado**: Se a docs nao vive junto ao codigo, vai desincronizar.
  Mantenha no mesmo repositorio ou com sync automatico
- **Focar em estetica sobre utilidade**: Um style guide bonito mas sem exemplos copiaveis
  e sem search e inutil na pratica
- **Nao ter owners**: Documentacao sem responsaveis definidos degrada rapidamente
- **Documentar tudo de uma vez**: Comece pelos componentes mais usados e expanda incrementalmente
- **Ignorar a experiencia de contribuicao**: Se e dificil adicionar ou atualizar docs,
  ninguem vai fazer. Simplifique o processo de contribuicao
- **Falta de discoverability**: Se a equipe nao sabe que o style guide existe ou onde
  encontra-lo, ele nao sera usado. Integre em todos os workflows
- **Nao versionar**: Sem versionamento, equipes em versoes antigas do sistema nao tem referencia

## Cross-References

- [frost-pattern-lab.md](frost-pattern-lab.md) — Tooling especifico para style guides
- [frost-maintaining-design-systems.md](frost-maintaining-design-systems.md) — Manutencao continua
- [design-system-layer.md](design-system-layer.md) — Documentacao como camada do design system
- [handoff-layer.md](handoff-layer.md) — Style guide como ponte entre design e dev
- [component-spec-framework.md](component-spec-framework.md) — O que documentar por componente
- [design-to-code-handoff.md](design-to-code-handoff.md) — Handoff facilitado por docs vivas
