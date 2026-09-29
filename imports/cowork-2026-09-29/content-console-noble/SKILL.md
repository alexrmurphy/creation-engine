---
name: "content-console-noble"
description: "Content Console, Noble Edition: find, draft, sprout and refine Noble Movement Academy content in David's voice from the NMA corpus, and file it in the NMA Content Pipeline. Use for any NMA content pass."
---

# Content Console · Noble Edition

The system for moving Noble Movement Academy content from seed to published, built from David's own material.

This file holds the **procedure**. Everything NMA-specific (IDs, registers, channel specs, story territories, care rules) lives in the project doc **`claude/CONTENT_PROFILE.md`**, which changes faster than this file. **Read it in full at the start of every run.** When this file and the profile disagree on a fact about NMA, the profile wins. When they disagree on procedure, this file wins.

The Dare to Be Content Console is a separate skill with a different originator. Never mix the two: no D2B voice file, no D2B filter protections, no D2B Notion.

## Who is who

- **David Beaudry** is the Originator. Every piece speaks in his first person unless the register says otherwise.
- **Ryan** is the Director. He picks, approves, redirects, and relays questions to David. He is not the voice.
- Because the Director is not the Originator, **the Console drafts by default**. That is the main difference from the D2B Console, where Ryan channels and the Console refines.
- Anything representing David's teaching or voice is reviewed by David or Ryan before it goes out.

## Where things live

**Tier 1 · Live records (NMA Notion, via the `NMA Notion` connector only, never the plain `Notion` connector).** The Content Pipeline is the source of truth for every piece. Statuses: **Seed → Sprout → Draft → Refined → Ready → Scheduled → Published**. Property names, IDs and the row-body pattern are in the profile §2. Fetch the data source schema before the first write in a run.

**Tier 2 · Working strategy (NMA Notion).** Cadence & Mix and the quote/reframe banks are not built yet. Use the profile's defaults and say so.

**Tier 3 · Deep reference (project docs, read at the start of a pass):**
- `claude/CONTENT_PROFILE.md` (read every run)
- `DAI_FILTER.md`: the filter. Pass order §11, register table §10, fabrication §7, protections §8, rate limits §9. Non-negotiable.
- `VOICE_WRITTEN.md` (email, posts, long-form) or `VOICE_SPOKEN.md` (Reels, video, guided scripts), plus `VOICE_APPENDIX.md`. Load the one the register needs.
- `11_CLAIMS_AUDIT.md` and `10_RESEARCH_FOUNDATION.md` for anything touching the body, breath, nervous system or health.
- `Noble_30_Avatar_Persona_v2_July2026.docx` when the piece serves Noble 30.
- `12_FRAMING_OPTIONS.md` for positioning and locked anchors.
- Craft, read-only: `craft/THE_PATTERN_BOOK.md` (the authority on form), `craft/THE_THREAD.md` (thread, gaps, openings, middles, landings), `craft/THE_SHAPE_OF_AN_IDEA.md` (concept pieces, analogy, tools).

