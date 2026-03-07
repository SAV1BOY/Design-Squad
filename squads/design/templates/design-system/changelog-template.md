# Design System Changelog Template

## Metadata

| Campo                | Valor                                           |
|----------------------|--------------------------------------------------|
| **DS Name**          | [PREENCHER — nome do design system]              |
| **Versao**           | [PREENCHER — ex.: v3.2.0]                        |
| **Data de release**  | [PREENCHER — YYYY-MM-DD]                         |
| **Release manager**  | [PREENCHER — responsavel pelo release]           |
| **Tipo de release**  | [PREENCHER — Major / Minor / Patch]              |
| **Breaking changes** | [PREENCHER — Sim / Nao]                          |
| **Migration guide**  | [PREENCHER — link, se aplicavel]                 |

## Instructions (Como Usar)

1. Preencha este changelog para cada release do design system.
2. Categorize mudancas em: Added, Changed, Deprecated, Removed, Fixed, Security.
3. Comunique breaking changes com destaque e inclua migration guide.
4. Publique junto com o release — squads precisam saber o que mudou.
5. Mantenha um historico ordenado por versao (mais recente primeiro).

> **Dica:** Escreva pensando no consumidor do DS — use linguagem clara e inclua links para docs atualizados.

## Template

---

### [PREENCHER — vX.Y.Z] — [PREENCHER — YYYY-MM-DD]

**Resumo do release:** [PREENCHER — 1-2 frases sobre o que este release traz de mais importante]

**Compatibilidade:** [PREENCHER — compativel com versao anterior / requer migracao]

---

#### Added (Novo)

| Componente / Token     | Descricao                                    | Docs link            |
|------------------------|----------------------------------------------|----------------------|
| [PREENCHER — nome]     | [PREENCHER — o que foi adicionado]           | [PREENCHER — link]   |
| [PREENCHER — nome]     | [PREENCHER]                                  | [PREENCHER]          |
| [PREENCHER — nome]     | [PREENCHER]                                  | [PREENCHER]          |

#### Changed (Alterado)

| Componente / Token     | Antes                    | Depois                   | Motivo               |
|------------------------|--------------------------|--------------------------|----------------------|
| [PREENCHER — nome]     | [PREENCHER — valor/comp] | [PREENCHER — novo valor] | [PREENCHER — motivo] |
| [PREENCHER — nome]     | [PREENCHER]              | [PREENCHER]              | [PREENCHER]          |

#### Deprecated (Depreciado)

| Componente / Token     | Substituto                  | Removal date         |
|------------------------|-----------------------------|----------------------|
| [PREENCHER — nome]     | [PREENCHER — novo nome/comp]| [PREENCHER — versao] |
| [PREENCHER — nome]     | [PREENCHER]                 | [PREENCHER]          |

> Itens deprecated continuam funcionando nesta versao mas serao removidos em [PREENCHER — versao futura].

#### Removed (Removido)

| Componente / Token     | Motivo                          | Substituto                |
|------------------------|---------------------------------|---------------------------|
| [PREENCHER — nome]     | [PREENCHER — justificativa]     | [PREENCHER — alternativa] |

#### Fixed (Corrigido)

| Componente / Token     | Bug                              | Fix                       |
|------------------------|----------------------------------|---------------------------|
| [PREENCHER — nome]     | [PREENCHER — descricao do bug]   | [PREENCHER — correcao]    |
| [PREENCHER — nome]     | [PREENCHER]                      | [PREENCHER]               |
| [PREENCHER — nome]     | [PREENCHER]                      | [PREENCHER]               |

#### Breaking Changes

> **ATENCAO:** As seguintes mudancas requerem atualizacao no codigo dos consumidores.

| Mudanca                         | Impacto                          | Como migrar                   |
|---------------------------------|----------------------------------|-------------------------------|
| [PREENCHER — mudanca]           | [PREENCHER — o que quebra]       | [PREENCHER — passo a passo]   |
| [PREENCHER — mudanca]           | [PREENCHER]                      | [PREENCHER]                   |

**Migration guide completo:** [PREENCHER — link para guia detalhado]

---

### Releases Anteriores

#### [PREENCHER — vX.Y.Z] — [PREENCHER — YYYY-MM-DD]

**Added:**
- [PREENCHER — item adicionado]
- [PREENCHER — item adicionado]

**Changed:**
- [PREENCHER — item alterado]

**Fixed:**
- [PREENCHER — bug corrigido]
- [PREENCHER — bug corrigido]

---

#### [PREENCHER — vX.Y.Z] — [PREENCHER — YYYY-MM-DD]

**Added:**
- [PREENCHER]

**Fixed:**
- [PREENCHER]

---

### Metricas do Release

| Metrica                         | Valor                            |
|---------------------------------|----------------------------------|
| Componentes novos               | [PREENCHER — numero]             |
| Componentes alterados           | [PREENCHER — numero]             |
| Bugs corrigidos                 | [PREENCHER — numero]             |
| Tokens adicionados/alterados    | [PREENCHER — numero]             |
| Breaking changes                | [PREENCHER — numero]             |
| Squads impactados               | [PREENCHER — numero]             |

### Comunicacao

- [ ] Changelog publicado em [PREENCHER — canal/plataforma]
- [ ] Slack notification enviada para [PREENCHER — canais]
- [ ] Migration guide compartilhado
- [ ] Office hours agendado para duvidas — [PREENCHER — data]
- [ ] Storybook atualizado — [PREENCHER — link]
- [ ] Figma library atualizada e publicada

## Example (Parcialmente Preenchido)

**v3.2.0 — 2026-02-20**
**Added:** Novo componente `DateRangePicker` com suporte a presets (7d, 30d, 90d, custom).
**Changed:** `Button` — padding horizontal aumentado de 16px para 20px em tamanho Medium.
**Fixed:** `Modal` — focus trap nao funcionava corretamente com nested modals.
**Breaking:** Prop `size` do `Input` renomeada de `inputSize` para `size` — buscar e substituir necessario.

## Notes

- Siga Semantic Versioning: Major (breaking), Minor (novo, compativel), Patch (fix).
- Publique o changelog no mesmo momento do release do pacote.
- Inclua links diretos para Storybook e Figma sempre que possivel.
- Para breaking changes, ofereca codemod ou script de migracao quando viavel.
- Mantenha historico completo — nunca delete entradas de changelog anteriores.
