# Routing map

Where each kind of unit goes in the Dare to Be Notion, with IDs and property formats as of 28 Sept 2026.

IDs can change as Ryan restructures. If a write fails, search Notion for the page by name, fetch it, and use what's there. Before writing to a database, fetch its data source once per run to confirm the current option values; Ryan renames properties and options as the system evolves (Form became Shape, Status became Stage).

Connector: **Notion** (Dare to Be workspace). Root page: Dare to Be `3a833a5a60888130b329e39ccb42df9e`.

## Contents
1. The map (kind → home)
2. Content Pipeline
3. The Work pages (foundation candidates)
4. The Potent Person (hungers)
5. Life: Ryan's Life and Currents
6. Quotes, openers, reframes
7. Open Loops
8. Other homes

## 1. The map

| What the unit is | Home | How |
|---|---|---|
| Story idea, concept only | Content Pipeline | New row, Stage Seed |
| Story with a shape showing, or long loose channelled material | Content Pipeline | New row, Stage Sprout, everything connected gathered in |
| Dictated close to postable | Content Pipeline | New row, Stage Draft, light clean only |
| New material for an existing row | That row | Merge: append a dated section; update Stage if it's grown |
| Principle, orientation, distinction, premise line, lexicon term | The Work pages | Candidates section at the bottom, for the monthly sweep |
| A refinement of an existing principle he approves as stated | That page | Filed in the candidates section, marked "filed with your yes" |
| Hunger (a pain or longing in the people he serves) | The Potent Person | Appended under a dated heading |
| Life event (a moment with a when) | Ryan's Life | New row, or update the existing event |
| Through-line across years | Currents | New row |
| His quotable line | My Quotes | Bullet with the source piece in brackets |
| His opener | Phrase Bank | Bullet with the pattern it uses |
| His reframe (from X to Y) | Reframe Bank | Bullet with the source piece |
| Someone else's quote | Quotes from Others | Under "Unverified", with what's known of the source |
| Tool, practice, method | Tools Library (under The Work / What We Do) | Check first; often already there |
| Mechanism or model | Maps & Models | Candidate if new; merge note if it adds wording |
| Brand, audience, why-this-orbit note | Brand / Premise, Orbit & the Offer Path | Appended, dated |
| Decision, question, naming choice, system build, study idea | Open Loops | New row, always |
| Instruction to Claude about process | This skill | Apply now; Open Loop row "fold into Capture" if lasting |
| Old material being mined | Harvest Queue (Dare to Be / Capture) | Only for legacy mining, not fresh captures |

## 2. Content Pipeline

Data source: `2acb329d-1935-4d5a-a051-f302a05ead4b`

Properties:
- `Title` (title)
- `Stage`: Seed, Sprout, Draft, Refined, Ready, Scheduled, Published (video track: Seed, Sprout, Scripted, Prepped to Film, Filmed, Editing, Ready, Scheduled, Published)
- `Shape` (multi-select, JSON array string): the 22 forms from The Pattern Book. Used so far: Distinction, Confession, Turn, Mechanism, Return, Diagnostic, Object, Model, Reframe, Moment, Sequence. Leave empty on a Seed unless the shape is obvious.
- `Medium` (select): e.g. Long Post, Photo with Caption, Essay / Article, Quote Card, Carousel, Text-on-Screen Video. Confirm options from the schema.
- `Pillars` (multi-select, JSON array string): Somatics, Soul, Story, Strategy, Systems
- `Anchor` (checkbox, `__YES__`): a long anchor piece others spin off from
- `Notes` (text): one or two lines: source, what it is, what's open

Row body pattern:
```
## As channelled (walk capture, 27 Sept 2026)
[his words, fillers removed, in order; if gathered from several passages, "### First pass" / "### Second pass"]

## Ties to
- [Existing row](https://app.notion.com/p/<id>): how it relates, spacing note if close
- Foundation candidates this piece carries

## Open before drafting        (or "## Notes for shaping")
- The specific questions only he can answer
- Craft notes: one analogy per piece, where to open, where it lands
```
For a Draft: `## Draft (as dictated, light clean only)` then the text, then `## Notes`.

