# Progressive Profiling Patterns

## Pattern Description

Padroes de coleta progressiva de dados do usuario ao longo do tempo, em vez de solicitar tudo no registro. Reduz friccao no signup e melhora a qualidade dos dados coletados.

## Examples

### Example 1: LinkedIn — Profile Completeness

LinkedIn usa um modelo de completude de perfil:
- Registro minimo: nome, email, senha
- Barra de progresso "Forca do perfil" (Beginner → All-Star)
- Prompts contextuais: "Adicione sua experiencia para aparecer em buscas"
- Cada adicao desbloqueia funcionalidades ou visibilidade

Destaque: motivacao intrinseca (ser encontrado) + extrinseca (barra de progresso).

### Example 2: Spotify — Taste Building

Spotify coleta preferencias musicais progressivamente:
- Signup: apenas credenciais
- Primeiro acesso: "Escolha 3 artistas que voce gosta"
- Semana 1: sugestoes baseadas no que ouviu
- Continuo: Discover Weekly melhora com mais dados

Destaque: a coleta de dados e o proprio valor do produto — quanto mais dados, melhor a experiencia.

### Example 3: Notion — Template Selection

Notion pergunta sobre uso ao longo do tempo:
- Signup: email/Google
- Primeiro acesso: "Para que voce usara o Notion?"
- Depois de 3 usos: "Convide colegas para colaborar"
- Apos 1 semana: survey de NPS contextual

Destaque: cada pergunta e feita no momento de maior relevancia e menor friccao.

## Analysis

Progressive profiling eficaz:
- **Timing**: pergunte quando a informacao e relevante para o usuario
- **Valor reciproco**: mostre o beneficio de fornecer cada dado
- **Nao bloqueante**: nunca force — sempre permita pular
- **Contexto**: pergunte dentro do fluxo natural, nao em pop-ups intrusivos
- **Limites**: maximo 1-2 perguntas por sessao

Impacto mensuravel: signup completion rate +20-40% vs. formularios longos.

## Tags

`progressive-profiling`, `onboarding`, `data-collection`, `friction-reduction`, `personalization`
