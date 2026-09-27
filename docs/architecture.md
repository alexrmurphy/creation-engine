# Architecture

How the Creation Engine is organised: what belongs to the engine, what belongs to a creator's profile, and where each thing is stored.

This is a living spec. It changes when the structure changes, and every change is logged in `CHANGELOG.md`.

## Two separate questions

Every piece of the system answers two questions, and they are independent of each other.

1. **Whose is it?** Engine (any creator could use it) or profile (specific to one creator). See *The four buckets*.
2. **Where is it stored?** Notion, the repo, or the installed skill. See *Where things are stored*.

Engine vs profile is decided by whether another creator would use it, not by who invented it. A framework Ryan created still belongs to the engine if any creator could apply it.

## The four buckets

| Bucket | What it is | Creator can change it? | Belongs to |
|---|---|---|---|
| **1. Locked rules** | Integrity. What makes this the system. | No | Engine |
| **2. Craft library** | The wisdom the engine thinks with: forms, openings, landings, gaps, the specificity ladder, lenses such as the fire test. | Adds only (see below) | Engine |
| **3. Dials** | Preferences with a sensible default, such as edit depth, notes per pass, platform lengths. | Yes, set in the profile | Engine sets the default, profile overrides |
| **4. Profile content** | What only this creator has: identity, voice rules, lexicon, life archive, doctrine, Notion page map, pillars. | Entirely theirs | Profile |

Voice rules (for example, no em dashes) are profile content, not locked rules. They describe how one creator sounds.

**Status of the bucket list:** which rules are locked and which are dials is provisional. It will be settled closer to the first client integration, around December 2026. Until then, classify new items as best fits and mark them provisional when unsure.

### Craft library additions

The craft library is **canonical**: one base, the same for every creator. The engine is meant to be smart on its own, so foundational wisdom (books, frameworks, craft knowledge) is built into it rather than supplied by each creator. Creators may be given readable versions to study, as "what the engine is informed by".

Creators study the craft library as part of working with the system. Advanced creators may add their own entries, which live in their profile (a `craft-additions/` folder inside it) and sit alongside the engine library. The engine library is changed only by the engine owner. A creator's addition can be promoted into the engine library if it proves useful for everyone.

## Taxonomy

The structure is shared across every install, so each creator's Notion workspace is built from the same template. The values of some fields are shared too; others belong to the creator.

| Field | Values |
|---|---|
| Status (Seed → Sprout → Draft → Refined → Completed → Published) | Shared. The procedure depends on these stages. |
| Form (the twenty-two forms) | Shared. Comes from the craft library. |
| Medium (for example written, video, carousel, text on screen, quote card) | Shared. The engine names them; creators use the same names. |
| Content pillars | Per creator. The engine defines that pillars exist; the profile lists them. |
| Series | Per creator. |
| Hungers and similar doctrine | Per creator. |

The field definitions live in this repo (the schema map, task T0.5). Each creator's Notion database is built from that definition, and the skill reads the same definition, so all three stay in step.

## Where things are stored

| Kind of thing | Stored in | How Claude reads it |
|---|---|---|
| Live records (Pipeline rows) | Creator's Notion | Queried fresh every run, never copied |
| Working strategy the creator edits often (Cadence & Mix, banks, life archive) | Creator's Notion | Read live |
| Procedure and locked rules | `SKILL.md` in this repo | Loaded every run |
| Craft library | Files packaged with the skill, canonical in this repo | Opened when a pass needs them |
| Dials, voice, doctrine, Notion page map | The creator's profile | Loaded with the skill |
| Long personal reference docs (voice file, foundations, life story) | The creator's project, snapshotted here for history | Loaded at the start of a pass |

### Why the craft library travels with the skill

Project files in the Claude app belong to one project. A skill is installed once and is available in every project, and it can carry supporting files. Packaging the craft library with the skill means the same library is available wherever the skill runs, and updating it means editing this repo and reinstalling the skill.

A client install is therefore: the skill (carrying the craft library) plus a profile folder they fill in, with their personal reference docs in their own project or local folder.

## Planned layout

Proposed; built out as the related tasks happen.

```
engine/
  skills/
    content-console/
      SKILL.md            procedure, locked rules, craft essentials, dial defaults
      craft/              craft library as Markdown (planned, T1.5)
profiles/
  dare-to-be/
    profile.md            who, voice rules, conventions, doctrine, dial settings
    notion-map.md         where each Notion page and database lives
    craft-examples/       Dare to Be worked examples taken out of the craft books (planned, T1.5)
    craft-additions/      Dare to Be's own additions to the craft library, if any
    snapshots/            dated copies of Notion reference docs (planned, T1.3)
schemas/                  field definitions (T0.5) and glossary (T0.4)
docs/
  architecture.md         this spec
  decisions/              one short note per open or settled design decision
```

## Planned work

- **Craft library to Markdown (T1.5).** Convert *The Pattern Book*, *The Thread* and *The Shape of an Idea* into Markdown under `engine/skills/content-console/craft/`, with Dare to Be examples moved to `profiles/dare-to-be/craft-examples/`. Then write neutral examples drawn from many kinds of businesses so the library stands on its own for other creators, before the Feed a Brain pilot (T3.2). Nicer PDFs for creators to study can be produced from the Markdown later.
- **Locked vs dials.** Settle which rules creators can adjust, around December 2026.
