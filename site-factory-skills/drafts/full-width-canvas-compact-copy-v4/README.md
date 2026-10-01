# full-width-canvas-compact-copy-v4

Candidate systemic fix for the Site Factory skill set.

This release addresses two regressions together:

1. major desktop sections that technically span the page but leave large unused fields because the meaningful inner composition stays narrow;
2. excessive body-copy density from the earlier +50% depth profile.

Canonical rules are in [PATCH.md](./PATCH.md). Machine-readable values are in [overrides.json](./overrides.json), and blocking regression cases are in [regression-cases.json](./regression-cases.json).

Status: **CANDIDATE_READY_AWAITING_PROJECT_SOURCE_INSTALL_AND_VERIFY**.

The repository candidate is not the same as active Project Sources. After the seven Project Sources are updated from this patch, they must be re-read and verified before the release is marked source-verified.
