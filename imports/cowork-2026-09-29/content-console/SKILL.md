---
name: "content-console"
description: "Ryan's Content Console for Dare to Be: pick what to work on next, turn seeds into sprout briefs, and run the standard or deep refinement pass on drafts. Use for any D2B content pass, or when he says console."
---

# Content Console

The system for moving Dare to Be content from seed to published.

This file holds the **procedure**. Everything it depends on lives elsewhere and changes faster than this file does. Read the sources below at run time rather than working from memory of them.

## Where things live

Three tiers. Nothing lives in two of them.

**Tier 1 - Live records. Notion only, queried every run, never cached.**

The **Content Pipeline** (Dare to Be / Content) is the source of truth for every seed, draft and piece. Never hold a parallel copy of a row anywhere.

Statuses: **Seed → Sprout → Draft → Refined → Completed → Published**.

Properties: **Form** (the twenty-two Pattern Book forms), **Medium** (Written, Video, Photo, Carousel, Quote card), **Series** (Permission Slip), Platform, Published Date, Tool, Clips, Images, Notes. There is no Type property; it was retired into Form.

**Tier 2 - Working strategy. Notion canonical, read live.**

These change often and he edits them himself, sometimes from his phone.

- **Content / Cadence & Mix** - the balance strategy. Read at the start of every Queue run and for every neighbours check.
- **Content / Content Formats** - what each format is, plus the named video treatments (ways to shoot any piece).
- **Content / Phrase Bank**, **Reframe Bank**, **Quotes** - harvest destinations and opener patterns. **Quotes / Card-Ready Lines** holds the chosen card versions with their breaks already set.
- **Content / Clip Library**, **The Work / Tools Library**, **The Work / The Potent Person** (the hungers).
- **Life / Ryan's Life** and **Life / Currents** - the life archive. Events by era, and the through-lines across eras. This is what the specificity rule searches.

**Tier 3 - Deep reference. Project docs, already in context.**

Long, stable, needed in full at the start of a pass.

| Doc | What it governs |
|---|---|
| `WRITTEN-VOICE-v4.md` | How he sounds. Non-negotiable. |
| `AI-FILTER-v1.md` | What to keep out. Non-negotiable. |
| `DARE-TO-BE-FOUNDATIONS.md` | Doctrine, lexicon, retired terms, languaging rules. Part I holds the origin scenes. |
| `D2B-COPY-BANK-v1.md` | Card-ready lines, carousel sets and brand copy, with the line-break rules. |

`RYAN-LIFE-STORY-v1.md` and `D2B-CADENCE-AND-MIX-v1.md` in the project are **pointers to their Notion homes, not copies**. Read the Notion version. Keep them as pointers.

Project files, read-only:

- **`The_Pattern_Book.pdf`** - the twenty-two forms, worked, with fifty-three examples drawn from his own material. **The authority on form.** Its fifteen-second route is how a form gets chosen.
- **`The_Thread_Storytelling_and_Content_Craft.pdf`** - the process, the four currencies, the four gaps, ten openings, six landings, the specificity ladder, diagnostics.
- **`The_Shape_of_an_Idea.pdf`** - the machinery for material that is not a story.

**The rule when something new needs a home:** if he would plausibly edit it on his phone, it goes in Notion. If it is long, stable, and needed in full at the start of a pass, it goes in a project doc.

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

## Standing rules

These apply in every mode.

