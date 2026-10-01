# Current Skills

This directory tracks the candidate/current seven-bundle skill set.

`index.json` contains exact SHA-256 fingerprints for the latest generated bundle set.

## Promotion rule

The seven bundle files are promoted/mirrored here only after the user installs the patch into Project Sources and the active Sources are verified.

Until that verification, the repository release is a **release candidate**, not the active Project Source truth.

After a successful `перевір`:
1. mark the release source-verified;
2. sync the verified seven bundles here;
3. update `../CURRENT.json`;
4. append `../CHANGELOG.md`.
