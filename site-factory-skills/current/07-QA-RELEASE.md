# 07 QA RELEASE

**Bundle format:** Source Bundle v1.5  
**Policy baseline:** Site Factory v4.9.15  
**Bundling rule:** logical module boundaries and aliases are preserved inside bundles. Source Bundle v1.5 applies the Site Factory v4.9.14 interaction, micro-motion, hover/focus and semantic interactive-section expansion while preserving v1.4 rich-content, live UI/UX research, morphological section variation, v1.3 adult-premium visuals and the 7-file Project Source architecture.

## Module aliases in this bundle

- `10-QA-RUNTIME.md` → this file, section `LEGACY MODULE: 10-QA-RUNTIME.md`
- `11-VISUAL-QA.md` → this file, section `LEGACY MODULE: 11-VISUAL-QA.md`

## Cross-reference rule

References inside logical module text to filenames such as `15-SECTION-IMAGE-ENGINE.md` remain valid **logical module IDs**. Resolve them against the module aliases declared across the loaded Source Bundles. `SOURCE-BUNDLE-MAP.md` is maintenance documentation only and is **not required** as a Project Source.

---

<!-- BUNDLE-MODULE-START: 10-QA-RUNTIME.md -->

# LEGACY MODULE: 10-QA-RUNTIME.md

# RUNTIME / BROWSER QA

**Version:** 4.8.0  
**Role:** довести, що сайт реально працює після WordPress install і rich-content/layout research artifacts узгоджені

---

## 1. Static QA — тільки перший рівень

Перевірити:
- PHP syntax;
- archive integrity;
- namespace;
- required files;
- no placeholders;
- no numeric px;
- manifest completeness.

Але Static PASS не означає runtime PASS.

---

## 2. Install test

На disposable/reusable WordPress:

1. upload theme ZIP;
2. activate;
3. open frontend;
4. let first-request provisioning run;
5. inspect provisioning status.

---

## 3. Page state

Перевірити:
- managed page count = manifest page count;
- every required page exists;
- published;
- correct slug;
- correct title;
- correct page-ID map;
- Home assigned.

---

## 4. Navigation

Перевірити:
- visible header labels = current manifest;
- destination IDs = current managed pages;
- no stale Polish/old-theme labels;
- footer legal links;
- cards;
- CTAs;
- related content.

---

## 5. URL runtime

Для кожного internal link:
- click;
- capture final browser URL;
- verify it matches the selected URL mode;
- no 404;
- no redirect loop;
- no old theme content;
- correct destination context.

`?page_id=` is allowed only when runtime state is `QUERY_URL_PASS`.
`/index.php/slug/` is allowed only when state is `DEGRADED_URL_PASS`.

---

## 6. Page-context

Після link:
- expected page loaded;
- correct H1;
- correct eyebrow/breadcrumb;
- URL matches;
- menu context reasonable.

---

## 7. Browser errors

Перевірити:
- console errors;
- JS exceptions;
- failed critical network requests;
- broken images;
- missing CSS/JS;
- CSP/integration problems if relevant.

---

## 8. Responsive

Перевірити representative widths:
- wide desktop;
- laptop;
- tablet;
- mobile.

Не лише screenshot:
- nav;
- cards;
- tabs/accordion;
- CTA;
- legal TOC;
- consent;
- forms.

---

## 9. Horizontal overflow

Blocking:
- body wider than viewport;
- offscreen button;
- long URL breaks legal page;
- nav overflow;
- image fixed width.

---

## 10. Interaction

Якщо є:
- mobile menu;
- tabs;
- accordion;
- filters;
- cookie preferences;
- forms

— кожен pattern перевіряється функціонально.

---

## 11. Legal runtime

Перевірити:
- Privacy opens;
- Terms opens;
- Cookies opens;
- footer destinations current;
- consent behavior matches runtime technologies;
- legal TOC anchors work.

---

## 12. 404

Intentional:
- 404 template;
- Home CTA;
- no PHP error;
- visually consistent.

---

## 13. Runtime PASS

PASS лише якщо:
- page state;
- link state;
- browser state;
- responsive;
- interaction;
- legal links

всі пройшли.

Інакше `FIX_REQUIRED`.


---

## 14. Contact runtime QA

Перевірити:
- email href (`mailto:`) відповідає видимому email;
- phone href (`tel:`) нормалізований;
- visible phone формат відповідає GEO;
- postal address збігається між Contact / footer / legal;
- factory-generated public email host exactly matches site `DOMAIN`; explicit `OWNER_SUPPLIED` / `VERIFIED` email may override;
- немає `.example`, `test@`, `demo@`, `000 000 000`, `Rua Exemplo` та інших obvious placeholders;
- synthetic phone/address мають status `SYNTHETIC_GEO_CONTACT`;
- synthetic values не названі verified/registered/legal facts;
- `mailto:` / `tel:` активні тільки відповідно до contact interaction state.

---

## 15. Content / media runtime depth

Для ключових сторінок:
- expected section count;
- images/SVG/background assets реально завантажуються;
- visual moments не зникають через CSS;
- media не broken;
- internal pages не виглядають thin.


---

## 16. Generated-image runtime QA

Для кожного asset із `SECTION IMAGE MANIFEST`:

- file реально присутній;
- HTTP status 200;
- correct MIME;
- image decode успішний;
- intrinsic/aspect ratio відповідає manifest;
- object-fit/crop не руйнує subject;
- mobile rendition не обрізає ключовий subject;
- alt відповідає section purpose;
- decorative background не має misleading alt;
- critical hero image не lazy-load, якщо це погіршує LCP;
- below-fold assets можуть lazy-load;
- немає remote temporary generation URLs у final theme.

Blocking:
- broken generated image;
- missing local asset;
- section очікує image, але фактично показує empty container;
- image generation output не потрапив у install-ready ZIP.

---

## 17. Input-contract runtime QA

До RELEASE assert:

```text
DOMAIN != empty
GEO != empty
TOPIC/NICHE != empty
```

Canonical host, sitemap host та internal URLs повинні походити з того самого `DOMAIN`, якщо deployment не задає explicit override. Factory-generated public email host MUST equal that same `DOMAIN`; only explicit `OWNER_SUPPLIED` / `VERIFIED` email may use another host.


---

## 18. Rendered IMG attribute QA

Crawler збирає кожен rendered `<img>`:

```text
src
alt_attribute_present
alt_value
title_attribute_present
title_value
role
page
section
owner
```

### Meaningful image

Required:
```text
ALT present and non-empty
TITLE present and non-empty
```

ALT:
- описує зміст/function;
- localized;
- без keyword stuffing.

TITLE:
- короткий human-readable visual label;
- localized;
- може бути коротшим за ALT.

### Decorative image

Preferred:
- CSS background / pseudo-element;
- або explicit decorative classification.

Не залишати випадковий `<img>` без ALT/TITLE лише через те, що “він декоративний”.

### Gate

Для factory-owned meaningful images:

```text
images_missing_alt = 0
images_missing_title = 0
```

Якщо missing:
- знайти shared template/helper;
- виправити source;
- rerun rendered crawl.

---

## 19. Rendered LINK attribute QA

Crawler збирає кожен `<a>`:

```text
href
text
title
internal/external/hash/mailto
HTTP/final state
owner
```

Factory-owned links:

```text
missing title = 0
broken = 0
```

Hash/skip links теж отримують localized title.

`title` не компенсує поганий visible label.

---

## 20. Verified production URL QA

URL quality is state-based:

```text
CLEAN_URL_PASS      → /slug/
DEGRADED_URL_PASS   → /index.php/slug/
QUERY_URL_PASS      → ?page_id=ID
URL_FAIL_VERIFIED   → RELEASE BLOCKED
```

Preferred state is `CLEAN_URL_PASS`.

QA must verify:
- selected mode actually resolves;
- every managed link uses the selected mode;
- no raw server 404;
- canonical matches the reachable page;
- no mixed-mode navigation.

---

## 21. Browser SEO-extension parity check

Перед RELEASE виконати page-level audit, еквівалентний browser SEO inspection:

```text
images total
images missing ALT
images missing TITLE
links total
unique links
internal unique
links missing TITLE
title
description
keywords
keyword_term_count
canonical
robots
author
publisher
lang
H1/H2/H3
```

Blocking factory-owned counts:

```text
images missing ALT > 0
images missing TITLE > 0
links missing TITLE > 0
```

Мета — не “намалювати зелені цифри”, а прибрати реальні omissions у factory-controlled HTML.

---

## 22. Critical internal-link click audit (v4.4 patch)

QA must click/resolve all critical internal links from rendered pages.

Mandatory audit set:
- header navigation;
- footer navigation;
- hero CTA(s);
- at least one CTA per major section;
- policy links;
- contact links.

PASS only if destination is reachable and contextually correct.

## 23. Rendered DOM attribute zero-miss audit

Release blockers:
- meaningful rendered images missing `alt` > `0` → FAIL;
- meaningful rendered images missing `title` > `0` → FAIL;
- factory-owned rendered links missing `title` > `0` → FAIL.

QA must inspect rendered DOM, not only source templates.

## 24. Browser console cleanliness

Run console audit in a clean browser profile when possible.

Blocking:
- theme-owned uncaught errors;
- failed theme asset loads;
- broken initialization that affects nav, modal, consent, slider, tabs, accordions.

Extension-only noise may be logged separately, but must not be confused with a theme PASS.

## 25. Cookie / modal runtime audit

Verify:
- cookie bar renders;
- preferences modal opens;
- modal can close;
- legal links inside consent UI work;
- no JS breakage around modal state.


---

## 26. Managed-page exhaustive 404 gate

After provisioning, crawl **every managed page URL**, not a sample only.

For each managed page assert:
- final status success;
- not Apache/host `Not Found`;
- expected page H1/context;
- final URL matches selected verified mode;
- page reachable from at least one intended navigation/related link where applicable.

Any managed page 404 = `RUNTIME_FAIL`.


---

## 27. Three-mode URL acceptance test

For one managed page, test in order:

```text
/slug/
/index.php/slug/
?page_id=ID
```

Record:
- request URL;
- HTTP status;
- final URL;
- factory page marker/H1;
- selected mode.

At least one verified mode must work.

If clean fails with raw Apache/Nginx 404, QA must not stop there; it must test PATHINFO and query fallback.

## 28. Stable theme-root update regression

For every in-place update:

1. inspect ZIP root;
2. assert it equals previous installed theme root;
3. upload while old theme is active;
4. confirm WordPress updates the existing theme;
5. open frontend without manual activation;
6. confirm new provision version executed.

Different root directory for same site's version update = blocking FAIL.

## 29. Link-mode consistency crawl

After URL mode selection:
- header links use selected mode;
- footer links use selected mode;
- cards/CTA use selected mode;
- legal links use selected mode;
- canonical uses selected mode;
- sitemap/core permalink output does not point to a known broken route.

Any mixed state where navigation points to raw 404 paths = `RUNTIME_FAIL`.


---

## 30. Image-source runtime audit (v4.4.6)

For every non-generated external raster used in production verify:

```text
local asset = yes
remote hotlink = no
provenance record = present
rights_state = publishable
required attribution = satisfied
decode = success
HTTP local asset = 200
MIME = expected
dimensions = appropriate
metadata sanitization = recorded
```

Publishable rights states:
- `OWNER_SUPPLIED`;
- `PUBLIC_DOMAIN_CC0`;
- `OPEN_LICENSE_COMPATIBLE`;
- `EXPLICIT_REUSE_PERMISSION`.

`REFERENCE_ONLY`, `REJECTED_UNKNOWN_RIGHTS` or missing rights state = FAIL.

If attribution is required, metadata removal does not cancel that obligation.

## 31. Unwanted edge artifact runtime gate

Review rendered image at normal and high zoom.

