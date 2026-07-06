# daily-music

An ongoing archive of daily music exploration — historical context,
architectural analysis, and active listening notes for each piece studied.
Designed for deep listening and musical comprehension.

This document is also the procedure an AI assistant follows to produce each
day's recommendation. The recommendations and listening notes themselves
live in `ARCHIVE.md`, which this procedure reads from and writes to.

## Daily Procedure

1. **Review the archive.** Read the index table at the top of `ARCHIVE.md` to
   see what's been covered: genre, composer, piece, and date for every past
   entry.
2. **Propose genre options.** Based on the index, propose 2-3 genres for
   today — favor ones that haven't appeared recently or at all, but the human
   makes the final call. Don't pick silently; always ask.
3. **Pick the piece.** Once a genre is chosen, select a specific piece within
   it.
4. **Verify originality.** Check the piece and composer against the index:
   - Never repeat the exact same piece.
   - Avoid repeating a composer within the last 5 entries (soft cooldown —
     it's fine to revisit a composer eventually, just not back-to-back).
   If a conflict is found, pick a different piece before researching.
5. **Research.** Search the internet for accurate historical, biographical,
   and analytical context. Prioritize primary sources, program notes from
   major orchestras/ensembles, musicological writing, and the composer's own
   letters/statements where available. Note where each claim comes from.
6. **Write the recommendation** using the standardized format below.
7. **Append to the archive**: add a row to the index table and the full entry
   to the bottom of `ARCHIVE.md`.

## Recommendation Format

**The Track** — Title, Composer, Year, Recommended Recording (performer/
conductor/ensemble, and why this recording specifically).

**The Expanded Context** — Historical moment, philosophical or cultural
shift underway, and the composer's intent in writing the piece.

**The Architecture** — Technical mechanics (form, harmony, orchestration,
etc.) and the specific analytical "lens" for the day (e.g., focus on
counterpoint, or on rhythmic displacement, or on a particular motif).

**Active Listening Guide** — Chronological timestamp markers noting exactly
what to listen for, tied to the recommended recording.

**Connections** — How this piece relates to previously covered entries
(shared form, direct influence, contrast in approach, same era/different
philosophy, etc.). This is what turns the archive into a web instead of a
flat list — always try to draw at least one link if a plausible one exists.

**Sources** — Links/citations for the research in step 5.

**Your Notes** — Left blank for the human to fill in after listening.

## Archive Index Schema

Each entry in `ARCHIVE.md`'s index table has these columns:

| Date | Genre | Composer | Title | Year |
|------|-------|----------|-------|------|

This is what steps 1 and 4 scan — keep it in sync with every new entry so
dedup and genre-gap checks stay fast as the archive grows.
