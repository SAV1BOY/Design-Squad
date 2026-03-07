# Address Input Patterns

## Pattern Description

Padroes para campos de endereco em formularios. Endereco e um dos formularios mais complexos — autocomplete, formatacao por pais e validacao sao essenciais.

## Examples

### Example 1: Google Places — Autocomplete Address
Google Places API oferece autocomplete inteligente:
- Campo unico com sugestoes conforme digitacao
- Sugestoes mostram endereco completo formatado
- Selecao preenche automaticamente todos os campos
- Fallback para entrada manual se autocomplete falhar
- Suporte a geolocalizacao para sugestoes proximas

### Example 2: Shopify Checkout — Structured Address
Shopify usa campos estruturados adaptados por pais:
- Campos mudam conforme pais selecionado (CEP no Brasil, ZIP nos EUA)
- Autocomplete de CEP preenche cidade e estado
- Validacao de formato por pais
- Campo de complemento claramente opcional
- Labels adaptados por locale (Bairro, Neighborhood, District)

### Example 3: Amazon — Address Book
Amazon gerencia multiplos enderecos:
- Lista de enderecos salvos com selecao rapida
- "Adicionar novo endereco" como opcao
- Endereco padrao destacado
- Edicao inline sem sair do checkout
- Validacao com sugestao de correcao (USPS, Correios)

## Analysis

Campos de endereco eficazes:
- **Autocomplete**: use APIs de geocoding para reduzir digitacao
- **Adaptativo**: adapte campos por pais (formato, labels, validacao)
- **CEP first**: no Brasil, CEP pode preencher 80% do endereco
- **Opcional vs obrigatorio**: marque "complemento" como opcional explicitamente
- **Validacao**: valide formato mas aceite variacoes regionais
- **Address book**: para ecommerce, salve enderecos para reutilizacao

## Tags

`address`, `forms`, `autocomplete`, `geocoding`, `internationalization`, `checkout`
