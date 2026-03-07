# Documentation Style

## Context

Guia de estilo para toda documentação produzida pelo Design Squad — desde docs de
componentes no design system até ADRs, guides de pattern e wikis internas. Documentação
bem escrita reduz perguntas repetitivas, acelera onboarding e cria fonte única de verdade.

A documentação do Design Squad é bilíngue por natureza: estrutura e títulos em inglês
(para compatibilidade com tooling e busca), conteúdo explicativo em PT-BR (para o time
consumir), e termos técnicos em inglês (tokens, components, patterns) mantidos no original.

**Aplicação:** Design system docs, wikis, ADRs, guides, READMEs.
**Tom predominante:** System Thinker + Pragmatic Builder
**Frequência:** Contínua — toda documentação segue este guia

## Do's

### Estrutura consistente
- Todo documento começa com título H1 e metadata (autor, data, status)
- Seções seguem hierarquia H2 > H3 > H4 sem pular níveis
- Table of contents automático para docs com mais de 3 seções H2
- Cross-references com links internos para documentos relacionados

### Linguagem clara e scannable
- Parágrafos curtos (3-5 linhas máximo)
- Bullet points para listas de 3 ou mais items
- Bold para termos-chave na primeira ocorrência
- Code blocks para tokens, valores e snippets

### Exemplos concretos
- Todo conceito abstrato acompanhado de exemplo prático
- Screenshots atualizados (marcar como "captura de [data]")
- Code snippets testados e funcionais
- Before/after para mudanças e migrações

### Manutenção e ownership
- Cada documento tem um owner explícito
- Data de última atualização visível no metadata
- Status claro: Draft, Review, Published, Deprecated
- Changelog para documentos de referência

### Nomenclatura de arquivos
- kebab-case para nomes de arquivo: `design-tokens-guide.md`
- Prefixo de categoria quando relevante: `adr-001-color-system.md`
- Sem caracteres especiais, acentos ou espaços
- Extensão .md para todos os documentos de texto

## Don'ts

### Documentação orphan
- Criar documento sem linkar de nenhum lugar (ninguém encontra)
- Documentar sem definir owner (ninguém mantém)
- Escrever sem público-alvo claro (não serve para ninguém)

### Wall of text
- Parágrafos de 10+ linhas sem quebra visual
- Explicações teóricas sem exemplo prático
- Repetição de informação já documentada em outro lugar (linkar)

### Documentação desatualizada
- Screenshots de versões antigas do produto
- Referências a componentes deprecated sem nota
- Links quebrados para recursos externos

### Formatação inconsistente
- Misturar estilos de heading (## e **bold** como título)
- Usar tabs e spaces inconsistentemente em code blocks
- Listas sem padrão (às vezes bullet, às vezes número, sem critério)

### Jargão sem explicação
- Usar siglas sem definir na primeira ocorrência
- Assumir conhecimento de ferramentas específicas
- Referenciar processos internos sem link para definição

## Templates

### Template de documento de componente
```markdown
# [Component Name]

## Metadata
- **Status:** [Stable | Beta | Deprecated]
- **Owner:** [Nome]
- **Última atualização:** [Data]
- **Figma:** [Link]
- **Storybook:** [Link]

## Descrição
[O que é e para que serve]

## Variantes
[Lista de variantes com visual e uso]

## Props / API
[Tabela de propriedades]

## Acessibilidade
[Requisitos de a11y específicos]

## Exemplos de uso
[Screenshots + contexto]

## Referências
[Links para guidelines e decisões relacionadas]
```

### Template de ADR (Architecture Decision Record)
```markdown
# ADR-[NNN]: [Título da Decisão]

## Status
[Proposed | Accepted | Deprecated | Superseded by ADR-NNN]

## Contexto
[Qual problema estamos resolvendo]

## Decisão
[O que decidimos fazer]

## Alternativas consideradas
[O que mais foi avaliado e por que foi descartado]

## Consequências
[Impactos positivos e negativos da decisão]
```
