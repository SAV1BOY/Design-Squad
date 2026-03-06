# Malouf Ethics and User Impact

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Malouf                         |
| Domain      | Design Ethics                  |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Malouf Lead                    |

## Objective

Avaliar se as decisoes de design consideram impactos eticos, sociais e psicologicos
sobre os usuarios. Design etico vai alem da usabilidade e questiona se o produto
respeita a autonomia, privacidade, bem-estar e dignidade dos usuarios, evitando
dark patterns e manipulacao.

## When to Apply

- Em revisoes de design de features que envolvem dados pessoais ou financeiros.
- Ao projetar fluxos de engajamento, retencao ou monetizacao.
- Quando ha risco de impacto negativo sobre grupos vulneraveis.
- Em auditorias anuais de etica em design.

## Criteria

- [ ] O design respeita a autonomia do usuario, oferecendo escolhas claras e reversiveis.
- [ ] Nenhum dark pattern e utilizado (confirmshaming, roach motel, hidden costs, etc.).
- [ ] Consentimento e obtido de forma explicita, informada e granular.
- [ ] Dados coletados sao minimizados ao estritamente necessario para a funcionalidade.
- [ ] O design considera o impacto sobre saude mental (uso excessivo, FOMO, ansiedade).
- [ ] Linguagem utilizada e honesta, transparente e nao manipuladora.
- [ ] Fluxos de cancelamento sao tao simples quanto fluxos de ativacao.
- [ ] O produto e acessivel a pessoas com diferentes capacidades e contextos.
- [ ] Existe avaliacao de impacto sobre grupos sub-representados ou vulneraveis.
- [ ] Notificacoes e interrupcoes respeitam o tempo e atencao do usuario.
- [ ] O design nao explora vieses cognitivos para direcionar decisoes do usuario.
- [ ] Existe processo de revisao etica como parte do ciclo de design.
- [ ] Metricas de sucesso incluem indicadores de bem-estar do usuario, nao apenas engajamento.
- [ ] A equipe tem treinamento em design etico e awareness de dark patterns.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Dark patterns identificados ou dados coletados sem consentimento claro.  |
| Major    | Fluxo de cancelamento significativamente mais dificil que o de ativacao. |
| Minor    | Notificacoes excessivas ou metricas focadas apenas em engajamento.       |
| Info     | Oportunidade de adicionar indicadores de bem-estar ou treinamento etico. |

## Cross-References

- `malouf/malouf-ux-strategy-audit.md` — Estrategia de UX.
- `malouf/malouf-design-quality-principles-audit.md` — Principios de qualidade.
- `accessibility/a11y-wcag-audit.md` — Auditoria WCAG.
- `research/research-consent-and-privacy.md` — Consentimento e privacidade.
