# Behavioral Design Ethics



## Metadata

- **Categoria:** Ethics, Behavioral Design, Dark Patterns
- **Relevancia para o Squad:** Alta — responsabilidade etica do designer
- **Ultima revisao:** 2026-03-06



## Summary

Behavioral design ethics aborda a responsabilidade do designer ao usar conhecimento de psicologia e comportamento humano para influenciar decisoes. A linha entre persuasao (ajudar o usuario a tomar melhores decisoes) e manipulacao (explorar vieses para beneficio da empresa) e tenue e requer reflexao consciente.



## Key Concepts


### 1. Dark Patterns Taxonomy

Confirmshaming ("Nao, nao quero economizar dinheiro"), Roach Motel (facil entrar, dificil sair), Forced Continuity (cobranca automatica apos trial), Misdirection (atencao desviada do que importa), Trick Questions (double negatives confusas), Hidden Costs (custos revelados no ultimo passo), Bait and Switch (promete X, entrega Y).


### 2. Ethical Design Framework

Para cada decisao de design que influencia comportamento: (1) A quem isso beneficia? Se so beneficia a empresa, e suspeito. (2) O usuario tomaria a mesma decisao com informacao completa? Se nao, e manipulacao. (3) O usuario ficaria confortavel se soubesse como o design o influencia? Se nao, e antiético.


### 3. Informed Consent in Design

O usuario deve poder tomar decisoes informadas. Isso significa: linguagem clara (nao juridica), consequencias visiveis (nao escondidas), opcoes equivalentes (opt-in e opt-out igualmente faceis), e transparencia sobre o que acontece com dados pessoais.


### 4. Regulatory Landscape

GDPR (Europa), LGPD (Brasil), CCPA (California) regulamentam aspectos de design: consentimento informado, data minimization, right to deletion, cookie banners. FTC (USA) tem enforcement crescente contra dark patterns. Compliance nao e opcional — e requisito legal.


### 5. Designing for Vulnerability

Usuarios vulneraveis (criancas, idosos, pessoas em distress financeiro, usuarios com deficiencia cognitiva) sao mais suscetiveis a design manipulativo. Design etico considera o usuario mais vulneravel, nao o mais sofisticado. LGPD e Estatuto do Idoso no Brasil tem provisoes especificas.



## Application to Design Squad

- **Dark pattern checklist:** Antes de aprovar designs de conversion, retention ou cancelamento, passar por checklist de dark patterns. Nenhum dark pattern conhecido deve ser implementado.
- **Ethical review para features sensíveis:** Features que envolvem pagamento, dados pessoais, cancelamento ou retencao devem ter revisao etica explicita pelo squad.
- **Regulatory compliance check:** Manter checklist de compliance com LGPD para todo fluxo que envolve dados pessoais. Cookie banners, termos de uso e consentimento devem seguir a lei.
- **Vulnerability assessment:** Para features com base de usuarios diversa, avaliar: como o usuario mais vulneravel (idoso, baixa literacia digital) experimentaria isso?
- **Design ethics training:** Incluir modulo de etica em design no onboarding de novos designers. Manter discussoes periodicas sobre casos ambiguos.



## Key Takeaways

1. **Se so beneficia a empresa, questione.** Design etico busca alinhamento de interesse — bom para o usuario e para o negocio.

2. **Transparencia e o teste basico.** Se o usuario ficaria desconfortável sabendo como o design o influencia, o design e antiético.

3. **Dark patterns tem custo de longo prazo.** Conversao por manipulacao gera churn, desconfianca e risco regulatorio crescente.

4. **Projete para o usuario mais vulnerável.** Se funciona para quem tem menos literacia digital, funciona para todos.

5. **Compliance com LGPD nao e opcional.** Design de cookies, consentimento e dados pessoais e obrigação legal no Brasil.



## Cross-References

- [Design for Cognitive Bias — Rudd](../books/rudd-design-for-cognitive-bias.md) — vieses e etica
- [Nudge — Thaler](../books/thaler-nudge.md) — nudge etico vs. sludge
- [Hooked — Eyal](../books/eyal-hooked.md) — manipulation matrix
- [Trust and Credibility Signals](trust-and-credibility-signals.md) — construir confianca
- [Brazil LATAM Design Context](../industries/brazil-latam-design-context.md) — LGPD e regulamentacao BR
