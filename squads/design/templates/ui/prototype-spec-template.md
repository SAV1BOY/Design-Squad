# Prototype Spec Template

## Metadata

| Campo                | Valor                                          |
|----------------------|------------------------------------------------|
| **Projeto**          | [PREENCHER — nome do projeto]                  |
| **Designer**         | [PREENCHER — designer responsavel]             |
| **Data de criacao**  | [PREENCHER — YYYY-MM-DD]                       |
| **Ferramenta**       | [PREENCHER — Figma / ProtoPie / Framer / Code] |
| **Fidelidade**       | [PREENCHER — Low-fi / Mid-fi / High-fi]        |
| **Versao**           | [PREENCHER — v1.0]                             |
| **Status**           | [PREENCHER — Draft / Em teste / Validado]      |
| **Link do prototipo** | [PREENCHER — URL compartilhavel]              |

## Instructions (Como Usar)

1. Defina o escopo do prototipo antes de comecar a construi-lo — nem todo fluxo precisa ser prototipado.
2. Documente cada tela, hotspot e animacao para que qualquer designer possa atualizar o prototipo.
3. Inclua cenarios de teste para validar se o prototipo atende aos objetivos de pesquisa.
4. Use como referencia durante testes de usabilidade e apresentacoes para stakeholders.
5. Atualize os criterios de sucesso apos cada rodada de teste.

> **Dica:** O prototipo mais util e o mais simples que responde a pergunta de pesquisa. Nao invista tempo em animacoes se o objetivo e testar o fluxo.

## Template

### 1. Escopo do Prototipo

**Objetivo:** [PREENCHER — o que este prototipo pretende validar ou demonstrar]

**Tipo de prototipo:**
- [ ] Fluxo de navegacao (testar caminhos)
- [ ] Interacao especifica (testar micro-interacao)
- [ ] Prova de conceito (demonstrar viabilidade)
- [ ] Apresentacao para stakeholders (vender a ideia)
- [ ] Teste de usabilidade (coletar feedback)
- [ ] Outro: [PREENCHER]

**O que esta DENTRO do escopo:**
- [PREENCHER — fluxo ou funcionalidade incluida]
- [PREENCHER]
- [PREENCHER]

**O que esta FORA do escopo:**
- [PREENCHER — o que nao sera prototipado e por que]
- [PREENCHER]

### 2. Telas Incluidas

| # | Nome da tela         | Descricao                              | Status no prototipo    | Link Figma frame      |
|---|----------------------|----------------------------------------|------------------------|-----------------------|
| 1 | [PREENCHER]          | [PREENCHER — o que o usuario ve]       | [PREENCHER — Pronto / Em construcao] | [PREENCHER]  |
| 2 | [PREENCHER]          | [PREENCHER]                            | [PREENCHER]            | [PREENCHER]           |
| 3 | [PREENCHER]          | [PREENCHER]                            | [PREENCHER]            | [PREENCHER]           |
| 4 | [PREENCHER]          | [PREENCHER]                            | [PREENCHER]            | [PREENCHER]           |
| 5 | [PREENCHER]          | [PREENCHER]                            | [PREENCHER]            | [PREENCHER]           |
| 6 | [PREENCHER]          | [PREENCHER]                            | [PREENCHER]            | [PREENCHER]           |

**Tela inicial:** [PREENCHER — de onde o prototipo comeca]
**Tela final:** [PREENCHER — onde o fluxo termina]

### 3. Fluxos de Interacao

**Fluxo A: [PREENCHER — nome do fluxo, ex.: Happy path de cadastro]**

```
[Tela 1] --[acao]--> [Tela 2] --[acao]--> [Tela 3] --[acao]--> [Tela 4]
```

Detalhamento:

| Passo | De (tela)     | Acao do usuario                    | Para (tela)    | Observacao                        |
|-------|---------------|------------------------------------|----------------|-----------------------------------|
| 1     | [PREENCHER]   | [PREENCHER — clique, swipe, etc.]  | [PREENCHER]    | [PREENCHER]                       |
| 2     | [PREENCHER]   | [PREENCHER]                        | [PREENCHER]    | [PREENCHER]                       |
| 3     | [PREENCHER]   | [PREENCHER]                        | [PREENCHER]    | [PREENCHER]                       |
| 4     | [PREENCHER]   | [PREENCHER]                        | [PREENCHER]    | [PREENCHER]                       |

**Fluxo B: [PREENCHER — nome do fluxo alternativo, ex.: Erro de validacao]**

| Passo | De (tela)     | Acao do usuario                    | Para (tela)    | Observacao                        |
|-------|---------------|------------------------------------|----------------|-----------------------------------|
| 1     | [PREENCHER]   | [PREENCHER]                        | [PREENCHER]    | [PREENCHER]                       |
| 2     | [PREENCHER]   | [PREENCHER]                        | [PREENCHER]    | [PREENCHER]                       |

### 4. Mapa de Hotspots

Documente todos os pontos clicaveis/interativos por tela.

**Tela: [PREENCHER — nome da tela]**

| # | Elemento              | Tipo de interacao        | Destino / Acao                     | Condicional?            |
|---|-----------------------|--------------------------|------------------------------------|-------------------------|
| 1 | [PREENCHER — botao/link/area] | [PREENCHER — tap / hover / drag] | [PREENCHER — vai para tela X / abre modal] | [Sim — condicao / Nao] |
| 2 | [PREENCHER]           | [PREENCHER]              | [PREENCHER]                        | [PREENCHER]             |
| 3 | [PREENCHER]           | [PREENCHER]              | [PREENCHER]                        | [PREENCHER]             |

**Tela: [PREENCHER — nome de outra tela]**

