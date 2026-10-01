# 06 VISUAL ENGINE

**Bundle format:** Source Bundle v1.5  
**Policy baseline:** Site Factory v4.9.17  
**Bundling rule:** logical module boundaries and aliases are preserved inside bundles. Source Bundle v1.5 applies the Site Factory v4.9.14 interaction, micro-motion, hover/focus and semantic interactive-section expansion while preserving v1.4 rich-content, live UI/UX research, morphological section variation, v1.3 adult-premium visuals and the 7-file Project Source architecture.

## Module aliases in this bundle

- `09-VISUAL-ASSET-ENGINE.md` → this file, section `LEGACY MODULE: 09-VISUAL-ASSET-ENGINE.md`
- `15-SECTION-IMAGE-ENGINE.md` → this file, section `LEGACY MODULE: 15-SECTION-IMAGE-ENGINE.md`
- `16-ADVANCED-VISUAL-GENERATION.md` → this file, section `LEGACY MODULE: 16-ADVANCED-VISUAL-GENERATION.md`

## Cross-reference rule

References inside logical module text to filenames such as `15-SECTION-IMAGE-ENGINE.md` remain valid **logical module IDs**. Resolve them against the module aliases declared across the loaded Source Bundles. `SOURCE-BUNDLE-MAP.md` is maintenance documentation only and is **not required** as a Project Source.

---

<!-- BUNDLE-MODULE-START: 09-VISUAL-ASSET-ENGINE.md -->

# LEGACY MODULE: 09-VISUAL-ASSET-ENGINE.md

# VISUAL ASSET ENGINE

**Version:** 4.6.0  
**Role:** visual plan, assets, media density

---

## 1. Asset Manifest

До coding визначити:

- asset ID;
- page;
- section;
- role;
- source/generation method;
- aspect ratio;
- crop;
- alt intent;
- priority;
- mobile treatment;
- uniqueness/reuse policy.

---


## 1.1. Section Image Engine ownership

`09-VISUAL-ASSET-ENGINE.md` визначає budget, roles, density і consistency.

Безпосередня генерація high-quality section images, prompt design, semantic placement та image-specific QA належать `15-SECTION-IMAGE-ENGINE.md`.

Default rich-site rule:

```text
CHOOSE BEST SOURCE MODE PER SECTION
→ verify semantic fit + rights + crop + quality
→ localize/optimize
```

Possible final modes:
- `GENERATED_ORIGINAL`;
- `VERIFIED_REUSABLE_WEB`;
- `OWNER_SUPPLIED`;
- `ORIGINAL_SVG`;
- `CSS_BACKGROUND`.

Немає глобального правила “generated завжди перший”. Не використовувати випадковий stock лише тому, що він доступний.

---

## 2. Golden-derived asset budget

Observed Golden Sites показують, що mature design використовує media регулярно.

Default targets:

### Simple informational
5–7 meaningful visuals

### Gaming/editorial
10–18

### Store/showcase
12–20+

Це не вимога створювати filler.
Кожен visual повинен мати роль.

---

## 3. Gaming visual strategy

Перед assets:
- оцінити official source art direction;
- вибрати Golden gaming family;
- визначити, чи доречні screenshots, generated scenes, product-style visuals, editorial crops, 3D/render, UI panels.

Gaming не означає cartoon.

---

## 4. Source assets

Використовувати third-party visual assets лише коли:
- користувач має права;
- використання дозволене;
- або це явно допустимий supplied asset.

Інакше:
- створити original supporting visuals;
- використовувати abstract/editorial imagery, але не робити її єдиною identity;
- посилатися на official source для factual reference.

---

## 5. Hero

Hero media:
- має відповідати ніші;
- не бути random SVG;
- підтримувати message;
- мати desktop/mobile crop;
- бути достатньо сильним, але не монополізувати сторінку.

---

## 6. Non-hero media

Для gaming home:
- принаймні 4 meaningful non-hero media sections;
- 2–4 reusable background/decorative SVG systems;
- 2–3 visual moments на ключовій внутрішній сторінці.

Examples:
- category visuals;
- feature scene;
- library covers;
- comparison media;
- gameplay concept visuals;
- guide illustration;
- background editorial image.

---

## 7. Visual consistency

Assets узгоджені за:
- lighting;
- palette;
- crop logic;
- texture;
- perspective;
- tone;
- corner treatment;
- contrast.

---

## 8. Avoid

- watermarks;
- accidental text in generated imagery;
- mismatched stock;
- same image reused everywhere;
- random decorative shapes without role;
- one abstract chart as site identity;
- cartoon mascot without design justification.

---

## 9. Performance

Assets:
- optimized;
- correctly sized;
- no giant source files for tiny cards;
- responsive image handling when practical;
- local critical assets preferred for reliable theme rendering.

---

## 10. Alt text

Alt describes information/function, not keyword stuffing.

Decorative visual:
- empty alt / appropriate decorative handling.

---

## 11. Visual asset QA

FAIL якщо:
- broken asset;
- missing critical hero media;
- homepage feels visually empty;
- asset budget declared but not represented;
- all visual moments are same component;
- mobile crop destroys meaning.


---

## 12. Background system

Кожен Design DNA повинен визначити background language:
- texture / grain;
- gradient field;
- geometric SVG motif;
- silhouette/landscape layer;
- branded line-work;
- subtle pattern;
- media-backed band.

Background assets не повинні бути випадковою декорацією.
Вони мають:
- повторювати visual DNA;
- підтримувати hierarchy;
- не погіршувати readability;
- мати mobile simplification.

Default rich site:
- 2–4 background SVG/pattern families;
- кожна може мати світлу/темну або desktop/mobile варіацію.

---

## 13. Internal-page visual depth

Ключова внутрішня сторінка повинна мати:
- hero visual або branded background;
- мінімум 1 additional contextual media block;
- бажано 2–3 distinct visual moments для gaming/editorial;
- related-content visual treatment.

FAIL якщо всі внутрішні сторінки — лише текст на одному фоні.


---

## 14. Section-specific image requirement

Для rich/editorial/gaming site:

- hero visual повинен мати окрему art direction;
- щонайменше 3 non-hero sections на Home повинні мати **section-specific** visual, а не один reused generic asset;
- ключові internal pages повинні отримати 1–3 context-aware images/illustrations;
- кожен selected/generated image повинен пояснювати, підсилювати або атмосферно підтримувати зміст section;
- generic “pretty background” не зараховується як section-specific visual.

Фабрика обов'язково створює `SECTION IMAGE MANIFEST`, після чого для кожного asset виконує source-mode selection:
`GENERATED_ORIGINAL / VERIFIED_REUSABLE_WEB / OWNER_SUPPLIED / ORIGINAL_SVG / CSS_BACKGROUND`.

Generation є одним із методів, а не обов'язковим методом для кожної section.

Деталі: `15-SECTION-IMAGE-ENGINE.md`.

---

## 15. AI/generated image rejection

FAIL якщо generated image має:
- gibberish text;
- watermark/signature;
- malformed anatomy/objects;
- impossible geometry, якщо scene має бути реалістичною;
- випадкові UI/text fragments;
- style drift від Design DNA;
- subject mismatch із section;
- очевидний low-resolution/upscaled look;
- занадто generic stock-like composition;
- copyrighted logo/brand imitation, якщо це не supplied/authorized asset.

---

## 16.1. Sharpness / clarity gate (v4.4 patch)

Generated or selected imagery must be:
- crisp;
- high-detail;
- visually clean;
- free from accidental blur/fog/smear;
- free from random embedded labels, UI chips or pseudo-interface baked into the image unless explicitly planned.

Any image that looks soft, muddy or artifact-heavy = `REGENERATE`.

## 16.2. HTML attribute completeness handoff

For every rendered meaningful image the asset pipeline must hand off:
- semantic filename;
- localized `alt`;
- localized `title`.

Derived/resized/theme-duplicated versions must inherit these attributes where applicable.

## 16.3. Page fullness media rule

Default target:
- homepage: multiple section-supporting visuals + background supports;
- internal page: at least one strong media element and usually more than one decorative/support visual system;
- cookie/contact/legal can use lighter visual density but still must feel designed.


---

## 17. Hybrid asset sourcing (v4.5.1)

Asset planning must assign `source_mode` per asset:

```text
GENERATED_ORIGINAL
VERIFIED_REUSABLE_WEB
OWNER_SUPPLIED
ORIGINAL_SVG
CSS_BACKGROUND
```

Do not decide "all AI" or "all web" at project level.

### Best-fit examples

Prefer generated/original when:
- hero needs custom composition;
- section concept is abstract;
- source/product art cannot be reused;
- a branded visual world is needed.

Prefer verified reusable web imagery when:
- real environment/texture/object photography materially improves credibility;
- a natural photo is more useful than synthetic art;
- the section benefits from authentic geographic/editorial atmosphere;
- reuse rights are known and compatible.

### External asset provenance manifest

For every web-sourced candidate record:

```text
asset_id
source_url
source_page_url
source_name
author_creator_if_known
rights_state
licence_name
licence_url_if_any
attribution_required
attribution_text
retrieved_at
original_mime
original_dimensions
local_filename
output_format
output_dimensions
metadata_stripped
semantic_alt
semantic_title
section_assignment
```

No source/provenance record → no production publish.

## 18. Image sanitization + optimization pipeline

Before a downloaded web image enters `/assets/`:

1. decode successfully;
2. apply EXIF orientation to pixels;
3. strip nonessential EXIF/IPTC/XMP/private camera/location metadata;
4. keep or normalize color handling so the rendered image does not shift unexpectedly;
5. remove embedded thumbnails/previews where tooling supports it;
6. resize to the maximum rendition actually needed;
7. compress;
8. convert to:
   - WebP by default for photographic/illustrative raster where practical;
   - AVIF when the build supports it safely and fallback policy is defined;
   - PNG when alpha/lossless detail materially requires it;
   - JPEG only when it is the better compatibility/quality choice;
9. semantic filename;
10. checksum/dedupe;
11. no remote hotlink in final theme.

Do not upscale a weak source just to hit a nominal dimension.

## 19. Edge/matte artifact gate

Reject or repair when a visual contains an **unintended**:
- white/near-white border band;
- matte;
- collage divider;
- scan/export margin;
- letterbox/pillarbox;
- transparent halo that turns white on the page;
- baked card frame that fights the site's CSS frame.

Automated QA may flag suspicious uniform edge bands, but final decision is semantic/visual: legitimate white content is not itself an error.

For cropped multi-panel generations, inspect all four edges at 100% view before publish.

---

## v4.5.11 patch — asset-source accounting and local attribute readiness

### 1. Asset-source accounting
For every meaningful visible raster asset store:
```text
source_mode
source_ratio_bucket
render_instances
alt_seed
image_title_seed
link_title_seed_if_wrapped
```

Allowed `source_ratio_bucket`:
- `GENERATED_65_POOL`
- `WEB_35_POOL`
- `EXCLUDED_FROM_RATIO`

### 2. Ratio policy
At project level, meaningful visible section raster images must satisfy:
- generated originals >= `65%`
- reusable/supplied raster images <= `35%`

The asset engine must count planned and final selected assets and rebalance before release.

### 3. Attribute readiness
Before placement, every meaningful image asset must already have:
- localized ALT seed;
- localized TITLE seed;
- if the image is wrapped in a factory-owned link, that link also receives a localized TITLE seed.

