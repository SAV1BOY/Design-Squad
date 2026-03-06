# Design Documentation Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Design Operations
- **Version:** 1.0.0
- **Owner Agent:** Design Ops Agent

## Objective
Garantir que a documentacao de design seja completa, acessivel e mantenha o conhecimento do time organizado e disponivel para consulta.
Boa documentacao reduz dependencia de individuos e acelera o onboarding de novos membros.

## When to Apply
- Ao documentar decisoes de design, rationale e trade-offs.
- Ao criar ou atualizar guidelines e standards do time.
- Ao encerrar projetos ou fases para preservar o conhecimento adquirido.

## Criteria
- [ ] O documento possui titulo, data, autor e versao claramente identificados
- [ ] O contexto e o problema que originou a decisao de design estao descritos
- [ ] As alternativas consideradas estao documentadas com pros e contras de cada uma
- [ ] A decisao final esta claramente indicada com rationale que a justifica
- [ ] Os trade-offs aceitos estao explicitamente documentados
- [ ] Os stakeholders envolvidos na decisao estao listados
- [ ] As evidencias que suportam a decisao (pesquisa, dados, benchmarks) estao referenciadas
- [ ] O documento esta armazenado em local padronizado e facilmente encontravel
- [ ] A nomenclatura do arquivo segue a convencao do time
- [ ] Os links para artefatos relacionados (Figma, prototipos, pesquisa) estao incluidos
- [ ] O documento e auto-contido o suficiente para ser compreendido sem explicacao verbal
- [ ] As imagens e diagramas possuem legendas e sao de boa qualidade
- [ ] O historico de alteracoes esta registrado (changelog ou version history)
- [ ] Os proximos passos ou pendencias estao indicados quando aplicavel
- [ ] O documento foi revisado por pelo menos um membro do time

## Severity Guide

### Critico
- Decisoes de design nao documentadas em projetos complexos.
- Documentacao inacessivel ou em local desconhecido pelo time.
- Rationale de decisoes criticas ausente.

### Major
- Alternativas consideradas nao documentadas, impedindo entendimento das escolhas.
- Links quebrados para artefatos referenciados.
- Trade-offs nao explicitados gerando questionamentos recorrentes.

### Minor
- Nomenclatura de arquivo fora da convencao mas documento encontravel.
- Changelog nao mantido em documentos de baixa frequencia de atualizacao.
- Legendas ausentes em imagens auto-explicativas.

## Cross-References
- [Discovery Brief Quality](discovery-brief-quality.md)
- [Design Critique Quality](design-critique-quality.md)
- [Handoff Quality](handoff-quality.md)
- [Design System Quality](design-system-quality.md)
- [Design Debt Quality](design-debt-quality.md)
