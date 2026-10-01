# Site Factory Layout Memory

This directory is a compact anti-repeat memory layer.

It contains no implementation archetype catalogue and no active skill logic.

- `structural-signatures.json` — normalized structural fingerprints from prior sites.
- `global-frequency.json` — how often high-level structural choices appeared.
- `banned-recent-patterns.json` — user-rejected defects + cooldown signatures.

## Use
1. Read history index.
2. Generate candidate layout using Project Source skills.
3. Compare candidate geometry, text/media anchors, section silhouettes, sequences and mobile transformation against this memory.
4. Reject/reroll materially repeated candidates.
5. After an accepted/reviewed site, update its canonical history record and rebuild these derived indexes.

Never copy a previous site's implementation from this directory.
