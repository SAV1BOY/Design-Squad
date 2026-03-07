# Design System Contribution Guide Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Design System**    | [PREENCHER — nome do DS]                       |
| **Autor(a)**         | [PREENCHER — DS team lead]                     |
| **Data de criacao**  | [PREENCHER — YYYY-MM-DD]                       |
| **Ultima atualizacao** | [PREENCHER — YYYY-MM-DD]                    |
| **Versao do guia**   | [PREENCHER — v1.0]                             |
| **Status**           | [PREENCHER — Draft / Publicado]                |

## Instructions (Como Usar)

1. Distribua este guia para todos os designers e devs que possam contribuir com o DS.
2. Use como referencia padrao quando alguem quiser adicionar ou modificar componentes.
3. Atualize conforme os processos do DS evoluem.
4. Disponibilize em local de facil acesso (wiki, README do repo, Notion, etc.).
5. Revise anualmente ou quando o processo mudar significativamente.

> **Dica:** Um guia de contribuicao claro reduz fricao e aumenta a qualidade das contribuicoes.

## Template

### 1. Bem-vindo(a) ao [PREENCHER — nome do DS]

[PREENCHER — breve introducao sobre o DS, sua missao e por que contribuicoes sao importantes. 2-3 frases motivacionais.]

**Quem pode contribuir:** [PREENCHER — todos os designers e devs / time de DS apenas / criterios]

### 2. Tipos de Contribuicao

| Tipo                      | Descricao                                  | Quem pode fazer       |
|---------------------------|--------------------------------------------|-----------------------|
| Bug report                | [PREENCHER — reportar problemas]           | [PREENCHER — qualquer um] |
| Feature request           | [PREENCHER — solicitar novo componente/token] | [PREENCHER]        |
| Design contribution       | [PREENCHER — propor design de componente]  | [PREENCHER]           |
| Code contribution         | [PREENCHER — implementar componente]       | [PREENCHER]           |
| Documentation             | [PREENCHER — melhorar docs/exemplos]       | [PREENCHER]           |
| Token update              | [PREENCHER — propor novos tokens]          | [PREENCHER]           |

### 3. Processo de Contribuicao

```
[PREENCHER — Step 1: Ideia/Necessidade]
        |
        v
[PREENCHER — Step 2: Verificar se ja existe]
        |
        v
[PREENCHER — Step 3: Abrir request/issue]
        |
        v
[PREENCHER — Step 4: Triagem pelo DS team]
        |
    Aprovado?
      / \
    Sim   Nao --> [PREENCHER — feedback e alternativas]
     |
     v
[PREENCHER — Step 5: RFC (se novo componente)]
     |
     v
[PREENCHER — Step 6: Design + Code]
     |
     v
[PREENCHER — Step 7: Review]
     |
     v
[PREENCHER — Step 8: Merge + Release]
```

### 4. Antes de Contribuir

**Checklist pre-contribuicao:**
- [ ] Verifiquei se o componente/token ja existe no DS — [PREENCHER — onde verificar]
- [ ] Verifiquei issues abertas para evitar duplicacao — [PREENCHER — link]
- [ ] Li os principios de design do DS — [PREENCHER — link]
- [ ] Li o coding style guide — [PREENCHER — link]
- [ ] Entendi a convencao de nomenclatura — [PREENCHER — link]

### 5. Como Reportar Bugs

**Canal:** [PREENCHER — onde reportar, ex.: GitHub Issues, Jira]

**Template de bug report:**
```
**Componente:** [PREENCHER — nome do componente]
**Versao do DS:** [PREENCHER — versao]
**Browser/Device:** [PREENCHER — onde ocorre]
**Descricao:** [PREENCHER — o que esta errado]
**Comportamento esperado:** [PREENCHER]
**Comportamento atual:** [PREENCHER]
**Steps para reproduzir:**
1. [PREENCHER]
2. [PREENCHER]
**Screenshot/Video:** [PREENCHER — evidencia]
```

### 6. Como Propor Novos Componentes

1. **Abra um request:** [PREENCHER — canal e formato]
2. **Inclua justificativa:** Por que o DS precisa deste componente? Quantos squads se beneficiariam?
3. **Triagem:** O DS team avaliara em ate [PREENCHER — SLA, ex.: 5 dias uteis]
4. **Se aprovado:** Escreva um RFC usando o template [PREENCHER — link para RFC template]
5. **Review do RFC:** Periodo de [PREENCHER — dias] para feedback
6. **Implementacao:** Siga as guidelines de design e codigo abaixo