Blocking when unintended:
- white border/matte appears inside the image frame;
- collage separator survives crop;
- transparent fringe becomes a white halo;
- image has baked white rounded-card background while CSS also provides the card;
- letterboxing/pillarboxing looks accidental.

For edge-to-edge media components:
```text
asset crop edge == visible media edge
```

unless the section design explicitly requests an internal frame.

If defect exists:
`ASSET_REPAIR_OR_REGENERATE → RERENDER → VISUAL_QA`.

---

## v4.5.11 patch — public SEO zero-red enforcement

### 1. Logged-out public audit is mandatory
Run rendered audits in a logged-out browser state on public pages.
Record any logged-in toolbar noise separately, but public release PASS depends on public frontend counts.

### 2. Zero-red browser extension parity
Factory must emulate common browser SEO extension checks and PASS with:
```text
images missing ALT = 0
images missing TITLE = 0
links missing TITLE = 0
indexable meta keyword term count >= 16
```
for all factory-owned public pages.

### 3. Rendered `<img>` universal gate
For every factory-owned meaningful rendered `<img>` instance, including:
- featured images;
- attachment-derived sizes;
- card thumbnails;
- hero images;
- inline editorial images;
- attribution-adjacent images;

required final DOM state:
```text
alt attribute present and non-empty
title attribute present and non-empty
```

### 4. Rendered `<a>` universal gate
For every factory-owned rendered `<a>`, including:
- nav links;
- CTA links;
- footer links;
- policy links;
- source links;
- attribution links;
- image wrapper links;
- skip links;

required final DOM state:
```text
title attribute present and non-empty
```

### 5. Ratio verification
QA must compute project-level meaningful visible raster image mix:
- generated originals >= 65%
- reusable/supplied <= 35%

If ratio fails, release fails.

### 6. Recommended capture set
Audit at least:
- home;
- one key internal guide page;
- one informational page;
- contact;
- legal page;
- one page containing reusable external imagery.


---

## 32. Global Text runtime QA (v4.4.7)

Release requires:

```text
persistent global-text.json exists = yes
JSON valid = yes
required key coverage = 100%
factory-owned visible hardcoded copy outside Global Text = 0
last-known-good safety = verified
FastPanel-style edit propagation = verified
```

### Edit propagation test

On a disposable/runtime environment:
1. capture a known rendered string and its key;
2. edit that key in persistent `global-text.json`;
3. save;
4. request the page again in an uncached/logged-out request;
5. assert new text appears at the correct location;
6. assert no rebuild/reprovision was required;
7. restore test value.

### Invalid JSON test

1. back up file;
2. deliberately make JSON invalid;
3. request frontend;
4. assert no fatal/white screen;
5. assert last-known-good content renders;
6. assert admin diagnostic shows `GLOBAL_TEXT_INVALID`;
7. restore valid file;
8. assert state self-recovers.

### Missing-key test

Remove one required key temporarily:
- exact key must be logged;
- safe fallback/LKG behavior must occur;
- release state must fail until key is restored.

### Hardcoded public-copy scanner

Static QA must scan theme templates/components/JS for user-visible literals.

Blocking examples:
- literal H1/H2/paragraph text in PHP template;
- literal button/nav/footer label;
- literal image ALT/TITLE;
- literal link TITLE;
- literal cookie/modal UI string;
- literal JS user-facing message.

Technical strings are allowlisted separately.

### Cache test

If host/plugin/CDN page cache exists:
- verify the Global Text change becomes visible after the factory's supported purge path;
- if automatic purge is impossible, report the cache layer explicitly rather than claiming instant propagation.

---

## 33. Footer + image-source presentation QA (v4.4.8)

### Footer bottom bar gate
For every public template that renders the standard footer, assert:
```text
footer_bottom_bar_present = yes
copyright_brand_present = yes
copyright_year_resolves = yes
rights_reserved_localized = yes
```

The bottom bar must not expose an invented legal company/operator.

### Web-image public-source gate
For every `VERIFIED_REUSABLE_WEB` raster:
- internal provenance record exists;
- local production asset exists;
- nonessential metadata is stripped;
- no hotlink remains;
- ALT/TITLE describe section semantics, not the source website.

When `attribution_required = false`, assert:
```text
visible_source_caption = 0
visible_source_link = 0
```

When `attribution_required = true`, assert either:
- required attribution is present and compliant; or
- the asset was replaced before release.

Unnecessary source captions/links for attribution-free web assets = `FIX_REQUIRED`.



---

## 34. Section Composition runtime/static QA (v4.5.0)

Before RELEASE verify module 18 outputs.

Required build artifacts/state:

```text
site_composition_seed = present
SECTION COMPOSITION MANIFEST = present
PAGE COMPOSITION FINGERPRINTS = present
SITE COMPOSITION FINGERPRINT = present
```

### Static checks
- every meaningful section has `pattern_family` and `section_fingerprint`;
- unexplained exact fingerprint duplicates on one rich page = 0;
- key pages do not share an identical visible section-family sequence;
- every unusual/sticky/rail/tab/accordion composition declares a mobile fallback;
- interactive patterns declare keyboard/ARIA behavior where applicable;
- same-site update preserves the existing composition seed unless explicit redesign is recorded.

### Browser checks
At representative widths inspect:
- section order;
- overlap/clipping;
- sticky fallback;
- rail overflow containment;
- mosaic collapse;
- text expansion resilience;
- focus order;
- reduced-motion behavior.

If composition is technically valid but visually repetitive, static PASS is not enough; Visual QA may still reject it.



---

## 35. Density / major-image-reuse / footer-composition QA (v4.5.1)

### Section density capture
At representative desktop widths, record/inspect:
- section bounding height;
- heading line count;
- headline/body/media relationship;
- unusually large empty regions;
- disconnected text islands.

Blocking:
- ordinary non-hero section is stretched mainly by padding/min-height;
- eyebrow/title/body are visibly disconnected;
- large blank column/field has no declared function;
- non-hero heading behaves like an oversized hero without justification.

### Major raster reuse audit
For every rendered major raster collect:

```text
page
section
asset_id
source_asset_id
file_hash
visual_signature
major_media_boolean
```

Default blockers:
- same `source_asset_id` in more than one major section;
- hero `source_asset_id` used again as major media;
- multiple major files derived from one collage/contact-sheet source;
- obvious visual near-duplicate pair without allowlisted narrative reason.

Derived crop/resize/format variants count as one source.

### Footer composition audit
Record:
- footer family;
- column count/ratios;
- brand/nav/contact/legal/source positions;
- bottom-bar signature;
- mobile order.

Verify:
- footer is consistent across pages of the same site;
- mobile order remains logical;
- legal/contact destinations remain correct;
- cross-site comparison is performed when recent footer fingerprints are available.



## 36. Contact / SEO parity / all-media uniqueness QA (v4.5.2)

### Contact screenshot gate
For Contact Profile fields that are resolved for public display, capture desktop + mobile and assert:
```text
public_email_visible = yes
public_phone_visible = yes when resolved
public_address_visible = yes when resolved
product_support_relationship_clear = yes when present (first-party same-studio or clearly separated third-party according to resolved relationship)
```
`DISPLAY_ONLY` phone still counts as required visible text.

### SEO browser parity gate
On Home + at least one key domain page + Contact:
```text
author != empty
publisher != empty
keyword_term_count >= 16 for every indexable page in factory SEO mode
robots_tag_count = 1
robots_value = expected coherent state
description length = reviewed against page intent
```
For normal key content pages, description under roughly `120` characters is normally `FIX_REQUIRED` unless explicitly justified.

### Rendered density gate
At approximately 1440px-class desktop review each representative page for:
- oversized non-hero headings;
- unused second columns;
- giant blank fields;
- disconnected eyebrow/title/body groups;
- section height driven mostly by padding/min-height.

A screenshot may fail even when CSS values individually fall inside allowed envelopes.

### All-media reuse gate
Collect major visible assets across pages regardless of type:
```text
asset_id
asset_type (raster/svg/diagram)
visual_signature
page
section
```
Default blockers:
- exact major SVG/diagram reused across unrelated pages;
- same hero/major asset reused elsewhere;
- visually obvious near-duplicate compositions without narrative reason.



## 37. Section/visual v4.7 artifact readiness

Static/runtime handoff for v4.7 requires these artifacts/state where applicable:

```text
PAGE RHYTHM RECIPES = present for key pages
SECTION COMPOSITION MANIFEST = macro + grammar dimensions complete
SITE COMPOSITION FINGERPRINT = present
VISUAL MEDIUM RHYTHM = present for visual-rich builds
SECTION IMAGE MANIFEST = present
SECTION BACKGROUND MANIFEST = present when non-plain authored backgrounds are used
major SVG visual signatures = present when major SVGs are used
```

Missing an artifact does not justify inventing a PASS; report the unavailable comparison/history explicitly.



## 38. Rich-content + live-research artifact gate (v4.7.0)

For full rich BUILDs require, when applicable:

```text
CONTENT DEPTH MANIFEST = present
LIVE UIUX RESEARCH MANIFEST = present when web research was available
LIVE SECTION PATTERN BANK = present when web research was available
SECTION COMPOSITION MANIFEST modifier stacks = complete
```

If web was unavailable, record the limitation rather than inventing research evidence.

### Content runtime/static checks
For representative pages record:
- visible word count;
- meaningful section count;
- information-role distribution;
- repeated paragraph/section warning;
- unsupported factual claim audit;
- page-specific internal link targets.

A page may pass below the normal word envelope only with an explicit source/format limitation note.

### Empty-stage blocker
A large visual frame/panel/column with no meaningful content, media, data, diagram or intentional atmospheric function is a blocking composition defect.



## 39. Interaction / motion runtime QA (v4.8.0)

For each component in `INTERACTION-MOTION-MANIFEST.json`, test:

```text
static fallback content present
mouse/pointer interaction
keyboard interaction
visible focus
touch/mobile behavior
ARIA/state coherence
reduced-motion behavior
resize/reflow
no horizontal page overflow
no console errors
```

Additional gates:
- slider previous/next controls work and disabled/end states are coherent;
- no autoplay by default;
- tabs switch panels without losing focus context;
- accordion state is operable by keyboard and content remains in DOM;
- filter/switcher empty states are intentional;
- hover-only required content = `0`;
- pointer hover does not leave sticky transformed states on touch;
- `prefers-reduced-motion` disables/simplifies reveal/parallax/progress animation.

Missing interaction artifact for a rich BUILD that uses custom interactive sections = FAIL.

---

## 40. Production hygiene + owner-directed identity QA (v4.8.1)

When module `19-PRODUCTION-HYGIENE-IDENTITY.md` is enabled, perform two separate audits.

### Public-output residue audit

For logged-out rendered HTML/head/visible UI assert:

```text
public_internal_build_terms = 0
public_debug_comments = 0
accidental_generator_metadata = 0
stale_previous_project_identity = 0
```

Search/classify build-specific terms and markers, but do not remove legitimate licence, factual, legal or subject-matter text merely because a keyword matches.

### Owner-directed identity audit

If the user supplied a real concept/editorial owner:

```text
owner_identity_status = OWNER_SUPPLIED
meta_author_matches_owner = yes on applicable editorial pages
schema_author_matches_owner = yes where Person author is used
visible_credit_matches_owner = yes when configured
publisher_remains_coherent = yes
legal_identity_not_invented = yes
```

PASS means the real owner's editorial direction is represented consistently. It does not require or permit a false `human-only/no-tools` claim.

### Bespoke-output audit

Compare the site's `AUTHORED SITE FINGERPRINT` with available recent unrelated builds. `FIX_REQUIRED` when the site is effectively the same wireframe/voice/visual system with only superficial token changes.

Do not use external AI-detector scores as a release target.



## 45. DOMAIN MAILBOX CONTACT GATE (v5.7)

For every factory-generated primary website email:

