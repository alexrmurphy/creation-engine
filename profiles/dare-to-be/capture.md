# Dare to Be - Capture Settings

Everything Capture needs that is specific to Ryan and Dare to Be. The engine reads this file with `profile.md` and `notion-map.md` at the start of every run. Anything here overrides the engine's defaults.

Page links and data source IDs live in `notion-map.md`; this file names pages by their role there. Pipeline values (Medium, Track, Pillars, Series) live in `profile.md`. Property formats below are a snapshot as of 28 Sept 2026: fetch each data source once per run and trust the live schema over this file. Ryan renames properties and options as the system evolves (Form became Shape, Status became Stage).

## Who and how

- **Capture triggers:** "capture", "sort this", "file this", "where does this go", "disseminate this", "run the walk".
- **What he captures:** long walks, talked out loud. One hour can hold a dozen story ideas, a principle, two hungers, a life memory, a quote from the Tao Te Ching and three things he wants to build.
- **Connector:** the one named **Notion** (the Dare to Be workspace). Never "NMA Notion".
- **Extra reference:** *The Architecture of the Teaching*, which the Dare to Be Notion follows. Read it with the voice file and AI filter listed in `profile.md`.
- **Worked example:** `capture-worked-example.md` in this folder, the first walk capture and the corrections he made to it.

## Dials

| Dial | Setting |
|---|---|
| Source label | `Walk capture, [date]`. On Open Loops: `D2B Creations chat: walk capture ([date])` |
| Raw original section heading | `As channelled (walk capture, [date])` |
| Candidates heading | `Candidates from the walk capture ([date]), for the monthly sweep` |
| Review deck headline | In his register, for example `Your walk, sorted.` |
| Decisions header | `Walk capture decisions` |
| Artifact icon | `drum` |
| Label case in Notion | Title case (engine default) |

## Review deck theme

The Dare to Be palette and type: bone paper, deep water, gold hairlines, Fraunces and Work Sans.

