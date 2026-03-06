# Prototyping Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Interaction Design
- **Version:** 1.0.0
- **Owner Agent:** Prototyping Agent

## Objective
Assegurar que prototipos sejam eficazes como ferramenta de comunicacao, teste e validacao de conceitos de design.
Um prototipo de qualidade equilibra fidelidade com velocidade de iteracao conforme o objetivo de uso.

## When to Apply
- Ao criar prototipos para testes de usabilidade.
- Ao construir prototipos para apresentacao a stakeholders.
- Ao preparar prototipos de interacao para handoff ao desenvolvimento.

## Criteria
- [ ] O nivel de fidelidade (low, mid, high) e adequado ao objetivo do prototipo
- [ ] Os user flows principais estao completamente navegaveis no prototipo
- [ ] As interacoes simulam o comportamento real do produto com fidelidade suficiente
- [ ] Os hotspots e areas clicaveis estao dimensionados adequadamente (minimo 44px em mobile)
- [ ] Os dead ends sao evitados — todo caminho tem continuidade ou saida clara
- [ ] Os estados intermediarios (loading, transitions) estao representados quando relevantes
- [ ] O prototipo funciona no device-alvo do teste (mobile, desktop, tablet)
- [ ] Os dados utilizados sao realistas e representativos do uso real
- [ ] O prototipo inclui error states para os cenarios que serao testados
- [ ] A navegacao dentro do prototipo e intuitiva para o participante do teste
- [ ] As animacoes e transicoes comunicam relacoes espaciais e hierarquicas
- [ ] O prototipo esta organizado com flows nomeados e documentados
- [ ] Existe um roteiro de demonstracao (demo script) para apresentacoes
- [ ] O prototipo foi testado internamente antes do uso com participantes
- [ ] Os links de compartilhamento estao configurados com permissoes adequadas

## Severity Guide

### Critico
- User flows principais com dead ends que impedem a conclusao do teste.
- Nivel de fidelidade inadequado que confunde participantes sobre o que testar.
- Prototipo nao funcional no device-alvo do teste.

### Major
- Ausencia de error states em cenarios que serao explorados no teste.
- Dados visivelmente falsos que distraem o participante da tarefa.
- Hotspots muito pequenos causando dificuldade de interacao.

### Minor
- Transicoes ausentes entre telas mas flow compreensivel.
- Organizacao interna do prototipo poderia ser mais clara.
- Demo script nao documentado para apresentacoes internas.

## Cross-References
- [User Flow Quality](user-flow-quality.md)
- [Usability Test Quality](usability-test-quality.md)
- [Wireframe Quality](wireframe-quality.md)
- [Motion Quality](motion-quality.md)
- [Handoff Quality](handoff-quality.md)
