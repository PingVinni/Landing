# Latest Ready Site Baseline

This directory is the persistent handoff point between site builds.

## Rule before every new BUILD

Before starting a new unrelated site:
1. finalize the current site package;
2. run static QA and composition self-check;
3. update this folder to that latest delivered build;
4. store its metadata, QA, build manifest, complete file integrity index and visual-asset hashes;
5. update structural history;
6. only then start the next site's structural selection.

This baseline is used for:
- regression comparison;
- identifying the exact latest delivered build;
- detecting accidental contamination;
- comparing hero/section grammar and visuals;
- checking whether files changed unexpectedly between builds.

## Binary artifact policy

The connected GitHub text workflow does not directly ingest the local binary ZIP. Therefore:
- `current.json` records the exact artifact name/version;
- `source-index.json` records every theme file with byte size and SHA-256;
- `assets-manifest.json` records visual binaries with dimensions and SHA-256;
- `qa.md` and `build-manifest.json` preserve build state;
- the user-facing install ZIP remains the canonical binary artifact.

Before the next BUILD, this directory is overwritten/updated to the newest completed site baseline.
