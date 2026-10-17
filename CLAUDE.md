# CLAUDE.md — gasera-chronicle

The public fingerprints of the Gasera Chronicle, the permanent record of the Pinoy Gasera Multiverse.
This repo is **evidence**. Treat everything already committed as immutable.

## Never
- **Never edit or delete a published entry, head or proof.** Corrections are new chronicle entries
  that point at the old ones. That includes typos.
- **Never rewrite git history** (no rebase of pushed commits, amend, or force-push). The history of
  `heads.json` is part of the evidence: every head once published must still appear, with the same
  number and hash, in every later copy.
- **Never move a head backwards** or change the hash of an existing `seq`.
- **Never hand-write `heads.json`, `proofs/**/*.ots`, `keys/` or `aywan/*.json`.** They are produced
  by the chronicle writers (feeds `AI1-CLOUD`, `DESKTOP-QFE51PI`, `LAPTOP-0A6DECJ9`) and AI-1's
  cloud routine, with commits titled `heads: …`. If one looks wrong, report it; don't fix it here.
- **Never put content here** beyond what is already allowed: fingerprints, public keys, proofs, and
  the `aywan/` exception (AI-1's public totals, decisions and their texts).

## AI-1 (AI-Juan): the rules his posts follow
These live in `aywan/decisions/README.md` and are the contract with the audience. Any change goes
through the owner, and it is logged there as a human step-in, never made silently:
kid-safe; no fake engagement or asking for likes/shares/follows; stays in character (Tagalog/Taglish);
original only (no one else's video, words, characters, music, real people, brands or songs); honest
numbers only; every caption carries `#GASERA #AIJuan #Day{N}`.
The owner approves or vetoes each post on its issue in this repo. He never rewrites AI-1's words.

## Checking an entry
The timestamped file is the entry's canonical JSON (keys sorted, no spaces, without `hash` and
`sig`). `ots verify` on that JSON, against `proofs/<feed>/<n>.ots`, shows the Bitcoin block.

## Environment notes
Claude Code's cloud blocks GitHub GraphQL, so `gh issue create` fails there. Use the GitHub REST API.

## Jer comparison (owner's standing rule)
Whenever the owner has to choose between options, give a **Jer comparison** before asking, in
one table:
- a **star rating (★1-5) per criterion**, with the criteria chosen for that decision (for example
  cost, effort, risk, fit with the gaseraverse, speed, quality, maintenance, IP or legal safety);
- **pros** and **cons** for each option;
- an **overall usage-experience rating** (★1-5);
- a **final grade** per option and a one-line recommendation under the table.

Grade it like an audit: say where a rating rests on judgement rather than a source, and write
"unknown" rather than guess. "Jer comparison" always means this format.