Hash-like filenames or attachment-derived variants do not exempt the asset from attribute readiness.

### 4. External-source localization rule
If an external reusable asset is accepted:
- download locally;
- sanitize metadata;
- optimize format;
- generate local ALT/TITLE from section context, not filename;
- create attribution record when license requires.

---

## 20. Clean web-image presentation + photoreal raster patch (v4.5.2)

### 20.1. Internal provenance, clean public rendering
For `VERIFIED_REUSABLE_WEB`, provenance remains mandatory in the internal asset manifest, but public attribution is **not automatic**.

Default production rendering must not add:
- visible source URL;
- `Source:` / `Photo by:` caption;
- source-site badge;
- link back to the image/source page;
- creator/source text in ALT or TITLE;
solely because the raster was sourced from the web.

ALT and TITLE describe the image's semantic role in the section, not its acquisition source.

If `attribution_required = false`:
```text
public_source_caption = none
public_source_link = none
```

If `attribution_required = true`:
- satisfy only the licence-required attribution; or
- reject/reselect the asset if the project requires a clean no-credit presentation.

The provenance manifest is retained internally even when the public site shows no source information.

### 20.2. Preferred reusable-image rights profile
When equally suitable assets exist, prefer reusable sources that allow clean production use without mandatory visible credit.
Do not downgrade semantic/visual quality solely to avoid attribution, but do not add unnecessary source clutter either.

### 20.3. Photoreal generated-raster default
For major hero/section raster media, `GENERATED_ORIGINAL` should default to professional photoreal/editorial rendering unless the project explicitly requires another style.

Preferred qualities:
- commercial/editorial photography art direction;
- believable camera perspective and focal behavior;
- realistic material response and microtexture;
- natural lighting or controlled studio lighting;
- professional retouching;
- cinematic realism where literal photography is impossible;
- custom composition tied to the section intent.

Reject as primary raster direction unless explicitly justified:
- childish/cartoon illustration;
- toy-like 3D;
- plastic CGI surfaces;
- mascot art;
- flat vector poster look;
- generic AI fantasy filler;
- cheap synthetic stock-photo aesthetics.


---

## 26. Major raster uniqueness contract (v4.5.3)

For hero and major content/editorial raster assets:

```text
exact_asset_reuse_across_major_sections = 0 by default
hero_reuse = 0
same_source_crop_reuse_as_new_asset = 0
```

Track at least:
- `asset_id`;
- `source_asset_id`;
- checksum/hash;
- source/generation lineage;
- `major_media_boolean`;
- `visual_signature`;
- render locations.

A resized/cropped/converted copy inherits the same `source_asset_id`.

Allowed repeated systems:
- logo;
- icons;
- decorative pattern/texture;
- intentionally repeated product thumbnail where identity continuity is required.

They must not be counted as unique major media.

### Visual signature
For major images record a compact semantic signature:
- subject;
- environment;
- camera/perspective;
- focal placement;
- action/state;
- lighting;
- composition family.

Even different files should be rejected as near-duplicates when those dimensions are effectively the same and the page feels repetitive.



## 27. Site-wide major visual uniqueness (v4.5.4)

The uniqueness contract applies to every **major visible media asset**, not only photographic raster.

By default across unrelated major sections/pages:
```text
major_raster_exact_reuse = 0
major_svg_exact_reuse = 0
major_diagram_exact_reuse = 0
hero_major_reuse = 0
```

Decorative systems such as logo, icons, tiny repeated UI symbols, textures or intentionally repeated product identity thumbnails remain exempt.

For SVG/diagram media track:
- asset ID;
- semantic/visual signature;
- major-media flag;
- render locations.

Different filenames that preserve the same obvious subject + geometry + composition are still near-duplicates and may fail Visual QA.

Internal pages should receive page-specific major visual roles whenever practical; do not rotate the same `source-card`, `corridor-map`, generic device or diagram through Guide/About/Contact/Legal merely for convenience.

<!-- BUNDLE-MODULE-END: 09-VISUAL-ASSET-ENGINE.md -->

---

<!-- BUNDLE-MODULE-START: 15-SECTION-IMAGE-ENGINE.md -->

# LEGACY MODULE: 15-SECTION-IMAGE-ENGINE.md

# SECTION IMAGE ENGINE

**Version:** 4.7.0  
**Role:** select, generate, curate and place high-quality section-aware imagery into the right site sections  
**Scope:** art direction, source-mode selection, web curation/rights brief, prompt engineering, generation, selection, placement, crops, responsive variants, optimization, semantic QA

---

## 1. Мета

Фабрика повинна не просто “мати картинки”.

Вона повинна **підбирати, курувати, створювати або генерувати якісні візуали, що відповідають конкретній темі та конкретній секції**, і вставляти їх у сайт так, щоб вони:

- підсилювали content;
- створювали visual storytelling;
- відповідали Golden Design DNA;
- не виглядали випадковим AI/stock filler;
- були стилістично цілісними;
- працювали desktop + mobile.

---

## 2. Ownership

`09-VISUAL-ASSET-ENGINE.md`:
- визначає asset budget;
- media density;
- visual roles;
- background system.

`15-SECTION-IMAGE-ENGINE.md`:
- визначає, **який visual потрібен section**;
- вибирає source mode;
- для generated assets формує prompt;
- для web assets формує search/rights/crop brief;
- перевіряє результат;
- визначає placement/crop/variant;
- вирішує, коли repair / replace / regenerate.

`11-VISUAL-QA.md`:
- приймає або відхиляє фінальний visual result.

---

## 3. Input

До image planning отримати:

```text
DOMAIN
GEO
TOPIC / NICHE
BRAND
GOLDEN FAMILY
PAGE MANIFEST
SECTION MANIFEST
CONTENT BIBLE
COLOR / TYPE / MATERIAL DNA
```

Optional:
- official source/reference URL;
- user-provided assets;
- allowed visual references;
- product screenshots;
- brand palette.

---

## 4. Section Image Manifest

Для кожного meaningful image створити:

```text
asset_id
page_key
section_key
section_intent
visual_role
semantic_subject
source_mode
art_direction
style_family
aspect_ratio
desktop_crop
mobile_crop
focal_point
palette_notes
lighting_notes
negative_constraints
alt_intent
image_title_intent
social_candidate
reuse_policy
priority
status
```

Status:

```text
PLANNED
SOURCE_MODE_SELECTED
GENERATED | SOURCED | OWNER_SUPPLIED_READY | SVG_READY
RIGHTS_VERIFIED
SELECTED
SANITIZED
OPTIMIZED
PLACED
VISUAL_PASS
REPAIR | REPLACE | REGENERATE
```

---

## 5. Source / production methods

Допустимі:

### A. Generated original scene
Для:
- hero;
- atmospheric feature section;
- custom product/editorial story;
- conceptual environment;
- composition that must be built around layout.

### B. Generated original illustration
Для:
- guides;
- process;
- concept explanation;
- mechanics;
- editorial explanation.

### C. Verified reusable web image
Для:
- authentic photography;
- real environment/texture/object context;
- GEO/editorial atmosphere;
- cases where a real image is stronger than synthetic art.

Only when rights/provenance are publishable.

### D. Original SVG / diagram / CSS visual
Для:
- routes;
- timelines;
- control systems;
- charts;
- iconographic explainers;
- backgrounds/patterns.

### E. User/owner supplied visual
Use when quality/licensing/fit are sufficient.

### F. Official/source visual
Publish only when rights/use context allows. Otherwise `REFERENCE_ONLY`.

No global source priority exists. The engine chooses the best valid mode per section.

---

## 6. Section visual trigger

Якщо section має meaningful visual role:

`SELECT SOURCE MODE`.

Then:
- generate an original asset; or
- curate a verified reusable web asset; or
- use an owner-supplied asset; or
- create an original SVG/CSS visual.

Фабрика не повинна замінювати потрібну картинку:
- random gradient;
- порожнім SVG rectangle;
- generic icon;
- abstract blobs only.

Для rich/editorial/gaming Home:
- 1 strong hero visual from the best valid source mode;
- 3–6 section-specific visuals from a deliberate hybrid mix where useful;
- 2–4 background/SVG systems.

Для key internal page:
- hero/background visual;
- 1–3 contextual visuals selected/generated for the actual section intent.

---

## 7. Section → visual mapping

### Hero
Visual повинен:
- одразу передати niche/topic;
- мати clear focal point;
- залишити композиційний простір під text, якщо layout overlay;
- створити brand mood.

### Features / benefits
Visual:
- показує benefit/context;
- не просто декоративний предмет.

### Process / how it works
Visual:
- sequence;
- workflow;
- action state;
- diagram/illustration.

### Gaming controls
Visual:
- controller/device/input interaction;
- readable motion;
- no fake UI text.

### Progression
Visual:
- route;
- rhythm;
- stages;
- increasing complexity;
- vertical/horizontal journey.

### Catalog / collection
Visual:
- category-specific scene/cover/product presentation;
- consistent series style.

### About
Visual:
- editorial process;
- craft/source/method;
- brand atmosphere.

### Contact
Visual:
- communication/network/location abstraction;
- actual map/photo only when location is real/verified;
- synthetic address ≠ map pin.

### Legal
Visual:
- restrained branded pattern/texture;
- no fake office/team photography.

---

## 8. Prompt architecture

Кожен generation prompt формується з блоків:

```text
1. SUBJECT
2. SECTION PURPOSE
3. ENVIRONMENT / CONTEXT
4. ART DIRECTION
5. COMPOSITION
6. PALETTE
7. LIGHTING
8. MATERIAL / TEXTURE
9. CAMERA / PERSPECTIVE
10. ASPECT RATIO
11. NEGATIVE CONSTRAINTS
```

Example structure:

```text
Create an editorial cinematic scene for a Portuguese gaming guide section about progression.
Subject: vertical safari platforms rising through layered terrain.
Purpose: communicate increasing pace and anticipation.
Art direction: mature editorial game-world illustration, premium, tactile, not cartoon.
Composition: clear ascending diagonal route, focal point in upper-right, quiet negative space on left for text.
Palette: deep teal, warm sand, muted gold, acid-lime accent.
Lighting: late-afternoon atmospheric light, controlled contrast.
Texture: subtle grain, layered depth.
No text, no logo, no watermark, no UI labels, no mascot, no childish proportions.
Aspect ratio: 16:10.
```

---

## 9. Negative prompt / constraints

Default avoid:
- text;
- letters;
- fake logos;
- watermark;
- signature;
- gibberish UI;
- extra fingers/limbs;
- malformed products;
- duplicated objects;
- random cyber neon;
- cartoon mascot unless Design DNA explicitly requires;
- cheap stock-photo smile;
- unrelated office imagery;
- excessive lens flare;
- over-saturated colors;
- low-detail background;
- copied franchise key art.

---

## 10. Style consistency

До першої генерації створити:

```text
IMAGE STYLE BIBLE
```

Поля:
- rendering style;
- realism level;
- line/shape language;
- palette;
- material feel;
- texture;
- lighting;
- contrast;
- depth;
- camera logic;
- corner/crop treatment;
- human/character policy.

Наступні images повинні наслідувати цю visual family.

