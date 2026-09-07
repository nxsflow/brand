# nxsflow (parent) — Landing Copy Deck

> Source of truth: `BRAND.md → Messaging`. EN is the original; DE is a crafted
> adaptation (Core Lexicon), not a literal translation. Structure mirrors the live
> staging site (hero → trias → pillars → two products → open foundation), re-led by the belief.
> Register: the parent sells nothing directly, so belief/foundation statements stay
> in the neutral third person; direct address ("you") appears only where the offer to
> the reader is described.

## Hero

> **The hero is the promise; the three sections under it are the proof** (landing
> repo `cyb7.s0y5`). It used to carry the whole argument in five sentences. Since
> 2026-09-07 it carries the hook, and each line of the title is redeemed by its
> own section below — see "Trias" further down.

- **Category line (EN):** Issue tracker for coding agents — with the memory and the channel
- **Category line (DE):** Issue-Tracker für Coding-Agenten — mit dem Gedächtnis und dem Kanal
- **Title (EN):** Set the direction. Assign the ticket. Keep what they learn.
- **Title (DE):** Gib die Richtung vor. Weise das Ticket zu. Behalte, was sie lernen.
- **Subhead (EN):** Your agents keep forgetting where the project is going — and which rules it runs by. With nexus-flow, every new session starts knowing what's queued, what the rules are, and what's already been figured out.
- **Subhead (DE):** Vergessen deine Agenten ständig, wohin die Reise geht und welche Regeln im Projekt gelten? Mit nexus-flow beginnt jede neue Sitzung im Bilde: Sie kennt die anstehende Arbeit, die Regeln — und das schon Herausgefundene.
- **Own line under it (EN):** Offline-first — fast locally, convergent when connected.
- **Own line under it (DE):** Offline-first — lokal schnell, konvergent sobald verbunden.
- **Primary action (both):** the real install one-liner with a copy button — `curl -fsSL https://nxsflow.com/nxs/install.sh | sh`
- **Button (EN / DE):** Get started / Loslegen — into the documentation
- **Beside it (EN / DE):** Read the source on GitHub / Den Quellcode auf GitHub lesen

**Three things about this hero are decisions, not wording, and a later edit
undoes them at a price:**

1. **"Open source ·" is gone from the category line, and it did not go for free.**
   The Head of Marketing held against dropping it; his condition was that a
   *visible way to the source* stands above the fold instead, because `curl | sh`
   shows a free download, not source code. That is the GitHub link. **Remove the
   link and the word comes back.**
2. **"Assign the ticket", not "assign the work".** "the work" leaves the category
   open and hits the competitor's loudest word — CrewAI assigns tasks to agents.
   The object carries the classification.
3. **"Keep what THEY learn", not "what you learned".** The second reading turns
   the product into a notebook for the human, and the competition can say it word
   for word.

**Barred in the hero and the three sections:** "orchestration", "coordination
layer", "agent teams", "workflow". The word "workflow" has exactly one allowed
place on the site and it is not here.

**Not in the copy, on purpose:** "and machines" / "und über Rechner hinweg". The
persistence claim stops at branch switches until the sync decision is made
(landing repo `cyb7.hdgg`, carried in by `cyb7.9z4j`). `nxs sync` ships without a
default endpoint and without a public self-host guide, so on day one the claim
would not be true.

## Trias — the three sections that redeem the title

Each section carries the title line it answers as its kicker, in the title's own
order, and nothing stands between the hero and the first of them. The German is
built, not translated: "file it" is **not** "ablegen" — in a German ticket
register one *legt Tickets an*.

**1 — "Set the direction." / "Gib die Richtung vor."**

- **EN:** You plan. Your agents file it. — You plan the direction with your agents: it lands on the board as epics and tickets, and it stays there — across sessions and branch switches.
- **DE:** Du planst. Deine Agenten legen die Tickets an. — Die Richtung planst du mit deinen Agenten – sie steht danach als Epics und Tickets auf dem Board, und dort bleibt sie: über Sitzungen und Branch-Wechsel hinweg.

**2 — "Assign the ticket." / "Weise das Ticket zu."**

- **EN:** You assign. Your agents build. — One message sets them to work through it in order, without you watching.
- **DE:** Du beauftragst. Deine Agenten bauen. — Eine Nachricht setzt sie darauf an, der Reihe nach abzuarbeiten – die Arbeit läuft, ohne dass du zusiehst.

**3 — "Keep what they learn." / "Behalte, was sie lernen."**