```text
email_shape = {locale_natural_role}@{DOMAIN}
normalized_email_host == normalized_canonical_DOMAIN
generated_email_localpart != placeholder
contact_email_source_mode = SITE_DOMAIN_ROLE
contact_email_status = SYNTHETIC_GEO_CONTACT until owner verification
```

Blocking:
- generated primary email uses Gmail/Outlook/other off-domain host;
- host differs from normalized canonical site `DOMAIN`;
- generated value contains a scheme/path/port because `DOMAIN` was not normalized before mailbox construction;
- local-part is `test`, `demo`, `example`, random hash, build ID or awkward duplicated brand string;
- Contact, footer, legal or Global Text disagree on the public email;
- synthetic domain mailbox is described as verified/deliverable without owner confirmation.

Allowed override:
- exact `OWNER_SUPPLIED` or `VERIFIED` email explicitly intended for publication, even if its host differs from `DOMAIN`.

Example:

```text
DOMAIN = wonparyn.org
PASS generated: kontakt@wonparyn.org
FAIL generated: wonparyn.guide@gmail.com
```

Runtime/static QA must compare visible email + `mailto:` target (when rendered) + Global Text value + Contact Profile host. For factory-generated primary email, the only accepted source mode is `SITE_DOMAIN_ROLE`; no freemail/off-domain fallback is permitted.

<!-- BUNDLE-MODULE-END: 10-QA-RUNTIME.md -->

---

<!-- BUNDLE-MODULE-START: 11-VISUAL-QA.md -->

# LEGACY MODULE: 11-VISUAL-QA.md

# VISUAL QA — GOLDEN BAR

**Version:** 5.4  
**Role:** відсікти технічно валідні, але слабкі/повторювані дизайни і thin-content presentation

---

## 1. Головний принцип

“Працює” не означає “якісно”.

Якщо screenshot суттєво слабший за Golden Sites:
`FAIL`.

---

## 2. Golden mapping

Перед review записати:
- primary Golden reference;
- secondary Golden reference;
- які принципи були використані;
- чому новий сайт не є clone.

---

## 3. First viewport gate

Перевірити:
- чи є clear brand/header;
- чи hero readable;
- чи media meaningful;
- чи CTA видно;
- чи наступний content moment не надто далеко;
- чи немає великої purposeless пустоти.

FAIL якщо перший екран відчувається як:
- unfinished;
- giant headline poster;
- blank canvas;
- random illustration demo.

---

## 4. Typography

FAIL:
- H1 фізично домінує над усім сайтом;
- oversized line breaks виглядають випадково;
- body дрібний;
- contrast слабкий;
- all-caps надмірний;
- type system не відповідає Golden family.

---

## 5. Density rhythm

Потрібна зміна щільності:
- hero;
- compact strip;
- rich media;
- content block;
- catalog;
- trust;
- finale.

Усі секції з однаковим vertical rhythm = монотонність.

---

## 6. Media recurrence

Для gaming:
- media не зникає після hero;
- visual storytelling продовжується;
- homepage має щонайменше 4 meaningful non-hero media moments;
- key internal pages мають 2–3 visual moments;
- catalog/library мають visual value;
- background SVG/pattern system формує єдину visual мову.

---

## 7. Cards

FAIL якщо:
- майже весь сайт = однакові прямокутники;
- картки однакового розміру без narrative reason;
- лише background color відрізняється;
- card text generic.

---

## 8. Whitespace

Whitespace має:
- створювати hierarchy;
- давати breathing room;
- підтримувати media.

Не має:
- компенсувати відсутність content;
- віддаляти CTA;
- створювати пусту половину viewport.

---

## 9. Cookie/consent visual

Має:
- відповідати Design DNA;
- бути компактним;
- не перекривати primary CTA;
- читатися;
- мати clear dismiss/preferences;
- працювати mobile.

Generic black rectangle = FAIL.

---

## 10. Internal pages

Не лише Home.

Visual QA:
- domain pages;
- About;
- legal article;
- catalog/guide;
- 404.

Legal може бути спокійнішим, але все одно branded/readable.

---

## 11. Mobile visual

Mobile:
- intentional order;
- media crop;
- type scale;
- spacing;
- CTA;
- navigation;
- no desktop leftovers.

---

## 12. Rejection conditions

Blocking:
- design не відповідає жодній Golden family;
- gaming site автоматично став cartoon або random cyber;
- visual asset budget не відчувається;
- screenshot виглядає “пусто”;
- hero занадто великий;
- weak content hierarchy;
- cookie UI поганий;
- internal pages shallow;
- modernity досягнута лише кольором/large type.

---

## 13. Acceptance question

Перед RELEASE відповісти:

> Якби цей сайт стояв поруч із 7 Golden Sites у одному портфоліо, чи виглядав би він як продукт тієї ж production maturity?

Якщо ні — `FIX_REQUIRED`.


---

## 14. Contact-page visual gate

Contact page не повинна виглядати як службова заглушка.

Очікується:
- branded hero/background;
- contact details grouping;
- support/operator distinction;
- contextual visual or map only when location is real;
- legal/privacy links;
- coherent footer handoff.

---

## 15. Internal-page fullness gate

FAIL якщо:
- усі внутрішні сторінки мають однаковий текстовий шаблон;
- немає background variation;
- немає media beyond hero;
- 4–7 meaningful blocks не досягнуті без обґрунтування;
- сторінка виглядає недоробленою поруч із Golden corpus.


---

## 16. Section-image quality gate

Generated/source image для section проходить PASS лише якщо:

- subject відповідає змісту section;
- composition підтримує layout;
- focal point не конфліктує з text overlay;
- palette/lighting/material treatment узгоджені з Design DNA;
- image має достатню detail quality;
- немає AI artifacts, gibberish text, watermark, accidental logo;
- visual не виглядає як generic stock filler;
- image не повторює hero без narrative reason.

### Semantic placement

Приклади:

- control section → control/device/interaction visual;
- progression section → rhythm/route/progression visual;
- product/category section → product/category scene;
- process section → sequential/process visual;
- About → brand/source/workflow/editorial visual;
- Contact → communication/location abstraction; map/photo тільки якщо location реальна;
- Legal → restrained branded decorative support, не fake office photography.

FAIL якщо visual красивий сам по собі, але не має зв'язку із section.

---

## 17. Cross-page image coherence

Перед VISUAL_PASS перевірити:
- hero + section images виглядають як одна visual family;
- однаковий rendering style там, де це потрібно;
- variation існує без style chaos;
- same seed/composition не відчувається reused;
- mobile crops зберігають focal points;
- Home не забрала всі сильні assets, залишивши internal pages порожніми.

---

## 18. Contact realism visual gate

Contact block FAIL якщо:
- `.example`;
- `000 000 000`;
- `Rua Exemplo` / `Example Street`;
- obvious placeholder text;
- contact values стилістично виглядають як debug/staging data.

Synthetic GEO contact може виглядати як нормальний production contact block, але visual layer не повинен називати його:
- verified;
- registered office;
- official hotline;
якщо такого статусу немає.

---

## 19. Split-section proportion gate (v4.4 patch)

For text/media split sections, reject if:
- headline occupies overwhelming majority of attention and media feels undersized;
- image is too small relative to typographic block;
- empty neutral background overwhelms both;
- section looks like unfinished wireframe rather than polished editorial layout.

Preferred outcome:
- strong headline;
- readable supporting copy;
- meaningful image with comparable visual weight;
- balanced negative space.

## 20. Image clarity gate

Reject visuals that show:
- blur/fog without reason;
- mushy textures;
- distorted objects;
- random overglow;
- accidental text or UI artifacts baked into imagery.

## 21. Trust/engagement visual completeness

Full-site visual PASS expects visible presence of:
- trust/proof UI appropriate to the business model; in `OFFICIAL_GAME_STUDIO`, synthetic customer/player testimonials are not an acceptable substitute for sourced proof;
- consent UI that looks designed, not like a generic dark block;
- contact cards/blocks that feel natural and complete.


---

## 22. Wide desktop composition check

Review at standard desktop and wide/4K-class viewport widths.

Reject if widening the viewport causes:
- heading scale to overpower the media;
- excessive empty side/vertical space;
- media to appear like a thumbnail beside typography;
- content cluster to feel lost inside the canvas.


---

## 23. GEO typography visual gate (v4.5)

Before `VISUAL_PASS`, typography must be reviewed in the **actual target language**.

Verify:
- body text is comfortable for several paragraphs;
- H1/H2 remain proportionate with imagery;
- locale-specific accented characters look balanced;
- navigation labels remain readable;
- bold/italic weights are coherent;
- no unexpected fallback glyphs;
- mobile typography remains comfortable;
- wide desktop does not turn the display face into an oversized poster;
- the type direction is supported by the recorded GEO web research.

Reject if:
- font was chosen only because it looked good in English;
- diacritics feel mismatched;
- body reading is tiring;
- a trendy font fights the content;
- headings visually overpower media;
- fallback materially changes layout;
- no GEO typography research record exists.


---

## 24. Hybrid imagery coherence gate (v4.6)

A site that mixes generated and reusable web imagery must still feel like one visual system.

Verify:
- palette/temperature is reasonably coherent;
- crop language is coherent;
- corner/frame treatment is controlled by the site, not randomly baked into images;
- detail/contrast does not jump chaotically between sections;
- realistic web photography and generated art have intentional roles;
- no section looks like a random stock-photo insert.

Reject if mixed sourcing creates obvious style fragmentation.

## 25. White-edge / matte visual gate

Inspect hero and every major section image for:
- thin white strip on any edge;
- white separator from a source collage;
- accidental export canvas;
- visible matte inside rounded media;
- white halo around transparent foreground;
- double framing (baked frame + CSS frame);
- accidental letterbox/pillarbox.

If no frame was explicitly intended, any such visible artifact = `VISUAL_FAIL`.

A legitimate white object/background inside the artwork is allowed; the failure is an **unintended geometric edge artifact**.

---

## v4.5.11 patch — visual acceptance + source coherence

A page does not visually PASS if it relies mostly on web-sourced imagery while generated thematic imagery is weak or absent.

### Mandatory mix acceptance
For Home + key internals:
- generated original thematic images should visually lead the site;
- target share >= 65% of meaningful visible raster section images;
- reusable web assets may support authenticity, but must not dominate.

### Rejection triggers
Reject a page/image set if:
- generated images are too few to establish the site's own visual identity;
- external images overwhelm the editorial/system look;
- a generated image includes border/matte/white frame;
- imagery is semantically right but SEO attributes remain incomplete in rendered DOM.


---

## 26. Cross-site color uniqueness visual gate (v4.7)

Before `VISUAL_PASS`, compare the site's full-page screenshot and palette fingerprint with recent factory sites.

### Reject when
- the site immediately recalls a prior site's color world;
- same dominant background family and same accent family repeat;
- only minor HEX changes separate two otherwise identical palettes;
- repeated teal/cream/coral, navy/lime/sand, purple/cyan or another recurring combination becomes a factory habit;
- cards, CTA, hero and footer reproduce the same color-role pattern as a recent site.

### PASS requires
- clear independent visual identity at first glance;
- a materially different dominant/accent relationship from the nearest prior site;
- at least 3 major color-fingerprint dimensions differ unless owner brand constraints prevent it;
- generated imagery is art-directed to the new site's palette rather than carrying the previous site's palette forward;
- accessibility and content readability still pass.

This is a cross-project gate, not only an intra-page consistency check.


---

## 27. Global Text edit resilience visual gate (v4.8)

The design must tolerate realistic text edits made through `global-text.json`.

Test representative changes:
- hero title +25–40% longer;
- CTA label longer;
- nav label longer;
- legal paragraph longer;
- FAQ answer longer.

Reject if ordinary text edits cause:
- overlap;
- clipped text;
- broken card height;
- button overflow;
- navigation collision;
- media/text imbalance;
- hidden content.

