# Search Patterns

## Pattern Description

Padroes para funcionalidade de busca em interfaces. Cobre search bars, autocomplete, busca com filtros, resultados de busca, busca recente e busca global (command palette).

## Patterns

### Search Bar Basico

```html
<form class="search" role="search" aria-label="Busca global">
  <label for="search-input" class="sr-only">Buscar</label>
  <input
    id="search-input"
    type="search"
    placeholder="Buscar projetos, pessoas, arquivos..."
    autocomplete="off"
    aria-describedby="search-hint"
  />
  <kbd class="search-shortcut">⌘K</kbd>
</form>
```

### Autocomplete / Typeahead

```
Input: "des"
┌──────────────────────────────────┐
│ 🔍 des                          │
├──────────────────────────────────┤
│ Sugestoes                        │
│   Design System                  │
│   Design Sprint Q1               │
│   Desktop Responsive Audit       │
│                                  │
│ Pessoas                          │
│   👤 Designer Ana Silva          │
├──────────────────────────────────┤
│ Buscar "des" em todos →          │
└──────────────────────────────────┘
```

Regras:
- Inicie sugestoes apos 2+ caracteres
- Debounce de 300ms para evitar requests excessivos
- Agrupe resultados por tipo/categoria
- Destaque o trecho que corresponde ao termo
- Maximo 7-10 sugestoes visiveis

### Command Palette (Global Search)

```
⌘K para abrir:
┌──────────────────────────────────┐
│ > Buscar comandos ou arquivos... │
├──────────────────────────────────┤
│ Recentes                         │
│   📄 Dashboard Redesign          │
│   ⚙️ Configuracoes               │
│                                  │
│ Acoes                            │
│   + Criar novo projeto           │
│   📤 Exportar relatorio          │
│   🔔 Configurar notificacoes     │
└──────────────────────────────────┘
```

### Search Results Page

```
┌──────────────────────────────────┐
│ Resultados para "dashboard"       │
│ 42 resultados (0.3s)             │
│                                  │
│ Filtros: [Todos] [Projetos]      │
│          [Arquivos] [Pessoas]    │
│                                  │
│ 📄 Dashboard Redesign v2         │
│    Projeto · Atualizado 2 dias   │
│    "...novo dashboard com..."    │
│                                  │
│ 📄 Dashboard Metrics Q4          │
│    Arquivo · Criado 15/01/2026   │
│    "...metricas do dashboard..." │
└──────────────────────────────────┘
```

### Recent Searches

```
Ao focar no input (sem digitar):
┌──────────────────────────────────┐
│ Buscas recentes                  │
│   🕐 design system tokens        │
│   🕐 onboarding flow             │
│   🕐 accessibility audit         │
│                                  │
│ [Limpar historico]               │
└──────────────────────────────────┘
```

## Analysis

Busca eficaz:
- Deve ser acessivel via teclado (shortcut global)
- Resultados relevantes em < 500ms
- Tolere erros de digitacao (fuzzy matching)
- Preserve contexto de busca na URL
- Ofereça filtros para refinar sem refazer busca
- Mostre empty state util quando sem resultados

## Tags

`search`, `autocomplete`, `command-palette`, `typeahead`, `information-retrieval`
