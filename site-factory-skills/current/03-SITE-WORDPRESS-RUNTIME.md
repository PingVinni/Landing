# 03 SITE WORDPRESS RUNTIME

**Bundle format:** Source Bundle v1.5  
**Policy baseline:** Site Factory v4.9.14  
**Bundling rule:** logical module boundaries and aliases are preserved inside bundles. Source Bundle v1.5 applies the Site Factory v4.9.14 interaction, micro-motion, hover/focus and semantic interactive-section expansion while preserving v1.4 rich-content, live UI/UX research, morphological section variation, v1.3 adult-premium visuals and the 7-file Project Source architecture.

## Module aliases in this bundle

- `04-SITE-ARCHITECTURE.md` → this file, section `LEGACY MODULE: 04-SITE-ARCHITECTURE.md`
- `05-WORDPRESS-RUNTIME.md` → this file, section `LEGACY MODULE: 05-WORDPRESS-RUNTIME.md`
- `06-LINKS-PERMALINKS.md` → this file, section `LEGACY MODULE: 06-LINKS-PERMALINKS.md`

## Cross-reference rule

References inside logical module text to filenames such as `15-SECTION-IMAGE-ENGINE.md` remain valid **logical module IDs**. Resolve them against the module aliases declared across the loaded Source Bundles. `SOURCE-BUNDLE-MAP.md` is maintenance documentation only and is **not required** as a Project Source.

---

<!-- BUNDLE-MODULE-START: 04-SITE-ARCHITECTURE.md -->

# LEGACY MODULE: 04-SITE-ARCHITECTURE.md

# SITE ARCHITECTURE

**Version:** 4.6.0  
**Role:** формування сторінок, rich-content depth та information architecture

---

## 1. Architecture formula

`CORE + DOMAIN + LEGAL`

Не існує універсального page count для всіх ніш.

---

## 2. Core pages

За замовчуванням:

- Home
- About
- Contact

### Contact page — обов'язкова глибина
Contact не може бути заглушкою з одним реченням.

Має містити:
- public email state;
- phone state;
- address state;
- service/support scope;
- opening/response expectations лише якщо реально відомі;
- external official support, якщо він справді належить продукту/джерелу;
- privacy note;
- related legal links;
- optional map/location block лише якщо реальна адреса підтверджена.

Якщо owner contacts відсутні, factory може використати `SYNTHETIC_GEO_CONTACT` згідно з `13-CONTACT-GEO-ENGINE.md`.
Synthetic contacts можуть виглядати production-ready у UI, але не вважаються verified/working/legal identity.

---

## 3. Domain pages

Page jobs are selected by **business model first**, then niche/source depth. There is no universal gaming-guide page set.

### `OFFICIAL_GAME_STUDIO` — default gaming/product branch
When the developer/brand relationship truth gate passes, the site is a first-party studio/product site. Prefer 3–6 domain pages or equivalent deep sections from:

- Game / Product
- Development / Making of
- Mechanics Design
- Levels / Progression Design
- Controls & Feel
- Art / Visual Direction
- Testing / Balancing
- Updates / Release story — only when factual
- Support / FAQ

The dominant thematic weight should be **studio + product + development**, not outsider gameplay guidance. A pure `Game Guide / Tips / Library` set is a model-drift defect for an official studio unless the product genuinely needs those pages.

### Other business models
Editorial/service/store examples remain valid only when the active business model calls for them.

---

## 4. Legal pages

Завжди provision:
- Privacy Policy
- Terms
- Cookie Policy

Footer links обов’язкові.

---

## 5. Page Manifest

Для кожної сторінки:

- stable factory key;
- localized title;
- canonical slug;
- type: core/domain/legal;
- purpose;
- primary intent;
- navigation role;
- section plan;
- CTA;
- related pages;
- SEO intent;
- visual asset requirements;
- interactive pattern;
- provision automatically: yes/no.

---

## 6. Home architecture

Home must communicate the active business model, not behave like a generic article index.

### `OFFICIAL_GAME_STUDIO` Home story
A rich studio/product Home normally distributes 7–11 meaningful roles such as:

1. studio + game opening / product proposition;
2. what we built / player promise;
3. one strong gameplay/product proof moment;
4. design challenge or product principle;
5. development/process story;
6. mechanic / level / art / controls design spotlight;
7. team/studio approach at a truthful level;
8. testing/refinement or product proof when supported;
9. support / FAQ / platform context;
10. play/download/store conversion.

This is a semantic story arc, **not a fixed visual sequence**. Section order and geometry still come from the composition engine and Layout DNA history.

Gameplay description should support the product story; it must not consume the entire site while the studio/development model remains invisible.

---

## 7. Internal page depth

### Default depth envelope
Для ключової domain page:
- 4–7 meaningful content blocks;
- 1–3 media/visual moments;
- related links;
- one context-specific CTA;
- FAQ/steps/comparison/table тільки коли доречно.



Заборонено робити всі domain pages однаковими:

`H1 + paragraph + 3 cards`

Кожна сторінка має мати власний content pattern.

Наприклад:
- guide → article + steps + related content;
- catalog → filters/categories/items;
- comparison → table + explanation;
- glossary → alphabet/filter;
- examples → media gallery + context;
- FAQ → accordion + related links.

---

## 8. About

About follows the active business model.

### `OFFICIAL_GAME_STUDIO`
About is a Studio page, not an editorial-methodology page. It should normally establish:
- who the studio/brand is;
- what game/product it represents;
- what kind of experience/product it is building;
- product/creative principles;
- how the team approaches design/development at the evidence-supported level;
- team identity in aggregate (`our team`) when the creator relationship is resolved;
- named people, roles, headcount, offices, founding dates or biographies **only** when owner-supplied/verified;
- play/download and support continuation.

Do not inject `independent editorial`, `sourcing methodology`, `review portal` or similar language into this branch.

### Independent/editorial modes
Editorial method/provenance/independence remain valid only when the active business model is actually editorial.

---

## 9. Proof / trust

Trust is selected by business model.

### `OFFICIAL_GAME_STUDIO`
Synthetic player/customer/editorial testimonials are **not mandatory and are prohibited as factual proof**. Prefer:
- verified store presence;
- sourced real player/store reviews when available;
- sourced press/coverage when available;
- observable product features;
- development/process transparency;
- real update/support information;
- concrete product screenshots/visual explanations where rights allow.

If no external review evidence exists, use product/development proof instead of inventing voices.

