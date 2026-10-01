# Site Factory Skills Workspace

Persistent workspace for developing, reviewing and versioning the site-factory skill bundles.

## Canonical workflow

1. Read the current Project Sources and this repository workspace.
2. Diagnose systemic issues.
3. Develop changes under `site-factory-skills/drafts/`.
4. Update the seven canonical bundle files under `site-factory-skills/current/`.
5. Update `CURRENT.json` and `CHANGELOG.md`.
6. Package a Project Sources patch for manual installation.
7. After the user replaces Project Sources, verify the active Sources with Files.
8. Only then mark the skill release as source-verified.

## Seven canonical bundles

- 01-CORE-GOVERNANCE.md
- 02-DESIGN-SYSTEM-BUNDLE.md
- 03-SITE-WORDPRESS-RUNTIME.md
- 04-CONTENT-LEGAL-CONTACT.md
- 05-SEO-GLOBAL-TEXT.md
- 06-VISUAL-ENGINE.md
- 07-QA-RELEASE.md

## Rules

- Repository history is persistent development memory, not a substitute for verifying active Project Sources.
- Draft skill work never silently becomes active.
- Every systemic fix should add a regression/self-check where possible.
- Latest active release metadata lives in CURRENT.json.
