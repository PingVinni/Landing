# Latest Ready Site Baseline

This directory is the persistent handoff point between site builds.

## Rule before every new BUILD

Before starting a new unrelated site:
1. finalize the current site package;
2. run static QA and composition self-check;
3. update this folder to that latest delivered build;
4. store its exact metadata, textual-source snapshot, visual-asset hashes and QA state;
5. only then start the next site's structural selection.

This baseline is used for:
- regression comparison;
- recovery of the previous textual source;
- detecting accidental contamination;
- comparing hero/section grammar and visuals;
- knowing exactly which site was the latest delivered artifact.

## Binary asset note

The GitHub connector can persist text directly. Binary visual files are tracked here by exact path, size and SHA-256 in `assets-manifest.json`. The user-facing install ZIP remains the canonical binary artifact unless/ until a binary upload path is available through the connector.
