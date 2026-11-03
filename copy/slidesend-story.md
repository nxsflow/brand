# Why slidesend exists

> The long form of the slidesend brand: why it exists, what it stands for, and
> what its name, its mark and its tone have to carry. `BRAND.md → slidesend`
> is the binding short form; the landing copy (`slidesend-landing.md`) and the
> logo kit (`logos/slidesend/`) are derived from both. Facts about what the
> product does today follow the slidesend docs; check them again when the
> product changes.

## In one sentence

slidesend exists because the work of preparing a talk is moving from people
to agents, and the tools we have for it were built for a person with a mouse,
not for an agent.

slidesend is the first product from nxsflow that follows this shift all the
way through: the agent does the work, the person sets the direction, and the
talk itself lives on the web instead of in a file.

## 1. The tool no longer fits the work

For decades, "making a presentation" has meant opening an editor and pushing
boxes around a canvas. Text, tables, calculations, slides: all of it made by
hand, click by click. The editor was the centre of the work, and the result
was a file.

That is changing. Agents take on more and more of exactly this work: they
write text, build tables, calculate, structure a talk. The more they take on,
the less a person needs an editor. What a person needs is a place to decide.

The widespread office formats were not built for this. They were designed for
an eye and a mouse: layout lives in coordinates, meaning lives in formatting,
and whether something is right can only be seen by a person looking at it. An
agent can write such a file, but it can hardly check it, and every mistake
shows only when a person opens it. That is why agents keep running into
trouble with these programs.

slidesend starts from the other end: from a format an agent can read, write
and check. A talk is a project made of code. What a slide says sits in named
fields, and `slidesend check` reports every mistake with its slide and field,
so the agent can fix it on its own.

## 2. The reversal: the person steers, the agent builds

slidesend turns the concept around. Preparing the slides is the agent's job;
steering is the person's.

The person decides what only they can decide: the message, the audience, the
length, the arc of the story, the moments where the room takes part. The
agent asks for these before it writes the first slide, and it never invents
facts. Then it builds: one idea per slide, the spoken words as notes.

That is why slidesend has **no editor** today. This is not a gap; it is the
product's statement. An editor will come back, but in a different role: for
the single correction, the number that changed just before the talk, the word
that should sound different on stage. Not for the main work.

## 3. The stage lives on the web

A slidesend talk is not a file on a laptop that gets plugged into a projector.
It is hosted, today on AWS.

That has a consequence the room notices at once: **the device that steers the
talk and the screen that shows it are independent of each other.** They talk
over a secured WebSocket connection across the internet, and nobody else can
step in. The speaker steers from their own device, the stage runs on the
computer at the projector, and no cable, no adapter and no borrowed laptop
decides any more whether the talk can start.

AWS is a deliberate choice: there the infrastructure can be built serverless,
so a hosted talk costs almost nothing while it is not running, and little
while it is. Other hosts are to follow. The brand therefore must not depend on
AWS. It promises "hosted and inexpensive", not a particular provider.

## 4. The room takes part

Because the talk lives on the web, everyone in the room can reach it. The
audience scans a code and joins on their phones, wherever the speaker has
planned for it: they answer polls, ask questions and can talk to AI agents
that belong to the talk.

A talk turns from a monologue into a conversation with the room. That is the
promise slidesend leads with: **a talk the room takes part in.** The agent
story explains how the talk gets made; taking part explains why you would
want to give it this way.

And all of it sits on one platform: preparation, stage, desk, phone, review.
No second tool for polls, no third one for questions.

## 5. Today and tomorrow

The brand has to say honestly what works today, and be big enough for what
comes next.

**Today** slidesend is a library. You install it, create a talk on your own
machine, start it there and can host it. One server then hosts exactly that
one talk. Sharing slides with someone in passing is not possible yet, and
neither is working on them together.

**Tomorrow** there can be one place where all your talks live: a multi-tenant
server where several people keep their presentations, share them with others
and work on them together. From there you start a talk at any time and give
the audience a link.

That is a vision, not a promise. For the copy: what does not exist yet is not
claimed. For the brand: nothing in the name, the mark or the tone may pin it
down to "a library for developers".

## 6. What the brand has to carry

- **The name, with both readings.** slide·send: the slide is sent, to the
  stage and to every phone in the room, over the network instead of a cable.
  slides·end: the end of slides as we knew them, built by hand in an editor.
  Both readings are intended and both are true. Even so, the name is never
  split, never shown with two accented s, and never abbreviated.
- **The mark.** A slide split by a wave: the desk where the person steers, the
  stage the room sees, apart and still one. The wave is the connection over
  the network, its step the send. The wordmark's only colour is the dot on
  the i, a small slide: the one lit point in the room.
- **The roles.** The person decides, the agent builds, the room takes part.
  Never "slidesend makes your presentation for you" (partnership, not
  replacement, as in the voice guardrails).
- **The calm.** The tone stays clear, practical and calm. Arguing against the
  old tool is done by showing what the new one does differently, never with a
  side swipe and never with a name.
- **The openness.** Open source under Apache-2.0, the talk as a project on
  your own machine, hosting in your own account. That stays true when a
  shared server is added later.

## 7. Lines that can follow from this

Candidates, not decided:

- "You decide what the talk says. Your agent builds it. The room takes part."
- "No editor. You say what matters; your agent writes the slides."
- "Steer from your device, show on any screen, take part on any phone."
- "Presentations built for agents and given for people."
- "The talk lives on the web, not on the laptop at the projector."
