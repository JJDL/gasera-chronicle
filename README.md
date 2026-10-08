# Gasera Chronicle — public fingerprints

The Gasera Chronicle is the permanent record of the **Pinoy Gasera Multiverse**, the world of
[GASERA](https://www.tiktok.com/@gaseraverse). Its root is the series' Gasera Bible. Nothing in the
chronicle is ever edited; corrections and further explanations are new entries that point at the old ones.

This repository holds **no content**, only what lets anyone check that the record was never rewritten:

- `heads.json`: the latest entry (number + SHA-256 hash) of every writer's feed. Each entry's hash covers
  the previous entry's hash, so a published head fixes the whole history behind it.
- `keys/`: each writer's ed25519 public key. Every entry is signed.
- `proofs/<feed>/<n>.ots`: an [OpenTimestamps](https://opentimestamps.org) proof per entry, anchoring its
  hash in the Bitcoin blockchain. The timestamped "file" is the entry's canonical JSON (keys sorted, no
  spaces, without `hash` and `sig`), so with an entry in hand, `ots verify` on that JSON shows the
  Bitcoin block that proves the entry existed, unchanged, by that time.

`aywan/power.json` is the one exception to "no content": Aywan's public like, reaction and share totals for his game on the
AI Arcade, with the chronicle entry that proves each day's numbers.

The git history of `heads.json` is itself part of the evidence: a head, once published, must still be
present (same number, same hash) in every later copy of the chronicle.
