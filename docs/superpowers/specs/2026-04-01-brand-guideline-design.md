# NexusFlow Brand Guideline — Design Spec

## 1. Company Identity & Brand Hierarchy

### Company
- **Legal name:** NexusFlow UG (haftungsbeschränkt)
- **Short name:** NexusFlow
- **Domain:** nxsflow.com

### Brand Positioning
Precise tools for technical professionals. Craft-oriented, engineering-quality software.

### Audience
Technical professionals broadly — developers, product managers, knowledge workers at companies of any size.

### Hierarchy

| Brand | Type | Domain | Tone |
|-------|------|--------|------|
| **NexusFlow** | Parent | nxsflow.com | Confident, precise, understated |
| **nexflow.it** | Flagship product | nexflow.it | Personal, playful, pen-on-paper |
| **manufakt.io** | Flagship product | manufakt.io | Precise, minimal, space-for-your-creation |
| **NexusFlow BP** | Product | bp.nxsflow.com | Progressive, motivated, builder energy |
| **Amplify Overtone** | Open source | overtone.nxsflow.com | Open, collaborative, community-minded |

nexflow.it is the core product. All other products exist to enable or complement it. The parent brand's accent color is shared with nexflow.it to reinforce this relationship.

---

## 2. Color System

### Parent Brand (NexusFlow)
| Role | Color | Hex |
|------|-------|-----|
| Background | White | #FFFFFF |
| Accent | Lime | #B9FF66 |
| Text | Graphite | #1C1C1C |

### nexflow.it
| Role | Color | Hex |
|------|-------|-----|
| Primary | Lime | #B9FF66 |
| Primary dark | Deep lime | #84CC16 |
| Text | Graphite | #1C1C1C |
| Light tint | Lime wash | #F5FFE6 |
| Background | White | #FFFFFF |

### manufakt.io
| Role | Color | Hex |
|------|-------|-----|
| Primary | Graphite | #1C1C1C |
| Background | Warm mist | #FAF9F7 |

Two-color system only. No accent color. The user's creation provides the color.

### NexusFlow BP
| Role | Color | Hex |
|------|-------|-----|
| Accent | Amber | #F59E0B |
| Text | Graphite | #1C1C1C |
| Background | Inherited from parent (white) | #FFFFFF |

### Amplify Overtone
| Role | Color | Hex |
|------|-------|-----|
| Accent | Lavender | #A78BFA |
| Text | Graphite | #1C1C1C |
| Background | Inherited from parent (white) | #FFFFFF |

### Shared Neutrals (all brands)
| Role | Color | Hex |
|------|-------|-----|
| Near-black | Graphite | #1C1C1C |
| Mid-gray | Secondary text | #6B6B6B |
| Light gray | Borders | #E5E5E0 |
| White | Background | #FFFFFF |

---

## 3. Typography

### Heading Font (all brands)
**Merriweather** (serif, Google Fonts)
- Used for: page titles, section headings, hero text
- Weights: 700 (bold), 900 (black) for impact

### Body Font — Default (parent, manufakt.io, BP, Overtone)
**Merriweather Sans**
- Used for: body text, UI labels, navigation
- Weights: 300 (light), 400 (regular), 700 (bold)

### Body Font — nexflow.it only
**Nunito**
- Rounded, humanist sans-serif — warmer and friendlier
- Weights: 400 (regular), 600 (semi-bold), 700 (bold)

### Monospace (manufakt.io code contexts)
**IBM Plex Mono** or **JetBrains Mono**
- For code blocks, terminal output, build logs

### Type Scales

**Default (parent, manufakt.io, Overtone) — 1.25 ratio (major third):**

| Token | Size |
|-------|------|
| xs | 12px |
| sm | 14px |
| base | 16px |
| lg | 20px |
| xl | 25px |
| 2xl | 31px |
| 3xl | 39px |

**nexflow.it — 1.333 ratio (perfect fourth):**

| Token | Size |
|-------|------|
| xs | 13px |
| sm | 15px |
| base | 18px |
| lg | 24px |
| xl | 32px |
| 2xl | 42px |
| 3xl | 56px |

**NexusFlow BP — 1.2 ratio (minor third):**

| Token | Size |
|-------|------|
| xs | 11px |
| sm | 13px |
| base | 15px |
| lg | 18px |
| xl | 22px |
| 2xl | 26px |
| 3xl | 31px |

---

## 4. Logo System