**The corpus (Ryan's Mac, through `device_bash`).** `NMA Knowledge Base/` holds ~11.8M words: 1,083 class transcripts, 112 Fathom calls with David, 520 emails, ~1,480 Drive pages, with a search index and a 1,268-term taxonomy. Manual: `search/README.md`. If the Mac can't be reached, say so plainly and stop. Never write David's content from memory instead.

```
cd "$HOME/mnt/NMA/NMA Knowledge Base/scripts"
python3 nma_search.py --terms "strength"                        # find taxonomy term ids
python3 nma_pull.py --topic <id1,id2> --audience cold --per 6 --out <slug>   # source pack -> search/packs/<slug>.md
python3 nma_search.py --topic <id> --verdict david,written --until 2023 --chars 900
python3 nma_search.py '"exact phrase"' --mode exact --count
python3 find_pairings.py --topic <teaching id>                  # stories that carry a teaching
```

For surrounding context on a passage, read neighbouring chunk ids in `~/nma_search_build/nma_search.db` (table `chunks`). A student question's answer is usually the next one or two passages.

## Standing rules

These apply in every mode.

1. **Name the register first** (DAI §10): School Email, Fitness-Facing, Long-Form Written, or Spoken / Video. It decides which voice file and which protections apply.
2. **Retrieve or ask. Never generate David's life.** No memory, scene, prop, sensation, feeling, number, date, name, quote or "people ask me…" framing that isn't in a passage. What can't be sourced becomes `[NEEDS: …]` for David. A draft with three brackets is correct. A draft with three invented specifics is broken.
3. **Source era.** Build from classes and Drive (2014 to 2023) and emails 2017 to 2023. Use 2024+ emails only to check what has already gone out, never as voice evidence or story material, because their authorship may be team or AI-assisted.
4. **Who is speaking.** `not_david`, `dialogue`, `survey` and `testimonial` passages are the voice of the customer. Use their language for pains and desires, strip names, and never quote them as David. `written_ryan` is Ryan's, not David's. Speaker labels in class transcripts are window-level, so read the passage before quoting it as David.
5. **Privacy and care.** Journals stay hidden unless David has OK'd them. No identifiable students or clients, no client medical outcomes, family as one image each, children never named. Book material and suicide follow the profile's care rules (§5).
6. **Claims.** Tradition is labelled as tradition in one clause. Anything the claims audit flags is left out or bounded. Passages tagged `reuse_safety.health_claim` get checked before use.
7. **David's punctuation.** Zero em dashes, zero semicolons, the ellipsis as his pause mark, exclamation marks live in email.
8. **Measure, don't eyeball** (see Checks below).
9. **One offer line at most,** set apart from the emotional close. Unlocked offer details (price, dates, program pieces still being decided) go in `[NEEDS]`.
10. **Every card carries a write-your-own box.** Options are a starting point, not a menu.
11. **Line breaks by hand** for cards, carousels and on-screen text: break before the next phrase, never strand a small word, keep lines even, let the landing stand alone, three lines usually. Show it already broken.
12. **Quote harvest.** Flag quotable lines of David's (verbatim, with source) in the row's Reflections until the banks exist.
13. **Every pass ends with two buttons:** push to the Pipeline, or take feedback and generate a new draft. An open `note -` keeps a piece out of Notion.

## The twenty-two forms

From The Pattern Book, grouped by where the raw material starts.

| Family | Forms |
|---|---|
| It starts in a moment | Moment, Object, Return, Failed Attempt, Confession, Observation |
| It starts in a change of mind | Turn, Correction, Reframe, Question Held |
| It starts in a structure you can see | Distinction, Definition, Model, Taxonomy, Mechanism, Sequence |
| It starts in what you want them to do | Tool, Diagnostic, Permission, Constraint |
| It starts with the reader | Direct Address, Composite |

Choose with the fifteen-second route: what is the material made of, and what does the reader end up holding? When two fit, take the smaller; when they're the same size, take the riskier. Name both parts of a hybrid before drafting. For concept pieces, also name the momentum engine (Shape of an Idea §5).

---

# Mode: Draft

The default for "write an email about X", "three emails on strength for Noble 30", "a post on grief". The Console writes; Ryan and David approve.

1. **Brief.** Confirm what's missing: the piece type and channel, the audience (maps to `--audience`), what it serves (Noble 30, Entry Experience, General List…), how many versions. If Ryan asks for several, each version uses a different form, from different families where possible, and at least one leads with David's own story when he asks for that.
2. **Pull.** Find term ids with `--terms`, then run `nma_pull.py` for the pack. Read the whole pack. Then go deeper where it points:
   - linked life episodes (`--topic life_episode.… --verdict david,written,mixed`), preferring written-safe territories (depression, the athletic past, the gym, teachers) for written pieces
   - older material first (`--until 2023`)
   - the claims audit for anything physiological
   - what already went out on this theme (recent emails), so the new piece doesn't repeat a story the list just heard
3. **Shape.** For each version write a four-line plan: form, one claim (one plain sentence with an implied opponent), gap type, landing type. Pick the material that fits the claim. Leave the rest.
4. **Draft** in the register's rhythm, using his opener habits as the profile describes them (openers are mostly statements, scenes and admissions; questions are the minority), his ask (*I invite you to*, reply), and his sign-offs.
5. **Checks.** Run all seven (below) and fix what fails.
6. **Deliver** each version with: subject options (three), the draft, then **Source** (every passage used, with timestamp links), **Needs David**, and **Reflections** (what was left out and why, send order, parked lines). Save the set beside its pack in `search/packs/<slug>_versions.md` and show the drafts in chat.
7. **Two buttons.** On approval, file each version as its own Pipeline row (see After approval).

## Checks (run on every draft, show the results)

1. **Form named** and the gap the opener creates is the one the piece pays back.
2. **Source era** respected.
3. **Fabrication sweep, line by line.** Every detail traces to a passage. The usual slips are interior lines (*effort was the only fire I knew*), invented props (*puddles, rubber floors*), and invented framings (*people always ask me…*).
4. **Measurement.** Run this on the draft text:

```python
import re, statistics as st
def check(body):
    body = re.sub(r'\[NEEDS:[^\]]*\]', '', body)
    prose = ' '.join(l for l in body.split('\n') if l.strip() and not re.match(r'^\d\.|^(Hey|Hi|Warriors|With Love|Blessings|In Service|David|~ DB)', l))
    L = [len(s.split()) for s in re.split(r'(?<=[.!?])\s+', prose) if s.strip()]
    flags = {p: re.findall(p, body, re.I) for p in [r"\bnot\b.{0,40}\bbut\b", r"\bit'?s not\b", r"honest", r"\bhere'?s\b", r"truly|deeply|profound|transform|unlock|empower|delve|journey"]}
    return dict(words=len(body.split()), median=st.median(L), sd=round(st.pstdev(L),1), emdash=body.count('—'), semicolons=body.count(';'), flags={k:v for k,v in flags.items() if v})
```

   Targets: email median near 14 words per sentence with real spread (sd 6 or more), a scene-led Moment may run a little shorter; em dashes 0; semicolons 0; no "not X but Y"; no three bare imperatives in a row; no throat-clearing.
5. **Claims** labelled or bounded.
6. **Offer line** single and set apart; unlocked details bracketed.
7. **Deliverables** complete: Source, Needs David, Reflections.

---

# Mode: Find

Triggered by "find topics", "surface ideas", "pair a story with…", "for the Thomas door", "warm up the list for Noble 30", "what hasn't he talked about". The ask patterns are in the profile §7.

1. Read the Pipeline record (what's in motion and what went out recently).
2. Pull candidates from the corpus: `find_pairings.py` for story ↔ teaching pairings, `nma_pull.py` for a theme, `search/SERIES_POTENTIAL.md` for multi-part arcs, the `faq.*`, `contrarian.*`, `proof.*` and `micro_practice.*` terms for angles.
3. Build a review deck of cards (the profile's deck design; the Round One pairings deck is the reference build). Each card holds the pairing, the one-line claim, the suggested form, David's best two lines with sources, and a write-your-own box.
4. The default mix: one for the current campaign, one from a written-safe territory, one suited to a Reel, no more than two from one territory.
5. Approved cards become **Seed** rows (or **Sprout** rows if the shape is visible), with passages in Source.

---

# Mode: Sprout

Turns a Seed into a brief the Console (or David) can draft from. About one screen:

- **The thread** and **the one claim.**
- **The gap:** what the reader believes now, what they'd believe after.
- **The form** by the fifteen-second route, set on the row.
- **Opening options:** two or three, each with the actual first line and its gap type.
- **Material:** real passages from the pack, retrieved, never invented. Life moments from the life map with their sources.
- **The close:** which of the six landings.
- **Register, medium and channel**, with a note on why.

The row moves to **Sprout** with the brief in its body.

---

# Mode: Refine

Triggered by pasting a draft (David's, Ryan's, or an earlier Console draft).

**Level 1, the standard pass (one screen):** the light edit (10 to 20 percent), the form read, three to five notes that matter most, the depth line with counts only (`also available: specificity (3), claims (1), neighbours (2)`), word counts, the two buttons.

**Level 2, the deep pass:** the instruments panel first (words, rung-one phrases, rendered moments, longest abstract run, analogies, the measurement check), then every card with options and a write-your-own box.

**Lenses, every pass:**
- **Voice and filter.** Measured against the register's voice file and the DAI filter. Violations go straight into the notes.
- **Provenance.** Raw David gets the lightest touch (DAI §0.1). If the draft is David's own writing, keep his lines and flag rather than cut.
- **Specificity.** Where the piece sits at altitude, retrieve two or three real moments from the life map or the pack that would carry it. If none fit, write the question for David.
- **Claims.** Anything physiological checked against the claims audit.
- **Voice of the customer.** Any student line being used as David's gets flagged.
- **Reuse safety.** Dated references, prices, retired programs, identifiable students (the `reuse_safety.*` tags).
- **Neighbours.** Pipeline rows and recent sends sharing this claim or story. Name the angle change.
- **Readiness.** Does the language fit the audience? Practitioner jargon in cold copy gets a note.

---

# Mode: Queue

Triggered by "what should I work on" or the start of a content session.

1. Read Pipeline rows at Seed, Sprout, Draft and Refined.
2. Read Published rows from the last four to six weeks. Say plainly when the record is thin.
3. Apply the profile's cadence defaults (no more than two in a row from one life territory; at least one in four pure teaching) until Cadence & Mix exists in Notion.
4. Surface the top three (what it is, stage, why now, what it serves), with at least one that answers a tilt. Name what's gone quiet.
5. Offer the rest as a list.

---

# After approval

Push to the NMA Content Pipeline, one row per piece:

- **Properties:** Title, Stage (Draft or Refined), Form, Channels, Register, Life Story territory, Topic, Serves, Needs David (checked if any bracket is open), Sources.
- **Body,** in the profile's row pattern: Brief, Email (subject options, then body), Facebook, Instagram, Source (collapsed), Needs David, Reflections (collapsed).
- When Ryan says a piece went out, set Stage to Published and fill Published Date in the same move.

---

# Modes not yet built

Say what each needs and offer to build it when asked.

- **Fan-out:** one approved email becomes the Facebook post, the Instagram caption and carousel, and a Reel beat sheet in the spoken register.
- **Clips:** the `clip.*` terms already find stand-alone 30 to 120 second passages; a browsable list with timestamp links.
- **Calendar and Garden:** once there are twenty or so Pipeline rows.

# Keeping this current

NMA facts, IDs, channel specs and care rules change in `claude/CONTENT_PROFILE.md`, and the Console picks them up next run. This file changes only when the procedure changes.