Не робити:
- hero = cinematic 3D;
- section 2 = flat cartoon;
- section 3 = stock photo;
- section 4 = anime;
без explicit narrative reason.

---

## 11. Brand/topic fidelity

Generated images:
- відповідають TOPIC/NICHE;
- не повинні копіювати Golden assets;
- Golden Sites задають maturity/composition principles;
- official source може задавати factual visual context, але не license на копіювання art.

Для copyrighted game/product:
- створювати original editorial interpretation;
- не копіювати protected characters/logo/key art, якщо user не надав/не дозволив.

---

## 12. GEO fidelity

GEO впливає лише коли доречно:
- architecture;
- environment;
- service context;
- people/clothing/context;
- language-bearing objects.

Не вставляти прапор/ландмарк у кожне image лише заради GEO.

Якщо text у scene не потрібен — **не генерувати text**.
Text краще накладати HTML/CSS.

---

## 13. Asset selection / production loop

Для кожного important asset:

```text
PLAN
→ SELECT SOURCE MODE
→ GENERATE / SEARCH-CURATE / PREPARE OWNER ASSET / CREATE SVG
→ RIGHTS + PROVENANCE CHECK WHEN EXTERNAL
→ INSPECT
→ SELECT
→ SANITIZE WHEN DOWNLOADED
→ CROP TEST
→ MOBILE TEST
→ OPTIMIZE
→ PLACE
→ SCREENSHOT QA
```

Якщо FAIL:

```text
REJECT REASON
→ REPAIR / SEARCH ANOTHER / PROMPT ADJUSTMENT
→ REPLACE OR REGENERATE
```

Не приймати перший generation або перший web-search result автоматично.

---

## 14. Inspection gate

Перевірити:

### Semantic
- image дійсно про section?

### Quality
- sharp focal subject?
- enough detail?
- no accidental artifacts?

### Composition
- text-safe region?
- crop works?
- subject not awkwardly cut?

### Style
- same visual family?
- correct palette/lighting?

### Integrity
- no watermark?
- no gibberish text?
- no accidental real-world brand?

FAIL → repair / replace / regenerate.

---

## 15. Placement engine

Image placement визначається section composition:

### Full-bleed
Для:
- hero;
- atmospheric transition;
- finale.

### Split layout
Для:
- editorial story;
- guide;
- feature explanation.

### Card media
Для:
- catalog;
- categories;
- resources.

### Inline article visual
Для:
- explanatory content;
- process;
- comparison.

### Background
Для:
- pattern/texture/atmospheric layer;
- не використовувати як єдиний носій important information.

---

## 16. Responsive crops

Для кожного important visual:

```text
desktop aspect
tablet behavior
mobile aspect/crop
focal point
object-position
```

Hero:
- desktop crop не можна просто стискати на mobile;
- mobile може мати окремий crop/rendition.

Critical subject не обрізається.

---

## 17. File output

Final selected raster images — generated, sourced or owner-supplied — повинні бути локальними theme assets.

Preferred:
- WebP / AVIF where runtime/tooling supports;
- optimized PNG/JPEG where needed;
- SVG тільки для vector-native art.

Не залишати:
- temporary generator URLs;
- chat-only image references;
- remote ephemeral asset dependencies.

Filename:

```text
{page}-{section}-{subject}.{ext}
```

Example:

```text
home-progression-safari-route.webp
controls-touch-input-scene.webp
about-editorial-method.webp
```

---

## 18. Performance

Перед ZIP:
- optimize filesize;
- remove unnecessary metadata;
- correct dimensions;
- responsive sizes/srcset where practical;
- avoid 4K source for small card;
- preserve sufficient visual quality.

Hero/LCP:
- prioritize appropriately.

Below fold:
- lazy loading where appropriate.

---

## 19. Alt handoff

Image engine передає:

```text
semantic_subject
informational_role
decorative_boolean
```

`14-SEO-GEO-METADATA-ENGINE.md` формує final alt.

Decorative image:
`alt=""`.

Meaningful image:
natural descriptive alt without keyword stuffing.

---

## 20. Social image handoff

Strong visual asset може бути:
`social_candidate: true`.

Але social rendition:
- окремий crop;
- 1.91:1;
- readable subject;
- no accidental text;
- optional HTML/vector brand overlay generated separately.

---

## 21. Background/SVG generation

Background systems:
- 2–4 families для rich site;
- derived from Design DNA;
- lightweight;
- seamless/repeat-aware;
- readability-safe;
- reduced complexity on mobile.

Examples:
- contour lines;
- grain;
- geometric motif;
- landscape silhouette;
- route/path language;
- botanical/editorial forms.

---

## 22. Contact imagery rule

Якщо Contact Profile = `SYNTHETIC_GEO_CONTACT`:

Allowed:
- abstract communication visual;
- editorial location motif;
- branded network lines;
- neutral city atmosphere without claiming exact place.

Forbidden:
- fake photo of “our office”;
- map pin to synthetic exact address;
- photo of a real unrelated building presented as operator location.

---

## 23. Visual diversity

Не повторювати:
- same composition;
- same camera angle;
- same hero pose;
- same background;
- same subject/asset composition without intentional reuse.

Re-use allowed:
- background pattern family;
- icon system;
- intentional campaign motif.

---

## 24. QA metrics

Home:
- hero visual PASS;
- 3+ non-hero section-specific visuals PASS;
- 2–4 background/SVG systems PASS.

Key internal page:
- 1 hero/background visual;
- 1–3 contextual images;
- no broken/media-empty section.

Asset rejection/replacement count:
- unlimited until quality bar met.

---

## 25. Release blocking

`VISUAL_PASS` forbidden if:
- image missing;
- low-quality generated or sourced asset accepted;
- semantic mismatch;
- style inconsistency;
- visible watermark/gibberish;
- hero is generic/unrelated;
- final asset only exists remotely / is hotlinked instead of localized;
- mobile crop destroys focal subject;
- Home has visuals, internal pages are empty;
- contact uses fake-office/map imagery for synthetic address.

---

## 26. Factory learning

Every image defect:

```text
IMAGE DEFECT
→ SECTION INTENT
→ SOURCE/PROMPT/CROP FAILURE
→ VISUAL QA REASON
→ SOURCE/PROMPT/RULE UPDATE
→ REPAIR / REPLACE / REGENERATE
→ REGRESSION CASE
```

The factory learns prompt patterns, not one-off patches.


---

## 27. Image HTML attribute handoff

Section Image Engine передає для кожного meaningful asset:

```text
alt_intent
image_title_intent
semantic_subject
page_context
section_context
decorative_boolean
```

### ALT
Розгорнутий semantic description.

### TITLE
Коротка localized назва visual.

Example:

```text
alt:
Schemat łodzi i koncentrycznego zasięgu automatycznego łowienia

title:
Zasięg automatycznego łowienia
```

Final factory-owned meaningful `<img>`:
- ALT non-empty;
- TITLE non-empty.

Decorative pattern:
- краще CSS background;
- не повинен випадково потрапляти в rendered IMG audit як missing ALT/TITLE.

`14-SEO-GEO-METADATA-ENGINE.md` формує final localized attributes.

---

## 28. Image audit regression

Після placement browser/runtime crawler рахує:

```text
images_total
meaningful_images
images_missing_alt
images_missing_title
```

Factory-controlled target:

```text
images_missing_alt = 0
images_missing_title = 0
```

Якщо meaningful selected image має файл, але не має повних HTML attributes:
`PLACED ≠ VISUAL_PASS`.

---

## 29. Split-layout composition patch (v4.4 patch)

When a section uses text + image side by side, the engine must co-plan:
- heading length;
- paragraph depth;
- image aspect ratio;
- image scale;
- column ratio;
- negative space.

Default target:
- text block ≈ `42%–58%`;
- media block ≈ `42%–58%`;
- image aspect ratio usually between `4:3`, `16:10`, `3:2` depending on content;
- media card should feel substantial, not ornamental.

If the section heading is very long:
- reduce typographic scale;
- tighten line length;
- move part of concept to eyebrow/deck/body;
- upscale or reframe the media.

## 30. No accidental overlays rule

The engine must not accept or create random chips, captions, numbers, pseudo-UI labels, or text baked into artwork unless the section spec explicitly asks for it.

HTML overlays belong in HTML/CSS, not accidentally inside artwork.

## 31. High-fidelity image acceptance

Selected image must pass all of:
- sharp detail;
- coherent composition;
- no blur;
- no duplicate fish/objects/limbs or AI artifacts;
- no muddy water/smear if underwater/ocean theme;
- clear thematic relevance.


---

## 32. Section-level source-mode decision (v4.5.1)

Every meaningful section image manifest entry must include:

```text
source_mode
source_candidate_url
rights_state
provenance_required
desired_aspect_ratio
focal_zone
edge_behavior
frame_behavior
output_format
```

Allowed final `source_mode`:
- `GENERATED_ORIGINAL`;
- `VERIFIED_REUSABLE_WEB`;
- `OWNER_SUPPLIED`;
- `ORIGINAL_SVG`;
- `CSS_BACKGROUND`.

The choice must be made from section intent, not habit.

### Decision examples

`real place / natural texture / real-world atmosphere`
→ consider reusable web photo first if rights/quality fit.

`mechanic / progression / concept / impossible composition`
→ generated original is often better.

`brand/source reference without reusable rights`
→ use as `REFERENCE_ONLY`, generate an original interpretation.

## 33. Crop + edge behavior

Manifest must declare:

```text
edge_behavior:
  EDGE_TO_EDGE | INTENTIONAL_INSET | TRANSPARENT_SUBJECT

frame_behavior:
  CSS_FRAME | NO_FRAME | ARTWORK_FRAME_EXPLICIT
```

Default major section media:

```text
EDGE_TO_EDGE + CSS_FRAME
```

Therefore the bitmap itself must not contain an accidental white card/frame.

### Multi-panel generated source rule

If generation returns a collage/contact-sheet/multiple panels:
- split panels cleanly;
- remove divider pixels;
- use slight safe crop/bleed where needed;
- inspect all edges;
- do not publish the raw collage unless the section explicitly wants a collage.

## 34. Web-image acceptance checklist

Before assigning a web-sourced image to a section:
- semantic fit = PASS;
- visual quality = PASS;
- rights state = publishable;
- no watermark = PASS;
- provenance recorded = PASS;
- no unsafe hotlink dependency = PASS;
- crop works at required aspect ratio = PASS;
- edge/matte artifacts = 0;
- metadata sanitization planned = yes;
- ALT/TITLE intent created.

Unknown rights or poor crop fit → reject candidate and search/generate another asset.

---

## 35. Generated-image share rule (v4.5.11)

For meaningful visible raster section images on Home + key internal pages, the engine must plan a source mix where:
- `GENERATED_ORIGINAL` = at least `65%`
- `VERIFIED_REUSABLE_WEB + OWNER_SUPPLIED` = at most `35%`

This is a hard planning rule, not a nice-to-have.

### Ratio denominator includes
- hero raster;
- section raster images;
- inline thematic editorial images;
- support raster visuals that are visibly part of content.

### Excludes
- logo;
- favicon;
- tiny UI icons;
- CSS backgrounds;
- vector-only ornaments;
- duplicate responsive instances of the same image.

