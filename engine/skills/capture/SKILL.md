---
name: capture
description: Ryan's Capture skill for Dare to Be, part of the Creation Engine alongside the Content Console. Sorts long raw captures (walk transcripts, voice notes, brain dumps, big multi-topic shares) into their homes in the Dare to Be Notion. It segments the capture, runs a content pass and a foundation pass, checks Notion for what already exists, builds an interactive review deck with a card and a write-your-own box for every item, and files only what he approves. Use this whenever Ryan pastes or uploads a transcript or long dictation holding several ideas, says "capture", "sort this", "file this", "where does this go", "disseminate this", or "run the walk", or shares a raw dump mixing story ideas, philosophy, hungers, life memories, quotes and open questions, even if he doesn't name the skill. For shaping a single piece that already has a Pipeline row, use the Content Console instead.
---

# Capture

Capture answers one question: what's in here, and where does each part belong?

Ryan thinks out loud, often on long walks, and one hour of talking can hold a dozen story ideas, a principle, two hungers, a life memory, a quote from the Tao Te Ching and three things he wants to build. Capture breaks that apart, finds each piece's home in the Dare to Be Notion, shows him the whole placement plan on one review surface, and files what he approves. The Content Console takes over from there: Capture gets things into the Pipeline, the Console makes a single piece good.

Nothing is filed before he approves it. That's the heart of the skill. He is the originator and the director; Capture proposes, he decides.

## Before you start

Read these standing references (they live in the project files and in Notion):
- The written voice file and the AI filter, for the light cleaning of his words.
- The Pattern Book (for naming a Shape when one is visible), The Shape of an Idea, The Thread, and The Architecture of the Teaching.
- `references/routing-map.md` in this skill: every destination, its Notion ID, and the property schemas. Read it every run.
- `references/foundation-pass.md` and `references/stages.md` in this skill.
- `references/worked-example.md` when you want to see a full run and the corrections Ryan made to it.

Use the connector named **Notion** (the Dare to Be workspace), not "NMA Notion".

If Ryan says "receive this, don't analyse yet", do exactly that: acknowledge, and wait.

## The run

### 1. Segment by what each unit is

Read the whole capture first. Then cut it into units by what each one *is*, not where it sits. One riff can yield several units: the sovereignty riff in the first run held a story seed, a distinction, an orientation, three outside quotes, an opener, a life fact and a question to Claude.

Also:
- Merge passages that return to the same idea later in the capture (he circles back; "a little bit more about the cult of sovereignty peace" belongs with the first sovereignty passage).
- Drop exact duplicates. Transcripts sometimes repeat a section when he pastes twice.
- Notice every idea mentioned in passing that could be a deeper dive. He wants these surfaced as pathways of discovery, not lost.
- Pull out instructions addressed to Claude ("Claude, when you go through these...") as procedure. They're not content. Apply them to this run, and if they're lasting, propose them as an Open Loop to fold into this skill.

### 2. Run two passes on every unit

**The content pass** asks: what is this, and where does it live? See the routing map for the full list. The main kinds are story seeds and sprouts, near-finished drafts, hungers, life events and through-lines, his quotes, openers and reframes, other people's quotes, tools and methods, open loops, and brand or offer notes.

**The foundation pass** asks: what does this point at underneath? Ryan asked for this explicitly. Something told as a story or a riff often carries a principle, an orientation, a distinction, a premise line, or a lexicon term. Those are foundational and change slowly, so they don't go straight into The Work. They go into a candidates section at the bottom of their home page, marked for the monthly deep sweep, where he decides what earns a permanent place. Read `references/foundation-pass.md`.

Both passes run on every unit. A single line can be a Sprout, a quote and a principle candidate at once. Give it one primary home and link the others, so nothing lives in two places.

### 3. Set the Stage honestly

Use Ryan's stage rule (full version in `references/stages.md`):
- **Seed**: a concept without a forming shape.
- **Sprout**: raw material, even when long, loose and channelled, and even when there's enough for a draft but the shape isn't reviewed and confirmed yet.
- **Draft**: actually drafted. Close to postable after a light edit.
- **Merge**: an existing row gets the new material instead of a new row.

Every piece placed at Sprout carries *everything* he channelled that connects to it, gathered from across the whole capture, in his words. He was clear about this: bring in absolutely everything connected.

