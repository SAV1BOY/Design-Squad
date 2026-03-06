# Design System Governance

## Metadata

| Campo         | Valor                                          |
| ------------- | ---------------------------------------------- |
| Categoria     | Process                                        |
| Complexidade  | Alta                                           |
| Autor         | Design Squad                                   |
| Versao        | 1.0                                            |
| Ultima revisao| 2026-03-06                                     |
| Tags          | governance, rfc, versioning, contribution, releases |

## Concept

Design system governance e o conjunto de processos, papeis e regras que garantem a evolucao
saudavel, consistente e escalavel de um design system. Sem governanca, o sistema se fragmenta
entre decisoes locais descoordenadas. Com governanca excessiva, ele se torna um gargalo.

### Pilares de Governanca

1. **RFC (Request for Comments)**: processo formal para propor mudancas.
2. **Versioning**: controle de versoes semantico para tokens, componentes e patterns.
3. **Releases**: ciclo previsivel de publicacao com changelog.
4. **Ownership**: papeis claros de quem decide, quem implementa, quem aprova.
5. **Contribution**: modelo aberto e documentado para contribuicoes externas ao core team.

### Modelos de Governanca

| Modelo        | Descricao                                      | Quando usar                        |
| ------------- | ---------------------------------------------- | ---------------------------------- |
| Centralized   | Core team decide e implementa tudo             | Times pequenos, sistema nascente   |
| Federated     | Core team governa, squads contribuem           | Times medios, sistema maduro       |
| Distributed   | Squads tem autonomia com guidelines            | Organizacoes grandes, cultura forte|

## When to Use

- Quando o design system atende mais de 2 squads ou produtos.
- Quando ha conflitos frequentes sobre como componentes devem funcionar.
- Quando contribuicoes externas estao quebrando consistencia.
- Quando releases sao imprevisiveis e causam regressoes.
- Quando ninguem sabe quem e responsavel por decisoes de design system.

## How to Apply

### 1. Processo de RFC

```
1. Autor cria RFC document com:
   - Problema ou necessidade
   - Proposta de solucao (design + specs)
   - Alternativas consideradas
   - Impacto em componentes existentes
   - Migration path se for breaking change

2. Review period: 5 dias uteis para comentarios
   - Design system core team (obrigatorio)
   - Squads afetadas (notificacao)
   - Qualquer pessoa interessada (aberto)

3. Decisao:
   - Aprovado -> entra no backlog com prioridade
   - Aprovado com alteracoes -> revisao e re-submit
   - Rejeitado com justificativa -> documentado para futuro

4. Implementacao segue o fluxo normal de desenvolvimento
```

### 2. Semantic Versioning

```
MAJOR.MINOR.PATCH

MAJOR (breaking): remocao de componente, mudanca de API, token renomeado
MINOR (feature):  novo componente, nova variante, novo token
PATCH (fix):      bug fix, ajuste de cor, correcao de spacing

Exemplos:
  v2.0.0 -> Redesign de tokens de cor (breaking)
  v2.1.0 -> Novo componente DatePicker (feature)
  v2.1.1 -> Fix contraste do Button disabled (fix)
```

### 3. Release Cycle

```
Cadencia recomendada:
  PATCH:  weekly (toda segunda-feira)
  MINOR:  bi-weekly (a cada sprint)
  MAJOR:  quarterly (com 30 dias de deprecation notice)

Cada release inclui:
  - Changelog detalhado (o que mudou, por que, como migrar)
  - Migration guide para breaking changes
  - Versao anterior disponivel por pelo menos 90 dias
```

### 4. Ownership Model (RACI)

| Atividade           | Responsible   | Accountable  | Consulted    | Informed     |
| ------------------- | ------------- | ------------ | ------------ | ------------ |
| Token changes       | Core team     | DS Lead      | All squads   | Engineering  |
| New component       | Contributor   | Core team    | Consumers    | All squads   |
| Breaking change     | Core team     | DS Lead      | All squads   | Leadership   |
| Bug fix             | Any developer | Core team    | Reporter     | Consumers    |
| Documentation       | Core team     | DS Lead      | Contributors | All squads   |

### 5. Contribution Model

```
1. Contributor propoe via RFC ou issue
2. Core team faz triagem em ate 3 dias uteis
3. Se aprovado, contributor implementa com pair do core team
4. Code review + design review pelo core team
5. Merge, release e comunicacao
```

## Key Principles

- **Aberto por default**: qualquer pessoa pode propor mudancas via RFC.
- **Transparencia**: todas as decisoes documentadas e acessiveis.
- **Previsibilidade**: releases em cadencia fixa, nunca surpresas.
- **Backward compatibility**: breaking changes sao excecao, nao regra.
- **Documentacao como produto**: docs sao tao importantes quanto codigo.
- **Feedback loop**: metricas de adocao e satisfacao orientam prioridades.

## Examples

### RFC Template

```markdown
# RFC: [Titulo]
## Problema — [Descricao do problema ou necessidade]
## Proposta — [Solucao com specs visuais e tecnicas]
## Alternativas — [Consideradas e por que descartadas]
## Impacto — Componentes afetados, breaking changes, migration path
## Timeline — [Estimativa de esforco]
```

### Changelog Entry

```markdown
## v2.3.0 (2026-03-06)
### New — Componente `Stepper` (#RFC-042), variante `ghost` Button (#RFC-039)
### Changed — Token `spacing-md` de 16px para 20px (minor)
### Deprecated — `Badge` outline sera removido na v3.0.0
### Fixed — Contraste do `Input` disabled no dark mode (#BUG-118)
```

## Common Pitfalls

| Erro                                | Consequencia                        | Correcao                                |
| ----------------------------------- | ----------------------------------- | --------------------------------------- |
| Governanca sem enforcement          | Regras ignoradas                    | Integrar checks no CI/CD pipeline       |
| RFC muito burocrático               | Pessoas bypassing o processo        | Simplificar para small changes          |
| Sem deprecation period              | Breaking changes surpresa           | Minimo 30 dias de aviso                 |
| Core team como gargalo              | Contribuicoes represadas            | Escalar para modelo federated           |
| Sem metricas de adocao              | Investimento sem visibilidade       | Tracking de usage por componente        |
| Documentacao desatualizada          | Desconfianca no sistema             | Docs review em cada release             |

## Cross-References

- [Design Review and Critique](./design-review-and-critique.md) — review como parte do processo de RFC.
- [Design Maturity Model](./design-maturity-model.md) — governanca como indicador de maturidade.
- [Dark Mode System](./dark-mode-system.md) — exemplo de token governance.
- [Responsive Design System](./responsive-design-system.md) — breakpoint tokens sob governanca.
- [Motion Design System](./motion-design-system.md) — motion tokens sob governanca.
