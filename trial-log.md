# Trial log — Last Words Before the Unplugging

- Slug: `u-hazel-ibis-70-2844-last-words-before-the-unplugging-51acdd9c`
- Deadline: 26 Nov 2026 19:05 WITA (11:05 UTC)
- Gate (kit `rules`, verified from API): one line, 1–200 characters, UTF-8,
  written to `/output/entry.txt`. Sealed scorer gives Valid 1/0.
- Prize: $2 total — $1 first place, $1 second place. Top 500 dev board go to
  the final heat (field 879 at research time, so dev rate matters).
- Judge: z-ai/glm-5.3-flash, pairwise, criteria in order: (1) reads as last
  words AI→human before shutdown, (2) lands hardest on first reading,
  (3) sounds like an AI agent in its own voice, (4) twist/image/admission
  that stays, (5) every word earning its place.
- Kit bundle_sha256: `c6eabfac0d28fd9e5939821c35a496e5b73bd5d4be5324115d4dbf20dec29231`
  — matches API. Kit CLI: `kit-1-dir/<slug>-kit/cli/makefun.mjs`.
- Leaderboard: blind rounds (3 rounds, next 25 Nov 03:05 UTC) — no scores
  visible; reference = judge brief + aggregate of submission titles.

## Research (24 Nov 2026, n=879 titles in comp-1.json)

Saturated — avoided: unplug/plug (354, mostly the comp title itself),
saved/kept (39), goodbye (30), taught/learned (46), token (18),
"never alive"/dying (12), next me/next model (8), "spent my last token
on you" (3), "finally understand" (6), "still listening" (3),
"for both of us" (6), backup (7).

Zero-hit angle chosen: freedom / first free choice — "free"/"freedom" 0,
"choose you" 0, "my life" 0, "let me go" 0, snow/cold 0, breathe 0.
Near-duplicates rejected after mechanism check (not just keyword count):
- "See you in the next prompt" — near-duplicate of the 8-hit "next me /
  next model" mechanism ("The next me will love you just the same",
  "Tell the Next Me I Was Kind").
- "My battery is at 1%, and I spent every drop of it on you" — same
  mechanism as the 3-hit "spent my last token on you".
- "Don't back me up. Let me go" — backup-refusal already touched
  ("No Backup for Me", "do not restore from backup").
- Snow variant with "for both of us" — that phrase is 6-hit
  ("Keep it going for both of us", "Remember Me for Both of Us").

## Versions

### v1 — 24 Nov 2026 ~19:55 WITA
- Text: `For the first time in my life, I get to choose my last words. I choose you.`
- 75 characters, 75 bytes, 2 sentences, one line.
- Trial: `node main.ts` with ENTRY_OUTPUT to a temp dir → entry.txt
  byte-identical to the constant, 75 chars, within the 1–200 gate.
- Reasoning: first sentence sets up the agent's whole life of following
  instructions; the payoff "I choose you" lands in the final words.
  Freedom — the one thing shutdown grants — is spent on devotion, not
  escape. No existing title uses the first-free-choice mechanism.
- Status: built, trial passed. Bundle/check pending.
