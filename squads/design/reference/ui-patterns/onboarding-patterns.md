# Onboarding Patterns

## Summary

Padrões de onboarding guiam novos usuários através dos primeiros momentos de interação com um produto, reduzindo a curva de aprendizado e aumentando a retenção. Um onboarding eficaz equilibra educação com ação, permitindo que o usuário comece a obter valor rapidamente. Este documento cobre welcome flows, tooltips, coach marks e progressive disclosure como estratégias fundamentais de onboarding.

## Key Concepts

### Welcome Flows

Fluxos de boas-vindas são sequências estruturadas que apresentam o produto ao novo usuário, coletam preferências iniciais e configuram o ambiente para o primeiro uso.

- **Welcome Screens**: Slides ou carrossel apresentando os principais benefícios do produto
- **Setup Wizard**: Fluxo guiado de configuração inicial com passos obrigatórios
- **Personalization Flow**: Coleta preferências do usuário para personalizar a experiência
- **Quick Start Guide**: Visão geral rápida das funcionalidades essenciais com links diretos
- **Video Introduction**: Vídeo curto demonstrando as funcionalidades principais

### Tooltips

Tooltips são elementos flutuantes que fornecem informações contextuais sobre elementos específicos da interface quando o usuário interage com eles.

- **Hover Tooltip**: Aparece ao passar o mouse sobre um elemento (desktop only)
- **Click Tooltip**: Aparece ao clicar em um ícone de ajuda ou informação
- **Contextual Tooltip**: Ativado automaticamente baseado no comportamento do usuário
- **Rich Tooltip**: Inclui formatação, links ou imagens além de texto simples
- **Persistent Tooltip**: Permanece visível até ser explicitamente dispensado

### Coach Marks

Coach marks são destaques visuais que direcionam a atenção do usuário para elementos específicos da interface, geralmente como parte de um tour guiado.

- **Spotlight Tour**: Destaca um elemento por vez com overlay escurecendo o restante
- **Hotspot Indicators**: Pontos pulsantes que indicam elementos interativos para explorar
- **Sequential Tour**: Guia passo-a-passo pelos principais elementos da interface
- **Contextual Coach Mark**: Aparece quando o usuário acessa uma funcionalidade pela primeira vez
- **Dismissible Tour**: Permite que o usuário pule ou encerre o tour a qualquer momento

### Progressive Disclosure

Progressive disclosure é a estratégia de revelar funcionalidades gradualmente, mostrando apenas o essencial inicialmente e disponibilizando opções avançadas conforme o usuário amadurece.

- **Layered Interface**: Funcionalidades básicas visíveis, avançadas sob "Show more"
- **Contextual Features**: Funcionalidades reveladas quando se tornam relevantes
- **Level-based Unlock**: Funcionalidades desbloqueadas conforme o usuário progride
- **Complexity Gradient**: Interface simplificada inicialmente, com opção de modo avançado
- **Smart Defaults**: Valores pré-configurados que funcionam para a maioria dos usuários

## When to Use

| Padrão | Cenário Ideal | Evitar Quando |
|--------|--------------|---------------|
| Welcome Flow | Primeiro acesso ao produto ou nova versão major | O produto é simples e auto-explicativo |
| Tooltips | Elementos que precisam de explicação pontual | A informação é essencial e deve estar sempre visível |
| Coach Marks | Interface complexa com muitas funcionalidades | O usuário é experiente e já conhece a interface |
| Progressive Disclosure | Interface com funcionalidades para diferentes níveis de expertise | Todas as opções são igualmente importantes |

## Anatomy

### Welcome Flow Structure

```
┌─ Screen 1 ──────────────┐  ┌─ Screen 2 ──────────────┐  ┌─ Screen 3 ──────────────┐
│                          │  │                          │  │                          │
│    [Ilustração]          │  │    [Ilustração]          │  │    [Ilustração]          │
│                          │  │                          │  │                          │
│  Bem-vindo ao App!       │  │  Organize seus projetos  │  │  Colabore com sua equipe │
│  Descrição breve do      │  │  Descrição da funciona-  │  │  Descrição da funciona-  │
│  valor principal.        │  │  lidade de organização.  │  │  lidade colaborativa.    │
│                          │  │                          │  │                          │
│  ● ○ ○                   │  │  ○ ● ○                   │  │  ○ ○ ●                   │
│  [Pular]  [Próximo →]   │  │  [← Voltar] [Próximo →] │  │  [← Voltar] [Começar!]  │
└──────────────────────────┘  └──────────────────────────┘  └──────────────────────────┘
```

