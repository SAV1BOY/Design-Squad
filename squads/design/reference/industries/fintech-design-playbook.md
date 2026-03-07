# Fintech Design Playbook



## Metadata

- **Categoria:** Industry Playbook, Fintech, Regulated Design
- **Relevancia para o Squad:** Media — padroes para design de servicos financeiros
- **Ultima revisao:** 2026-03-06



## Summary

Fintech design opera na intersecao de usabilidade, seguranca e regulamentacao. Dinheiro amplifica emocoes — ansiedade, medo, satisfacao — tornando decisoes de design mais impactantes. O desafio e tornar servicos financeiros acessiveis e intuitivos sem sacrificar seguranca ou compliance.



## Key Concepts


### 1. Security-Usability Balance

Autenticacao forte sem friccao excessiva: biometric login, progressive MFA, contextual security (pedir confirmacao apenas para operacoes de risco). O padrao PSD2/SCA (Europa) e Pix (Brasil) definem requisitos minimos de seguranca.


### 2. Financial Data Visualization

Dashboards financeiros com: saldo proeminente, graficos de receita/despesa, categorizacao automatica. Dados financeiros exigem precisao absoluta — arredondamento errado ou grafico distorcido destroi confianca instantaneamente.


### 3. Onboarding Regulamentado (KYC/KYB)

Know Your Customer (KYC) exige coleta de documentos, verificacao de identidade e validacao de dados. Design challenge: tornar processo regulatorio tolerable — progress indicator, upload por camera, OCR automatico, feedback em tempo real do status de verificacao.


### 4. Transaction Design

Confirmacao clara antes de executar (resumo de transferencia), feedback imediato apos execucao ("Transferencia realizada"), comprovante disponivel imediatamente, historico acessivel e filtravel. Reversibilidade quando possivel (cancelamento de agendamento).


### 5. Financial Literacy Integration

Muitos usuarios tem baixa literacia financeira. Design inclusivo: explicar termos financeiros em tooltips, mostrar impacto de decisoes (simulacoes), usar linguagem clara em vez de jargao, oferecer educational moments contextuais.



## Application to Design Squad

- **Security pattern library:** Documentar padroes de seguranca no design system: biometric prompt, MFA flow, transaction confirmation, sensitive data display (mascarar parcialmente).
- **Data precision policy:** Para dados financeiros, definir politica de precisao: sempre mostrar centavos, nunca arredondar, atualizar em tempo real ou mostrar timestamp.
- **KYC flow optimization:** Se o produto tem KYC, mapear o fluxo completo. Medir abandono por step. Investir em OCR, autofill e feedback em tempo real para reduzir friccao.
- **Financial terminology glossary:** Manter glossario de termos financeiros com explicacoes em linguagem simples. Usar em tooltips e contextos de ajuda.
- **Pix integration patterns:** Para produtos fintech no Brasil, padronizar padroes de Pix: QR code display, copia-e-cola, confirmacao de pagamento, comprovante.



## Key Takeaways

1. **Precisao e confianca sao inegociaveis em fintech.** Um centavo errado destrói credibilidade.

2. **Seguranca proporcional ao risco.** Biometric para login, MFA para transferencias altas. Nao uma seguranca so para tudo.

3. **KYC e conversao — investir em UX de KYC e investir em growth.** Cada ponto de abandono no KYC e cliente perdido.

4. **Explique termos financeiros.** Inclusao financeira comeca com linguagem acessivel.

5. **Pix mudou o design de pagamentos no Brasil.** Integrar padroes Pix nativos, nao adaptar padroes de cartao.



## Cross-References

- [Auth and MFA Patterns](../ui-patterns/auth-and-mfa-patterns.md) — seguranca
- [Trust and Credibility Signals](../psychology/trust-and-credibility-signals.md) — confianca financeira
- [Dashboards and Tables Patterns](../ui-patterns/dashboards-and-tables-patterns.md) — financial dashboards
- [Brazil LATAM Design Context](brazil-latam-design-context.md) — Pix, regulamentacao BR
- [WCAG 2.x Notes](../standards/wcag-2-x-notes.md) — acessibilidade financeira
