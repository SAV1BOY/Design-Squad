# Onboarding Patterns

## Pattern Description

Padroes para onboarding de novos usuarios — desde o primeiro acesso ate a ativacao. Cobre welcome tours, progressive profiling, checklists de setup, tooltips educativos e empty states como onboarding.

## Patterns

### Welcome Screen

```
┌────────────────────────────────────┐
│       Bem-vindo ao [Produto]!      │
│                                    │
│  [Ilustracao / animacao]           │
│                                    │
│  Organize seus projetos, colabore  │
│  com sua equipe e acompanhe        │
│  resultados em tempo real.         │
│                                    │
│  [Comecar setup]  [Explorar]       │
└────────────────────────────────────┘
```

### Setup Checklist

```
┌────────────────────────────────────┐
│  Configure sua conta (2 de 4)      │
│  ━━━━━━━━━━━━━━░░░░░░░  50%       │
│                                    │
│  ✅ Criar conta                    │
│  ✅ Completar perfil               │
│  ○  Convidar equipe                │
│  ○  Criar primeiro projeto         │
│                                    │
│  [Continuar: Convidar equipe →]    │
└────────────────────────────────────┘
```

### Tooltip Tour

```
Passo 1 de 4:
┌─────────────────────────────────┐
│  Este e o seu dashboard.        │
│  Aqui voce acompanha metricas   │
│  e atividades recentes.         │
│                                 │
│  [Pular tour]  [Proximo →]      │
└─────────────────────────────────┘
         ▼ (pointing to dashboard)
```

Regras do tour:
- Maximo 5 passos
- Sempre ofereca opcao de pular
- Destaque o elemento referenciado com spotlight
- Nao bloqueie a interacao principal

### Progressive Profiling

```
Coleta de dados em etapas ao longo do tempo:
- Signup: apenas email + senha
- Primeiro login: nome + cargo
- Apos 3 dias: tamanho da equipe + objetivo
- Apos primeira acao: preferencias de notificacao
```

### Contextual Education

```
Momento de ensino no ponto de acao:
- Tooltip ao hover em feature nova (badge "Novo")
- Coach mark na primeira vez que usuario acessa uma tela
- Inline tip dentro de um formulario complexo
- Video curto (< 30s) em contexto
```

## Analysis

Onboarding eficaz:
- Reduz time-to-value (tempo ate primeiro resultado de valor)
- E progressivo, nao front-loaded (nao despeja tudo de uma vez)
- Respeita diferentes estilos de aprendizado (visual, textual, hands-on)
- Pode ser re-acessado (help center, tour replay)
- Mede completion rate de cada etapa para otimizar

## Tags

`onboarding`, `first-use`, `activation`, `progressive-disclosure`, `engagement`
