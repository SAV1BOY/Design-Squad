# Brazil and LATAM Design Context



## Metadata

- **Categoria:** Regional Context, Localization, Cultural Design
- **Relevancia para o Squad:** Alta — contexto cultural e regulatorio brasileiro e latino-americano
- **Ultima revisao:** 2026-03-06



## Summary

Projetar para o Brasil e America Latina exige compreensao de contextos culturais, tecnologicos, regulatorios e socioeconomicos especificos. Desde a predominancia do mobile e WhatsApp como canal de comunicacao ate a LGPD como marco regulatorio e o Pix como revolucao de pagamentos, o contexto BR/LATAM tem particularidades que designs "globais" frequentemente ignoram.

Este documento compila as particularidades mais relevantes para design de produtos digitais no Brasil e LATAM, servindo como referencia para evitar os erros mais comuns de localizacao e para aproveitar oportunidades unicas do mercado.



## Key Concepts


### 1. Mobile-First Reality

No Brasil, 62% dos domicilios acessam internet exclusivamente via mobile (TIC Domicilios 2023). Muitos usuarios tem smartphones de entrada com tela pequena, memoria limitada e conexao 3G/4G instavel. Mobile-first nao e preferencia de design — e a realidade do mercado. Performance e offline capability sao features, nao otimizações.


### 2. WhatsApp as Infrastructure

WhatsApp e o canal de comunicacao dominante no Brasil — usado para suporte ao cliente, vendas, pagamentos (WhatsApp Pay), notificacoes e ate onboarding. Produtos que integram WhatsApp (botoes de compartilhamento, atendimento via WhatsApp, notificações via WhatsApp) tem vantagem sobre os que dependem apenas de email.


### 3. Pix as Payment Standard

Pix se tornou o metodo de pagamento dominante no Brasil, superando cartão de credito e boleto bancario. Design implications: Pix como opcao primaria de pagamento (nao terceira), QR code display padronizado, copia-e-cola simplificado, confirmacao instantanea. Boleto ainda relevante para populacao sem conta bancaria.


### 4. LGPD (Lei Geral de Protecao de Dados)

A LGPD regula coleta, uso e armazenamento de dados pessoais no Brasil. Design implications: consent banners claros e honestos (nao dark patterns), politica de privacidade em linguagem acessivel, opcao de exclusao de dados facil, data minimization (coletar so o necessario). Dados de saude e financeiros tem protecao adicional.


### 5. Socioeconomic Diversity

O Brasil tem extrema diversidade socioeconomica que impacta design: niveis de literacia digital variam enormemente, dispositivos variam de iPhone de ultima geracao a Android de entrada, conexao varia de fibra a 3G, e expectativas culturais variam por regiao. Design inclusivo no Brasil significa projetar para o extremo mais limitado, nao para a media.


### 6. Cultural and Linguistic Considerations

Portugues brasileiro tem nuances regionais e de registro. Formal vs. informal (voce vs. tu), regionalismos (diferenca entre SP e NE), e nivel de linguagem (simples vs. tecnico). Tom de voz do produto deve ser calibrado ao publico-alvo. Datas em DD/MM/AAAA, moeda em R$ com ponto como milhar e virgula como decimal (R$ 1.234,56). CPF como identificador universal.



## Application to Design Squad

- **Mobile-first como requisito:** Todo design comeca em mobile. Testar em dispositivos de entrada (Android low-end) com conexao limitada (3G throttling). Se nao funciona la, nao funciona para a maioria.
- **WhatsApp integration:** Para suporte, compartilhamento e notificacoes, priorizar WhatsApp sobre email. Incluir botoes de WhatsApp em pontos de contato.
- **Pix-first payment:** Em flows de pagamento, Pix como primeira opcao. QR code + copia-e-cola + confirmacao instantanea. Boleto como segunda opcao.
- **LGPD compliance:** Revisar todo fluxo que coleta dados pessoais. Consent claro e especifico. Opcao de exclusao acessivel. Dados minimos.
- **Inclusive language and formatting:** Usar linguagem simples e acessivel. Formatos BR para datas (DD/MM/AAAA), moeda (R$ 1.234,56) e documentos (CPF: 000.000.000-00). Testar com usuarios de diferentes regioes e niveis de literacia.
- **Low-end device testing:** Manter dispositivo Android de entrada no squad para testes regulares. Performance nesses dispositivos e o real test de qualidade.



## Key Takeaways

1. **Mobile-first e realidade brasileira, nao tendencia.** A maioria acessa exclusivamente por mobile, frequentemente em dispositivos limitados.

2. **WhatsApp e infraestrutura, nao app.** Integrar WhatsApp e encontrar o usuario onde ele ja esta.

3. **Pix mudou pagamentos para sempre.** Projetar pagamento sem Pix como opcao primaria e ignorar o mercado.

4. **LGPD e obrigacao legal com implicacoes de design.** Consent, data minimization e exclusao devem ser projetados, nao apenas implementados.

5. **Diversidade socioeconomica exige design inclusivo.** Projetar para o dispositivo mais limitado e a conexao mais lenta atende a maioria.

6. **Localizacao vai alem de traducao.** Formatos de data, moeda, documentos e tom de voz precisam ser nativamente brasileiros.



## Cross-References

- [Mobile-First Design Playbook](mobile-first-design-playbook.md) — design mobile
- [Behavioral Design Ethics](../psychology/behavioral-design-ethics.md) — LGPD e etica
- [WCAG 2.x Notes](../standards/wcag-2-x-notes.md) — acessibilidade
- [Fintech Design Playbook](fintech-design-playbook.md) — Pix e pagamentos
- [Auth and MFA Patterns](../ui-patterns/auth-and-mfa-patterns.md) — autenticacao
