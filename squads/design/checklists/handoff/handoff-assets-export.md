# Handoff Assets Export

## Metadata

| Campo       | Valor                          |
|-------------|--------------------------------|
| Squad       | Design                         |
| Domain      | Asset Management               |
| Author      | Design Squad                   |
| Version     | 1.0.0                          |
| Owner       | Handoff Lead                   |

## Objective

Verificar se todos os assets necessarios para implementacao foram exportados
corretamente, nos formatos adequados, com qualidade e nomenclatura padronizadas.
Assets mal exportados causam retrabalho, inconsistencia visual e problemas de
performance.

## When to Apply

- Antes de cada handoff que inclui assets visuais.
- Ao exportar assets para diferentes plataformas (web, iOS, Android).
- Quando desenvolvedores reportam problemas com assets recebidos.
- Em revisoes de processo de exportacao.

## Criteria

- [ ] Icones sao exportados em SVG otimizado com paths limpos e viewBox correto.
- [ ] Imagens raster (fotos, ilustracoes) sao exportadas em resolucoes 1x, 2x e 3x.
- [ ] Formatos de imagem sao adequados: WebP para web, PNG para transparencia, JPEG para fotos.
- [ ] Nomenclatura de arquivos segue convencao padronizada (kebab-case, prefixo por tipo).
- [ ] Assets estao organizados em pastas por categoria (icons, illustrations, images).
- [ ] SVGs nao contem elementos desnecessarios (layers ocultos, metadados de ferramenta).
- [ ] Imagens possuem tamanho otimizado sem perda visual perceptivel (compressao adequada).
- [ ] Favicons e app icons estao exportados em todos os tamanhos necessarios.
- [ ] Assets de dark mode (versoes alternativas) estao incluidos quando necessarios.
- [ ] Fontes customizadas sao fornecidas nos formatos necessarios (woff2, otf, ttf).
- [ ] Existe manifesto ou lista dos assets entregues para conferencia do desenvolvedor.
- [ ] Assets sao acessiveis em repositorio compartilhado (CDN, bucket, Figma exports).
- [ ] O processo de export e reprodutivel e documentado passo a passo.
- [ ] Lottie files ou animacoes exportadas estao testadas e funcionam corretamente.

## Severity Guide

| Nivel    | Descricao                                                                 |
|----------|---------------------------------------------------------------------------|
| Critical | Assets ausentes para fluxos criticos ou SVGs corrompidos.                |
| Major    | Resolucoes incorretas ou formatos inadequados para a plataforma.          |
| Minor    | Nomenclatura inconsistente ou imagens nao otimizadas em tamanho.         |
| Info     | Oportunidade de automatizar export pipeline ou melhorar manifesto.       |

## Cross-References

- `handoff/handoff-specs-and-redlines.md` — Especificacoes de handoff.
- `ui/ui-iconography-quality.md` — Qualidade de iconografia.
- `handoff/handoff-token-sync.md` — Sincronizacao de tokens.
- `design-system/ds-design-code-sync-audit.md` — Sincronizacao design-code.
