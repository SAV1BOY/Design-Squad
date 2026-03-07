# Cultural Adaptation — Brasil (PT-BR)

## Metadata

- **Categoria:** Calibração de Voz
- **Aplicação:** Adaptações culturais para comunicação no contexto brasileiro
- **Última atualização:** 2026-03-06

## Description

Este guia documenta as adaptações culturais necessárias para que a comunicação do
Design Squad funcione efetivamente no contexto brasileiro. O Brasil tem características
culturais únicas que impactam como informação é recebida, processada e respondida —
desde a preferência por comunicação relacional até as especificidades linguísticas do
português brasileiro.

Não se trata de estereotipar, mas de reconhecer padrões culturais que, quando
ignorados, geram fricção na comunicação.

## Linguistic Adaptations

### Português Brasileiro vs. Europeu
- Usar **sempre** PT-BR (não PT-PT)
- "Você" ao invés de "tu" (exceto contextos regionais onde "tu" é natural)
- Gerúndio: "Estamos carregando" (BR) vs. "Estamos a carregar" (PT)
- Vocabulário: "celular" (não "telemóvel"), "tela" (não "ecrã"), "mouse" (não "rato")
- "Cadastro" (não "registro"), "boleto" (não existe equivalente em PT-PT)

### Termos técnicos em inglês mantidos
- Manter em inglês sem itálico: design system, tokens, components, sprint, backlog
- Manter em inglês com explicação na primeira ocorrência: "handoff (entrega de design
  para desenvolvimento)"
- **Não** aportuguesar: "designar" não significa "to design", "tokenizar" é forçado
- Exceções aceitas: "debugar", "commitar", "deploiar" (já naturalizados em tech BR)

### Formatação localizada
- Datas: DD/MM/AAAA (06/03/2026), nunca MM/DD/YYYY
- Moeda: R$ 1.234,56 (ponto para milhar, vírgula para decimal)
- Hora: 14h30 ou 14:30 (formato 24h preferível em docs, 12h aceito em conversa)
- Telefone: (11) 99999-9999
- CPF: 123.456.789-00
- CEP: 12345-678

## Cultural Communication Patterns

### Comunicação relacional
- No Brasil, **relacionamento vem antes de conteúdo**
- Um "bom dia" ou "tudo bem?" antes de ir direto ao ponto não é perda de tempo
- Em reuniões, os primeiros 2-3 minutos de conversa informal são investimento social
- Feedback direto é aceito, mas contexto relacional suaviza a recepção
- "Preciso da sua ajuda com..." funciona melhor que "Faça isso..."

### Comunicação indireta em feedback negativo
- Brasileiros tendem a suavizar feedback negativo com contexto positivo
- O modelo "sanduíche" (positivo → construtivo → positivo) é culturalmente alinhado
- Porém, não confundir suavização com ambiguidade — ser claro sobre o que precisa mudar
- "Gostei muito da direção visual. O ponto que precisa de ajuste é o contraste do
  texto secundário — está abaixo de WCAG AA. Com esse fix, fica excelente."

### Hierarquia e formalidade
- O Brasil é relativamente hierárquico em contextos corporativos
- Primeiro nome é aceitável mesmo com superiores (diferente de culturas asiáticas)
- Mas tom e respeito importam — informalidade não é desrespeito
- Em comunicação escrita com liderança sênior, preferir Nível 3-4 da Formality Scale

### Senso de urgência e prazos
- "Urgente" é usado com frequência e pode perder significado — definir critérios claros
- Prazos específicos ("até sexta 17h") funcionam melhor que vagos ("essa semana")
- Follow-up é esperado e não é percebido como microgerenciamento
- "Preciso disso para ontem" é culturalmente compreendido mas não é comunicação eficaz

## Microcopy Localization

### Tratamento consistente
- Sempre "você" — nunca alternar com "tu" ou "o(a) senhor(a)"
- Tom conversacional mas respeitoso: "Sua sessão expirou" (não "Ei, cadê você?")
- Gênero: preferir linguagem neutra quando possível ("Pessoa usuária" em docs,
  "Você" em UI)

### Expressões naturais em PT-BR
- "Pronto!" (confirmação de sucesso — natural e satisfatório)
- "Quase lá" (progresso — brasileiro entende como encorajamento)
- "Ops, algo deu errado" (erro leve — informal mas não infantil)
- "Tente novamente" (recuperação — direto e acionável)

### Expressões a evitar em UI
- "Favor informar" — burocrático demais para interface digital
- "Prezado(a) usuário(a)" — corporativo demais para produto digital
- "Clique aqui" — fora de contexto em mobile (não se "clica")
- "Preencha corretamente" — culpabiliza o usuário

## Regional Considerations

- O Brasil tem 5 regiões com particularidades linguísticas
- Para produto nacional, usar PT-BR "neutro" (base São Paulo/Rio)
- Evitar regionalismos: "oxe", "bah", "uai" — a menos que o produto seja regional
- Considerar diversidade socioeconômica: nem todos têm vocabulário técnico
- Testar microcopy com usuários de diferentes regiões e classes sociais

## Cross-References

- `voice/language-guides/microcopy-tone.md` — Tom de microcopy
- `voice/calibration/formality-scale.md` — Escala de formalidade
- `phrases/microcopy-library.md` — Biblioteca de microcopy em PT-BR
- `phrases/error-messages-library.md` — Mensagens de erro localizadas
