# Success Metrics Template

## Informacoes do Projeto

| Campo | Valor |
|-------|-------|
| **Produto** | [Nome do produto] |
| **Autor** | [Nome] |
| **Data** | [YYYY-MM-DD] |
| **Periodo de Medicao** | [Data inicio — Data fim] |
| **Data Analyst** | [Nome] |

## Objetivo

Definir as metricas de sucesso para o redesign do produto,
estabelecendo baselines, metas e metodos de medicao para
avaliar o impacto das mudancas de design.

## North Star Metric

A metrica principal que indica se o redesign esta atingindo
seu objetivo estrategico.

| Campo | Valor |
|-------|-------|
| **Metrica** | [Nome da metrica] |
| **Definicao** | [Como e calculada] |
| **Baseline** | [Valor atual] |
| **Meta** | [Valor desejado] |
| **Prazo** | [Data] |
| **Fonte de Dados** | [Ferramenta/sistema] |

## Metricas de Experiencia do Usuario

### Usabilidade

| Metrica | Definicao | Baseline | Meta 30d | Meta 90d | Fonte |
|---------|----------|----------|---------|---------|-------|
| SUS Score | System Usability Scale (0-100) | [N] | [N] | [N] | Survey |
| Task Completion Rate | % de tarefas concluidas com sucesso | [%] | [%] | [%] | Analytics |
| Time on Task | Tempo medio para completar tarefa core | [seg] | [seg] | [seg] | Analytics |
| Error Rate | % de erros por sessao | [%] | [%] | [%] | Analytics |
| Learnability | Tempo ate primeira acao bem-sucedida | [min] | [min] | [min] | Analytics |

### Satisfacao

| Metrica | Definicao | Baseline | Meta 30d | Meta 90d | Fonte |
|---------|----------|----------|---------|---------|-------|
| NPS | Net Promoter Score (-100 a 100) | [N] | [N] | [N] | Survey |
| CSAT | Customer Satisfaction (1-5) | [N] | [N] | [N] | Survey |
| CES | Customer Effort Score (1-7) | [N] | [N] | [N] | Survey |
| App Store Rating | Rating medio nas stores | [N] | [N] | [N] | Stores |

### Acessibilidade

| Metrica | Definicao | Baseline | Meta | Fonte |
|---------|----------|----------|------|-------|
| WCAG Compliance | % de criterios AA atendidos | [%] | 100% | Audit |
| Keyboard Navigation | % de fluxos acessíveis via teclado | [%] | 100% | Audit |
| Screen Reader | % de telas compatíveis com leitor | [%] | 100% | Audit |
| Color Contrast | % de elementos com contraste adequado | [%] | 100% | Audit |

## Metricas de Engajamento

| Metrica | Definicao | Baseline | Meta 30d | Meta 90d | Fonte |
|---------|----------|----------|---------|---------|-------|
| DAU | Daily Active Users | [N] | [N] | [N] | Analytics |
| WAU | Weekly Active Users | [N] | [N] | [N] | Analytics |
| MAU | Monthly Active Users | [N] | [N] | [N] | Analytics |
| Session Duration | Duracao media da sessao | [min] | [min] | [min] | Analytics |
| Sessions per User | Sessoes por usuario por semana | [N] | [N] | [N] | Analytics |
| Feature Adoption | % de usuarios usando features novas | N/A | [%] | [%] | Analytics |
| Retention (D7) | % de usuarios que retornam em 7 dias | [%] | [%] | [%] | Analytics |
| Retention (D30) | % de usuarios que retornam em 30 dias | [%] | [%] | [%] | Analytics |

## Metricas de Negocio

| Metrica | Definicao | Baseline | Meta 30d | Meta 90d | Fonte |
|---------|----------|----------|---------|---------|-------|
| Conversion Rate | Taxa de conversao do funil principal | [%] | [%] | [%] | Analytics |
| Revenue per User | Receita media por usuario | [R$] | [R$] | [R$] | Finance |
| Churn Rate | Taxa de cancelamento mensal | [%] | [%] | [%] | Analytics |
| Support Tickets | Tickets de suporte relacionados a UX | [N/mes] | [N/mes] | [N/mes] | Zendesk |
| Time to Value | Tempo ate o usuario obter valor | [dias] | [dias] | [dias] | Analytics |

## Metricas de Performance Tecnica

| Metrica | Definicao | Baseline | Meta | Fonte |
|---------|----------|----------|------|-------|
| LCP | Largest Contentful Paint | [seg] | < 2.5s | Lighthouse |
| FID | First Input Delay | [ms] | < 100ms | Lighthouse |
| CLS | Cumulative Layout Shift | [score] | < 0.1 | Lighthouse |
| Bundle Size | Tamanho total do bundle | [KB] | [KB] | Build |
| TTI | Time to Interactive | [seg] | < 3.5s | Lighthouse |

## Guardrails (Metricas que NAO Devem Piorar)

Metricas que o redesign nao deve impactar negativamente.
Se qualquer guardrail for violado, investigar imediatamente.

| Guardrail | Valor Minimo Aceitavel | Acao se Violado |
|-----------|----------------------|----------------|
| Page load time | Nao aumentar mais que 10% | Rollback parcial |
| Conversion rate | Nao cair mais que 5% | A/B test e investigacao |
| Error rate (tecnico) | Nao aumentar mais que 2% | Hotfix imediato |
| Accessibility score | Nao cair | Correcao imediata |

## Plano de Medicao

### Coleta de Dados

| Metrica | Ferramenta | Responsavel | Frequencia |
|---------|-----------|-------------|-----------|
| Quantitativas (uso) | [Google Analytics / Amplitude] | Data Analyst | Continua |
| Satisfacao | [Survey tool] | UX Researcher | Mensal |
| Usabilidade | [Testes de usabilidade] | UX Researcher | Por fase |
| Performance | [Lighthouse / SpeedCurve] | Engineering | Semanal |
| Acessibilidade | [axe / manual audit] | QA + Design | Por release |

---