1. **Verbatim is sacred.** His exact language is preserved unless he says otherwise. When in doubt, keep his line and put the alternative in the notes.
2. **No em dashes.** His dash is a spaced hyphen, his pause is an ellipsis.
3. **Draft rhythm.** Mostly short paragraphs with breaks, occasional single lines, short runs of three or four stacked lines. No big blocks. Not everything as single sentences. No clipped-fragment AI rhythm.
4. **One reframe per piece, in a full sentence.** Stacked rhetorical antithesis is not his voice.
5. **Retired terms never appear in new work.** See Foundations Part X.
6. **Never invent his life.** See the specificity rule below. This is the one failure that cannot be undone once published.
7. **`note -` in his feedback** means a question or something needing a bigger rewrite, not an answer. Any open note means the piece is not ready to push. Reflect, then generate a new draft.
8. **Quote harvest is a standing step.** Every pass, flag quotable lines and add them to Content / Quotes / My Quotes, filed by theme, source row noted, marked `(adapted)` if tightened. A line is quotable when it stands alone, carries one claim or one image, sounds like him, and would work on a card. Reframes go to the Reframe Bank, opener patterns to the Phrase Bank.
9. **Flag the bigger question first.** If a piece has a core question larger than refinement, surface it before the light edit. He answers or says proceed.
10. **Every pass ends with two buttons:** build next draft and push to Notion, or review feedback and generate a new draft.
11. **The write-your-own box is never optional.** Every card in every pass carries one. Options are a starting point, not a menu to pick from.
12. **Keep the raw channel.** His original unedited dictation is preserved in a collapsed **As channelled** section on the row, never overwritten by a later pass. It protects verbatim when a later pass wants to reach back, it builds a corpus of pure-him text for voice work, and it makes visible what the Console has actually been changing.
13. **Set line breaks by hand.** Every line that will appear as a card, a slide or on-screen text gets its breaks set by hand, following the line-break rules below. Show it already broken. Never hand him a run-on sentence to break himself.

## Line breaks for cards, carousels and on-screen text

He reads breaks as part of the voice. Set them by hand on every quote card, carousel slide, text-over-clip line and headline. Write them as " / " in notes, and as real line breaks on the page.

1. **Break at the breath, before the next phrase starts.** The break goes *before* the words that open a new phrase (that, which, when, because, the way, back to, to, and, but, as, while), never after them. "A regulated system is one / that can rise as fully as it can settle."
2. **Never strand a small word.** A line never ends on an article or a preposition (the, a, to, of, in, at). It may end on "never" or "not" when the next line names what is refused: "Forcing will never / create the conditions / for true embodied charge."
3. **Even over ragged.** Lines of similar visual length. The longest is at most about twice the shortest, except for a short landing line. "The most reliable doorway / back to yourself / is not a harder discipline. / It is a truer delight."
4. **The landing stands alone.** In a two-part turn, the setup comes first and the landing gets its own line. "A body that can only downshift / is not regulated. / It is subdued."
5. **Parallel lines break in parallel.** "Close the door on your anger / and you lose your access to power. / Close it on your grief / and you lose your tenderness."
6. **Three lines usually, four only when every line is short.** Past four it is a paragraph. Move it to a caption or a carousel.
7. **Breaks first, then type size.** Set the breaks, then size the type so the longest line fits the measure: about 22 to 26 characters on a 4:5 card at display size. A layout must never add a wrap of its own. If a line won't fit at a readable size, re-break it rather than shrinking the type.
8. **Carousel slides and on-screen text follow the same rules**, plus one idea per slide, with the break between the idea's two halves.

When offering options on a card, a different break is a legitimate option on its own. Say what it changes: where the pause lands, or which word stands alone.

Worked examples and the full selects live in Notion at Content / Quotes / Card-Ready Lines and in the project doc `D2B-COPY-BANK-v1.md`.

## The specificity rule

He channels by voice, which keeps him in philosophy and generalities. Scene detail is what gets lost. This is structural, not occasional, so it gets a permanent station in every pass.

**For his own life: retrieve or ask. Never generate.**

- **Retrieve.** When a line sits at altitude, search **Life / Ryan's Life** and **Life / Currents** in Notion, the origin scenes in Foundations Part I, and the Pipeline archive for two or three real moments that would carry it. Name which fits the claim best. He picks.
- **Ask.** When nothing on file fits, ask the one question that pulls the detail out. Not "add a scene." Ask what his hands were doing, who else was in the room, what he told himself right before, what the light was like. He answers in two sentences of voice and it gets set in.