### Editorial modes
Illustrative/synthetic editorial-review patterns may exist only where the separate content policy explicitly permits them and disclosure is correct.

---

## 10. Product / development information pages

For `OFFICIAL_GAME_STUDIO`, do not default to catalog/library/guide pages merely because the niche is gaming. Select pages that deepen the studio/product story:
- product/game overview;
- development story;
- mechanics systems;
- level/progression design;
- controls/feel;
- art direction;
- testing/balancing;
- factual updates/release notes;
- support/FAQ.

Catalogs, collections, libraries, guides and comparisons remain valid only when the actual product/business model benefits from them.

A full thematic site should feel like a **studio/product website with a coherent business purpose**, not a collection of SEO articles.

---

## 11. Page-context integrity

На внутрішній сторінці:
- URL;
- menu label;
- eyebrow/breadcrumb;
- H1;
- Site Manifest

мають відповідати одна одній.

Technical IDs, namespace, text-domain або internal keys не повинні з’являтися в UI.


---

## 12. Contact Profile placement

Контактні дані, якщо вони відомі/підтверджені, повинні узгоджено використовуватись у:
- Contact page;
- footer;
- About/contact section;
- Privacy Policy;
- Terms;
- structured data, якщо воно реально генерується.

Email/phone/address у різних місцях не можуть суперечити один одному.

---

## 13. Mandatory proof + consent architecture (v4.2 patch)

Кожен full site повинен включати:

### Reviews / testimonials
- мінімум 1 dedicated reviews/testimonials section;
- зазвичай `3–6` localized synthetic editorial reviews with disclosure;
- review author names мають відповідати GEO/locale;
- можна використовувати short quote + context label + rating cue;
- reviews не повинні виглядати autogenerated spam.

### Cookie system
- compact cookie bar/banner;
- окремий cookie settings modal / preferences dialog;
- direct links на Privacy Policy та Cookie Policy;
- localized concise copy.

## 14. Internal-page fullness patch

Кожна domain page повинна мати не менше:
- 3 meaningful content sections;
- 1 meaningful image or SVG-supported media block;
- 1 related-links / onward-navigation zone;
- 1 CTA, summary box або practical note.

Thin one-screen internal pages = FAIL.


---

## 15. Global Text architecture (v4.3)

Every managed page must receive a stable `page_key` that maps to a branch in `global-text.json`.

Example:

```text
page_key: home
text_root: pages.home

page_key: guide
text_root: pages.guide

page_key: privacy
text_root: legal.privacy
```

The page/section architecture owns **where** text appears; `17-GLOBAL-TEXT-ENGINE.md` owns **where the text value is stored**.

### Hierarchical location model

The editable file must be self-navigable:

```text
site
navigation
pages
  home
    hero
    sections
  guide
  controls
components
  reviews
  cookie
contact
legal
  privacy
  terms
  cookies
footer
errors
seo
images
links
accessibility
```

Optional reserved keys beginning with `_`, such as:

```text
_location
_note
```

may explain placement for FastPanel editing and must never render publicly.

### Page rendering rule

Managed pages are structural WordPress entities. Their public content must not depend on a one-time copied `post_content` snapshot when that would prevent `global-text.json` edits from appearing immediately.

Page templates/component manifests render from the current Global Text tree.

### Structural data stays outside

Do not move these into `global-text.json` merely because they look like strings:
- canonical slugs;
- page IDs;
- URL-mode state;
- asset paths;
- CSS classes;
- template names;
- schema property names;
- source URLs used as machine targets.

Visible labels for those structures do belong in Global Text.

---

## 16. Footer completion patch (v4.3.1)

Every full site must include a **two-level footer structure** where appropriate:

1. main footer content/navigation/contact/legal area;
2. compact bottom bar at the absolute bottom of the site.

Bottom bar requirements:
- localized copyright line;
- current year via safe runtime interpolation;
- site brand;
- locale-natural `All rights reserved` wording;
- optional compact Privacy / Terms / Cookies links;
- visually quieter than the main footer, but still part of Design DNA.

Do not use the bottom bar to invent a legal company/operator. Brand display name is sufficient unless legal identity is verified or owner-supplied.

Public wording is sourced from `global-text.json` under the footer branch.



---

## 17. Section Composition architecture handoff (v4.4.0)

Site Architecture defines **what each section must accomplish**. `18-SECTION-COMPOSITION-ENGINE.md` defines **how that section is visually composed**.

For every page, Architecture must output semantic section descriptors before layout selection:

```text
page_key
section_key
section_intent
content_shape
priority
dependencies
required_media_role
interaction_need
can_reorder_with_peers
```

Do not encode a fixed visual template into the architecture merely because the content type is familiar.

Examples:
- `features` does not automatically mean 3 equal cards;
- `how it works` does not automatically mean 3 numbered columns;
- `reviews` does not automatically mean 3 quote cards;
- `contact` does not automatically mean left text / right form;
- `FAQ` does not automatically mean one generic accordion style.

The same semantic page manifest may map to different valid composition families across sites.

### Page grammar requirement
Home and each key internal page receive their own `PAGE COMPOSITION FINGERPRINT` from module 18.

Architecture FAIL if all key pages are structurally distinct in copy but visibly reuse the same section skeleton sequence.



---

## 18. Footer semantic architecture + variable geometry (v4.4.1)

Architecture owns **which footer information exists**. Module 18 owns **how it is composed**.

Footer semantic manifest:

```text
brand_zone
optional_descriptor_zone
primary_nav_zone
secondary/domain_nav_zone
contact_zone
legal_zone
official_source_zone
optional_cta_zone
bottom_bar_zone
```

Only include zones supported by the actual site/runtime. `optional_descriptor_zone` is normally absent unless a concise useful phrase materially helps orientation. It must never be populated merely to fill space.

Rules:
- do not hardcode a universal `brand | nav | legal | contact` four-column order;
- do not assume Contact is always rightmost;
- do not assume brand is always leftmost;
- do not assume legal links must be their own vertical column;
- official product/source destination may be integrated into brand, resource or CTA zone when contextually clear;
- the compact copyright bottom bar remains the final footer layer, but its internal alignment/grouping may vary.

Architecture hands semantic zones to `18-SECTION-COMPOSITION-ENGINE.md`, which selects footer family, ordering and proportions.

Footer must remain:
- easy to scan;
- accessible;
- consistent with page navigation;
- correct on mobile;
- stable across all pages of the same site.



## 19. Contact visibility architecture (v4.4.2)

