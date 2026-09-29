# Dare to Be - Gardener Settings

The Gardener profile for Ryan's Dare to Be Notion. The engine (`engine/skills/gardener/SKILL.md`) holds the procedure. This file holds the facts about this workspace. Keep workspace changes here, and keep procedure changes in the engine.

## Owner

- **Owner:** Ryan (he/him). Label OWNER items as **RYAN** in walker findings and in reports.
- **Context:** Part of the Creation Engine (Skill Map #7). Sibling to Capture and the Content Console.

## Connector

- Use only the D2B Notion tools (`mcp__Notion__*`).
- **Never** use `mcp__NMA_Notion__*`. That is Noble Movement Academy's workspace. Pass this rule to every walker.

## Where things live

- Dare to Be root: https://app.notion.com/p/3a833a5a60888130b329e39ccb42df9e
- **Gardening Log**: https://app.notion.com/p/5ba1c10bf9ae4642886b6575dd8f5bcd (collection://a652c430-7296-4b9a-87cc-0860bb4cbfe8), under Systems & Infrastructure.
  - Properties: Pass, Date, Kind (Weekly Tend / Monthly Deep), Status, Findings, Applied, Loops Closed, Loops Added, Carried Forward, Notes.
  - Status values: Walked → **In Review** (report written) → **Applied**.
- **Open Loops**: collection://f5ef0637-e233-41ac-a68d-d6e4494c643b
  - Fields to fill when logging: Area, Kind, Priority, Raised, Source ("Gardening pass, <date>"), Where it lives, Context.
  - Status values: Open / Ready to decide / Decided / Dropped. When closing, write **Decision**.
  - The location field for the stale-path check in bed 6 is **Where it lives**.
- **Content Pipeline** (the main working database): collection://2acb329d-1935-4d5a-a051-f302a05ead4b
- **Media Library**: collection://e71b57cb-584d-4df4-afa7-f5a16497fdc9 (photos and clips; it replaced the Image and Clip Libraries on Sept 27).
- **Writings**: https://app.notion.com/p/d221d7a037344f82a666eb42736c124a (collection://93b797c9-6e14-4f17-9506-53c3f2586bf2), under the root. Old posts and passages are kept whole here. It is the candidate exit destination, and harvest source texts live here too.
- **Zones:**
  - Capture (the front door: Inbox + Harvest Queue)
  - Ground
  - The Work, in five groups: What We Hold True, How We Turn Perception, How Change Works, What We Do, What We Carry
  - Content, Offers, People, Study & Reflection
  - Working layer: Open Loops, Brand, Reference Docs, Systems & Infrastructure (Build Plan, Skill Map, Database Registry, Architecture Change Log, Improvement Log, Gardening Log)
  - Personal life: Life OS (a separate home; Ryan's Life + Currents under Story & Legacy)

## How the beds map here

1. **Inbox**: Capture / Inbox items. The Harvest Queue backlog is counted by Decision.
2. **Structure**: finished working pages move to a **Past passes** toggle.
3. **Database hygiene**: check **Anchor checkbox vs Spin-offs** (plus Anchor Post) for relation sync. Stale rows are **Seeds** that haven't moved.
4. **Harvest**: legacy material is anything from before Dare to Be.
5. **Language**: retired terms come from the **Terms database** (Retired rows and their replacements) plus the retired list below. Multi-word labels use **Title Case**.
6. **Loops**: see Open Loops above.

**System description pages (where drift hides):** hub pages, Cadence & Mix, Content Formats, Image Selection, Database Registry.
**Change log for the rename sweep:** Architecture Change Log.
**Registry to keep current:** Database Registry.

## Canon to check against

Read the Database Registry and Architecture Change Log at the start of every pass. They win over this list.

- Pipeline fields:
  - **Stage**, written: Seed → Sprout → Draft → Refined → Ready → Scheduled → Published
  - **Stage**, video: Seed → Sprout → Scripted → Prepped to Film → Filmed → Editing → Ready → Scheduled → Published
  - **Shape** (Pattern Book forms), **Medium**, **Track** (a formula)
  - **Pillars**, the paired five: Somatics & Soul, Expression & Transmission, Story & Craft, Rhythms & Rituals, Strategy & Systems
  - Platform, Series, Versions, Scheduled For, Metricool Link, Anchor / Anchor Post / Spin-offs, Media, Tool
- **Retired:** Status, Form, Type, Vehicle, Completed, Clip Library, Image Library, "closet self" (→ the hidden self), Capture Queue (→ Inbox).
- **Stage rules:** Seed = a concept without a forming shape. Sprout = raw material whose shape isn't confirmed. Draft = actually drafted.
- Multi-word labels in Title Case.

## Auto-apply

- Ryan's standing rule: questions found sitting as page text are logged to Open Loops during the walk, without waiting for review. Nothing else auto-applies.

## Extra checks

**Weekly Tend**
- Publishing loose ends: Pipeline rows at Scheduled whose date has passed, and rows missing a Metricool Link.

**Monthly Deep**
- Feeds the ground: candidate sections across The Work.
- Cadence & Mix checked against what was actually Published.

## Candidates exit rule

- **On** (since Sept 29).
- Applies to every Candidates entry on a Work or Ground page. That includes the Principles, Methods, Maps & Models and other candidate lists.
- Outcomes: promote to Canon, merge into an existing entry, or send to **Writings** (collection://93b797c9-6e14-4f17-9506-53c3f2586bf2).

## Legacy convention

Legacy (pre-Dare to Be) material goes in an italic section below a divider on its destination page. It is never melded into current text.

## Protected areas

- **Life archive** (Life OS): check dates, eras, duplicates and order only. Never judge the content.

## Walker split (Monthly Deep)

- **A** Ground + What We Hold True + How We Turn Perception
- **B** How Change Works + What We Do + What We Carry
- **C** Content Pipeline + Media Library databases
- **D** Content hub and its pages
- **E** Capture, Harvest Queue, Study & Reflection, Poetry
- **F** Offers, People, Brand, Reference Docs, Systems & Infrastructure, Life OS, the root page
- **G** Open Loops resolution audit

## Tool notes (this workspace)

- The workspace's Notion SQL quota runs out during a full walk. Use view mode for large reads, and save SQL for the Pipeline and Open Loops.
- The Pipeline's Track field is a formula SQL can't read. Group by Medium instead.

## Review preferences

- Every item carries full context, with plain-language labels.
- Candidate promotion (feeds the ground) and anything with several options work best as cards with a write-your-own space.
- He prefers to see placement plans before anything is filed.
