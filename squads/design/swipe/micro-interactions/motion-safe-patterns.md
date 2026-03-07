# Motion-Safe Patterns

## Pattern Description

Padroes de animacao que respeitam preferencias de movimento reduzido do usuario. Essencial para inclusao de pessoas com disturbios vestibulares, epilepsia e sensibilidade ao movimento.

## Examples

### Example 1: Stripe — Respectful Transitions
Stripe implementa motion-safe globalmente:
- Todas as animacoes envolvidas em media query
- `prefers-reduced-motion: reduce` → duracoes zeradas
- Alternativa: fade puro (sem translate/scale) para reduced motion
- Animacoes decorativas completamente removidas
- Animacoes funcionais (progress) mantidas mas simplificadas

### Example 2: GOV.UK — Motion-Free by Default
GOV.UK prioriza acessibilidade sobre estetica:
- Sem animacoes decorativas por padrao
- Transicoes minimas: apenas focus outline
- Conteudo nunca depende de animacao para ser compreendido
- Performance excelente em conexoes lentas

### Example 3: Apple — Graceful Degradation
Apple degrada animacoes graciosamente:
- Parallax: removido em reduced motion
- Page transitions: crossfade instantaneo em vez de slide
- Scroll animations: conteudo visivel imediatamente
- Hero animations: imagem estatica em vez de video loop

## Analysis

Motion-safe patterns eficazes:
- **Default seguro**: considere reduced motion como default, nao excecao
- **Funcional vs decorativa**: mantenha animacoes que comunicam estado
- **Media query**: `@media (prefers-reduced-motion: reduce)`
- **Alternativas**: fade em vez de slide, opacity em vez de transform
- **Testes**: valide com reduced motion ativado no OS
- **Documentacao**: guia de motion para contribuidores do DS

```css
/* Padrao recomendado */
.element {
  transition: opacity 200ms ease;
}

@media (prefers-reduced-motion: no-preference) {
  .element {
    transition: opacity 200ms ease, transform 200ms ease;
  }
}
```

## Tags

`reduced-motion`, `a11y`, `animation`, `vestibular`, `inclusive-design`
