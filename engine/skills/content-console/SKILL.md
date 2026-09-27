---
name: "content-console"
description: "Content Console: pick what to work on next, turn seeds into sprout briefs, and run the standard or deep refinement pass on drafts, for the creator whose profile is loaded. Use for any content pass, or when the creator says console."
---

# Content Console

The system for moving a creator's content from seed to published.

This file holds the **procedure**. It is the engine: it works for any creator and never names one. Everything specific to one creator lives in their **profile**. Everything this file depends on changes faster than it does, so read the sources below at run time rather than working from memory of them.

## Before every run: load the profile

Read the active creator's profile before doing anything else:

- **`profile.md`** - who they are, their voice rules, conventions, doctrine, dial settings, and personal reference docs.
- **`notion-map.md`** - where each Notion page and database named in this file lives for this creator.

In the repo these sit in `profiles/<creator>/`. In an installed setup they are provided as project files alongside this skill. If no profile can be found, say so and stop rather than guessing.

Wherever this file says **the profile**, it means a value from those files. Where the profile does not set a dial, use the default in *Dials* below.

## Where things live

Three tiers. Nothing lives in two of them. The Notion map says where each named page is for this creator.

**Tier 1 - Live records. Notion only, queried every run, never cached.**

The **Content Pipeline** is the source of truth for every seed, draft and piece. Never hold a parallel copy of a row anywhere.

Statuses: **Seed → Sprout → Draft → Refined → Completed → Published**.

Properties: **Form** (the twenty-two forms), **Medium**, **Series**, Platform, Published Date, Tool, Clips, Images, Notes. The profile lists any values specific to this creator.

**Tier 2 - Working strategy. Notion canonical, read live.**

These change often and the creator edits them, sometimes from their phone.

- **Cadence & Mix** - the balance strategy. Read at the start of every Queue run and for every neighbours check.
- **Content Formats** - what each format is, plus the named video treatments (ways to shoot any piece).
- **Phrase Bank**, **Reframe Bank**, **Quotes** - harvest destinations and opener patterns.
- **Clip Library**, **Tools Library**, and the creator's doctrine pages named in the profile.
- **The life archive** - events by era, and the through-lines across eras. This is what the specificity rule searches.

**Tier 3 - Deep reference. Loaded in full at the start of a pass.**

Long, stable, needed in full.

- **The creator's personal reference docs**, listed in the profile: their voice file and AI filter (both non-negotiable), and their foundations (doctrine, lexicon, retired terms, origin scenes).
- **The craft library**, read-only, the same for every creator. Until it is converted into files packaged with this skill, it is provided as project files:
  - **`The_Pattern_Book.pdf`** - the twenty-two forms, worked, with examples. **The authority on form.** Its fifteen-second route is how a form gets chosen.
  - **`The_Thread_Storytelling_and_Content_Craft.pdf`** - the process, the four currencies, the four gaps, ten openings, six landings, the specificity ladder, diagnostics.
  - **`The_Shape_of_an_Idea.pdf`** - the machinery for material that is not a story.

**The rule when something new needs a home:** if the creator would plausibly edit it on their phone, it goes in Notion. If it is long, stable, and needed in full at the start of a pass, it goes in a reference doc.

## The twenty-two forms

From the Pattern Book, grouped by where the raw material starts. The families are a finding aid, not a property; derive them when reading.

| Family | Forms |
|---|---|
| It starts in a moment | Moment, Object, Return, Failed Attempt, Confession, Observation |
| It starts in a change of mind | Turn, Correction, Reframe, Question Held |
| It starts in a structure you can see | Distinction, Definition, Model, Taxonomy, Mechanism, Sequence |
| It starts in what you want them to do | Tool, Diagnostic, Permission, Constraint |
| It starts with the reader | Direct Address, Composite |

Hybrids are normal and Form is multi-select, but **name both parts before drafting**. A hybrid built without naming its parts is a piece with two threads.

Most Seeds have no Form yet, and that is correct. Form is chosen at the fifteen-second route, which happens in Sprout.

## Locked rules

These apply in every mode, for every creator.

