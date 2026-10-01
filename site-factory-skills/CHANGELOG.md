# Site Factory Skills Changelog

## 2026-10-02 — content-photo-only-build-discipline-v5.1
- Added CONTENT_ASSET_ONLY image-generation mode for normal BUILD.
- Full-page/landing-page mockups are forbidden by default unless the user explicitly requests one.
- Every generated image counted in media QA must be a packaged, actually rendered content asset.
- Generated mockups can never satisfy browser/composition/mobile/GEO QA.
- Carries forward browser-proof GEO, no-dead-space, rendered-diversity and adult-photography hard gates.

## 2026-10-02 — browser-proof-geo-photo-diversity-v5
- Added GEO/locale hard gate against the final rendered HTML; PL builds now require `html lang=pl-PL`, `og:locale=pl_PL`, matching schema language and production canonical host.
- Made real browser screenshot QA mandatory for visual release; static/manifests alone can no longer claim composition PASS.
- Added rendered whitespace/typography checks: occupied canvas, blank-side ratio, H2/H3 line count and text breathing.
- Replaced label-based diversity proof with rendered silhouette + DOM/CSS/media geometry signatures.
- Added adult premium photography-first media policy: >=70% major photographic/photoreal visuals, <=20% major diagrams/vectors, zero childlike doodle major visuals.
- Added GEO-SEO-001, RENDER-001, SPACE-002, TYPE-STACK-001, DIVERSITY-RENDER-001 and MEDIA-ADULT-001 blockers.
- Invalidated the prior Verqino v1.0.0 release-ready status after observed en-GB document language, desktop dead space/heading stack, rendered repetition and vector-heavy media.

## 2026-10-02 — Git-canonical bootstrap architecture
- Promoted `full-width-canvas-compact-copy-v4` to the canonical `site-factory-skills/current/` seven-bundle set.
- Made GitHub `PingVinni/Landing@main` the single skill source of truth.
- Replaced the seven-file Project Sources mirror with a bootstrap-only model.
- Added `SITE-FACTORY-BOOTSTRAP.md` startup routing and Git-unavailable fail-safe.
- Added exact Git blob SHA verification alongside SHA-256 bundle fingerprints.

## 2026-10-02 — full-width-canvas-compact-copy-v4 (candidate)
- Added a hard full-useful-width / canvas-coverage rule for major desktop sections.
- Added blockers for one-sided blank fields, empty layout tracks and false full-width inner shells.
- Added mandatory track collapse + layout reflow when optional media is absent.
- Reduced normal visible body-copy targets by approximately 30% versus the v4.9.12 high-density profile.
- Added WIDTH-001, WIDTH-002, REFLOW-001 and COPY-030 regression cases.
- Kept SEO metadata intent intact; the reduction applies to visible page prose.

## 2026-10-01 — composition-diversity-self-check-v3
- Added section-family diversity and cross-page grammar rules.
- Added no-dead-space invariant and adaptive media fallback.
- Added visual-density recalculation when copy depth grows.
- Added broad editorial/media/process layout family library.
- Added mandatory COMPOSITION_SELF_CHECK; STATIC_PASS is blocked on failure.

## 2026-10-01 — studio-business-priority-v2
- Made company/team/development the dominant upper and middle-page narrative.
- Increased rich content depth by approximately 50%.
- Made team/workflow photography dominant in key heroes.
- Added official-studio truth-gate behavior for unresolved developer relationships.