When Contact Profile contains resolved public values, Contact architecture must allocate visible slots for:
- public website email;
- phone display state;
- postal address;
- field-status/disclosure context when synthetic;
- official product/developer support as a separate zone when available.

Default desktop requirement: email + phone + address are visible together in the Contact hero/intro cluster or immediate first content block without forcing the user through unrelated sections.

Do not hide a resolved phone/address only in legal copy, schema, footer state or internal JSON.

Footer contact zone, when present, should expose the resolved public contact set coherently rather than silently dropping phone/address.



## 20. Rich Content Architecture (v4.5.0)

For rich gaming/editorial/app-guide sites, Site Architecture must plan for deeper pages before copywriting begins.

### Home
Normal target:
- about `8–12` meaningful sections;
- at least `5–8` distinct information roles;
- a mix of overview, discovery, explanation, practical guidance, visual/data interpretation, trust/source context and next-step navigation;
- approximately `900–1350` visible words when the subject supports it.

Home must still scan quickly. Long content is distributed across varied section geometries rather than one giant article block.

### Key domain / informational page
Normal target:
- about `5–9` meaningful content blocks;
- approximately `950–1700` words or equivalent structured information density;
- `2–4` meaningful visual/data/diagram moments where useful;
- page-specific related links and next steps;
- its own page grammar, not a shared generic renderer.

### Page Manifest additions

Each managed page now records:

```text
content_depth_tier
estimated_visible_word_envelope
information_roles[]
required_unique_concepts[]
page_grammar_id
live_research_relevance
section_modifier_strategy
```

### Thin-content exception

If authoritative/source information is genuinely limited, the page may be shorter only when the Content Manifest records:
- source limitation;
- what useful interpretive/organizational expansion was still possible;
- why additional copy would become repetitive or speculative.

## 21. Page Grammar Independence v2

Do not render multiple domain pages through one universal visual loop such as:

```text
index + H2 + paragraphs + list + image-right
```

Each key page should vary at least these high-impact dimensions relative to neighboring pages where semantics allow:
- opening/hero topology;
- dominant content flow;
- primary information component;
- media/data integration;
- density rhythm;
- closing/navigation pattern.

A shared design system is expected; a shared page skeleton is not.



## 22. Interaction Architecture (v4.6.0)

Architecture now records interaction intent separately from visual implementation.

Page Manifest additions:

```text
interaction_budget
interaction_roles[]
interaction_priority_sections[]
interaction_fallback_mode
mobile_interaction_strategy
```

Valid semantic roles include:
- browse peers;
- compare states/items;
- reveal optional detail;
- navigate chapters;
- inspect media;
- filter a sufficiently large collection;
- switch device/context/mode;
- show progression/state relationships.

Do not assign interaction to a section whose content is clearer as static editorial composition.


## 20. Header/navigation identity layers (v4.6.1)

Page architecture must separate machine identity from public navigation wording.

For every managed page record:

```text
page_key
page_business_role
localized_page_title
page_display_title
nav_label
nav_label_role
nav_label_family
nav_label_compact_optional
canonical_slug
seo_intent
managed_page_id
```

Rules:
- `page_key` is stable across updates;
- `canonical_slug` is stable unless an explicit URL migration is requested;
- `nav_label` may be a randomized locale-natural synonym selected for the current site;
- `page_display_title`/H1 may be more expressive than the compact nav label;
- SEO title is owned by the SEO profile, not copied blindly from the nav label;
- changing only navigation copy must not create/delete/rename the managed WordPress page.

Site architecture also records:

```text
header_composition_nonce
navigation_copy_nonce
navigation_lexical_profile
domain_lexical_salt
menu_lexical_fingerprint
HEADER_COMPOSITION_MANIFEST
NAVIGATION_COPY_MANIFEST
```

Header structure is selected once per site and shared coherently across pages.

<!-- BUNDLE-MODULE-END: 04-SITE-ARCHITECTURE.md -->

---

<!-- BUNDLE-MODULE-START: 05-WORDPRESS-RUNTIME.md -->

# LEGACY MODULE: 05-WORDPRESS-RUNTIME.md

# WORDPRESS RUNTIME & PROVISIONING

**Version:** 4.5.4  
**Role:** реальне створення та self-heal WordPress structure

---

## 1. Основний принцип

Theme source code не доводить, що сторінки реально існують у WordPress.

Provisioning повинен бути:
- versioned;
- idempotent;
- self-healing;
- verified.

---

## 2. Критична проблема update

Якщо користувач завантажує нову версію вже активної теми:

`after_switch_theme` може не спрацювати.

Тому provisioning **не може** залежати лише від activation.

---

## 3. Mandatory triggers

Provisioning bootstrap перевіряється:

1. на `init` першого frontend request після зміни provisioning version;
2. на `after_switch_theme`;
3. на `admin_init`.

`init` — критичний self-heal path.

---

## 4. Provision lock

Щоб уникнути рекурсії/конкурентних запусків:

- transient або lock;
- короткий TTL;
- release lock після transaction;
- не provision-ити на кожному request після PASS.

---

## 5. Managed page map

Тема зберігає:

`factory_key → WordPress page ID`

Наприклад:

```text
home → 101
guide → 102
privacy → 109
```

Це authoritative runtime map.

---

## 6. Page resolution order

Для кожної managed page:

1. stored page ID;
2. `_factory_key` post meta;
3. canonical slug;
4. create new page.

Якщо знайдено:
- force correct title;
- force correct `post_name`;
- force `publish`;
- update managed meta.

---

## 7. Page creation

Через WordPress API:

- `wp_insert_post`
- `wp_update_post`

Ніколи:
- direct DB insert;
- static assumption, що slug уже є;
- duplicate page on each activation.

---

## 8. Front page

Після managed pages verification:

- `show_on_front = page`
- `page_on_front = managed home ID`

Перевірити runtime state.

---

## 9. Navigation ownership

Default factory mode:
**render navigation directly from Site Manifest + managed page IDs.**

Це найнадійніше для generated themes.

Не залежати від старого WordPress Menu.

Optional:
- створити editable WP Menu як secondary convenience layer;
- але visible default navigation не повинна успадковувати старе menu assignment.

---

## 10. Existing content protection

Заборонено:
- видаляти старі pages/posts;
- змінювати чужі pages;
- імпортувати всі existing pages у menu;
- чистити БД.

Factory управляє лише entity, які:
- мають її managed key/meta;
- або були явно визначені manifest.

---

## 11. Provision verification

Після transaction перевірити:

