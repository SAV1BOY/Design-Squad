# Motion Design Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Motion & Interaction Design
- **Version:** 1.0.0
- **Owner Agent:** Motion Design Agent

## Objective
Assegurar que animacoes e transicoes em interfaces melhorem a experiencia do usuario comunicando relacoes, estado e feedback sem prejudicar performance ou acessibilidade.
Motion design de qualidade e funcional primeiro, estetico depois.

## When to Apply
- Ao projetar animacoes e transicoes para interfaces.
- Ao especificar motion para handoff ao desenvolvimento.
- Ao auditar animacoes existentes para consistencia e performance.

## Criteria
- [ ] Cada animacao tem um proposito funcional claro (feedback, orientacao, hierarquia, continuidade)
- [ ] A duracao das animacoes e adequada: 100-300ms para micro-interactions, 300-500ms para transicoes
- [ ] As curvas de easing sao consistentes e semanticas (ease-out para entradas, ease-in para saidas)
- [ ] As animacoes respeitam prefers-reduced-motion, oferecendo alternativas sem movimento
- [ ] Nenhuma animacao causa mais de 3 flashes por segundo (risco de seizure)
- [ ] As transicoes comunicam relacoes espaciais e hierarquicas entre elementos
- [ ] O stagger (atraso sequencial) em listas segue timing consistente e nao excede 1 segundo total
- [ ] As animacoes de loading informam progresso e nao bloqueiam interacao desnecessariamente
- [ ] Os motion tokens (duration, easing, delay) estao definidos e documentados
- [ ] A performance das animacoes foi validada (utilizando transform e opacity preferencialmente)
- [ ] As animacoes nao interferem na legibilidade do conteudo durante a execucao
- [ ] O motion design e consistente com o tom e personalidade da marca
- [ ] As specs de animacao incluem valores exatos (duracao em ms, easing curve, propriedades animadas)
- [ ] As animacoes foram testadas em devices de baixa performance
- [ ] Existe documentacao visual (video ou prototipo) das animacoes para referencia

## Severity Guide

### Critico
- Animacoes que causam mais de 3 flashes por segundo.
- Ausencia de suporte a prefers-reduced-motion.
- Animacoes que bloqueiam interacao do usuario por tempo excessivo.

### Major
- Duracoes excessivas que tornam a interface lenta de usar.
- Animacoes sem proposito funcional que apenas distraem.
- Performance ruim em devices-alvo do produto.

### Minor
- Easing curves levemente inconsistentes entre animacoes similares.
- Motion tokens nao documentados mas valores consistentes.
- Documentacao visual ausente mas specs escritas completas.

## Cross-References
- [Token Quality](token-quality.md)
- [Prototyping Quality](prototyping-quality.md)
- [Performance UX Quality](performance-ux-quality.md)
- [Accessibility Quality](accessibility-quality.md)
- [Handoff Quality](handoff-quality.md)
