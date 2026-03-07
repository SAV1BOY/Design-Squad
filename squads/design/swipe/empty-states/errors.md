# Error Empty State Patterns

## Pattern Description

Padroes para estados de erro que substituem conteudo esperado — quando dados nao puderam ser carregados ou uma operacao falhou.

## Examples

### Example 1: Slack — Connection Error
Slack trata desconexao com leveza:
- Ilustracao tematica (nuvem desconectada)
- "Estamos tendo problemas para conectar"
- Indicador de tentativas automaticas de reconexao
- Botao manual "Tentar novamente"
- Mensagens offline preservadas para envio posterior

### Example 2: GitHub — 500 Error Page
GitHub usa humor e utilidade no erro 500:
- Ilustracao do Octocat tematica
- "This is not the web page you are looking for"
- Status da plataforma: link para status.github.com
- Sugestao de tentar novamente em alguns minutos
- Link para suporte se o problema persistir

### Example 3: Linear — Partial Load Error
Linear trata erros parciais sem quebrar a pagina:
- Componente que falhou mostra erro inline
- Resto da pagina funciona normalmente
- Botao "Retry" especifico para o componente
- Log do erro visivel para report de bug

## Analysis

Error empty states eficazes:
- **Honestidade**: admita o problema sem culpar o usuario
- **Especificidade**: diferencie erro de rede, servidor e permissao
- **Recuperacao**: sempre ofereca acao (retry, voltar, contato)
- **Graceful degradation**: mostre o maximo possivel, erre parcialmente
- **Tom**: amigavel sem minimizar a frustacao do usuario

## Tags

`error-states`, `empty-states`, `error-handling`, `graceful-degradation`, `retry`
