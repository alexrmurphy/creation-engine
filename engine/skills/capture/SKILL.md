---
name: "capture"
description: "Capture: sort long raw captures (walk transcripts, voice notes, brain dumps, big multi-topic shares) into their homes in the creator's Notion, for the creator whose profile is loaded. It segments the capture, runs a content pass and a foundation pass, checks Notion for what already exists, builds an interactive review deck with a card and a write-your-own box for every item, and files only what the creator approves. Use whenever the creator pastes or uploads a transcript or long dictation holding several ideas, says \"capture\", \"sort this\", \"file this\", \"where does this go\" or \"disseminate this\", or shares a raw dump mixing story ideas, philosophy, audience hungers, life memories, quotes and open questions, even without naming the skill. For shaping a single piece that already has a Pipeline row, use the Content Console instead."
---

# Capture

Capture answers one question: what's in here, and where does each part belong?

Creators often think out loud, and one hour of talking can hold a dozen story ideas, a principle, two audience hungers, a life memory, someone else's quote and three things they want to build. Capture breaks that apart, finds each piece's home in the creator's Notion, shows them the whole placement plan on one review surface, and files what they approve. The Content Console takes over from there: Capture gets things into the Pipeline, the Console makes a single piece good.

This file holds the **procedure**. It is the engine: it works for any creator and never names one. Everything specific to one creator lives in their **profile**.

## Before every run: load the profile

Read the active creator's profile before doing anything else:

- **`profile.md`** - who they are, their voice rules, conventions, doctrine, Pipeline values and personal reference docs.
- **`notion-map.md`** - where each Notion page and database lives for this creator.
- **`capture.md`** - Capture's settings for this creator: the routing map, the formats for each destination, how their foundations are organised, the review deck's look and labels, dial settings and care points.
- Any worked example the profile's `capture.md` points to, when you want to see a full run and the corrections the creator made to it.

In the repo these sit in `profiles/<creator>/`. In an installed setup they are provided as project files alongside this skill. If no profile can be found, say so and stop rather than guessing.

Wherever this file says **the profile**, it means a value from those files. Where the profile does not set a dial, use the default in *Dials* below.

Also read, every run:

- The creator's voice file and AI filter, named in the profile, for the light cleaning of their words.
- The craft library, for naming a Shape when one is visible: *The Pattern Book*, *The Shape of an Idea* and *The Thread*. Until it is packaged with the skill, it is provided as project files.
- `references/foundation-pass.md` and `references/stages.md` in this skill.

Use the Notion connector the profile names. Never write to another creator's workspace.

If the creator says to receive something without analysing it yet, do exactly that: acknowledge, and wait.

## Locked rules

These apply on every run, for every creator.

1. **Nothing is filed before the creator approves it.** That's the heart of the skill. They are the originator and the director; Capture proposes, they decide.
2. **Their words stay theirs.** Clean only fillers ("um", false starts) and obvious transcription slips. Don't rewrite, polish or tighten in the raw original section (the profile names it). Adapted quote lines are marked "(adapted)".
3. **Don't file inferences.** If they didn't say it, it doesn't go in as theirs.
4. **Life facts need dates from the creator.** Never guess a year. File "needs confirming" and ask.
5. **Other people's quotes are unverified** until checked. File them with what you know about the source, and never state a paraphrase as exact wording.
6. **Other people's privacy.** A client's words go in without their name unless the creator says otherwise. Ask before describing a client's material in a post. The profile may add rules about specific people.
7. **Open loops always become rows.** Any decision, naming choice, question or system change goes into Open Loops, not only the chat.
8. **One primary home.** A unit can be several things at once. Give it one home and link the others, so nothing lives in two places.
9. **Every card carries its full context.** A bare question without context doesn't work. Every card has the four options and a write-your-own box, always.
10. **Nothing lives only in the chat.** When the run is done, confirm it.

## Dials

Settings with a default. The profile's `capture.md` overrides any of them.

| Dial | Default |
|---|---|
| Source label on every row and addition | `Capture, [date]` |
| Raw original section heading | `As captured ([date])` |
| Candidates heading on foundation pages | `Candidates from the capture ([date]), for the monthly sweep` |
| Review deck headline | `Your capture, sorted.` |
| Decisions header (first line of the pasted-back block) | `Capture decisions` |
| Review deck look | The neutral theme in `assets/review-deck.html` |
| Review deck section labels and notes | The defaults in `assets/review-deck.html` |
| Artifact icon | `note` |
| Label case in Notion | Title case for multi-word labels |

## The run

### 1. Segment by what each unit is

Read the whole capture first. Then cut it into units by what each one *is*, not where it sits. One riff can yield several units: a story seed, a distinction, an orientation, three outside quotes, an opener, a life fact and a question to Claude can all sit in a single passage.