## 36. Mandatory generated set
At minimum the generated set should include:
- homepage hero;
- at least 2 additional homepage section visuals;
- at least 1 generated thematic visual on each key internal guide page.

## 37. Edge-to-edge image integrity reiteration
Generated images selected for section media must be full-bleed within the asset bounds.
Do not publish a generated image if it has:
- inner white border;
- white halo;
- baked frame;
- accidental matte;
- visible collage gutter.

If present:
`crop safely → else regenerate`.


---

## 38. Image semantic text stored in Global Text (v4.5.3)

For every meaningful asset, semantic text handoff must create stable Global Text keys:

```text
images.{asset_id}.alt
images.{asset_id}.title
```

If the image is wrapped in a factory-owned link:

```text
links.{link_key}.title
```

The rendered helper consumes these keys directly.

Do not duplicate ALT/TITLE literals in PHP templates or attachment-specific markup.

Responsive/derived instances of the same semantic asset reuse the same localized semantic keys unless the crop changes meaning enough to require its own asset ID/key.

---

## 39. Photoreal-first section raster + clean attribution (v4.5.5)

### 39.1. Default source-mode rendering target
Source-mode selection remains per section, but when the selected mode is `GENERATED_ORIGINAL` for a major raster visual, default style is:

```text
PHOTOREAL_EDITORIAL
COMMERCIAL_PHOTOGRAPHY
CINEMATIC_REALISM
```

Use illustration/cartoon rendering only when:
- the user explicitly requests it; or
- the section is genuinely diagrammatic/explanatory and photography would reduce clarity; or
- Design DNA records a strong source/brand reason.

For gaming/app subjects, prefer a realistic editorial reinterpretation of mechanics, environment, objects and mood rather than recreating the source's cartoon/key-art style.

### 39.2. Professional image-maker prompt block
Major generated-raster prompts should include appropriate photographic direction:
- professional commercial/editorial photographer + art director mindset;
- camera position and perspective;
- lens/focal behavior when useful;
- lighting setup / time of day;
- realistic material and surface detail;
- depth and atmospheric realism;
- premium retouching;
- natural imperfections;
- custom section-specific composition.

Default negative constraints add:
- no cartoon;
- no children's illustration;
- no mascot;
- no toy/diorama look;
- no plastic CGI;
- no flat vector rendering;
- no glossy mobile-game ad aesthetic;
- no generic AI-stock composition.

### 39.3. Web-source display policy
For `VERIFIED_REUSABLE_WEB`:
- keep `source_url`, author/licence/status and retrieval evidence in the internal provenance manifest;
- strip nonessential embedded metadata;
- localize the asset;
- render semantic ALT/TITLE from section context.

Do **not** automatically create a visible caption or link to the source image/page.
If visible attribution is legally required, use the minimum compliant credit or choose another asset that supports clean presentation.



---

## 40. Section Composition Engine handoff (v4.6.0)

Before selecting/generating a major section image, consume the composition contract from `18-SECTION-COMPOSITION-ENGINE.md`.

Required additional input:

```text
pattern_family
media_mode
media_slot_geometry
expected_aspect_ratio
focal_region
text_safe_region
overlap_behavior
desktop_crop_behavior
mobile_transformation
```

### Rule
Image planning follows the chosen section composition; it must not silently force the layout back to the factory's familiar split template.

Examples:
- mosaic section → generate/select multiple compatible crops or one composition that supports the mosaic role;
- media rail → assets need consistent sequence rhythm, not one oversized hero crop repeated;
- annotated visual → leave annotation-safe regions and semantic focal space;
- full-bleed stage → protect text-safe negative space if overlay is used;
- asymmetrical spotlight → place the focal subject according to the dominant media cell;
- mobile transformation → verify subject survives the mobile crop/reorder.

`SECTION IMAGE MANIFEST` and `SECTION COMPOSITION MANIFEST` must agree on media geometry before BUILD.



---

## 41. Independent-major-image generation rule (v4.6.1)

For every section marked `major_media_unique_required = yes`:

```text
ONE MAJOR SECTION
→ ONE INDEPENDENT VISUAL BRIEF
→ ONE INDEPENDENT SOURCE/GENERATION DECISION
→ UNIQUE visual_signature
```

Do not satisfy several major section slots by:
- generating one 2×2 / 3×3 collage and slicing it;
- taking several crops from one photo/generation;
- mirroring/flipping the same scene;
- changing grade/blur/overlay on the same source;
- generating near-identical prompts that preserve the same board, camera, lighting and environment.

### Diversity planning
Across the page/site rotate major visual roles where semantically useful:
- wide establishing environment;
- macro/detail;
- top-down/diagrammatic;
- oblique tabletop/object;
- device/product context;
- human-action close-up;
- architecture/environment;
- structured diagram/data visual;
- restrained non-photo editorial graphic.

The goal is **visual rhythm**, not arbitrary style switching. All assets still belong to the same Design DNA.

### Asset-series exception
A deliberate series may share art direction, but each asset must have a different:
- scene or semantic state;
- camera/composition;
- focal arrangement;
- section purpose.

If users would reasonably describe two major images as “the same picture again”, replace one.

### Build-time uniqueness check
Before final placement:
1. exact checksum/source-lineage compare;
2. visual-signature compare;
3. perceptual/near-duplicate check when tooling is available;
4. human screenshot review.

Any major duplicate not allowlisted → `REPLACE / REGENERATE`.

<!-- BUNDLE-MODULE-END: 15-SECTION-IMAGE-ENGINE.md -->

---

<!-- BUNDLE-MODULE-START: 16-ADVANCED-VISUAL-GENERATION.md -->

# LEGACY MODULE: 16-ADVANCED-VISUAL-GENERATION.md

# 16-ADVANCED-VISUAL-GENERATION.md

**Module:** Advanced Visual Generation  
**Version:** 2.1.0  
**Owner:** Site Factory  
**Status:** Active  
**Scope:** All factory-generated sites with thematic image generation, section visuals, background systems, and modern visual direction

---

## 1. Purpose

This module defines how Site Factory must create **better visual assets automatically**.

The goal is to move away from:
- primitive filler illustrations;
- generic SVG placeholders;
- empty sections with weak visuals;
- random decorative graphics;
- childish / cartoonish style unless explicitly requested.

The factory must instead produce a curated visual system using the best valid source mode:
- modern thematic hero visuals;
- section-specific generated or verified reusable imagery;
- background systems;
- decorative support assets;
- visually rich, consistent, contemporary image language.

This module applies especially to:
- gaming sites;
- app guide sites;
- info/editorial landing pages;
- niche content sites where thematic imagery materially improves quality.

---

## 2. Core visual principle

The factory must create images that feel:

- **modern**
- **clean**
- **editorial**
- **high-quality**
- **context-aware**
- **topically relevant**
- **stylistically coherent across the whole site**

The system must not treat images as filler.  
It must treat them as part of:
- design quality;
- information architecture;
- user perception;
- conversion support;
- brand-like coherence.

---

## 3. Inputs

Before planning or producing visuals, the module must collect:

### Required inputs
- project type
- topic / niche
- GEO
- locale
- domain
- page map
- section map
- content strategy
- design direction
- source URL if provided (for example Google Play / App Store / website)

### Optional but recommended
- screenshots
- icon
- brand colors
- user-provided examples
- reference themes from golden sources

---

## 4. Source-grounded visual intelligence

If the user provides an app page, game page, product page, or source page, the factory must use it as a **visual intelligence input**.

This means the factory may analyze:

- title
- subtitle
- category
- description
- feature list
- visible screenshots
- visible icon
- palette
- tone
- recurring objects
- game mechanics
- environment / setting
- mood

### Important rule
The system may use the supplied official/product source as **reference intelligence**.

If the source image itself is not owner-supplied or verified reusable, it stays `REFERENCE_ONLY` and the factory must create a new original interpretation rather than copy it.

Separate independently sourced images may still be used under `VERIFIED_REUSABLE_WEB` when their rights/provenance pass the asset engine.

The factory must **not** directly reproduce:
- official poster art;
- exact game key art;
- exact screenshots;
- exact cover art;
- direct copies of official image compositions.

Allowed:
- thematic inspiration;
- atmosphere extraction;
- palette extraction;
- mechanic-driven visual interpretation;
- object-driven scene generation.

---

## 5. Visual extraction model

For each project, build a compact internal profile:

### 5.1. Topic profile
- site type
- main subject
- user intent
- content function

### 5.2. Visual DNA
- dominant palette
- contrast level
- visual density
- realism level
- softness / sharpness
- geometric vs organic balance
- lighting direction
- editorial tone

### 5.3. Motif inventory
Recurring thematic objects, for example:
- fishing boats
- fish species
- sea zones
- upgrades
- tools
- maps
- arcade motion cues
- level gates
- reward systems

### 5.4. Section mapping
Every important section must have:
- content intent
- visual intent
- image type
- suggested composition

---

## 6. Default style modes

The factory must classify the project into one of these primary style modes.

### 6.1. modern-editorial
Use for:
- informational landing pages
- guide sites
- knowledge pages
- premium niche content

Features:
- clean layouts
- balanced whitespace
- structured composition
- sophisticated palette
- restrained decorative elements
- high readability

### 6.2. product-illustrative
Use for:
- utility sites
- explanatory sites
- process-heavy pages
- structured information pages

Features:
- object-driven visuals
- diagram-like clarity
- clean support illustrations
- concise concept representation

### 6.3. game-atmospheric
Use for:
- gaming pages
- guide pages for games
- gameplay-analysis pages

Features:
- thematic scenes
- stronger mood
- richer lighting
- motion or gameplay cues
- more visual personality
- deeper immersion

---

## 7. Style exclusions

Unless explicitly requested, the factory must avoid:
- childish cartoon style;
- low-effort flat clipart look;
- random icon-pile layouts;
- primitive placeholder SVGs;
- oversimplified vector blobs with no semantic value;
- chaotic neon overload;
- visually empty sections;
- generic stock-illustration feel.

If a page looks:
- too empty,
- too toy-like,
- too generic,
- too obviously AI-filler,

the visual sourcing/production result must be considered **failed** and repaired, replaced or regenerated.

---

## 8. Visual asset classes

The factory must plan and produce visuals in layers.

### 8.1. Hero visual
Required for homepage and key internal pages.

Purpose:
- define tone;
- establish quality impression;
- communicate theme;
- provide emotional hook.

Hero images should be:
- the most polished assets;
- visually rich;
- compositionally controlled;
- clearly tied to the page topic.

### 8.2. Section images
Each important section should have a specific thematic visual.

Examples:
- controls
- progression
- upgrades
- economy
- comparison
- item types
- maps
- tips
- strategy
- FAQ support
- contact/about support

### 8.3. Background systems
The site must not rely on blank color blocks only.

Possible background assets:
- subtle gradients
- pattern systems
- texture layers
- grid overlays
- wave systems
- map-like linework
- geometric atmosphere layers
- soft glows
- thematic abstract motifs

### 8.4. Decorative support assets
These include:
- inline mini-illustrations
- badge-like assets
- stat markers
- card corner ornaments
- icon clusters
- section dividers
- diagram support graphics
- editorial callout visuals

---

## 9. Minimum visual density rules

The factory must not produce pages that feel empty.

### Homepage minimum
Homepage should usually contain:
- 1 strong hero visual
- 4 to 8 section visuals
- 2 to 4 background treatments
- 1 to 3 support/decorative systems