- **EN:** You correct. Your agents remember. — Something goes wrong, you say why once, and the rule outlives the session that earned it.
- **DE:** Du korrigierst. Deine Agenten merken es sich. — Etwas geht schief, du sagst einmal, warum – und die Regel überlebt die Sitzung, in der sie entstanden ist.

**Two findings of the Head of Marketing that look like defects and are not:**

- Section 1 is the weakest of the three texts — its body does double duty on
  planning and on persistence. It stays, because the persistence half is the
  strike against beads, where the board state dissolves into git's
  last-write-wins.
- Section 2 is the strongest *promise* and the weakest *exclusive*: "You assign.
  Your agents build." is the one head CrewAI can say word for word. The
  consequence is not a copy change but a requirement on the figure beside it — it
  shows the mechanism (one message, an order derived from the dependency graph,
  the answers in the same log) instead of illustrating the claim.

## Positioning

**EN:** nxsflow builds tools that keep you in the lead of ambitious work — while a growing share of the execution is carried by your team of agents. You initiate, coordinate, and decide; your agents build and ship. So your energy goes where it matters, not the busywork.

**DE:** nxsflow baut Werkzeuge, mit denen du bei ambitionierten Vorhaben die Führung behältst — während ein wachsender Anteil der Ausführung von deinem Team aus Agenten getragen wird. Du initiierst, koordinierst und entscheidest; deine Agenten bauen und liefern. So fließt eure Energie dahin, wo sie zählt — nicht in den Kleinkram.

## Pillar 1 — "You set the direction." / "Du gibst die Richtung vor."

**Body (EN):** You're the one who initiates, coordinates, and decides. Your agents propose and execute — the calls that matter stay yours.

**Body (DE):** Du initiierst, koordinierst und entscheidest. Deine Agenten schlagen vor und führen aus — die Entscheidungen, auf die es ankommt, bleiben deine.

**Proof:** Clear approval and decision points, full transparency, steerable at any moment. / Klare Freigabe- und Entscheidungspunkte, volle Transparenz, jederzeit steuerbar.

## Pillar 2 — "Your team of agents does the execution." / "Dein Team aus Agenten übernimmt die Ausführung."

**Body (EN):** A growing share of the doing moves to your agents — more with every release. Your output grows without your team burning out.

**Body (DE):** Ein wachsender Anteil der Ausführung wandert an deine Agenten — mit jedem Release mehr. Euer Output wächst, ohne dass das Team ausbrennt.

**Proof:** Agents pick up tasks and run them in parallel. / Agenten übernehmen Aufgaben und erledigen sie parallel.

## Pillar 3 — "Nothing drifts, nothing gets lost." / "Nichts entgleitet, nichts geht verloren."

**Body (EN):** People and agents work toward the same goal, from one shared picture of what's happening and what's next. Everyone pulls in the same direction.

**Body (DE):** Menschen und Agenten arbeiten gemeinsam auf das Ziel hin — aus einem gemeinsamen Bild davon, was läuft und was als Nächstes kommt. Alle ziehen an einem Strang.

**Proof:** One place that keeps it all together, offline-first — the nxs platform under both products. / Ein Ort, der alles zusammenhält, offline-first — die nxs-Plattform unter beiden Produkten.

## Two products

**manufakt.io — building software (EN):** You architect and decide; your coding agents build and ship. You lead, they ship. → _From intent to shipped._

**manufakt.io — Software bauen (DE):** Du entwirfst und entscheidest, deine Coding-Agenten bauen und liefern. Du führst, sie liefern. → _Aus dem Plan wird das Release._

**nexflow.it — running knowledge-work projects (EN):** You think it through; your agents see it through. → _From 'someday' to done._

**nexflow.it — Wissensarbeit-Projekte führen (DE):** Du denkst es durch, deine Agenten ziehen es durch. → _Aus 'irgendwann' wird erledigt._

## Open foundation

**EN:** Both products stand on one open foundation — nexus-flow, an agent-native, offline-first engine that keeps the work of people and agents together.

**DE:** Beide Produkte stehen auf einem offenen Fundament — nexus-flow, einer agent-nativen, offline-first-Engine, die die Arbeit von Menschen und Agenten zusammenhält.

## Payoff & closing

- **Payoff (EN):** So your energy goes where it matters — not the busywork.
- **Payoff (DE):** So fließt eure Energie dahin, wo sie zählt — nicht in den Kleinkram.
- **Closing CTA (EN / DE):** Explore the products / Die Produkte ansehen