| # | Elemento              | Tipo de interacao        | Destino / Acao                     | Condicional?            |
|---|-----------------------|--------------------------|------------------------------------|-------------------------|
| 1 | [PREENCHER]           | [PREENCHER]              | [PREENCHER]                        | [PREENCHER]             |
| 2 | [PREENCHER]           | [PREENCHER]              | [PREENCHER]                        | [PREENCHER]             |

### 5. Especificacoes de Animacao

| # | Elemento / Transicao         | Tipo de animacao              | Duracao     | Easing              | Trigger                   |
|---|------------------------------|-------------------------------|-------------|----------------------|---------------------------|
| 1 | [PREENCHER — ex.: Transicao entre telas] | [PREENCHER — slide / fade / dissolve] | [PREENCHER] | [PREENCHER — ease-in-out] | [PREENCHER — tap no CTA] |
| 2 | [PREENCHER — ex.: Modal abrindo]  | [PREENCHER — scale + fade]   | [PREENCHER] | [PREENCHER]          | [PREENCHER]               |
| 3 | [PREENCHER — ex.: Loading spinner] | [PREENCHER — rotate loop]    | [PREENCHER] | [PREENCHER]          | [PREENCHER]               |
| 4 | [PREENCHER]                  | [PREENCHER]                   | [PREENCHER] | [PREENCHER]          | [PREENCHER]               |

**prefers-reduced-motion:** [PREENCHER — o que muda quando animacoes sao desligadas]

### 6. Cenarios de Teste

Cenarios para uso em testes de usabilidade ou validacao interna.

| # | Cenario                                   | Tarefa para o participante                     | Fluxo esperado        | Criterio de sucesso              |
|---|-------------------------------------------|------------------------------------------------|-----------------------|----------------------------------|
| 1 | [PREENCHER — contexto do cenario]         | [PREENCHER — instrucao para o usuario]         | [PREENCHER — fluxo A/B] | [PREENCHER — o que define sucesso] |
| 2 | [PREENCHER]                               | [PREENCHER]                                    | [PREENCHER]           | [PREENCHER]                      |
| 3 | [PREENCHER]                               | [PREENCHER]                                    | [PREENCHER]           | [PREENCHER]                      |
| 4 | [PREENCHER]                               | [PREENCHER]                                    | [PREENCHER]           | [PREENCHER]                      |

### 7. Criterios de Sucesso do Prototipo

**Metricas quantitativas:**

| Metrica                                  | Meta                           |
|------------------------------------------|--------------------------------|
| Task completion rate                     | [PREENCHER — ex.: >= 80%]     |
| Tempo medio para completar tarefa        | [PREENCHER — ex.: < 2 min]    |
| Numero de erros por tarefa               | [PREENCHER — ex.: <= 1]       |
| [PREENCHER — metrica adicional]          | [PREENCHER]                    |

**Criterios qualitativos:**

- [ ] [PREENCHER — ex.: Usuarios entendem o proximo passo sem ajuda]
- [ ] [PREENCHER — ex.: Nenhum participante confunde botao X com botao Y]
- [ ] [PREENCHER — ex.: Feedback geral positivo sobre a experiencia]
- [ ] [PREENCHER]

**Decisao apos teste:**
- Se criterios atendidos: [PREENCHER — ex.: Seguir para hi-fi / handoff]
- Se criterios nao atendidos: [PREENCHER — ex.: Iterar e retestar]

## Example (Parcialmente Preenchido)

**Projeto:** Onboarding do app MindFlow
**Escopo:** Happy path de cadastro + selecao de preferencias (6 telas). Fora do escopo: login com social, recuperacao de senha.
**Tela inicial:** Splash screen. **Tela final:** Home personalizada.
**Fluxo A:** Splash → Welcome → Cadastro email → Selecao interesses → Selecao horario → Home.
**Animacao:** Transicao entre telas com slide-left (300ms, ease-out). Modal de termos com fade-in (200ms).
**Cenario 1:** "Imagine que voce acabou de baixar um app de meditacao. Crie sua conta e configure suas preferencias."
**Criterio:** 90% completam sem ajuda, tempo medio < 3 min.

## Notes

- Nomeie as telas de forma consistente no Figma — facilita manutencao e documentacao.
- Teste o prototipo em dispositivo real antes de usa-lo com participantes.
- Prototipos de baixa fidelidade sao melhores para testar conceito; alta fidelidade para testar interacao.
- Documente bugs conhecidos do prototipo para nao confundir com problemas de design.
- Mantenha o prototipo atualizado — versoes desatualizadas geram confusao.
- Inclua dead-ends intencionais (ex.: "esta tela nao esta no escopo") quando necessario.

---

## Cross-references

- **Template de teste:** [Usability Test Plan](../research/usability-test-plan.md)
- **Template de motion:** [Motion Spec Template](../ui/motion-spec-template.md)
- **Template de wireframe:** [Wireframe Pack Template](../ui/wireframe-pack-template.md)
- **Task:** [Build Prototype](../../tasks/ui/build-prototype.md)
- **Task:** [Run Usability Test](../../tasks/research/run-usability-test.md)
- **Checklist:** [Prototyping Quality](../../checklists/prototyping-quality.md)
- **Checklist:** [Motion Quality](../../checklists/motion-quality.md)
- **Framework:** [Prototyping Layer](../../frameworks/prototyping-layer.md)
- **Framework:** [Usability Testing Framework](../../frameworks/usability-testing-framework.md)
- **Agent:** [Jessica UX/UI](../../agents/jessica-ux-ui.md)
- **Agent:** [UX Design Expert](../../agents/ux-design-expert.md)