### Internal page minimum
Important internal article/guide pages should usually contain:
- 1 page hero/support visual
- 2 to 5 section visuals
- 1 to 3 background treatments
- 1 to 2 support graphics

### Legal pages
Legal pages do not need rich imagery, but they also must not feel abandoned.
Allowed:
- subtle background
- a small supportive header graphic
- restrained section markers

---

## 10. Page-by-page image planning

Before selecting or generating images, the system must produce an **asset plan**.

For each page:
- page type
- priority
- visual style mode
- hero requirement
- number of section visuals
- number of background systems
- support asset need
- density target

Example structure:

```text
Page: Home
Hero: yes
Section visuals: 6
Background systems: 3
Support assets: 2
Style mode: game-atmospheric + modern-editorial hybrid
```

---

## 11. Section image planning

Every important section must receive a visual brief.

Required fields:
- page slug
- section id
- section heading
- content goal
- user intent
- visual goal
- image type
- semantic objects
- mood
- composition suggestion
- placement suggestion

Example:

```text
Section: Upgrades
Content goal: explain priority of upgrades
Visual goal: show upgrade progression clearly
Image type: conceptual illustration
Objects: boat, level markers, arrows, upgrade indicators
Mood: structured, confident, informative
Placement: right media block, desktop
```

---

## 12. Image prompt construction

All generation prompts must be:
- specific;
- section-aware;
- composition-aware;
- style-aware;
- modernity-aware.

Prompts must include:
- subject
- context
- composition
- style mode
- visual tone
- color direction
- realism/illustration level
- exclusions

### Prompt must explicitly avoid:
- childish cartoon look
- generic clipart
- random filler elements
- direct copy of source art
- low-detail flat placeholder feeling

---

## 13. Reference-informed generation

If reference material exists, generation must follow this logic:

### Allowed use
- interpret theme
- infer environment
- infer palette
- infer gameplay objects
- infer mood
- infer content hierarchy

### Disallowed use
- direct copy of poster
- direct copy of screenshot
- direct copy of key art
- exact UI duplication
- exact layout duplication from official visuals

### Output rule
Final image must feel:
- inspired by the topic
- faithful to the niche
- original in composition and rendering

---

## 14. Asset consistency system

All images for a project must feel like the same world.

Consistency vectors:
- palette family
- line/shadow behavior
- lighting logic
- shape language
- mood
- surface treatment
- framing logic
- detail density

Do not let:
- homepage hero feel premium,
- while internal images feel like unrelated clipart.

Consistency is mandatory.

---

## 15. Background generation rules

Backgrounds must support readability.

### Good backgrounds
- subtle thematic wave systems
- abstract maps
- structured grids
- blurred color fields
- environmental shapes
- depth layers

### Bad backgrounds
- loud noisy clutter
- repeated cheap icons everywhere
- aggressive contrast under text
- gimmicky effects
- visually empty flat rectangles when page needs more richness

Backgrounds must work in:
- desktop
- tablet
- mobile

---

## 16. SVG vs generated image balance

The factory may use:
- SVG for patterns, icons, abstract systems, diagrams, decorative support;
- generated raster/illustrative assets for custom hero and conceptual section visuals;
- verified reusable photography/raster imagery when authenticity or real-world context is stronger.

### Rule
Do not force everything into simple SVG if that reduces quality.

Use SVG where SVG is best:
- structure
- pattern
- small support graphics
- scalable decorative systems

Use richer generated or verified reusable raster visuals where they add value:
- hero
- major section illustration
- thematic content anchor image

---

## 17. Image originality quality threshold

A visual fails if it is:
- too generic;
- too simplistic;
- too empty;
- mismatched to the topic;
- visually ugly;
- obviously unrelated to the section.

Each asset should answer:
1. Is it relevant?
2. Is it attractive?
3. Does it feel current?
4. Does it match the theme?
5. Does it improve the section?

If 2 or more answers are “no”, repair, replace or regenerate the asset.

---

## 18. Image richness rule

Each important image should contain meaningful visual structure.

Depending on style, that may include:
- layered depth
- narrative focus
- object hierarchy
- atmospheric background
- subtle detail
- motion implication
- environmental context
- informative symbolism

Avoid:
- isolated object on empty nothingness unless the layout truly demands it.

---

## 19. Thematic image generation for gaming sites

For gaming sites, especially guide/editorial gaming sites:

### The system should extract:
- genre
- gameplay loop
- movement type
- reward systems
- progression systems
- enemies/objects if relevant
- environment type
- style tone
- difficulty rhythm

### Then images should represent:
- mechanics
- strategy
- progression
- categories
- challenges
- decision-making

Do not reduce a gaming site to:
- just random mascot art,
- just a logo block,
- just a shallow decorative illustration.

---

## 20. Contact and legal page visuals

Even non-core pages should have intentional visual direction.

### Contact page
Can include:
- editorial communication visual
- abstract connection visual
- topic-tied support graphic
- subtle location/contact mood treatment

### About page
Can include:
- mission graphic
- editorial collage
- thematic process illustration
- value card visuals

### Legal pages
Can include:
- restrained header support illustration
- calm background system
- section markers
- clean info styling

---

## 21. Image-to-content mapping

Every image must justify its presence.

Accepted mapping:
- explains a concept;
- reinforces a section;
- creates atmosphere;
- supports navigation;
- improves visual pacing;
- reduces emptiness;
- strengthens perceived quality.

Unaccepted mapping:
- random nice-looking art with no relation;
- duplicate visuals across many unrelated sections;
- decorative filler that causes noise.

---

## 22. Image library output model

For each generated site, the system should aim to produce a library like:

- hero-main
- hero-secondary
- section-controls
- section-upgrades
- section-economy
- section-progression
- section-comparison
- section-faq
- section-contact
- bg-primary
- bg-secondary
- bg-grid
- bg-pattern
- badge-01
- badge-02
- support-illustration-01
- support-illustration-02

The exact count depends on site complexity.

---

## 23. Section Image Engine integration

This module extends `15-SECTION-IMAGE-ENGINE.md`.

For each asset, pass forward:

- asset_name
- page_slug
- section_id
- asset_role
- style_mode
- subject
- mood
- palette_hint
- composition_intent
- detail_level
- decorative_boolean
- originality_constraints
- source_reference_summary
- source_mode
- rights_state
- provenance_required
- alt_intent
- image_title_intent

---

## 24. SEO and semantic handoff

Every meaningful visual must produce:
- alt intent
- image title intent
- placement note
- role classification

### Meaningful image
Must receive:
- localized ALT
- localized TITLE

### Decorative asset
Prefer CSS background or decorative classification.

This module improves visuals, but must remain compatible with:
- SEO audit
- accessibility intent
- rendered HTML audit
- content QA

---

## 25. Visual QA gates

The module must not stop at image selection/creation.  
It must run visual QA.

### Required visual QA questions
- Is the image topically correct?
- Is the image visually modern?
- Is the image attractive?
- Is the image section-specific?
- Does the image avoid childish generic style?
- Does the site still feel too empty?
- Do all images feel related?
- Is there enough visual density?
- Are hero and section visuals aligned?

### Hard failure cases
- ugly result
- weak filler look
- too empty
- unrelated theme
- direct-copy appearance
- inconsistent style set
- homepage high quality but internals low quality

---

## 26. Visual richness target

The site should feel closer to:
- premium editorial guide
- niche modern publication
- polished thematic resource

And farther from:
- generic affiliate shell
- placeholder WordPress theme
- random AI image dump
- cheap cartoon microsite

---

## 27. Repair / replacement / regeneration triggers

Repair, replace or regenerate visuals if:
- user says visuals feel poor;
- sections look empty;
- topic is not visually reflected;
- images feel too generic;
- images feel too simple;
- images feel too cartoonish;
- page lacks support graphics;
- images do not improve layout quality;
- a web-sourced candidate has weak rights/provenance, poor crop fit or stock-like mismatch.

---

## 28. User-controlled overrides

The user may define:
- desired style direction
- realism level
- “more premium”
- “more editorial”
- “more dark”
- “more minimal”
- “more colorful”
- “closer to app aesthetic”
- “less cartoon”
- “more modern”

This module must obey those overrides.

---

## 29. Golden-style alignment

When golden theme sources exist, the module must align with them at the level of:
- quality bar
- density
- rhythm
- polish
- compositional richness

But it must not blindly copy previous low-quality image systems.

Golden references are a quality anchor, not a creativity limit.

---

## 30. Operational factory rule

For every new project, the factory should follow this visual flow:

1. read source / app / topic  
2. extract thematic and visual DNA  
3. choose style mode  
4. build asset plan  
5. build page-by-page image plan  
6. define hero visual strategy + source-mode candidates  
7. define section visual strategy + source-mode candidates  
8. define background strategy  
9. generate / curate / prepare assets  
10. inject semantic metadata  
11. perform rendered visual QA  
12. repair / replace / regenerate weak assets if needed  

This must be automatic.

---

## 31. Release rule

A site should not be released as visually complete if:
- it uses mostly primitive filler illustrations;
- internal pages look empty;
- section visuals are weak;
- the image system lacks thematic relevance;
- the site has no real visual depth.

If visual quality fails, the site must return to the visual loop before release.

---

## 32. Summary

This module exists to ensure that Site Factory creates:

- better images
- richer sections
- more modern designs
- stronger thematic coherence
- less emptiness
- less filler
- more premium-looking results

The system must produce original and/or verified reusable, relevant, contemporary visuals guided by the source topic, section intent, rights status and overall site strategy.

**Target outcome:**  
A user should feel that the site has a deliberate visual direction, not just auto-filled images.

---

## 33. Modern-quality override (v1.1 patch)

Default output should feel:
- contemporary;
- refined;
- editorial or premium game-guide appropriate;
- visually rich;
- not childish by default.

Reject by default:
- simplistic cartoon filler;
- low-effort SVG-only site unless topic demands it;
- muddy AI images;
- off-topic fantasy/cyber aesthetics;
- random glows/fog/blur used to hide weak image quality.

## 34. Source-inspired but original Play Store workflow

When the source is Google Play / app listing / game page, the system may extract:
- game loop;
- palette;
- setting;
- objects;
- genre cues;
- UI mood;
- screenshot composition logic.

For assets derived directly from those official/source signals, it must create **original thematic visuals** rather than copy the source. Independently discovered `VERIFIED_REUSABLE_WEB` assets may still be used elsewhere when rights/provenance pass.

Do **not** directly copy:
- official key art;
- exact screenshots;
- exact poster compositions;
- standalone copyrighted cover art.

## 35. Section-to-image compromise rule

Image selection or generation does not happen in isolation.

Before final selection, the system must evaluate whether the chosen artwork actually fits:
- the heading size;
- the section width;
- the layout split;
- the surrounding spacing.

If not, regenerate or reframe.


---

## 36. GEO typography direction (v1.2)

Advanced Visual Direction includes typography, not only imagery.

Before final visual style mode:
1. read GEO + locale;
2. research current typography patterns on high-quality local web properties;
3. inspect candidate font coverage from authoritative/provider sources;
4. test real localized copy;
5. choose the visual type direction;
6. hand it to `03-DESIGN-SYSTEM.md`.

Output:

