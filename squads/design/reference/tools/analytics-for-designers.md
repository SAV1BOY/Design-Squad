# Analytics for Designers



## Metadata

- **Categoria:** Data-Informed Design, UX Metrics
- **Relevancia para o Squad:** Media-Alta — ferramentas para medir impacto de design
- **Ultima revisao:** 2026-03-06



## Summary

Analytics tools permitem que designers baseiem decisoes em dados reais de uso, nao apenas em intuicao ou feedback qualitativo. Este documento mapeia ferramentas e metricas relevantes para designers — nao para product managers ou data analysts, mas especificamente para informar decisoes de design.

O designer nao precisa ser data analyst, mas precisa saber: quais metricas importam para design, como acessar dados basicos, como formular hipoteses testáveis e como interpretar resultados de A/B tests.



## Key Concepts


### 1. Quantitative Tools

Google Analytics 4: pageviews, user flows, conversion funnels. Mixpanel/Amplitude: event-based analytics, cohort analysis, retention curves. Hotjar/FullStory: session recordings, heatmaps, scroll maps. Cada ferramenta responde perguntas diferentes — GA4 para "o que," Mixpanel para "quem e quando," Hotjar para "como."


### 2. UX Metrics That Matter for Designers

Task success rate (% de usuarios que completam a tarefa). Time on task (quanto tempo leva). Error rate (% de erros por tarefa). Abandonment rate (% que desiste no meio). SUS score (System Usability Scale). NPS (Net Promoter Score). CSAT (Customer Satisfaction Score).


### 3. Session Recording Analysis

Session recordings mostram exatamente como usuarios interagem — onde clicam, onde hesitam, onde se confundem. Analise qualitativa de recordings complementa dados quantitativos. Patterns identificados em 5-10 recordings geralmente representam padroes mais amplos.


### 4. A/B Testing for Design

Ferramentas como Optimizely, VWO e LaunchDarkly permitem testar variacoes de design com usuarios reais. Para designers: formular hipotese (variacao B vai aumentar conversao porque...), definir metrica primaria, esperar significancia estatistica, interpretar resultado.


### 5. Heatmaps and Click Maps

Heatmaps mostram onde usuarios olham e clicam. Click maps revelam elementos clicados que nao sao links e links que nao sao clicados. Scroll maps mostram onde usuarios param de scrollar. Essas ferramentas revelam problemas de affordance e hierarquia visual.



## Application to Design Squad

- **Dashboard de metricas de UX:** Criar dashboard compartilhado com metricas de UX (task success, error rate, NPS) atualizado mensalmente. Revisar em reuniao mensal do squad.
- **Session recording review:** Mensalmente, cada designer assiste 5-10 session recordings dos fluxos que projetou. Documentar padroes observados e oportunidades de melhoria.
- **Hypothesis-driven A/B tests:** Para mudancas significativas de UI, formular hipotese e conduzir A/B test. Documentar resultado e aprendizado independente do outcome.
- **Heatmap audit trimestral:** Para paginas criticas (landing, pricing, checkout), analisar heatmaps trimestralmente. Identificar onde usuarios clicam sem resultado e onde nao clicam onde deveriam.
- **Pre/post measurement:** Para todo redesign significativo, medir metricas antes e depois. Documentar impacto quantitativo do design.



## Key Takeaways

1. **Designers nao precisam ser data analysts — precisam ser data-literate.** Entender metricas basicas e formular hipoteses e suficiente.

2. **Session recordings sao a proxima melhor coisa apos usability testing.** Observar uso real revela problemas que dados quantitativos escondem.

3. **A/B testing valida, nao substitui design thinking.** Teste opcoes informadas por pesquisa, nao opcoes aleatorias.

4. **Meca antes e depois de todo redesign.** Sem baseline, nao ha como demonstrar impacto.

5. **Heatmaps revelam gaps de affordance.** Onde usuarios clicam sem resultado sinaliza affordance percebida sem funcionalidade real.



## Cross-References

- [Lean UX — Gothelf](../books/gothelf-lean-ux.md) — outcomes over outputs
- [Spool Articles Index](../books/spool-articles-index.md) — ROI de UX
- [Articulating Design Decisions — Greever](../books/greever-articulating-design-decisions.md) — comunicar valor com dados
- [Just Enough Research — Hall](../books/hall-just-enough-research.md) — pesquisa quantitativa
- [Research Tools](research-tools.md) — ferramentas complementares