- expected page count;
- кожен page ID існує;
- `post_status=publish`;
- `post_name` відповідає manifest;
- Home ID правильний;
- navigation target IDs правильні;
- legal pages існують;
- link mode визначений.

Тільки тоді записати provisioning version як complete.

---

## 12. Self-heal

Якщо verify FAIL:
- provisioning version не ставити PASS;
- наступний bootstrap може repair;
- admin diagnostic показує exact missing keys/errors.

---

## 13. Rewrite flush

Не flush на кожному request.

Після structural change:
- set `rewrite_flush_pending=1`;
- виконати один hard/required flush на appropriate hook;
- delete pending flag.

---

## 14. Theme update acceptance

Для in-place update обов’язково test:

- стара активна тема;
- завантажити нову версію;
- відкрити frontend без deactivation;
- сторінки/links повинні self-heal автоматично.

Це regression gate.


---

## 15. Verified permalink transaction

Preferred target:

```text
/%postname%/
```

Provisioning must verify actual reachability, not assume rewrite capability.

### Resolution sequence

1. keep navigation in safe query mode;
2. try `/%postname%/`;
3. flush once;
4. real runtime probe on a managed page;
5. if clean works → persist `CLEAN_URL_PASS`;
6. if clean fails → try `/index.php/%postname%/`;
7. real runtime probe;
8. if PATHINFO works → persist `DEGRADED_URL_PASS`;
9. if PATHINFO fails → use plain permalink/query mode;
10. verify `?page_id=ID`;
11. if query works → persist `QUERY_URL_PASS`;
12. if all fail → `URL_FAIL_VERIFIED`.

Server capability helpers may inform diagnostics but never replace this transaction.

---

## 16. Permalink state model

```text
CLEAN_URL_PASS
DEGRADED_URL_PASS
QUERY_URL_PASS
URL_FAIL_VERIFIED
```

Release is allowed only if one of the first three states has been runtime-verified. Preferred quality remains `CLEAN_URL_PASS`.

---

## 17. Rendered attribute ownership

WordPress runtime може додавати markup після static build.

Тому після install crawler перевіряє:
- усі rendered `<img>`;
- усі rendered `<a>`.

Factory-controlled missing `alt`, image `title` або link `title` автоматично повертаються в FIX LOOP до template/helper level.

Не виправляти один HTML occurrence вручну, якщо root cause у shared helper/template.

---

## 18. Provisioning completion is click-verified (v4.4 patch)

Provisioning вважається завершеним лише після того, як theme/runtime довели:
- всі managed pages існують;
- всі managed page IDs збережені в authoritative map;
- всі navigation targets резолвляться в working pages;
- `front page`, contact, legal pages і domain pages відкриваються у selected verified URL mode;
- жоден primary internal link не повертає `404`.

Якщо хоч одна умова не виконана:
`PROVISION_INCOMPLETE → SELF_HEAL REQUIRED`.

## 19. Navigation self-heal

Theme не повинна покладатися на stale hardcoded href.

Навігація, footer links, card links, CTA links і policy links повинні будуватися через managed page map + актуальний permalink.

Після update existing active theme система повинна:
1. re-read managed page map;
2. re-resolve every required page;
3. rebuild runtime navigation/link map;
4. re-run click probe.

## 20. Console-clean theme rule

Theme-owned JS/CSS runtime повинен бути browser-clean.

Factory QA розділяє:
- **theme-owned errors** → blocking FAIL;
- **extension-injected noise** → log separately.

Release PASS вимагає `0` theme-owned console errors, uncaught exceptions, missing asset fatals або DOM-init failures.


---

## 21. Central rendered-markup helpers

Theme should centralize factory-owned markup through helpers/components so audit fixes apply globally:

- image helper always receives `src`, `alt`, `title`, dimensions/ratio where relevant;
- link helper always receives `href`, visible label and localized `title`;
- nav/card/CTA/footer templates reuse these helpers.

Do not fix missing attributes occurrence-by-occurrence when a shared helper can enforce them.


---

## 22. Real URL probe transaction

After managed pages are created and Home is assigned:

1. temporarily keep factory navigation in safe query mode;
2. set `/%postname%/`;
3. flush once;
4. real-request one managed page, e.g. `/guia/`;
5. require:
   - HTTP 200;
   - response reached WordPress/theme;
   - expected factory page marker/H1;
6. if fail, set `/index.php/%postname%/`;
7. flush once;
8. real-request `/index.php/guia/`;
9. if fail, set plain permalink mode;
10. verify `/?page_id=ID`;
11. persist selected mode.

State model:

```text
CLEAN_URL_PASS
DEGRADED_URL_PASS
QUERY_URL_PASS
URL_FAIL_VERIFIED
```

No capability heuristic may skip this transaction.

## 23. Link generation after probe

Shared link helper must resolve by selected mode:

```text
clean    → /slug/
pathinfo → /index.php/slug/
query    → /?page_id=ID
```

Do not call `get_permalink()` first and return it unconditionally: WordPress can generate a clean-looking URL that Apache serves as raw 404.

## 24. Stable update root

The install-ready ZIP root folder is a stable site identifier.

For an existing site update:

```text
old ZIP root == new ZIP root
```

Versioned folder names are forbidden for updates.

Example:

```text
GOOD
norvard-catch-fish-pt-v2/  (2.0.0)
norvard-catch-fish-pt-v2/  (2.0.1)

BAD
norvard-catch-fish-pt-v2/
norvard-catch-fish-pt-v2.0.1/
```

Theme update QA must confirm WordPress performs an **update of the active theme**, not installation of a sibling theme.

## 25. Admin notice evidence rule

Do not show a red rewrite/server notice from:
- `got_url_rewrite()`;
- `.htaccess` existence;
- `.htaccess` writability;
- server-family guess.

Red error requires verified runtime failure after trying clean, PATHINFO and query modes.


---

## 26. Global Text persistent runtime (v4.5.3)

### Persistent path

On first successful provisioning create, if absent:

```text
/wp-content/uploads/site-factory/{theme_package_slug}/global-text.json
```

from the theme's generated seed.

The persistent file is authoritative after creation.

### Theme update behavior

On update:
1. read new seed schema/default tree;
2. read persistent user file;
3. recursively add keys that are new/missing;
4. preserve every existing user value;
5. never overwrite an existing value solely because the theme seed changed;
6. save only after valid merge;
7. record schema/content hash.

### Loader contract