```text
TYPOGRAPHY DIRECTION
- local_reference_patterns
- serif_sans_rationale
- heading_mood
- body_mood
- shortlisted_families
- selected_pairing
- locale_glyph_evidence
- performance_delivery_note
- fallback_stack
```

Do not let image style and typography come from unrelated visual worlds.

Examples:
- premium editorial imagery + cheap generic UI font = FAIL;
- playful source aesthetic + overly formal newspaper serif without reason = FAIL;
- mature local editorial tone + readable locale-correct serif/sans pairing = candidate PASS.


---

## 37. Hybrid visual-source strategy (v1.3)

Advanced Visual Direction must decide **where originality matters most** and **where authentic reusable web imagery is stronger**.

Do not force all images through generation.

For each visual role decide:
- `GENERATED_ORIGINAL`;
- `VERIFIED_REUSABLE_WEB`;
- `OWNER_SUPPLIED`;
- `ORIGINAL_SVG/CSS`.

Generated assets are preferred when composition, brand-like coherence, conceptual explanation or source-rights limitations require originality.

Reusable web imagery may be preferred when authentic photography, environment, texture, object realism or GEO atmosphere materially improves the section.

Public visibility alone is not reuse permission. Rights/provenance must pass `09-VISUAL-ASSET-ENGINE.md`.

## 38. No accidental frame in generated art

Generation/prompt/crop output must avoid accidental:
- white frame;
- postcard border;
- contact-sheet gutter;
- blank canvas margin;
- letterbox;
- baked rounded card;
- separator line;
- white alpha halo.

Prompt construction for edge-to-edge media should request:
- full-bleed composition;
- no border;
- no frame;
- no matte;
- no text panel;
- no collage divider;
- subject safely inside crop but artwork extending to image edges.

If the generator still returns a frame/matte:
1. crop/retouch if safe;
2. otherwise regenerate;
3. do not hide the artifact with CSS.

## 39. Generated + real-image art direction

When generated and web-sourced images coexist, normalize at art-direction level:
- comparable contrast;
- compatible warmth/coolness;
- intentional crop language;
- coherent corner treatment;
- similar perceived polish;
- no random stock-photo feel.

The goal is a curated editorial visual system, not proof that every asset came from the same tool.

---

## 40. Generated-image dominance rule (v1.3.1 / v4.5.11 alignment)

For each project, generated original thematic imagery must be the primary visual language.

Target mix for meaningful visible raster section images:
- generated original >= 65%
- reusable web or owner-supplied <= 35%

The factory should not drift into a mostly-curated stock/web site.
Reusable imagery exists to support authenticity, not replace the core visual identity.

## 41. Play-market-inspired but original generation requirement
When the project source is Google Play / app store:
- inspect screenshots, icon, palette, gameplay loop and thematic objects;
- create original high-quality visuals informed by those cues;
- ensure the generated set is not just one hero — it should cover multiple section roles.

Required generated roles for app/game guide projects:
- hero;
- progression/mechanics section;
- tips/strategy or controls section;
- at least one support/internal-page section visual.

## 42. SEO-aware visual completion
A visual is not complete until:
- it passes visual quality;
- it is localized;
- its rendered image ALT/TITLE are ready;
- any wrapping link TITLE is ready.

---

## 43. Photoreal professional default (v1.3.3)

The positive default for generated major raster media is no longer merely `not cartoon`.
It is explicitly:

```text
professional editorial photography
high-end commercial photography
cinematic photorealism
expert art direction + retouching
```

### Default visual character
Images should feel as if produced by an experienced photographer/image-maker for a premium editorial or commercial campaign:
- realistic light transport and shadows;
- plausible camera placement;
- natural depth of field when appropriate;
- tactile, believable materials;
- subtle imperfections and texture;
- restrained grading;
- high micro-detail without oversharpening;
- deliberate negative space for layout;
- strong but believable composition.

### For games and apps
The source provides **subject intelligence**, not a mandatory rendering style.
Unless the user explicitly asks for source-faithful stylization, reinterpret game/app mechanics and environments as mature photoreal/cinematic scenes, realistic objects, environments, product/editorial photography or believable composited imagery.

Do not directly reproduce protected characters, logos, screenshots or key art.

### Illustration exception
Illustration remains valid for:
- diagrams;
- process explainers;
- maps/routes;
- abstract concepts that photography cannot communicate efficiently;
- explicitly requested stylized projects.

It is not the default hero/section raster language.

### Expanded reject language
Reject/regenerate when major generated raster reads as:
- children's book art;
- cute/cartoon mascot art;
- flat vector illustration;
- toy photography/diorama;
- plastic 3D render;
- cheap game-ad CGI;
- glossy synthetic stock photo;
- obvious AI fantasy filler;
- overly smooth, sterile, textureless render.

### Web-image cleanliness
Web sourcing is an acquisition detail, not a public content block.
After rights verification and local ingestion, do not expose source description/link in the rendered section unless the licence actually requires visible attribution.


---

## 44. Scene-diversity art direction (v1.3.4)

The Image Style Bible defines a coherent world; it must not collapse into one repeated camera setup.

For a visual-rich site, build a `SCENE DIVERSITY PLAN` before generation.

Track across major assets:
- scene/location;
- subject scale;
- camera height/angle;
- lens/depth character;
- time/light condition;
- primary action;
- dominant material/background;
- composition direction.

Default:
- avoid reusing the same scene + angle + lighting combination for multiple major sections;
- do not keep the same tabletop/board/device setup and merely move stones/objects;
- source inspiration may be consistent, but each major visual should reveal a new facet of the topic.

For game/app guide sites, combine where appropriate:
- realistic physical interpretation;
- device/context shot;
- strategy/analysis scene;
- environment/atmosphere;
- diagrammatic/annotated visual;
- detail/macro material image.

This increases uniqueness without abandoning the site's visual family.



---

## 45. Adult Premium Visual Tier (v2.0.0)

Default tier for general-audience gaming, app-guide, editorial and showcase builds:

```text
ADULT_PREMIUM_EDITORIAL
```

Positive direction:
- mature editorial photography;
- cinematic photorealism;
- premium commercial still-life/environment photography;
- believable materials, weather, water, light and depth;
- controlled color grading;
- sophisticated composition;
- tactile detail and natural imperfection;
- no fake marketing text baked into scene assets.

Default reject unless explicitly source/audience-appropriate:
- childish illustration;
- cute mascot language;
- toy/diorama look;
- plastic low-detail CGI;
- generic flat vector poster as a major raster substitute;
- cheap mobile-ad fantasy rendering;
- hyper-saturated neon without thematic justification;
- overly smooth AI surfaces;
- fake webpage/mockup output when a scene asset was requested.

If the source clearly targets children, remain age-appropriate; do not force adult subject matter. The quality bar still remains professional and non-cheap.

## 46. Rich Visual Mix Contract

For visual-rich Home pages, when supported by section semantics, target a deliberate mix:

```text
major_generated_raster_scenes: 4–7
bespoke_major_svg_or_diagram_visuals: 3–6
distinctive_section_background_treatments: 2–5
quiet_text_led_sections: at least 1 where useful
```

These values are envelopes, not quotas.
Do not add meaningless filler merely to reach a number.

For key internal pages, rotate dominant medium:
- raster-led;
- diagram/SVG-led;
- background-led;
- editorial text/data-led.

Do not make every internal page a smaller clone of the Home media recipe.

## 47. Bespoke SVG / Diagram Engine

SVG is a first-class editorial medium, not a fallback icon format.

### Major SVG family pool
- `SV01_ROUTE_PATH_MAP`
- `SV02_UPGRADE_TREE`
- `SV03_ECONOMY_LOOP`
- `SV04_PROCESS_SWIMLANE`
- `SV05_RADIAL_SYSTEM_MAP`
- `SV06_LAYERED_ANATOMY_DIAGRAM`
- `SV07_TIMELINE_WITH_MILESTONES`
- `SV08_COMPARISON_SPECTRUM`
- `SV09_STATE_TRANSITION_MAP`
- `SV10_RESOURCE_FLOW`
- `SV11_CONTROL_INPUT_MAP`
- `SV12_RISK_REWARD_CURVE`
- `SV13_TAXONOMY_FIELD`
- `SV14_ANNOTATED_OBJECT_BLUEPRINT`
- `SV15_PROGRESS_LADDER`
- `SV16_LOCATION_OR_ZONE_MAP_ABSTRACT`
- `SV17_SCORE_OR_METRIC_DASHBOARD_ILLUSTRATION`
- `SV18_EDITORIAL_LINE_ART_SCENE`
- `SV19_MECHANIC_RELATIONSHIP_GRAPH`
- `SV20_COMPACT_FACT_SYSTEM`

### Rules
A bespoke major SVG must:
- explain or reinforce a real section concept;
- use site-specific geometry, not a generic downloaded diagram;
- inherit the project color system without becoming a recolored clone of another site's SVG;
- have responsive simplification;
- keep text in HTML whenever practical rather than baking long copy into SVG;
- have a `visual_signature` and recent-history uniqueness check;
- not repeat as major media across unrelated pages by default.

Tiny icons do not count toward bespoke SVG depth.

## 48. Section Background Illustration Engine

Backgrounds are authored visual layers, not only solid fills.

### Background family pool
- `BG01_EDITORIAL_GRAIN_FIELD`
- `BG02_CONTOUR_LINE_FIELD`
- `BG03_THEMATIC_LINE_ART`
- `BG04_GHOSTED_DIAGRAM`
- `BG05_FADED_SCENE_BACKPLATE`
- `BG06_DEPTH_GRADIENT_MESH`
- `BG07_RADIAL_LIGHT_STAGE`
- `BG08_TOPOGRAPHIC_PATH_FIELD`
- `BG09_WAVE_OR_FLOW_LINES`
- `BG10_ARCHITECTURAL_FRAME_FIELD`
- `BG11_ENVIRONMENTAL_SILHOUETTE`
- `BG12_DATA_GRID_WITH_SOFT_NOISE`
- `BG13_MACRO_TEXTURE_WASH`
- `BG14_MATERIAL_PAPER_OR_METAL_FIELD`
- `BG15_EDGE_ILLUSTRATION`
- `BG16_CORNER_SCENE_LINE_ART`
- `BG17_PARTICLE_DEPTH_FIELD`
- `BG18_LIGHT_CAUSTICS_OR_REFLECTION_FIELD`
- `BG19_MAP_GRID_OVERLAY`
- `BG20_OBJECT_SHADOW_FIELD`
- `BG21_EDITORIAL_STRIPE_SYSTEM`
- `BG22_SOFT_VIGNETTE_STAGE`
- `BG23_SECTION_SPECIFIC_PATTERN`
- `BG24_MEDIA_VEIL_WITH_SAFE_TEXT_ZONE`

### Background manifest
For each non-plain background record:

```text
background_asset_id
background_family
source_mode
semantic_role
contrast_safe_zone
intensity
edge_behavior
mobile_simplification
motion_mode
reuse_policy
visual_signature
```

### Usage
- use distinctive backgrounds selectively;
- keep intentional plain/rest sections between richer moments;
- do not repeat the same major background illustration across unrelated sections;
- decorative micro-pattern systems may repeat if explicitly classified as Design DNA support;
- mobile may remove or simplify complex background layers.

