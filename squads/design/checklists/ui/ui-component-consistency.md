# UI Component Consistency

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Visual Design                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | UI Lead                        |

## Objective

Verificar se os componentes visuais do produto sao consistentes em aparencia, comportamento
e implementacao ao longo de todas as telas e fluxos. Consistencia reduz a carga cognitiva
do usuario, acelera o aprendizado da interface e diminui custo de manutencao.

## When to Apply

- Em auditorias visuais trimestrais do produto.
- Ao integrar componentes de diferentes squads ou produtos.
- Quando usuarios reportam experiencia fragmentada entre telas.
- Em revisoes de design pre-handoff para garantir uso correto de componentes.

## Criteria

- [ ] Botoes usam os mesmos estilos (size, color, border-radius) em todas as telas.
- [ ] Inputs e formularios possuem aparencia e comportamento identicos em todo o produto.
- [ ] Tipografia segue a escala definida sem variacoes ad-hoc.
- [ ] Cores sao aplicadas via tokens, sem valores hardcoded ou hex diretos.
- [ ] Espacamento interno e externo de componentes segue os tokens de spacing.
- [ ] Sombras (elevation/shadow) seguem a escala definida no design system.
- [ ] Border-radius e consistente dentro de cada familia de componentes.
- [ ] Componentes de mesmo tipo possuem o mesmo comportamento de interacao.
- [ ] Modais, drawers e overlays seguem o mesmo padrao de abertura e fechamento.
- [ ] Tabelas e listas utilizam mesmo padrao de header, row e paginacao.
- [ ] Avatares, badges e tags seguem tamanhos e estilos padronizados.
- [ ] Componentes de navegacao (tabs, menus, breadcrumbs) sao consistentes.
- [ ] Existe checklist de componentes criticos validados em cada release.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Mesmo componente com aparencia completamente diferente entre telas.       |
| Major    | Cores ou tipografia hardcoded fora do sistema de tokens.                 |
| Minor    | Desvios menores de border-radius ou sombra em componentes isolados.      |
| Info     | Oportunidade de padronizar componentes de baixa frequencia de uso.       |

## Cross-References

- `ui/ui-spacing-and-grid.md` — Espacamento e grid.
- `frost/frost-component-inventory-audit.md` — Inventario de componentes.
- `frost/frost-pattern-library-quality.md` — Qualidade da pattern library.
- `design-system/ds-design-code-sync-audit.md` — Sincronizacao design-code.
