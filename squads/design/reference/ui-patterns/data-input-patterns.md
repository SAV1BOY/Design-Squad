# Data Input Patterns



## Metadata

- **Categoria:** UI Patterns, Form Components, Interaction
- **Relevancia para o Squad:** Alta — componentes de input sao os mais usados em interfaces
- **Ultima revisao:** 2026-03-06



## Summary

Data input patterns definem como cada tipo de dado e coletado do usuario — qual componente usar, como se comporta, como valida. A escolha errada de input component cria friccao desnecessaria; a escolha certa torna a entrada de dados intuitiva e eficiente.





## Key Concepts


### 1. Text Input Variants

Single-line (nome, email), multi-line/textarea (comentarios, descricoes), password (com show/hide toggle), search (com icone e clear button). Helper text abaixo para instrucoes contextuais. Character count para campos com limite.


### 2. Selection Inputs

Radio buttons: escolha exclusiva com poucas opcoes visiveis (2-5). Checkbox: multipla selecao, independentes entre si. Toggle/Switch: on/off binario com efeito imediato. Dropdown/Select: escolha exclusiva com muitas opcoes (>5). Combobox: dropdown com busca (>15 opcoes).


### 3. Date and Time Inputs

Date picker: calendario visual para selecao de data unica ou range. Time picker: para selecao de horario. Permitir input manual (digitacao) como alternativa ao picker visual. Formatos de data devem respeitar locale do usuario (DD/MM/YYYY para BR).


### 4. Numeric and Quantity Inputs

Stepper: incrementar/decrementar com botoes (+/-). Adequado para quantidades pequenas (1-10). Slider: selecao em range continuo, com valor visivel. Range slider: selecao de min-max. Input numerico: para valores exatos, com teclado numerico em mobile.


### 5. File Upload

Drag-and-drop zone + click-to-browse. Mostrar: tipos aceitos, tamanho maximo, preview do arquivo (imagem/pdf). Progress bar durante upload. Permitir remocao apos upload. Multiplos arquivos: lista com status individual.



## Application to Design Squad

- **Input component matrix:** Documentar no design system qual componente usar para cada tipo de dado. Tabela: tipo de dado > componente > comportamento > validacao.
- **Mobile keyboard optimization:** Para cada tipo de input, especificar o input type HTML que ativa o teclado mobile adequado.
- **Consistent states:** Todos os input components devem ter os mesmos states visuais: default, hover, focus, filled, error, disabled, read-only. Padronizar no design system.
- **Date format localization:** Implementar date inputs que respeitam locale. Para Brasil: DD/MM/YYYY. Nunca forcar formato americano.
- **File upload component robusto:** Investir em componente de file upload no design system com drag-drop, progress, preview e error handling. E reutilizado em muitos contextos.



## Key Takeaways

1. **O tipo de dado determina o componente.** Radio para poucos exclusivos, checkbox para multiplos, dropdown para muitos exclusivos, combobox para muitissimos.

2. **Oferecer input manual como alternativa.** Date pickers, sliders e steppers devem permitir digitacao direta como alternativa.

3. **States consistentes sao inegociaveis.** Todo input component tem os mesmos 7 states. Padronize no design system.

4. **Mobile keyboard e decision de design.** Especifique input types que ativam o teclado correto — numerico para telefone, email para email.

5. **Locale matters.** Formatos de data, moeda e numero devem respeitar o locale do usuario.



## Cross-References

- [Forms and Validation Patterns](forms-and-validation-patterns.md) — formularios completos
- [Web Form Design — Wroblewski](../books/wroblewski-web-form-design.md) — input types e affordances
- [ARIA Authoring Practices](../standards/aria-authoring-practices.md) — acessibilidade de inputs
- [Material Design Notes](../standards/material-design-notes.md) — text field specs
- [Brazil LATAM Design Context](../industries/brazil-latam-design-context.md) — localizacao BR
