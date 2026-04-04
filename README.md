# nxsflow Brand Assets

Brand guideline, design tokens, and logos for nxsflow and its products.

## What's in this repo

| Path                      | Description                                      |
| ------------------------- | ------------------------------------------------ |
| `BRAND.md`                | The brand guideline — single source of truth     |
| `tokens/`                 | Design tokens (CSS custom properties + JSON)     |
| `logos/nexflow-it/`       | nexflow.it "nf" monogram (SVG, PNG, favicon)     |
| `logos/manufakt-io/`      | manufakt.io "mf" monogram (SVG, PNG, favicon)    |
| `logos/nexflow-parent/`   | nxsflow organic mesh icon (SVG, PNG, favicon)    |
| `logos/nexflow-bp/`       | nxsflow BP compass icon (SVG, PNG, favicon)      |
| `logos/amplify-overtone/` | Amplify Overtone tuning fork (SVG, PNG, favicon) |
| `scripts/`                | PNG and ICO export scripts                       |
| `plugin/`                 | Claude Code plugin for brand-aware AI assistance |

## Brand Guideline

See [BRAND.md](BRAND.md) for the full guideline covering colors, typography, logo rules, design language, and tone of voice for all nxsflow products.

## Products

| Brand                  | Domain               | Accent                                   |
| ---------------------- | -------------------- | ---------------------------------------- |
| **nxsflow** (parent)   | nxsflow.com          | Lime `#B9FF66`                           |
| **nexflow.it**         | nexflow.it           | Lime `#B9FF66`                           |
| **manufakt.io**        | manufakt.io          | Graphite `#1C1C1C` + Warm Mist `#FAF9F7` |
| **nxsflow BP**         | bp.nxsflow.com       | Amber `#F59E0B`                          |
| **Amplify Overtone**   | overtone.nxsflow.com | Lavender `#A78BFA`                       |

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
