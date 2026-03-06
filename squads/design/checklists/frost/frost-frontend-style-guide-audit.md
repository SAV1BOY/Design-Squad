# Frost Frontend Style Guide Audit

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Frost                          |
| Domain      | Frontend Standards             |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Frost Lead                     |

## Objective

Verificar se o style guide de frontend esta atualizado, completo e alinhado com as
definicoes do design system. O style guide serve como referencia para desenvolvedores
implementarem componentes de forma consistente, garantindo paridade entre design e codigo.

## When to Apply

- Ao atualizar o design system com novos tokens ou componentes.
- Em revisoes trimestrais de alinhamento design-code.
- Quando novos desenvolvedores ingressam nos squads consumidores.
- Apos migracoes de framework ou biblioteca de estilos.

## Criteria

- [ ] O style guide cobre todos os tokens de design: cores, tipografia, espacamento, sombras e bordas.
- [ ] Existe mapeamento claro entre tokens do Figma e variaveis CSS/JS correspondentes.
- [ ] Convencoes de nomenclatura de classes CSS seguem metodologia definida (BEM, utility-first, etc.).
- [ ] O style guide inclui exemplos de uso responsivo com breakpoints oficiais.
- [ ] Regras de z-index sao documentadas com escala padronizada.
- [ ] Convencoes de animacao e transicao estao documentadas com duracao e easing.
- [ ] O style guide proibe magic numbers e fornece alternativas via tokens.
- [ ] Existe lint configurado para validar conformidade com o style guide automaticamente.
- [ ] Temas (light, dark, high-contrast) estao documentados com instrucoes de implementacao.
- [ ] O style guide inclui secao de anti-patterns com exemplos do que evitar.
- [ ] Performance guidelines para CSS sao documentadas (evitar !important, seletores profundos).
- [ ] O style guide e acessivel online e possui busca funcional.
- [ ] Atualizacoes do style guide sao comunicadas via changelog.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Tokens no codigo divergem dos tokens no design tool.                     |
| Major    | Style guide desatualizado em relacao a versao corrente do sistema.        |
| Minor    | Ausencia de exemplos de anti-patterns ou guidelines de performance.       |
| Info     | Sugestao de automacao adicional via linting ou formatacao.                |

## Cross-References

- `frost/frost-design-system-governance.md` — Governanca do design system.
- `frost/frost-documentation-and-adoption.md` — Documentacao e adocao.
- `design-system/ds-token-architecture.md` — Arquitetura de tokens.
- `design-system/ds-design-code-sync-audit.md` — Sincronizacao design-code.
