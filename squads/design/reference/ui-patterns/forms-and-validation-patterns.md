# Forms and Validation Patterns



## Metadata

- **Categoria:** UI Patterns, Data Input, Conversion
- **Relevancia para o Squad:** Alta — formularios sao o ponto de conversao critico
- **Ultima revisao:** 2026-03-06



## Summary

Formularios sao onde o usuario commit informacao — e onde a maioria das conversoes acontece ou falha. Cada campo, cada label, cada mensagem de erro impacta completion rate. Este documento sintetiza padroes comprovados de design de formularios baseados em pesquisa.



## Key Concepts


### 1. Layout (Label Position and Alignment)

Labels acima dos campos (top-aligned) como default — mais rapido, melhor em mobile. Left-aligned labels para formularios de alta densidade (enterprise). Floating labels (dentro do campo) sao controversos — economizam espaco mas sacrificam clareza.


### 2. Inline Validation

Validar campos em tempo real: no blur (quando usuario sai do campo) para campos com formato (email, telefone), no input para campos com tamanho (senha, username). Feedback positivo (checkmark verde) e negativo (mensagem de erro especifica). Nunca validar enquanto o usuario ainda esta digitando.


### 3. Error Messages

Especificas e acionaveis: "Use formato DD/MM/AAAA" em vez de "Data invalida." Posicionadas abaixo do campo com erro. Cor + icone (nao apenas cor) para acessibilidade. Summary de erros no topo do form para formularios longos.


### 4. Multi-Step Forms (Wizards)

Para formularios longos (>7 campos): dividir em steps com progress indicator. Cada step tem tema (informacoes pessoais, pagamento, confirmacao). Permitir navegacao entre steps (nao so forward). Persistir dados entre steps (nao perder ao voltar).


### 5. Input Types e Masks

Usar input type correto para mobile keyboard: type="email" (teclado com @), type="tel" (teclado numerico), type="number" (numerico). Mascaras para formatos especificos (telefone, CPF, cartao). Auto-format reduz erros de digitacao.



## Application to Design Squad

- **Form component library:** Padronizar no design system: input states (default, focus, filled, error, disabled, read-only), label position, error message format, helper text format.
- **Inline validation obrigatoria:** Todo campo com formato ou restricao deve ter inline validation. Documentar no design system o trigger (blur vs. input) para cada tipo.
- **Error message library:** Manter biblioteca de mensagens de erro especificas e acionaveis. Cada tipo de validacao tem mensagem padronizada no produto.
- **Mobile-first input types:** Sempre especificar input type correto no design spec. Teclado mobile adequado reduz erros significativamente.
- **Multi-step threshold:** Formularios com mais de 7 campos devem ser multi-step. Documentar criterios de split no design system.



## Key Takeaways

1. **Labels acima dos campos como default.** Mais rapido, melhor em mobile, comprovado por pesquisa.

2. **Inline validation e obrigatoria.** Feedback em tempo real reduz erros e aumenta completion.

3. **Mensagens de erro sao instrucoes de correcao.** "Campo invalido" nao ajuda. "Use apenas numeros" resolve.

4. **Multi-step reduz perceived complexity.** 3 steps de 4 campos assusta menos que 1 form de 12 campos.

5. **Input type correto = teclado correto = menos erros.** Especifique sempre no design spec.



## Cross-References

- [Web Form Design — Wroblewski](../books/wroblewski-web-form-design.md) — referencia completa
- [Data Input Patterns](data-input-patterns.md) — padroes de input especificos
- [Cognitive Load Theory](../psychology/cognitive-load-theory.md) — por que simplificar funciona
- [WCAG 2.x Notes](../standards/wcag-2-x-notes.md) — formularios acessiveis
- [Auth and MFA Patterns](auth-and-mfa-patterns.md) — formularios de autenticacao
