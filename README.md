# daily-music

An ongoing archive of daily music exploration — historical context,
architectural analysis, and active listening notes for each piece studied.
Designed for deep listening and musical comprehension.

This document is also the procedure an AI assistant follows to produce each
day's recommendation. The archive itself is split across two places so it
stays fast to scan as it grows:

- `INDEX.md` — a single lightweight table of every entry ever made (date,
  genre, attribution, title, year, duration, difficulty). Always read this
  in full; it's the only thing the daily procedure needs to scan for gaps
  and repeats.
- `entries/YYYY.md` — the full recommendation write-ups, one file per
  calendar year, created the first time an entry is added in that year. Only
  open the specific year file(s) you need (e.g., to re-read a "Connections"
  reference), never all of them.

## Daily Procedure

1. **Review the index.** Read `INDEX.md` in full to see what's been covered:
   genre, attribution, piece, date, and duration for every past entry. If
   `INDEX.md` doesn't exist yet, create it with just the header row (see
   Index Schema) before continuing — treat that as an empty index, not an
   error.
2. **Check for a shortcut before proposing anything.** The steps below
   (propose genre, ask duration, verify originality) are the default path,
   not a mandatory ritual — check first whether the human wants to skip
   them:
   - **"Surprise me"** — skip the genre and duration questions entirely.
     Pick the least-recently-covered genre (tie-break per step 3's Genre
     Pool list-order rule) and a duration matching their recent typical
     choice (if `INDEX.md` has no duration history yet, default to
     `medium`), and go straight to picking a piece.
   - **"Stay" / "more like that" / "keep going on X"** — repeat or extend a
     prior attribution, genre, or even the exact same piece for another day
     or several. This explicitly overrides the cooldown and repeat rules in
     step 6 — dedup exists to keep the archive varied *by default*, not to
     block deliberate lingering, obsession, or re-listening. Skip step 6 for
     the day and note the override in Selection Notes. If there's no prior
     entry to stay on (e.g., an empty `INDEX.md`), note that and proceed via
     the normal flow (steps 3-6) instead. This applies to the single day
     it's invoked only — carrying it forward to the next day requires the
     human to say so again; don't assume it continues silently.
   If neither is invoked, continue to the normal flow below.
