# NexusFlow Brand Guideline

## Company

- **Legal name:** NexusFlow UG (haftungsbeschränkt)
- **Short name:** NexusFlow
- **Domain:** nxsflow.com
- **Positioning:** Precise tools for technical professionals

## Brand Hierarchy

| Brand            | Type        | Domain               | Accent Color                         |
| ---------------- | ----------- | -------------------- | ------------------------------------ |
| NexusFlow        | Parent      | nxsflow.com          | Lime #B9FF66                         |
| nexflow.it       | Flagship    | nexflow.it           | Lime #B9FF66                         |
| manufakt.io      | Flagship    | manufakt.io          | Graphite #1C1C1C + Warm Mist #FAF9F7 |
| NexusFlow BP     | Product     | bp.nxsflow.com       | Amber #F59E0B                        |
| Amplify Overtone | Open source | overtone.nxsflow.com | Lavender #A78BFA                     |

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

- **NexusFlow:** Organic mesh icon — asymmetric nodes connected by hand-drawn curves. Lime (#B9FF66) fills, graphite outlines. Full variant (5 nodes) for wordmark pairing, simplified variant (3 nodes) for favicons.
- **NexusFlow BP:** Hand-drawn compass icon — wobbly ring with draft stroke underneath, north needle solid amber (#F59E0B), south needle faded outline. Single design for all sizes.
- **Amplify Overtone:** Hand-drawn tuning fork icon — bold prongs with U-bend, handle, and resonance waves. Lavender (#A78BFA). Full variant (with waves) for large sizes, simplified variant (no waves) for favicons.

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

## Using This Guideline

### As a Claude Code Plugin

Install the brand skill so it's available in any NexusFlow repo.

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

Follow the NexusFlow brand guideline at /path/to/nxsflow/logos/BRAND.md
```