Global Text editability is not complete if the layout only works for the originally generated exact strings.

---

## 28. Professional photoreal visual gate (v4.9)

Unless illustration/cartoon style is explicitly requested or justified in Design DNA, major generated raster imagery must read as **professional custom photography or photoreal cinematic image-making**.

PASS signals:
- believable real-world lighting;
- convincing materials/skin/surfaces;
- natural lens and depth behavior;
- intentional editorial/commercial composition;
- premium retouching;
- section-specific subject and environment;
- image does not immediately read as generic AI art.

Reject by default:
- childish/cartoon treatment;
- cute mascot proportions;
- toy/diorama/plastic 3D look;
- game-promo CGI gloss without photographic credibility;
- flat illustrated backgrounds used as major media;
- over-smoothed faces/materials;
- impossible anatomy/objects;
- synthetic stock-photo smiles/poses;
- hyper-saturated fantasy lighting used without topic justification.

For game/app guides, photoreal/cinematic reinterpretation may use the source's objects, mechanics, environment and mood as reference intelligence without copying protected key art.

### Web-sourced visual cleanliness
A web-sourced asset should visually behave like a native site asset after ingestion.
Reject unnecessary visible `Source`, `Photo by`, source URL or source-link UI when the licence does not require it.



---

## 29. Section variability + cross-site composition gate (v5.0)

The site must not only have different content; its **section grammar must visibly vary**.

### Same-page PASS
For Home and rich internal pages:
- adjacent sections do not read as the same component repeated;
- exact outer section composition fingerprints do not repeat by default;
- card grids do not dominate the whole page;
- media position/dominance changes intentionally;
- surface/background rhythm changes without becoming chaotic;
- section transitions feel authored rather than mechanically stacked.

### Cross-page PASS
Compare Home + at least two key internal pages:
- intro/hero geometry is not identical on all three;
- dominant content pattern differs;
- closing CTA/related-content treatment is not cloned everywhere;
- page-specific purpose remains visible even in grayscale/wireframe view.

### Cross-site PASS
When recent `SITE COMPOSITION FINGERPRINT` artifacts are available:
- compare against recent factory sites;
- reject strong unrelated-site similarity above the module-18 threshold;
- changing only colors, fonts or images does not count as layout uniqueness;
- mutate high-impact composition dimensions and rerun screenshots.

### Anti-random-chaos gate
Reject novelty that causes:
- broken reading order;
- arbitrary alignment changes;
- inaccessible interactions;
- excessive motion;
- confusing content hierarchy;
- mobile layouts that feel like accidental collapse.

Target:

```text
VARIED SECTIONS
+ COHERENT DESIGN DNA
+ CLEAR USER JOURNEY
```



---

## 30. Content-density and connected-composition gate (v5.1)

Reject a section when:
- whitespace visually dominates without a deliberate editorial/media reason;
- a large title and small body are separated into distant zones that do not read as one composition;
- the eyebrow/kicker appears detached from its heading;
- non-hero typography is oversized relative to information density;
- section height feels designed to fill a viewport rather than serve content.

PASS should feel:
- connected;
- intentional;
- information-dense enough for its footprint;
- breathable without becoming empty.

Review at wide desktop because these failures often hide at smaller widths.

---

## 31. Major-image uniqueness visual gate (v5.1)

For the full site, review hero + every major section visual side by side.

Reject when:
- exact image repeats;
- same source image is shown through different crops;
- several images were clearly cut from one composite/contact sheet;
- two generated images use effectively the same scene, board/object arrangement, camera angle and lighting;
- repeated imagery makes different sections feel like the same section.

The test is perceptual, not filename-based.

Default target:

```text
major section visuals with distinct source/scene = 100%
unjustified major exact/derivative reuse = 0
```

Shared icons, decorative motifs and intentional small repeated thumbnails are excluded.

---

## 32. Footer uniqueness visual gate (v5.1)

Compare footer against recent unrelated factory sites when references/fingerprints are available.

Reject if the same recognizable footer template repeats:
- same number/proportions of columns;
- same brand position;
- same nav/contact/legal order;
- same CTA placement;
- same bottom-bar arrangement;
- with only colors/fonts changed.

PASS:
- footer remains coherent with the same site's Design DNA;
- at least two high-impact geometry/grouping dimensions change from a too-similar recent footer;
- semantic findability and mobile readability remain strong.

The footer is allowed to be visually quieter than the body, but it must still feel designed for this site.



---

## 33. Expanded section-library utilization gate (v5.2)

A large archetype library is useful only if the factory actually uses it.

For Home + two representative internal pages record:
- eligible macro families per section;
- selected family;
- page rhythm recipe;
- unique macro family ratio;
- sequence bigrams/trigrams;
- dominant topology count;
- recent-site family usage when fingerprints exist.

Blocking/fix conditions:
- the same comfortable 5–10 macro families dominate consecutive unrelated sites despite multiple equally valid alternatives;
- Home reproduces a recent unrelated 3-section macro subsequence without semantic necessity;
- three consecutive sections share the same dominant topology;
- page looks structurally identical in grayscale/wireframe after only colors/images are changed.

For rich Home with 7+ sections, target macro-family uniqueness ratio is normally `>= 0.80`.

## 34. Adult premium imagery gate (v5.2)

For general-audience visual-rich builds, inspect hero + every major raster at normal size and as a contact sheet.

Reject major imagery that reads as:
- childish/cute by accident;
- toy/diorama/plastic 3D;
- cheap mobile-ad CGI;
- generic low-detail AI fantasy;
- oversmoothed synthetic stock;
- whole website/mockup screenshot when a scene asset was requested;
- repeated scene/camera/light setup disguised as different subjects.

PASS expects premium editorial/commercial/cinematic image-making appropriate to the topic.

## 35. Bespoke SVG depth gate (v5.2)

When the content contains structured mechanics/process/economy/route/comparison concepts, verify the build considered original SVG/diagram media.

A major SVG counts only when:
- it explains/reinforces content;
- it is not merely a generic icon enlarged;
- topology/geometry is project-specific;
- text remains readable/responsive;
- mobile simplification works;
- major visual signature does not duplicate a recent/unrelated major SVG without justification.

Do not force SVG where photography/text communicates the concept better.

## 36. Section background quality gate (v5.2)

For each distinctive background treatment verify:
- declared background family/asset;
- readable contrast-safe text zone;
- no accidental competition with heading/body;
- no repeated major illustration across unrelated sections;
- mobile simplification/removal is intentional;
- motion respects reduced-motion preferences;
- background contributes hierarchy/atmosphere rather than decorative noise.

A rich site with every section on flat solid fills should enter visual review unless intentional minimalism is part of Design DNA.
A site with every section using a busy illustrated background also fails rhythm/coherence.

## 37. Visual medium rhythm gate (v5.2)

Inspect the sequence of dominant visual media across Home:
- raster;
- SVG/diagram;
- background illustration;
- data/table/list;
- quiet text-led moment.

Reject monotonous sequences where one medium is used for nearly every meaningful section despite available semantic alternatives.

For visual-rich gaming/editorial Home, use the module-16 target mix as a planning reference, not a filler quota.

## 38. Premium-preservation fix-loop gate (v5.2)

When comparing versions of the same site, reject an update that fixes a technical issue but materially downgrades visual quality.

Examples:
- strong cinematic photo replaced by weak generic SVG;
- detailed background removed leaving a large empty field;
- unique visual replaced by low-detail filler merely to satisfy reuse checks;
- premium image compression visibly damages detail.

A successful fix must preserve or improve the established visual quality tier.



## 39. Live-reference diversity gate (v5.3)

When `LIVE UIUX RESEARCH MANIFEST` exists, Visual QA verifies that research improved variety without producing a clone.

PASS requires:
- research references are current/relevant enough for the claim made;
- final page does not reproduce one reference's distinctive layout/sequence;
- reference-derived traits were recombined through module-18 grammar;
- the final page still belongs to this site's own Design DNA.

Reject:
- recognizable reference cloning;
- exact section sequence borrowed from one external site;
- exact unusual composition with only color/copy changed.

## 40. Modifier-stack diversity gate (v5.3)

For Home + representative internal pages record:

```text
macro_family
modifier_stack
adjacent_modifier_overlap
page_modifier_signature
recent_site_modifier_similarity
```

Default blocking/fix conditions:
- exact modifier stack repeats on the same rich page without semantic reason;
- three consecutive sections share essentially the same shell + content flow + media integration;
- internal pages differ only in copy while retaining one shared renderer silhouette;
- new site is a grayscale/wireframe clone of a recent unrelated build.

If the nearest recent-site silhouette is too similar, mutate at least `5` high-impact structural dimensions.

## 41. Rich-content presentation gate (v5.3)

More content must improve perceived usefulness, not create a wall of text.

Review:
- section-by-section information gain;
- heading hierarchy;
- line length;
- paragraph rhythm;
- lists/tables/diagrams used semantically;
- visual rests;
- internal navigation;
- whether the page feels complete at the bottom rather than abruptly ending.

Reject:
- repeated paragraphs with slightly different wording;
- 1000+ words squeezed into 2–3 giant text blocks;
- every section using the same text-left/media-right pattern;
- excessive typography scale that becomes more oppressive as content grows;
- filler cards created only to distribute text.

## 42. Current-web research QA fields

Record in QA report:

```text
live_research_used: yes/no
research_reference_count
live_site_reference_count
curated_pattern_source_count
research_freshness_summary
live_pattern_candidate_count
selected_research_influenced_sections
external_reference_clone_check
```

These fields are internal QA provenance, not public marketing claims.



## 39. Interaction visual-quality gate (v5.4)

Visual QA reviews interaction as part of page composition, not as a separate widget checklist.

Reject when:
- every content cluster becomes a slider/accordion;
- identical carousel/tabs geometry repeats across several pages;
- hover effects make the page feel noisy or cheap;
- generic card-lift hover dominates the visual language;
- an interactive section looks empty before user action;
- selected/active states are visually ambiguous;
- tabs/sliders introduce large layout jumps;
- motion distracts from nearby reading;
- mobile fallback feels like a broken desktop widget.

Prefer a varied interaction rhythm such as:
`static editorial → rail → static media → tabs → quiet text → accordion → CTA`
rather than interactive widgets back-to-back.

Hover/focus effects should reinforce hierarchy, material, direction or affordance. They are not mandatory decoration on every element.



## 43. HARD DIVERSITY RELEASE GATE (v5.5)

For every new unrelated full-site BUILD, `HARD_DIVERSITY_MODE = ON` is required.

### 43.1. Required report

QA must receive `HARD_DIVERSITY_REPORT` with:

```text
role_candidate_counts
selected_topology_clusters
selected_macro_families
pairwise_adjacent_distances
hero_recent_distances
footer_recent_distances
home_recent_silhouette_distance
reroll_count
new_grammar_count
cross_site_history_available
```

Missing report = `FIX_REQUIRED`.

### 43.2. Same-page blockers

Reject when:
- Hero and section 2 share the same dominant topology cluster;
- adjacent major sections have structural distance `< 0.62` without explicit semantic necessity;
- a rich Home with 7+ sections has fewer than `6` topology clusters when enough valid patterns exist;
- one split/card topology visibly dominates the page;
- two different layout IDs produce effectively the same neutral wireframe;
- final CTA reuses the Hero's stage silhouette;
- desktop variation disappears into one repeated mobile stack.

### 43.3. Cross-site blockers

When recent fingerprints are available, reject when:
- new Hero structural distance is `< 0.72` from any of the last 8 comparable unrelated Heroes and alternatives exist;
- new Footer distance is `< 0.68` from any of the last 6 comparable unrelated Footers and alternatives exist;
- Home silhouette distance is `< 0.68` from the nearest recent unrelated Home;
- recent-role hard exclusion was bypassed without candidate-scarcity evidence.

