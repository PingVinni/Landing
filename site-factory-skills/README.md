# Site Factory Skills Workspace

GitHub is the **single canonical source of truth** for Site Factory skills.

## Canonical runtime model

- `site-factory-skills/current/` — active seven-bundle skill set.
- `site-factory-skills/current/index.json` — exact active fingerprints.
- `site-factory-skills/CURRENT.json` — active release pointer and bundle paths.
- `site-factory-skills/drafts/` — work in progress.
- `site-factory-skills/releases/` — release metadata/history.
- `site-factory-skills/SITE-FACTORY-BOOTSTRAP.md` — the only Site Factory file that should remain in ChatGPT Project Sources.

## Project Sources

Do **not** duplicate the seven canonical bundles in Project Sources.

At the start of a new build or skill-sensitive task, the bootstrap directs the assistant to read the live canonical bundle set from GitHub. This avoids split-brain state where Git is newer but Project Sources contain stale copies.

## Change workflow

1. Read `CURRENT.json` and the active seven bundles.
2. Develop and validate the systemic change.
3. Update affected canonical bundles under `current/`.
4. Update `current/index.json`, `CURRENT.json`, and `CHANGELOG.md`.
5. Commit.
6. Re-read from GitHub and verify fingerprints/state.

## Seven canonical bundles

- 01-CORE-GOVERNANCE.md
- 02-DESIGN-SYSTEM-BUNDLE.md
- 03-SITE-WORDPRESS-RUNTIME.md
- 04-CONTENT-LEGAL-CONTACT.md
- 05-SEO-GLOBAL-TEXT.md
- 06-VISUAL-ENGINE.md
- 07-QA-RELEASE.md
