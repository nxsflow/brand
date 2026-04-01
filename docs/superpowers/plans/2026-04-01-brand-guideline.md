# NexusFlow Brand Guideline Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Create the NexusFlow brand guideline as a BRAND.md file, design tokens (CSS + JSON), SVG monogram logos for the flagship products, and a Claude Code plugin/skill for easy installation across repos.

**Architecture:** The brand guideline lives in this logos repo as the source of truth. Design tokens are generated alongside it for machine consumption. A Claude Code skill wraps the guideline so any repo can reference brand rules. Logos are hand-crafted SVGs exported to PNGs via CLI tooling.

**Tech Stack:** Markdown, CSS custom properties, JSON, SVG, Claude Code plugin system, sharp (Node.js) or rsvg-convert for PNG export

---

## File Structure

```text
logos/
├── BRAND.md                          # Human/AI-readable brand guideline (source of truth)
├── tokens/
│   ├── colors.css                    # CSS custom properties for all brand colors
│   ├── colors.json                   # JSON color tokens (Tailwind, etc.)
│   └── typography.css                # Font imports and type scale
├── logos/
│   ├── nexflow-it/
│   │   ├── nf-monogram.svg           # nexflow.it "nf" monogram (lime)
│   │   ├── nf-monogram-128.png       # PNG exports
│   │   ├── nf-monogram-256.png
│   │   ├── nf-monogram-512.png
│   │   ├── nf-monogram-1024.png
│   │   ├── nf-favicon-16.png
│   │   ├── nf-favicon-32.png
│   │   ├── nf-favicon-180.png
│   │   └── nf-favicon.ico
│   └── manufakt-io/
│       ├── mf-monogram.svg           # manufakt.io "mf" monogram (graphite)
│       ├── mf-monogram-light.svg     # Light variant for dark backgrounds
│       ├── mf-monogram-128.png
│       ├── mf-monogram-256.png
│       ├── mf-monogram-512.png
│       ├── mf-monogram-1024.png
│       ├── mf-favicon-16.png
│       ├── mf-favicon-32.png
│       ├── mf-favicon-180.png
│       └── mf-favicon.ico
├── scripts/
│   └── export-pngs.sh               # Script to regenerate PNGs from SVGs
└── plugin/
    ├── package.json                  # Claude Code plugin manifest
    └── skills/
        └── nxsflow-brand.md          # Brand guideline skill
```

---

### Task 1: Create BRAND.md

**Files:**
- Create: `BRAND.md`

- [ ] **Step 1: Write BRAND.md**

This is the human/AI-readable brand guideline, the single source of truth. It consolidates all decisions from the design spec into a clean, referenceable document.

```markdown
# NexusFlow Brand Guideline

## Company

- **Legal name:** NexusFlow UG (haftungsbeschränkt)
- **Short name:** NexusFlow
- **Domain:** nxsflow.com
- **Positioning:** Precise tools for technical professionals

## Brand Hierarchy

| Brand | Type | Domain | Accent Color |
|-------|------|--------|-------------|
| NexusFlow | Parent | nxsflow.com | Lime #B9FF66 |
| nexflow.it | Flagship | nexflow.it | Lime #B9FF66 |
| manufakt.io | Flagship | manufakt.io | Graphite #1C1C1C + Warm Mist #FAF9F7 |
| NexusFlow BP | Product | bp.nxsflow.com | Amber #F59E0B |
| Amplify Overtone | Open source | overtone.nxsflow.com | Lavender #A78BFA |

nexflow.it is the core product. The parent brand shares its lime accent to reinforce this.

## Colors

### Shared Neutrals
- Graphite (text): `#1C1C1C`
- Secondary text: `#6B6B6B`
- Borders: `#E5E5E0`
- White: `#FFFFFF`

### nexflow.it
- Primary: `#B9FF66` (lime)
- Primary dark: `#84CC16` (deep lime)
- Light tint: `#F5FFE6` (lime wash)
- Background: `#FFFFFF`

### manufakt.io
- Primary: `#1C1C1C` (graphite)
- Background: `#FAF9F7` (warm mist)
- Two colors only. No accent. The user's creation is the color.

