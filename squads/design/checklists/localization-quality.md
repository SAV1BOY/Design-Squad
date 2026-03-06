# Localization Quality Checklist

## Metadata
- **Squad:** Design
- **Domain:** Internationalization & Localization
- **Version:** 1.0.0
- **Owner Agent:** Localization Agent

## Objective
Garantir que o design do produto esteja preparado para suportar multiplos idiomas e contextos culturais sem comprometer a experiencia do usuario.
Um design localization-ready evita redesigns caros e experiencias quebradas em mercados internacionais.

## When to Apply
- Ao projetar interfaces que serao traduzidas para outros idiomas.
- Ao expandir o produto para novos mercados ou regioes.
- Ao revisar a prontidao do design para internacionalizacao.

## Criteria
- [ ] O layout acomoda expansao de texto de ate 30-40% para traducoes mais longas
- [ ] Os containers de texto sao flexiveis e nao dependem de tamanho fixo
- [ ] O design considera idiomas RTL (right-to-left) quando aplicavel, com mirroring de layout
- [ ] Os icones e ilustracoes sao culturalmente neutros ou adaptaveis por regiao
- [ ] As cores nao possuem significados culturais conflitantes nos mercados-alvo
- [ ] Os formatos de data, hora, moeda e numeros sao localizaveis (nao hard-coded)
- [ ] Os formularios suportam formatos de endereco, telefone e nome de diferentes paises
- [ ] A tipografia selecionada suporta os character sets necessarios (Latin, Cyrillic, CJK)
- [ ] O conteudo evita expressoes idiomaticas dificeis de traduzir
- [ ] Os plurais e genero gramatical sao tratados dinamicamente, nao com concatenacao
- [ ] As imagens com texto embedded possuem versao localizavel ou alternativa
- [ ] Os sort orders e collation consideram regras do idioma local
- [ ] O truncamento de texto funciona adequadamente em todos os idiomas suportados
- [ ] Existe um processo definido para revisao de traducoes em contexto visual
- [ ] Os legal disclaimers e termos sao adaptaveis por jurisdicao

## Severity Guide

### Critico
- Layout quebrado com traducoes mais longas que o idioma original.
- Ausencia de suporte a RTL quando ha mercados arabes ou hebraicos planejados.
- Fontes que nao suportam character sets dos idiomas-alvo.

### Major
- Formatos de data e moeda hard-coded no design.
- Icones culturalmente ofensivos ou confusos em mercados-alvo.
- Concatenacao de strings impedindo traducao adequada.

### Minor
- Processo de revisao de traducoes em contexto nao formalizado.
- Sort order nao adaptado mas funcional com fallback.
- Expressoes idiomaticas em textos secundarios.

## Cross-References
- [Content Design Quality](content-design-quality.md)
- [Typography Quality](typography-quality.md)
- [Responsive Breakpoints Quality](responsive-breakpoints-quality.md)
- [Cross-Platform Quality](cross-platform-quality.md)
- [Accessibility Quality](accessibility-quality.md)
