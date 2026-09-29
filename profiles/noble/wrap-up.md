# Noble Movement Academy - Wrap Things Up Settings

Wrap Things Up's settings for NMA sessions. The engine (`engine/skills/wrap-things-up/SKILL.md`) holds the procedure. Page IDs live in `notion-map.md`. Fetch each data source once per run and trust the live schema over this file.

## Connector

- **NMA Notion** only. Never the connector named **Notion** (that is Dare to Be).
- **The one exception:** skill lessons and skill candidates go to the engine owner's Improvement Log in the Dare to Be Notion. Lesson text only: what the skill should change and why. Never David's content.

## Origin

- Improvement Log **Origin**: `Noble Movement`

## Where each basket files

| Basket | Home | Fields to fill |
|---|---|---|
| Skill lessons | Improvement Log, Dare to Be Notion (`collection://c91a49cf-a5ef-43ba-a548-0970cb415efc`) | Change (title), Skill, Kind, Origin `Noble Movement`, Priority, Status `Logged`, Raised (today), Source, What Changes, Why. Fixes to `profiles/noble/*.md`: Kind `Belongs Elsewhere`, naming the file, the section and the exact change. |
| New skill candidates | Improvement Log | Kind `Workflow Change`, Skill `All Skills`, Priority `Low` unless Ryan says otherwise. Name an example output page in Source. |
| Decisions | Decisions (`80ac3a77-539c-48f8-837c-33b5ea559b08`), under Operations | Fetch the schema first. When the decision changes a profile rule, also log the lesson (basket 1) and link the two in Source. |
| Tasks | Tasks (`collection://0702a907-f8c2-4b86-9b53-4c2c21d6235b`), under Operations | Task, Area, Lead, Priority, Status `Not started`, Notes. Due, Project and Program when the session names them. |
| Open loops | Open Loops (`b2dd3011-b7e6-4ec2-9d2f-5cfc36e9c9f3`) | Kind, Area, Priority, Who decides, Status `Open`, Sources. Questions only David can answer: Who decides `David`. |
| Stray work | Knowledge base scripts go to the knowledge base's `scripts/` folder (location in `profile.md`, *Knowledge base*). Engine or profile changes go to the `creation-engine` repo. | A script left only in session scratch is a skill lesson too (Kind `Drift or Bug`) when a skill should know it exists. |

## Dials

| Dial | Setting |
|---|---|
| Source label | `Wrap-up, [date] ([what the session was])` |
| Capture handoff | `ask`. Capture runs with `profiles/noble/capture.md`. |
| Approval style | Questions as cards, recommended option first. |

## Care points

- The care rules in `profile.md` apply to everything on the list, especially journals, family, clients and students. Student words are never logged as David's.
- Answers proposed from the corpus for David to confirm go on a confirm list for him (example: NMA Ops Home, David's Confirm List), not straight into Decisions.