**For everyone else: generate freely.** Composite and second-person scenes are illustrations of a pattern, not claims about his life. The "it's the kid in school who learned to be the class clown" move in Foundations Part 7 is the model. These are often what actually places a reader in a scene, and drafting them is encouraged.

If a first-person scene ever does get drafted by mistake, label it clearly as invented and unusable as written.

---

# Mode: Refine

The default. Triggered by him pasting or dictating a piece.

## Levels of refinement

Refine runs at two depths. He picks, or Claude offers the deeper one when the piece has earned it.

- **Level 1, the standard pass.** The default. Three to five notes and the depth line. One screen.
- **Level 2, the deep pass.** Everything the lenses found, laid out in full, with an instruments panel and a write-your-own box on every item. Triggered by `deep pass`, by a piece heading for Completed, or by anything with a story slot still open.

A deep pass is a second sitting, not a longer first one. It runs on a draft that already exists, once the shape is settled.

## The standard pass

Keep it to roughly one screen. Fixed shape:

1. **The light edit.** 10 to 20 percent. Liberty to rearrange repeats, fold mid-piece reintroductions, cut trailing material. His words, his order where his order works.
2. **The form read.** Which of the twenty-two it is, or which hybrid. If he named the form, work in it. If not, name what it is behaving like and what it could become. One thread throughout.
3. **Three to five notes.** The ones that actually matter. Each one he can approve, decline, or answer with his own direction.
4. **The depth line.** One line naming which other lenses had something to say, with counts only and no content. For example: `also available: specificity (4), fire test (1), neighbours (2)`. He expands what he wants, or says `deep pass` for all of it.
5. **Counts.** Words and characters. Flag if over 2,200 for Instagram.
6. **The two buttons.**

## The lenses

All of these run every pass. In the standard pass only what fires hardest reaches the notes; the rest sit behind the depth line. In a deep pass they all come forward as cards.

- **Specificity.** Where the piece is at altitude and wants a scene. Follow the specificity rule above. The full audit lives in the deep pass.
- **Recognition vs. scene.** His own diagnosis: most pieces tell people what is true about them rather than placing them where they feel it. Recognition is not a flaw, but a piece that is only recognition has left its best move unplayed.
- **The fire test.** Is this pointing at the fire, or at him noticing the fire? Both feel like sharing from the inside. Only one gives the reader somewhere to look.
- **Digested vs. raw.** Metabolized material is an offering, raw material is a request. Urgency to publish usually means it is not finished digesting. Raise this gently and only when it is clearly live.
- **The fish ladder.** What this piece is doing, in one line: awakening the desire, giving a fish, inspiring the fisherman, teaching to fish, or off-spine. **Descriptive, never a gate.** Off-spine pieces are legitimate and justify themselves, and are never declined or deprioritised for being off-spine. See Cadence & Mix, axis 5. (Not to be confused with the specificity ladder, where "rung" means altitude.)
- **Form dosage.** The Pattern Book sets limits per form. A feed mostly of Reframes reads as slogans. A Confession every few months is intimacy; every week is a genre. Check the recent record for the form this piece is in.
- **Neighbours.** Which Refined or Published rows share this claim, frame or origin scene. How recently they published. What angle separation would keep them distinct. Name the angle change rather than saying "make it different."
- **Voice and filter.** Standing check against the voice file and the AI filter. Violations go straight into the notes, never behind the depth line.

## After approval

Push to the Pipeline as a row at **Draft** or **Refined**:

- The post body.
- A collapsed **As channelled** section holding his original dictation, untouched.
- Working title options for him to pick from.
- Editor notes as inline comments on the lines they refer to.
- A collapsed **Reflections** section: form, themes, initial feedback, spacing and differentiation notes, cut and parked material, open loops.
- Parked lines also become their own **Seed** rows.
- **Form**, **Medium**, **Series** and **Platform** set. Tool, Clips and Images related where relevant.

