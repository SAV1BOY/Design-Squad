# Marketplace Design Playbook



## Metadata

- **Categoria:** Industry Playbook, Marketplace, Two-Sided Platform
- **Relevancia para o Squad:** Media — padroes para plataformas de dois lados
- **Ultima revisao:** 2026-03-06



## Summary

Marketplaces sao plataformas de dois lados que conectam oferta (sellers/providers) e demanda (buyers/consumers). O desafio de design e servir dois publicos com necessidades diferentes na mesma plataforma — buyers querem encontrar e comparar; sellers querem vender e gerenciar. O sucesso depende de resolver o "chicken-and-egg problem" e manter ambos os lados engajados.



## Key Concepts


### 1. Two-Sided Experience Design

Buyers: search/browse optimizado, comparação facilitada, trust signals (reviews, verificacoes), checkout simplificado. Sellers: listing creation intuitivo, dashboard de performance, ferramentas de pricing, comunicacao com buyers. Cada lado tem jornada e metricas proprias.


### 2. Trust and Review Systems

Em marketplaces, trust entre estranhos e critica. Review systems bilaterais (buyer avalia seller e vice-versa), verificacoes de identidade, garantias da plataforma, dispute resolution. Design de review: facilitar avaliacoes honestas, mitigar review bombing, mostrar patterns (nao apenas media).


### 3. Search and Discovery

Marketplace search e mais complexo que e-commerce — inclui geolocation, availability, pricing variation, seller attributes. Faceted filtering e essential. Sort by: relevance, price, rating, distance. Map view para servicos locais. Recommendations para discovery.


### 4. Listing Creation Flow

Sellers precisam criar listings atraentes com minimo esforco: templates por categoria, auto-fill quando possivel, image guidelines e quality check, pricing suggestions baseadas em mercado, preview antes de publicar.


### 5. Matching and Booking

Para service marketplaces: matching algorithm que conecta buyer ao provider certo. Booking flow: disponibilidade em real-time, confirmacao instantanea ou request-based, pagamento seguro (escrow), comunicacao in-platform.



## Application to Design Squad

- **Dual persona research:** Se o produto e marketplace, manter personas separadas para cada lado. Pesquisar ambos separadamente e projetar jornadas distintas.
- **Review system design:** Projetar sistema de reviews que incentiva avaliacoes honestas (reminder pos-transacao, rating rapido), desincentiva manipulacao (detecção de anomalias) e mostra informacao util (not just average).
- **Seller tools investment:** Seller experience e frequentemente negligenciada. Dashboard de performance, analytics de listing e ferramentas de otimizacao retêm sellers — e sellers retidos mantem buyers.
- **Search quality metrics:** Medir search quality: click-through rate em resultados, conversion rate pos-search, zero results rate. Investir em search quality e investir em GMV.
- **Trust building progressivo:** Trust se constrói incrementalmente — verificacao basica no cadastro, badges apos primeiras transacoes bem-sucedidas, status elevated apos historico consistente.



## Key Takeaways

1. **Dois lados = duas experiencias.** Buyers e sellers tem necessidades, jornadas e metricas diferentes.

2. **Trust e o produto principal do marketplace.** Sem trust entre estranhos, nao ha transacao.

3. **Seller experience retém supply.** Marketplace sem sellers bons nao atrai buyers. Invista em seller tools.

4. **Search quality = GMV.** Se o buyer nao encontra, nao compra. Search e o feature de maior impacto em revenue.

5. **Reviews sao infraestrutura de trust.** Investir em review quality, nao apenas review quantity.



## Cross-References

- [Search and Filter Patterns](../ui-patterns/search-and-filter-patterns.md) — discovery
- [Trust and Credibility Signals](../psychology/trust-and-credibility-signals.md) — trust building
- [Ecommerce Design Playbook](ecommerce-design-playbook.md) — buyer side patterns
- [Dashboards and Tables Patterns](../ui-patterns/dashboards-and-tables-patterns.md) — seller dashboard
- [Brazil LATAM Design Context](brazil-latam-design-context.md) — marketplaces BR