## 49. Generated Scene Independence

For major generated raster scenes:
- one section brief → one independently conceived scene;
- no contact-sheet/collage slicing into multiple major assets;
- no repeated device/tabletop/room setup with superficial object changes;
- vary camera, environment, scale, time/light and action;
- preserve coherent Design DNA through palette/material/grade rather than scene duplication.

Before accepting a generated asset, classify output:

```text
SINGLE_SCENE_VALID
DIAGRAM_VALID
DEVICE_CONTEXT_VALID
WEBSITE_OR_MARKETING_MOCKUP_REJECT
COLLAGE_OR_CONTACT_SHEET_REJECT_FOR_MAJOR_MULTIUSE
LOW_DETAIL_REGENERATE
CHILDISH_STYLE_REGENERATE
```

## 50. Visual Medium Rhythm

Create a site-level `VISUAL MEDIUM RHYTHM` such as:

```text
RASTER → QUIET → SVG → BACKGROUND → RASTER → DATA → SVG → RASTER → QUIET
```

or another semantically valid sequence.

Avoid:
- raster after raster after raster with identical frame treatment;
- every section represented by cards;
- every explanation represented by the same diagram grammar;
- every section using a decorative background.

Variation must remain coherent with the site's color/material/type DNA.

## 51. Premium Quality Preservation During Fix Loops

When fixing layout, contact, SEO or duplication defects:
- do not downgrade a strong major raster to a generic icon/SVG merely for convenience;
- do not remove rich background art without replacing its visual function when the section becomes empty;
- replacement assets must meet or exceed the prior quality tier;
- preserve the intended visual-density envelope unless the section semantics changed.

A technical fix that makes the site visibly cheaper is not a complete fix.



## 51. Live UI/UX research visual handoff (v2.1.0)

Module 16 consumes the `LIVE UIUX RESEARCH MANIFEST` from module 18 when available.

It may learn abstract visual pacing such as:
- image-to-text ratio;
- when a section uses full-bleed media versus diagram/data;
- background intensity rhythm;
- editorial framing;
- transition style;
- how long pages use visual rests.

It must not reproduce a reference site's exact art, screenshots, animation, typography lockup or distinctive composition.

## 52. Rich-page media pacing

When internal pages become longer, visual support must scale intelligently.

For a key `950–1700` word page, normally plan:
- `2–4` meaningful visual/data/diagram moments when useful;
- at least one non-raster explanatory medium where the content benefits from it;
- intentional quiet reading sections between richer visual stages;
- no decorative image inserted solely to interrupt text.

Do not make every internal page use the same sequence:
`hero image → text → SVG → cards → CTA`.
Rotate media rhythm according to page intent and live-research findings.



## 52. Interactive media harmony (v4.8.0)

When media participates in tabs, sliders, rails, lightboxes or state-switchers:
- every item remains semantically tied to its heading/copy;
- a carousel is not permission to dump visually unrelated assets;
- slide crops should feel like a deliberate series while preserving subject diversity;
- tabs that change media need stable aspect-ratio strategy to avoid layout jump;
- lightbox/zoom is used for inspectable detail, not as a default decoration;
- hover media effects remain subtle and preserve legibility/subject integrity;
- touch users see a stable intentional crop without relying on hover.

Interactive media assets remain subject to major-image uniqueness and metadata-sanitization rules.



## 53. OFFICIAL GAME STUDIO VISUAL STORYTELLING (v4.8.1)

When `business_model_mode = OFFICIAL_GAME_STUDIO`, visual planning should reinforce the first-party studio/product story rather than look like an unrelated review portal.

Recommended visual roles include:
- hero/product world establishing scene;
- gameplay/mechanic explanation;
- progression/system diagram;
- art-direction/material/mood board;
- prototype/iteration/process visualization;
- balancing/testing flow;
- release/update/support visual;
- studio/product brand moments.

The sequence should help communicate:

```text
STUDIO → IDEA → BUILD → MECHANICS → TEST/REFINE → RELEASE → PLAY
```

This is a narrative model, not permission to invent documentary evidence.

### Documentary-truth boundary
Do not generate or present as factual evidence:
- fake photographs of the actual development team;
- fake office/studio interiors claimed as real;
- fake screenshots of internal tools/builds;
- fake archival concept art claimed to be original production material;
- fake whiteboards, code captures, milestone documents or QA reports.

If generated visuals illustrate a development concept/process rather than document a real artifact, their role must remain clearly conceptual/illustrative in the asset manifest and surrounding copy when confusion is plausible.

Owner-supplied/verified genuine behind-the-scenes assets may be used according to normal rights/provenance rules.

### Product-promotion priority
The strongest visuals should support the actual game proposition and play/download conversion. Behind-the-scenes/process visuals enrich the story but must not displace clear game/product imagery.



## 54. MANDATORY BRAND UTILITY ICON SET (v4.8.2)

The visual plan must include a compact site-icon/favicons asset role for every full production site.

Create `BRAND_UTILITY_ASSET_SET`:

```text
brand_mark_source
favicon_svg_or_vector_mark
favicon_small_png
apple_touch_icon
site_icon_large_square
current_site_brand_signature
```

When no owner-supplied brand icon exists, derive an original simple mark from the site's Design DNA/domain brand. It must remain legible at tiny sizes and must not be a random unrelated symbol.

Design requirements:
- square-safe silhouette;
- strong small-size contrast;
- minimal detail;
- no tiny text;
- no copied third-party/game logo unless rights/owner input permit it;
- consistent with current brand colors/forms;
- stale icon from a previous build = reject.

The favicon is excluded from the thematic-raster generation ratio, but it is **not optional** for production completeness.

Handoff:
- Runtime owns `<head>`/WordPress Site Icon behavior;
- SEO owns head/audit parity;
- QA verifies reachable final assets and current-brand match.


<!-- BUNDLE-MODULE-END: 16-ADVANCED-VISUAL-GENERATION.md -->

---



## 55. STUDIO / TEAM / DEVELOPMENT VISUAL NARRATIVE (v4.8.3)

For first-party studio sites, visual storytelling should make the **work behind the product** visible, not only repeat gameplay scenes.

### Preferred visual jobs

Depending on the source/evidence, create distinct visuals for:
- product/game world;
- mechanic interaction;
- level/progression structure;
- control/feedback relationship;
- visual-language/art-direction study;
- design challenge / constraint diagram;
- system flow / state map;
- balancing/refinement concept;
- development stages/framework;
- update/support relationship;
- studio/team principles as abstract work/process visualization.

### Team depiction rule

Do not generate anonymous people and present them as the actual studio team.

If no genuine team imagery is owner-supplied/verified, represent `our team` through:
- hands/process/details without identity claims;
- abstract collaboration/workflow graphics;
- product artifacts/diagrams that show disciplines;
- studio brand/product environment;
- role-neutral process scenes clearly treated as conceptual.

No fake staff portraits, fake named profile photography, fake office documentary or invented archival material.

### Process visual hierarchy

A strong rich studio site should normally contain several **different** process/product media roles rather than one repeated cinematic game image. For example:

```text
GAME WORLD SCENE
→ SYSTEM DIAGRAM
→ LEVEL / PROGRESSION VISUAL
→ ART / READABILITY STUDY
→ TEST / REFINE FLOW
→ PRODUCT CTA VISUAL
```

This sequence is illustrative, not fixed; composition and cross-site history still control layout selection.

### Documentary evidence distinction

Every behind-the-scenes-looking asset records:

```text
DOCUMENTARY_OWNER_SUPPLIED
DOCUMENTARY_VERIFIED_SOURCE
CONCEPTUAL_PROCESS_VISUAL
PRODUCT_EXPLANATION_VISUAL
```

Only the first two may be presented as real documentary development material.


## 56. SECTION-SPECIFIC ORIGINAL VISUAL + MICRO-ICON ENGINE (v4.8.4)

This section strengthens the existing Section Image Engine for future rich gaming / official-studio builds. Where older wording made section visuals optional or treated generation as merely one equal habit, this module is authoritative for **major narrative sections**.

### 56.1. Major-section dedicated visual requirement

For every major Home section and every major thematic section on key internal pages:

```text
CONTENT BRIEF
→ SECTION HEADING MEANING
→ PARAGRAPH CLUSTER SUMMARY
→ VISUAL JOB
→ DEDICATED VISUAL BRIEF
→ CREATE / GENERATE / DRAW THE BEST ORIGINAL VISUAL FORM
→ SEMANTIC QA
→ PLACE
```

Default for rich gaming/studio builds: create a **separate, section-specific visual asset** rather than reusing a broad `game` image.

Preferred visual form by content:
- atmosphere / product moment → generated original raster scene;
- mechanic / system relationship → generated conceptual scene or original diagram;
- level/progression → original map/runway/sequence visual;
- development/process → original process illustration/diagram unless documentary evidence exists;
- art/readability → original visual study / controlled scene pair;
- testing/refinement → conceptual iteration/comparison visual without fake metrics;
- studio/team philosophy → abstracted craft/collaboration/process visual unless real team imagery exists;
- support/contact → restrained iconography/micro-visual system; major raster only when useful.

Do not use a large raster merely to satisfy a quota. If raster adds little meaning, use a bespoke SVG/diagram/iconographic composition instead.

### 56.2. Image-to-copy semantic lock

Every dedicated major asset records:

```text
section_heading_meaning
paragraph_cluster_summary
visual_job
visual_must_show[]
visual_must_not_imply[]
semantic_match_reason
```

Acceptance question:

> If the heading/body text were hidden, would the visual still plausibly communicate the same topic? And when the text is restored, does the visual explain/support it rather than merely match the site's general gaming mood?

If not, `REGENERATE / REDRAW / RESELECT`.

### 56.3. Adult premium image default

Major generated raster direction defaults to mature, premium, editorial/commercial quality unless source art direction explicitly requires something else.

Require:
- clear intentional subject;
- controlled composition and negative space based on layout needs;
- believable lighting/depth/material response;
- crisp detail and clean edges;
- thoughtful focal hierarchy;
- no random embedded labels/UI;
- no cheap stock-photo smile/pose;
- no childish mascot/cartoon shorthand;
- no toy/plastic CGI;
- no generic fantasy/cyber filler;
- no repeated cinematic scene recipe for every section.

### 56.4. Cross-section visual-role diversity

A site should rotate meaningful visual roles rather than repeat `cinematic scene in frame` everywhere.

Healthy mix may include:

```text
SCENE
OBJECT / DETAIL STUDY
DIAGRAM
PROCESS MAP
LEVEL / PROGRESSION VISUAL
ANNOTATED SYSTEM
DIPTYCH / STATE COMPARISON
TEXTURE / MATERIAL STUDY
ICONOGRAPHIC LEDGER
MICRO-VISUAL FIELD
```

For rich Home pages with 7+ meaningful sections, target at least `4` materially different visual-role families when content supports them.

### 56.5. Site-specific icon family

Before UI implementation create:

```text
ICONOGRAPHY_MANIFEST
site_icon_family_id
style_family
source_mode = ORIGINAL_SVG | ORIGINAL_DRAWN
stroke_or_fill_strategy
optical_grid
corner_language
size_tiers[]
semantic_roles{}
section_assignments{}
allowed_reuse{}
forbidden_generic_substitutions[]
```