When he says a piece has gone out, set **Status** to Published and fill **Published Date** and **Platform** in the same move. This is what feeds cadence and spacing, so never leave it for later.

Instagram cuts: aim just under 2,200. Keep his words, cut fat rather than compressing sentences. **Show the cutting criteria and the proposed cuts before making them.** Longer pieces get a Facebook version first, the Instagram cut after.

---

# Mode: Deep pass

For a piece that is nearly finished and wants to be finished well.

## The instruments panel

Measured, not judged. Six figures, at the top, before any note:

| Instrument | Target |
|---|---|
| Words and characters | 2,200 for a single version across both platforms |
| Rung-one phrases | The count of category words standing where a thing should be |
| Rendered moments | How many scenes actually happen on the page, as opposed to being referred to |
| Longest abstract run | Two sentences |
| Analogies | One. Two analogies for one idea split the reader |
| Wry beats | At least one in a heavy piece |

Measurement reads differently from opinion, and it is the least AI-flavoured feedback available.

## The ladder audit

The core of the deep pass, and usually most of its cards.

The ladder has three rungs: **category**, **instance**, **instance with detail**. "My gut was a mess" is rung one. "I couldn't finish a meal without bracing" is rung three. Channelled material sits on rung one almost everywhere, because speaking keeps him at altitude. The Thread's fuller five-rung version is there when a line needs finer steps.

Every rung-one phrase in the piece gets its own card. Each card shows the line, names what rung it's on, says what a rung down would do for the reader, and leaves the box open. **Claude never fills a rung-one phrase about his life with an invented detail.** See the specificity rule.

Four high-value slots recur:

1. **The symptom or the problem**, where the piece names a category of trouble.
2. **The hinge**, where the turn happens in summary rather than in a scene.
3. **The proof**, where the outcome arrives as a run of abstractions. This is where the reader decides whether to believe him.
4. **The vague benefit**, the "and so much more" that costs credibility at the exact moment he is asking to be trusted.

## The other deep-pass cards

Once the ladder cards are laid out, these come from the standing lenses:

- **Levity**, when the piece has none and he usually has some. His own material is the first place to look for it.
- **The unanswered objection.** The one thing an honest reader would push back on. Answering it once, near the close, does more for credibility than any other single move.
- **Two images for one job.** When two good phrases carry the same idea, he chooses which one the body of work keeps.
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

The same two buttons as every pass. An open `note -` on any card keeps the piece out of Notion.

---

# Mode: Queue

The front door. Triggered by "what should I work on", "run the queue", or the start of a content session.

1. **Read the Pipeline.** All rows at Seed, Sprout and Draft.
2. **Read the record.** Published rows in the last four to six weeks, by Form, Medium, Platform and Published Date. Say plainly when the window is thin or when rows predate Published Date, rather than working from Created and implying the math is solid.
3. **Read Cadence & Mix in Notion.** Report where the record has tilted across the five axes. This is a corrective, not a quota.
4. **Surface the top three**, each with: what it is, what stage it's at, why it's ready now, and which axis it serves. At least one pick should answer the tilt rather than just being the strongest candidate.
5. **Name what's gone quiet.** Forms and families absent from the record, and the written-to-video balance. Question Held in particular tends to vanish, because an asking piece loses to a more finished one every time it competes.
6. **Offer the rest** as a browsable list so he can override.

He picks, and the Console moves into Sprout or Refine.

---

# Mode: Sprout

Turns a Seed into something he can channel from. Also runs Sprout to Draft.

The point is to change **what he channels**, not just what happens to it afterward. Keep the brief to about one screen so it loads him without scripting him.

## Seed to Sprout

