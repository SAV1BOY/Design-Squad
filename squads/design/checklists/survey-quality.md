# Survey Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** UX Research
- **Version:** 1.0.0
- **Owner Agent:** Research Agent

## Objective
Garantir que questionarios e surveys produzam dados confiaveis, validos e representativos da populacao-alvo.
Um survey bem construido equilibra rigor metodologico com uma experiencia de preenchimento agradavel.

## When to Apply
- Ao criar qualquer tipo de questionario ou survey para usuarios.
- Ao revisar surveys antes do lancamento para coleta de dados.
- Quando se precisa validar quantitativamente insights qualitativos.

## Criteria
- [ ] O objetivo do survey esta claramente definido e alinhado com as research questions
- [ ] O publico-alvo e o metodo de distribuicao estao definidos
- [ ] O tempo estimado de preenchimento esta informado na introducao e nao excede 10 minutos
- [ ] As perguntas seguem uma ordem logica, do geral para o especifico
- [ ] Cada pergunta mede apenas um conceito (evita double-barreled questions)
- [ ] As escalas de resposta sao consistentes e balanceadas ao longo do survey
- [ ] Opcoes como "Nao se aplica" ou "Prefiro nao responder" estao disponiveis quando pertinente
- [ ] As perguntas obrigatorias sao apenas as essenciais para a analise
- [ ] O survey foi testado em diferentes devices (mobile, desktop, tablet)
- [ ] A linguagem e acessivel e livre de jargoes tecnicos desnecessarios
- [ ] Existe randomizacao de opcoes para reduzir order bias quando aplicavel
- [ ] A logica de branching (skip logic) esta configurada e testada
- [ ] A introducao explica o proposito, anonimato e uso dos dados
- [ ] Um pilot test com 5-10 pessoas foi realizado antes do lancamento
- [ ] O plano de analise estatistica esta definido previamente
- [ ] A meta de sample size foi calculada para garantir significancia estatistica

## Severity Guide

### Critico
- Presenca de double-barreled questions comprometendo a validade dos dados.
- Sample size planejado insuficiente para analise estatistica.
- Ausencia de informacao sobre anonimato e uso dos dados.

### Major
- Escalas de resposta inconsistentes entre perguntas similares.
- Survey nao testado em mobile quando o publico e predominantemente mobile.
- Tempo de preenchimento excede 15 minutos sem justificativa.

### Minor
- Falta de randomizacao de opcoes em perguntas nao criticas.
- Pequenos ajustes de linguagem necessarios apos pilot test.
- Branching logic com caminhos nao otimizados.

## Cross-References
- [Research Plan Quality](research-plan-quality.md)
- [Synthesis Quality](synthesis-quality.md)
- [Content Design Quality](content-design-quality.md)
- [Accessibility Quality](accessibility-quality.md)
- [Localization Quality](localization-quality.md)
