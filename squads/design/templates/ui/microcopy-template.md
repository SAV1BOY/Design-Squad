# Microcopy Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Projeto**          | [PREENCHER — nome do projeto]                  |
| **Tela / Fluxo**     | [PREENCHER — nome da tela ou fluxo]            |
| **Designer**         | [PREENCHER — designer responsavel]             |
| **Content Designer** | [PREENCHER — redator(a) UX, se houver]         |
| **Data de criacao**  | [PREENCHER — YYYY-MM-DD]                       |
| **Versao**           | [PREENCHER — v1.0]                             |
| **Status**           | [PREENCHER — Draft / Em review / Aprovado]     |
| **Figma link**       | [PREENCHER — link para a tela no Figma]        |

## Instructions (Como Usar)

1. Crie um documento deste para cada tela ou fluxo que contenha microcopy relevante.
2. Preencha todas as variantes de estado — default, erro, sucesso, vazio e loading.
3. Valide o copy com o guia de voz e tom do produto antes de aprovar.
4. Respeite os limites de caracteres — teste em dispositivos reais quando possivel.
5. Use como single source of truth durante handoff para engenharia.

> **Dica:** Microcopy deve ser util primeiro, amigavel depois. Se o usuario nao entender o que fazer, nenhum tom de voz salva.

## Template

### 1. Identificacao da Tela

**Nome da tela:** [PREENCHER — ex.: Checkout — Pagamento]
**Fluxo pai:** [PREENCHER — ex.: Fluxo de compra]
**Posicao no fluxo:** [PREENCHER — ex.: Etapa 3 de 4]
**URL / Rota:** [PREENCHER — ex.: /checkout/payment]

### 2. Contexto e Objetivo

**O que o usuario esta fazendo nesta tela:** [PREENCHER — acao principal]
**De onde o usuario veio:** [PREENCHER — tela anterior]
**Para onde o usuario vai:** [PREENCHER — tela seguinte]
**Emocao provavel do usuario:** [PREENCHER — ex.: ansioso (inserindo dados de pagamento), confiante, frustrado]

### 3. Estado do Usuario

Marque os estados aplicaveis a esta tela:

- [ ] **First-time user** — nunca viu esta tela antes
- [ ] **Returning user** — ja completou este fluxo anteriormente
- [ ] **Erro anterior** — chegou aqui apos uma falha
- [ ] **Upgrade / Upsell** — esta sendo direcionado a uma acao comercial
- [ ] **Onboarding** — esta configurando o produto pela primeira vez
- [ ] **Outro:** [PREENCHER]

### 4. Copy por Elemento

#### 4.1 Titulo da Tela

| Estado    | Copy                                           | Limite de caracteres |
|-----------|-------------------------------------------------|----------------------|
| Default   | [PREENCHER — titulo principal]                  | [PREENCHER — max]    |

#### 4.2 Subtitulo / Descricao

| Estado    | Copy                                           | Limite de caracteres |
|-----------|-------------------------------------------------|----------------------|
| Default   | [PREENCHER — texto de suporte]                  | [PREENCHER — max]    |

#### 4.3 Labels de Formulario

| Campo              | Label                | Placeholder                      | Helper text                     |
|--------------------|----------------------|----------------------------------|---------------------------------|
| [PREENCHER — campo] | [PREENCHER — label] | [PREENCHER — texto de placeholder] | [PREENCHER — texto auxiliar]  |
| [PREENCHER]        | [PREENCHER]          | [PREENCHER]                      | [PREENCHER]                     |
| [PREENCHER]        | [PREENCHER]          | [PREENCHER]                      | [PREENCHER]                     |

#### 4.4 Botoes e CTAs

| Elemento           | Copy — Default       | Copy — Loading        | Copy — Disabled       | Limite    |
|--------------------|----------------------|-----------------------|-----------------------|-----------|
| CTA principal      | [PREENCHER]          | [PREENCHER — ex.: Processando...] | [PREENCHER]  | [PREENCHER] |
| CTA secundario     | [PREENCHER]          | [PREENCHER]           | [PREENCHER]           | [PREENCHER] |
| Link de cancelar   | [PREENCHER]          | —                     | —                     | [PREENCHER] |

#### 4.5 Mensagens de Feedback

**Sucesso:**

| Contexto                         | Titulo                          | Descricao                                  |
|----------------------------------|---------------------------------|--------------------------------------------|
| [PREENCHER — acao completada]    | [PREENCHER — titulo de sucesso] | [PREENCHER — mensagem de confirmacao]      |
| [PREENCHER]                      | [PREENCHER]                     | [PREENCHER]                                |

**Erro:**

| Contexto do erro                 | Titulo                          | Descricao                                  | Acao sugerida                  |
|----------------------------------|---------------------------------|--------------------------------------------|--------------------------------|
| [PREENCHER — tipo de erro]       | [PREENCHER — titulo de erro]    | [PREENCHER — explique o que aconteceu]     | [PREENCHER — o que fazer]      |
| [PREENCHER]                      | [PREENCHER]                     | [PREENCHER]                                | [PREENCHER]                    |
| [PREENCHER]                      | [PREENCHER]                     | [PREENCHER]                                | [PREENCHER]                    |

