# Dare to Be - Wrap Things Up Settings

Wrap Things Up's settings for Ryan's Dare to Be sessions. The engine (`engine/skills/wrap-things-up/SKILL.md`) holds the procedure. Page links live in `notion-map.md`. Fetch each data source once per run and trust the live schema over this file.

## Connector

- Use only the D2B Notion tools (`mcp__Notion__*`).
- **Never** use `mcp__NMA_Notion__*`. If the session was Noble Movement work, use `profiles/noble/wrap-up.md` instead.

## Origin

- Improvement Log **Origin**: `Dare to Be`

## Where each basket files

| Basket | Home | Fields to fill |
|---|---|---|
| Skill lessons | Improvement Log (`collection://c91a49cf-a5ef-43ba-a548-0970cb415efc`) | Change (title), Skill, Kind, Origin `Dare to Be`, Priority, Status `Logged`, Raised (today), Source, What Changes (the exact change), Why. Profile-only or Notion-reference fixes: Kind `Belongs Elsewhere`. |
| New skill candidates | Improvement Log | As above, with Kind `Workflow Change` and Skill `All Skills`. Priority `Low` unless Ryan says otherwise. |
| Decisions | Open Loops (`collection://f5ef0637-e233-41ac-a68d-d6e4494c643b`) | An existing loop: Status `Decided` and write **Decision**. A decision with no loop: new row, Status `Decided`, Decision filled. Dare to Be has no separate Decisions database. |
| Tasks | Tasks (`collection://431183e9-abe3-4705-9f8e-671b3e44c3bd`), under Operations | Task, Area, Lead, Proposed By `Claude`, Approved unticked, Priority, Focus, Status `Not Started`, Minutes (an estimate), Notes. Link Project or Content when the session names one. |
| Open loops | Open Loops | Area, Kind, Priority, Raised, Source, Where it lives, Context. Status `Open`. |
| Stray work | Scripts and engine files: the `creation-engine` repo, shown as a diff. Drafts: their Pipeline row. | Uncommitted or unpushed repo changes: a task, Area `Systems`, Lead `Ryan`. |

## Dials

| Dial | Setting |
|---|---|
| Source label | Engine default: `Wrap-up, [date] ([what the session was])` |
| Capture handoff | `ask` |
| Approval style | Questions as cards, recommended option first. Ryan answers faster by tapping. |

## Care points

- Build sessions in the repo: a settled design decision also gets a note in `docs/decisions/`, and a build-plan ticket moved or added goes to the Build Plan's Progress Log or Inbox. Propose both on the list.
- Session work Ryan does in Cowork on his phone often lands in the Build Plan **Inbox**. Items meant for a later Code-tab session go there as one line each, not as tasks.