If recent history is unavailable, record that limitation; never invent a comparison PASS.

### 43.4. Randomness audit

For roles with a sufficiently large eligible distant pool:
- final selection must not always be the highest semantic-score candidate;
- selection must occur after grouping by materially different topology clusters;
- seeded random draw must be reproducible for the same site seed;
- changing the new-site nonce should be capable of choosing a different eligible topology.

A large library with deterministic safe-family gravity = `FAIL`.

### 43.5. Neutral silhouette review

Review Home + two key internal pages in a neutral representation:
- colors removed;
- imagery reduced to neutral blocks;
- brand typography neutralized;
- borders/shadows simplified.

The pages must remain visibly distinct from one another and, when history is available, from recent unrelated sites.

If the reviewer can still identify the same repeated template, return to composition selection and reroll/mutate.

### 43.6. Longer build time is acceptable

`REROLL`, `MUTATE_LAYOUT`, and `SYNTHESIZE_NEW_GRAMMAR` are valid fix-loop outcomes.
Do not lower the diversity threshold merely to finish faster.



## 44. ALL-PAGES HARD DIVERSITY GATE (v5.6)

Hard Diversity PASS is site-wide, not Home-only.

### 44.1. Managed-page coverage

For every managed public page assert:

```text
page_composition_nonce = present
page_rhythm_family = present
selected_topology_clusters = present
per_page_reroll_count = recorded
mobile_page_rhythm_signature = present
```

Missing data on an internal page = `FIX_REQUIRED`.

### 44.2. Key-page cross-comparison

Neutral-wireframe compare at minimum:
- Home;
- About;
- Contact;
- two key domain/editorial pages;
- FAQ/resources when present.

Blocking by default:
- exact opening macro family repeated across key pages while alternatives existed;
- same dominant topology controls all compared pages;
- identical 2/3-section sequence appears across unrelated-purpose pages;
- one shared internal-page skeleton survives after neutralizing color/type/images;
- key-page pair silhouette distance `< 0.62` without documented semantic constraint.

### 44.3. Legal-page comparison

Review Privacy + Terms + Cookies.
They may share reading conventions and legal navigation, but reject:
- exact whole-page clone with only headings/body replaced;
- same intro/TOC/article/closing geometry on all three when multiple legal-safe families were eligible;
- novelty that harms legal readability.

Legal accuracy and scanning remain higher priority than novelty.

### 44.4. Per-page topology targets

For key pages with `4+` meaningful sections:

```text
unique_topology_cluster_ratio >= 0.75 normally
exact_section_fingerprint_repeat = 0
```

For rich key pages with `6+` sections:

```text
unique_topology_cluster_ratio >= 0.80 normally
```

Home keeps its stricter threshold.

### 44.5. Mobile cross-page gate

At representative mobile widths compare the full-page rhythm of Home + key internals.
Reject when all pages collapse into essentially one repeated mobile template despite different desktop grammars.

Still require:

```text
horizontal_overflow = 0
focus_order = coherent
essential_content_present = yes
```

### 44.6. Random-selection evidence

For each key page with a healthy eligible pool, QA records:
- eligible role candidates;
- topology clusters considered;
- random cluster selected;
- random layout selected;
- rerolls triggered by similarity;
- final selection rationale limited to semantic/accessibility/mobile validity, not subjective safe-family preference.

A site where only Home uses stochastic selection and internal pages fall back to deterministic templates = `FAIL`.



## 46. OFFICIAL GAME STUDIO BUSINESS MODEL GATE (v5.8)

When `business_model_mode = OFFICIAL_GAME_STUDIO`, RELEASE requires a coherent first-party studio/product narrative across the entire site.

### 46.1 Required profile

```text
business_model_mode = OFFICIAL_GAME_STUDIO
studio_brand = present
game_name = present
source_developer_name = recorded when source exposes it
developer_relationship_status = resolved or explicitly INPUT_REQUIRED
ownership_evidence_type = recorded
first_person_creator_claims_allowed = yes/no
commercial_goal = PROMOTE_GAME
primary_conversion = PLAY_OR_DOWNLOAD_GAME
BUSINESS_MODEL_CONTENT_MAP = complete
```

### 46.2 Ownership truth blockers

Blocking:
- `we created`, `our game`, `our studio developed`, `official developer site` or equivalent appears while relationship status is unresolved/conflicting;
- source developer differs from the studio/domain brand and no owner-supplied/verified relationship explains it;
- domain-derived brand is presented as a registered/legal company without owner-supplied/verified legal identity;
- creator/developer/publisher schema relation exceeds the evidence state;
- official-store/support relationship is misrepresented.

A desired marketing persona never overrides source/owner truth state.

### 46.3 Whole-site narrative audit

Review at minimum:
- Home;
- Game/Product page;
- Development/Behind-the-scenes page or equivalent process sections;
- About/Studio;
- FAQ;
- Contact/Support;
- footer;
- SEO head/schema on representative pages.

Reject mixed-model output such as:
- Home says `our game` while About says `independent editorial guide`;
- footer publisher is an editorial brand while product pages claim a studio;
- Contact treats the verified same-studio game support as unrelated third-party support;
- internal pages revert to outsider review/affiliate language.

### 46.4 Commercial-model coverage

The site must visibly communicate, without repetitive filler:
- who the studio/brand is;
- what game it created/owns **when that relationship is resolved**;
- what the game does;
- design/development/process story supported by evidence;
- player value/features;
- support route;
- play/download/store conversion.

Missing a meaningful product conversion path on a promotional studio site = `FIX_REQUIRED`.

### 46.5 Development-story evidence gate

For any `how we built it` / development process copy, classify claims as:

```text
OWNER_SUPPLIED
SOURCE_VERIFIED
HIGH_LEVEL_CONFIRMED_PROCESS
UNSUPPORTED
```

`UNSUPPORTED` exact chronology, team size, engine/toolchain, budgets, dates, milestone anecdotes, testing numbers or roadmap promises = `FAIL`.

### 46.6 Trust/review gate

In `OFFICIAL_GAME_STUDIO` mode:
- synthetic editorial/player/customer testimonial cards = `FAIL`;
- sourced store/player reviews or press quotes are allowed with accurate attribution;
- if no real reviews exist, use non-testimonial trust/product/development proof.

### 46.7 SEO / Global Text parity

Assert:

```text
visible studio brand == SEO publisher brand
creator claims == developer_relationship_status
Global Text business-model keys = present
footer/product relationship = coherent
store CTA destination = verified/current
legal operator claims <= owner/verified legal data
```

Any business-model drift between visible copy, schema, metadata and legal/contact state = `FIX_REQUIRED`.



## 47. STUDIO STORY / DEVELOPMENT PAGE GATE (v5.9)

When `business_model_mode = OFFICIAL_GAME_STUDIO`, verify that the business model is visible through page architecture and thematic depth, not only through pronouns.

### 47.1 About / Studio gate

About must clearly establish, when creator relationship is resolved:

```text
studio identity = clear
game relationship = clear
product/game description = present
creative/product approach = present at truthful level
unsupported corporate biography = 0
play/download or game continuation = present
support/contact continuation = present
```

Reject a generic About page that could belong to any unrelated company after swapping the logo/name.

### 47.2 Development-topic coverage

For a rich official game site, require meaningful creator/product topic coverage across internal pages or deep sections. Normally expect at least `2` distinct development/product-design jobs in addition to About + basic Product/FAQ, when the source/owner facts support them.

Examples:
- mechanics design;
- controls & feel;
- progression/level design;
- art direction;
- balancing/testing;
- development/making-of;
- release/iteration.

Do not fail a source-limited project for missing unsupported history. Instead record `owner_data_gap` and choose a factual product/system page.

### 47.3 Page-role anti-clone

Reject when:
- About, Development, Mechanics and Game pages all contain the same generic `intro → features → CTA` information story;
- internal pages are merely player guides with studio pronouns pasted in;
- several pages repeat the same `we created the game` paragraph without new information gain;
- page titles differ but their `page_business_role` is effectively identical.

### 47.4 Creator-intent evidence audit

For each public first-person historical/motivational statement, record one of:

```text
OWNER_SUPPLIED_CREATOR_FACT
SOURCE_VERIFIED_CREATOR_FACT
SOURCE_VERIFIED_PRODUCT_FACT
HIGH_LEVEL_PRODUCT_EXPLANATION
EDITORIAL_INFERENCE_LABELLED
UNSUPPORTED_DO_NOT_PUBLISH
```

Public `UNSUPPORTED_DO_NOT_PUBLISH` count must equal `0`.

### 47.5 Conversion-path audit

Across representative pages verify contextual continuation:

```text
Home → play/download
About → game/product
Development → finished game / related dev topic
Mechanics/Controls → play/game page
FAQ/Support → help + game/store where appropriate
```

The exact same CTA label and section treatment on every page is not required and is discouraged.

### 47.6 Required artifact

```text
STUDIO_STORY_MAP = present
selected_page_topics = non-empty
creator_claim_evidence = complete
owner_data_gaps = recorded
related_page_graph = coherent
```

Missing `STUDIO_STORY_MAP` on a rich `OFFICIAL_GAME_STUDIO` BUILD = `FIX_REQUIRED`.


## 48. HEADER + NAVIGATION VARIATION GATE (v6.2)

This gate verifies both structural header diversity and randomized role-safe navigation naming.

### 48.1. Required artifacts

For every new full-site BUILD require:

```text
header_composition_nonce = present
navigation_copy_nonce = present
navigation_lexical_profile = present
domain_lexical_salt = present
resolved_navigation_locale = present
locale_lexical_lane = present
NAVIGATION_LOCALE_LEXICON = complete
menu_lexical_fingerprint = present
HEADER_COMPOSITION_MANIFEST = complete
NAVIGATION_COPY_MANIFEST = complete
```

For each primary destination record:

```text
page_key
semantic_role
eligible_candidate_count
selected_nav_label
selected_label_family
resolved_destination_id
resolved_destination_url
```

### 48.2. Header structure gate

Reject when:
- the build silently falls back to one universal brand-left/nav-right/CTA-right header while multiple valid families exist;
- selected family is not present in the manifest;
- brand/nav/action geometry differs only cosmetically from another family ID;
- label set does not fit the selected topology;
- mobile transformation is missing;
- opened mobile menu clips labels or creates page overflow;
- DOM/focus order contradicts the visual order.

Representative desktop + mobile screenshots must include the header.

### 48.3. Navigation synonym gate

For each main-nav label:

```text
semantic_match = PASS
locale_naturalness = PASS
normalized_duplicate = false
visible_label_nonempty = true
resolved_destination = expected page_key
```

For common roles with `eligible_candidate_count >= 4`, a selector that ignores `navigation_copy_nonce` and always emits the same canonical default is a diversity failure.

Do not require novelty when the locale/role genuinely has only one or two clear labels.

### 48.4. Whole-menu meaning gate

Read the menu without page bodies.
A user should still be able to predict destinations reasonably.

Reject:
- vague marketing slogans used as primary navigation labels;
- two different pages both labelled `Explore`, `Discover`, `Info`, or another collision-like generic term;
- `Support` used for a generic Contact page when the page does not provide support;
- `News/Updates` when no factual update/news content exists;
- `Team` wording when no truthful team context exists.

### 48.5. Page naming separation gate

Assert:

```text
nav_label may differ from page_display_title = yes
nav_label may differ from seo_title = yes
nav_label edit changes canonical_slug = no
nav_label edit changes managed_page_id = no
nav_label edit changes page_key = no
```

Changing `About → Our Studio` in Global Text must leave the same managed destination and canonical unless a separate explicit URL migration is performed.

### 48.6. Same-site update persistence

Ordinary update regression:
1. capture header family, header nonce, nav nonce and selected labels;
2. update the active theme without redesign request;
3. reload public site;
4. assert all four remain unchanged;
5. if a navigation label was manually edited in Global Text, assert that edit survives.