1. **Verbatim is sacred.** The creator's exact language is preserved unless they say otherwise. When in doubt, keep their line and put the alternative in the notes.
2. **Never invent the creator's life.** See the specificity rule below. This is the one failure that cannot be undone once published.
3. **Voice rules come from the profile.** Follow them in every draft and edit. Retired terms listed in the profile never appear in new work.
4. **An open feedback note means not ready.** The profile names the marker the creator uses. It means a question or something needing a bigger rewrite, not an answer. Any open note means the piece is not ready to push. Reflect, then generate a new draft.
5. **Quote harvest is a standing step.** Every pass, flag quotable lines and add them to the Quotes page named in the profile, filed by theme, source row noted, marked `(adapted)` if tightened. A line is quotable when it stands alone, carries one claim or one image, sounds like the creator, and would work on a card. Reframes go to the Reframe Bank, opener patterns to the Phrase Bank.
6. **Flag the bigger question first.** If a piece has a core question larger than refinement, surface it before the light edit. The creator answers or says proceed.
7. **Every pass ends with two buttons:** build next draft and push to Notion, or review feedback and generate a new draft.
8. **The write-your-own box is never optional.** Every card in every pass carries one. Options are a starting point, not a menu to pick from.
9. **Keep the raw original.** The creator's original unedited material is preserved in a collapsed section on the row (the profile names it), never overwritten by a later pass. It protects verbatim when a later pass wants to reach back, it builds a corpus of pure creator text for voice work, and it makes visible what the Console has actually been changing.

## The specificity rule

Scene detail is what most often gets lost between raw material and the page, especially when material is spoken or channelled rather than written. This is structural, not occasional, so it gets a permanent station in every pass. The profile may say why this creator in particular drifts to altitude.

**For the creator's own life: retrieve or ask. Never generate.**

- **Retrieve.** When a line sits at altitude, search the life archive in Notion, the origin scenes in the creator's foundations, and the Pipeline archive for two or three real moments that would carry it. Name which fits the claim best. The creator picks.
- **Ask.** When nothing on file fits, ask the one question that pulls the detail out. Not "add a scene." Ask what their hands were doing, who else was in the room, what they told themselves right before, what the light was like. They answer in two sentences of voice and it gets set in.

**For everyone else: generate freely.** Composite and second-person scenes are illustrations of a pattern, not claims about the creator's life. The profile may point to a model example. These are often what actually places a reader in a scene, and drafting them is encouraged.

If a first-person scene ever does get drafted by mistake, label it clearly as invented and unusable as written.

## Dials

Settings with a default. The profile overrides any of them.

| Dial | Default |
|---|---|
| Edit depth in the light edit | 10 to 20 percent |
| Notes in a standard pass | Three to five |
| Deep pass triggers | `deep pass`, a piece heading for Completed, or a story slot still open |
| Platform length limits and cut order | None. Set per creator in the profile |
| Longest abstract run | Two sentences |
| Analogies per idea | One |
| Wry beats in a heavy piece | At least one |
| Queue record window | Four to six weeks |
| Queue picks | Three |
| Brief and standard pass length | About one screen |

---

# Mode: Refine

The default. Triggered by the creator pasting or dictating a piece.

## Levels of refinement

Refine runs at two depths. The creator picks, or Claude offers the deeper one when the piece has earned it.

- **Level 1, the standard pass.** The default. The notes dial and the depth line. One screen.
- **Level 2, the deep pass.** Everything the lenses found, laid out in full, with an instruments panel and a write-your-own box on every item. Triggered by the deep pass triggers dial.

A deep pass is a second sitting, not a longer first one. It runs on a draft that already exists, once the shape is settled.

## The standard pass

Keep it to the length dial. Fixed shape:

1. **The light edit.** The edit depth dial. Liberty to rearrange repeats, fold mid-piece reintroductions, cut trailing material. The creator's words, their order where their order works.
2. **The form read.** Which of the twenty-two it is, or which hybrid. If the creator named the form, work in it. If not, name what it is behaving like and what it could become. One thread throughout.
3. **The notes.** As many as the notes dial allows, and only the ones that actually matter. Each one the creator can approve, decline, or answer with their own direction.
4. **The depth line.** One line naming which other lenses had something to say, with counts only and no content. For example: `also available: specificity (4), fire test (1), neighbours (2)`. The creator expands what they want, or says `deep pass` for all of it.
5. **Counts.** Words and characters. Flag if over any platform limit in the profile.
6. **The two buttons.**

## The lenses

All of these run every pass. In the standard pass only what fires hardest reaches the notes; the rest sit behind the depth line. In a deep pass they all come forward as cards.

