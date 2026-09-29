# Visual Media - workflow spec

**Engine version:** spec v0.1, Sept 29. Nothing built yet. Decision note: `docs/decisions/visual-media-skill.md`.

Filled in from the Build Plan's workflow spec template. Blanks and open items are marked **Open**.

## Name

**Visual Media.** It takes in the place of the Skill Map's Visuals and the Console's planned Clips skill.

## Purpose

Keep the creator's photos, clips and artwork findable, and put the right visual next to the right words, while training both the creator's eye and the selection criteria.

## Trigger

| Mode | Asked for as | Also started by |
|---|---|---|
| **Intake** | "take in the new photos", "tag this batch", "new footage from the shoot" | Files landing in the intake folders (a scheduled sweep later, only if Intake gets heavy) |
| **Browse** | "show me the library", "what do I have for…", "what footage exists" | Video, before a shoot plan |
| **Pair** | "find a photo for this", "what goes with this piece" | The Console's handoff, or a Fan-out request |
| **Generate** | "make an image for this", "build the card" | A Fan-out request, or Pair finding nothing that fits |

## How it connects to the other skills

```
Console ──── finished anchor ────► Fan-out ──── words for each version ──┐
   │                                  │                                  │
   │ "want a visual for this?"        │ "visual for this carousel/card"  │
   ▼                                  ▼                                  ▼
 Pair ◄──────────────────────── Visual Media ────────────────────► Generate
   │                                  ▲                                  │
   └───── spin-off row with words + visual, at Ready for Review ◄───────┘
                                      │
 Browse ── "make something from this frame" ──► Console (new Seed row)
```

