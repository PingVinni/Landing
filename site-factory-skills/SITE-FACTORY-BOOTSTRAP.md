# SITE FACTORY BOOTSTRAP

**Mode:** Git-canonical / Project-Sources-bootstrap-only  
**Canonical repository:** `PingVinni/Landing`  
**Canonical branch:** `main`  
**Skills root:** `site-factory-skills/`

## Mandatory startup

For every new Site Factory build, QA pass, skill edit, or continuation where the active skill state matters:

1. Connect to GitHub.
2. Read `site-factory-skills/CURRENT.json` from `PingVinni/Landing@main`.
3. Read `site-factory-skills/current/index.json`.
4. Load the seven paths listed in `CURRENT.json.current_bundle_paths`.
5. Treat those GitHub files as the active skill truth for the task.
6. For release-critical work, verify the bundle fingerprints against `current/index.json`.

Do **not** treat stale chat copies, old attachments, or removed Project Source bundles as authoritative.

## Git availability rule

If the canonical GitHub state cannot be read, do not silently fall back to remembered or stale skill text for a release-critical build.

Record:

```text
SKILL_SOURCE_UNAVAILABLE
git_canonical_loaded = false
```

Then state that the canonical skill source could not be loaded.

## Skill-change workflow

```text
READ CURRENT
→ DEVELOP / VALIDATE
→ UPDATE current/ BUNDLES
→ UPDATE current/index.json
→ UPDATE CURRENT.json
→ UPDATE CHANGELOG.md
→ COMMIT
→ READ-AFTER-WRITE VERIFY
```

Draft work may live under `site-factory-skills/drafts/`, but `site-factory-skills/current/` is the active canonical bundle set.

## Persistent factory state

Structural/layout memory:

```text
site-factory-history/
site-factory-layout-bank/
```

Latest delivered build metadata:

```text
site-factory-latest-ready/
```

## Project Sources policy

This bootstrap file is intended to be the **only Site Factory skill file kept in Project Sources**.

The seven large bundles are not duplicated in Project Sources and are not expected to auto-sync there. GitHub is the single canonical source.

## Split-brain blocker

If `CURRENT.json`, `current/index.json`, and the actual `current/*.md` files disagree, stop promotion/release claims and repair the Git state before continuing.
