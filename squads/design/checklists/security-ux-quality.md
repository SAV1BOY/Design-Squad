# Security UX Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Security & Trust
- **Version:** 1.0.0
- **Owner Agent:** Security UX Agent

## Objective
Garantir que as interfaces que lidam com seguranca, privacidade e dados sensiveis sejam projetadas para proteger o usuario sem sacrificar a usabilidade.
Security UX de qualidade constroi confianca e reduz erros humanos que levam a vulnerabilidades.

## When to Apply
- Ao projetar flows de autenticacao, autorizacao e gerenciamento de conta.
- Ao tratar dados sensiveis (pessoais, financeiros, de saude) na interface.
- Ao implementar funcionalidades de privacidade e consentimento.

## Criteria
- [ ] Os flows de autenticacao (login, signup, password recovery) sao claros e seguros
- [ ] Os campos de senha possuem opcao de show/hide e indicador de forca (password strength)
- [ ] A autenticacao multifator (MFA) esta integrada de forma usavel quando requerida
- [ ] Os dados sensiveis sao mascarados por padrao com opcao de revelacao controlada
- [ ] Os consent flows para coleta de dados sao transparentes e compreensiveis
- [ ] As permissoes solicitadas sao justificadas com contexto no momento da solicitacao
- [ ] Os indicadores de seguranca (cadeado, badges, selos) sao usados corretamente
- [ ] As sessoes expiradas possuem tratamento UX adequado (save state, redirect, mensagem)
- [ ] Os error messages de seguranca nao revelam informacoes exploraveis (ex: "usuario nao existe")
- [ ] O logout e facilmente acessivel e confirmado ao usuario
- [ ] Os dados do usuario podem ser exportados e excluidos conforme LGPD/GDPR
- [ ] As acoes destrutivas possuem confirmacao e sao potencialmente reversiveis
- [ ] O feedback de acoes de seguranca (alteracao de senha, revogacao de acesso) e claro
- [ ] Os termos de privacidade sao apresentados de forma legivel e acessivel
- [ ] O design nao utiliza dark patterns para manipular decisoes de privacidade
- [ ] Os emails transacionais de seguranca possuem design consistente e identificavel

## Severity Guide

### Critico
- Error messages que revelam informacoes exploraveis por atacantes.
- Dark patterns em consent flows de privacidade.
- Acoes destrutivas sem confirmacao ou possibilidade de reverter.

### Major
- Dados sensiveis exibidos sem mascaramento padrao.
- Sessoes expiradas sem tratamento UX adequado.
- Permissoes solicitadas sem justificativa contextual.

### Minor
- Indicador de forca de senha ausente mas validacao presente.
- Design de emails transacionais inconsistente com o produto.
- Opcao de exportacao de dados existente mas nao facilmente encontravel.

## Cross-References
- [Content Design Quality](content-design-quality.md)
- [Accessibility Quality](accessibility-quality.md)
- [User Flow Quality](user-flow-quality.md)
- [Design Documentation Quality](design-documentation-quality.md)
- [UX Audit Quality](ux-audit-quality.md)