`{{FONT_LINK}}`:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500&family=Work+Sans:wght@400;500;600&display=swap" rel="stylesheet">
```

`{{THEME_CSS}}`:

```css
:root{
  --paper:#EFE6D6; --water:#14263F; --river:#3F7FA6; --clay:#9A5B3C; --gold:#E3A92B; --ember:#B8391E; --ink:#171310;
  --bg:var(--paper); --fg:var(--ink); --soft:#5b5046; --panel:#f7f1e6; --chip:#e4d8c3;
  --rule:var(--gold); --accent:var(--water); --mark:var(--clay); --done:var(--river); --focus:var(--gold);
  --font-display:"Fraunces",Georgia,serif;
  --font-body:"Work Sans",system-ui,-apple-system,"Segoe UI",sans-serif;
}
@media (prefers-color-scheme:dark){
  :root:not([data-theme="light"]){ --bg:var(--water); --fg:var(--paper); --soft:#b9c3cf; --panel:#1b3150; --chip:#243d60; --rule:var(--gold); --accent:var(--gold); --mark:var(--clay); --done:var(--river); --focus:var(--gold); }
}
:root[data-theme="dark"]{ --bg:var(--water); --fg:var(--paper); --soft:#b9c3cf; --panel:#1b3150; --chip:#243d60; --rule:var(--gold); --accent:var(--gold); --mark:var(--clay); --done:var(--river); --focus:var(--gold); }
```

### Section labels and notes

| Key | Label | Note |
|---|---|---|
| F | What sits underneath | Lines that point at something you hold true. "Yes" here sends them to a holding list for the monthly deep sweep, not straight into The Work, so the ground stays distilled. |
| H | Hungers | For The Potent Person page. |
| P | (engine default) | (engine default) |
| L | (engine default) | For Ryan's Life and Currents. Several need a date only you have. |
| Q | (engine default) | Your lines go to My Quotes, the Phrase Bank or the Reframe Bank. Other people's lines get checked before we use them. |
| O | (engine default) | (engine default) |

## How the foundations are organised

The Work holds five groups, following *The Architecture of the Teaching*. The foundation pass maps each kind to a page:

| Group | Kinds | Page (notion-map role) |
|---|---|---|
| **What We Hold True** | Premise, creed | Foundations: premise, creed |
| | Principles | Foundations: principles |
| | Orientations | Foundations: orientations |
| **How We Turn Perception** | Distinctions | Foundations: distinctions |
| | Reframes | Reframe Bank |
| **How Change Works** | Maps, models, mechanisms | Foundations: maps, models, mechanisms |
| **What We Do** | Tools, practices, methods | Tools Library |
| **What We Carry** | Lexicon, images, metaphors | Foundations: lexicon, images |

Audience hungers go to **The Potent Person**. Brand premises (why a soul mentor talks about AI) go to **Brand premise**.

His metal-element principle is why the ground stays distilled: refine, distil, let go. The monthly deep sweep is run by the Gardener.

Examples from his own material, for recognising the kinds: a premise ("I'm here to help people change how they behave, not just how they think"); a principle ("joy is a prerequisite, not a reward"); an orientation ("individuated unity"); distinctions (maintenance vs. creation; egoic vs. surrendered sovereignty); a mechanism (why a breakthrough fades: the predictive pattern isn't updated by the lived experience); tools (the flinch diagnostic; catharsis's three steps); lexicon (unguarded, the old gravity, the bodyguard); an image (two suns). A borrowed phrase to watch: "Power vs. force" is also a book title.

## Routing map

| What the unit is | Home (notion-map role) | How |
|---|---|---|
| Story idea, concept only | Content Pipeline | New row, Stage Seed |
| Story with a shape showing, or long loose channelled material | Content Pipeline | New row, Stage Sprout, everything connected gathered in |
| Dictated close to postable | Content Pipeline | New row, Stage Draft, light clean only |
| New material for an existing row | That row | Merge: append a dated section; update Stage if it's grown |
| Principle, orientation, distinction, premise line, lexicon term | The foundation page for its kind (above) | Candidates section at the bottom, for the monthly sweep |
| A refinement of an existing principle he approves as stated | That page | Filed in the candidates section, marked "filed with your yes" |
| Hunger (a pain or longing in the people he serves) | Doctrine: audience hungers (The Potent Person) | Appended under a dated heading |
| Life event (a moment with a when) | Life archive: events by era (Ryan's Life) | New row, or update the existing event |
| Through-line across years | Life archive: through-lines (Currents) | New row |
| His quotable line | Quotes: his own lines (My Quotes) | Bullet with the source piece in brackets |
| His opener | Phrase Bank | Bullet with the pattern it uses |
| His reframe (from X to Y) | Reframe Bank | Bullet with the source piece |
| Someone else's quote | Quotes: other people's (Quotes from Others) | Under "Unverified", with what's known of the source |
| Tool, practice, method | Tools Library | Check first; often already there. Example: "The flinch diagnostic" |
| Mechanism or model | Foundations: maps, models, mechanisms | Candidate if new; merge note if it adds wording |
| Brand, audience, why-this-orbit note | Brand premise | Appended, dated |
| Photo or clip idea, shoot list | Media Library | Search by name |
| Decision, question, naming choice, system build, study idea | Open Loops | New row, always |
| Instruction to Claude about process | Capture, or this profile | Apply now; Open Loop row "fold into Capture" if lasting |
| Old material being mined | Legacy mining queue (Harvest Queue) | Only for legacy mining, not fresh captures |

## Formats

### Content Pipeline

Properties (snapshot):
- `Title` (title)
- `Stage`: see the engine's stages.
- `Shape` (multi-select, JSON array string): the twenty-two shapes. Leave empty on a Seed unless the shape is obvious.
- `Medium` (select), `Pillars` (multi-select, JSON array string): values in `profile.md`.
- `Anchor` (checkbox, `__YES__`): a long anchor piece others spin off from.
- `Notes` (text): one or two lines: source, what it is, what's open.

Row body:
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

### Foundation pages

Append at the end with `insert_content`, under the candidates heading. Each candidate: bold name, his exact words in quotes, one line on what it is, links to the Pipeline pieces that carry it.

### The Potent Person

Append `### Hungers from the walk capture ([date])`. Each hunger: bold name, his words, one line of reading. If it deepens an existing hunger, say which ("adds to Hunger 1"). Client-sourced hungers: no name.

### Ryan's Life

- `Moment` (title), `What happened` (text)
- `date:When:start` / `date:When:end` (ISO dates), `date:When:is_datetime`: 0
- `Date confidence`: Month, Approximate, Needs confirming
- `Era`: formatted like "6 - The Initiated Descent". Fetch the schema for the current list; his eras have changed before.
- `Place`, `Source` (multi: Life story doc, Facebook, Transcripts), `Told publicly` (checkbox), `Type` (multi: Loss, Practice, Initiation, ...), `Currents` (relation)

Search the data source for existing entries before creating one (Jesse Elder, film school and NMA were all already there). Update `What happened` in full when adding to an entry; keep what was there.

### Currents

`Current` (title), `Summary`, `Status` (Live), `Source`; the body can list linked Pipeline rows and proof points.

### Quotes, openers, reframes

Append under a dated heading. Mark adapted lines "(adapted)". Others' quotes go under "Unverified ... Check wording and source before use" with what's known (chapter, likely translation, shaky attribution).

### Open Loops

- `Loop` (title), `Context` (the full thought, his words where possible)
- `Kind`: System change, Decision, Question
- `Area`: Content system, Study guides, D2B Foundations, D2B Content, D2B Brand
- `Priority`: High, Medium, Low
- `Status`: Open
- `Source`: the Open Loops source label
- `Where it lives`: where the answer will land
- `date:Raised:start`, `date:Raised:is_datetime`: 0

## Stage examples

From the first walk capture (27 Sept 2026), where the stage rule was set:

- **Seed:** The knowledge base. "More of just a concept or a thing I'm doing."
- **Sprout:** I've officially left the cult of sovereignty (two full passes of channelled material); AI: more yourself or less (loose and channelling); The drum and The urn (the Object shape is visible).
- **Draft:** Confession: almost everything I share is touched by AI.
- **Merge:** The old gravity went from Seed to Sprout when the walk gave it a shape.

He was clear about Sprouts: fine for loose channelled pieces "as long as we're bringing in absolutely everything that's connected".

## Care points

- **Transcription slips he makes often:** "Dowdy Ching" is the Tao Te Ching, "clawed" is Claude, "reconcolidation" is reconsolidation.
- **Mentors** he wants alluded to are not named in drafts.
- **A former client's words** go in without her name unless he says otherwise.
- **Open loops he cut on the first run** because he's handling them elsewhere: text-on-screen videos, feedback hub, manager agents, Qigong naming, architecture restructure, engine naming, maps vs. models. Don't re-propose them from later captures unless he raises them again.