Also:
- Merge passages that return to the same idea later in the capture. People circle back.
- Drop exact duplicates. Transcripts sometimes repeat a section when it's pasted twice.
- Notice every idea mentioned in passing that could be a deeper dive. Surface these as pathways of discovery, not lost.
- Pull out instructions addressed to Claude ("Claude, when you go through these...") as procedure. They're not content. Apply them to this run, and if they're lasting, propose them as an Open Loop to fold into this skill or the profile.

### 2. Run two passes on every unit

**The content pass** asks: what is this, and where does it live? The profile's routing map lists every kind and its home. The main kinds are story seeds and sprouts, near-finished drafts, audience hungers, life events and through-lines, the creator's quotes, openers and reframes, other people's quotes, tools and methods, open loops, and brand or offer notes.

**The foundation pass** asks: what does this point at underneath? Something told as a story or a riff often carries a principle, an orientation, a distinction, a premise line or a lexicon term. Those are foundational and change slowly, so they don't go straight into the creator's doctrine pages. They go into a candidates section at the bottom of their home page, marked for the monthly deep sweep, where the creator decides what earns a permanent place. Read `references/foundation-pass.md`.

Both passes run on every unit. A single line can be a Sprout, a quote and a principle candidate at once (locked rule 8).

### 3. Set the Stage honestly

Use the stage rule in `references/stages.md`:
- **Seed**: a concept without a forming shape.
- **Sprout**: raw material, even when long, loose and channelled, and even when there's enough for a draft but the shape isn't reviewed and confirmed yet.
- **Draft**: actually drafted. Close to postable after a light edit.
- **Merge**: an existing row gets the new material instead of a new row.

Every piece placed at Sprout carries *everything* the creator said that connects to it, gathered from across the whole capture, in their words.

When they ask for a Draft but the shape isn't confirmed, file at Sprout with all the material gathered and say in one line that it's ready to draft whenever they say.

### 4. Check Notion before proposing anything

Search Notion for each likely match (the idea's key words, its lexicon term, its obvious title). Name the existing match on the card. A match becomes Merge, or a new row with a note on how to keep the angles apart. Spacing notes matter: if two pieces are close, say how far apart to post them.

Check facts against what's filed too. When the capture and Notion disagree, don't pick one. Put the mismatch on the card and ask.

Before writing to any database, fetch its data source once per run to confirm the current property names and option values. The profile's formats are a snapshot; the live schema wins.

### 5. Build the review deck

Copy `assets/review-deck.html` to `/mnt/user-data/outputs/` and fill it:

- `{{TITLE}}`, `{{HEADLINE}}` (short, in the creator's register), `{{STORAGE_KEY}}` (unique per capture) and `{{DECISIONS_HEADER}}`, from the dials.
- `{{FONT_LINK}}` and `{{THEME_CSS}}`, from the deck theme in the profile. If the profile sets none, replace both with nothing and the neutral theme applies.
- `SECTIONS`: keep the six keys and their order. Replace a label or note only where the profile gives one.
- `ITEMS`: replace the examples with the real units.

Each card:
- `id`: short code, section key plus number (F1, H2, P6, L3, Q4, O9).
- `t`: plain-language title.
- `w`: their words, the exact passage (lightly trimmed, no fillers).
- `h`: where it goes, in plain language, with the Stage and Shape for Pipeline items.
- `m`: what's already in Notion, named.
- `n`: your note: the reasoning, the craft suggestion, or the specific question only they can answer.

The four options (Yes, file it / Somewhere else / Maybe later / Cut) and the write-your-own box are built into the template. Cards are grouped in this order: what sits underneath (F), audience hungers (H), pieces for the Pipeline (P), life archive (L), quotes (Q), open loops (O).

Publish it with the Artifact tool, using the profile's icon. In the chat, write a short note: what the deck holds, the facts that need the creator, and any direct question they asked answered in a sentence and pointed to its card. Keep plain-language labels; no guide jargon.

### 6. File what they approve

They paste back the block headed with the decisions header. Then:
- **Yes**: file as proposed.
- **Somewhere else**: follow their note. If the note changes a rule, apply it to every similar item, not just that card, and say so in one line.
- **Maybe later**: file Open Loops anyway so nothing is lost; hold other kinds and list them in the reply.
- **Cut**: don't file.
- Answers in their notes (dates, names, confirmations) go straight into the entries they belong to.

Write order: Pipeline rows (one create call with all new rows), then merges onto existing rows, then candidates sections on the foundation pages, then audience hungers, then the life archive, then quotes, then Open Loops. Every row and addition carries the source label. Formats and property values are in the profile's routing map.

### 7. Close the loop

Reply with a short account of what was filed, grouped the same way as the deck, plus the facts still open (each noted on its row). Ask for the missing facts plainly; when they answer, update the rows. Don't recite everything back; they can see it in Notion.

When a question lands differently than meant, quote their exact words back.

When they're done, confirm nothing lives only in the chat.

---

# Keeping this current

Anything specific to one creator changes in their profile, never here. This file changes only when the **procedure** changes: a new pass, a new locked rule, a change to the deck, or a change to where a kind of thing is filed.
