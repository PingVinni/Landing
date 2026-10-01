# Site Factory Git Memory

This repository is intentionally **not** the active skill source.

## Active runtime rules
Active Site Factory skills live in **Project Sources**.

Git stores only:

1. `site-factory-history/` — per-site structural fingerprints.
2. `site-factory-layout-bank/` — derived anti-repeat indexes: frequencies, rejected/recent patterns, structural signatures.
3. `site-factory-archive/` — optional full-theme archive, used only after the user explicitly approves archiving the previous theme before a new BUILD.

## Never store here as active runtime state
- canonical/active skill bundles;
- bootstrap files that tell the model to load skills from Git;
- `latest-ready` working-build state;
- reusable section templates or implementation archetype catalogues;
- full theme ZIPs unless the user explicitly says to archive the previous theme.

## New-build storage rule
Before a new site BUILD, if a previous completed working theme exists, ask:

**Зберегти попередню тему в Git перед новим BUILD?**

YES → archive it under `site-factory-archive/<domain>/<version>/`, verify, then continue.  
NO → do not archive it.

Structural fingerprints are updated independently because they are required for anti-repeat comparison.

## Anti-repeat rule
Read `site-factory-history/index.json`, then `site-factory-layout-bank/structural-signatures.json`, `global-frequency.json`, and `banned-recent-patterns.json`.

Generate a new structural candidate in the active Project Source skills, compare actual geometry/silhouettes against history, reject material similarity, reroll, then build.

Git memory is for **comparison, not copying**.