Central loader must:
- load once per PHP request;
- use UTF-8 JSON;
- reject malformed JSON cleanly;
- support dot-path lookup;
- support scalar and array values;
- support safe placeholder interpolation;
- expose context-specific escaping helpers.

Reference API pattern:

```text
global_text('pages.home.hero.title')
global_text_array('pages.faq.items')
global_text_attr('images.home_hero.title')
global_text_link_title('links.header.guide')
```

Exact PHP names may differ; behavior may not.

### Last-known-good safety

Store last-known-good parsed data + hash in WordPress option/state.

If disk JSON becomes invalid:
- frontend uses last-known-good snapshot;
- admin diagnostic names the file and JSON error;
- no fatal/white screen;
- runtime state becomes `GLOBAL_TEXT_INVALID`.

### Change detection

At minimum compare file mtime + content hash.

When a valid change is detected:
- refresh in-request data;
- update last-known-good;
- update text hash/version;
- flush relevant WordPress object/transient caches;
- fire a factory text-change hook for cache adapters.

### Full-page cache limitation

If a reverse proxy/CDN/host page cache bypasses PHP, text can remain cached until that layer is purged. The factory must:
- expose a purge hook/adapter where possible;
- document the exact persistent path;
- verify FastPanel edit propagation in runtime QA.

### No one-time database copy

Do not treat `global-text.json → wp_post.post_content` as the production runtime source.

WordPress pages can keep managed metadata/admin titles, but public body/head/component text resolves from Global Text so a file edit does not require reprovisioning.



## 27. Safe factory-default migration (v4.5.4)

Persistent Global Text still preserves user edits across theme updates.

When a factory bugfix must change an old generated default, use an explicit value-aware migration:
1. identify the exact previous factory default;
2. update the persistent value **only if it still exactly equals that old factory default**;
3. never overwrite a value that differs, because it may be a user edit;
4. then perform the normal missing-key merge;
5. update last-known-good only after valid JSON/write success.

Use this for corrected default metadata/contact wording where simply changing the new seed would otherwise leave an already-installed site on the defective old default.



## 26. Interactive component runtime contract (v4.6.0)

Factory-owned interactions should prefer resilient native/CSS/vanilla-JS implementations. Heavy third-party slider/animation libraries require a documented reason.

Runtime rules:
- HTML contains essential content before JS runs;
- JS enhances states rather than generating the only copy/source of truth;
- event listeners are scoped and idempotent;
- duplicate initialization after cache/navigation/update is prevented;
- controls use buttons rather than clickable generic divs;
- URL/hash state is used only when it materially improves deep-linking;
- tabs/accordion/carousel state must survive long localized labels;
- slider/rail resize handling must not create horizontal page overflow;
- components remain usable if `IntersectionObserver` or optional animation code is unavailable.

All user-visible interaction labels/instructions belong to Global Text.


## 34. Header/navigation persistence runtime (v4.5.5)

On first provisioning:
- persist `header_composition_nonce` and selected header family in site-owned factory state;
- persist `navigation_copy_nonce`, `navigation_lexical_profile`, `domain_lexical_salt`, `locale_lexical_lane`, `menu_lexical_fingerprint`, resolved locale and role→label selection metadata in site-owned factory state;
- seed the visible selected navigation strings into persistent `global-text.json`.

On ordinary same-site update:

```text
existing header selection wins
existing navigation nonce wins
existing user-edited Global Text navigation labels win
```

Do not reroll because a theme ZIP version changed.

Explicit regeneration modes may be implemented as controlled maintenance actions:

```text
REGENERATE_HEADER
REGENERATE_NAVIGATION_COPY
REGENERATE_HEADER_AND_NAVIGATION
```

They must not run silently.

Desktop and mobile navigation should normally resolve the same semantic `nav_label`. A shorter `nav_label_compact` may be used only when:
- it is semantically equivalent;
- the long label genuinely does not fit the mobile pattern;
- the compact variant is recorded in the manifest/Global Text;
- accessible link context remains clear.



### 34.1. Universal locale persistence (v4.5.6)

Persist the resolved navigation language identity separately from visible labels:

```text
navigation_geo
navigation_locale
navigation_regional_variant
navigation_lexicon_source_mode
locale_lexical_lane
```

A normal theme update must not silently change locale, lexical lane or selected role labels. If the site's locale is intentionally changed, run a controlled navigation-copy regeneration and revalidate header fit, URLs, accessibility and Global Text.

For a batch-generation runtime, the batch coordinator may persist a temporary `batch_lexical_assignment` so role labels can be distributed without replacement before individual themes are finalized. This batch artifact is build metadata, not public copy.

<!-- BUNDLE-MODULE-END: 05-WORDPRESS-RUNTIME.md -->

---

<!-- BUNDLE-MODULE-START: 06-LINKS-PERMALINKS.md -->

# LEGACY MODULE: 06-LINKS-PERMALINKS.md

# LINKS & PERMALINKS

**Version:** 4.5.2  
**Role:** canonical readable URL і link integrity

---

## 1. Вимога

Користувач повинен отримати **working internal navigation**.

Preferred:

`/como-jogar/`

Compatibility:

`/index.php/como-jogar/`

Last-resort verified fallback:

`?page_id=74`

Broken pretty URL is never acceptable.

---

## 2. Link source

After URL mode is selected, generate all internal links through the central verified-mode resolver.

Do not blindly return `get_permalink(page_id)` before runtime URL mode is known.

---

## 3. Preferred mode

Primary:

`/%postname%/`

Use only after real runtime probe confirms the page resolves.

---

## 4. PATHINFO compatibility mode

`/index.php/%postname%/` is accepted when root-clean rewrites fail but PATHINFO is runtime-verified.

State:

```text
DEGRADED_URL_PASS
```

It is not the preferred aesthetic state, but it is valid operationally.

---

## 5. Query compatibility mode

If clean and PATHINFO fail, verify:

```text
/?page_id=ID
```

If it resolves to the correct managed page:

```text
QUERY_URL_PASS
```

This is the least desirable mode but remains valid as a working fallback.

---

## 6. Runtime probe

For the candidate modes capture:

```text
requested URL
HTTP status
redirect chain
final browser URL
expected page marker/H1
canonical URL
```

Select the first verified working mode:

```text
clean → PATHINFO → query
```

Do not stop after a raw Apache/Nginx 404 on `/slug/`.

---

## 7. Forbidden URL states

Final release does not allow:
- raw server 404;
- stale slug;
- wrong locale slug;
- old-theme URL;
- redirect loop;
- mixed URL modes after selection;
- query IDs exposed when a verified cleaner mode is available.

