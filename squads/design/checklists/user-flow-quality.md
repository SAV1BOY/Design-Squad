# User Flow Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Interaction Design
- **Version:** 1.0.0
- **Owner Agent:** Interaction Design Agent

## Objective
Assegurar que user flows representem todos os caminhos possiveis do usuario de forma clara, completa e implementavel.
Flows bem documentados sao a base para wireframes, prototipos e comunicacao com desenvolvimento.

## When to Apply
- Ao projetar novos fluxos de interacao para features.
- Ao documentar fluxos existentes para analise ou redesign.
- Antes de iniciar wireframing para validar a logica de navegacao.

## Criteria
- [ ] O flow possui um ponto de entrada (entry point) claramente definido
- [ ] O(s) ponto(s) de saida (exit points / success states) estao identificados
- [ ] Todos os decision points estao representados com ramificacoes claras
- [ ] Os error states e recovery paths estao mapeados para cada passo critico
- [ ] Os edge cases conhecidos estao documentados com seus respectivos tratamentos
- [ ] O happy path esta visualmente destacado em relacao aos caminhos alternativos
- [ ] Cada step do flow indica a acao do usuario e a resposta do sistema
- [ ] Os pontos de integracao com sistemas externos estao indicados
- [ ] O flow considera diferentes niveis de permissao (roles) quando aplicavel
- [ ] Loading states e feedback intermediarios estao representados
- [ ] Os pontos de abandono mais provaveis estao identificados com estrategias de retencao
- [ ] O flow e consistente com patterns existentes no produto para acoes similares
- [ ] A nomenclatura dos steps e padronizada e alinhada com o time de desenvolvimento
- [ ] O flow foi revisado por pelo menos um stakeholder tecnico para viabilidade
- [ ] Existe versionamento do flow com historico de alteracoes

## Severity Guide

### Critico
- Error states nao mapeados para acoes criticas (ex: pagamento, cadastro).
- Happy path incompleto ou com lacunas logicas.
- Decision points ambiguos que podem gerar interpretacoes diferentes.

### Major
- Edge cases conhecidos nao documentados.
- Ausencia de loading states em operacoes assincronas.
- Flow nao revisado por stakeholder tecnico antes da implementacao.

### Minor
- Nomenclatura de steps inconsistente com o glossario do time.
- Falta de destaque visual para o happy path.
- Historico de versoes nao mantido.

## Cross-References
- [Wireframe Quality](wireframe-quality.md)
- [Prototyping Quality](prototyping-quality.md)
- [IA and Navigation Quality](ia-and-navigation-quality.md)
- [Handoff Quality](handoff-quality.md)
- [Persona Quality](persona-quality.md)
