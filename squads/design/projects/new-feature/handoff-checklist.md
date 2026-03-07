# Handoff Checklist Template

## Informacoes do Projeto

| Campo | Valor |
|-------|-------|
| **Feature** | [Nome da feature] |
| **Designer** | [Nome do designer] |
| **Dev Lead** | [Nome do dev responsavel] |
| **Data do Handoff** | [YYYY-MM-DD] |
| **Figma Link** | [URL do arquivo] |

## Pre-Handoff Checklist

Itens que devem ser verificados pelo designer ANTES de iniciar
o processo de handoff com o time de engenharia.

### Design Files

- [ ] Arquivo Figma organizado com naming convention padrao
- [ ] Todas as telas nomeadas corretamente
- [ ] Frames organizados por fluxo e estado
- [ ] Componentes atualizados (sem detached components)
- [ ] Auto layout aplicado corretamente
- [ ] Constraints definidos para responsividade

### Design Tokens

- [ ] Cores utilizando tokens do Design System
- [ ] Tipografia utilizando estilos do Design System
- [ ] Espacamento seguindo o grid e tokens de spacing
- [ ] Elevacao (shadows) utilizando tokens padrao
- [ ] Border radius seguindo tokens padrao

### Estados e Variacoes

- [ ] Default state documentado
- [ ] Hover state documentado
- [ ] Active/pressed state documentado
- [ ] Focus state documentado (acessibilidade)
- [ ] Disabled state documentado
- [ ] Loading state documentado
- [ ] Error state documentado
- [ ] Empty state documentado
- [ ] Success state documentado

### Responsividade

- [ ] Layout mobile (320px - 767px) definido
- [ ] Layout tablet (768px - 1023px) definido
- [ ] Layout desktop (1024px - 1439px) definido
- [ ] Layout large desktop (1440px+) definido
- [ ] Comportamento entre breakpoints documentado

### Acessibilidade

- [ ] Contraste verificado (WCAG 2.1 AA)
- [ ] Tab order definido e documentado
- [ ] ARIA labels especificados
- [ ] Alt text para imagens definido
- [ ] Screen reader behavior documentado
- [ ] Hierarquia de headings correta

## Documentacao de Handoff

### Especificacoes Tecnicas

| Item | Detalhe | Referencia |
|------|---------|-----------|
| Espacamento | [Valores e tokens] | [Link/frame no Figma] |
| Tipografia | [Estilos utilizados] | [Link/frame no Figma] |
| Cores | [Tokens utilizados] | [Link/frame no Figma] |
| Animacoes | [Duracao e easing] | [Link/frame no Figma] |

### Comportamentos Interativos

Documente comportamentos que nao sao obvios visualmente.

| Interacao | Comportamento | Notas |
|-----------|---------------|-------|
| [Interacao 1] | [Descricao detalhada] | [Notas adicionais] |
| [Interacao 2] | [Descricao detalhada] | [Notas adicionais] |

### Conteudo e Copy

- [ ] Textos finais revisados pelo content team
- [ ] Traducoes necessarias identificadas
- [ ] Textos de error messages definidos
- [ ] Textos de empty states definidos
- [ ] Textos de tooltips definidos
- [ ] Placeholders definidos

### Assets

- [ ] Icones exportados em SVG
- [ ] Ilustracoes exportadas nos formatos necessarios
- [ ] Imagens otimizadas e em resolucao adequada
- [ ] Assets nomeados com convencao padrao

## Reuniao de Handoff

### Agenda Sugerida

1. **Contexto** (5 min) — Apresentacao do problema e solucao
2. **Walkthrough** (15 min) — Demonstracao do fluxo principal
3. **Detalhes tecnicos** (10 min) — Especificacoes e edge cases
4. **Perguntas** (10 min) — Duvidas do time de engenharia
5. **Proximos passos** (5 min) — Alinhamento de timeline

### Participantes Obrigatorios

- [ ] Designer responsavel
- [ ] Dev lead
- [ ] QA lead
- [ ] Product Owner

## Pos-Handoff


---
