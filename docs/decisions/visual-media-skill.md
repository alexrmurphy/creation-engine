# One Visual Media skill

**Status:** Settled Sept 29: one skill, not two. The build freeze was lifted the same day, so the workflow spec comes next, then the build.

The Skill Map's **Visuals** and the imported Console's planned **Clips** skill become one skill, **Visual Media**.

## Why one

- **The data is already one thing.** The Image and Clip Libraries merged into the Media Library on Sept 27.
- **Most library upkeep is already owned.** Capture files photo and clip ideas and shoot lists into the Media Library. The Gardener checks it in walker C. The Console's publishing handoff files the final photo and fills Drive Link. What's left (taking in new media, and browsing it) is too small for a skill of its own.
- **Tags exist to serve pairing.** When the same skill tags and pairs, the categories get designed for how they are actually used.
- **One way of asking.** "What photos do I have for this?" and "tag the new batch" are both requests about visual media. Two skills would need routing between them.

## Four modes

| Mode | Job | Needs the brand guide |
|---|---|---|
| **Intake** | New photos and footage become Media Library rows, tagged and measured (palette, aperture, passage). Covers the Dump and Keep lanes in Image Selection Criteria. | No |
| **Browse** | See the library: a lightbox filtered by rung, category, palette fit and spacing, a gaps view, and footage by category. This takes in the planned Clips skill. | No |
| **Pair** | A visual for a piece, with reasons (what the image is doing, how it fits the message, palette, spacing). Fills Used in, Last used and Drive Link. | Yes |
| **Generate** | The AI image queue, keeping image and message in step. Includes the face check before type is placed. | Yes |

Intake and Browse could ship first.

## Training the eye (proposed, to settle in the spec)

Browse and Pair log each pick along with Ryan's one-line reason. Those reasons are promoted into new versions of Image Selection Criteria, the same way Capture's worked example turned corrections into rules. Ryan's eye gets trained by seeing the library laid out, and the criteria get trained by his choices.

## Boundaries

- **Fan-out stays separate.** It decides what to make and writes the words for a carousel or quote card. Visual Media supplies the image.
- **Video stays separate.** Editing is its own process. Browse only shows it what footage exists.
- **The Console** offers a handoff ("want a visual for this?") and doesn't load the brand guide or photo criteria itself.

## When to split

Only if Intake grows into a heavy job with its own schedule, such as a weekly Drive sweep with bulk tagging. Even then, a scheduled mode inside the same skill is probably enough.

## Engine and profile

- **Engine:** the procedure, the head-crop rule, the spacing logic, a measuring script, the lightbox template, and a neutral edition of *The Frame*.
- **Profile** (`profiles/dare-to-be/visual-media.md`, to add): folders and intake lanes, palette values, categories, signature devices (aperture, passage), spacing dials, and the image generation tool.

## Open, for the spec

- **Captions for a visual.** Pair includes "a caption for a visual" in the proposal. That is voice work, so it may belong to Fan-out or the Console instead.
- **The lightbox.** An HTML review deck like Capture's, the Notion Gallery view, or both.
- **Build order.** Intake and Browse first (they don't need the brand guide), then Pair and Generate once the brand guide is v1.
- **Drift found:** Image Selection Criteria v1.3 still says no image uploads to Notion and that the Preview field was removed. The Media Library now has a Preview field and a Gallery view. Update the page to match whichever is true.
