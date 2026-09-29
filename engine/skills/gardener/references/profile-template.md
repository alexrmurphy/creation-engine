# Profile: <Workspace name>

Copy this file to `profiles/<creator>/gardener.md` and fill in every slot. Delete a section only if the engine step it feeds doesn't apply. The engine (`engine/skills/gardener/SKILL.md`) reads this file at the start of every pass.

## Owner

- **Owner:** <name> (<pronouns>). The label for OWNER items in reports: <e.g. their first name in caps>.
- **Context:** <optional: what system this belongs to, sibling skills>

## Connector

- Use only: <tool prefix, e.g. `mcp__Notion__*`>
- Never use: <any other workspace connectors that must not be touched>

## Where things live

- Root: <url>
- **Gardening Log**: <url> (<collection id>)
  - Properties: <list>
  - Status values: <walked> → <in review> → <applied>
- **Open Loops**: <collection id>
  - Fields to fill when logging: <list>
  - Status values: <list>. When closing, write <decision field>.
  - Location field (for the stale-path check): <field>
- **Main working database**: <collection id>
- **Other databases**: <list>
- **Zones**: <list>

## How the beds map here

1. **Inbox**: <intake locations, queues and how to count them>
2. **Structure**: <archive / "past passes" convention>
3. **Database hygiene**: <relation pairs to check for sync; what counts as a stale row>
4. **Harvest**: <what counts as legacy material>
5. **Language**: <terms source; naming conventions>
6. **Loops**: <anything special>

**System description pages (where drift hides):** <list>
**Change log for the rename sweep:** <page>
**Registry to keep current:** <page>

## Canon to check against

<Canon sources to read first, which win over this list. Then: key fields and their allowed values, retired terms (→ replacements), stage rules.>

## Auto-apply

<What the walk may change without review. The usual choice is "log open questions to Open Loops". Write "None" for fully read-only walks.>

## Extra checks

**Weekly Tend:** <e.g. publishing loose ends>
**Monthly Deep:** <e.g. strategy docs vs actual output>

## Candidates exit rule

- On / Off
- Applies to: <which pages' candidate sections>
- Outcomes: promote to <canon>, merge, or send to <exit destination + id>

## Legacy convention

<How legacy material is placed on a page>

## Protected areas

<Areas and the only checks allowed there>

## Walker split (Monthly Deep)

<Groups of zones, one walker each>

## Overrides

<Optional: engine steps this workspace does differently, e.g. Monthly Deep interval>

## Tool notes (this workspace)

<Quotas, formula fields, quirks>

## Review preferences

<How the owner likes to review>
