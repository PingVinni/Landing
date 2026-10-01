# Site Factory Layout DNA Bank

This repository stores persistent structural diversity memory for generated sites.

## Goal

Prevent unrelated sites from converging on the same visible skeleton.

The bank is **not** a template catalogue. It combines:
- 380 macro archetypes;
- 272 atomic morphology options;
- hard structural-distance gates;
- recent-site history;
- sequence bigram/trigram memory;
- desktop + mobile silhouette comparison.

Raw independent-axis Cartesian space: **2982495040611287040000** combinations before semantic/compatibility filtering.

## Build flow

1. Load `site-factory-history/index.json`.
2. Resolve page/section semantic roles.
3. Filter invalid archetypes.
4. Exclude recent/overused clusters and sequences.
5. Select an underused topology cluster.
6. Select a macro archetype.
7. Apply compatible modifier axes.
8. Create a neutral wireframe fingerprint.
9. Compare with same-page, same-site and recent unrelated sites.
10. Reroll/mutate/synthesize until distance gates pass.
11. Build and QA the site.
12. **MANDATORY:** write/update one per-site structural fingerprint JSON.
13. **MANDATORY:** update `site-factory-history/index.json` frequency/recency summaries.
14. Re-read both written files and verify repository persistence before recording `STRUCTURAL_MEMORY_WRITE_PASS`.

## Per-site history contract

Every completed new-site build must create exactly one canonical file:

`site-factory-history/sites/{normalized-domain}.json`

Examples:
- `site-factory-history/sites/example-org.json`
- `site-factory-history/sites/elvantam-org.json`

For a same-domain update, update the existing canonical file instead of creating a duplicate. Preserve a compact `revisions[]` summary when the structure materially changes.

The file stores structural memory only: page silhouettes, layout families, topology sequences, anchors, media rhythm, interaction/mobile profiles, and fingerprints. It must not store public page copy, prompts, secrets, credentials, private user data, or unnecessary personal information.

A full new-site BUILD is not structurally finalized until:
- per-site file write = PASS;
- global history index update = PASS;
- read-after-write verification = PASS.

If GitHub is unavailable or write permission fails, record `STRUCTURAL_MEMORY_WRITE_BLOCKED` and do **not** claim cross-session anti-repeat persistence for that build.

## Uniqueness rule

These do **not** count as structural uniqueness by themselves:
- image left instead of right;
- new colors;
- new font;
- different border radius;
- another image;
- renamed CSS classes;
- slightly different gaps.

## History read rule

Before every unrelated new-site BUILD:
- load the history index;
- inspect recent sites;
- inspect same-niche/GEO candidates when relevant;
- inspect nearest structural matches;
- hard-exclude/re-roll structures that fail configured distance thresholds.

No public page copy or private user data belongs in structural history.
