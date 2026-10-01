# Verqino / Pitch Invaders PL — QA v1.1.0

**Domain:** verqino.org  
**Version:** 1.1.0  
**Theme root:** verqino-pitch-invaders-pl  

## Source / truth gate
- Source: Google Play package `no.norapps.pitchinvaders`.
- Source developer/support owner: FotMob AS.
- Site model: `INDEPENDENT_GAME_GUIDE`.
- Verqino ↔ FotMob ownership/developer relationship is not asserted.
- Generated editorial photos are explicitly described as conceptual Verqino material and not gameplay screenshots.

## GEO / SEO
- Requested: `PL / pl-PL`.
- Runtime provisions `WPLANG = pl_PL`.
- Front-end locale filter: `pl_PL`.
- Final document language hook forces `lang=pl-PL`.
- `og:locale = pl_PL`.
- Schema `inLanguage = pl-PL`.
- Explicit robots: `index,follow,max-image-preview:large`.
- Static browser implementation probes: **PASS**.

## Browser composition QA
- Home viewports: 390×844, 1366×768, 1600×1000, 1920×1080.
- Representative internal pages at 1600×1000: Taktyka, Skład, Rywalizacja.
- Browser failure count: **0**.
- Home distinct rendered-family ratio: **1.00**.
- Horizontal overflow failures: **0**.
- Large one-sided blank-field failures: **0**.
- Heading-stack failures: **0**.

## Media
- Packaged adult editorial/photoreal content photos: **5**.
- Major photo placements: **10**.
- Major photo/photoreal ratio: **1.00**.
- Major abstract/vector/diagram ratio: **0.00**.
- Childlike doodle major visuals: **0**.
- Full-page generated mockups packaged/used: **0**.

## Static QA
- PHP syntax: PASS.
- JSON syntax: PASS.
- Numeric `px` in production CSS: 0.
- Major SVG/diagram references in Global Text: 0.
- Global Text editable option/admin screen retained.
- Managed page manifest: 10 pages.
- Legal pages: Privacy / Terms / Cookies.

## Remaining runtime gate
A live WordPress instance was not available in the build container. Activation-level checks for final WordPress HTML, permalink provisioning, outbound mail and actual server headers remain post-install verification.

## Build state
`STATIC_PASS + BROWSER_COMPOSITION_PASS + GEO_SEO_IMPLEMENTATION_PASS + ADULT_MEDIA_PASS + WORDPRESS_LIVE_NOT_RUN`