### 7. Guidelines de Design

**Para Figma:**
- [ ] Use a biblioteca de tokens do DS — [PREENCHER — link]
- [ ] Siga o naming convention: [PREENCHER — formato]
- [ ] Inclua todas as variantes e estados: [PREENCHER — lista minima]
- [ ] Documente props e comportamentos em annotations
- [ ] Organize no page template do DS: [PREENCHER — estrutura]
- [ ] Use auto-layout para todos os componentes

**Criterios de qualidade (design):**
- [ ] Funciona em light e dark theme
- [ ] Responsivo (mobile, tablet, desktop)
- [ ] Acessivel (contraste, labels, keyboard)
- [ ] Consistente com outros componentes do DS
- [ ] Inclui empty, loading, error states

### 8. Guidelines de Codigo

**Para desenvolvimento:**
- [ ] Branch a partir de [PREENCHER — branch base, ex.: main / develop]
- [ ] Siga a estrutura de arquivos: [PREENCHER — padrao do repo]
- [ ] Use tokens em vez de valores hardcoded
- [ ] Escreva testes: [PREENCHER — unit, visual regression, a11y]
- [ ] Adicione Storybook stories para cada variante e estado
- [ ] Documente a API (props) no formato padrao
- [ ] Garanta que `prefers-reduced-motion` e respeitado

**Naming conventions (codigo):**
- Componentes: [PREENCHER — ex.: PascalCase]
- Props: [PREENCHER — ex.: camelCase]
- CSS/Tokens: [PREENCHER — ex.: kebab-case]
- Arquivos: [PREENCHER — ex.: kebab-case.tsx]

### 9. Review Process

| Etapa            | Reviewer(s)                | Criterios                           | SLA           |
|------------------|----------------------------|-------------------------------------|---------------|
| Design review    | [PREENCHER — quem revisa]  | [PREENCHER — criterios de design]   | [PREENCHER]   |
| Code review      | [PREENCHER — quem revisa]  | [PREENCHER — criterios de codigo]   | [PREENCHER]   |
| A11y review      | [PREENCHER — quem revisa]  | [PREENCHER — criterios de a11y]     | [PREENCHER]   |
| Final approval   | [PREENCHER — DS lead]      | [PREENCHER — criterios finais]      | [PREENCHER]   |

### 10. Contato e Suporte

| Canal                    | Uso                                  | SLA de resposta    |
|--------------------------|--------------------------------------|--------------------|
| [PREENCHER — Slack]      | [PREENCHER — duvidas rapidas]        | [PREENCHER]        |
| [PREENCHER — Office hours]| [PREENCHER — pairing, demos]        | [PREENCHER]        |
| [PREENCHER — Issue tracker]| [PREENCHER — bugs, requests]       | [PREENCHER]        |
| [PREENCHER — Email]      | [PREENCHER — assuntos formais]       | [PREENCHER]        |

**DS Team:**

| Nome             | Papel                 | Contato                  |
|------------------|-----------------------|--------------------------|
| [PREENCHER]      | [PREENCHER — DS Lead] | [PREENCHER — handle]     |
| [PREENCHER]      | [PREENCHER — Designer]| [PREENCHER]              |
| [PREENCHER]      | [PREENCHER — Dev]     | [PREENCHER]              |

## Example (Parcialmente Preenchido)

**Processo resumido:** Designer identifica necessidade de Tooltip component -> Abre request no Slack #design-system -> DS team triagem em 3 dias -> Aprovado -> RFC escrito e revisado em 5 dias -> Design em Figma + Code em React -> Review de design (2 dias) + Code review (3 dias) -> Merge + Release na proxima minor version.

## Notes

- Contribuicoes sao incentivadas mas devem seguir os padroes de qualidade do DS.
- O DS team tem a palavra final sobre o que entra no sistema.
- Contribuicoes rejeitadas recebem feedback detalhado com alternativas.
- Reconheca publicamente os contribuidores — isso incentiva mais participacao.
- Mantenha este guia atualizado — um guia desatualizado e pior que nenhum guia.