---

## 8. Slug rules

Slugs:
- semantic;
- human-readable;
- concise;
- localized;
- stable;
- без internal IDs.

Examples PT:
- `/como-jogar/`
- `/controlos/`
- `/guia-do-safari/`
- `/privacidade/`
- `/termos/`
- `/cookies/`

---

## 9. Navigation labels

Link label повинен бути коротким і зрозумілим.

Header:
- не більше необхідних primary destinations;
- legal не в main nav без причини;
- domain labels локалізовані.

Footer:
- About
- Contact
- Privacy
- Terms
- Cookies
- contextual links.

---

## 10. External links

Для external source:
- correct destination;
- `rel="noopener noreferrer"` when opening separate browsing context;
- не маскувати external link як internal;
- labels типу `Google Play ↗`, якщо це зрозуміло.

---

## 11. Runtime crawl

Crawler/QA проходить:

- header;
- footer;
- cards;
- CTA;
- related content;
- legal TOC anchors;
- external source links.

Для internal:
- success;
- correct final URL;
- expected context;
- no redirect loop;
- no 404.

---

## 12. Link RELEASE gate

PASS лише якщо:
- усі required pages існують;
- selected URL mode має runtime-verified state (`CLEAN_URL_PASS`, `DEGRADED_URL_PASS` або `QUERY_URL_PASS`);
- усі internal links ведуть на current manifest pages;
- усі internal links використовують один selected verified mode;
- final URLs реально відкривають correct page context;
- old theme links відсутні;
- raw server 404 / redirect loops / stale destinations = 0;
- query-ID URLs використовуються лише коли cleaner verified mode недоступний.


---

## 13. Link TITLE audit compatibility

Для factory-owned `<a>` у rendered DOM:

```text
missing title = 0
```

Title:
- localized;
- concise;
- описує destination/action;
- не spam;
- не замінює descriptive anchor text.

Examples:

```html
<a href="/poradnik/" title="Otwórz poradnik Idle Fish 2">Poradnik</a>
<a href="#main" title="Przejdź do głównej treści">Przejdź do treści</a>
<a href="https://play.google.com/..." title="Otwórz Idle Fish 2 w Google Play">Google Play ↗</a>
```

Для repeated link destination допускається той самий semantic title, якщо context однаковий.

Crawler reports:
```text
links_total
links_unique
links_missing_title
internal_links_missing_title
external_links_missing_title
```

`links_missing_title > 0` для factory-owned markup → FIX LOOP.

---

## 14. Zero-broken-link doctrine (v4.4 patch)

Factory release заборонений, якщо будь-який із таких link classes broken:
- header nav;
- hero CTA;
- section CTA;
- footer nav;
- legal links;
- contact links;
- related-page cards.

Broken = `404`, `Not Found`, wrong page context, empty href, stale slug або URL that does not match the selected verified mode.

## 15. Runtime click-probe

Фабрика повинна не просто проаналізувати href textually, а виконати runtime probe для всіх critical internal links.

Minimum probe set:
- all header links;
- all footer links;
- one CTA per major section;
- legal links;
- contact link.

Кожний link повинен мати:
- final URL у selected verified mode;
- HTTP 200 або expected 301 → 200;
- correct destination H1/title context.

## 16. Link title enforcement

Кожен factory-owned rendered `<a>` отримує localized `title` attribute через central helper.

Rule:
- `title` описує destination / action;
- не дублює blindly slug;
- не stuffed with keywords.


---

## 17. Verified-mode URL resolver

Permalink preference and permalink functionality are separate concerns.

Factory selection:

```text
VERIFIED /slug/
→ VERIFIED /index.php/slug/
→ VERIFIED ?page_id=ID
```

A pretty URL that returns a raw server 404 is always worse than a working compatibility URL.

Before probe completion, navigation must not emit an unverified route.

## 18. Runtime marker requirement

The probe target must contain a unique factory marker or equivalent expected page context so that an HTTP 200 homepage/error-soft-404 is not mistaken for the requested managed page.

Example:

```html
<!-- factory-page:guide -->
```

Probe PASS:

```text
HTTP 200
+ marker = guide
```

## 19. Query compatibility mode

`?page_id=ID` is allowed as the final safe fallback when both clean and PATHINFO routes fail on the target host.

Requirements:
- page exists;
- HTTP 200;
- correct page context;
- no redirect loop;
- all internal links use the same selected runtime mode;
- canonical follows the reachable URL.

It is a compatibility state, not the preferred aesthetic state.


## 20. Navigation label / URL decoupling (v4.5.3)

Visible menu copy is not a permalink source after the page has been provisioned.

Internal navigation resolves as:

```text
stable page_key
→ managed page ID
→ selected verified URL mode
→ canonical_slug / query ID
```

and renders text separately from Global Text:

```text
navigation.{page_key}
```

Therefore a user/factory change such as:

```text
About → Our Studio
```

must keep the same destination page and canonical URL unless an explicit URL migration is requested.

Link `title` / accessible context may be more descriptive than the visible nav label but must describe the same destination.

<!-- BUNDLE-MODULE-END: 06-LINKS-PERMALINKS.md -->

---



## 35. Footer public-copy runtime contract (v4.5.7)

The renderer must not assume a footer paragraph exists. Footer templates must render cleanly when only brand/navigation/legal/contact/store/bottom-bar data are present.

In `OFFICIAL_GAME_STUDIO` mode:
```text
footer_independent_editorial_copy = forbidden
footer_methodology_paragraph = forbidden_by_default
footer_repeated_about_copy = forbidden
footer_store_link = allowed
footer_navigation = allowed
footer_contact_support = allowed
footer_legal = allowed
footer_bottom_bar = required
```

If a legacy `global-text.json` contains an old factory-default footer disclaimer/descriptor that conflicts with the active business model, the migration/self-heal layer may retire that **factory-owned default**. Preserve genuine manual user edits and do not delete owner-authored copy silently.



## 36. Per-page hero renderer contract (v4.5.8)

A theme may centralize hero semantics in a helper, but it must not hardcode one universal hero DOM/grid silhouette for every managed page.

Each page receives a `HERO_COMPOSITION_MANIFEST` entry:

```text
page_key
hero_family
hero_topology_cluster
hero_text_anchor
hero_text_alignment
hero_media_topology
hero_title_scale_tier
hero_eyebrow_position
hero_cta_position
hero_mobile_transform
hero_signature
```