Normal target for a rich gaming/studio site when semantics support it:
- roughly `12–24` distinct small icons/glyphs;
- at least several topic-specific icons, not only generic `arrow / check / info` symbols;
- consistent family across feature/process/contact/support/metadata moments.

Examples of topic-aware icon concepts:
- movement/input;
- checkpoint/progression;
- heat/pressure/state;
- obstacle/hazard;
- iteration/prototype;
- balance/tuning;
- visual/readability;
- testing/verification;
- support/contact/store.

Only use concepts actually supported by the product/content.

### 56.6. Micro-visual toolkit

The factory may create and place original:
- section markers;
- numbered stage nodes;
- connectors;
- fact glyphs;
- tiny illustrative diagrams;
- branded bullets;
- micro badges/chips;
- compact state indicators;
- decorative rules/anchors derived from Design DNA.

These are created to improve hierarchy/scanning and make the site feel authored. They must not become a noisy icon soup.

### 56.7. Reuse semantics

Small icons may repeat only when their meaning repeats. Reuse of the same icon for unrelated meanings is prohibited.

Major visuals remain unique by default. A crop, color filter, mirrored layout or background swap does not create a new visual.

### 56.8. Generation workflow integration

For visual-rich builds, generation/creation is planned per section **after copy meaning is known**, not from a site-wide generic prompt batch.

Prompt inputs now include:

```text
section_heading_meaning
paragraph_cluster_summary
visual_job
semantic_subject
required_action_or_state
layout_focal_zone
text_safe_zone
visual_role_family
site_image_style_bible
negative_constraints
```

The engine should generate/select the final assets as separate outputs. Do not publish raw contact sheets/collages as a shortcut for multiple section images.

### 56.9. Internal-page requirement

For each key internal studio/product/development page:
- opening visual/background = unique to that page;
- at least `2` additional section-specific visual moments for rich pages where content supports them;
- at least one visual moment should differ in **visual role family** from the opening;
- micro-icon/diagram support should be added where semantic structure benefits.

Utility/legal pages may remain visually quieter.

### 56.10. Blocking visual defects

`VISUAL_FAIL` when:
- visual semantic match is weak/generic;
- major image reused across unrelated sections;
- near-identical generated scenes dominate several sections;
- section-specific prompt ignores heading/body meaning;
- adult/premium direction degrades into childish/toy/cheap AI aesthetics without source reason;
- all process/mechanic content is only text despite clear diagram/icon opportunities;
- icon styles are mixed or generic-library-looking;
- micro-visuals are decorative noise with no hierarchy/semantic value.




## 57. TEAM / WORKFLOW PHOTOGRAPHY DOMINANCE (v4.8.5)

For rich `OFFICIAL_GAME_STUDIO` sites, visual storytelling now follows the business model: the studio/team/work behind the product should be seen before the page becomes product-detail heavy.

### 57.1 Hero priority

Across Home + key non-legal pages:

```text
team_or_workflow_led_heroes >= 70%
product_only_heroes <= 30%
```

Home hero defaults to a **premium team/work/development scene** when a truthful first-party studio relationship is active.

Key page hero subjects should vary by discipline:
- product review;
- game design collaboration;
- systems/mechanics review;
- level planning;
- art-direction work;
- QA/balance session;
- release/support coordination;
- studio strategy/creative review.

Do not use the same meeting-room composition repeatedly.

### 57.2 Upper/middle-page image priority

For a rich key page, normal target:

```text
2–4 major team/work/process visuals
1–3 major product/game visuals
```

The first and middle major visual moments should normally be team/work/process led.

Game screenshots/product close-ups become stronger in the lower part of the page where the narrative moves from work → result.

### 57.3 Adult premium photographic direction

Default generated visual direction:
- credible adult professionals;
- premium contemporary studio/workplace;
- cinematic but believable lighting;
- authentic work posture;
- design review / testing / planning / production context;
- sophisticated editorial/commercial photography;
- realistic materials, screens, desks and tools;
- no childish toy aesthetic;
- no cartoon office scene;
- no exaggerated startup-stock smiles;
- no fake text baked into monitors/whiteboards;
- no visibly nonsensical hands/UI when avoidable.

### 57.4 Conceptual team scenes vs documentary team photos

Generated people are **illustrative studio/workflow scenes**, not documentary evidence of actual employees.

Asset manifest state:

```text
TEAM_VISUAL_ROLE =
  OWNER_SUPPLIED_REAL_TEAM
  VERIFIED_REAL_TEAM
  CONCEPTUAL_STUDIO_WORK_SCENE
```

Only the first two may be captioned or described as literal real staff photography.

`CONCEPTUAL_STUDIO_WORK_SCENE` may support the studio story but must not:
- name people;
- claim the pictured people are real employees;
- claim the pictured room is the real office;
- be used as proof of headcount/roles/location.

### 57.5 Hero scene diversity bank

Rotate among:
- collaborative screen review;
- level-design planning table;
- art-direction/color review;
- systems design session;
- QA/balance analysis;
- prototype review;
- release readiness meeting;
- support/product coordination;
- desk-level hands/tools/detail;
- remote/hybrid collaboration;
- production board review;
- creative director + team critique without identifying real individuals.

### 57.6 Product visual transition

A preferred page visual rhythm is:

```text
TEAM / WORK HERO
→ WORK DETAIL / TASK
→ PROCESS / REVIEW
→ PRODUCT RESULT
→ GAME DETAIL / MECHANIC
→ CTA / STORE
```

The exact layout remains randomized.

### 57.7 Anti-stock / anti-repetition gate

Reject:
- five pages using the same four-person meeting around one monitor;
- generic handshake/business stock;
- smiling call-center imagery unrelated to the section;
- childlike illustration where mature business photography is required;
- product-only visual rhythm that hides the company/team model.



## 58. TEXT-GROWTH VISUAL-DENSITY + EDITORIAL MEDIA RHYTHM (v4.8.6)

When content density changes, visual planning must be recalculated. The ~30% compact-copy policy must not be converted into weaker media rhythm or larger empty shells.

### 58.1 Media-density planning

For rich non-legal pages, evaluate one meaningful visual moment per approximately `300–450` visible words.

This is an evaluation cadence, not a quota.

A visual moment may be:
- premium team/workflow photo;
- product/game image;
- original diagram;
- annotated process visual;
- compact gallery;
- editorial inset;
- image wrap;
- visual comparison;
- meaningful background illustration.

### 58.2 Studio-first priority

In the upper/middle zones:
- team/work/process imagery should remain dominant;
- different pages should show different work situations;
- do not reuse one generic meeting composition.

Lower zones may shift toward product/game results.

### 58.3 Editorial photo placement families

Support:
- full-bleed scene;
- side media;
- floated editorial image;
- inset image;
- vertical photo rail;
- panoramic strip;
- overlapping photograph;
- two-image stagger;
- work-detail close-up;
- team-wide scene + detail pair.

### 58.4 Media omission rule

If a major image is removed/rejected:
- either replace/regenerate;
- or redesign the section to a text-led family.

Never leave the old media geometry empty.

### 58.5 Visual repetition audit

Track:

```text
visual_scene_family
camera_relationship
subject_count
workspace_context
composition_direction
crop_family
section_visual_role
```

Near-identical work scenes should be treated as repetition even when filenames differ.

### 58.6 Photo/text harmony

A photo should not look like a small sticker beside a large body of text.

Check:
- visual scale;
- copy weight;
- focal direction;
- crop;
- neighboring section rhythm;
- caption/semantic relationship.

If the image is too weak for the copy, enlarge/recompose or remove it and use a stronger text-led design.


---

## 59. ADULT PREMIUM PHOTOGRAPHY-FIRST ENGINE (v4.9.1)

For premium commercial/product/gaming builds, the default major-media language is **adult editorial photography / photorealistic imagery**, not flat doodles, generic vector scenes or diagram-heavy pages.

### 59.1 Major visual mix

For Home + representative key pages, target:

```text
photographic_or_photoreal_major_visual_ratio >= 0.70
abstract_vector_or_diagram_major_visual_ratio <= 0.20
childlike_cartoon_or_doodle_major_visual_count = 0
```

A vector illustration may be elegant and still be the wrong medium. Repetition of custom SVG scenes does not become premium merely because each file is unique.

### 59.2 Preferred imagery

Prefer contextually truthful, mature visual directions such as:
- cinematic/editorial sports environments;
- adult players/fans/coaches in believable situations;
- premium device-in-hand / over-shoulder product context;
- stadium, tactical, urban or studio atmospheres when relevant;
- controlled close-ups and material detail;
- source-owned official screenshots when usage is appropriate.

When source photography is unavailable, generate original photorealistic editorial imagery. Do not generate fake gameplay UI or visuals that imply an unverified studio/team relationship.

### 59.3 Diagram limit

Diagrams, radar charts, tactical boards, SVG explainers and abstract compositions are **secondary** media. They may support explanation, but:
- never default the hero to a diagram when a premium photo-led concept is viable;
- do not use diagram-after-diagram as the page's primary visual rhythm;
- do not count icons/utility SVGs as major media moments;
- no “childlike doodle”, mascot/cartoon, clip-art or simplistic line-scene style for an adult premium build unless the owner explicitly requests it.

### 59.4 Image-generation quality gate

Generated photorealistic images must pass:
- adult/professional tone;
- believable anatomy and hands;
- no accidental text/logos/watermarks;
- no fabricated awards/claims;
- coherent lighting/crop;
- enough resolution for intended display size;
- unique composition across major sections.


---

## 60. CONTENT-ASSET-ONLY GENERATION MODE (v4.9.2)

Normal BUILD image generation operates in `CONTENT_ASSET_ONLY` mode.

Allowed by default:
- standalone editorial / photoreal content photography;
- environment, people, sports and product-context imagery;
- section-specific production media;
- secondary diagrams only when the media mix allows them.

Not allowed by default:
- full webpage mockups;
- landing-page screenshots;
- baked-in navigation, headings, buttons or whole UI compositions;
- generated fake gameplay screenshots.

Before generation, record the intended `target_page`, `target_section`, semantic role, crop/orientation and truth constraints. After generation, the file must be integrated into the real theme or discarded. Unused concept renders do not count toward media density.

HTML/CSS/JS owns layout, typography, responsiveness and section geometry. Browser rendering owns visual acceptance.


---

## 61. PRODUCTION PHOTO OPTIMIZATION + FALLBACK (v4.9.3)

Every packaged major content photo must be optimized for real web delivery.

Default photo pipeline:
- remove unnecessary metadata/EXIF;
- resize to the largest actually required display width;
- keep aspect ratio intentional;
- generate responsive large and medium variants when useful;
- encode WebP at visually high quality;
- encode JPEG fallback at visually high quality;
- avoid shipping only the original oversized source.

Normal practical targets for a 16:9 editorial asset:
```text
large: about 1440–1600 × 810–900
medium: about 900–1000 × 506–563
WebP quality: roughly 78–84
JPEG quality: roughly 80–86
```

Targets are quality envelopes, not rigid values.

Quality checks:
- no obvious banding/blocking around faces or stadium lights;
- skin and hands remain believable;
- crop preserves the intended subject;
- file is not needlessly multi-megabyte;
- both WebP and JPEG fallback decode successfully.

A production photo is not considered integrated until browser QA confirms it actually displays.