Merges onto an existing row: `insert_content` at the end with `## As channelled (walk capture, [date])` and `## Ties to (added [date])`; update Stage, Shape and Notes if the row has grown.

## 3. The Work pages

Append at the end with `insert_content`, heading `### Candidates from the walk capture ([date]), for the monthly sweep`:

| Page | ID |
|---|---|
| Principles (What We Hold True) | `3ad33a5a608881ac8253c0c402a4b630` |
| Orientations | `3ad33a5a608881bcab91c46a2f968feb` |
| Distinctions (How We Turn Perception) | `3e333a5a6088813fbae9cc4df844b0de` |
| Maps & Models (How Change Works) | `3ad33a5a608881bc97edd37baec29a63` |
| What We Carry (lexicon candidates) | `3e533a5a6088811b9485f6b5fedfc122` |
| Foundations (premise, creed) | `3ad33a5a608881d2837cf5ebac5e3808` |
| Lexicon term example: The old gravity | `3e833a5a608881f1867fe26b52d3c5be` |

Each candidate: bold name, his exact words in quotes, one line on what it is, links to the Pipeline pieces that carry it.

## 4. The Potent Person

Page `3e333a5a608881d2b199e47b38b9f3fe`. Append `### Hungers from the walk capture ([date])`. Each hunger: bold name, his words, one line of reading. If it deepens an existing hunger, say which ("adds to Hunger 1"). Client-sourced hungers: no name.

## 5. Life

**Ryan's Life** data source `4354d290-2c42-4568-aee9-b8424c72ee0a`
- `Moment` (title), `What happened` (text)
- `date:When:start` / `date:When:end` (ISO dates), `date:When:is_datetime`: 0
- `Date confidence`: Month, Approximate, Needs confirming (confirm options from schema)
- `Era`: formatted like "6 - The Initiated Descent". Fetch the schema for the current list; Ryan's eras have changed before.
- `Place`, `Source` (multi: Life story doc, Facebook, Transcripts), `Told publicly` (checkbox), `Type` (multi: Loss, Practice, Initiation, ...), `Currents` (relation)

Search the data source for existing entries before creating one (Jesse Elder, film school, NMA were all already there). Update `What happened` in full when adding to an entry; keep what was there.

**Currents** data source `0f5a5747-2897-41eb-9559-33b5d34f42a2`
- `Current` (title), `Summary`, `Status` (Live), `Source`; body can list linked Pipeline rows and proof points.

## 6. Quotes

| Page | ID |
|---|---|
| My Quotes | `3e333a5a608881cfb2c6dd1f04af46f8` |
| Phrase Bank (openers) | `3e333a5a60888173ba83fa79c682ce41` |
| Reframe Bank | `3e333a5a6088816eb7abe254a5d892d6` |
| Quotes from Others | `3e333a5a6088813db33df40bc24e962c` |

Append under a dated heading. Mark adapted lines "(adapted)". Others' quotes go under "Unverified ... Check wording and source before use" with what's known (chapter, likely translation, shaky attribution).

## 7. Open Loops

Page: https://app.notion.com/p/053e0024c8014a6483cdfa18f15d0b9a
Data source `f5ef0637-e233-41ac-a68d-d6e4494c643b`
- `Loop` (title), `Context` (the full thought, his words where possible)
- `Kind`: System change, Decision, Question
- `Area`: Content system, Study guides, D2B Foundations, D2B Content, D2B Brand (confirm from schema)
- `Priority`: High, Medium, Low
- `Status`: Open
- `Source`: e.g. "D2B Creations chat: walk capture ([date])"
- `Where it lives`: where the answer will land
- `date:Raised:start`, `date:Raised:is_datetime`: 0

## 8. Other homes

- Brand / Premise, Orbit & the Offer Path: `3e833a5a60888171adcbf9a4fb1ef635`
- Life page: `3c533a5a60888001aa1ff97af050ba1e`
- Media Library (photos and clips, capture ideas and shoot lists): search by name
- Tools Library: search by name (e.g. "The flinch diagnostic" `3e333a5a60888184a77ee8914f1ffc5a`)
