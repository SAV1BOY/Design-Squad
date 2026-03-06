# UI Visual Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Visual Design
- **Version:** 1.0.0
- **Owner Agent:** Visual Design Agent

## Objective
Assegurar que o design visual do produto seja esteticamente coerente, alinhado com a identidade da marca e funcional.
A qualidade visual impacta diretamente a percepcao de credibilidade e a usabilidade do produto.

## When to Apply
- Ao criar composicoes visuais de alta fidelidade para telas e componentes.
- Ao revisar entregas visuais antes do handoff para desenvolvimento.
- Ao avaliar a consistencia visual entre diferentes partes do produto.

## Criteria
- [ ] O design segue as guidelines da brand identity (logo, cores, tom visual)
- [ ] A hierarquia visual esta clara com uso adequado de tamanho, peso, cor e espacamento
- [ ] O contraste entre elementos atende aos requisitos de accessibility (WCAG AA minimo)
- [ ] Os espacamentos seguem a escala definida no design system (spacing scale)
- [ ] As imagens e ilustracoes possuem qualidade adequada e estao otimizadas
- [ ] A iconografia e consistente em estilo, tamanho e peso de linha
- [ ] Os componentes visuais estao alinhados ao grid definido
- [ ] O uso de sombras, bordas e elevacao segue um sistema coerente
- [ ] Os estados visuais de componentes interativos estao todos definidos
- [ ] A paleta de cores esta aplicada de acordo com o color system documentado
- [ ] A tipografia segue a type scale e as regras de uso definidas
- [ ] Os elementos visuais nao competem por atencao, ha um foco claro por tela
- [ ] O design e pixel-perfect nos detalhes de alinhamento e espacamento
- [ ] O tratamento visual e consistente entre telas do mesmo flow
- [ ] Os assets estao organizados e nomeados conforme convencao do time
- [ ] O design foi revisado em diferentes resolucoes e densidades de tela

## Severity Guide

### Critico
- Contraste insuficiente que compromete a legibilidade (falha WCAG AA).
- Inconsistencia visual grave entre telas do mesmo flow.
- Hierarquia visual confusa que prejudica a compreensao do conteudo.

### Major
- Componentes fora do grid sem justificativa de design.
- Iconografia com estilos misturados no mesmo contexto.
- Uso de cores fora da paleta definida sem documentacao.

### Minor
- Pequenos desalinhamentos em resolucoes especificas.
- Assets nao nomeados conforme convencao mas funcionais.
- Sombras levemente inconsistentes entre componentes similares.

## Cross-References
- [Typography Quality](typography-quality.md)
- [Color System Quality](color-system-quality.md)
- [Component Spec Quality](component-spec-quality.md)
- [Design System Quality](design-system-quality.md)
- [Accessibility Quality](accessibility-quality.md)
