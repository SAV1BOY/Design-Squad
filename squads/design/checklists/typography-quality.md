# Typography Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Visual Design
- **Version:** 1.0.0
- **Owner Agent:** Typography Agent

## Objective
Garantir que o sistema tipografico do produto seja legivel, acessivel, hierarquicamente claro e consistente em todas as plataformas.
A tipografia e o principal veiculo de comunicacao em interfaces digitais.

## When to Apply
- Ao definir ou revisar o type system de um produto ou design system.
- Ao criar novas telas que introduzem novos usos tipograficos.
- Ao avaliar a legibilidade em diferentes devices e contextos.

## Criteria
- [ ] A type scale esta definida com uma razao matematica consistente (modular scale)
- [ ] Os niveis hierarquicos (heading 1-6, body, caption, overline) estao claramente diferenciados
- [ ] As fontes selecionadas possuem licenca adequada para uso digital
- [ ] O font stack inclui fallback fonts apropriadas para cada plataforma
- [ ] O line-height (leading) garante legibilidade em blocos de texto (minimo 1.5x para body)
- [ ] O comprimento de linha (line length) esta entre 45-75 caracteres para body text
- [ ] O espacamento entre letras (letter-spacing) esta ajustado para headings e uppercase
- [ ] O contraste tipografico atende WCAG AA (4.5:1 para body, 3:1 para large text)
- [ ] O tamanho minimo de fonte e 16px para body text em interfaces web
- [ ] O sistema tipografico funciona bem em dark mode e light mode
- [ ] As regras de truncamento (truncation) e overflow de texto estao definidas
- [ ] O uso de font weights esta limitado a 2-3 pesos por tipo para manter clareza
- [ ] Os estilos tipograficos estao tokenizados no design system
- [ ] A tipografia e testada e legivel em dispositivos de baixa resolucao
- [ ] As regras de uso (quando usar cada estilo) estao documentadas com exemplos

## Severity Guide

### Critico
- Tamanho de fonte body abaixo de 14px comprometendo legibilidade.
- Contraste tipografico abaixo dos niveis WCAG AA.
- Fontes sem licenca adequada para uso comercial.

### Major
- Line-height insuficiente em blocos de texto longos.
- Line length excedendo 85 caracteres em body text.
- Hierarquia tipografica confusa entre niveis.

### Minor
- Fallback fonts nao definidas mas fonte principal carrega adequadamente.
- Letter-spacing nao ajustado para uppercase text.
- Documentacao de uso tipografico incompleta.

## Cross-References
- [UI Visual Quality](ui-visual-quality.md)
- [Color System Quality](color-system-quality.md)
- [Design System Quality](design-system-quality.md)
- [Token Quality](token-quality.md)
- [Accessibility Quality](accessibility-quality.md)
