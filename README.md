# nxsflow Brand Assets

Brand guideline, design tokens, and logos for nxsflow and its products.

## What's in this repo

| Path                      | Description                                      |
| ------------------------- | ------------------------------------------------ |
| `BRAND.md`                | The brand guideline — single source of truth     |
| `copy/`                   | Landing copy decks (EN + DE) per product         |
| `tokens/`                 | Design tokens (CSS custom properties + JSON)     |
| `logos/nexflow-it/`       | nexflow.it "nf" monogram (SVG, PNG, favicon)     |
| `logos/manufakt-io/`      | manufakt.io "mf" monogram (SVG, PNG, favicon)    |
| `logos/nexflow-parent/`   | nxsflow wordmark logotype (SVG, PNG, favicon)    |
| `logos/nexflow-bp/`       | nxsflow BP compass icon (SVG, PNG, favicon)      || `scripts/`                | Logo render script (SVG → PNG/favicon/ico)       |
| `plugin/`                 | Claude Code plugin for brand-aware AI assistance |

## Brand Guideline

See [BRAND.md](BRAND.md) for the full guideline covering **core messaging & positioning**, colors, typography, logo rules, design language, and tone of voice for all nxsflow products. The `## Messaging` section is the source the copy derives from; the distilled landing copy for each product lives in [`copy/`](copy/).

## Products

| Brand                  | Domain               | Accent                                   |
| ---------------------- | -------------------- | ---------------------------------------- |
| **nxsflow** (parent)   | nxsflow.com          | Lime `#B9FF66`                           |
| **nexflow.it**         | nexflow.it           | Lime `#B9FF66`                           |
| **manufakt.io**        | manufakt.io          | Ember Red `#DC2626`                      |
| **nxsflow BP**         | bp.nxsflow.com       | Amber `#F59E0B`                          |
## Using the Design Tokens

**CSS** — import directly:

```css
@import url("path/to/tokens/colors.css");
@import url("path/to/tokens/typography.css");
```

**Tailwind / JS frameworks** — use the JSON:

```js
const colors = require("path/to/tokens/colors.json");
```

## Regenerating Logo Assets

The SVGs in `logos/<family>/svg/` are the source of truth. After editing an SVG
(or adding a new logo that follows the naming convention), rebuild all derived
rasters — PNG (128/256/512/1024), favicon PNGs (16/32/180), and `.ico` bundles:

```bash
scripts/render-logos                 # rebuild every logo family
scripts/render-logos manufakt-io     # rebuild only the given family folder(s)
```

The first run bootstraps a local, git-ignored virtualenv at `scripts/.venv`
(cairosvg + Pillow); it needs Python 3 and a system Cairo library. Favicons are
generated from the simplified variant (`*-sm-*` / `*-simple-*`) when one exists,
otherwise the base SVG.

## Claude Code Plugin

Install the brand skill so Claude follows the guideline in any nxsflow repo.

Add to `~/.claude/settings.json` (user-wide) or `.claude/settings.json` (per-project):

```json
{
  "plugins": ["/path/to/nxsflow/logos/plugin"]
}
```

## License

See [LICENSE.md](LICENSE.md).