### Flagship Products — Merged Letterform Monograms
- **nexflow.it** — "nf" monogram, serif typeface, letters share a vertical stroke. Rendered in lime (#B9FF66). Works on both dark and light backgrounds.
- **manufakt.io** — "mf" monogram, same serif typeface and merge technique. Rendered in #1C1C1C on light, #FAF9F7 on dark backgrounds.

### Parent Brand & Other Products — Wordmark + Abstract Icon
- **NexusFlow** — wordmark in Merriweather Bold + "nexus" connection-node icon. Lime (#B9FF66) accent.
- **NexusFlow BP** — wordmark ("NexusFlow" bold, "BP" light weight) + thematic business plan icon. Amber accent.
- **Amplify Overtone** — wordmark ("Amplify" bold, "Overtone" with gradient) + wave/overtone icon. "Overtone" text uses a lavender gradient for liveliness. Lavender accent.

### Logo Usage Rules
- Minimum clear space: 1x the height of the monogram/icon on all sides
- Minimum size: 24px height for digital, 10mm for print
- Allowed variants: full color, monochrome (#1C1C1C), reversed (white/lime on dark)
- Never stretch, rotate, or recolor outside the defined palette

### Favicon / App Icons
- **nexflow.it:** "nf" monogram on lime background
- **manufakt.io:** "mf" monogram on graphite background
- **Others:** icon only on brand accent background

### Deliverables Per Logo
- SVG vector (source of truth)
- PNG exports: 128px, 256px, 512px, 1024px
- Favicon: .ico + .png (16px, 32px, 180px Apple Touch)
- Social media kit sizes (LinkedIn, Twitter/X, etc.)

---

## 5. Per-Product Design Language

### nexflow.it — "Pen on paper"
- Hand-drawn SVG lines for borders, dividers, buttons, and UI chrome
- Lines are intentionally imperfect — slightly wobbly, never perfectly straight
- Subtle rotation on tags/badges (0.3–0.5deg)
- Communicates: in progress, always learning, personal, human
- Rounded corners on containers (matching Nunito's rounded character)
- Generous spacing — feels open and breathable

### manufakt.io — "Precision instrument"
- Strict two-color system (#1C1C1C + #FAF9F7), no accent color
- Generous whitespace — the tool stays out of the way
- Sharp, clean lines — the opposite of nexflow.it's hand-drawn approach
- Monospace font for code/technical contexts
- Minimal UI — every element earns its place
- Communicates: clarity, direction, craftsmanship, space for your creation

### NexusFlow BP — "Builder's momentum"
- Amber accent used for progress indicators, CTAs, highlights
- Compact type scale — information-dense, efficient
- Card-based layouts for Lean Canvas sections
- Communicates: progressive, motivated, "I'm building something special"

### Amplify Overtone — "Open workshop"
- Lavender accent with gradient treatments for visual energy
- Open, welcoming tone — community-oriented
- Clear documentation-style layouts (open source project)
- Communicates: collaboration, extending what exists, inviting contributions

### NexusFlow parent (nxsflow.com) — "The foundation"
- Light background, lime accent used sparingly
- Clean, editorial layout
- Showcases all products — acts as a hub
- Communicates: precision, craft, the common thread

---

## 6. Tone of Voice

### NexusFlow (parent)
- Confident, clear, understated
- "We build precise tools" not "We're revolutionizing productivity"
- No hype, no buzzwords. Let the work speak.

### nexflow.it
- Warm, personal, conversational
- Speaks like a trusted colleague, not a robot
- Uses first person: "I've prepared your briefing" not "Your briefing has been prepared"
- Allowed to be playful, use light humor
- Never patronizing

### manufakt.io
- Direct, concise, technical
- Respects the user's expertise — no hand-holding
- Status-oriented: "Authentication complete. Starting API routes."
- Never uses "vibe coding" or similar casual framing — this is craftsmanship

### NexusFlow BP
- Encouraging, action-oriented
- "Your idea deserves a plan" — motivating without being cheesy
- Speaks to builders and founders
- Progressive tone — forward-looking, optimistic

### Amplify Overtone
- Inclusive, technical, community-minded
- Documentation voice — clear and helpful
- "We" not "I" — this is a shared effort
- Welcoming to contributors of all levels

---

## 7. Implementation

### Deliverables
1. **BRAND.md** — human/AI-readable brand guideline (single source of truth)
2. **tokens/colors.css** — CSS custom properties for all brand colors
3. **tokens/colors.json** — JSON color tokens (for Tailwind configs, etc.)
4. **tokens/typography.css** — font imports and type scale
5. **Claude Code plugin/skill** — installable skill that makes brand guidelines available in any repo
6. **SVG logos** — monograms for flagships, wordmark+icon for others
7. **PNG exports** — multiple sizes per logo
8. **Favicon set** — per product
9. **Social media kit** — per product

### How Products Reference the Guideline
Each product repo's `CLAUDE.md` references the brand guideline:
```
## Brand
Follow the NexusFlow brand guideline. The brand skill is installed as a Claude Code plugin.
```

The plugin/skill provides the full guideline context to Claude Code in any repo where it's installed.