Runtime dispatch pattern:

```text
page_key + HERO_COMPOSITION_MANIFEST
→ family-specific renderer / modifier set
→ Global Text values
→ responsive hero output
```

A single `render_hero(title, body, image)` function is acceptable only when it dispatches to materially different family implementations/modifier stacks. A helper that always emits `text-left + media-right` is a factory defect.

Same-site update preserves the selected hero manifest unless explicit redesign/regeneration is requested.


## 37. Footer contact + utility-phrase runtime contract (v4.5.9)

For the standard full-site Contact Profile, footer contact rendering consumes the same authoritative public values as Contact:

```text
contact.public_email
contact.phone_display
contact.address_lines[]
```

When a value is resolved for public display, footer renderer must not silently drop it because a compact footer template lacks a slot. Change footer family/geometry instead.

Bottom bar may render:

```text
footer.bottom_bar.copyright
footer.bottom_bar.rights_reserved
footer.bottom_bar.utility_phrase   optional but preferred when the layout has a second text slot
```

`footer.bottom_bar.utility_phrase` is short locale-natural microcopy, not a navigation placeholder.

Do not render an unlabeled arrow as filler. If a back-to-top action is deliberately enabled, it must be a real focusable control/link with visible or accessible localized label and working target; otherwise omit it.


## 38. Favicon / site-icon runtime contract (v4.5.10)

Every production theme must have one coherent icon owner.

Priority:

```text
OWNER / WORDPRESS SITE ICON when intentionally configured
→ THEME BRAND-UTILITY ICON FALLBACK
```

If WordPress `has_site_icon()` is true, allow WordPress to emit the site icon and avoid conflicting duplicate theme icon tags.

If no Site Icon exists, the theme must emit local fallback links using packaged brand-utility assets, normally covering:
- browser favicon SVG and/or PNG;
- small PNG fallback;
- `apple-touch-icon` when packaged;
- a larger square site icon when packaged.

Requirements:
- local URL, no temporary generator URL;
- valid MIME/decode;
- current site brand, never stale previous-project artwork;
- versioned/cache-busted URL when theme asset changes;
- no duplicate conflicting icon tags from multiple theme helpers.

A missing WordPress Site Icon is not permission to ship without a favicon; the theme fallback is mandatory.


## 39. Structural-memory build finalization contract (v4.5.11)

Persistent layout history is a build/release artifact outside the public WordPress theme ZIP.

Canonical repository:

```text
PingVinni/Landing
```

Canonical outputs after a full new-site build:

```text
site-factory-history/sites/{normalized-domain}.json
site-factory-history/index.json
```

### Finalization order

```text
THEME BUILD
→ STATIC QA
→ RUNTIME QA when available
→ FINAL COMPOSITION MANIFEST LOCK
→ GENERATE COMPACT STRUCTURAL FINGERPRINT
→ CREATE / UPDATE PER-SITE HISTORY FILE
→ UPDATE GLOBAL HISTORY INDEX
→ RE-FETCH BOTH FILES
→ VERIFY CURRENT SITE FINGERPRINT
→ STRUCTURAL_MEMORY_WRITE_PASS
```

The repository JSON is **not** packaged inside the install-ready WordPress ZIP and must not be publicly rendered by the theme.

### Domain identity

Normalize the public domain deterministically for the filename, for example:

```text
elvantam.org → elvantam-org.json
www.example.co.uk → example-co-uk.json
```

Use one canonical file per normalized domain.

A same-domain theme update uses the same file. A material structural redesign updates its fingerprint and appends a compact revision summary.

### Runtime/build separation

GitHub structural-memory persistence is not a substitute for WordPress Runtime PASS. Likewise, a valid WordPress runtime does not prove that cross-session structural history was persisted.

Track separately:

```text
runtime_validation_state
structural_memory_read_state
structural_memory_write_state
```

Never expose repository paths, internal structural IDs, fingerprints or history diagnostics in public HTML, metadata, Global Text, legal copy or browser-visible comments.



## 40. OFFICIAL-STUDIO CONTENT ARCHITECTURE OVERRIDE (v4.6.0)

This section is authoritative over older generic `gaming guide/editorial` examples whenever `business_model_mode = OFFICIAL_GAME_STUDIO` and the relationship truth gate passes.

### Managed page-role preference

A normal rich site should choose a coherent subset from:

```text
HOME
GAME_PRODUCT
DEVELOPMENT
MECHANICS_DESIGN
LEVEL_PROGRESSION
CONTROLS_FEEL
ART_DIRECTION
TESTING_BALANCING
ABOUT_STUDIO
SUPPORT_FAQ
CONTACT
LEGAL
```

Do not provision empty pages just to satisfy the list. Prefer deep sections when the source is too limited for a standalone page.

### Home business arc

Home must visibly answer:
1. who we are / what game this is;
2. what we built and why a player should care;
3. how one or more core systems work;
4. how the studio approached building/refining them at a truthful level;
5. how to continue into product/development pages;
6. where to play/download/get support.

### Internal-page narrative isolation

Each key page gets its own business job and unique information gain. Examples:
- `Game` = product proposition + core loop + modes/features + platform/store;
- `Development` = overall build/refinement story;
- `Mechanics` = rules/systems + implementation consequences;
- `Levels` = pacing/progression/challenge structure;
- `Controls` = input/feedback/feel;
- `Art` = readability/mood/visual system;
- `About` = studio/team/product philosophy;
- `Support` = first-party help + factual platform/store context.

Do not rewrite the same product paragraph under different H1s.

### Proof override

In `OFFICIAL_GAME_STUDIO`, the legacy mandatory synthetic-review requirement does not apply. Use real sourced reviews/press only when available; otherwise use product/development proof.


## 41. SEMANTIC SECTION-ASSET + ICON RUNTIME CONTRACT (v4.6.1)

Theme/runtime rendering must consume a section visual manifest rather than hardcoding generic image/icon slots.

### Per-section visual binding

Each meaningful section may bind:

```text
section_key
visual_asset_id
visual_job
visual_semantic_subject
visual_variant_desktop
visual_variant_mobile
micro_icon_ids[]
micro_visual_mode
```

A renderer must never substitute an unrelated generic asset merely because the preferred file is missing. Missing required major media returns the section/build to `FIX_REQUIRED` or an explicitly designed no-major-image fallback.

### Central image helper

Factory image helpers should resolve:
- local asset path;
- responsive rendition;
- width/height or aspect-ratio strategy;
- localized ALT/TITLE Global Text keys;
- loading priority;
- crop/focal treatment;
- section ownership.

