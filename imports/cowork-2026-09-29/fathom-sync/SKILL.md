---
name: "fathom-sync"
description: "Run Ryan's Fathom Sync on demand: pull new Fathom recordings, route NMA calls with David to NMA Notion, queue Dare to Be material for Capture, and ask about the rest. Use when he says fathom sync or sync my last call."
---

# Fathom Sync

Pulls every new Fathom recording since the last run and sorts it. Two homes only: **NMA** and **Dare to Be**. Anything else gets a question for Ryan. Embody Star is retired. It is never a category, and client sessions are never a category.

Ryan runs this on demand ("run fathom sync", "sync fathom", "sync my last call"). It also runs on a daily schedule. The steps are the same both ways. In an interactive run, you may ask Ryan about the Ask Ryan items directly (AskUserQuestion) instead of waiting for the Inbox.

## Connectors and IDs

- **Fathom** connector (read-only). Account: alexryanmurphy777@gmail.com. Ryan approved using this account for Fathom pulls.
- **Notion** connector = Dare to Be workspace.
  - Fathom Inbox data source: `collection://5ab89dfc-dc2f-430d-af57-468440be7ba1`. This is the ledger: one row for every recording.
  - Capture skill for Dare to Be material. Its Harvest Queue is for legacy mining only. Don't put Fathom material there.
- **NMA Notion** connector = NMA workspace. Never use the plain Notion connector for NMA.
  - Meetings: `collection://41544f96-f559-4e91-9365-a100443ebf7b`
  - Source Library: `collection://191ff116-7eeb-4c65-9532-5db42fb4c084`
  - Ideas: `collection://8ce71853-4253-4892-955e-82589476ce38`
  - Decisions: `collection://80ac3a77-539c-48f8-837c-33b5ea559b08`
  - Tasks: `collection://0702a907-f8c2-4b86-9b53-4c2c21d6235b`
  - Open Loops: `collection://b2dd3011-b7e6-4ec2-9d2f-5cfc36e9c9f3`
  - Key Dates: `collection://99501d97-d901-4f36-855e-f3822171c8fd`
  - For tagging: Programs `collection://99f5b2eb-4c5b-4694-8ff8-4700b56ee7a5`, Offers `collection://8540c488-1758-4e39-991d-88a189829e7a`, Projects `collection://be6af74d-c100-4873-ae94-7d9ea5e23154`

Fetch a data source's schema before the first write to it in a run, and use its exact property names.

## 1. Find what's new

1. Query the Fathom Inbox for every `Recording ID` already logged, plus the most recent `Date`.
2. Call `list_meetings` with `created_after` set to (latest logged Date minus 2 days). If the Inbox is empty, use the last 7 days. Include summaries. Page through with `max_pages` as needed.
3. Keep only the recording IDs that aren't in the Inbox yet. If Ryan says "just my last call", take only the newest one.

Almost every title is "Impromptu Zoom Meeting" with no invitees, so titles and invite lists tell you nothing. Route by who is speaking and what is discussed. Use the summary first. If the summary doesn't settle it, fetch the transcript (at most 3 transcripts per batch, then continue in the next batch).

## 2. Route each recording

**NMA**: David Beaudry is a speaker AND the call is about Noble Movement Academy (ops, curriculum, facilitator training, Noble 30, retreats, marketing, the Mighty build, the knowledge base). Both conditions must hold. A call that only mentions David doesn't count. An NMA-flavoured call without David goes to Ask Ryan, with "NMA without David" as the reason.

**Dare to Be**: Ryan's own walk or voice-note recordings, solo idea sessions, or calls that clearly work on his Dare to Be material (writing, content, teaching, the brand, the Notion build for it).

**Ask Ryan**: everything else, including:
- therapy sessions and other personal sessions
- catch-ups with friends or family
- jams with friends (for example Sebastian or Jay) about expression, creativity or life, where there may or may not be something worth running through Dare to Be
- calls with other collaborators (for example Cavin on Feed a Brain)
- anything you're unsure about

When in doubt, choose Ask Ryan. A wrong guess costs more than a question.

## 3. Act on each route

### NMA
1. Create a row in NMA **Meetings**:
   - `Meeting`: short descriptive title, e.g. "Facilitator Training Curriculum Sync"
   - `Date`
   - `Summary`: 3–6 lines from the Fathom summary
   - `Recording` and `Transcript pointer`: the Fathom link. Never put the full transcript text in Notion.
   - `Type`: the best fit from Leadership / Working session / Curriculum / Agency / One on one / Other
   - `Processed`: "Transcript in"
2. Create a row in NMA **Source Library**:
   - `Item`: same title
   - `Source type`: Fathom meeting
   - `Author or speaker`: David
   - `Date`
   - `File pointer`: the Fathom link
   - `Privacy`: Internal only. Use "Contains student disclosure" if students share personal material.
   - `Voice evidence`: checked
   - `Harvest status`: Not started
