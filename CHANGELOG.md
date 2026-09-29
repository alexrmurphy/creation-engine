# Changelog

All notable changes to this project are recorded here, newest first.

## 2026-09-29

- **Gardener brought into the engine.** It was built in a standalone `gardener-skill/` folder, already split into engine and profile, and is now in the repo alongside Capture and the Console.
  - `engine/skills/gardener/SKILL.md`: the procedure, unchanged except that it now finds its profile at `profiles/<creator>/gardener.md` (read with `profile.md` and `notion-map.md`) and stops if none is found.
  - `engine/skills/gardener/references/profile-template.md`: the blank profile, moved from `profiles/_template/PROFILE.md` so it travels with the skill.
  - New `profiles/dare-to-be/gardener.md`: the Dare to Be Gardener settings, moved from the standalone folder.
  - README, architecture layout and `profile.md` updated to list it.
- **Capture imported and split into engine and Dare to Be profile.**
  - `engine/skills/capture/SKILL.md`: procedure only. Names no creator and loads the profile first. Care points that apply to every creator became numbered locked rules. New Dials table (source label, section headings, deck headline and decisions header, deck look, icon).
  - `engine/skills/capture/references/`: the foundation pass (the kinds to look for, where candidates go) and the stage rule, with neutral examples.
  - `engine/skills/capture/assets/review-deck.html`: same behaviour. Colours and fonts are now tokens with a neutral default, filled from the profile through `{{FONT_LINK}}` and `{{THEME_CSS}}`. Section notes and example cards made neutral.
  - New `profiles/dare-to-be/capture.md`: triggers, connector, dials, the Dare to Be deck theme and section notes, how The Work maps kinds to pages, the routing map, formats per destination, stage examples, care points.
  - `profiles/dare-to-be/capture-worked-example.md`: the first walk capture, moved from the skill.
  - `profiles/dare-to-be/notion-map.md`: added the foundation pages, My Quotes, Quotes from Others, Brand premise, Life page, Harvest Queue, the Reframe Bank link, and a data source table. Page IDs no longer live in the skill.
  - Dropped from Capture's routing map: the old Pillars list (Somatics, Soul, Story, Strategy, Systems). `profile.md` holds the current paired five.

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
