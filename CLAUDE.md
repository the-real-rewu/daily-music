# CLAUDE.md

This repository is a daily music exploration archive. `README.md` is not
just documentation — it is the operating protocol for producing each day's
recommendation, and must be followed exactly, in order, every time this
project is worked on.

Before doing anything else in this repo (proposing a genre, picking a
piece, writing an entry), re-read `README.md` in full. Its Daily Procedure,
Genre Pool, Recommendation Format, and Index Schema sections are binding,
not suggestions — including the "surprise me"/"stay" shortcut handling,
the day-1/tie-break/cold-start rules, and the exact field definitions in
`INDEX.md`. Read `INDEX.md` in full per step 1 before proposing anything.

After step 9 (appending to the archive), always finish by opening a pull
request: create a branch, commit the `INDEX.md` and `entries/YYYY.md`
changes, push, and `gh pr create`. Before pushing to a branch used in a
prior session, check whether its existing PR was already merged (`gh pr
view <n> --json state`) rather than assuming a push will update an open
PR — if it's merged, branch fresh off `master` instead. This is how the
human receives each day's entry, so it's not optional cleanup — it's the
last step of the daily procedure, every time.

Once the PR is created, merge it immediately (`gh pr merge --merge`) —
there's no CI or required review on this repo, so there's no reason to
wait on a manual click. The human reviews after the fact via git history,
not by gatekeeping the merge.
