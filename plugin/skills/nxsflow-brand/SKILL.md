---
name: nxsflow-brand
description: nxsflow brand guideline — colors, typography, tone of voice, logo rules, and per-product design language for all nxsflow products (nexflow.it, manufakt.io, nxsflow BP, Amplify Overtone). Use this skill whenever building UI, writing copy, choosing colors or fonts, designing layouts, or making any design/style/tone decision for any nxsflow product. Also use when creating marketing materials, landing pages, email templates, or documentation styling. Even if the user doesn't mention "brand", if they're working on an nxsflow product and making visual or tone choices, this skill applies.
---

# nxsflow Brand Guideline

This skill provides the complete brand system for nxsflow and all its products. Follow these rules when making any design, styling, or tone-of-voice decision.

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
| Amplify Overtone | Open source | overtone.nxsflow.com | Lavender #A78BFA + Rose #F472B6       |

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

### Amplify Overtone

- Accent: `#A78BFA` (lavender)
- Accent secondary: `#F472B6` (rose)
- Gradient: `linear-gradient(135deg, #A78BFA, #F472B6)`
- Background: `#FFFFFF`

### nxsflow (parent)

- Accent: `#B9FF66` (lime, shared with nexflow.it)
- Background: `#FFFFFF`

### CSS Custom Properties

When building UI, use the design token variable names:

```
--nxs-graphite, --nxs-gray, --nxs-border, --nxs-white
--nxs-nexflow-primary, --nxs-nexflow-primary-dark, --nxs-nexflow-tint
--nxs-manufakt-accent, --nxs-manufakt-accent-dark, --nxs-manufakt-tint, --nxs-manufakt-gradient, --nxs-manufakt-bg
--nxs-bp-accent, --nxs-overtone-accent, --nxs-overtone-accent-secondary
--nxs-parent-accent
```

These tokens live in the `nxsflow/logos` repo under `tokens/colors.css` and `tokens/colors.json`. Copy them into your project or reference them via a shared path.

## Typography

### Fonts

- **Headings (all brands):** Merriweather — weights 700, 900
- **Body (default):** Merriweather Sans — weights 300, 400, 700
- **Body (nexflow.it):** Nunito — weights 400, 600, 700
- **Monospace (manufakt.io):** JetBrains Mono

### Type Scales

**Default (parent, manufakt.io) — 1.25 ratio:**
xs: 12px, sm: 14px, base: 16px, lg: 20px, xl: 25px, 2xl: 31px, 3xl: 39px

**Amplify Overtone — 1.4 ratio:**
xs: 12px, sm: 14px, base: 16px, lg: 22px, xl: 31px, 2xl: 44px, 3xl: 61px

**nexflow.it — 1.333 ratio:**
xs: 13px, sm: 15px, base: 18px, lg: 24px, xl: 32px, 2xl: 42px, 3xl: 56px

**nxsflow BP — 1.2 ratio:**
xs: 11px, sm: 13px, base: 15px, lg: 18px, xl: 22px, 2xl: 26px, 3xl: 31px

### CSS Custom Properties

```
--nxs-font-heading, --nxs-font-body, --nxs-font-body-nexflow, --nxs-font-mono
--nxs-text-xs through --nxs-text-3xl
```

Use `[data-brand="overtone"]`, `[data-brand="nexflow"]`, or `[data-brand="bp"]` on a parent element to activate product-specific type scales.

## Logo System

### Flagship Monograms

- **nexflow.it:** "nf" merged letterform in lime (#B9FF66). Works on dark and light backgrounds.
- **manufakt.io:** "mf" merged letterform in graphite (#1C1C1C). Light variant (#FAF9F7) for dark backgrounds. _Ember-palette redesign pending; the retained `logos/beads-dashboard/` "db" monogram (d in graphite, b in ember red) is the starting point._

### Other Brands

- **nxsflow:** Organic mesh icon — asymmetric nodes connected by hand-drawn curves. Lime (#B9FF66) fills, graphite outlines. Full variant (5 nodes) for wordmark pairing, simplified variant (3 nodes) for favicons.
- **nxsflow BP:** Hand-drawn compass icon — wobbly ring with draft stroke underneath, north needle solid amber (#F59E0B), south needle faded outline. Single design for all sizes.
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
- Subtle rotation on tags/badges (0.3-0.5deg)
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

### Amplify Overtone — "Open workshop"

- Lavender with gradient treatments
- Documentation-style layouts
- Communicates: collaboration, community, inviting contributions

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

### Amplify Overtone

Inclusive, technical, community-minded. "We" not "I." Documentation voice. Welcoming to all levels.

## How to Apply

When working on an nxsflow product:

1. **Identify which product** you're working on from the brand hierarchy
2. **Use that product's colors** — never mix colors between products
3. **Use that product's type scale** — set `data-brand` attribute if using CSS tokens
4. **Follow that product's design language** — nexflow.it is hand-drawn and playful, manufakt.io is minimal and precise
5. **Match that product's tone of voice** — especially in UI copy, error messages, onboarding text
6. **Use CSS custom properties** from the design tokens rather than hardcoding hex values