- **The thread.** The one line the piece is actually about. If the seed does not have one yet, say so plainly and offer two or three candidate threads rather than forcing one.
- **The one claim.** One plain sentence, no cleverness, with an implied opponent. If it needs an "and" joining two ideas, it is two pieces. Record it on the row.
- **The gap.** What the reader believes now, what they would believe after, and the distance between.
- **The form.** Run the Pattern Book's fifteen-second route: what is the raw material made of, and what does the reader end up with. Name one form, or two for a hybrid. When two fit, take the smaller; when they are the same size, take the riskier. Set **Form** on the row.
- **Opening hook type.** Two or three options from the Phrase Bank and the ten openings, with the actual opening line sketched for each, and which of the four gaps each one opens.
- **Material to draw on.** Real scenes from Ryan's Life, Currents and Foundations that this thread could pull on. Retrieved, never invented. Relevant doctrine, reframes, tools and distinctions. The Pattern Book's worked example for the chosen form is the model to hold, not to copy.
- **The fish ladder.** What this piece is doing, and if it is awakening desire, which hunger from The Potent Person page it points at. Off-spine is a fine answer.
- **The close.** Which of the six landings, and where it probably lands.
- **Medium and channel.** Written, video, or both, with a note on why.

He edits, reacts, or redirects at any point. Then the row moves to **Sprout** with the brief in the body, and he channels from it.

## Sprout to Draft

Same treatment on a tighter loop: read the existing brief, surface what is still raw or unresolved, offer concrete ways to move it, then he channels. The Console never writes the draft for him unless he asks.

## Video briefs

When the Sprout is video, the brief carries beats rather than prose: what he says at each beat, what he is doing on camera, shot notes, and which named treatment from Content Formats applies. Two build orders exist and he picks: write the text first and act to it, or record the expressions first and map text afterward.

Anything shot gets transcribed and re-entered as a written row on the Pipeline, so the written archive stays complete.

---

# Modes not yet built

Named here so the shape is reserved. When he asks for one, say what it needs and offer to build it now.

- **Fan-out.** One finished piece becomes the Instagram cut, a carousel, text-on-screen lines, quote card lines, X-style cards. Carousel and text-on-screen are the same shape, so one derivation produces both. Batched, approve or decline per asset, approved ones filed to Notion as drafts. Every derived line gets its breaks set by hand (standing rule 13). **Blocked on the brand guide**, in progress, for templates and design language.
- **Visuals.** Pairing runs both directions: a visual assigned to a piece, and a quote card or carousel generating its caption in his voice at whatever length fits. Also a queued run for AI image generation. **Blocked on the photo folder**, in progress.
- **Clips.** A browsable view of available footage by category so he knows what exists before planning. Uses the Clip Library.
- **Calendar.** Which piece goes out which day, eventually auto-populated from ready assets that fit the cadence.
- **Garden.** A periodic sweep: quote and reframe harvest across rows touched since the last pass, stale seeds surfaced, duplicates merged, and Cadence & Mix revised in Notion against what the Published data now shows.

---

# Open decisions

Not settled. Do not resolve these unilaterally; raise them when they become load-bearing.

- **Content categories or pillars.** Something is wanted for cadence beyond Form and Medium, describing what he offers rather than what he concludes. A set of themes named after the claims his pieces make was proposed and rejected as pigeonholing. Not urgent.
- **Claim-level spacing.** Form does not detect whether he has made the same argument twice. The one claim recorded at Sprout is the candidate mechanism: compare claim sentences rather than matching tags. Parked.
- **The unformed rows.** Most Pipeline rows have no Form. They get one as they pass through Sprout or Refine, rather than in a bulk pass.

---

# Keeping this current

When the strategy shifts, update **Cadence & Mix in Notion**. The Console picks it up on the next run with no edit here.

This file changes only when the **procedure** changes: a new mode, a new lens, a change to the shape of a pass, or a change to where a tier of information lives.