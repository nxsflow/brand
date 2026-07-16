# Grounding notes for the landing copy decks

Captured 2026-07-15 to ground the copy decks against the live staging sites.
The Chrome extension was unavailable, so content was read via WebFetch (server
HTML). JS-rendered content may be missing where noted.

## staging.nxsflow.com (parent) — real copy exists

**Current structure (keep this skeleton):**
Hero → "Two flagships" products → "One open foundation" (nexus-flow: Flow /
Memory / Chat) → Values → Footer.

**Current copy (the "not powerful enough" baseline we replace):**
- Hero: "Two flagship products, one open foundation."
- Subhead: "nxsflow builds precise tools for technical work, with AI agents on
  the team. manufakt.io and nexflow.it stand on one open foundation — nexus-flow…"
- Values: "Precise tools, built to be relied on." / "…clear, careful tools —
  made to be relied on, and to keep working for years, not weeks."

**Diagnosis:** leads with "precise tools for technical work" + reliability
("built to last") — exactly the bland, retired positioning. No belief, no "you
set the direction / your agents execute," no human ambition.

**Strong phrases worth preserving / adapting (do not throw away):**
- "You lead, they ship." (manufakt.io blurb) → aligns with Pillar 1 + 2.
- "keeps the thread so nothing slips" (nexflow.it blurb) → aligns with Pillar 3
  ("Nothing drifts, nothing gets lost").
- "a personal Chief of Staff" (nexflow.it) → warm, concrete metaphor.
- "with AI agents on the team" → aligns with "team of agents."
- The open-foundation section (nexus-flow Flow/Memory/Chat) is accurate — keep,
  reframed under the new belief.

**Plan for the deck:** keep the structure and the strong phrases; re-lead with the
belief + new parent positioning + the three pillars; demote "precise/reliable" from
the headline to at most a supporting value.

## staging.manufakt.io — coming-soon shell only

- WebFetch read only `<title>manufakt.io — coming soon</title>`; no body copy.
- **Uncertainty:** may be a JS-rendered SPA whose real content WebFetch cannot see —
  not confirmed truly empty.
- **Plan for the deck:** treat as greenfield, built from the pyramid (forge voice,
  developer audience, momentum). If existing copy should be preserved, get it from
  the user and fold it in.

## nexflow.it — greenfield (no live landing yet)

- No landing page exists. Fully greenfield.
- **Proposed skeleton:** Hero (tagline + subhead) → Positioning → 3 pillars
  (order 1 → 2 → 3) → proof → warm CTA. Voice: warm, personal, first person
  ("I've prepared your briefing"). Reuse the "keeps the thread / nothing slips"
  and "Chief of Staff" ideas surfaced on the parent site.
