# Verqino / Pitch Invaders PL — QA v1.2.0

**Domain:** verqino.org  
**Version:** 1.2.0  
**Skill release:** studio-first-photo-delivery-v5.2  

## Business model
- Mode: `OFFICIAL_GAME_STUDIO`.
- Relationship: `OWNER_SUPPLIED_CREATOR_RELATIONSHIP`.
- Evidence type: `USER_EXPLICIT_BUSINESS_ASSERTION`.
- Primary entity: **Verqino / company / team**.
- Product role: **Pitch Invaders = proof of work / promoted product**.
- Estimated company/team/development narrative ratio: **0.77** (target >= 0.60).
- Company-first pages: Home, Studio, Jak tworzyliśmy, Zespół, Kontakt.
- Public Google Play listing remains recorded separately as currently showing FotMob AS; the site does not claim the marketplace independently verifies the Verqino relationship.

## Photo delivery
- Photo families: **5**.
- Each family packages `960 + 1600` WebP and JPEG variants.
- Browser codec decode matrix: **PASS**.
- Forced WebP failure -> JPEG JS fallback: **PASS**.
- Broken required major images in browser QA: **0**.
- Original oversized single-codec photo files removed.
- Intrinsic `1600×900` dimensions are emitted in runtime markup.

## Browser composition
- Home: 390×844, 1366×768, 1600×1000, 1920×1080.
- Studio / Development / Team / Product: 1600×1000 representative checks.
- Browser failure count: **0**.
- Home distinct rendered-family ratio: **1.00**.
- Heading-stack failures: **0**.
- Dead-space / coverage failures: **0**.
- Horizontal overflow: **0**.

## GEO / SEO implementation
- GEO: PL.
- HTML language: `pl-PL`.
- OG locale: `pl_PL`.
- Schema language: `pl-PL`.
- Author: `Zespół Verqino`.
- Publisher: `Verqino`.
- `Organization` is primary entity; `VideoGame` is product entity.
- Robots: `index,follow,max-image-preview:large`.

## Static QA
- PHP syntax: **PASS**.
- JSON parse: **PASS**.
- Numeric `px` in production CSS: **0**.
- Managed pages: **10**.
- Old `/taktyka/`, `/sklad/`, `/rywalizacja/` routes receive migration redirects to the new business-first architecture.

## Remaining gate
Live WordPress activation was not available in the build container. Final server/WordPress checks for permalink migration, outbound mail, headers and actual installed HTML remain post-install.

## Build state
`STATIC_PASS + BROWSER_COMPOSITION_PASS + PHOTO_DELIVERY_PASS + STUDIO_BUSINESS_MODEL_PASS + GEO_SEO_IMPLEMENTATION_PASS + WORDPRESS_LIVE_NOT_RUN`