- **The Console** makes one finished piece from raw material, including a carousel or card born from a seed. It writes the words and the caption, and offers a handoff to Pair.
- **Fan-out** turns any finished thing (an anchor post, a line in the creator's quotes, an old published piece) into other versions. It writes their words (slide text, card lines with breaks set, captions) and asks Visual Media for each visual.
- **Visual Media** never writes the words that go out. It supplies and composes the image: it finds frames, generates images, and lays the creator's words onto a card using the brand templates.
- **Video** edits. Browse shows it what footage exists.
- **Capture** files photo ideas and shoot lists into the Media Library. **The Gardener** checks the library in its sweep. Neither overlaps with Intake, which handles files that already exist.

## Inputs

- **Intake:** a folder of new files (photos, clips) in one of the profile's two intake lanes.
- **Browse:** optional filters or a question ("quiet frames for quote cards").
- **Pair:** a Pipeline row, or the words and Medium of a version Fan-out is making.
- **Generate:** a Pipeline row or Fan-out request, the words, the Medium, and the brand template to use.

## Outputs

- **Intake:** Media Library rows (tagged, measured, with a preview), copies in the selects folder, and a contact-sheet deck for veto.
- **Browse:** the **Browse deck** (an HTML page) and the creator's picks and reasons.
- **Pair:** three frames with reasons, and the chosen one linked to the row.
- **Generate:** finished image files in the ready-to-publish folder and a Media Library row for each.

## Steps

### Intake

1. **Read the lane.** The profile names two lanes. **Dump** means unculled, so Claude selects. **Keep** means already chosen, so Claude files only. If a Dump drop looks already curated (under about 30 files, no bursts), ask instead of culling.
2. **File the originals.** Date each file from its metadata and file it in the archive folder under an ISO-dated shoot name. The archive is append-only: nothing is moved out of it or re-sorted.
3. **Cluster bursts.** A burst is one moment. Keep the frame where the gesture is fullest, not the sharpest.
4. **Cull (Dump only).** Apply the hard filter, then the craft criteria in priority order, from the profile's selection criteria.
5. **Measure.** `scripts/measure_image.py` computes palette fit, aperture safety and passage safety, using thresholds and palette values from the profile. For clips, it measures a frame pulled from the middle.
6. **Propose tags.** Category, Rung, Setting, Wardrobe, Shoot, Place, Orientation, Style and Type, from the live Media Library options. Read the option lists at run time. A new option value is proposed, never added silently.
7. **Contact-sheet deck.** A card per keeper with its proposed tags, which the creator can correct. Dump cards can be vetoed.
8. **File what's approved.** Copy the keepers into the selects folder, write the rows (Status: Unused, Last used empty), and upload a small preview so the Notion Gallery works away from the desk.
9. **Report the gaps.** How the new batch shifts the library's distribution, for example "still only one Rung 3 frame".

### Browse

1. **Query the Media Library** live, never from a cached copy.
2. **Build the Browse deck** from `assets/browse-deck.html`, themed from the profile. Thumbnails are embedded in the page, because Notion file links expire.
   - **Grid** with filters: Rung, Category, Palette fit, Setting, Wardrobe, Shoot, Status, Loved, Orientation, aperture safe, passage safe, and photo, clip or artwork.
   - **Compare:** two to four frames side by side at a large size.
   - **Gaps:** counts by rung, category and orientation, how many frames are passage safe, and how many clips there are. Thin spots are named as shoot-list ideas.
   - **Spacing:** what has been used in the spacing window, by setting, wardrobe and shoot, and what is rested and ready.
   - **The eye drill:** pairs of similar frames with the question *which one, and why?*. A one-line answer goes in a box.
3. **Take back the decisions** the same way Capture's deck does: picks, Loved ticks, tag corrections and reasons.
4. **File them.** Apply the approved tag corrections and Loved ticks. Log every reason in the **Eye Log**, word for word.
5. **Offer the handoffs.** A frame that sparks a piece goes to the Console as a Seed. A gap becomes a Media Library row at Status Idea, with capture notes.

### Pair

1. **Read the piece:** its words, Medium, Pillars and what it is doing (its rung). For a Fan-out request, read the anchor too.
2. **Name what the image must do** in one line, and what it must show if the piece names a practice. This is the **parity check**: if the words say "shake and wake", the image shows the bouncing shake, not a different practice.
3. **Filter:** hard filter, orientation for the Medium, palette fit, and aperture or passage safety if a signature device is planned.
4. **Check spacing** against recent and scheduled pieces: the same shoot not on consecutive pieces, and the same setting or wardrobe no more than once per spacing window. The exception: the same place is fine when the place is the story.
5. **Propose three**, each with a one-line reason covering what it is doing, parity, palette and spacing. Where two are equal, rank the one further up the rung first.
6. **Nothing fits?** Say so, and offer Generate or a shoot-list idea (a Media Library row at Status Idea).
7. **On the pick:** relate the frame to the row (Used in), copy the publish file to the ready-to-publish folder, and fill Drive Link. Log the reason in the Eye Log if the creator gives one.

### Generate

1. **Choose the job.** It is either an AI image, or a card or carousel built from the creator's words plus a frame or an AI image.
2. **AI image.** Write the prompt from the parity line and the profile's image direction, following the AI-image rules in *The Frame*. Run it in the generation tool the profile names. Generated images go through the same review as real ones.
3. **Card or carousel.** Use the brand template for the Medium. The words arrive with their line breaks already set by the Console or Fan-out, and Visual Media never re-breaks them. Size the type to the longest line. If a line won't fit at a readable size, send it back for a re-break rather than shrinking the type.
4. **Face check.** No type across a face, and nothing essential under the type. Check every slide.
5. **Review deck.** Every version goes on a card to approve, park or redo with a note.
6. **File what's approved.** Save the files to the ready-to-publish folder, create a Media Library row for each (Type Artwork or Photo, Style set, related to the piece), and fill Drive Link.

## Rules

**Always**

1. **Nothing is filed before the creator approves it.** Intake proposes, the deck decides.
2. **Originals are never moved, renamed or deleted.** The archive is append-only. Anything to delete is staged in a to-delete folder for the creator to empty.
3. **The hard filter wins.** A frame cropped through the head is out, however good it looks.
4. **Parity before beauty.** The image shows what the words say.
5. **Spacing is checked on every pair.**
6. **Reasons are logged word for word** in the Eye Log. They are the creator's, and they become criteria only when the creator approves a revision.
7. **Open loops become rows. Skill lessons go to the Improvement Log.** These are the same rules as the other skills.

**Never**

8. **Never write the words that go out.** Captions, slide text and card lines come from the Console or Fan-out.
9. **Never use a Notion file link as a public URL.** Notion links expire within hours. Public URL holds a real host's link only.
10. **Never show a recognisable person** other than the creator without the creator's OK that they are fine being in the feed.
11. **Never add a new tag value silently.** Propose it.

## Training the eye

The loop that makes this skill more than a filing system:

1. The creator picks in Browse, Pair and Generate, and says why in a line.
2. Each reason goes in the **Eye Log**, with the date, the frames and the mode.
3. At the monthly Gardener pass, or once there are ten new entries, Visual Media reads the log and proposes a **criteria revision**: a new craft criterion, a sharper category, or a changed priority. It quotes the reasons behind each proposal.
4. The creator approves it, and the profile's selection criteria get a new version and a revision-log line.

So the creator's eye is trained by seeing the library laid out and comparing frames. The criteria are trained by the creator's choices.

## Context it reads

| What | Tier | Needed by |
|---|---|---|
| Media Library (live) | Notion | All modes |
| Selection criteria (profile's page) | Notion, read in full at the start | All modes |
| Eye Log | Notion | Browse, and the criteria revision |
| Content Pipeline rows (live) | Notion | Pair, Generate |
| Brand guide and templates | Profile reference doc | Generate, and Pair when a signature device is planned |
| Composition kit | Profile reference doc | Generate |
| *The Frame* (craft edition) | `engine/craft/`, packaged with the skill | Intake, Pair, Generate |
| Carousel, quote card and text-on-screen guides | `engine/craft/`, packaged with the skill | Generate (layout only) |
| `profile.md`, `notion-map.md`, `visual-media.md` | Profile | All modes |

It does **not** read the voice file, the AI filter or the story craft books. That's what keeps it lean.

## Tools it uses

- **The profile's Notion connector:** Media Library, Pipeline and Eye Log reads and writes.
- **Local files:** the intake, archive and selects folders on the creator's machine.
- **Python scripts:** `measure_image.py` (palette, aperture, passage), `contact_sheet.py` (thumbnails for the decks, frames pulled from clips). They need Pillow, and ffmpeg for clips.
- **Google Drive:** the ready-to-publish folder.
- **The image generation tool** the profile names, for Generate.
- **Claude reading the images itself,** for tagging, the parity check and the face check.

## Human checkpoints

| Where | The creator decides |
|---|---|
| Intake, contact-sheet deck | Which frames stay (Dump), and whether the tags are right |
| Browse deck | Picks, Loved, tag corrections, reasons |
| Pair | Which of the three frames, or none |
| Generate, review deck | Approve, park or redo each version |
| Criteria revision | Whether a proposed change to the criteria is accepted |

## What it writes back

- **Media Library:** new rows, tags, Preview, Loved, Used in, Drive Link and Status. Last used and Status Used are set when a piece publishes, by Publish, or by the Console's publishing handoff until Publish exists.
- **Pipeline:** the relation to the frame, on the piece's row.
- **Eye Log:** a dated entry for each reason.
- **Open Loops:** decisions and questions. **Improvement Log:** skill lessons.
- **The selection criteria page:** only through an approved revision.

## Failure modes

- **Expired links.** Notion file URLs expire, so the deck embeds its own thumbnails and never hotlinks.
- **Drive isn't an image host.** Its share links open a viewer page, not the image. Use Drive only as the ready-to-publish folder.
- **Missing or wrong dates.** Some files have no date metadata, and some archive folders are mislabelled. Ask; never guess a date.
- **Large shoots.** Hundreds of files make a heavy deck. Cull in batches and show clusters, not every frame.
- **A thin library.** When Pair keeps finding nothing (rung 3, other people, video), say so, and turn the gap into shoot-list rows instead of forcing a weak match.
- **The brand guide isn't v1.** Generate's cards wait. Intake, Browse and Pair run now, with palette values from the selection criteria.
- **Tags drift** from the live option lists. Read the lists every run, and flag any mismatch with the Database Registry.

## Done when

- **Intake:** every approved file has a tagged row with a preview, its copy is in selects, the originals are in the archive, and the gaps report has been shown.
- **Browse:** decisions are filed, reasons are logged, and handoffs are offered.
- **Pair:** the chosen frame is related to the row, the publish copy is in the folder, and Drive Link is filled.
- **Generate:** approved files are in the folder with rows and links, and parked or redo items are noted on the row.

## Engine vs profile

**Engine** (`engine/skills/visual-media/`):

- `SKILL.md`: the procedure above, the locked rules, and the dial defaults.
- `scripts/measure_image.py` and `scripts/contact_sheet.py`.
- `assets/browse-deck.html` and `assets/review-deck.html`: neutral themes with slots, like Capture's deck.
- `references/profile-template.md`: every slot a creator's `visual-media.md` fills.
- *The Frame*, carousel, quote card and text-on-screen guides from `engine/craft/`, copied in at packaging.

**Profile** (`profiles/dare-to-be/visual-media.md`):

- The intake lanes and folder paths (archive, selects, contact sheets, to-delete, ready to publish).
- Palette values and thresholds (bone paper, ink, gold, deep water; sky over 8% fights it).
- Categories and what each is for, and the rung meanings for images.
- Signature devices (aperture, passage) and how often they run (about one in three).
- Spacing dials, and the same-place exception.
- The generation tool, the brand templates, and the composition kit pointer.
- The selection criteria page and Eye Log locations (also added to `notion-map.md`).
- The deck theme.

## Dials (engine defaults)

| Dial | Default |
|---|---|
| Frames proposed per pair | 3 |
| Spacing window | 30 days |
| Same shoot on consecutive pieces | Not allowed |
| Signature device frequency | About 1 in 3 pieces |
| Criteria revision trigger | 10 new Eye Log entries, or the monthly Gardener pass |
| "Looks already curated" threshold for Dump | Under 30 files, no bursts |

## Build order

1. **Intake and Browse.** They don't need the brand guide. Browse is the first thing to use, to start training the eye.
2. **Pair.** It can run now, with palette values from the criteria.
3. **Generate.** After the brand guide is v1 and the quote card and carousel templates exist.

## Open

- **Eye Log's home.** A new Notion database (date, frames, mode, reason, promoted?) or a section on the selection criteria page. **Recommended:** a small database, so the revision step can query it.
- **Selection criteria drift.** Choosing the Notion Gallery settles that previews do get uploaded. Image Selection Criteria v1.3 still says they don't, and still says "Image Library". Update it to v1.4.
- **Intake source.** The criteria page puts the intake lanes on the desktop, but the other chat said new files arrive in Drive. Confirm which, or both.
- **Where Visual Media runs.** Intake needs local files and scripts, which suits Claude Code. Browse, Pair and Generate could also run in Cowork. Confirm Cowork has folder access before building.
- **Generation tool.** ChatGPT image generation is named in the Open Loop. Confirm how it's reached from Claude, or whether Generate prepares prompts for Ryan to run by hand at first.