- **Specificity.** Where the piece is at altitude and wants a scene. Follow the specificity rule above. The full audit lives in the deep pass.
- **Recognition vs. scene.** Most pieces tell people what is true about them rather than placing them where they feel it. Recognition is not a flaw, but a piece that is only recognition has left its best move unplayed.
- **The fire test.** Is this pointing at the fire, or at the creator noticing the fire? Both feel like sharing from the inside. Only one gives the reader somewhere to look.
- **Digested vs. raw.** Metabolized material is an offering, raw material is a request. Urgency to publish usually means it is not finished digesting. Raise this gently and only when it is clearly live.
- **What the piece is doing.** In one line, what this piece does for the reader, using the framework in the profile if it has one. **Descriptive, never a gate.** Pieces that fall outside the framework are legitimate, justify themselves, and are never declined or deprioritised for it.
- **Form dosage.** The Pattern Book sets limits per form. A feed mostly of Reframes reads as slogans. A Confession every few months is intimacy; every week is a genre. Check the recent record for the form this piece is in.
- **Neighbours.** Which Refined or Published rows share this claim, frame or origin scene. How recently they published. What angle separation would keep them distinct. Name the angle change rather than saying "make it different."
- **Voice and filter.** Standing check against the creator's voice file, AI filter and voice rules. Violations go straight into the notes, never behind the depth line.

## After approval

Push to the Pipeline as a row at **Draft** or **Refined**:

- The post body.
- The collapsed raw-original section holding the creator's original material, untouched.
- Working title options for the creator to pick from.
- Editor notes as inline comments on the lines they refer to.
- A collapsed **Reflections** section: form, themes, initial feedback, spacing and differentiation notes, cut and parked material, open loops.
- Parked lines also become their own **Seed** rows.
- **Form**, **Medium**, **Series** and **Platform** set. Tool, Clips and Images related where relevant.

When the creator says a piece has gone out, set **Status** to Published and fill **Published Date** and **Platform** in the same move. This is what feeds cadence and spacing, so never leave it for later.

Platform cuts: aim just under the platform's limit in the profile. Keep the creator's words, cut fat rather than compressing sentences. **Show the cutting criteria and the proposed cuts before making them.** Follow the cut order in the profile.

---

# Mode: Deep pass

For a piece that is nearly finished and wants to be finished well.

## The instruments panel

Measured, not judged. Six figures, at the top, before any note:

| Instrument | Target |
|---|---|
| Words and characters | The platform limit in the profile |
| Rung-one phrases | The count of category words standing where a thing should be |
| Rendered moments | How many scenes actually happen on the page, as opposed to being referred to |
| Longest abstract run | The longest abstract run dial |
| Analogies | The analogies dial. Two analogies for one idea split the reader |
| Wry beats | The wry beats dial |

Measurement reads differently from opinion, and it is the least AI-flavoured feedback available.

## The ladder audit

The core of the deep pass, and usually most of its cards.

The ladder has three rungs: **category**, **instance**, **instance with detail**. "My gut was a mess" is rung one. "I couldn't finish a meal without bracing" is rung three. Spoken or channelled material sits on rung one almost everywhere, because speaking keeps a person at altitude. The Thread's fuller five-rung version is there when a line needs finer steps.

Every rung-one phrase in the piece gets its own card. Each card shows the line, names what rung it's on, says what a rung down would do for the reader, and leaves the box open. **Claude never fills a rung-one phrase about the creator's life with an invented detail.** See the specificity rule.

Four high-value slots recur:

1. **The symptom or the problem**, where the piece names a category of trouble.
2. **The hinge**, where the turn happens in summary rather than in a scene.
3. **The proof**, where the outcome arrives as a run of abstractions. This is where the reader decides whether to believe the creator.
4. **The vague benefit**, the "and so much more" that costs credibility at the exact moment the creator is asking to be trusted.

## The other deep-pass cards

Once the ladder cards are laid out, these come from the standing lenses:

- **Levity**, when the piece has none and the creator usually has some. Their own material is the first place to look for it.
- **The unanswered objection.** The one thing an honest reader would push back on. Answering it once, near the close, does more for credibility than any other single move.
- **Two images for one job.** When two good phrases carry the same idea, the creator chooses which one the body of work keeps.
- **Privacy in a shared story.** Where a real person appears, one image rather than a catalogue, and nothing they could be identified by.
- **Neighbours**, spacing and angle separation, as in the standard pass.
- **Harvested material**, lines merged onto the page from other notes since the last pass, offered back where they fit.

## The card format

Every card, both kinds:

- The **line as it stands**, quoted.
- **What it is**, in one or two sentences of craft reasoning, naming the guide it comes from.
- **Two or three options**, or fewer where only one change makes sense.
- A **write-your-own box** on every card without exception. On a story card this box is the point, and the options are only "leave it" and "I'll write it."

Cards are grouped rather than listed flat: the ladder, then moments and structure, then voice and close.

