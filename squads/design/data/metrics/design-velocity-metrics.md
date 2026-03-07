# Design Velocity Metrics

## Overview

Metricas de velocidade e throughput do time de design. Mede capacidade de entrega, ciclo de feedback e eficiencia de processo.

## Velocity Dashboard

### Throughput
```
Metrica                    | Valor Atual | Meta    | Trend
---------------------------|-------------|---------|--------
Screens designed/sprint    | 12          | 15      | +2
Components shipped/month   | 4           | 6       | +1
Design reviews/week        | 3           | 4       | estavel
Prototypes delivered/month | 6           | 8       | +1
```

### Cycle Time
```
Fase                       | Tempo Medio | Meta    | Trend
---------------------------|-------------|---------|--------
Brief → First draft        | 2.5 days    | 2 days  | -0.5d
Draft → Review             | 1 day       | 0.5 day | estavel
Review → Approval          | 1.5 days    | 1 day   | -0.3d
Approval → Handoff         | 1 day       | 0.5 day | estavel
Total design cycle         | 6 days      | 4 days  | -0.8d
```

### Quality Gates
```
Gate                       | Pass Rate | Meta    | Trend
---------------------------|-----------|---------|--------
Design review 1st pass     | 72%       | 85%     | +5%
A11y check pass rate       | 85%       | 95%     | +3%
Dev handoff completeness   | 78%       | 90%     | +4%
Visual QA 1st pass         | 80%       | 90%     | +2%
```

### Rework Rate
```
Tipo de Rework             | Percentual | Meta
---------------------------|-----------|-------
Post-handoff design changes| 18%       | 10%
Post-review major revisions| 12%       | 5%
Post-launch design fixes   | 8%        | 3%
```

## Sprint Velocity (Last 6 Sprints)

```
Sprint  | Planned | Completed | Velocity | Carry-over
--------|---------|-----------|----------|------------
S20     | 18      | 14        | 78%      | 4
S21     | 16      | 15        | 94%      | 1
S22     | 17      | 13        | 76%      | 4
S23     | 15      | 14        | 93%      | 1
S24     | 16      | 15        | 94%      | 1
S25     | 16      | 14        | 88%      | 2
Avg     | 16.3    | 14.2      | 87%      | 2.2
```

## Notes

- Velocity medida em story points ou design tasks (consistente por sprint)
- Cycle time rastreado via Figma timestamps e Jira transitions
- Rework rate e o indicador mais importante de qualidade de processo
- Target: reduzir rework post-handoff para < 10% ate Q3 2026
