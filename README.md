# nxsflow Brand Assets

Brand guideline, design tokens, and logos for nxsflow and its products.

## What's in this repo

| Path                      | Description                                      |
| ------------------------- | ------------------------------------------------ |
| `BRAND.md`                | The brand guideline — single source of truth     |
| `copy/`                   | Landing copy decks (EN + DE) per product, and the long-form brand stories (`*-story.md`: why a brand exists) |
| `tokens/`                 | Design tokens (CSS custom properties + JSON)     |
| `logos/nexflow-it/`       | nexflow.it "nf" monogram + wordmark (SVG, PNG, favicon) |
| `logos/manufakt-io/`      | manufakt.io "mf" monogram + wordmark (SVG, PNG, favicon) |
| `logos/nexflow-parent/`   | nxsflow wordmark logotype (SVG, PNG, favicon)    |
| `logos/nexflow-bp/`       | nxsflow BP compass icon (SVG, PNG, favicon)      |
| `logos/slidesend/`        | slidesend's complete logo kit: symbol, wordmark, one-colour, app icon, favicons, link preview, the mark in context, and its guide (`README.md`) |
| `scripts/`                | Wordmark generators (`build-wordmarks`, `build-slidesend`) + logo render script |
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
| **slidesend**          | nxsflow.com/slidesend | Spotlight `#F04E23`                      |
## Using the Design Tokens

**CSS** — import directly:

```css
@import url("path/to/tokens/colors.css");
@import url("path/to/tokens/typography.css");
```

slidesend has a complete light/dark theme of its own in `tokens/slidesend.css`
(and `tokens/slidesend.json`, with the measured contrast ratios).

**Tailwind / JS frameworks** — use the JSON:

```js
const colors = require("path/to/tokens/colors.json");
```

## Regenerating Logo Assets

The wordmarks (`*-wordmark-*.svg`) are generated from the vendored Merriweather
Black in `scripts/fonts/` (SIL OFL, see `scripts/fonts/OFL.txt`):

```bash
scripts/build-wordmarks              # rewrite every wordmark SVG
scripts/build-wordmarks --check      # fail if a committed wordmark is out of date
```

slidesend is the exception: its symbol, constructed wordmark, one-colour
versions, app icon, favicon and link preview all come from one script.
`logos/slidesend/README.md` is its logo guide.

```bash
scripts/build-slidesend              # rewrite every slidesend logo SVG
scripts/build-slidesend --check      # fail if a committed one is out of date
```

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
otherwise the base SVG. A family with an adaptive `favicon/<prefix>-favicon.svg`
also gets an opaque apple-touch icon, and `social/*.svg` link previews are
rendered to PNG at their own size.

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
