# UI Data Visualization Quality

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Data Visualization             |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | UI Lead                        |

## Objective

Avaliar a qualidade das visualizacoes de dados no produto, verificando se graficos,
tabelas e dashboards comunicam informacao de forma precisa, acessivel e esteticamente
coerente. Visualizacoes de dados eficazes permitem tomada de decisao rapida e reduzem
interpretacoes erroneas.

## When to Apply

- Ao projetar novos graficos, charts ou dashboards.
- Em auditorias de qualidade de interfaces de analytics.
- Quando usuarios reportam dificuldade em interpretar dados.
- Ao padronizar biblioteca de chart components.

## Criteria

- [ ] O tipo de grafico escolhido e adequado para o tipo de dado representado.
- [ ] Eixos possuem labels claras com unidade de medida e escala.
- [ ] Eixo Y comeca em zero quando apropriado para evitar distorcao visual.
- [ ] Cores sao distinguiveis entre si e acessiveis para daltonismo (colorblind-safe palette).
- [ ] Legends sao posicionadas de forma nao obstrutiva e proximas ao dado.
- [ ] Tooltips fornecem detalhes precisos ao interagir com pontos de dados.
- [ ] Dados vazios ou ausentes sao tratados com mensagem informativa.
- [ ] O grafico e responsivo e legivel em diferentes tamanhos de tela.
- [ ] Numeros sao formatados de acordo com locale (separadores, moeda, datas).
- [ ] Existe opcao de exportar dados ou visualizacao quando relevante.
- [ ] Animacoes de transicao de dados sao suaves e nao distraem.
- [ ] Comparacoes temporais utilizam mesma escala para evitar vieses.
- [ ] Visualizacoes sao acessiveis via screen reader com dados em tabela alternativa.
- [ ] A paleta de cores segue os tokens do design system.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Grafico distorce dados (eixo truncado) ou cores indistinguiveis.         |
| Major    | Ausencia de labels em eixos ou grafico inadequado para o tipo de dado.   |
| Minor    | Tooltips ausentes ou formatacao de numeros inconsistente.                |
| Info     | Oportunidade de adicionar export ou melhorar animacoes de transicao.     |

## Cross-References

- `accessibility/a11y-color-contrast.md` — Contraste de cores.
- `accessibility/a11y-screen-reader-audit.md` — Auditoria de screen reader.
- `ui/ui-component-consistency.md` — Consistencia de componentes.
- `ui/ui-dark-mode-quality.md` — Qualidade do dark mode.
