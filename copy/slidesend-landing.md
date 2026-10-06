# slidesend — Landing Copy Deck

> Source of truth: `BRAND.md → Messaging → slidesend`. EN first; a DE
> adaptation follows later (Core Lexicon: crafted, never translated). Voice:
> clear, practical, calm — "the stage." Audience: people who give talks, many
> of them developers who already work with a coding agent. The name is always
> lowercase, also at the start of a sentence. Surface: the product page at
> nxsflow.com/slidesend. Every fact below is taken from the slidesend docs as
> of v0.3.1 (README, `packages/*/docs`); when the product changes, check the
> numbers and commands again.

## Page meta

- **Title:** slidesend — a talk the room takes part in
- **Meta description:** Open-source presentations your audience joins on their phones. Write the talk in TypeScript with your AI agent, rehearse it, present it, review it.
- **Link preview image:** `logos/slidesend/social/slidesend-social.png` (1200×630). Alt text: "slidesend — A talk the room takes part in."
- **Wordmark alt text:** slidesend

## 1. Hero

- **Eyebrow:** Open source · Apache-2.0
- **Headline:** A talk the room takes part in.
- **Subline:** slidesend is a presentation tool for talks your audience joins on their phones. You write the talk with your AI agent, in TypeScript; the room answers polls and questions while you speak.
- **Install (with a copy button):** `npm create @slidesend@latest my-talk`
- **Under the command:** Then `cd my-talk` and `npm run dev`. Phones on your network can join right away — no cloud account needed.
- **Secondary link:** Read the docs →

## 2. Stage, desk and phone

**Heading:** Three views of one talk.

Every talk runs on three screens at once, and they stay in step.

- **Stage** — what the room sees on the projector: the slide, the code to join, and the answers as they come in.
- **Desk** — your view, dark for a dark room: your notes in large type, what is on stage now and what comes next, and a clock that shows whether you are ahead of plan or behind.
- **Phone** — the audience scans the code and joins. They answer polls and open questions, and a phone that was locked finds its way back to the current slide on its own.

## 3. Written with your AI agent

**Heading:** Written with your AI agent.

Every talk comes with an `AGENTS.md` that points your coding agent at the docs of the slidesend version you installed. The docs ship inside the packages, so the agent reads the ones that match your code.

Before it writes a single slide, the agent asks you for the calls only you can make: the message, the audience, the length, the storyline, where the room takes part. Your answers are written into the talk, so the next session starts from them. It does not invent facts or quotes — it asks, or leaves a visible placeholder.

Then it writes one idea per slide, with what you will say as the notes. `slidesend check` names every mistake by slide and field, so the agent can fix it.

## 4. Rehearse, go live, review

**Heading:** Rehearse. Go live. Review.

- **Rehearse** with a private join link and a clock on every step. A rehearsal keeps its own answers and timings, apart from the real talk.
- **Go live** in one click, or plan the talk for later and the session opens by itself before you start. The audience joins with the code on the stage.
- **Review** afterwards: planned against measured time for every step. Adopt the measured times as your new plan, or export every answer as JSON.

## 5. Hosting

**Heading:** On your laptop, or on your own AWS account.

- **Local.** `npm run dev` serves the talk from your laptop. Phones on the same network join directly — no cloud account, no sign-up, nothing to pay.
- **On AWS.** Create the talk with `--aws`, and `slidesend deploy` puts it online with one command, so anyone with the link can join. Between talks it costs about USD 1 a month; a session for a class-sized audience costs a few cents. `slidesend destroy` removes it all.
- **An AI agent for the audience, if you want one.** The room can ask questions to an agent on their phones, running on Amazon Bedrock, for about USD 0.0005 per question. Nothing that costs money runs outside an open session, and a forgotten session closes on its own.

**Fine print:** Estimates at eu-central-1 prices. The costs are AWS's, billed to your own account — check your bill.

## 6. Links

**Heading:** Start your talk.

- **GitHub** — source, issues and releases: https://github.com/nxsflow/slidesend
- **npm** — the `@slidesend` packages: https://www.npmjs.com/org/slidesend
- **Docs** — from your first talk to your own slide types: https://github.com/nxsflow/slidesend/tree/main/packages/core/docs

Repeat the install command here, with its copy button: `npm create @slidesend@latest my-talk`

## 7. Footer

- **Line:** slidesend is open source under the Apache License 2.0. Made by [nxsflow](https://nxsflow.com).
- **Legal notice:** https://nxsflow.com/legal-notice
- **Privacy policy:** https://nxsflow.com/privacy