### Central icon helper

Use a local, site-owned icon registry/helper for factory micro-icons. Preferred final forms are optimized local SVG/SVG sprite/symbol components or equivalent safe local markup.

The helper must support:
- icon ID → asset/symbol resolution;
- decorative vs semantic state;
- localized accessible name for interactive icon-only controls;
- consistent classes/tokens for size/stroke/fill;
- currentColor or controlled semantic color roles where appropriate;
- no external icon-font dependency solely for factory icons.

### Asset failure rule

Production must not show:
- broken `<img>`;
- missing SVG references;
- fallback question-mark/unknown glyphs;
- stale icons from another project;
- remote temporary generation URLs.

### Micro-UI public-copy rule

Visible badge/chip/label text remains Global Text owned. The icon graphic itself is structural/asset data; its human-readable label/title/ARIA text is localized through Global Text/accessibility keys.




## 42. OFFICIAL-STUDIO TOP/MIDDLE/BOTTOM PAGE CONTRACT (v4.6.2)

For the current studio-first product branch, every managed key non-legal page records:

```text
business_narrative_zone_plan
opening_business_job
middle_work_jobs[]
lower_product_jobs[]
team_process_visual_slots[]
content_depth_multiplier = 1.50
```

### Required zone behavior

```text
OPENING
→ company/team responsibility + page-specific work problem

EARLY CONTENT
→ task/process/collaboration/design decision

MIDDLE
→ iteration/review/QA/production evidence at a truthful level

LOWER CONTENT
→ game/system/player-facing result

CLOSE
→ related studio story + play/download/support CTA
```

Home and internal pages may use different layout grammars, but they may not bypass this semantic contract.

### Internal depth override

For `OFFICIAL_GAME_STUDIO`, the old generic `4–7 meaningful blocks` envelope is replaced for key domain pages by:

```text
7–11 meaningful blocks
2–4 major team/work/process media moments
1–3 product/game media moments
2–4 useful interactive or progressive-disclosure moments when semantically useful
```

Home normally uses `10–15` meaningful sections.

### Page-type examples

`GAME / PRODUCT`
- who owns the product experience;
- current product/design priorities;
- how the team evaluates clarity/engagement;
- review/checklist/process;
- then game loop/features/store.

`MECHANICS`
- systems-design responsibility;
- mechanic design problem;
- tuning/review workflow;
- implementation principle;
- then detailed mechanic explanation.

`LEVELS`
- level-design responsibility;
- level task / goal;
- progression planning;
- QA/balance review;
- then examples of level/player rhythm.

`ABOUT / STUDIO`
- company identity;
- team working model;
- disciplines;
- how decisions move through the studio;
- quality principles;
- then product relationship.

`CONTACT / SUPPORT`
- who handles what;
- support workflow;
- what information helps the team respond;
- escalation/ownership model at a truthful level;
- then channels and legal links.

### Interaction requirement

Rich studio pages should prefer interaction patterns that reveal real working structure:
- process tabs;
- task/state switchers;
- chapter navigation;
- review accordion;
- decision matrix;
- progression rail;
- media inspection;
- FAQ groups.

Do not add interaction only for decoration.

### Existing-site content migration

When a previous factory seed used an older game-first narrative, a versioned migration may update **factory-owned unedited defaults** into the new studio-first branch.

Preserve manual user edits.

Record:

```text
content_model_version
migrated_factory_defaults[]
preserved_manual_values[]
```



## 43. ADAPTIVE SECTION RENDERER + COMPOSITION MANIFEST (v4.6.3)

Runtime/rendering must not map many semantic section types to one visual skeleton.

### Per-section render manifest

Each section records:

```text
section_key
semantic_role
layout_family
topology_cluster
text_flow_mode
media_relationship
media_required
media_asset_id
no_media_fallback_family
interaction_family
background_family
density_mode
mobile_transform
```

### Renderer requirement

A renderer should dispatch to materially different layout renderers/components.

Forbidden implementation pattern:

```text
render_section(type)
→ same DOM grid
→ swap classes/text
```

when the resulting pages remain visually identical.

### Runtime no-media behavior

Before emitting DOM:

```text
if media_required && asset_missing
  → FIX_REQUIRED

if media_optional && asset_missing
  → switch_to(no_media_fallback_family)
  → remove media column
  → recompute text width
  → recompute spacing
```

Do not emit empty `<figure>`, placeholder shell, blank grid track or fixed-height media wrapper.

### Content-aware density

Renderer may use section copy size to choose:
- paragraph width;
- number of text columns;
- internal subhead placement;
- image-wrap eligibility;
- supporting diagram/card density.

Long copy should not inherit the same narrow half-column width as a short teaser.

### Page-level composition manifest

Before rendering a key page, record:

```text
page_key
section_family_sequence[]
topology_sequence[]
media_relationship_sequence[]
text_flow_sequence[]
interaction_sequence[]
page_visual_word_ratio
page_dead_space_risk[]
page_repetition_risk[]
```

Any unresolved `page_dead_space_risk` or `page_repetition_risk` blocks final release.
---

## 44. RUNTIME WIDTH-OCCUPANCY + COMPACT COPY CONTRACT (v4.6.4)

The runtime renderer must enforce the new full-width and compact-copy invariants rather than relying on static design intent.

### Per-section runtime fields

For every major section, extend the render/composition record with:

```text
copy_density_profile = COMPACT_070
available_canvas_width
meaningful_content_span
canvas_coverage_ratio
largest_unassigned_blank_region_ratio
empty_track_count
media_slot_state
reflow_applied
```

### Render behavior

If an optional side is empty:

```text
empty_track_count > 0
→ collapse/remove track before HTML/CSS finalization
→ recompute inner width
→ recompute text placement
→ recompute section height
```

Do not leave an empty `<figure>`, empty grid child, placeholder wrapper or reserved `min-height` as a geometry holder.

### Copy envelope handoff

Runtime content manifests should expect the compact planning envelopes:

```text
Home ~900–1350
Key domain/product/development ~950–1700
About/Studio ~750–1250
FAQ ~750–1350
Contact/Support ~525–950
```

Longer output is allowed when information genuinely requires it, but it must be explicit in the content-depth manifest rather than caused by repeated factory prose.

### Runtime blocker

A major desktop section that renders as a narrow side island with a functionally empty opposite field must set `page_dead_space_risk` and block release until recomposed.
