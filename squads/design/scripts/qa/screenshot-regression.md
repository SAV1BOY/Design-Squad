# Screenshot Regression

## Title
Script de teste de regressão visual via comparação de screenshots.

## Purpose

Detectar mudanças visuais não intencionais na interface comparando screenshots da
versão atual com uma baseline aprovada. Cada pixel de diferença é identificado e
reportado, permitindo que o time avalie se a mudança é intencional ou regressão.

Visual regression testing é a rede de segurança do design system — garante que
mudanças em componentes compartilhados não quebrem telas que os consomem.

## Prerequisites

- **Node.js** >= 18.0
- **Playwright** >= 1.40 com screenshot comparison built-in
- **Percy** ou **Chromatic** (opcional — serviço de visual testing)
- **Baseline screenshots** aprovadas (geradas na primeira execução)
- **Produto rodando** em staging

Dependências:
```bash
npm install @playwright/test
npx playwright install --with-deps chromium firefox webkit
```

## Steps

### 1. Configurar test suite

```bash
# Criar configuração de visual regression
cat > playwright.visual.config.ts << 'EOF'
import { defineConfig } from '@playwright/test';
export default defineConfig({
  testDir: './visual-tests',
  snapshotDir: './visual-tests/snapshots',
  updateSnapshots: process.env.UPDATE_SNAPSHOTS === 'true' ? 'all' : 'none',
  expect: {
    toHaveScreenshot: {
      maxDiffPixelRatio: 0.01,
      threshold: 0.2,
      animations: 'disabled',
    },
  },
  projects: [
    { name: 'desktop', use: { viewport: { width: 1440, height: 900 } } },
    { name: 'mobile', use: { viewport: { width: 375, height: 812 } } },
  ],
});
EOF
```

### 2. Criar testes visuais

```bash
# Testes são definidos por página/componente
cat > visual-tests/pages.spec.ts << 'EOF'
import { test, expect } from '@playwright/test';

const pages = [
  { name: 'home', url: '/' },
  { name: 'login', url: '/login' },
  { name: 'dashboard', url: '/dashboard' },
  { name: 'checkout', url: '/checkout/cart' },
];

for (const page of pages) {
  test(`Visual regression - ${page.name}`, async ({ page: p }) => {
    await p.goto(page.url);
    await p.waitForLoadState('networkidle');
    await expect(p).toHaveScreenshot(`${page.name}.png`);
  });
}
EOF
```

### 3. Gerar baseline (primeira vez)

```bash
# Gerar screenshots de referência
UPDATE_SNAPSHOTS=true npx playwright test --config playwright.visual.config.ts

# Revisar e aprovar baseline
# Screenshots são salvas em visual-tests/snapshots/
```

### 4. Executar testes de regressão

```bash
# Comparar estado atual com baseline
npx playwright test --config playwright.visual.config.ts

# Output: PASS/FAIL por screenshot
# Diffs salvos em test-results/ quando falha
```

### 5. Analisar diffs

```bash
# Gerar relatório visual de diffs
node scripts/generate-visual-diff-report.js \
  --results-dir test-results/ \
  --output visual-reports/regression-$(date +%Y%m%d).html

# O relatório HTML mostra side-by-side:
# - Baseline (esperado)
# - Atual (capturado)
# - Diff (pixels diferentes em vermelho)
```

### 6. Atualizar baseline (quando mudança é intencional)

```bash
# Após confirmar que mudança é intencional:
UPDATE_SNAPSHOTS=true npx playwright test \
  --config playwright.visual.config.ts \
  --grep "nome-do-teste-que-mudou"

# Commit da nova baseline
git add visual-tests/snapshots/
git commit -m "chore(visual): update baseline for [mudança]"
```

## Expected Output

```
Running 20 tests using 4 workers

  PASS  home-desktop.png (0.02% diff)
  PASS  home-mobile.png (0.00% diff)
  FAIL  login-desktop.png (3.47% diff)
  PASS  login-mobile.png (0.01% diff)
  FAIL  dashboard-desktop.png (1.23% diff)
  ...

  18 passed, 2 failed

  Diff images saved to:
  - test-results/login-desktop-diff.png
  - test-results/dashboard-desktop-diff.png
```

## Automation Notes

- **Frequência:** A cada PR que toca CSS, componentes ou layouts
- **CI/CD:** GitHub Actions com Playwright — roda em PRs automaticamente
- **Threshold:** maxDiffPixelRatio de 0.01 (1%) para tolerar anti-aliasing
- **Paralelismo:** Usar sharding para rodar testes em paralelo (4 workers)
- **Fonts:** Instalar fontes no CI para evitar diffs por font rendering
- **Dynamic content:** Mascarar áreas com conteúdo dinâmico (timestamps, avatars)
- **Approval flow:** Diffs são reviewados pelo designer antes de aprovar atualização