**Estado vazio (Empty state):**

| Contexto                         | Titulo                          | Descricao                                  | CTA                            |
|----------------------------------|---------------------------------|--------------------------------------------|--------------------------------|
| [PREENCHER — quando aparece]     | [PREENCHER — titulo]            | [PREENCHER — mensagem orientadora]         | [PREENCHER — acao]             |

**Loading:**

| Contexto                         | Mensagem                                        |
|----------------------------------|-------------------------------------------------|
| [PREENCHER — o que esta carregando] | [PREENCHER — ex.: Verificando seus dados...]  |
| [PREENCHER]                      | [PREENCHER]                                     |

#### 4.6 Tooltips e Popovers

| Elemento gatilho     | Texto do tooltip                               | Limite    |
|----------------------|-------------------------------------------------|-----------|
| [PREENCHER — icone/link] | [PREENCHER — texto explicativo]             | [PREENCHER] |
| [PREENCHER]          | [PREENCHER]                                     | [PREENCHER] |

#### 4.7 Modais e Dialogs

| Modal                | Titulo                | Body                                      | CTA primario   | CTA secundario |
|----------------------|-----------------------|-------------------------------------------|----------------|----------------|
| [PREENCHER — quando aparece] | [PREENCHER]   | [PREENCHER — mensagem do modal]           | [PREENCHER]    | [PREENCHER]    |

### 5. Diretrizes de Tom

**Tom nesta tela:** [PREENCHER — ex.: Confiante e direto (tela de pagamento exige clareza)]

| Dimensao         | Nivel (1-5)                                 |
|------------------|---------------------------------------------|
| Formal — Casual  | [PREENCHER — 1=muito formal, 5=muito casual] |
| Serio — Leve     | [PREENCHER — 1=muito serio, 5=muito leve]   |
| Direto — Detalhado | [PREENCHER — 1=minimo, 5=explicativo]      |
| Tecnico — Leigo  | [PREENCHER — 1=muito tecnico, 5=muito leigo] |

**Palavras a usar:** [PREENCHER — ex.: confirmar, proteger, seguro, pronto]
**Palavras a evitar:** [PREENCHER — ex.: falha, invalido, problema, cancelar (quando puder usar "voltar")]

### 6. Limites de Caracteres — Resumo

| Elemento            | Min    | Max    | Ideal  | Motivo da restricao              |
|---------------------|--------|--------|--------|----------------------------------|
| Titulo              | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER — ex.: caber em 1 linha no mobile] |
| Descricao           | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER]                 |
| Botao CTA           | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER]                 |
| Tooltip             | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER]                 |
| Mensagem de erro    | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER]                 |

## Example (Parcialmente Preenchido)

**Tela:** Checkout — Confirmacao de pagamento
**Titulo default:** "Confirme seu pagamento"
**Subtitulo:** "Revise os dados antes de finalizar. Voce nao sera cobrado ate confirmar."
**CTA principal:** "Pagar R$ [valor]" (loading: "Processando pagamento...")
**Erro — cartao recusado:** Titulo: "Pagamento nao aprovado" / Descricao: "Seu banco nao autorizou esta transacao. Tente outro cartao ou entre em contato com seu banco." / Acao: "Tentar outro cartao"
**Tom:** Confiante (3), Formal-medio (2), Direto (2), Leigo (4). Palavras: confirmar, seguro, revisar. Evitar: falha, erro, invalido.

## Notes

- Microcopy deve ser testado com usuarios reais — o que parece claro para o time pode nao ser para o usuario.
- Sempre escreva todas as variantes de estado — empty states e mensagens de erro sao frequentemente esquecidos.
- Respeite o guia de voz e tom do produto — consistencia e mais importante que criatividade.
- Considere localizacao desde o inicio — textos em portugues podem ser 20-30% mais longos que em ingles.
- Valide limites de caracteres em todas as plataformas e tamanhos de tela.
- Mensagens de erro devem explicar o problema E sugerir uma acao — nunca deixe o usuario sem saida.

---

## Cross-references

- **Guia de voz e tom:** [Voice — Tone Profiles](../../voice/tone-profiles/)
- **Guia de linguagem:** [Voice — Language Guides](../../voice/language-guides/)
- **Template de empty states:** [Empty State Library Template](../ui/empty-state-library-template.md)
- **Template de componente:** [Component Spec Template](../ui/component-spec-template.md)
- **Task:** [UI Design High Fidelity](../../tasks/ui/ui-design-high-fidelity.md)
- **Checklist:** [Content Design Quality](../../checklists/content-design-quality.md)
- **Framework:** [Content Design Microcopy](../../frameworks/content-design-microcopy.md)
- **Framework:** [Error Prevention and Recovery](../../frameworks/error-prevention-and-recovery.md)
- **Framework:** [Empty States and Loading States](../../frameworks/empty-states-and-loading-states.md)
- **Agent:** [Jessica UX/UI](../../agents/jessica-ux-ui.md)
