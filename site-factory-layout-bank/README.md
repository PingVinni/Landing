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
11. Build the site.
12. Save one compact site fingerprint JSON and update history index.

## Uniqueness rule

These do **not** count as structural uniqueness by themselves:
- image left instead of right;
- new colors;
- new font;
- different border radius;
- another image;
- renamed CSS classes;
- slightly different gaps.

## History

After every completed build, create:

`site-factory-history/sites/{normalized-domain}.json`

Then update:

`site-factory-history/index.json`

No public page copy or private user data belongs in structural history.
