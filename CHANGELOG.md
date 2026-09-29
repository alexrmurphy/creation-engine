# Changelog

All notable changes to this project are recorded here, newest first.

## 2026-09-28

- **First skill tune-up (Improvement Log, 13 Console rows).**
  - Engine: reads field and stage names from the Database Registry at run time instead of hardcoding them. Status → **Stage** (adds Ready, Scheduled and the video stages; Completed retired). Form → **Shape**. Clip Library → **Media Library**. Seed / Sprout / Draft defined. Medium, Track, Pillars, Anchor Post and Spin-offs named by job.
  - Engine: new locked rules 10-13 (line breaks by hand, one row per medium version, open loops logged with placement suggestions, lessons logged to the Improvement Log). Rule 8 extended: questions come as cards that carry their full context.
  - Engine: publishing handoff (Ready → Scheduled → Published). "Modes not yet built" replaced by a pointer to the Skill Map.
  - Profile: Pillars, Track and Medium notes, Metricool and the Ready to Publish folder, and the line-break rules and Copy Bank. The line-break rules were in the installed Cowork copy but never reached the repo; restored here so the reinstall does not lose them.
  - Notion map: Database Registry, Media Library, Open Loops, Improvement Log, Skill Map.
  - Architecture and decision notes updated for the renames. Content pillars partly settled.
- Added `docs/improvement-log.md`.

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
