# Accessibility Audit Brief

## Metadata

| Campo               | Valor                                            |
|---------------------|--------------------------------------------------|
| **Produto / Feature** | [PREENCHER — nome do produto ou feature]       |
| **Solicitante**     | [PREENCHER — quem solicitou a auditoria]         |
| **Auditor(a)**      | [PREENCHER — responsavel pela auditoria]         |
| **Data de criacao** | [PREENCHER — YYYY-MM-DD]                         |
| **Standard alvo**   | [PREENCHER — WCAG 2.1 AA / WCAG 2.2 AA / AAA]  |
| **Status**          | [PREENCHER — Planejado / Em andamento / Concluido] |
| **Deadline**        | [PREENCHER — data de entrega do relatorio]       |

## Instructions (Como Usar)

1. Preencha este brief antes de iniciar qualquer auditoria de acessibilidade.
2. Defina claramente o escopo — auditar tudo de uma vez e ineficiente.
3. Alinhe com o time de engenharia sobre a disponibilidade do ambiente de teste.
4. Use o checklist da secao 6 como guia durante a auditoria.
5. Registre os findings no template de report de a11y ao finalizar.

> **Dica:** Priorize fluxos criticos do usuario — login, cadastro, pagamento, e principal funcionalidade do produto.

## Template

### 1. Objetivo da Auditoria

[PREENCHER — qual o objetivo principal? Compliance legal? Melhoria de experiencia? Lancamento de feature?]

### 2. Escopo

**Paginas / Telas a auditar:**

| # | Pagina / Tela              | URL / Rota                    | Prioridade |
|---|----------------------------|-------------------------------|------------|
| 1 | [PREENCHER — pagina]       | [PREENCHER — URL]             | Alta       |
| 2 | [PREENCHER — pagina]       | [PREENCHER — URL]             | Alta       |
| 3 | [PREENCHER — pagina]       | [PREENCHER — URL]             | Media      |
| 4 | [PREENCHER — pagina]       | [PREENCHER — URL]             | Baixa      |

**Fora do escopo:**
- [PREENCHER — paginas ou areas nao incluidas]

### 3. Ambiente de Teste

- **URL de staging/test:** [PREENCHER]
- **Credenciais de teste:** [PREENCHER — ou link para vault]
- **Browsers alvo:** [PREENCHER — Chrome, Firefox, Safari, Edge]
- **Devices:** [PREENCHER — Desktop, Tablet, Mobile]
- **Screen readers:** [PREENCHER — NVDA, VoiceOver, JAWS]

### 4. Criterios de Avaliacao

**Nivel de conformidade alvo:** [PREENCHER — WCAG 2.1 Level AA]

**Categorias a avaliar:**
- [ ] Perceivable — texto alternativo, contraste, legendas
- [ ] Operable — teclado, tempo, navegacao, input modalities
- [ ] Understandable — legibilidade, previsibilidade, assistencia a input
- [ ] Robust — compatibilidade com assistive technologies

### 5. Ferramentas de Auditoria

| Ferramenta           | Tipo                    | Uso planejado                    |
|----------------------|-------------------------|----------------------------------|
| [PREENCHER — ex.: axe] | Automatizada          | Scan inicial de paginas          |
| [PREENCHER — ex.: WAVE] | Automatizada          | Validacao visual                 |
| [PREENCHER — ex.: NVDA] | Screen reader         | Teste manual de navegacao        |
| [PREENCHER — ex.: Colour Contrast Analyser] | Manual | Verificacao de contraste |
| Keyboard only        | Manual                  | Teste de navegacao por teclado   |

### 6. Checklist de Auditoria (Resumo)

**Perceivable:**
- [ ] Todas as imagens possuem alt text adequado
- [ ] Contraste de texto atende ratio minimo (4.5:1 texto / 3:1 texto grande)
- [ ] Conteudo de video possui legendas/captions
- [ ] Informacao nao depende apenas de cor

**Operable:**
- [ ] Todos os elementos interativos sao acessiveis via teclado
- [ ] Ordem de foco (tab order) e logica
- [ ] Focus indicators sao visiveis
- [ ] Nao ha armadilhas de teclado (keyboard traps)

**Understandable:**
- [ ] Linguagem da pagina esta definida (`lang` attribute)
- [ ] Formularios possuem labels associados
- [ ] Mensagens de erro sao claras e acessiveis
- [ ] Navegacao e consistente entre paginas

**Robust:**
- [ ] HTML e semanticamente correto
- [ ] ARIA roles e attributes estao corretos
- [ ] Componentes customizados seguem ARIA patterns

### 7. Cronograma

| Fase               | Data                 | Responsavel     |
|--------------------|----------------------|-----------------|
| Preparacao         | [PREENCHER]          | [PREENCHER]     |
| Audit automatizado | [PREENCHER]          | [PREENCHER]     |
| Audit manual       | [PREENCHER]          | [PREENCHER]     |
| Report             | [PREENCHER]          | [PREENCHER]     |
| Review com eng     | [PREENCHER]          | [PREENCHER]     |

### 8. Entregaveis

- [ ] Relatorio de auditoria com severity ratings
- [ ] Lista de issues priorizadas
- [ ] Recomendacoes de fix com exemplos
- [ ] Retest plan para validar correcoes

## Example (Parcialmente Preenchido)

**Produto:** App de Delivery — Fluxo de Checkout
**Standard alvo:** WCAG 2.1 AA
**Paginas:** Carrinho, Endereco de entrega, Pagamento, Confirmacao
**Ferramentas:** axe DevTools, VoiceOver (macOS), teclado manual

## Notes

- Ferramentas automatizadas capturam apenas 30-40% dos problemas. Teste manual e essencial.
- Documente cada finding com: descricao, severity, criterio WCAG violado, e sugestao de fix.
- Considere incluir usuarios reais com deficiencia em testes quando possivel.
- Reagende a auditoria se o ambiente de teste nao estiver estavel.
- Mantenha um historico de auditorias para acompanhar evolucao ao longo do tempo.