Any silent reselection = `FAIL`.

### 48.7. New-site randomness audit

Using the same semantic site spec but several fixed synthetic new-site nonces, verify the selector is actually nonce-sensitive.

When pools are healthy:
- header selection should produce more than one eligible family across the test nonce set;
- at least several common page roles should produce more than one valid label across the test nonce set;
- destination page keys/IDs remain unchanged.

If different nonces still force one top-ranked header/label set without scarcity, return `FIX_REQUIRED`.

### 48.8. Responsive fit blockers

Blocking:

```text
header_horizontal_overflow > 0
clipped_primary_nav_label > 0
offscreen_header_action > 0
mobile_menu_unreachable = true
mobile_menu_label_overlap = true
```

Do not solve a fit failure by replacing every varied label with the shortest canonical word. Reroll the affected label/header family while preserving semantic quality.


### 48.9. Same-locale lexical diversity audit

When generating a same-locale batch, or when recent same-locale manifests are available, compare visible primary-navigation copy independently from layout.

For a healthy pool:

```text
exact_menu_lexical_fingerprint_repeat = 0
avoidable_high_frequency_role_label_repeat = 0 within current batch while unused clear alternatives remain
max_pairwise_primary_label_overlap <= 0.50 normally when comparable menus contain enough varied roles
```

For a batch of up to `5` PT-PT official-game-studio sites with overlapping page roles, common roles should normally be distributed without replacement from the native PT-PT bank. Example acceptable differentiation:

```text
Site A: O estúdio | O jogo | Desenvolvimento | Perguntas frequentes | Contacto
Site B: Quem somos | Conhece {Game} | Nos bastidores | Dúvidas frequentes | Fale connosco
Site C: Sobre nós | Explora {Game} | Criação do jogo | Perguntas e respostas | Escreva-nos
Site D: A nossa história | A experiência | O processo | Ajuda e respostas | Entrar em contacto
Site E: Por dentro do estúdio | Sobre o jogo | Do conceito ao jogo | Perguntas comuns | Contactar o estúdio
```

These are examples, not a fixed sequence. The actual draw remains nonce-driven after eligibility.

Blocking:
- all same-GEO sites use the same canonical menu despite healthy pools;
- exact complete menu wording repeats inside the current batch;
- the selector repeatedly chooses the same `About/Contact/FAQ` labels while unused native alternatives exist;
- diversity is achieved through awkward, ambiguous or conspicuously creative labels.

If cross-site history is unavailable and sites are not being built together, record:

```text
cross_site_lexical_history_available = false
```

Do not invent a comparison PASS. Still verify nonce/domain-salt sensitivity with synthetic test domains and confirm that label distributions can change without changing destination semantics.

### 48.10. Quiet-naturalness review

Read only the header menu in the target language. PASS requires:
- every label looks normal for a real local website;
- destination meaning is reasonably predictable;
- the menu does not look like a synonym exercise;
- grammatical tone is coherent enough to feel authored;
- differences from another site are subtle rather than gimmicky.

Clarity outranks uniqueness for any individual label; diversity is achieved by the **large bank + distribution strategy**, not by publishing bad synonyms.



### 48.11. Universal GEO / locale lexical gate

Run this gate for **every** target GEO/locale.

Assert:

```text
resolved_navigation_locale == resolved_site_locale
regional_language_variant = recorded
common-role native candidate pools = healthy or explicitly CONSTRAINED
English/default fallback caused by missing locale pack = false
literal-translation warning count = 0
wrong-regional-variant warning count = 0
```

For a healthy common role, normally expect at least `6` eligible natural candidates after filtering; `8+` is preferred. A smaller pool is acceptable only with `LEXICON_POOL_CONSTRAINED` and a clarity reason.

For multilingual GEOs, unresolved locale before nav generation = `FAIL`.

### 48.12. Multi-site same-locale distribution gate

When `N >= 2` sites are generated together for one locale, compare their primary-nav assignments.

Blocking while healthy unused variants remain:
- same common-role exact label reused before pool exhaustion;
- identical full `menu_lexical_fingerprint`;
- pairwise menu exact-label overlap above `0.50` without constrained-pool evidence;
- all sites collapse to the same canonical wording set.

Record per role:

```text
batch_site_count
eligible_pool_size
labels_assigned[]
reuse_before_exhaustion_count
```

Target `reuse_before_exhaustion_count = 0`.

### 48.13. Cross-locale regression sample

A factory release of this engine is not considered tested by PT-only examples. Static QA should exercise at least two materially different locales when modifying navigation lexical logic, preferably with different regional/language characteristics.

<!-- BUNDLE-MODULE-END: 11-VISUAL-QA.md -->

---



## 49. FOOTER CONTENT MINIMALISM GATE (v6.1)

Review the rendered footer independently from the body.

### Required useful layers
Where present in the manifest/runtime, footer may contain:
- brand/logo;
- working navigation;
- legal links;
- concise contact/support;
- real social links;
- official store/play/download link;
- copyright/rights bottom bar.

### Blocking prose defects
For `OFFICIAL_GAME_STUDIO`, reject:
- `independent guide`, `independent review`, `editorial portal` or equivalent positioning;
- source-methodology paragraphs;
- advice-vs-confirmed-feature disclaimers;
- repeated About/mission/product-story paragraph;
- SEO filler written only to occupy footer space;
- visible publisher/editorial-credit prose with no footer-specific user value.

Default assertions:
```text
footer_longform_prose_blocks = 0
footer_repeated_body_narrative = 0
official_studio_independent_positioning = 0
footer_store_link_may_exist = true
footer_links_work = true
footer_bottom_bar_present = true
```

A short descriptor is allowed only when it passes business-model truth, locale naturalness, non-duplication and usefulness checks. `No descriptor` is a valid and often preferred PASS.

### Screenshot regression
Given a footer containing a paragraph equivalent to:
`Independent Polish guide to {Game}. Facts from the official source, practical interpretations...`
plus a valid `{Game} in Google Play` link, expected repair is:
- remove the descriptive paragraph;
- retain the useful store link;
- retain applicable nav/legal/contact/bottom-bar elements;
- rebalance footer geometry without inventing replacement filler copy.


## 50. CLEAN GAMING / ZERO GAMBLING-ASSOCIATION GATE (v6.2)

Run this gate for every normal gaming/app/game-studio build in this project family.

### Pre-build source classification

Require:

```text
clean_gaming_mode = REQUIRED
source_gambling_relevance = NONE
source_vertical_conflict = false
CLEAN_NICHE_EXCLUSION_LEXICON = present for resolved locale
```

If authoritative source materially indicates casino/gambling/betting/wagering/real-money-stake activity:

```text
source_vertical_conflict = true
→ BUILD BLOCKED
→ INPUT_REQUIRED
```

Do not convert the conflict into a public `not gambling` disclaimer.

### Public zero-mention crawl

Scan final factory-controlled public output including:
- rendered visible DOM text;
- header/navigation/breadcrumbs;
- all managed page body text;
- FAQ;
- footer;
- Contact/Support;
- Privacy/Terms/Cookies and consent UI;
- 404/empty states;
- `<title>` / meta description / meta keywords;
- OG/Twitter text;
- JSON-LD human-readable values;
- image ALT/TITLE;
- link TITLE;
- ARIA/accessibility strings;
- JS-rendered public strings;
- persistent Global Text values that are actually rendered or metadata-bound.

For a clean source, target:

```text
casino_semantic_mentions = 0
gambling_semantic_mentions = 0
betting_semantic_mentions = 0
wagering_semantic_mentions = 0
real_money_gambling_mentions = 0
negative_gambling_disclaimer_mentions = 0
```

### Denial language is also a failure

The following are failures when gambling relevance is absent:
- `not a casino`;
- `not gambling`;
- `no betting`;
- `no wagering`;
- `not a real-money game`;
- localized equivalents.

Do not count absence/reassurance as a positive trust feature. The semantic association itself is unwanted.

### Locale-aware semantic scanner

Use concept/phrase matching appropriate to the resolved locale. Do not rely solely on an English list and do not use unsafe substring-only matching.

False-positive guard:
- `bonus` alone is not gambling;
- `reward` alone is not gambling;
- `score` alone is not gambling;
- `random` / `chance` alone are not gambling;
- collectible or virtual game currency alone is not proof of real-money wagering.

Escalate ambiguous cases to semantic review instead of deleting legitimate game content.

### Blocking conditions

`FAIL` when:
- any unrelated prohibited concept appears in factory-generated public copy or metadata;
- a negative casino/gambling disclaimer appears despite no source relevance;
- meta keywords target gambling/casino/betting concepts;
- legal/FAQ introduces an unrelated gambling topic;
- footer contains such positioning;
- a source conflict is hidden or euphemized rather than stopped;
- scanner only checks visible body while metadata/Global Text still contains the association.

### Regression sample

For a source-supported ordinary arcade/mobile game with bonuses, scores and variable layouts:
- describe those mechanics normally;
- require zero casino/gambling/betting/wagering semantic mentions across all public surfaces;
- verify that words like `bonus` and `score` are not falsely rejected;
- inject a test `not a casino` phrase into footer or meta description and require `FAIL`;
- inject a material real-money wagering fact into the authoritative-source profile and require `SOURCE_VERTICAL_CONFLICT`, not silent sanitization.



## 51. HERO / FIRST-VIEWPORT DIVERSITY GATE (v6.3)

Run on Home + at least three key internal pages when present, and on cross-site history when available.

Required hero record per page:

```text
hero_family
hero_topology_cluster
hero_text_anchor
hero_media_topology
hero_title_scale_tier
hero_signature
h1_line_count
h1_visual_height_ratio
primary_cta_visible_in_first_viewport
media_visible_in_first_viewport
```

### Blocking same-site defects

Reject when healthy alternatives existed and:
- Home + all key internal pages use the same left-text/right-media hero skeleton;
- exact `hero_signature` repeats across unrelated page roles;
- representative set contains fewer than `3` materially different hero topology/text-anchor families;
- all key heroes anchor primary copy on the left with no semantic/brand reason;
- one shared renderer visibly survives neutralization of color/image/copy.

### H1 / first-viewport blockers

At representative desktop widths reject when:
- normal Home H1 is materially above the intended `~3.5rem–4.25rem` envelope without a recorded manifesto reason;
- normal internal H1 is materially above `~2.75rem–3.75rem` without reason;
- H1 becomes a large `5+` line wall because scale/measure was not adapted;
- H1 visually dominates most of the first viewport;
- useful lead/CTA/media is pushed away and the hero reads as a giant type poster;
- media is visually reduced to decoration beside a huge headline.

Screenshot perception wins over nominal CSS values.

### Cross-site regression

When recent hero fingerprints exist:
- compare against recent comparable unrelated sites;
- a familiar `giant left headline + right media + CTA row` silhouette must be rerolled/mutated even if content/colors/assets differ;
- changing only image, color, font or border radius does not count as a new hero.

If history is unavailable, record it and test nonce sensitivity across synthetic new-site nonces.


## 52. FOOTER CONTACT + BOTTOM-BAR MICROCOPY GATE (v6.4)

For standard full-site builds, compare Footer against Contact Profile and Global Text.

When resolved for public display, assert:

```text
footer_public_email_visible = yes
footer_public_phone_visible = yes
footer_public_address_visible = yes
footer_contact_values_match_contact_profile = yes
```

Missing phone/address solely because the chosen footer family had no room = `FAIL`; change the composition.

Bottom bar assertions:

```text
footer_bottom_bar_present = yes
copyright_brand_present = yes
copyright_year_resolves = yes
rights_reserved_localized = yes
```

When a secondary bottom-bar slot is used:

```text
footer_utility_phrase_present = yes
footer_utility_phrase_locale_natural = yes
footer_utility_phrase_truth_safe = yes
naked_decorative_arrow_or_icon = 0
```

