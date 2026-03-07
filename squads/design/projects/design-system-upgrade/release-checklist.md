# Release Checklist Template

## Informacoes do Release

| Campo | Valor |
|-------|-------|
| **Versao** | [ex. v4.0.0] |
| **Tipo de Release** | [Major / Minor / Patch] |
| **Release Manager** | [Nome] |
| **Data Planejada** | [YYYY-MM-DD] |
| **Data Real** | [YYYY-MM-DD] |

## Pre-Release Checklist

### Codigo e Qualidade

- [ ] Todos os PRs do milestone foram merged
- [ ] Code review concluido em todos os PRs
- [ ] Nenhum bug critico ou major aberto
- [ ] Test suite passando (100% green)
- [ ] Visual regression tests aprovados
- [ ] a11y audit concluido e aprovado
- [ ] Performance benchmarks dentro dos thresholds
- [ ] Cross-browser testing concluido

### Documentacao

- [ ] Changelog atualizado com todas as mudancas
- [ ] Migration guide escrito e revisado
- [ ] API documentation atualizada
- [ ] Storybook atualizado com novos componentes/variantes
- [ ] Release notes escritas para comunicacao
- [ ] Breaking changes claramente documentados

### Design Assets

- [ ] Biblioteca Figma atualizada
- [ ] Componentes Figma sincronizados com codigo
- [ ] Design tokens atualizados no Figma
- [ ] Templates e exemplos atualizados
- [ ] Thumbnails e previews atualizados no Storybook

### Comunicacao

- [ ] Release notes revisadas pelo Design System Lead
- [ ] Email de anuncio preparado
- [ ] Post no Slack preparado (#design-system channel)
- [ ] Office hours agendadas para suporte pos-release
- [ ] FAQ atualizado com perguntas antecipadas

## Release Day Checklist

### Sequencia de Release

Siga esta sequencia rigorosamente para evitar problemas.

#### 1. Preparacao (1h antes)

- [ ] Verificar CI/CD pipeline saudavel
- [ ] Confirmar que staging esta estavel
- [ ] Notificar time no Slack sobre inicio do release
- [ ] Confirmar disponibilidade do time para suporte

#### 2. Publicacao do Package

- [ ] Criar release branch (se aplicavel)
- [ ] Bump version no `package.json`
- [ ] Gerar changelog automatico
- [ ] Criar tag no Git
- [ ] Publicar no npm registry
- [ ] Verificar que o package esta acessivel no npm
- [ ] Testar instalacao em projeto limpo

#### 3. Publicacao de Assets

- [ ] Publicar Figma library atualizada
- [ ] Publicar Storybook atualizado
- [ ] Publicar documentacao atualizada
- [ ] Atualizar CDN (se aplicavel)

#### 4. Verificacao Pos-Publicacao

- [ ] Instalar nova versao em projeto piloto
- [ ] Verificar que todos os componentes renderizam corretamente
- [ ] Executar smoke tests basicos
- [ ] Verificar que codemods funcionam corretamente
- [ ] Verificar que compatibility layer funciona (se aplicavel)

#### 5. Comunicacao

- [ ] Publicar release notes no GitHub
- [ ] Enviar anuncio no Slack
- [ ] Enviar email para stakeholders
- [ ] Atualizar status page / roadmap publico

## Pos-Release Checklist

### Dia 1 (D+0)

- [ ] Monitorar canal do Slack para duvidas e problemas
- [ ] Triagiar issues reportados
- [ ] Documentar problemas conhecidos (se houver)

### Semana 1 (D+1 a D+7)

- [ ] Conduzir office hours de suporte
- [ ] Acompanhar adocao (metricas de download/install)
- [ ] Resolver bugs criticos com hotfix se necessario
- [ ] Coletar feedback dos early adopters
- [ ] Atualizar FAQ com novas perguntas frequentes

### Semana 2-4 (D+8 a D+30)

- [ ] Acompanhar metricas de adocao por produto
- [ ] Conduzir retrospectiva do release
- [ ] Planejar deprecation da versao anterior
- [ ] Documentar lessons learned


---
