# UX HEART Dashboard

## Overview

Dashboard de metricas UX baseado no framework HEART do Google. Organiza metricas em cinco dimensoes para avaliacao holistica da experiencia do usuario.

## HEART Metrics

### Happiness (Satisfacao)
```
Metrica          | Valor Atual | Meta    | Trend
-----------------|-------------|---------|--------
NPS              | 42          | 50      | +3 vs Q4
CSAT (suporte)   | 4.2/5       | 4.5/5   | +0.1
SUS Score        | 72          | 80      | +5
Ease of Use      | 3.8/5       | 4.2/5   | +0.2
```

### Engagement (Engajamento)
```
Metrica          | Valor Atual | Meta    | Trend
-----------------|-------------|---------|--------
DAU/MAU ratio    | 38%         | 45%     | +2%
Avg session/day  | 3.2         | 4.0     | +0.3
Features used    | 4.8/session | 6.0     | +0.5
Return rate D7   | 62%         | 70%     | +4%
```

### Adoption (Adocao)
```
Metrica          | Valor Atual | Meta    | Trend
-----------------|-------------|---------|--------
New signups/week | 1,240       | 1,500   | +8%
Activation rate  | 64%         | 75%     | +6%
Feature adoption | 45%         | 60%     | +3%
Onboarding comp. | 76%         | 85%     | +18%
```

### Retention (Retencao)
```
Metrica          | Valor Atual | Meta    | Trend
-----------------|-------------|---------|--------
D1 retention     | 78%         | 82%     | +2%
D7 retention     | 62%         | 70%     | +4%
D30 retention    | 48%         | 55%     | +3%
Churn rate       | 4.2%/mo     | 3.0%    | -0.5%
```

### Task Success (Sucesso de Tarefa)
```
Metrica          | Valor Atual | Meta    | Trend
-----------------|-------------|---------|--------
Task completion  | 87%         | 93%     | +2%
Error rate       | 8%          | 5%      | -1%
Time on task     | 2.4min avg  | 1.8min  | -0.2min
Support tickets  | 320/week    | 200     | -15/week
```

## Measurement Cadence

```
Frequencia    | Metricas
--------------|------------------------------------------
Diaria        | DAU, session metrics, error rate
Semanal       | Signups, support tickets, feature adoption
Mensal        | NPS, retention, churn, HEART rollup
Trimestral    | SUS, CSAT deep dive, benchmark comparison
```

## Notes

- Dados atualizados automaticamente via integracao com analytics
- NPS coletado via in-app survey (amostra de 10% dos MAU)
- SUS coletado trimestralmente via survey dedicado
- Task success medido via session replay (amostra)