Reject:
- unlabeled arrow used merely to fill the far-right slot;
- generic `back to top` added by habit when not intentionally designed/useful;
- false security/protection claims;
- repeated factory-identical phrase across available recent unrelated sites when natural alternatives exist;
- long descriptor paragraph masquerading as bottom-bar microcopy.

A genuine back-to-top control is allowed only when it has working behavior, focusability and visible/accessibility labeling.


## 53. FAVICON / SITE-ICON RELEASE GATE (v6.5)

Every full production build must pass a final public-head icon audit.

Collect:

```text
favicon_owner
head_icon_link_count
favicon_url
favicon_http_status
favicon_mime
favicon_decode_status
favicon_dimensions_or_svg_viewbox
apple_touch_icon_url when used
current_brand_match
stale_previous_project_icon
```

Blocking:
- no effective favicon/site icon in final public head;
- icon URL 404/broken/decode failure;
- stale icon from previous site/theme;
- generic unrelated placeholder mark;
- duplicate conflicting WordPress + theme icon owners;
- theme assumes WordPress Site Icon exists but none is configured and no fallback is emitted.

PASS model:

```text
WORDPRESS_SITE_ICON configured intentionally
OR
THEME_FALLBACK brand utility icon set emitted
```

At least one browser-usable icon must resolve successfully; packaged touch/large square renditions should also resolve when declared.

Regression:
1. run with WordPress Site Icon unset → require theme fallback icon in public head;
2. set an intentional WordPress Site Icon → require no conflicting duplicate theme owner;
3. update favicon asset → verify cache-versioned URL/current icon is served;
4. ensure old project icon fingerprint is absent.


## 54. PERSISTENT STRUCTURAL MEMORY RELEASE GATE (v6.6)

Run after final composition/QA for every full new-site BUILD.

Canonical expected outputs:

```text
repository = PingVinni/Landing
per_site_file = site-factory-history/sites/{normalized-domain}.json
history_index = site-factory-history/index.json
```

### 54.1. Pre-build history-read audit

For an unrelated new-site build, record:

```text
structural_history_repository_available
history_index_loaded
history_site_count
recent_comparison_count
same_niche_comparison_count
nearest_structural_match_count
cross_session_history_available
```

If repository/history is unavailable, do not invent comparison results or claim cross-session anti-repeat PASS.

### 54.2. Per-site file completeness

Assert the canonical file contains current-build values for at least:

```text
domain
geo
locale
niche
build_identity
hero
header
footer
home
key_pages
interaction_profile
mobile_profile
site_fingerprint
comparison_summary
revisions
```

For Home + representative key pages, structural records must be rich enough to compare:
- section archetype sequence;
- topology sequence;
- text/content-anchor sequence;
- media-topology sequence;
- surface/card/list rhythm;
- interaction rhythm;
- mobile transformation rhythm;
- neutral silhouette/page fingerprint.

### 54.3. Privacy/content minimization

Reject repository history that stores unnecessary:
- public page copy;
- prompts;
- secrets/credentials/tokens;
- private user data;
- source assets.

Structural fingerprints should be compact comparison metadata, not a site content backup.

### 54.4. Global index update

After the per-site write, assert:

```text
history_index_contains_domain = yes
history_index_site_count = expected
site_fingerprint_in_index = current
recency_order = coherent
frequency_counters = coherent
no_duplicate_canonical_domain_entry = yes
```

### 54.5. Read-after-write verification

Re-fetch both repository files from the target/default branch after write.

Blocking failures:
- create/update call returned success but file cannot be re-read;
- per-site JSON contains a stale fingerprint;
- index does not reference the site;
- same domain has multiple canonical files/entries without an explicit migration reason;
- structural schema invalid;
- write was skipped silently.

PASS state:

```text
STRUCTURAL_MEMORY_WRITE_PASS
per_site_file_verified = yes
history_index_verified = yes
cross_session_structural_memory_persisted = true
```

Failure state:

```text
STRUCTURAL_MEMORY_WRITE_BLOCKED
cross_session_structural_memory_persisted = false
```

Without explicit owner waiver, a full factory `RELEASE PASS` may not be claimed while `STRUCTURAL_MEMORY_WRITE_BLOCKED` is unresolved.

### 54.6. Next-build consumption regression

After persisting a synthetic site:
1. start a second unrelated synthetic build;
2. load the first site's entry through the global index;
3. attempt to reuse the same Hero topology + Home sequence + Footer family;
4. require recent-history exclusion / distance failure;
5. reroll to a materially different structure;
6. verify the second site also writes its own canonical per-domain JSON.

This regression proves the repository is being used as **memory**, not merely as an archive.



## 54. STUDIO-FIRST BUSINESS CONTENT RELEASE GATE (v6.6)

Run when `business_model_mode = OFFICIAL_GAME_STUDIO`.

### 54.1 Business-model visibility

Across Home + representative key pages, verify:

```text
studio_identity_visible = yes
game_is_presented_as_studio_product = yes when truth gate passes
development_design_work_visible = yes
team_approach_visible = yes at truthful level
product_gameplay_explanation = present but not dominant by default
play_download_conversion = present
support_relationship = coherent
independent_editorial_drift = 0
```

A site that could still be mistaken for an independent game guide after replacing the logo = `FIX_REQUIRED`.

### 54.2 Thematic balance

For rich first-party studio builds, review the semantic distribution of non-legal sections. Normally expect the **majority** of thematic depth to come from studio/product/development/design jobs.

Record:

```text
studio_product_development_sections
player_guide_faq_sections
business_model_job_coverage[]
```

Do not fail a source-limited build merely for a numeric ratio, but fail when generic guide content dominates despite enough source/product material to tell a studio story.

### 54.3 Development-story quality

Require at least two materially distinct development/design information jobs on a rich site when the source supports them, for example:
- mechanics design;
- levels/progression;
- controls/feel;
- art direction;
- balancing/testing;
- development framework;
- release/iteration.

Reject if all development content is one vague paragraph repeated across pages.

### 54.4 Team truth gate

Allowed without named-person evidence after creator relationship is resolved:
- aggregate `our team` studio voice;
- shared creative/product principles;
- high-level work descriptions supported by product/source facts.

Blocking without owner/source evidence:
- staff names;
- job titles/responsibilities;
- headcount;
- founder biographies;
- employee quotes;
- fake team portraits presented as real;
- office/history claims.

### 54.5 Situation / challenge truth gate

For each development `situation`, `problem`, `challenge`, or `lesson` classify:

```text
VERIFIED_DEVELOPMENT_EVENT
OWNER_SUPPLIED_DEVELOPMENT_EVENT
DESIGN_PROBLEM_EXPLANATION
UNSUPPORTED_HISTORICAL_ANECDOTE
```

`UNSUPPORTED_HISTORICAL_ANECDOTE > 0` → `FAIL`.

`DESIGN_PROBLEM_EXPLANATION` may describe a product constraint and solution principle, but must not pretend that a specific historical incident occurred.

### 54.6 Page-role uniqueness

Verify that Game, Development, About/Studio and at least two design-discipline pages have different information jobs and do not merely rename the same content.

Fail examples:
- every page = game description + three features + same CTA;
- About = generic marketing paragraph with no studio/product relationship;
- Development = gameplay guide with `we` pronouns added;
- Mechanics/Levels/Controls all repeat the same feature list.

### 54.7 Conversion coherence

Representative paths should support the business goal:

```text
Home → Game / Development / Play
About → Game / Development / Contact
Development → Design topic / Play
Mechanics/Levels/Controls/Art → related design topic / Game / Play
Support → Game / Store / Contact when appropriate
```

Conversion should be contextual; exact same CTA text/geometry across all pages is discouraged.

### 54.8 Old editorial-architecture override

In `OFFICIAL_GAME_STUDIO`, do not fail a build for missing synthetic testimonials or generic guide/catalog/library pages. Those older requirements are superseded by product/development proof and the active first-party business model.


## 55. SEMANTIC VISUAL RELEVANCE + MICRO-ICON RELEASE GATE (v6.7)

Run this gate for every visual-rich gaming/studio BUILD.

### 55.1. Section semantic-match audit

For every major narrative section collect:

```text
page_key
section_key
heading_meaning
paragraph_cluster_summary
visual_job
asset_id
visual_role_family
semantic_match_reason
```

PASS requires the visual to support the actual section topic, not merely the broad site niche.

Blocking examples:
- mechanics, art and testing sections all use generic game-world scenes;
- a development-process image has no visible/process relationship to the copy;
- a team/studio section uses generic office people that are not factual and do not represent the stated creative/process concept;
- an image was selected because it matched palette, but not meaning.

### 55.2. Dedicated major-asset audit

Default targets:

```text
major_asset_exact_reuse_across_unrelated_sections = 0
hero_major_asset_reuse = 0
near_duplicate_scene_reuse = 0
section_visual_brief_present = 100% for major visual-bearing sections
```

A mirrored/cropped/recolored copy of one source remains the same source for this gate.

### 55.3. Visual-role diversity audit

For rich Home with 7+ meaningful sections, when semantically possible:
- at least `4` materially different visual-role families across major moments;
- reject a page dominated by one repeated framed-cinematic-scene treatment.

For key internal pages:
- opening visual is page-specific;
- normally at least `2` further contextual visual moments on rich pages;
- at least one of those differs in role family from the opening.

### 55.4. Adult/premium quality audit

Reject major imagery that looks:
- childish/cartoon by default without source reason;
- toy-like/plastic;
- cheap mobile-ad CGI;
- generic stock/AI filler;
- muddy/blurred/oversmoothed;
- randomly cyber/neon;
- visually unrelated to the paragraph/heading.

Source-authentic playful/cartoon art direction may pass when deliberately required by the actual product.

### 55.5. Iconography manifest gate

Require on rich visual builds when semantic opportunities exist:

```text
ICONOGRAPHY_MANIFEST = present
icon_style_family = coherent
semantic_icon_roles = mapped
mixed_unrelated_icon_styles = 0
stale_previous_project_icons = 0
```

Normal target where useful: approximately `12–24` distinct site-specific small icons/glyphs. A lower count can PASS when content does not justify more; meaningless filler icons must never be created to satisfy the target.

### 55.6. Micro-UI usefulness audit

Inspect feature groups, process stages, fact ledgers, support/contact blocks and section indexes.

PASS if micro-elements improve at least one of:
- scanning;
- grouping;
- sequence comprehension;
- state recognition;
- brand rhythm.

FAIL if:
- every item receives an arbitrary icon with no semantic distinction;
- same icon is reused for unrelated meanings;
- badges imply unsupported status/quality/security;
- micro-decoration competes with headings/body;
- icon-only interactive controls lack accessible names.

### 55.7. Metadata/runtime parity

For each major image verify:
- asset loaded locally;
- final asset subject matches manifest;
- ALT/TITLE describe final subject + section context;
- replaced/regenerated asset did not retain stale ALT/TITLE;
- mobile crop preserves the semantic subject.

For icons verify:
- no broken SVG/sprite references;
- decorative icons are exposed appropriately;
- semantic/interactive icons have correct accessible treatment;
- no icon filename/internal ID leaks publicly.

### 55.8. Regression cases

#### VISUAL-006 — generic scene repeated for every topic
Given Home sections for `development`, `mechanics`, `art`, `testing`, assigning near-identical cinematic game scenes to all four must fail. At least several sections must receive distinct visual jobs/roles.

#### VISUAL-007 — image matches palette but not paragraph
A visually attractive image that only matches brand colors but cannot explain/support the section heading/body must be rejected.

#### ICON-002 — icon soup
A component set with mixed outline/filled/emoji/3D icons or semantically arbitrary glyphs must fail and be replaced by one coherent site icon family.

