# Dark Patterns Cases

## Overview

Documentacao de dark patterns notaveis em interfaces — padroes de design manipulativos que enganam usuarios em acoes nao intencionais. Estudo essencial para evitar e combater praticas antiéticas.

## Taxonomy of Dark Patterns

```
Tipo                    | Descricao
------------------------|------------------------------------------
Bait and Switch         | Oferecer algo e entregar outro
Confirmshaming          | Usar culpa para influenciar decisao
Disguised Ads           | Anuncios disfarçados de conteudo
Forced Continuity       | Cobrar apos trial sem aviso claro
Friend Spam             | Usar contatos sem consentimento claro
Hidden Costs            | Custos revelados apenas no final
Misdirection            | Distrair de opcao real
Privacy Zuckering       | Confundir para coletar mais dados
Roach Motel             | Facil de entrar, dificil de sair
Trick Questions         | Perguntas confusas para opt-in acidental
```

## Notable Cases

### Case 1: Amazon — Cancelar Prime
```
Padrao: Roach Motel
- Cancelar Prime requer 6+ clicks em paginas confusas
- Paginas intermediarias com "ofertas" para nao cancelar
- Botao de cancelar usa linguagem ambigua
- FTC processou Amazon em 2023 ("Project Iliad")
- Redesignado apos pressao regulatoria (2024)

Impacto: multa potencial de bilhoes, dano reputacional
```

### Case 2: Cookie Consent Banners
```
Padrao: Misdirection + Forced Action
- "Accept All" como botao primario colorido
- "Manage Preferences" como link sutil
- 30+ clicks para rejeitar cookies individualmente
- Muitos sites nao oferecem "Reject All"
- Violacao do GDPR em muitos casos

Impacto: multas na Europa, regulacao mais rigorosa
```

### Case 3: Confirmshaming Examples
```
Padrao: Confirmshaming
Exemplos reais de copy manipulativa:
- "No thanks, I don't want to save money"
- "I'll pass on this exclusive deal"
- "No, I prefer paying full price"
- "I don't care about my health"

Impacto: conversao de curto prazo, dano de confianca de longo prazo
```

### Case 4: LinkedIn — Contact Import
```
Padrao: Friend Spam
- Flow de importacao de contatos ambiguo
- Emails enviados a todos os contatos sem consentimento claro
- Class action lawsuit de $13M (2015)
- Flow redesenhado apos processo

Impacto: multa, dano reputacional, perda de confianca
```

## Regulatory Response

```
Regulacao                    | Impacto em Dark Patterns
-----------------------------|----------------------------------
GDPR (Europa, 2018)          | Cookie consent, data collection
CCPA (California, 2020)      | Opt-out deve ser tao facil quanto opt-in
Digital Services Act (EU)    | Proibe interfaces manipulativas
FTC (EUA)                    | Acoes contra deceptive design
```

## Ethical Design Principles

```
Principio                    | Pratica
-----------------------------|----------------------------------
Transparencia                | Opcoes claras sem manipulacao
Consentimento informado      | Linguagem simples e honesta
Simetria                     | Cancelar tao facil quanto assinar
Respeito                     | Nao usar culpa ou medo
Privacidade por padrao       | Menor coleta de dados por default
```

## Lessons

- Dark patterns geram receita de curto prazo e destroem confianca de longo prazo
- Regulacao esta aumentando — o que e legal hoje pode nao ser amanha
- Design etico e vantagem competitiva em mercados maduros
- Teste com usuarios reais se suas interfaces sao percebidas como manipulativas
- Documente decisoes de design controversas e suas justificativas

## Tags

`dark-patterns`, `ethics`, `deceptive-design`, `regulation`, `gdpr`, `trust`
