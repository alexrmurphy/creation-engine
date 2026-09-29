---
name: "wrap-things-up"
description: "Wrap Things Up: close out a working session so nothing lives only in the chat, for the creator whose profile is loaded. It sweeps the whole conversation for skill lessons, decisions, tasks, open loops, updates to existing records, work stranded in session scratch, and new skill candidates, checks Notion for what already exists, shows one approval list, files what the creator approves, and hands any creative raw material to Capture. Use when the creator says \"wrap things up\", \"wrap up\", \"wrap-up\", \"close this out\", \"let's land this\" or \"end of session\", or is clearly finishing a long working session. For sorting a walk transcript or brain dump, use Capture instead."
---

# Wrap Things Up

Wrap Things Up answers one question: what happened in this session that shouldn't be lost?

A long session leaves things everywhere: a rule settled halfway through, a fix a skill needs, a script that only exists in scratch, a task someone said they'd do, a question nobody answered. Wrap Things Up sweeps the whole conversation, sorts each of those into its home, shows the creator one list to approve, and files it. Creative raw material (ideas, stories, lines) isn't sorted here; it goes to Capture, which already knows where content lives.

This file holds the **procedure**. It is the engine: it works for any creator and never names one. Everything specific to one creator lives in their **profile**.

*Rebuilt on 29 Sep 2026 from the evidence of its first run (five Improvement Log rows), not from the original Cowork text. If the original turns up, diff it against this file.*

## Before every run: load the profile

Read the active creator's profile before doing anything else:

- **`profile.md`**: who they are, their conventions and voice rules.
- **`notion-map.md`**: where each Notion page and database lives.
- **`wrap-up.md`**: this skill's settings for the creator: connector, where each basket files, field formats, the Origin value, dials. `references/profile-template.md` lists every slot.

In the repo these sit in `profiles/<creator>/`. In an installed setup they are provided as project files alongside this skill. If no `wrap-up.md` can be found, say so and stop rather than guessing.

**Choosing the profile.** Use the profile the session worked in. If the session touched two creators, wrap up each one separately, one after the other, and never file one creator's items into the other's workspace. If that's unclear, ask.

Where this file says **the profile**, it means a value from those files. Where the profile does not set a dial, use the default in *Dials*.

## Locked rules

1. **Nothing is filed before the creator approves it.** Wrap Things Up proposes one list; they decide.
2. **Sweep the whole session, not the last few messages.** Early decisions are the easiest to lose.
3. **Only what happened.** File what was said, decided or built in the session. Never file your own inference as a decision, and never mark something done that wasn't.
4. **One home per item.** An item can touch several places. Give it one home and link the rest.
5. **Check before creating.** Search each destination for an existing row first. A match gets updated, not duplicated.
6. **Skill lessons go to the engine owner's Improvement Log,** wherever the profile's Notion map points, even when the rest of the run files into another workspace. Only the lesson text crosses over: what the skill should change and why. Never the creator's content.
7. **Profile fixes are marked as profile fixes.** A lesson that only changes one creator's profile or a Notion reference page is logged with the Kind that means "belongs elsewhere", and names the exact file or page and the exact change.
8. **Nothing stranded.** Any file written only to session scratch or outputs gets a lasting home or a task. Uncommitted or unpushed repo changes become a task.
9. **Creative material goes to Capture.** Wrap Things Up never routes content ideas, stories, principles or quotes itself.
10. **Every item carries its context.** Each line on the list says what it is, where it goes, and why, so the creator can approve without scrolling back.
11. **Nothing lives only in the chat.** End by confirming it.

## Dials

The profile's `wrap-up.md` overrides any of them.

| Dial | Default |
|---|---|
| Source label on every row | `Wrap-up, [date] ([what the session was])` |
| Capture handoff | `ask`: offer it when creative material is found. `on` runs it straight after filing; `off` lists the passages only. |
| Approval style | One grouped list; the creator approves all or names what to change. Anything needing a real choice goes on a card with options. |
| Default priority for new rows | Medium, unless the session said otherwise |
| Stray files | Propose a lasting home; if none is obvious, a task |

## The seven baskets

Every item the sweep finds goes in one basket. The profile's `wrap-up.md` names each basket's home and field formats.

| Basket | What it is | Home |
|---|---|---|
| **1. Skill lessons** | A correction the creator made, a rule settled, a rename, a bug or a workflow change that should alter a skill. Includes profile-only fixes (rule 7). | Improvement Log |
| **2. New skill candidates** | A pass done by hand more than once in the session, or one the creator says they'll want again. | Improvement Log, as a workflow change for all skills |
| **3. Decisions** | Something settled in the session that others need to know, with the reason. | The profile's decisions home |
| **4. Tasks** | Something someone will do after the session, with a lead. | The profile's tasks database |
| **5. Open loops** | A question, naming choice or system change raised and not settled. | Open Loops |
| **6. Updates** | Existing rows the session changed: a task done, a loop decided, a lesson shipped, a fact confirmed. | The row itself |
| **7. Stray work** | Scripts, files or drafts that exist only in session scratch or outputs; uncommitted repo changes. | A lasting home, or a task |

Creative raw material is not a basket. It is set aside for the Capture handoff.

## The run

### 1. Sweep

Read the whole session from the start. List every candidate item with its basket and the exact words or evidence behind it. Also:

- Merge items that come up more than once.
- Pull out lasting instructions the creator gave Claude ("from now on..."). They are skill lessons or profile fixes, not tasks.
- Notice files you wrote, where they are, and whether they were saved anywhere lasting. If the session worked in a repo, check for uncommitted or unpushed changes.
- Set aside passages of creative raw material for Capture. Note them; don't sort them.

### 2. Check Notion

Fetch each destination's data source once per run to confirm the current property names and option values. The profile's formats are a snapshot; the live schema wins.

Search each destination for a match before proposing a new row: the Improvement Log for the same lesson, Tasks for the same task, Open Loops for the same question. A match becomes an update (basket 6). Close calls get named on the list.

### 3. Show the list

Write one list in the chat, grouped by basket, in the order above. Each line: a short title, where it goes, and one line of why or evidence. For skill lessons, give the skill, the Kind, the priority and the exact change. Put anything that needs a real choice (which option, who leads, keep or drop) on a card with a recommended option first.

End with the Capture line: how many creative passages were found and what they're about, and whether to hand them over.

### 4. File what they approve

Write order: updates to existing rows, then skill lessons and skill candidates (one create call), then decisions, then tasks, then open loops. Save stray work to its approved home. Every new row carries the source label and today's date. When the creator changes an item, apply the change to every similar item and say so in one line.

### 5. Hand off to Capture

Follow the Capture handoff dial. When it runs, pass Capture only the creative passages, in the creator's words, with the session as the source. Capture runs its own review and approval; don't repeat its work here.

### 6. Close

Reply with a short account of what was filed, grouped by basket, with links. Name anything still open and where it's logged. Confirm nothing lives only in the chat. Don't recite everything back; they can see it in Notion.

---

# Keeping this current

Anything specific to one creator changes in their profile, never here. This file changes only when the **procedure** changes: a new basket, a new locked rule, or a change to the approval step or the Capture handoff.