#### ICON-003 — bare rich process UI
A rich process/development page with repeated text/card blocks and clear stage/mechanic relationships but no designed micro-visual/diagram support is `FIX_REQUIRED` unless the composition intentionally proves a text-only editorial rationale.




## 56. COMPANY / TEAM / DEVELOPMENT-FIRST RELEASE GATE (v6.8)

This gate is mandatory for rich `OFFICIAL_GAME_STUDIO` builds after the developer/creator relationship is resolved.

### 56.1 Per-page narrative audit

For Home + every key non-legal page record:

```text
visible_word_count
opening_information_roles[]
upper_half_business_role_count
middle_process_role_count
lower_product_role_count
team_process_visual_count
product_visual_count
hero_visual_role
```

Require:

```text
opening_company_team_process_roles >= 2
middle_work_process_roles >= 1
lower_product_game_result_role >= 1 when relevant
```

A game/product page may contain more product detail overall, but the first and middle narrative still need a studio-owned work story.

### 56.2 New word-depth envelopes

Normal rich targets:

```text
Home              900–1350 visible words
Key domain page   950–1700
About / Studio    750–1250
FAQ               525–950
Contact / Support  525–950
```

A lower result is allowed only with a documented source/format limitation.

Word count alone never creates PASS. Semantic repetition still fails.

### 56.3 Hero visual business-model gate

Across Home + key non-legal pages:

```text
team_or_workflow_led_hero_ratio >= 0.70
```

Home hero should normally be team/workflow/business-process led.

Exceptions require a documented semantic reason.

### 56.4 Major media distribution

For a rich key page, expect approximately:

```text
team/work/process major media = 2–4
product/game major media      = 1–3
```

Reject a page where all meaningful imagery is product art and the studio/team story is invisible.

### 56.5 Team-image truth gate

If generated people are used:

```text
asset_role = CONCEPTUAL_STUDIO_WORK_SCENE
named_person_claims = 0
real_employee_claims = 0
real_office_claims = 0
```

Owner-supplied/verified real team imagery may be labeled as documentary.

### 56.6 Business-model order audit

Screenshot-review each key page at desktop and mobile.

Fail when:
- first viewport is only a game screenshot + generic slogan;
- first two sections are gameplay facts with no company/team/task context;
- middle page contains no development/process/review story;
- team/process copy exists only in About while Product/Mechanics/Levels remain outsider-like;
- product/game detail overwhelms the entire page before the business model is established.

### 56.7 Content-model regression IDs

`STUDIO-PAGE-001` — top half lacks team/company/process emphasis.

`STUDIO-PAGE-002` — middle lacks task/development/review content.

`STUDIO-VIS-001` — fewer than 70% of key heroes are team/workflow led without justified exception.

`STUDIO-TEXT-001` — page remains materially inside legacy word envelope without source limitation.

`STUDIO-TRUTH-001` — generated people presented as literal real employees/office documentary.

### 56.8 Relationship unresolved behavior

If the requested model is `OFFICIAL_GAME_STUDIO` but source developer relationship is unresolved, final public build must not receive a normal business-model PASS.

Expected state:

```text
INPUT_REQUIRED
```

Do not mark a neutral outsider rewrite as equivalent success unless the user explicitly requested a different business model.



## 57. COMPOSITION SELF-CHECK + ANTI-REPETITION RELEASE GATE (v6.9)

This is a mandatory **self-check** before claiming static release PASS.

The factory must generate and inspect a `COMPOSITION_SELF_CHECK` for Home + every key internal page.

### 57.1 Per-section audit record

For every meaningful section record:

```text
page_key
section_key
semantic_role
layout_family
topology_cluster
text_flow_mode
media_relationship
media_asset_id
visual_scene_family
interaction_family
visible_word_estimate
desktop_width_usage
dead_space_detected
neighbor_similarity_score
```

### 57.2 Per-page self-check

Compute:

```text
section_count
distinct_layout_family_count
distinct_topology_cluster_count
exact_layout_repeat_count
consecutive_text_flow_repeat_count
dominant_family_share
major_media_count
team_work_media_count
product_media_count
visible_word_count
words_per_major_visual
dead_space_section_count
empty_media_slot_count
```

### 57.3 Blocking thresholds

Normal rich internal page:

```text
distinct_layout_family_count >= 5
exact_layout_repeat_count = 0
empty_media_slot_count = 0
dead_space_section_count = 0
dominant_family_share <= 0.30
```

Normal rich Home:

```text
distinct_layout_family_count >= 7
distinct_topology_cluster_count >= 4
exact_layout_repeat_count = 0
empty_media_slot_count = 0
dead_space_section_count = 0
dominant_family_share <= 0.25
```

When semantics genuinely justify fewer families, record an explicit rationale and screenshot-review the result. "Renderer supports only a few families" is never a valid rationale.

### 57.4 Visual-density check

Flag:

```text
words_per_major_visual > 550
```

on a rich studio/business page for review.

It may PASS only when:
- the section/page intentionally uses strong full-width editorial text;
- no meaningful image/diagram is missing;
- screenshot review confirms the page does not feel visually starved.

### 57.5 Dead-space screenshot audit

At desktop, laptop and mobile inspect each key page.

FAIL if:
- one half of a split is visibly empty;
- a large shell remains after media removal;
- text occupies a narrow column while most container width is unused;
- fixed/min-height creates a dead lower field;
- section feels unfinished because visual weight exists only on one side.

### 57.6 Neighbor similarity

Adjacent sections should not share the same:
- topology cluster;
- text anchor;
- media relationship;
- card geometry

all at once.

If at least 3 of 4 match, reroll or mutate unless there is an explicit editorial reason.

### 57.7 Cross-page clone audit

Build page grammar signatures for representative pages.

Reject when Product / Development / Mechanics / Levels / Studio reuse materially the same section sequence.

Cosmetic differences do not clear this gate.

### 57.8 Manual visual self-question

Before release, the builder must answer for every key page:

```text
1. Do any two neighboring sections look like the same template?
2. Is there any large blank field that has no compositional purpose?
3. Did the added text receive enough visual support?
4. If an image is absent, did the text reflow to use the width?
5. Does this page have a different visual grammar from the previous key page?
6. Does the page rhythm alternate rather than repeat?
7. Are team/work visuals dominant where the business model requires them?
```

Any `YES` to 1 or 2, or `NO` to 3–7 where applicable:
`COMPOSITION_SELF_CHECK_FAIL`.

### 57.9 Release state

Release summary must explicitly report:

```text
COMPOSITION_SELF_CHECK = PASS | FAIL
```

A build cannot claim `STATIC_PASS` when `COMPOSITION_SELF_CHECK = FAIL`.

### 57.10 Regression IDs

`COMP-001` — exact layout family repeats on one rich page.

`COMP-002` — several key pages share the same page grammar.

`COMP-003` — long-copy increase without visual-density recalculation.

`COMP-004` — missing media leaves an empty track/shell.

`COMP-005` — text-only section fails to expand to useful width.

`COMP-006` — adjacent sections match on 3+ core structural dimensions.

`COMP-007` — Home/internal page misses minimum distinct-family target.
---

## 58. FULL-WIDTH + COPY-DENSITY RELEASE GATE (v7.0)

This gate addresses the regression where a page technically passed structure checks but meaningful content occupied only part of the desktop width and large empty fields remained.

### 58.1 Desktop canvas audit

On Home + representative key pages, inspect at laptop, normal desktop and wide desktop widths.

For ordinary major non-hero sections record:

```text
available_canvas_width
meaningful_content_span
canvas_coverage_ratio
largest_unassigned_blank_region_ratio
empty_track_count
one_sided_blank_field
```

Default diagnostic targets:

```text
canvas_coverage_ratio >= 0.78
largest_unassigned_blank_region_ratio <= 0.22
empty_track_count = 0
one_sided_blank_field = false
```

Visual judgment overrides a mathematically acceptable ratio when the section still looks unfinished.

### 58.2 Blocking width failures

Release FAIL if:
- outer background is full width but the meaningful composition is unnecessarily confined to a narrow side island;
- a large opposite field is empty without a declared composition function;
- an optional media column disappears but its track remains;
- a nested max-width caps the entire major section instead of only the readable text measure;
- copy reduction leaves former section height as padding/min-height emptiness.

### 58.3 Compact-copy gate

Expected normal rich envelopes:

```text
Home                 900–1350
Key domain/product   950–1700
About / Studio       750–1250
FAQ                   750–1350
Contact / Support     525–950
Legal                 775–1550 when applicable
```

If visible copy materially exceeds the upper envelope (roughly >15%) without a documented information need, mark `COPY_DENSITY_FIX_REQUIRED` and review for repetition before release.

A lower count can PASS when the page still covers its semantic jobs. Word count is never padded to reach the minimum.

### 58.4 Reflow regression

Test at least one section with media intentionally unavailable:
1. remove/disable the optional asset;
2. render the page;
3. require the media track to disappear;
4. require content to recompute width/alignment;
5. require section height to shrink/recompose;
6. require no large one-sided blank field.

Failure = `REFLOW-001`.

### 58.5 Screenshot decision question

Before PASS answer:

```text
If the screenshot is viewed without reading the copy, does each major section visually use the page width as an intentional composition rather than a small block floating in empty space?
```

If `no` → `FIX_REQUIRED`.


---

## 59. BROWSER-PROOF RELEASE GATE — GEO / SPACE / DIVERSITY / PHOTO (v7.1)

This gate is mandatory for every new full-site BUILD and supersedes static-only release claims.

### 59.1 GEO/SEO browser probe

From final rendered HTML verify:

```text
requested_locale = pl-PL for PL build
html_lang = pl-PL
og_locale = pl_PL
schema_inLanguage = pl-PL
canonical_host = requested_domain
robots_public = index + follow + max-image-preview:large
```

Mismatch = `GEO-SEO-001 FAIL`.

### 59.2 Screenshot matrix is mandatory

Capture Home + representative key pages at:
- mobile narrow;
- laptop / ~1366-class;
- standard desktop / 1440–1600-class;
- wide desktop / ~1920-class.

If screenshot/browser capture cannot run:

```text
BROWSER_QA_BLOCKED
release_ready = false
```

The ZIP may be handed off only as a blocked/debug artifact, not as a visually approved release.

### 59.3 Whitespace + typography blockers

Fail when any ordinary major desktop section has:
- visible content concentrated into a narrow side island;
- a large functionless left/right field;
- body copy stranded far from its heading without a compositional bridge;
- standard H2/H3 rendered as a 4+ line oversized word stack;
- compressed multiline heading line-height that visually merges lines;
- copy reduction compensated by oversized padding/min-height.

Record browser-derived values:

```text
occupied_width_ratio
largest_blank_side_ratio
heading_visual_line_count
section_height_to_content_bbox_ratio
```

### 59.4 Rendered diversity blocker

For each major section record screenshot/DOM-derived `rendered_silhouette_signature`.

Require:
- `>= 0.80` distinct rendered-family ratio on rich pages with `6+` major sections;
- no adjacent near-duplicate major silhouettes;
- Home/key-page first-three-section silhouettes materially differ;
- repeated generic card grids do not dominate site-wide rhythm.

Different IDs with the same visible geometry = failure.

### 59.5 Adult premium media blocker

For applicable premium builds:

```text
major_photo_or_photoreal_ratio >= 0.70
major_abstract_vector_or_diagram_ratio <= 0.20
childlike_doodle_major_visual_count = 0
```

Inspect actual screenshots. Utility SVGs/icons do not count as premium major media.

### 59.6 Release state

A full build reaches visual release only when all are true:

```text
STATIC_PASS
GEO_SEO_BROWSER_PASS
COMPOSITION_BROWSER_PASS
RENDERED_DIVERSITY_PASS
ADULT_MEDIA_PASS
MOBILE_BROWSER_PASS
```

Any missing browser dimension keeps the build blocked.