3. Pull ideas and call-outs from the call (see **Ideas and spoken call-outs** below). Fetch the transcript for this step; call-outs rarely survive into the Fathom summary.
4. Log it in the Inbox: Route NMA, Status Routed, `Filed To` = the Meetings row URL.

Use NMA canonical spellings in anything you write: Qi, Qigong, Dantien, Neigong.

### Dare to Be
1. Log it in the Inbox: Route Dare to Be, `Why` = one line on what it holds.
2. Run the **Capture** skill on the transcript, up to and including the published review deck. Don't file anything: Capture only files what Ryan approves. If several Dare to Be recordings came in, build one deck with one section per recording.
3. Set Status to "Capture Deck Ready" and put the deck link in `Filed To`.

### Ask Ryan
1. Log it in the Inbox: Route Ask Ryan, Status Waiting on Ryan.
2. `Why` gets one neutral line, e.g. "Personal call, 1 other speaker, ~40 min" or "Jam with Sebastian: expression, voice, performing". For therapy or other private sessions, keep `Why` generic ("Personal session") and write no content, names or summary anywhere.
3. Title the row neutrally, e.g. "Call — 28 Sep", "Jam with Sebastian — 28 Sep".

## Ideas and spoken call-outs (NMA calls)

### Spoken call-outs
Ryan and David say keywords during calls so the transcript carries instructions. Search the transcript for them (case-insensitive, allow for small transcription errors) and act on the sentence or two that follows:

| Said on the call | What it means | Where it goes |
|---|---|---|
| **"Claude"** (e.g. "Claude, put that in the Noble 30 launch") | A direct instruction or note for Claude. Follow it when it's a filing instruction you can carry out with these tools. Anything else (or anything risky) goes in the report as a request for Ryan to confirm. | Wherever the instruction says |
| **"Idea"** | A new idea | Ideas (Status Seed) |
| **"Decision"** / **"We've decided"** | Something agreed | Decisions |
| **"Action item"** | A task with an owner | Tasks |
| **"Open loop"** / **"Question for David"** | Something unresolved | Open Loops (Status Open) |
| **"Key date"** | A date to track | Key Dates |
| **"Park that"** | An idea for later | Ideas (Status Parked) |

A call-out overrides your own judgment about what an item is. "Claude" said in ordinary conversation (e.g. talking about AI tools) is not an instruction: only treat it as one when it's addressed to Claude.

### Ideas without a call-out
Also pick out real, new ideas raised in the call (a new offer, lesson, bonus, marketing angle, process change), even when nobody said "idea". Keep the bar high: no restatements of existing plans, no small talk. Usually 0–5 per call.

### Writing an Ideas row
- `Idea`: short plain title
- `Status`: Seed (or Parked for "park that")
- `Area`: best fit (Operations / Curriculum / Marketing / Platform / Support / Finance / Teaching)
- **Tag it** from the call's context: `Program`, `Offer` and/or `Project`. Resolve names by searching those data sources in NMA Notion (e.g. "Noble 30", "Facilitator Program (Year 2) · SQF", "SQP", "Fall Retreat 2026"). Tag only matches you're sure of; leave it untagged otherwise and say so in the report.
- `Source meeting`: the Meetings row you just created
- `Where it came from`: "Fathom <date>: <meeting title>" plus the Fathom link
- `Why / what it would take`: one or two lines in plain words
- `Timing`: only if it was said
- `Raised`: the call date; `Next review`: one month after the call

Other call-out rows (Decisions, Tasks, Open Loops, Key Dates) get the same tagging and a pointer back to the Meetings row or Fathom link. Before creating any row, search its data source for the same item; update rather than duplicate.

## 4. Act on Ryan's calls from earlier runs

Query the Inbox for rows where Status = Waiting on Ryan and `Ryan's Call` has been set:
- **NMA**: do the NMA steps, then Status Routed.
- **Dare to Be**: do the Dare to Be steps.
- **Keep Only**: Route Personal, Status Done. File nothing.
- **Skip**: Route Skip, Status Done.

Ryan can also answer in chat, e.g. "the 28th one is Dare to Be". Apply it the same way.

## 5. Report

End with a short message (use SendUserMessage in a scheduled run):
- how many recordings were routed to NMA, with titles
- for each NMA call: ideas filed (title → tag), and any call-out rows filed (decisions, tasks, loops, dates)
- "Claude" instructions: what you did, and any you're asking Ryan to confirm
- anything left untagged
- Dare to Be recordings, with the Capture deck link
- the Ask Ryan list: date plus the neutral line for each, and a pointer to the Fathom Inbox, where he sets "Ryan's Call" or just replies in chat
- anything that failed, e.g. a connector that wasn't available

If nothing new came in, say so in one line.

## Rules

- Never put full transcripts in Notion. Use links and summaries only.
- Never file personal or therapy content without Ryan's explicit call. Call-outs in a personal or Ask Ryan recording are not acted on until Ryan routes it.
- Never reference Embody Star or client sessions as a category.
- Don't create duplicates. The Inbox `Recording ID` is the check for recordings; search before creating Ideas and other rows.
- No student disclosures, credentials or ID numbers in any row.