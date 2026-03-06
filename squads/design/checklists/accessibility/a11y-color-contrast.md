# A11Y Color Contrast

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Accessibility                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Accessibility Lead             |

## Objective

Verificar se todas as combinacoes de cor utilizadas no produto atendem aos requisitos
minimos de contraste definidos pelas WCAG. Contraste adequado e essencial para
legibilidade em diferentes condicoes de iluminacao, para usuarios com baixa visao
e para pessoas com daltonismo.

## When to Apply

- Ao definir ou atualizar paleta de cores do design system.
- Em auditorias de acessibilidade visual.
- Ao implementar dark mode ou novos temas.
- Quando usuarios reportam dificuldade de leitura.

## Criteria

- [ ] Texto normal (abaixo de 18pt) possui contraste minimo de 4.5:1 contra o background.
- [ ] Texto grande (18pt+ ou 14pt bold+) possui contraste minimo de 3:1.
- [ ] Elementos graficos e UI components possuem contraste minimo de 3:1.
- [ ] Placeholder text em inputs atende contraste minimo de 4.5:1.
- [ ] Links sao distinguiveis do texto ao redor por contraste ou estilo (underline).
- [ ] Cores semanticas (success, error, warning, info) atendem contraste em ambos os temas.
- [ ] Bordas de inputs e controles de formulario possuem contraste suficiente.
- [ ] Icones informativos atendem contraste minimo de 3:1.
- [ ] Texto sobre imagens possui overlay ou sombra para garantir legibilidade.
- [ ] Graficos e visualizacoes de dados usam paleta colorblind-safe.
- [ ] Contraste foi validado com ferramenta automatizada (Colour Contrast Analyser, axe).
- [ ] Todas as combinacoes de cor foram testadas em simulador de daltonismo.
- [ ] A paleta de cores inclui pares de cores pre-aprovados para uso em texto/background.
- [ ] Disabled states possuem contraste suficiente para serem percebidos como desabilitados.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Texto com contraste abaixo de 3:1 em fluxos criticos.                   |
| Major    | Elementos UI ou graficos informativos abaixo de 3:1 de contraste.        |
| Minor    | Placeholder text com contraste insuficiente ou icones decorativos.        |
| Info     | Oportunidade de atingir AAA (7:1) ou expandir paleta colorblind-safe.    |

## Cross-References

- `accessibility/a11y-wcag-audit.md` — Auditoria WCAG.
- `ui/ui-dark-mode-quality.md` — Qualidade do dark mode.
- `ui/ui-visual-hierarchy.md` — Hierarquia visual.
- `ui/ui-data-visualization-quality.md` — Qualidade de visualizacao de dados.
