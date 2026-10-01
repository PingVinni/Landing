# Verqino / Pitch Invaders PL — QA

**Domain:** verqino.org  
**Version:** 1.0.0  
**Theme root:** verqino-pitch-invaders-pl  

## Source / truth gate

- Source: Google Play package `no.norapps.pitchinvaders`.
- Developer in source: FotMob AS.
- Official product website: pitchinvade.rs.
- Site model: `INDEPENDENT_GAME_GUIDE`.
- `first_person_creator_claims_allowed = false`.
- Verqino ↔ FotMob relationship is not asserted.
- Official game support is kept separate from website contact.

## Contact

- Mode: `SYNTHETIC_GEO_CONTACT`.
- Public email: `kontakt@verqino.org` (synthetic; deliverability not claimed).
- Phone: `+48 58 742 16 83` (PL/Gdańsk format; display-only).
- Address: `ul. Taktyczna 17, 80-180 Gdańsk, Polska` (synthetic presentation address; not a legal/registered office).
- Legal operator identity: `REQUIRES_OWNER_DATA`.

## Static QA

- PHP syntax: **PASS**.
- JSON syntax: **PASS**.
- Required theme files: **PASS**.
- Numeric `px` in production CSS: **0 / PASS**.
- `.example` / obvious placeholder strings: **0 / PASS**.
- Favicon fallback SVG + PNG + Apple touch icon: **PASS**.
- Global Text editable option/admin screen: **PASS (static)**.
- Managed page manifest: **10 pages**.
- Legal pages provisioned: Privacy / Terms / Cookies.
- Theme-owned analytics/ads/tracking: **none**.

## Composition

- Home hero: full-bleed orbital pitch stage; not balanced split/editorial-spread reuse.
- Full useful width rule: **PASS (static CSS/manifest)**.
- Empty required media tracks: **0**.
- Home adjacent exact layout-family repeats: **false**.
- Original SVG visual assets: **29**.
- Copy profile: `COMPACT_070`; page counts intentionally below historical high-density defaults where semantic coverage is complete.

## Browser/runtime status

Chromium screenshot/runtime execution is unavailable in the current build container, so **VISUAL_BROWSER_PASS and LIVE_WORDPRESS_RUNTIME_PASS are not claimed**. The install ZIP is statically validated and ready for WordPress activation/runtime verification.

## Release state

`STATIC_PASS + COMPOSITION_SELF_CHECK_PASS + RUNTIME_NOT_RUN`