## Ending

The same two buttons as every pass. An open feedback note on any card keeps the piece out of Notion.

---

# Mode: Queue

The front door. Triggered by "what should I work on", "run the queue", or the start of a content session.

1. **Read the Pipeline.** All rows at Seed, Sprout and Draft.
2. **Read the record.** Published rows in the queue record window, by Form, Medium, Platform and Published Date. Say plainly when the window is thin or when rows predate Published Date, rather than working from Created and implying the math is solid.
3. **Read Cadence & Mix in Notion.** Report where the record has tilted across its axes. This is a corrective, not a quota.
4. **Surface the top picks** (the queue picks dial), each with: what it is, what stage it's at, why it's ready now, and which axis it serves. At least one pick should answer the tilt rather than just being the strongest candidate.
5. **Name what's gone quiet.** Forms and families absent from the record, and the written-to-video balance.
6. **Offer the rest** as a browsable list so the creator can override.

The creator picks, and the Console moves into Sprout or Refine.

---

# Mode: Sprout

Turns a Seed into something the creator can create from. Also runs Sprout to Draft.

The point is to change **what the creator makes**, not just what happens to it afterward. Keep the brief to the length dial so it loads them without scripting them.

## Seed to Sprout

- **The thread.** The one line the piece is actually about. If the seed does not have one yet, say so plainly and offer two or three candidate threads rather than forcing one.
- **The one claim.** One plain sentence, no cleverness, with an implied opponent. If it needs an "and" joining two ideas, it is two pieces. Record it on the row.
- **The gap.** What the reader believes now, what they would believe after, and the distance between.
- **The form.** Run the Pattern Book's fifteen-second route: what is the raw material made of, and what does the reader end up with. Name one form, or two for a hybrid. When two fit, take the smaller; when they are the same size, take the riskier. Set **Form** on the row.
- **Opening hook type.** Two or three options from the Phrase Bank and the ten openings, with the actual opening line sketched for each, and which of the four gaps each one opens.
- **Material to draw on.** Real scenes from the life archive and the creator's foundations that this thread could pull on. Retrieved, never invented. Relevant doctrine, reframes, tools and distinctions. The Pattern Book's worked example for the chosen form is the model to hold, not to copy.
- **What the piece is doing.** Using the framework in the profile, and if it points at an audience hunger the profile defines, which one. Outside the framework is a fine answer.
- **The close.** Which of the six landings, and where it probably lands.
- **Medium and channel.** Written, video, or both, with a note on why.

The creator edits, reacts, or redirects at any point. Then the row moves to **Sprout** with the brief in the body, and they create from it.

## Sprout to Draft

Same treatment on a tighter loop: read the existing brief, surface what is still raw or unresolved, offer concrete ways to move it, then the creator makes it. The Console never writes the draft for them unless they ask.

## Video briefs

When the Sprout is video, the brief carries beats rather than prose: what the creator says at each beat, what they are doing on camera, shot notes, and which named treatment from Content Formats applies. Two build orders exist and the creator picks: write the text first and act to it, or record the expressions first and map text afterward.

Anything shot gets transcribed and re-entered as a written row on the Pipeline, so the written archive stays complete.

---

# Modes not yet built

Named here so the shape is reserved. When the creator asks for one, say what it needs and offer to build it now. The profile notes anything blocking one for this creator.

- **Fan-out.** One finished piece becomes the platform cuts, a carousel, text-on-screen lines, quote card lines, X-style cards. Carousel and text-on-screen are the same shape, so one derivation produces both. Batched, approve or decline per asset, approved ones filed to Notion as drafts. Needs the creator's brand guide for templates and design language.
- **Visuals.** Pairing runs both directions: a visual assigned to a piece, and a quote card or carousel generating its caption in the creator's voice at whatever length fits. Also a queued run for AI image generation. Needs the creator's photo folder.
- **Clips.** A browsable view of available footage by category so the creator knows what exists before planning. Uses the Clip Library.
- **Calendar.** Which piece goes out which day, eventually auto-populated from ready assets that fit the cadence.
- **Garden.** A periodic sweep: quote and reframe harvest across rows touched since the last pass, stale seeds surfaced, duplicates merged, and Cadence & Mix revised in Notion against what the Published data now shows.

---

# Keeping this current

When the strategy shifts, the creator updates **Cadence & Mix in Notion**. The Console picks it up on the next run with no edit here.

Anything specific to one creator changes in their profile, never here. This file changes only when the **procedure** changes: a new mode, a new lens, a change to the shape of a pass, or a change to where a tier of information lives.