### NexusFlow BP
- Accent: `#F59E0B` (amber)
- Background: `#FFFFFF`

### Amplify Overtone
- Accent: `#A78BFA` (lavender)
- Background: `#FFFFFF`

### NexusFlow (parent)
- Accent: `#B9FF66` (lime, shared with nexflow.it)
- Background: `#FFFFFF`

## Typography

### Fonts
- **Headings (all brands):** Merriweather — weights 700, 900
- **Body (default):** Merriweather Sans — weights 300, 400, 700
- **Body (nexflow.it):** Nunito — weights 400, 600, 700
- **Monospace (manufakt.io):** JetBrains Mono

### Type Scales

**Default (parent, manufakt.io, Overtone) — 1.25 ratio:**
xs: 12px, sm: 14px, base: 16px, lg: 20px, xl: 25px, 2xl: 31px, 3xl: 39px

**nexflow.it — 1.333 ratio:**
xs: 13px, sm: 15px, base: 18px, lg: 24px, xl: 32px, 2xl: 42px, 3xl: 56px

**NexusFlow BP — 1.2 ratio:**
xs: 11px, sm: 13px, base: 15px, lg: 18px, xl: 22px, 2xl: 26px, 3xl: 31px

## Logo System

### Flagship Monograms
- **nexflow.it:** "nf" merged letterform in lime (#B9FF66). Works on dark and light backgrounds.
- **manufakt.io:** "mf" merged letterform in graphite (#1C1C1C). Light variant (#FAF9F7) for dark backgrounds.

### Other Brands
- **NexusFlow:** Merriweather Bold wordmark + connection-node icon. Lime accent.
- **NexusFlow BP:** Wordmark ("NexusFlow" bold, "BP" light) + icon. Amber accent.
- **Amplify Overtone:** Wordmark ("Amplify" bold, "Overtone" gradient) + wave icon. Lavender accent.

### Logo Rules
- Clear space: 1x monogram/icon height on all sides
- Minimum size: 24px digital, 10mm print
- Variants: full color, monochrome (#1C1C1C), reversed
- Never stretch, rotate, or recolor outside palette

## Design Language

### nexflow.it — "Pen on paper"
- Hand-drawn SVG lines for borders, dividers, buttons
- Intentionally imperfect lines — slightly wobbly, never straight
- Subtle rotation on tags/badges (0.3–0.5deg)
- Rounded corners matching Nunito's character
- Generous spacing
- Communicates: in progress, learning, personal, human

### manufakt.io — "Precision instrument"
- Strict two-color system only
- Generous whitespace — tool stays out of the way
- Sharp, clean lines
- Monospace for code contexts
- Minimal UI — every element earns its place
- Communicates: clarity, craftsmanship, space for your creation

### NexusFlow BP — "Builder's momentum"
- Amber for progress indicators, CTAs, highlights
- Compact type scale — information-dense
- Card-based Lean Canvas layouts
- Communicates: progressive, motivated, building something special

### Amplify Overtone — "Open workshop"
- Lavender with gradient treatments
- Documentation-style layouts
- Communicates: collaboration, community, inviting contributions

### NexusFlow (parent) — "The foundation"
- Light background, lime accent used sparingly
- Clean editorial layout
- Communicates: precision, craft, the common thread

## Tone of Voice

### NexusFlow (parent)
Confident, clear, understated. "We build precise tools" — no hype, no buzzwords.

### nexflow.it
Warm, personal, conversational. First person ("I've prepared your briefing"). Playful, light humor allowed. Never patronizing.

### manufakt.io
Direct, concise, technical. Respects user expertise. Status-oriented ("Authentication complete. Starting API routes."). Never "vibe coding" — this is craftsmanship.

### NexusFlow BP
Encouraging, action-oriented. "Your idea deserves a plan." Progressive, optimistic. Speaks to builders.

### Amplify Overtone
Inclusive, technical, community-minded. "We" not "I." Documentation voice. Welcoming to all levels.
```

- [ ] **Step 2: Commit**

```bash
git add BRAND.md
git commit -m "docs: add NexusFlow brand guideline"
```

---

### Task 2: Create Color Tokens

**Files:**
- Create: `tokens/colors.css`
- Create: `tokens/colors.json`

- [ ] **Step 1: Create tokens directory**

```bash
mkdir -p tokens
```

- [ ] **Step 2: Write tokens/colors.css**

```css
/* NexusFlow Brand Colors — generated from BRAND.md */
/* Usage: import this file and use var(--nxs-*) custom properties */

:root {
  /* Shared Neutrals */
  --nxs-graphite: #1C1C1C;
  --nxs-gray: #6B6B6B;
  --nxs-border: #E5E5E0;
  --nxs-white: #FFFFFF;

  /* nexflow.it */
  --nxs-nexflow-primary: #B9FF66;
  --nxs-nexflow-primary-dark: #84CC16;
  --nxs-nexflow-tint: #F5FFE6;
  --nxs-nexflow-bg: #FFFFFF;

  /* manufakt.io */
  --nxs-manufakt-primary: #1C1C1C;
  --nxs-manufakt-bg: #FAF9F7;

  /* NexusFlow BP */
  --nxs-bp-accent: #F59E0B;
  --nxs-bp-bg: #FFFFFF;

  /* Amplify Overtone */
  --nxs-overtone-accent: #A78BFA;
  --nxs-overtone-bg: #FFFFFF;

  /* NexusFlow Parent */
  --nxs-parent-accent: #B9FF66;
  --nxs-parent-bg: #FFFFFF;
}
```

- [ ] **Step 3: Write tokens/colors.json**

```json
{
  "shared": {
    "graphite": "#1C1C1C",
    "gray": "#6B6B6B",
    "border": "#E5E5E0",
    "white": "#FFFFFF"
  },
  "nexflow": {
    "primary": "#B9FF66",
    "primaryDark": "#84CC16",
    "tint": "#F5FFE6",
    "background": "#FFFFFF"
  },
  "manufakt": {
    "primary": "#1C1C1C",
    "background": "#FAF9F7"
  },
  "bp": {
    "accent": "#F59E0B",
    "background": "#FFFFFF"
  },
  "overtone": {
    "accent": "#A78BFA",
    "background": "#FFFFFF"
  },
  "parent": {
    "accent": "#B9FF66",
    "background": "#FFFFFF"
  }
}
```

- [ ] **Step 4: Commit**

```bash
git add tokens/
git commit -m "feat: add color design tokens (CSS + JSON)"
```

---

### Task 3: Create Typography Tokens

**Files:**
- Create: `tokens/typography.css`

- [ ] **Step 1: Write tokens/typography.css**

```css
/* NexusFlow Typography — generated from BRAND.md */
/* Usage: import this file for font loading and type scale custom properties */

/* Google Fonts imports */
@import url('https://fonts.googleapis.com/css2?family=Merriweather:wght@700;900&family=Merriweather+Sans:wght@300;400;700&family=Nunito:wght@400;600;700&family=JetBrains+Mono:wght@400;700&display=swap');

:root {
  /* Font families */
  --nxs-font-heading: 'Merriweather', Georgia, serif;
  --nxs-font-body: 'Merriweather Sans', system-ui, sans-serif;
  --nxs-font-body-nexflow: 'Nunito', system-ui, sans-serif;
  --nxs-font-mono: 'JetBrains Mono', monospace;

  /* Default type scale (1.25 — parent, manufakt.io, Overtone) */
  --nxs-text-xs: 12px;
  --nxs-text-sm: 14px;
  --nxs-text-base: 16px;
  --nxs-text-lg: 20px;
  --nxs-text-xl: 25px;
  --nxs-text-2xl: 31px;
  --nxs-text-3xl: 39px;
}

/* nexflow.it type scale override (1.333) */
[data-brand="nexflow"] {
  --nxs-text-xs: 13px;
  --nxs-text-sm: 15px;
  --nxs-text-base: 18px;
  --nxs-text-lg: 24px;
  --nxs-text-xl: 32px;
  --nxs-text-2xl: 42px;
  --nxs-text-3xl: 56px;
  --nxs-font-body: 'Nunito', system-ui, sans-serif;
}

/* NexusFlow BP type scale override (1.2) */
[data-brand="bp"] {
  --nxs-text-xs: 11px;
  --nxs-text-sm: 13px;
  --nxs-text-base: 15px;
  --nxs-text-lg: 18px;
  --nxs-text-xl: 22px;
  --nxs-text-2xl: 26px;
  --nxs-text-3xl: 31px;
}
```

- [ ] **Step 2: Commit**

```bash
git add tokens/typography.css
git commit -m "feat: add typography design tokens"
```

---

### Task 4: Create nexflow.it "nf" Monogram SVG

**Files:**
- Create: `logos/nexflow-it/nf-monogram.svg`

- [ ] **Step 1: Create directory**

```bash
mkdir -p logos/nexflow-it
```

- [ ] **Step 2: Create the "nf" monogram SVG**

Design the merged "nf" letterform in SVG. The letters share a vertical stroke where the "n" meets the "f". Use a serif typeface style (matching the screenshot — similar to a Playfair Display or Merriweather Bold aesthetic). The monogram is rendered in lime (#B9FF66).

The SVG should:
- Have a square viewBox (e.g., `0 0 200 200`)
- Contain the merged "nf" letterform centered
- Use `fill="#B9FF66"` for the letterform
- Have no background (transparent)
- Be clean, minimal paths — no unnecessary complexity

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 200 200" width="200" height="200">
  <!-- nf merged monogram — serif letterform, shared vertical stroke -->
  <!-- The "n" and "f" share the right vertical of "n" / left vertical of "f" -->
  <!-- IMPORTANT: This is a placeholder path. The actual SVG paths must be -->
  <!-- hand-crafted or traced from a serif typeface rendering of "nf" with -->
  <!-- the letters merged at the shared vertical stroke. Use a tool like -->
  <!-- Figma, Inkscape, or font-to-SVG conversion to create the final paths. -->
  <!-- The existing screenshot shows the style: bold serif, letters touching -->
  <!-- at the stem, lowercase, compact. -->
  <text x="100" y="145" text-anchor="middle"
        font-family="Merriweather, Georgia, serif"
        font-size="140" font-weight="900"
        fill="#B9FF66" letter-spacing="-20">nf</text>
</svg>
```

> **Note to implementer:** The `<text>` element above is a starting point to get the positioning right. For the final logo, convert this to `<path>` elements using one of these approaches:
> 1. Open in Inkscape → select text → Path > Object to Path → save
> 2. Use Figma: type "nf" in Merriweather Black, flatten to outlines, export SVG
> 3. Use `opentype.js` or `fontkit` in Node.js to convert font glyphs to SVG paths
>
> The paths must be merged so the "n" and "f" share the connecting vertical stroke, exactly like the screenshot reference.

- [ ] **Step 3: Verify the SVG renders correctly**

Open the SVG in a browser:

```bash
open logos/nexflow-it/nf-monogram.svg
```

Verify: lime green "nf" on transparent background, serif style, letters merged at shared stroke.

- [ ] **Step 4: Commit**

```bash
git add logos/nexflow-it/nf-monogram.svg
git commit -m "feat: add nexflow.it nf monogram SVG"
```

---

### Task 5: Create manufakt.io "mf" Monogram SVGs

**Files:**
- Create: `logos/manufakt-io/mf-monogram.svg`
- Create: `logos/manufakt-io/mf-monogram-light.svg`

- [ ] **Step 1: Create directory**

```bash
mkdir -p logos/manufakt-io
```

- [ ] **Step 2: Create the "mf" monogram SVG (dark, for light backgrounds)**

Same technique as the "nf" monogram — merged serif letterform, but in graphite (#1C1C1C).

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 200 200" width="200" height="200">
  <!-- mf merged monogram — serif letterform, shared vertical stroke -->
  <!-- Same approach as nf: convert to paths for final version -->
  <text x="100" y="145" text-anchor="middle"
        font-family="Merriweather, Georgia, serif"
        font-size="140" font-weight="900"
        fill="#1C1C1C" letter-spacing="-20">mf</text>
</svg>
```

> **Note to implementer:** Same conversion process as Task 4. Convert text to paths, merge the shared stroke between "m" and "f".

- [ ] **Step 3: Create the light variant (for dark backgrounds)**

Copy and change fill to warm mist (#FAF9F7):

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 200 200" width="200" height="200">
  <text x="100" y="145" text-anchor="middle"
        font-family="Merriweather, Georgia, serif"
        font-size="140" font-weight="900"
        fill="#FAF9F7" letter-spacing="-20">mf</text>
</svg>
```

- [ ] **Step 4: Verify both SVGs render correctly**

```bash
open logos/manufakt-io/mf-monogram.svg
open logos/manufakt-io/mf-monogram-light.svg
```

Verify: dark "mf" on transparent, light "mf" on transparent. Both serif, merged letterforms.

- [ ] **Step 5: Commit**

```bash
git add logos/manufakt-io/
git commit -m "feat: add manufakt.io mf monogram SVGs (dark + light)"
```

---

### Task 6: Create PNG Export Script

**Files:**
- Create: `scripts/export-pngs.sh`

- [ ] **Step 1: Check if rsvg-convert is available**

```bash
which rsvg-convert || brew install librsvg
```

> Alternative: if you prefer Node.js, use `sharp` instead. The script below uses `rsvg-convert` as it has no dependencies beyond the CLI tool.

- [ ] **Step 2: Write the export script**

```bash
#!/bin/bash
# Export SVG logos to PNG at multiple sizes
# Usage: ./scripts/export-pngs.sh

set -euo pipefail

SIZES=(128 256 512 1024)
FAVICON_SIZES=(16 32 180)

export_svg() {
  local svg_path="$1"
  local output_dir="$(dirname "$svg_path")"
  local basename="$(basename "$svg_path" .svg)"

  echo "Exporting $svg_path..."

  for size in "${SIZES[@]}"; do
    rsvg-convert -w "$size" -h "$size" "$svg_path" > "$output_dir/${basename}-${size}.png"
    echo "  ${basename}-${size}.png"
  done

  for size in "${FAVICON_SIZES[@]}"; do
    rsvg-convert -w "$size" -h "$size" "$svg_path" > "$output_dir/${basename}-favicon-${size}.png"
    echo "  ${basename}-favicon-${size}.png"
  done
}

# Export all monogram SVGs (skip light variants for favicon — they're for dark backgrounds only)
export_svg "logos/nexflow-it/nf-monogram.svg"
export_svg "logos/manufakt-io/mf-monogram.svg"
export_svg "logos/manufakt-io/mf-monogram-light.svg"

echo "Done. PNGs exported."
```

- [ ] **Step 3: Make executable and test**

```bash
chmod +x scripts/export-pngs.sh
./scripts/export-pngs.sh
```

Expected: PNG files created in each logo directory at all specified sizes.

- [ ] **Step 4: Verify a sample PNG**

```bash
file logos/nexflow-it/nf-monogram-256.png
```

Expected: `PNG image data, 256 x 256`

- [ ] **Step 5: Commit**

```bash
git add scripts/ logos/
git commit -m "feat: add PNG export script and generated PNGs"
```

---

### Task 7: Create Favicon ICO Files

**Files:**
- Create: `logos/nexflow-it/nf-favicon.ico`
- Create: `logos/manufakt-io/mf-favicon.ico`

- [ ] **Step 1: Check if ImageMagick is available**

```bash
which convert || brew install imagemagick
```

- [ ] **Step 2: Generate ICO files from the favicon PNGs**

```bash
# nexflow.it favicon
convert logos/nexflow-it/nf-monogram-favicon-16.png \
        logos/nexflow-it/nf-monogram-favicon-32.png \
        logos/nexflow-it/nf-favicon.ico

# manufakt.io favicon
convert logos/manufakt-io/mf-monogram-favicon-16.png \
        logos/manufakt-io/mf-monogram-favicon-32.png \
        logos/manufakt-io/mf-favicon.ico
```

- [ ] **Step 3: Verify ICO files**

```bash
file logos/nexflow-it/nf-favicon.ico
file logos/manufakt-io/mf-favicon.ico
```

Expected: `MS Windows icon resource`

- [ ] **Step 4: Commit**

```bash
git add logos/
git commit -m "feat: add favicon ICO files"
```

---

### Task 8: Create Claude Code Brand Plugin

**Files:**
- Create: `plugin/package.json`
- Create: `plugin/skills/nxsflow-brand.md`

- [ ] **Step 1: Create plugin directory**

```bash
mkdir -p plugin/skills
```

- [ ] **Step 2: Write plugin/package.json**

```json
{
  "name": "nxsflow-brand",
  "version": "1.0.0",
  "description": "NexusFlow brand guideline skill for Claude Code",
  "claude-plugin": true
}
```

- [ ] **Step 3: Write the brand skill**

The skill file should contain the full brand guideline so it's available in context when invoked. Read the content of `BRAND.md` (created in Task 1) and wrap it in the skill frontmatter:

```markdown
---
name: nxsflow-brand
description: NexusFlow brand guideline — colors, typography, tone of voice, logo rules, and per-product design language. Use when building any NexusFlow product or when making design, copy, or UI decisions.
---

[Full contents of BRAND.md inserted here]

## Design Tokens

The brand tokens are available at:
- CSS: `tokens/colors.css` and `tokens/typography.css` in the nxsflow/logos repo
- JSON: `tokens/colors.json` in the nxsflow/logos repo

When building UI components, use the CSS custom properties (e.g., `var(--nxs-nexflow-primary)`) rather than hardcoding hex values.

When configuring Tailwind or other CSS frameworks, import `tokens/colors.json` to keep colors in sync.
```

> **Note to implementer:** Copy the actual BRAND.md content into the skill file between the frontmatter and the "Design Tokens" section. The skill needs to be self-contained — it cannot reference external files at runtime.

- [ ] **Step 4: Commit**

```bash
git add plugin/
git commit -m "feat: add Claude Code brand plugin/skill"
```

- [ ] **Step 5: Document how to install the plugin**

Add installation instructions to the end of BRAND.md:

```markdown
## Using This Guideline

### As a Claude Code Plugin

Install the brand skill in your user or project settings:

#### User-wide (all projects):
Add to `~/.claude/settings.json`:
```json
{
  "plugins": [
    "/path/to/nxsflow/logos/plugin"
  ]
}
```

#### Per-project:
Add to your project's `.claude/settings.json`:
```json
{
  "plugins": [
    "/path/to/nxsflow/logos/plugin"
  ]
}
```

Then invoke with: `/nxsflow-brand`

### As a CLAUDE.md Reference
Add to any product repo's `CLAUDE.md`:
```
## Brand
Follow the NexusFlow brand guideline at /path/to/nxsflow/logos/BRAND.md
```
```

- [ ] **Step 6: Commit**

```bash
git add BRAND.md
git commit -m "docs: add plugin installation instructions to BRAND.md"
```

---

### Task 9: Update .gitignore and Clean Up

**Files:**
- Modify: `.gitignore`

- [ ] **Step 1: Update .gitignore**

Add entries for the superpowers brainstorm directory and any OS artifacts:

```text
.superpowers/
.DS_Store
```

- [ ] **Step 2: Verify repo state**

```bash
git status
```

Ensure no untracked files that shouldn't be committed.

- [ ] **Step 3: Final commit**

```bash
git add .gitignore
git commit -m "chore: update gitignore for superpowers and OS artifacts"
```

---

## Summary

| Task | What | Files |
|------|------|-------|
| 1 | BRAND.md guideline | `BRAND.md` |
| 2 | Color tokens | `tokens/colors.css`, `tokens/colors.json` |
| 3 | Typography tokens | `tokens/typography.css` |
| 4 | nexflow.it "nf" monogram SVG | `logos/nexflow-it/nf-monogram.svg` |
| 5 | manufakt.io "mf" monogram SVGs | `logos/manufakt-io/mf-monogram.svg`, `mf-monogram-light.svg` |
| 6 | PNG export script + exports | `scripts/export-pngs.sh`, PNG files |
| 7 | Favicon ICO files | `.ico` files |
| 8 | Claude Code plugin/skill | `plugin/package.json`, `plugin/skills/nxsflow-brand.md` |
| 9 | Gitignore cleanup | `.gitignore` |
