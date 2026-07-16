# nxsflow Brand Guideline

## Company

- **Legal name:** NexusFlow UG (haftungsbeschränkt)
- **Brand name:** nxsflow
- **Domain:** nxsflow.com
- **Positioning:** Precise tools for technical professionals

## Brand Name

The brand name is **nxsflow**, always lowercase. The legal company name remains NexusFlow UG (haftungsbeschränkt) for legal and contractual contexts only — everywhere else, use nxsflow.

### The F-highlight

When the nxsflow logotype is displayed, the letter "F" may be set in the brand lime (`#B9FF66` on dark backgrounds, `#84CC16` on light backgrounds) to visually connect the parent brand to its products. The "F" is the shared letter across nxsflow, nexflow.it, and manufakt.io — highlighting it reinforces the "flow" concept that runs through the brand family. This treatment is optional and should only be used where legibility is maintained.

## Brand Hierarchy

| Brand            | Type        | Domain               | Accent Color                         |
| ---------------- | ----------- | -------------------- | ------------------------------------ |
| nxsflow          | Parent      | nxsflow.com          | Lime #B9FF66                         |
| nexflow.it       | Flagship    | nexflow.it           | Lime #B9FF66                         |
| manufakt.io      | Flagship    | manufakt.io          | Ember Red #DC2626                    |
| nxsflow BP       | Product     | bp.nxsflow.com       | Amber #F59E0B                        |

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

- Accent: `#DC2626` (ember red)
- Accent dark: `#B91C1C` (deep ember) — hover, pressed
- Light tint: `#FEF2F2` (ember wash)
- Gradient: `linear-gradient(135deg, #DC2626, #EA580C)` (ember → flame)
- Background: `#FFFFFF` (light), full dark mode supported
- Text: `#1C1C1C` (graphite)

### nxsflow BP

- Accent: `#F59E0B` (amber)
- Background: `#FFFFFF`

### nxsflow (parent)

- Accent: `#B9FF66` (lime, shared with nexflow.it)
- Background: `#FFFFFF`

## Typography

### Fonts

- **Headings (all brands):** Merriweather — weights 700, 900
- **Body (default):** Merriweather Sans — 300 (default), 400 (emphasis), 700 (strong emphasis / H3–H4 subheadings)
- **Body (nexflow.it):** Nunito — weights 400, 600, 700
- **Monospace (manufakt.io):** JetBrains Mono

**Merriweather Sans weight usage:** 300 is the default for body copy — Merriweather Sans runs heavy, so the light weight keeps running text calm. Use 400 for emphasis (lead paragraphs, callouts) and 700 for strong emphasis or H3/H4-level subheadings.

### Type Scales

**Default (parent, manufakt.io) — 1.25 ratio:**
xs: 12px, sm: 14px, base: 16px, lg: 20px, xl: 25px, 2xl: 31px, 3xl: 39px

**nexflow.it — 1.333 ratio:**
xs: 13px, sm: 15px, base: 18px, lg: 24px, xl: 32px, 2xl: 42px, 3xl: 56px

**nxsflow BP — 1.2 ratio:**
xs: 11px, sm: 13px, base: 15px, lg: 18px, xl: 22px, 2xl: 26px, 3xl: 31px

## Logo System

### Flagship Monograms

- **nexflow.it:** "nf" merged letterform in lime (#B9FF66). Works on dark and light backgrounds.
- **manufakt.io:** "mf" merged letterform — the **m** in graphite (#1C1C1C), the **f** highlighted in ember red (#DC2626), sharing a single central stem (the same letter-joining play as the nexflow.it monogram). Light variant (m and strokes in #FAF9F7) for dark backgrounds.

### Other Brands

- **nxsflow:** Organic mesh icon — asymmetric nodes connected by hand-drawn curves. Lime (#B9FF66) fills, graphite outlines. Full variant (5 nodes) for wordmark pairing, simplified variant (3 nodes) for favicons.
- **nxsflow BP:** Hand-drawn compass icon — wobbly ring with draft stroke underneath, north needle solid amber (#F59E0B), south needle faded outline. Single design for all sizes.

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

### manufakt.io — "The forge"

- Ember red as a dominant, decisive accent — CTAs, active states, progress
- Soft, modern execution: generous rounded corners, plenty of whitespace, calm neutral surfaces
- Light by default, with full dark mode
- Sharp, clean lines where precision matters — every element earns its place
- Monospace (JetBrains Mono) for code and technical contexts
- Status-driven views — colour signals what's open, in progress, done
- Communicates: craftsmanship with momentum — precise tools, forged and shipped

### nxsflow BP — "Builder's momentum"

- Amber for progress indicators, CTAs, highlights
- Compact type scale — information-dense
- Card-based Lean Canvas layouts
- Communicates: progressive, motivated, building something special

### nxsflow (parent) — "The foundation"

- Light background, lime accent used sparingly
- Clean editorial layout
- Communicates: precision, craft, the common thread

## Tone of Voice

### nxsflow (parent)

Confident, clear, understated. "We build precise tools" — no hype, no buzzwords.

### nexflow.it

Warm, personal, conversational. First person ("I've prepared your briefing"). Playful, light humor allowed. Never patronizing.

### manufakt.io

Direct, technical, momentum-driven. Respects user expertise — never patronizing, never "vibe coding." Status-oriented and celebrates progress ("Build complete. Three tasks left — let's ship them."). Concise and active, no fluff. Craftsmanship with forward motion.

### nxsflow BP

Encouraging, action-oriented. "Your idea deserves a plan." Progressive, optimistic. Speaks to builders.

## Using This Guideline

### As a Claude Code Plugin

Install the brand skill so it's available in any nxsflow repo.

**User-wide (all projects)** — add to `~/.claude/settings.json`:

```json
{
  "plugins": ["/path/to/nxsflow/logos/plugin"]
}
```

**Per-project** — add to your project's `.claude/settings.json`:

```json
{
  "plugins": ["/path/to/nxsflow/logos/plugin"]
}
```

Then invoke with: `/nxsflow-brand`

### As a CLAUDE.md Reference

Add to any product repo's `CLAUDE.md`:

```markdown
## Brand

Follow the nxsflow brand guideline at /path/to/nxsflow/logos/BRAND.md
```