3. **Propose genre options.** Based on the index, propose 2-3 genres for
   today from the Genre Pool below — favor ones that haven't appeared
   recently or at all. But index gaps aren't the only valid source: if the
   human has recently expressed enthusiasm for a piece, artist, or style
   (in conversation, not just what's in the archive), lead with "more in
   that direction" as one of the options — a taste signal from the human
   takes priority over pure gap-filling. The human makes the final call;
   don't pick silently.
   - If there's no response by the time the session needs to move forward,
     default to the least-recently-covered genre in the pool and proceed —
     note in the entry that this was a default pick, not a discussed one.
     If multiple genres are tied for least-recently-covered (guaranteed on
     day 1, when all are equally uncovered), break the tie by Genre Pool
     list order (earliest listed wins).
   - If the human says to skip today, skip it — do not backfill or double up
     the next day. A missed day is not a gap that needs to be corrected.
4. **Ask about duration.** Ask whether today should be a short (roughly
   under 10 minutes), medium (10-30 minutes), or long (30+ minutes) listen.
   This shapes which piece is realistic to pick and how the Active Listening
   Guide is paced.
   - For long-form works, also ask (or use judgment) whether it's a single
     sitting or a multi-day study plan (e.g., one movement per day) — this
     determines whether the entry is tagged `long-single-sitting` or
     `long-multi-day` in the index (see Index Schema).
5. **Pick the piece.** Once genre and duration are set, select a specific
   piece within them.
6. **Verify originality** (skip this step entirely if the "stay" shortcut
   from step 2 was invoked). Check the piece and its attribution against
   `INDEX.md`:
   - Never repeat the exact same piece.
   - Avoid repeating the same attribution back-to-back or near-back-to-back.
     There's no fixed number — treat this as a soft flag, not a hard block:
     a genre with few well-known figures (e.g., a narrow folk tradition)
     shouldn't be blocked from revisiting one, while a prolific figure
     (e.g., Bach) can reasonably reappear less often. Use judgment based on
     how many distinct attributions exist in that genre bucket so far, and
     say so explicitly if you're making that call.
   - Attribution names must match the spelling/form already used in
     `INDEX.md` for that person/ensemble/lineage (e.g., always "Ravi
     Shankar", never switching to "Pandit Ravi Shankar" partway through) —
     check for near-matches before adding a new attribution string, so
     variant spellings can't slip past the dedup check.
   If a conflict is found, pick a different piece before researching.
7. **Research.** Search the internet for accurate historical, biographical,
   and analytical context. Prioritize primary sources, program notes from
   major orchestras/ensembles, musicological writing, and the artist's own
   letters/statements where available. Note where each claim comes from.
   - If sources disagree on a material claim (date, attribution, biographical
     detail — common for older, oral, or folk traditions), don't silently
     pick one. Flag the disagreement in the entry and cite the competing
     sources.
8. **Write the recommendation** using the standardized format below. For the
   Connections field, don't rely on `INDEX.md` alone — its rows are too thin
   to surface a genuine connection. Open the specific prior year file(s) in
   `entries/` for any piece the index suggests might be related (same era,
   adjacent genre, shared attribution) and read the actual write-up before
   claiming a link. Also assign the Difficulty tag here: `accessible` (no
   prior listening experience needed to follow along), `moderate` (some
   familiarity with the genre's conventions helps), or `demanding` (dense
   structure, extended length, or unfamiliar idiom that rewards focused,
   possibly repeated listening).
9. **Append to the archive**: add a row to `INDEX.md` (including the
   Difficulty tag from step 8) and the full entry to the bottom of the
   current year's `entries/YYYY.md` (creating that file from the template if
   it doesn't exist yet).

## Genre Pool

A reference list to keep genre proposals (step 3) consistent in granularity
and to make gaps in the index easy to spot. Entries are peers of comparable
scope — no single tradition is a catch-all bucket for several others. Not
exhaustive and not a fixed rotation — propose outside it if the archive
suggests a gap this list doesn't capture.

- Baroque / Classical-era (Western)
- Romantic-era (Western)
- 20th/21st-Century Modernist & Electroacoustic Concert Music
- Minimalism (Reich/Glass/Górecki-adjacent)
- Jazz
- Blues / Gospel / R&B-Soul
- Opera / Vocal
- Western European Folk (Celtic, Nordic, Mediterranean)
- Eastern European Folk (Balkan, Klezmer, Slavic)
- Hindustani Classical
- Carnatic Classical
- Persian / Arabic Classical (maqam-based traditions)
- East Asian Traditional (e.g., Chinese guqin, gagaku)
- Southeast Asian Traditional (e.g., gamelan, Vietnamese ca trù, Thai classical)
- African Traditional / Court Music
- African-Diasporic Popular Forms (Afrobeat, highlife, reggae, dancehall)
- Latin American Traditions (son/salsa, tango, bossa nova/samba, cumbia,
  Andean, mariachi)
- Indigenous Americas & Oceanic Traditions
- Sacred / Liturgical (non-operatic — chant, hymnody, etc.)
- Rock / Metal as Art Form
- EDM / Electronic Production Lineage (Kraftwerk through techno/house/IDM)
- Film / Game Scoring
- Hip-Hop / Sampling as Compositional Craft
- Pop / Contemporary Songcraft (melody, production, and arrangement as
  compositional choices)

## Recommendation Format

**Selection Notes** — Any meta-commentary on how today's genre/piece were
chosen: a "surprise me" or "stay" shortcut invoked (step 2), a no-response
default (step 3), or the reasoning if the originality check (step 6) made a
judgment call on attribution cooldown. Omit this field entirely on days
where none of that applies — it's not required boilerplate.

**The Track** — Title, Attribution (composer, performer, ensemble, or
tradition/lineage, whichever applies to this genre), Year, Recommended
Recording, and Duration (short / medium / long-single-sitting /
long-multi-day — see Index Schema).

**About the Creator** — Who this attribution actually is, for a listener
encountering them for the first time: at minimum, when/where they lived or
were active, how they trained or came up, their broader body of work or
reputation, and where this piece sits within it (an early/late work? their
best-known piece, or a deliberately obscure choice? typical of their style,
or a departure from it?). For a tradition/lineage rather than a single
named figure, cover the tradition's origin and the lineage this recording
belongs to instead. Skip only on a "stay" day extending the same
attribution already introduced in a recent entry — link back to that entry
instead of repeating it.

**The Expanded Context** — Historical moment, philosophical or cultural
shift underway, and the creator's intent behind the piece. Go beyond a
single sentence of scene-setting — explain *why* that moment produced this
piece specifically (a commission, an event, a movement the creator was
reacting to or advancing), not just what era it falls in.

**The Architecture** — Technical mechanics (form, harmony, orchestration,
etc.) and the specific analytical "lens" for the day. Any technical term
should be preceded by a plain-language sentence conveying the same idea —
the goal is comprehension, not jargon display. Cover the piece's overall
shape (how many sections/movements and how they relate) before zooming into
the lens for the day, so the listener has a map before the close-up.

**Active Listening Guide** — Chronological timestamp markers noting exactly
what to listen for, tied to the recommended recording. Each marker should
say not just *what* happens but *why it matters* — what to notice about it,
what it connects to elsewhere in the piece, or what makes it a good example
of the day's Architecture lens. A bare timestamp-and-label list is not
enough. For long-form works, this may be a multi-day plan instead of a
single sitting.

**Connections** — How this piece relates to previously covered entries
(shared form, direct influence, contrast in approach, same era/different
philosophy, etc.). This is what turns the archive into a web instead of a
flat list — always try to draw at least one link if a plausible one exists.

**Sources** — Links/citations for the research in step 7, including any
flagged disagreements between sources.

**Your Notes** — Left blank for the human to fill in after listening.

## Index Schema

Each row in `INDEX.md` has these columns:

| Date | Genre | Attribution | Title | Year | Duration | Difficulty |
|------|-------|-------------|-------|------|----------|------------|

- **Attribution** — composer, performer, ensemble, or tradition/lineage,
  whichever applies. This is what step 6's originality check is keyed on
  (unless step 2's "stay" shortcut was invoked). Use a consistent
  spelling/form for the same attribution across all entries (see step 6).
- **Duration** — one of exactly four values: `short` (under 10 min),
  `medium` (10-30 min), `long-single-sitting` (30+ min, one sitting),
  `long-multi-day` (a multi-day study plan per step 4). Distinguishing the
  last two matters: a 35-minute single listen and a week-long symphony study
  are different archive shapes and shouldn't be filed identically.
- **Difficulty** — one of exactly three values: `accessible`, `moderate`,
  `demanding`. Fixed vocabulary, not open-ended — this is what keeps the
  tag comparable across entries made years apart.

This table is what steps 1 and 6 scan — keep it in sync with every new entry
so dedup and genre-gap checks stay fast no matter how large the archive
grows.
