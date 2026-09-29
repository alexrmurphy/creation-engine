# Wrap Things Up is its own skill, and hands off to Capture

**Status:** Settled Sept 29. Built from evidence the same day; see the changelog.

## The question

Should Wrap Things Up be part of Capture, since both sort material into Notion and a wrap-up often ends with a capture?

## Decision

Keep them separate. Wrap Things Up's last step runs Capture on any creative raw material found in the session.

## Why

Checked against the Skill Map's edge rules:

- **Different input.** Capture sorts the creator's raw ideas, stories and lines. Wrap Things Up sorts the working session: lessons, decisions, tasks, loose files.
- **Different references and homes.** Wrap Things Up writes to the Improvement Log, Tasks and Decisions, and checks files and repos. None of that is in Capture's routing map, and adding it would load context Capture doesn't need on a walk transcript.
- **Different trigger.** A transcript arriving, versus the end of any session.
- **Reverse test.** They don't always run together, and they don't read the same references. The first wrap-up (Sept 29, NMA knowledge base session) had almost no creative material.

The handoff keeps routing rules for content in one place: Capture.

## Open

- The original Cowork text was never saved to the repo. If it turns up, diff it against `engine/skills/wrap-things-up/SKILL.md`.
- Add Wrap Things Up to the Skill Map (it isn't one of the ten), probably under Rhythms.