When he asks for a Draft but the shape isn't confirmed, file at Sprout with all the material gathered and say in one line that it's ready to draft whenever he says.

### 4. Check Notion before proposing anything

Search Notion for each likely match (the idea's key words, its lexicon term, its obvious title). Name the existing match on the card. A match becomes Merge, or a new row with a note on how to keep the angles apart. Spacing notes matter: if two pieces are close ("The weight of the mask" and "Authenticity is overrated"), say how far apart to post them.

Check facts against what's filed too. When the capture and Notion disagree (the drum's words, the name of a voice level), don't pick one. Put the mismatch on the card and ask.

### 5. Build the review deck

Copy `assets/review-deck.html` to `/mnt/user-data/outputs/` and fill it: replace `{{TITLE}}`, `{{HEADLINE}}` (short, in his register, e.g. "Your walk, sorted."), `{{STORAGE_KEY}}` (unique per capture) and `{{DECISIONS_HEADER}}` (e.g. "Walk capture decisions"), then replace the example `ITEMS` with the real ones. `SECTIONS` stays as is. Keep the design: it's built on the Dare to Be palette and type (bone paper, deep water, gold hairlines, Fraunces and Work Sans), works on his phone, saves his choices as he goes, and ends with a Copy decisions button that gives him one block to paste back. Each card carries its full context, because a bare question without context doesn't work for him:
- `id`: short code (F1, H2, P6, L3, Q4, O9).
- `t`: plain-language title.
- `w`: his words, the exact passage (lightly trimmed, no fillers).
- `h`: where it goes, in plain language, with the Stage and Shape for Pipeline items.
- `m`: what's already in Notion, named.
- `n`: your note: the reasoning, the craft suggestion, or the specific question only he can answer.

Every card has four options (Yes, file it / Somewhere else / Maybe later / Cut) and a write-your-own box, always. Group cards in this order: what sits underneath, hungers, pieces for the Pipeline, life archive, quotes, open loops.

Publish it with the Artifact tool, favicon 🥁 or another fitting emoji. In the chat, write a short note: what the deck holds, the facts that need him, and any direct question he asked (like "where does sovereignty sit?") answered in a sentence and pointed to its card. Keep plain-language labels; no guide jargon.

### 6. File what he approves

He pastes back "Walk capture decisions". Then:
- **Yes**: file as proposed.
- **Somewhere else**: follow his note. If the note changes a rule (like the Sprout vs. Draft line), apply it to every similar item, not just that card, and say so in one line.
- **Maybe later**: file Open Loops anyway so nothing is lost; hold other kinds and list them in the reply.
- **Cut**: don't file.
- Answers in his notes (dates, names, confirmations) go straight into the entries they belong to.

Write order: Pipeline rows (one create call with all new rows), then merges onto existing rows, then candidates sections on The Work pages, then hungers, then Ryan's Life and Currents, then quotes, then Open Loops. Every row and addition carries its source: "Walk capture, [date]". Formats and property values are in the routing map.

### 7. Close the loop

Reply with a short account of what was filed, grouped the same way as the deck, plus the facts still open (each noted on its row). Ask for the missing facts plainly; when he answers, update the rows. Don't recite everything back; he can see it in Notion.

When he's done, confirm nothing lives only in the chat.

## Care points

- **His words stay his.** Clean only fillers ("um", false starts) and obvious transcription slips ("Dowdy Ching" is the Tao Te Ching, "clawed" is Claude, "reconcolidation" is reconsolidation). Don't rewrite, polish or tighten in As channelled sections. Adapted quote lines are marked "(adapted)".
- **Other people.** A former client's words go in without her name unless he says otherwise. Mentors he wants alluded to are not named in drafts. Ask before describing clients' material in a post.
- **Other people's quotes are unverified** until checked. File them on Quotes from Others with what you know about the source, and never state a paraphrase as exact wording.
- **Life facts need dates from him.** Never guess a year. File "needs confirming" and ask.
- **Don't file inferences.** If he didn't say it, it doesn't go in as his.
- **Open loops always become rows.** Any decision, naming choice, question or system change goes into the Open Loops database, not only the chat.
- **Title case** for multi-word labels in Notion.
