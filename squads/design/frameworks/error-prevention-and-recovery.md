# Error Prevention and Recovery

## Metadata

| Campo         | Valor                                        |
| ------------- | -------------------------------------------- |
| Categoria     | UX Pattern                                   |
| Complexidade  | Media                                        |
| Autor         | Design Squad                                 |
| Versao        | 1.0                                          |
| Ultima revisao| 2026-03-06                                   |
| Tags          | error-handling, prevention, recovery, resilience |

## Concept

Error prevention and recovery e um framework que estrutura a abordagem de erros em tres fases:
**prevenir**, **explicar** e **recuperar**. O design de interfaces resilientes reconhece que erros
sao inevitaveis e que a qualidade da experiencia depende tanto de evita-los quanto de lidar com
eles graciosamente.

A abordagem se apoia na Heuristica 5 de Nielsen (Error Prevention) e na Heuristica 9
(Help Users Recognize, Diagnose, and Recover from Errors).

### As Tres Fases

1. **Prevenir** — Eliminar condicoes que levam ao erro antes que ele ocorra.
2. **Explicar** — Quando o erro ocorre, comunicar o que aconteceu de forma clara e humana.
3. **Recuperar** — Oferecer caminhos concretos para resolver a situacao e voltar ao fluxo.

### Taxonomia de Erros

- **Slips**: erros de atencao — o usuario sabe o que fazer mas erra na execucao.
- **Mistakes**: erros de intencao — o usuario tem um modelo mental incorreto.
- **System errors**: falhas de infraestrutura, timeout, indisponibilidade.
- **Validation errors**: dados invalidos ou incompletos.

## When to Use

- Em toda interface que aceita input do usuario (formularios, uploads, configuracoes).
- Em fluxos criticos (pagamento, exclusao de dados, envio irreversivel).
- Em sistemas com dependencias externas (APIs, servicos de terceiros).
- Quando metricas mostram alta taxa de erro ou abandono em determinado fluxo.
- Em operacoes destrutivas (delete, overwrite, reset).

## How to Apply

### Fase 1 — Prevencao

1. **Constraints**: limitar inputs validos (date pickers em vez de texto livre, dropdowns).
2. **Defaults inteligentes**: pre-preencher campos com valores mais comuns.
3. **Inline validation**: validar em tempo real, nao apenas no submit.
4. **Confirmacao em acoes destrutivas**: dialog com descricao do impacto.
5. **Undo over confirmation**: preferir undo a "Tem certeza?" quando possivel.
6. **Disabled states claros**: desabilitar botoes com tooltip explicando o motivo.

### Fase 2 — Explicacao

1. **Linguagem humana**: "Nao conseguimos salvar suas alteracoes" em vez de "Error 500".
2. **Especificidade**: indicar exatamente qual campo ou acao causou o problema.
3. **Proximidade**: exibir a mensagem perto do ponto de erro.
4. **Tom adequado**: nao culpar o usuario; assumir responsabilidade pelo sistema.
5. **Visibilidade**: usar cor, icone e posicao para garantir que a mensagem seja vista.

### Fase 3 — Recuperacao

1. **Sugestoes de correcao**: "Voce quis dizer joao@gmail.com?".
2. **Preservar dados**: nunca limpar o formulario apos um erro.
3. **Retry automatico**: para erros de rede, tentar novamente silenciosamente.
4. **Fallback gracioso**: degradar funcionalidade em vez de quebrar completamente.
5. **Caminho alternativo**: "Tente novamente ou entre em contato com o suporte".
6. **Auto-save**: salvar rascunhos periodicamente para evitar perda de dados.

## Key Principles

- **Prevenir e melhor que remediar**: invista mais em prevencao do que em mensagens de erro.
- **Preservar o trabalho do usuario**: dados inseridos nunca devem ser perdidos por erro do sistema.
- **Erros sao oportunidades**: cada erro e um sinal de design para melhorar.
- **Tom humano e nao tecnico**: mensagens de erro sao microcopy — trate como conteudo editorial.
- **Acessibilidade**: usar `aria-live="assertive"` para anunciar erros, `aria-invalid` para campos.
- **Logging**: todo erro de usuario deve gerar dados para analise e melhoria.

## Examples

### Formulario de Pagamento

```
Prevencao:  Mascara de cartao, validacao de Luhn em tempo real, dropdown de bandeira
Explicacao: "O numero do cartao parece incorreto. Verifique os digitos e tente novamente."
Recuperacao: Campo mantem o valor digitado, cursor posicionado no digito errado
```

### Upload de Arquivo

```
Prevencao:  Filtro de tipo e tamanho maximo no seletor, drag area com instrucoes
Explicacao: "O arquivo excede o limite de 10MB. Tamanho atual: 14.3MB."
Recuperacao: Sugestao de compressao, link para ferramenta de redimensionamento
```

### Exclusao de Conta

```
Prevencao:  Requer digitacao do email para confirmar, cooldown de 14 dias
Explicacao: "Sua conta sera desativada agora e excluida permanentemente em 14 dias."
Recuperacao: Email com link para cancelar exclusao durante o periodo de cooldown
```

## Common Pitfalls

| Erro                                | Consequencia                          | Correcao                                 |
| ----------------------------------- | ------------------------------------- | ---------------------------------------- |
| Mensagem generica "Algo deu errado" | Usuario sem acao possivel             | Ser especifico sobre causa e solucao     |
| Validacao apenas no submit          | Frustacao acumulada                   | Validacao inline em blur ou debounce     |
| Limpar formulario apos erro         | Perda de dados do usuario             | Preservar todos os campos preenchidos    |
| Jargao tecnico em mensagens         | Confusao e inseguranca                | Revisar com content designer             |
| Error state sem foco automatico     | Usuarios de screen reader nao percebem| Focus management + aria-live             |
| Nao logar erros do lado do cliente  | Problemas invisiveis para o time      | Integrar error tracking (Sentry, etc.)   |

## Cross-References

- [Content Design Microcopy](./content-design-microcopy.md) — tom e linguagem de mensagens de erro.
- [Empty States and Loading States](./empty-states-and-loading-states.md) — error states como caso especial.
- [Accessibility WCAG AA](./accessibility-wcag-aa.md) — requisitos de acessibilidade para erros.
- [Progressive Disclosure](./progressive-disclosure.md) — revelar ajuda contextual para correcao.
- [SUS System Usability Scale](./sus-system-usability-scale.md) — medir impacto de erros na usabilidade.
