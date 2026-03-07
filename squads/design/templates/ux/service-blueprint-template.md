# Service Blueprint Template

## Metadata

| Campo                | Valor                                           |
|----------------------|--------------------------------------------------|
| **Servico**          | [PREENCHER — nome do servico mapeado]            |
| **Escopo**           | [PREENCHER — jornada ou fluxo especifico]        |
| **Autor(a)**         | [PREENCHER — designer responsavel]               |
| **Colaboradores**    | [PREENCHER — quem participou do mapeamento]      |
| **Data de criacao**  | [PREENCHER — YYYY-MM-DD]                         |
| **Status**           | [PREENCHER — As-is / To-be / Validado]           |
| **Fontes**           | [PREENCHER — entrevistas, documentacao, observacao] |

## Instructions (Como Usar)

1. Mapeie primeiro as acoes do usuario (customer actions) como base.
2. Para cada acao, identifique o que acontece no frontstage e backstage.
3. Identifique as linhas de interacao, visibilidade e interacao interna.
4. Mapeie os support processes e sistemas de suporte para cada etapa.
5. Use colaborativamente com times de produto, eng, ops e CS.

> **Dica:** Service blueprints sao mais ricos que journey maps porque incluem a perspectiva operacional. Use quando precisar alinhar frontend e backend da experiencia.

## Template

### 1. Escopo e Cenario

**Servico:** [PREENCHER — descricao do servico]
**Cenario mapeado:** [PREENCHER — situacao especifica]
**Persona/Usuario:** [PREENCHER — quem esta usando o servico]
**Ponto de inicio:** [PREENCHER — onde a jornada comeca]
**Ponto de fim:** [PREENCHER — onde a jornada termina]

### 2. Legenda

- **Customer Actions:** Acoes visiveis do usuario
- **Frontstage:** Interacoes diretas entre usuario e servico (interfaces, atendentes)
- **Line of Visibility:** Divisoria entre o que o usuario ve e o que nao ve
- **Backstage:** Processos internos nao visiveis ao usuario
- **Support Processes:** Sistemas, ferramentas e infraestrutura de apoio

### 3. Blueprint — Fase 1: [PREENCHER — nome da fase]

**Customer Actions:**
- [PREENCHER — acao do usuario 1]
- [PREENCHER — acao do usuario 2]

**Physical Evidence:**
- [PREENCHER — artefato tangivel, ex.: email, tela, documento]

--- LINE OF INTERACTION ---

**Frontstage (Employee/System Actions):**
- [PREENCHER — o que o sistema/atendente faz visivelmente]
- [PREENCHER — resposta visivel ao usuario]

--- LINE OF VISIBILITY ---

**Backstage Actions:**
- [PREENCHER — processo interno 1]
- [PREENCHER — processo interno 2]

--- LINE OF INTERNAL INTERACTION ---

**Support Processes:**
- [PREENCHER — sistema/ferramenta de suporte]
- [PREENCHER — base de dados / API / servico externo]

**Tempo estimado:** [PREENCHER — duracao desta fase]
**Pain points:** [PREENCHER — problemas identificados]

---

### 4. Blueprint — Fase 2: [PREENCHER — nome da fase]

**Customer Actions:**
- [PREENCHER]
- [PREENCHER]

**Physical Evidence:**
- [PREENCHER]

--- LINE OF INTERACTION ---

**Frontstage:**
- [PREENCHER]

--- LINE OF VISIBILITY ---

**Backstage Actions:**
- [PREENCHER]
- [PREENCHER]

--- LINE OF INTERNAL INTERACTION ---

**Support Processes:**
- [PREENCHER]

**Tempo estimado:** [PREENCHER]
**Pain points:** [PREENCHER]

---

### 5. Blueprint — Fase 3: [PREENCHER — nome da fase]

**Customer Actions:**
- [PREENCHER]

**Physical Evidence:**
- [PREENCHER]

--- LINE OF INTERACTION ---

**Frontstage:**
- [PREENCHER]

--- LINE OF VISIBILITY ---

**Backstage Actions:**
- [PREENCHER]

--- LINE OF INTERNAL INTERACTION ---

**Support Processes:**
- [PREENCHER]

**Tempo estimado:** [PREENCHER]
**Pain points:** [PREENCHER]

---

### 6. Blueprint — Fase 4: [PREENCHER — nome da fase]

**Customer Actions:**
- [PREENCHER]

**Physical Evidence:**
- [PREENCHER]

--- LINE OF INTERACTION ---

**Frontstage:**
- [PREENCHER]

--- LINE OF VISIBILITY ---

**Backstage Actions:**
- [PREENCHER]

--- LINE OF INTERNAL INTERACTION ---

**Support Processes:**
- [PREENCHER]

**Tempo estimado:** [PREENCHER]
**Pain points:** [PREENCHER]

### 7. Pontos de Falha e Wait Points

| Tipo             | Fase | Descricao                             | Impacto          |
|------------------|------|---------------------------------------|------------------|
| Fail point       | [PREENCHER] | [PREENCHER — onde o processo pode falhar] | [PREENCHER] |
| Wait point       | [PREENCHER] | [PREENCHER — onde o usuario espera]   | [PREENCHER]      |
| Decision point   | [PREENCHER] | [PREENCHER — onde uma decisao e tomada] | [PREENCHER]    |
| Fail point       | [PREENCHER] | [PREENCHER]                           | [PREENCHER]      |

### 8. Metricas por Fase

| Fase          | Metrica                    | Valor atual     | Meta            |
|---------------|----------------------------|-----------------|-----------------|
| [PREENCHER]   | [PREENCHER — ex.: tempo]   | [PREENCHER]     | [PREENCHER]     |
| [PREENCHER]   | [PREENCHER — ex.: taxa erro]| [PREENCHER]    | [PREENCHER]     |
| [PREENCHER]   | [PREENCHER — ex.: NPS fase]| [PREENCHER]     | [PREENCHER]     |

### 9. Oportunidades de Melhoria

| # | Oportunidade                          | Camada          | Impacto | Esforco |
|---|---------------------------------------|-----------------|---------|---------|
| 1 | [PREENCHER — melhoria]                | Frontstage / Backstage / Support | [PREENCHER] | [PREENCHER] |
| 2 | [PREENCHER — melhoria]                | [PREENCHER]     | [PREENCHER] | [PREENCHER] |
| 3 | [PREENCHER — melhoria]                | [PREENCHER]     | [PREENCHER] | [PREENCHER] |

### 10. Proximos Passos

- [ ] [PREENCHER — acao de curto prazo]
- [ ] [PREENCHER — acao de medio prazo]
- [ ] [PREENCHER — acao de longo prazo]
- [ ] Validar blueprint com times de [PREENCHER — areas]

## Example (Parcialmente Preenchido)

**Servico:** Plataforma de agendamento medico
**Fase 2 — Agendamento:**
- Customer Action: Seleciona medico, data e horario
- Physical Evidence: Tela de calendario com horarios disponiveis
- Frontstage: Sistema exibe disponibilidade em tempo real
- Backstage: API consulta agenda do medico no sistema hospitalar
- Support: Sistema de gestao hospitalar (HIS), cache de disponibilidade
- Fail point: API do HIS pode estar indisponivel, causando erro de carregamento

## Notes

- Service blueprints devem ser criados colaborativamente — nenhum time tem visao completa sozinho.
- Comece pelo journey map e adicione as camadas de backstage e support.
- Identifique handoffs entre times — sao frequentes fontes de falha.
- Mantenha versoes as-is (atual) e to-be (desejada) separadas.
- Use cores ou icones para destacar fail points e wait points no diagrama visual.
