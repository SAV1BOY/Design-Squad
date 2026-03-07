# Billing Management Patterns

## Pattern Description

Padroes para paginas de gerenciamento de cobranca e faturamento. Transparencia, facilidade de acesso a faturas e clareza nos valores sao essenciais.

## Examples

### Example 1: Stripe Billing Portal — Self-Service
Stripe oferece portal de billing completo:
- Current plan com resumo de uso
- Historico de faturas com download em PDF
- Payment method management (add, remove, update)
- Upgrade/downgrade com preview de valor pro-rata
- Cancel subscription com retention flow

### Example 2: Vercel — Usage-Based Dashboard
Vercel mostra uso e custo em tempo real:
- Usage meters com barra visual (bandwidth, builds, functions)
- Spend alerts configuráveis
- Projecao de custo para fim do periodo
- Historico de faturas com detalhamento por recurso
- Invite team members com impacto no custo

### Example 3: GitHub — Organization Billing
GitHub gerencia billing organizacional:
- Seats e spending com breakdown por produto
- Cost management: spending limits por feature
- Payment history com status (paid, pending, failed)
- Tax ID e billing address editáveis
- Export de dados para contabilidade (CSV)

## Analysis

Billing management eficaz:
- **Transparencia**: sem custos ocultos, total visivel
- **Historico**: todas as faturas acessiveis e downloadable
- **Alertas**: aviso antes de limites e renovacoes
- **Self-service**: upgrade, downgrade, cancel sem suporte humano
- **Seguranca**: acesso restrito a billing info (role-based)
- **Compliance**: tax info, receipts, export para contabilidade

## Tags

`billing`, `payments`, `invoices`, `subscription`, `usage`, `self-service`
