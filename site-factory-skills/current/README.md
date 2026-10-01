# Current Skills

This directory is the **active canonical seven-bundle skill set**.

GitHub `main` is authoritative. Project Sources contain only the bootstrap.

`index.json` records the exact active release plus byte counts, SHA-256 fingerprints and Git blob SHAs for all seven bundles.

## Consumer rule

A new Site Factory task should:
1. read `../CURRENT.json`;
2. read this `index.json`;
3. load all seven bundle paths from GitHub;
4. use one coherent release for the entire task.

Do not mix files from different releases.

## Promotion rule

A candidate becomes current only after systemic rules are integrated into the seven bundles, static consistency checks pass, `index.json` is updated, the Git commit succeeds, and read-after-write verification confirms the committed blobs.

Project Sources verification is no longer part of promotion because Project Sources are bootstrap-only.