### Coach Mark Structure

```
┌────────────────────────────────────────────────────────┐
│  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  │
│  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  │
│  ░░░░░░┌─────────────────────┐░░░░░░░░░░░░░░░░░░░░░  │
│  ░░░░░░│  Elemento Destacado  │░░░░░░░░░░░░░░░░░░░░░  │
│  ░░░░░░└─────────────────────┘░░░░░░░░░░░░░░░░░░░░░  │
│  ░░░░░░░░░░░│░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  │
│  ░░░░░░░░░░░▼░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  │
│  ░░░░┌─────────────────────────┐░░░░░░░░░░░░░░░░░░░  │
│  ░░░░│ Título do Coach Mark    │░░░░░░░░░░░░░░░░░░░  │
│  ░░░░│ Explicação breve sobre  │░░░░░░░░░░░░░░░░░░░  │
│  ░░░░│ este elemento.          │░░░░░░░░░░░░░░░░░░░  │
│  ░░░░│ [Pular] [2/5] [Próx →] │░░░░░░░░░░░░░░░░░░░  │
│  ░░░░└─────────────────────────┘░░░░░░░░░░░░░░░░░░░  │
│  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  │
└────────────────────────────────────────────────────────┘
```

### Tooltip Anatomy

```
                    ┌──────────────────────────┐
                    │ Texto explicativo sobre   │
                    │ o elemento apontado.      │
                    └────────────┬─────────────┘
                                 ▼
                         [Elemento UI]
```

## Variations

### Por Timing

- **First-run Onboarding**: Executado apenas no primeiro acesso do usuário
- **Feature Onboarding**: Ativado quando uma nova funcionalidade é lançada
- **Contextual Onboarding**: Disparado quando o usuário acessa uma área pela primeira vez
- **Re-engagement Onboarding**: Para usuários que retornam após longo período de inatividade

### Por Abordagem

- **Self-serve**: Usuário explora no seu próprio ritmo com ajuda sob demanda
- **Guided**: Tour estruturado que guia o usuário passo a passo
- **Hybrid**: Combinação de tour inicial com dicas contextuais ao longo do uso
- **Gamified**: Usa elementos de gamificação como checklists e achievements

## Best Practices

1. **Permita sempre pular**: Todo fluxo de onboarding deve ser dispensável
2. **Mantenha curto**: Limite welcome flows a 3-5 telas no máximo
3. **Foque no valor, não nas features**: Mostre o que o usuário pode alcançar
4. **Use a abordagem "learn by doing"**: Prefira ações práticas a explicações teóricas
5. **Personalize quando possível**: Adapte o onboarding ao perfil e objetivo do usuário
6. **Meça e itere**: Tracked onde os usuários abandonam e otimize esses pontos
7. **Não sobrecarregue**: Revele informações gradualmente, não tudo de uma vez
8. **Forneça acesso posterior**: Permita revisitar o tour ou dicas a qualquer momento
9. **Celebre marcos**: Reconheça quando o usuário completa etapas importantes
10. **Teste com usuários novos**: O onboarding deve ser testado com pessoas sem experiência prévia

## Accessibility Considerations

- Welcome flows devem ser navegáveis por teclado com foco gerenciado entre slides
- Tooltips devem ser acessíveis via keyboard focus, não apenas hover do mouse
- Coach marks com overlay devem implementar focus trap e ser dismissíveis via Escape
- Conteúdo de tooltips deve ser acessível via `aria-describedby` vinculado ao elemento
- Tours sequenciais devem anunciar a navegação entre passos via `aria-live` regions
- Animações devem respeitar `prefers-reduced-motion` para usuários sensíveis a movimento
- Progressive disclosure deve garantir que conteúdo oculto ainda seja acessível por screen readers
- Hotspot indicators devem ter alternativa textual e ser focáveis por teclado
- Todo conteúdo educativo deve estar disponível em formato alternativo (não apenas visual)

## Cross-References

- Ver `feedback-patterns.md` para padrões de toasts e alerts usados durante onboarding
- Ver `form-patterns.md` para formulários de configuração inicial em setup wizards
- Ver `navigation-patterns.md` para orientação do usuário na estrutura de navegação
- Ver `dashboard-patterns.md` para onboarding em contextos de dashboard
- Ver `authentication-patterns.md` para fluxo de onboarding pós-registro
