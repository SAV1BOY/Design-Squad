# User Flow Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Feature / Fluxo**  | [PREENCHER — nome do fluxo]                   |
| **Produto**          | [PREENCHER — nome do produto]                  |
| **Designer**         | [PREENCHER — responsavel]                      |
| **Data de criacao**  | [PREENCHER — YYYY-MM-DD]                       |
| **Versao**           | [PREENCHER — v1.0]                             |
| **Plataforma**       | [PREENCHER — Web / iOS / Android / Todas]      |
| **Status**           | [PREENCHER — Draft / Aprovado / Implementado]  |
| **Link do diagrama** | [PREENCHER — link Figma/Miro/FigJam]           |

## Instructions (Como Usar)

1. Defina o ponto de entrada e o(s) ponto(s) de saida do fluxo.
2. Mapeie o caminho feliz (happy path) primeiro, depois adicione caminhos alternativos.
3. Use a notacao padrao: retangulos para telas, losangos para decisoes, setas para transicoes.
4. Inclua estados de erro e edge cases no mapeamento.
5. Valide o flow com PM e eng antes de iniciar wireframes/mockups.

> **Dica:** User flows devem ser simples o suficiente para qualquer pessoa do time entender. Se esta complexo demais, considere quebrar em sub-fluxos.

## Template

### 1. Descricao do Fluxo

[PREENCHER — descreva o fluxo em 2-3 frases. O que o usuario esta tentando fazer?]

**Entry point:** [PREENCHER — de onde o usuario vem, ex.: deep link, home, email]
**End point (sucesso):** [PREENCHER — onde termina o happy path]
**End point (erro/saida):** [PREENCHER — onde o usuario pode sair]

### 2. Pre-condicoes

- [PREENCHER — o que precisa ser verdade para o usuario entrar neste fluxo]
- [PREENCHER — estado do sistema necessario]
- [PREENCHER — permissoes ou dados necessarios]

### 3. Happy Path (Caminho Principal)

```
[PREENCHER — Entry Point]
        |
        v
[PREENCHER — Tela/Step 1: descricao]
        |
        v
[PREENCHER — Tela/Step 2: descricao]
        |
        v
    <PREENCHER — Decisao?>
       / \
     Sim   Nao
      |      |
      v      v
[PREENCHER] [PREENCHER — caminho alternativo]
      |
      v
[PREENCHER — Tela/Step 3: descricao]
      |
      v
[PREENCHER — Tela/Step 4: descricao]
      |
      v
[PREENCHER — Sucesso / Confirmacao]
```

### 4. Detalhamento por Step

#### Step 1: [PREENCHER — nome da tela/acao]

- **Tela:** [PREENCHER — nome da tela]
- **Acao do usuario:** [PREENCHER — o que o usuario faz]
- **Dados necessarios:** [PREENCHER — inputs requeridos]
- **Validacoes:** [PREENCHER — regras de validacao]
- **CTA principal:** [PREENCHER — botao/acao principal]
- **Acoes secundarias:** [PREENCHER — links, botao voltar, etc.]
- **Wireframe link:** [PREENCHER — link para wireframe]

#### Step 2: [PREENCHER — nome]

- **Tela:** [PREENCHER]
- **Acao do usuario:** [PREENCHER]
- **Dados necessarios:** [PREENCHER]
- **Validacoes:** [PREENCHER]
- **CTA principal:** [PREENCHER]
- **Acoes secundarias:** [PREENCHER]

#### Step 3: [PREENCHER — nome]

- **Tela:** [PREENCHER]
- **Acao do usuario:** [PREENCHER]
- **Dados necessarios:** [PREENCHER]
- **Validacoes:** [PREENCHER]
- **CTA principal:** [PREENCHER]

#### Step 4: [PREENCHER — nome]

- **Tela:** [PREENCHER]
- **Acao do usuario:** [PREENCHER]
- **CTA principal:** [PREENCHER]

### 5. Caminhos Alternativos

| # | Condicao / Trigger                     | Caminho                              |
|---|----------------------------------------|--------------------------------------|
| 1 | [PREENCHER — condicao que desvia]      | [PREENCHER — para onde vai]          |
| 2 | [PREENCHER — condicao]                 | [PREENCHER — destino]                |
| 3 | [PREENCHER — condicao]                 | [PREENCHER — destino]                |

### 6. Edge Cases e Estados de Erro

| # | Cenario                                | Comportamento esperado               |
|---|----------------------------------------|--------------------------------------|
| 1 | [PREENCHER — ex.: sem conexao]         | [PREENCHER — o que acontece]         |
| 2 | [PREENCHER — ex.: campo invalido]      | [PREENCHER — mensagem/acao]          |
| 3 | [PREENCHER — ex.: timeout de API]      | [PREENCHER — fallback]               |
| 4 | [PREENCHER — ex.: usuario ja existe]   | [PREENCHER — redirecionamento]       |
| 5 | [PREENCHER — ex.: sessao expirada]     | [PREENCHER — comportamento]          |

### 7. Estados Especiais

**Empty state:** [PREENCHER — o que aparece quando nao ha dados]
**Loading state:** [PREENCHER — skeleton / spinner / progressive loading]
**Error state:** [PREENCHER — mensagem e acao de recuperacao]
**Success state:** [PREENCHER — feedback de conclusao]

### 8. Metricas do Fluxo

| Metrica                      | Meta                        |
|------------------------------|-----------------------------|
| Completion rate              | [PREENCHER — % alvo]        |
| Drop-off rate por step       | [PREENCHER — % aceitavel]   |
| Tempo total do fluxo         | [PREENCHER — segundos/min]  |
| Error rate                   | [PREENCHER — % aceitavel]   |

### 9. Notas Tecnicas

- **APIs envolvidas:** [PREENCHER — endpoints]
- **Autenticacao:** [PREENCHER — requer login? tipo de auth]
- **Permissoes:** [PREENCHER — roles que tem acesso]
- **Analytics events:** [PREENCHER — eventos a trackear]

## Example (Parcialmente Preenchido)

**Fluxo:** Cadastro de novo usuario via email
**Entry point:** Landing page CTA "Criar conta gratis"
**Happy path:** Landing -> Form email/senha -> Verificacao email -> Setup perfil -> Dashboard
**Edge case:** Email ja cadastrado -> Exibe mensagem "Este email ja possui conta" com link para login.
**Metrica:** Completion rate alvo > 75%.

## Notes

- Sempre comece pelo happy path e depois adicione complexidade.
- Use numeracao consistente para facilitar referencia em reviews.
- Cada decisao (losango) deve ter claramente as condicoes de cada caminho.
- Alinhe com eng sobre viabilidade de validacoes e transicoes antes de finalizar.
- Mantenha o diagrama visual atualizado junto com este documento.
