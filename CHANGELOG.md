# Changelog

All notable changes to this project are recorded here, newest first.

## 2026-09-27

- **T0.3: split the Content Console into engine and profile.**
  - `engine/skills/content-console/SKILL.md` now holds only procedure, locked rules, the twenty-two forms, the lenses, and dial defaults. It names no creator and loads the active profile first.
  - New `profiles/dare-to-be/profile.md`: identity, reference docs, voice rules, conventions, creator traits, doctrine, dial settings, D2B pipeline values, working notes.
  - New `profiles/dare-to-be/notion-map.md`: where each Notion page lives (links still to add in T0.5).
  - Open decisions moved to `docs/decisions/` (content pillars, claim-level spacing).
  - `docs/architecture.md`: file names aligned with the build plan, craft library marked canonical, T1.5 added.
  - `CLAUDE.md`: build plan link, Inbox routine, T0.3 marked done.
- Added `docs/architecture.md`: the four buckets, shared vs per-creator taxonomy, where things are stored, and planned work (craft library to Markdown).
- Added `CLAUDE.md` with project context, the engine vs profile rule, principles, and Phase 0 status.
- Initial import of the Content Console skill (`engine/skills/content-console/SKILL.md`), copied unchanged.
- Set up the folder layout: `engine/skills`, `profiles/dare-to-be`, `schemas`, `docs`.
