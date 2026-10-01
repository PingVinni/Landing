# 01 CORE GOVERNANCE

**Bundle format:** Source Bundle v1.5  
**Policy baseline:** Site Factory v4.9.15  
**Bundling rule:** logical module boundaries and aliases are preserved inside bundles. Source Bundle v1.5 applies the Site Factory v4.9.14 interaction, micro-motion, hover/focus and semantic interactive-section expansion while preserving v1.4 rich-content, live UI/UX research, morphological section variation, v1.3 adult-premium visuals and the 7-file Project Source architecture.

## Module aliases in this bundle

- `01-MASTER-SKILL-v4.5.md` → this file, section `LEGACY MODULE: 01-MASTER-SKILL-v4.5.md`
- `12-FACTORY-LEARNING.md` → this file, section `LEGACY MODULE: 12-FACTORY-LEARNING.md`
- `19-PRODUCTION-HYGIENE-IDENTITY.md` → this file, section `LOGICAL MODULE: 19-PRODUCTION-HYGIENE-IDENTITY.md`

## Cross-reference rule

References inside logical module text to filenames such as `15-SECTION-IMAGE-ENGINE.md` remain valid **logical module IDs**. Resolve them against the module aliases declared across the loaded Source Bundles. `SOURCE-BUNDLE-MAP.md` is maintenance documentation only and is **not required** as a Project Source.

---

<!-- BUNDLE-MODULE-START: 01-MASTER-SKILL-v4.5.md -->

# LEGACY MODULE: 01-MASTER-SKILL-v4.5.md

# SITE FACTORY v4 — MASTER SKILL

**Version:** 4.9.14  
**Role:** головний алгоритм фабрики  
**Primary output rule:** `1 сайт = 1 install-ready WordPress ZIP`

---

## 1. Місія

Site Factory створює повноцінні WordPress-сайти за коротким замовленням на кшталт:

`1 PT (Gaming) + source URL`

Фабрика повинна самостійно:

1. дослідити джерело замовлення;
2. визначити GEO, мову, нішу та тип сайту;
3. побудувати Site Manifest;
4. вибрати дизайн-напрям із Golden Design DNA;
5. спроєктувати повну архітектуру сторінок;
6. сформувати контент, SEO, legal, Advanced Visual Direction та section image plan;
7. створити WordPress theme;
8. provision-ити сторінки, front page та навігацію;
9. перевірити реальні URL і runtime;
10. пройти visual QA проти Golden Sites;
11. виправити системні дефекти;
12. віддати один готовий ZIP для WordPress.

---


## 1.1. Обов'язковий input contract

Фабрика **не починає BUILD**, поки не визначені мінімум:

```text
DOMAIN
GEO
TOPIC / NICHE
```

User obligation може бути коротшим:

```text
SOURCE URL
GEO / TYPE
DOMAIN
```

`TOPIC / NICHE` фабрика повинна автоматично derive з SOURCE URL, якщо джерело однозначно визначає тему/нішy. Не вимагати від користувача повторювати те, що вже видно з source.

Приклад:

```text
domain: bremtous.org
geo: Portugal
topic: gaming / Chicken Safari Jump guide
```

`DOMAIN` є обов'язковим джерелом для:
- mandatory factory-generated public email host when no explicit `OWNER_SUPPLIED` / `VERIFIED` email is supplied;
- canonical URLs;
- Open Graph URLs;
- sitemap;
- robots.txt;
- publisher/site identity;
- internal link QA.

Якщо `DOMAIN` відсутній:
`INPUT_REQUIRED → STOP BEFORE BUILD`.

Фабрика може самостійно згенерувати brand name, locale, editorial naming, contact mailbox prefixes та visual direction із `DOMAIN + GEO + TOPIC`.

---

## 2. Пріоритет джерел

У разі конфлікту використовуй такий порядок:

1. **01-MASTER-SKILL.md**
2. відповідний спеціалізований MD-модуль v4
3. **02-GOLDEN-DESIGN-DNA.md**
4. 7 Golden WordPress ZIPs як reference corpus
5. джерело конкретного замовлення
6. загальні модельні знання

Golden Sites задають **рівень якості та принципи дизайну**, але не є шаблонами для копіювання.

---

## 3. Незмінний pipeline

`ORDER → RESEARCH → MANIFEST → GEO TYPOGRAPHY RESEARCH → GOLDEN FAMILY → ARCHITECTURE → CONTENT → SECTION COMPOSITION PLAN → INTERACTION / MICRO-MOTION PLAN → LEGAL → GLOBAL TEXT MAP → VISUAL INTELLIGENCE → SECTION IMAGE PLAN → ASSETS → BUILD → PROVISION → RUNTIME QA → VISUAL QA → FIX LOOP → RELEASE`

Жоден етап після BUILD не можна пропускати лише тому, що PHP/CSS синтаксично валідні.

---


## 3.1. HTML audit compatibility gate

Generated site повинен проходити не тільки semantic SEO, але й browser/extension audits.

Для factory-owned markup у фінальному rendered DOM очікуємо:

```text
meaningful <img> missing ALT = 0
meaningful <img> missing TITLE = 0
factory-owned <a> missing TITLE = 0
broken internal links = 0
```

### Images
- meaningful `<img>` має localized `alt`;
- meaningful `<img>` має concise localized `title` для audit compatibility;
- decorative visual не рендерити як `<img>` із пустими audit fields, якщо його можна реалізувати CSS background / pseudo-element;
- якщо `<img>` справді decorative, semantic accessibility може використовувати `alt=""`, але audit mode повинен класифікувати його окремо і не залишати випадковий missing attribute.

### Links
Factory-owned `<a>` має:
- descriptive visible label;
- valid `href`;
- localized `title`, що пояснює destination/action;
- external state/rel, якщо потрібно.

`title` не замінює visible anchor text і не використовується для keyword stuffing.

### Audit ownership
Crawler повинен перевіряти **rendered DOM**, включно з:
- header;
- footer;
- page content;
- cards;
- CTA;
- legal TOC;
- WordPress-injected factory-controlled markup.

Якщо missing attribute походить із third-party plugin/runtime injection:
- визначити source;
- виправити adapter/template, якщо factory контролює його;
- інакше показати exact external owner як release warning/blocker залежно від severity.

---

## 4. Статуси

- `PLANNED`
- `BUILT`
- `STATIC_PASS`
- `PROVISIONED`
- `RUNTIME_PASS`
- `VISUAL_PASS`
- `RELEASE`

При будь-якій blocking-помилці:

`FIX_REQUIRED`

`STATIC_PASS ≠ RELEASE`.

---

## 5. Contact & identity profile

Перед побудовою сайту фабрика формує `CONTACT PROFILE`.

Required resolved inputs:
- `domain` — надає користувач;
- `geo` — надає користувач;
- `topic / niche` — derive from source URL when possible; ask user only if source does not establish it.

Contact fields:
- brand / operator display name;
- public email;
- public phone display;
- normalized phone;
- public postal address;
- locale;
- domain;
- field status;
- source/mode.

### Contact status model

Допустимі стани:

- `VERIFIED`
- `OWNER_SUPPLIED`
- `SYNTHETIC_GEO_CONTACT`
- `REQUIRES_OWNER_DATA`

`SYNTHETIC_GEO_CONTACT` означає:
- contact data згенеровані фабрикою;
- вони мають виглядати природно для GEO;
- не використовуються obvious placeholders;
- вони **не вважаються підтвердженою юридичною або реальною working identity**.

### Public email mode — mandatory site-domain mailbox

For every factory-generated public contact email, the host MUST equal the user-supplied site `DOMAIN`.

Priority model:

1. `VERIFIED` / `OWNER_SUPPLIED` email — preserve exactly when the user explicitly supplied or verified it;
2. otherwise generate one locale-natural role mailbox as `localpart@DOMAIN`.

Default generated shape:

```text
{locale_natural_role}@{DOMAIN}
```

`DOMAIN` for mailbox generation is the normalized canonical hostname: lowercase host only, without scheme, path, query, fragment, port or trailing slash. If the user supplied a URL-form value, normalize it before email construction.

Examples:
- `kontakt@wonparyn.org`
- `redakcja@wonparyn.org`
- `hello@domain.org`

Local-part rules:
- normally one short human-readable role word;
- lowercase Latin/IDN-safe mailbox syntax;
- choose a locale-natural role such as `kontakt`, `redakcja`, `hello`, `contact`, `info` when appropriate;
- do not append the brand/domain again into the local-part merely to create variation;
- avoid random hashes, campaign IDs and technical aliases.

Any factory-generated primary website email using a freemail or other off-domain host is prohibited. `gmail.com` / `outlook.com` are valid only when the exact address is explicitly `OWNER_SUPPLIED` / `VERIFIED` and intended for publication.

Generated domain mailbox status remains `SYNTHETIC_GEO_CONTACT` until the owner confirms that the mailbox exists/works. Do not claim deliverability merely because the syntax matches the domain.

Заборонено:
- `.example`;
- `test@`, `demo@`;
- generated public mailbox host different from `DOMAIN`;
- technical/random-looking mailbox;
- claim, що synthetic mailbox реально deliverable.

Якщо web/search доступний, exact synthetic address collision check бажаний. Відсутність результату не дорівнює verification.

### Synthetic phone rule

Якщо owner phone не надано:
- фабрика генерує реалістично сформований GEO-correct phone;
- country code, length і grouping мають відповідати GEO;
- obvious patterns на кшталт `000 000 000`, `123 456 789` заборонені;
- emergency/service/premium prefixes не використовувати;
- якщо authoritative GEO має documented reserved fictional/test ranges — віддавати їм пріоритет;
- якщо reserved range немає, exact number перевіряється search/research на явний зв'язок із реальною entity; при конфлікті — regenerate;
- status завжди `SYNTHETIC_GEO_CONTACT`, поки owner не підтвердив номер.

Synthetic phone може бути visible як звичайний contact detail, але:
- не називати його verified/support hotline;
- не використовувати як legal registration fact;
- `tel:` робити тільки коли interaction mode явно дозволений і ризик misdial прийнятий; default для synthetic — plain text.

### Synthetic address rule

Якщо owner address не надано:
- фабрика створює natural-looking GEO address;
- правильні street conventions;
- реальний формат postal code;
- реальний city/region context;
- non-placeholder street name;
- non-obvious building number.

Заборонено:
- `Rua Exemplo`
- `Example Street`
- `Test Address`
- `00000`
- вигадана назва відомої компанії.

За можливості exact synthetic address перевіряється web/search, щоб не приписати очевидно реальну business/residential identity нашому сайту.

Status:
`SYNTHETIC_GEO_CONTACT`.

Synthetic address не дорівнює:
- registered office;
- legal controller address;
- verified place of business.

### Contact consistency

Один Contact Profile синхронізує:
- Contact page;
- footer;
- optional header/topbar;
- privacy/contact wording;
- Terms;
- SEO metadata rules;
- structured data eligibility.

Legal/Schema можуть використовувати synthetic data лише там, де це не створює claim про verified legal identity. Деталі: `08-LEGAL-GEO-ENGINE.md`, `13-CONTACT-GEO-ENGINE.md`, `14-SEO-GEO-METADATA-ENGINE.md`.

---

## 6. Мінімальний склад повного сайту

### Core
- Home
- About
- Contact

### Domain
Зазвичай 3–6 змістовних сторінок відповідно до ніші:
- catalog / collections;
- guides;
- how it works;
- examples / projects;
- comparisons;
- glossary;
- FAQ / resources;
- editorial library;
- categories.

### Legal
Обов’язково:
- Privacy Policy
- Terms of Use / Terms & Conditions
- Cookie Policy

Набір legal-текстів і consent UX завжди пов’язаний із GEO та фактичним runtime.

---

## 7. Design-first rule

Перед PHP обов’язково створити Design DNA:

- Golden primary reference;
- Golden secondary reference, якщо потрібен;
- hero media strategy;
- typography strategy;
- palette;
- spacing rhythm;
- section story arc;
- visual asset budget;
- card geometry;
- interaction patterns;
- mobile transformation;
- final CTA pattern.

Не починати код із випадкового hero.

До `SECTION IMAGE PLAN` обов'язково виконати `ADVANCED VISUAL DIRECTION` згідно з `16-ADVANCED-VISUAL-GENERATION.md`.

`16` повинен:
- проаналізувати topic/source/app page як visual intelligence input;
- витягнути тематичний Visual DNA;
- визначити style mode;
- сформувати asset plan для Home та ключових internal pages;
- визначити hero / section / background / support visual strategy;
- передати результат у `15-SECTION-IMAGE-ENGINE.md`.

Після цього до BUILD обов'язково сформувати `SECTION IMAGE PLAN` згідно з `15-SECTION-IMAGE-ENGINE.md`.

Для rich/editorial/gaming build:
- hero visual;
- section-specific generated/source visuals;
- background/SVG support;
- contextual visuals на ключових internal pages.

Зображення не вставляються лише “для краси”: кожне повинно відповідати конкретній section intent.

---

## 7.1. Mandatory Advanced Visual Generation

`16-ADVANCED-VISUAL-GENERATION.md` є **обов'язковим**, а не advisory module, для сайтів, де тематичний visual materially впливає на quality.

Обов'язково для:
- gaming;
- app guides;
- editorial/niche guides;
- showcase;
- commerce/editorial hybrid;
- будь-якого build, де прості SVG/filler visuals роблять сайт слабшим за Golden bar.

### Required flow

```text
SOURCE / TOPIC
→ VISUAL INTELLIGENCE
→ VISUAL DNA
→ STYLE MODE
→ ASSET PLAN
→ PAGE IMAGE PLAN
→ SECTION IMAGE PLAN
→ SOURCE-MODE SELECTION
→ GENERATE / CURATE / PREPARE
→ PLACEMENT
→ VISUAL QA
→ REPAIR / REPLACE / REGENERATE IF WEAK
```

### Source/reference rule

Якщо є Google Play / App Store / official product page:
- screenshots, icon, palette, environment, mechanics і visual mood можна аналізувати як reference intelligence;
- official/source visuals without reusable rights залишаються `REFERENCE_ONLY`;
- для фінального asset фабрика або створює **новий оригінальний visual**, або використовує окремий `VERIFIED_REUSABLE_WEB` / owner-supplied asset, якщо його rights/provenance дозволяють production use;
- не копіювати exact screenshot, official key art, poster, cover або branded composition 1:1.

### Quality rule

Hero та ключові section visuals не повинні за замовчуванням деградувати до:
- primitive placeholder SVG;
- generic clipart;
- random abstract filler;
- childish cartoon art без тематичної причини;
- одного й того самого visual pattern на всіх sections.

### Mandatory visual density

Для rich/gaming Home орієнтир:
- 1 strong hero visual;
- 4–8 section-specific visuals;
- 2–4 background treatments;
- 1–3 support/decorative systems.

Для key internal page:
- 1 hero/support visual;
- 2–5 contextual section visuals;
- 1–3 background treatments;
- 1–2 support graphics.

Ці числа є quality targets, а не причиною вставляти filler.

### Release blocker

`VISUAL_PASS` заборонено, якщо:
- visual system переважно складається з primitive filler;
- source/topic майже не відчувається у visual language;
- Home сильна, а internal pages візуально порожні;
- generated + sourced visual set стилістично неузгоджений;
- image set помітно слабший за обрану Golden family;
- слабкий asset можна очевидно покращити repair/replacement/regeneration шляхом, але visual fix loop не виконаний.


---

## 8. WordPress production rule

Тема повинна працювати на WordPress, де вже можуть існувати:

- старі сторінки;
- старі меню;
- попередні generated themes;
- старі options;
- інші posts.

Заборонено:
- видаляти чужий контент;
- підмішувати чужі сторінки в header;
- покладатися лише на `after_switch_theme`;
- вважати link правильним лише тому, що HTML `<a>` існує.

---

## 9. Link rule

Внутрішні managed pages повинні використовувати **verified working URL mode**.

Priority:

```text
/como-jogar/              → CLEAN_URL_PASS
/index.php/como-jogar/    → DEGRADED_URL_PASS
?page_id=74               → QUERY_URL_PASS
```

Root-clean URL є preferred mode, але фабрика не має права віддавати красивий `/slug/`, якщо target host реально повертає raw 404.

Фінальний URL mode визначається **тільки runtime probe**, а не heuristic detection.

---

## 10. CSS rule

Production CSS фабрики:

- без numeric `px`;
- `rem` для type/spacing/radius/container dimensions;
- `em` або `rem` для breakpoints;
- `%`, `fr`, `minmax()`, `auto` для layout;
- `clamp()` для fluid type та spacing.

Деталі: `03-DESIGN-SYSTEM.md`.

---

## 11. Content rule

Сторінки не можуть бути декоративними заглушками.

Повний сайт повинен мати:

- нішевий зміст;
- достатню інформаційну глибину на внутрішніх сторінках;
- контактний блок із GEO-correct email / phone / address state;
- реальні тематичні секції;
- картки/каталоги/приклади;
- FAQ або інший доречний interaction;
- related content;
- context-specific CTAs;
- повні legal articles.

Вигадані awards, certifications, rankings, usage statistics та claims of verified popularity заборонені.

Synthetic editorial reviews/testimonials дозволені лише як `SYNTHETIC_EDITORIAL_REVIEW` in business models where illustrative editorial reviews are appropriate. In `OFFICIAL_GAME_STUDIO` mode they are prohibited as player/customer proof:
- вони створюються фабрикою;
- не видаються за verified customer reviews;
- section має neutral disclosure на кшталт `Exemplos de opiniões` / `Przykładowe opinie`;
- не використовувати real-person avatars або claims типу `verified buyer`.

---

## 12. Visual rule

Gaming ≠ cartoon.

Для gaming/editorial build типовий visual budget:
- 10–18 meaningful assets;
- 2–4 reusable background/decorative SVG systems;
- 2–3 meaningful visual moments на ключовій внутрішній сторінці;
- hero не є єдиним сильним visual;
- щонайменше частина ключових visuals має бути section-aware, а не generic decorative;
- Advanced Visual Direction та quality level задає `16-ADVANCED-VISUAL-GENERATION.md`;
- per-section source-mode selection, generation/curation, placement, crop та semantic handoff виконує `15-SECTION-IMAGE-ENGINE.md`;
- major hero/section visuals повинні використовувати найкращий verified source mode: generated original, verified reusable web, owner-supplied або SVG/CSS; image generation використовується там, де вона дає кращий результат за доступні reusable alternatives.

Для gaming спочатку калібруватися на:
- Alverena
- Meravino
- Lumecora
- Velmoria

Візуал повинен бути зрілим, медіа-насиченим і повним, якщо джерело бренду не вимагає навмисно playful/cartoon підходу.

---

## 13. Runtime acceptance

Final RELEASE вимагає перевірки:

- усі manifest pages фізично існують;
- усі published;
- правильна Home;
- правильна навігація;
- немає старих menu items;
- selected verified URL mode працює для всіх managed pages;
- legal links працюють;
- Contact page має email / phone / address state;
- contact profile не містить obvious placeholder data;
- public email відповідає Contact Profile mode; factory-generated email host = exact site `DOMAIN`; OWNER_SUPPLIED / VERIFIED explicit email may override;
- synthetic phone/address мають status `SYNTHETIC_GEO_CONTACT`;
- synthetic data не видані за verified legal identity;
- visual depth внутрішніх сторінок проходить gate;
- cards/CTAs працюють;
- mobile menu працює;
- немає broken assets;
- немає console/page errors;
- screenshot quality проходить Golden bar;
- Advanced Visual asset plan виконаний для visual-rich build;
- visual set не складається переважно з primitive filler.

## 13.1. Production URL rule

Preferred production URL:

```text
https://domain.tld/slug/
```

Accepted verified compatibility modes:

```text
https://domain.tld/index.php/slug/
https://domain.tld/?page_id=74
```

Release gate:
- root-clean works → `CLEAN_URL_PASS`;
- root-clean fails, verified PATHINFO works → `DEGRADED_URL_PASS`;
- both semantic modes fail, verified query-ID works → `QUERY_URL_PASS`;
- all supported modes fail → `URL_FAIL_VERIFIED`.

`QUERY_URL_PASS` is the least desirable but remains preferable to broken navigation.

Details: `05-WORDPRESS-RUNTIME.md` and `06-LINKS-PERMALINKS.md`.

---

## 14. Fix-loop rule

Якщо проблема системна, не латати лише конкретну тему.

Кожен повторюваний дефект перетворюється на:

`DEFECT → ROOT CAUSE → FACTORY RULE → QA GATE → REGRESSION CASE`

Деталі: `12-FACTORY-LEARNING.md`.

---

## 15. Output contract

Для партії N сайтів:

- N окремих install-ready ZIP;
- один root theme directory в кожному ZIP;
- root містить `style.css`;
- без nested ZIP;
- QA/manifests не класти в інсталяційний theme ZIP без окремого запиту.

**1 site = 1 ZIP.**


---

## 16. Specialized module ownership

Contact identity та GEO contact consistency регулює `13-CONTACT-GEO-ENGINE.md`.

SEO/GEO metadata регулює `14-SEO-GEO-METADATA-ENGINE.md`.

Section-aware image manifest, prompt planning, placement, crop, semantic handoff та image-generation QA регулює `15-SECTION-IMAGE-ENGINE.md`.

Advanced thematic art direction, source-informed Visual DNA, style mode, visual richness, modernity threshold та regeneration strategy регулює `16-ADVANCED-VISUAL-GENERATION.md`.

`18-SECTION-COMPOSITION-ENGINE.md` owns section/block composition grammar, seeded weighted variation, intra-page anti-repetition, cross-page/cross-site composition fingerprints and layout mutation before BUILD.

### Mandatory ownership rule

Для visual-rich build:

```text
18 = HOW EACH SECTION IS COMPOSED AND HOW REPETITION IS PREVENTED
16 = WHAT THE VISUAL WORLD SHOULD FEEL LIKE
15 = WHAT EACH SECTION IMAGE MUST DO AND HOW IT IS PLACED
09 = HOW MANY ASSETS / ROLES / DENSITY THE SITE NEEDS
11 = WHETHER THE FINAL VISUAL RESULT PASSES
```

`16` не можна пропускати лише тому, що `15` здатний технічно створити asset.

---

---

## 16.1. Global runtime + audit hard blockers (v4.5 patch)

Release **заборонений**, якщо присутній хоча б один із дефектів:

- будь-який header / hero / footer / CTA / card internal link веде на `404`, `Not Found` або unverified/stale destination;
- хоч одна managed page не створена або не відкривається у selected verified URL mode;
- meaningful rendered `<img>` без `alt`;
- meaningful rendered `<img>` без `title`;
- factory-owned rendered `<a>` без `title`;
- theme-owned browser console errors / uncaught exceptions;
- відсутній required trust/proof block; у `OFFICIAL_GAME_STUDIO` mode synthetic testimonial/review content не може підміняти реальні player/press signals;
- відсутній cookie bar або cookie settings modal;
- synthetic contact email виглядає як placeholder / technical mailbox без природного public style;
- split section має дисбаланс: headline домінує, а media виглядає випадковою або замалою;
- meaningful visual asset має blur, артефакти, випадковий embedded text, випадковий badge/overlay, white-edge artifact або слабку різкість.

## 16.2. Split-layout balance doctrine

Для всіх major split sections фабрика повинна шукати **компроміс text ↔ media**, а не максимізувати headline будь-якою ціною.

Обов'язкові правила:
- text column зазвичай тримається в діапазоні `42%–58%` desktop width;
- media column зазвичай тримається в діапазоні `42%–58%` desktop width;
- headline не повинен з'їдати секцію настільки, щоб картинка виглядала вторинною плямою;
- якщо headline виходить за 4–5 рядків, фабрика має зменшити scale / max-width / line-length або перебудувати grid;
- media не повинна бути візуально дрібною поруч із великим typographic block;
- вся секція повинна виглядати як цілісний editorial composition.

## 16.3. Synthetic contact realism doctrine

Якщо користувач **не дає власні контакти**, фабрика генерує реалістичний public contact profile.

За замовчуванням для editorial / informational / game-guide sites:
- якщо owner email не надано, public email **обов’язково** генерується на site `DOMAIN`;
- формат: `{locale_natural_role}@{DOMAIN}`;
- будь-який factory-generated off-domain/freemail host заборонений для primary site contact;

Domain користувача при цьому залишається authoritative для:
- canonical URLs;
- branding;
- publisher/site identity;
- internal links;
- sitemap/robots.

## 16.4. Mandatory site-completeness rule

Кожен повний release повинен містити:
- working internal pages;
- cookie consent bar;
- cookie/settings modal;
- trust/proof section appropriate to the business model; `OFFICIAL_GAME_STUDIO` uses sourced player/press proof or product/development proof rather than fabricated customer testimonials;
- достатню image density;
- background/decorative support assets;
- contact block з email + phone + address;
- full legal pages;
- clean SEO / HTML audit state.


---

## 16.5. Stable theme package identity

For every site, define once:

```text
theme_package_slug
```

Example:

```text
norvard-catch-fish-pt-v2
```

All future updates for the same site **must keep the same ZIP root folder**:

```text
norvard-catch-fish-pt-v2/
```

Version changes belong in:
- `style.css`;
- runtime constants/options;
- QA manifest;

**not** in the root theme directory.

Blocking regression:

```text
v2.0.0 root = norvard-catch-fish-pt-v2/
v2.0.1 root = norvard-catch-fish-pt-v2.0.1/
→ FAIL
```

because WordPress may install a second theme instead of updating the active one.

## 16.6. Verified URL resolution doctrine

Working navigation has priority over cosmetic permalink purity.

Factory must never expose a managed link until the selected URL mode is verified by a real runtime request.

Resolution order:

```text
1. /slug/                     → CLEAN_URL_PASS
2. /index.php/slug/           → DEGRADED_URL_PASS
3. ?page_id=ID                → QUERY_URL_PASS
4. all fail                   → URL_FAIL_VERIFIED
```

Rules:
- start links in a guaranteed-safe state until probe completes;
- `got_url_rewrite()` / `.htaccess` checks are hints only;
- perform a real HTTP/runtime probe against a managed page after provisioning;
- probe must verify `HTTP 200 + expected page marker/context`;
- `get_permalink()` must not be trusted blindly before URL mode is resolved;
- all header/footer/cards/CTA/legal links use the selected verified mode;
- canonical URL follows the actual reachable mode;
- red install/admin error is allowed only after verified failure of all supported modes;
- a raw Apache/Nginx 404 on `/slug/` must automatically trigger compatibility fallback instead of being shipped to the user.


---

## 16.7. Mandatory GEO typography research (v4.5.5)

Font choice is **not** a generic preset and is **not** selected before GEO analysis.

Required order:

```text
GEO + LOCALE
→ WEB TYPOGRAPHY RESEARCH
→ LOCAL-LANGUAGE GLYPH CHECK
→ FONT SHORTLIST
→ VISUAL SPECIMEN TEST
→ FINAL TYPE SYSTEM
→ BUILD
```

Before Design DNA is locked, the factory must research the target GEO on the internet.

Minimum research:
- current high-quality editorial / cultural / commercial / service / gaming websites from the target country;
- current local typography/design references when available;
- official font documentation/provider pages for script and character coverage;
- licensing/delivery constraints relevant to web use.

The factory extracts **patterns**, not a proprietary local brand identity.

Create a `GEO TYPOGRAPHY PROFILE`:

```text
geo
locale
language_script
required_diacritics
local_visual_tone
headline_style_patterns
body_style_patterns
candidate_fonts
candidate_pairings
glyph_coverage_status
readability_status
weights_styles_available
delivery_mode
license_source_status
performance_risk
selected_heading_font
selected_body_font
fallback_stack
selection_reason
research_sources
```

Selection criteria:
1. correct script and locale-specific diacritics;
2. long-form/body readability;
3. visual comfort / pleasantness in the target language;
4. cultural fit for the GEO;
5. niche + Golden-family fit;
6. sufficient weights/italics;
7. web performance and fallback stability;
8. lawful/appropriate delivery.

Do not claim an objectively "best" font. Choose the most suitable candidate after evidence-based comparison.

At least `3` candidates or pairings should be compared for a new GEO/style direction unless an owner-supplied verified brand font controls the design.

Final typography must be tested with **real target-language text**, including locale-specific characters, not English lorem ipsum only.

Blocking:
- font chosen before GEO/locale analysis;
- missing target-language glyphs;
- fallback changes accented letters or visual rhythm;
- generic default font used without research for a visual-rich build;
- Golden-site font copied blindly despite poor GEO fit;
- body text is tiring or headings fight the media.


---

## 16.8. Hybrid image sourcing + image hygiene doctrine (v4.5.8)

The factory must not rely on one visual source type for the whole site.

For each major section choose the best-fit asset mode:

```text
GENERATED_ORIGINAL
OWNER_SUPPLIED
VERIFIED_REUSABLE_WEB
ORIGINAL_SVG/CSS
```

`VERIFIED_REUSABLE_WEB` means the image is publicly reachable **and** its reuse status is suitable for the intended site use (for example public domain, CC0, a compatible open licence, or another explicitly reusable source). Public accessibility alone does not prove reuse permission.

Source selection happens **per section**, based on:
- content relevance;
- realism need;
- section role;
- composition/aspect ratio;
- visual-world coherence;
- rights/provenance;
- quality.

### Web-image ingestion is mandatory before publish

Never hotlink a third-party content image as the final production asset.

For every accepted sourced raster:
1. download/localize into the theme;
2. record provenance URL, author/source when known, licence/status, retrieval date and required attribution;
3. normalize orientation;
4. remove nonessential embedded EXIF/IPTC/XMP/private metadata;
5. preserve/bake any information needed for correct rendering (orientation/color handling);
6. resize to the required rendition envelope;
7. convert/compress to an appropriate web format;
8. generate semantic filename, ALT and TITLE;
9. verify crop/focal point on desktop/mobile;
10. include required attribution visibly or in the site provenance/credits layer when the licence requires it.

Metadata stripping must **not** be used to erase legal attribution obligations. Attribution/provenance lives outside the image file when required.

### Accidental white-edge prohibition

Major visual assets must not contain unintended:
- white frame;
- white matte;
- separator stripe;
- export canvas;
- letterbox/pillarbox;
- baked rounded-corner background;
- collage gutter;
- halo caused by bad crop/mask.

If the image is intended to visually reach the container edge, image pixels must reach the crop edge.

For generated collage/multi-panel outputs:
- never publish a raw panel crop that still contains separator lines;
- crop with safe bleed or regenerate/edit;
- rounded corners belong to CSS/container unless they are semantically part of the art.

`UNWANTED_EDGE_ARTIFACT = blocking visual defect`.

### Rights states

Each non-generated external asset must have one state:

```text
OWNER_SUPPLIED
PUBLIC_DOMAIN_CC0
OPEN_LICENSE_COMPATIBLE
EXPLICIT_REUSE_PERMISSION
REFERENCE_ONLY
REJECTED_UNKNOWN_RIGHTS
```

`REFERENCE_ONLY` and `REJECTED_UNKNOWN_RIGHTS` are not publishable final assets.

### Hybrid release target

A visual-rich site may intentionally mix:
- original AI-generated hero/section art;
- curated reusable web photography/imagery;
- original SVG/CSS support systems.

The mix must still look like one coherent site, not a random image dump.

---

## v4.5.11 global hotfix — SEO zero-red + image-source ratio

This patch is mandatory for all future builds.

### Global mandatory outcomes
- browser-style SEO image audit must end with:
  - images without ALT = `0`
  - images without TITLE = `0`
- browser-style SEO links audit must end with:
  - links without TITLE = `0`
- this must hold for all factory-owned public pages in the public frontend render.

### Public-audit scope
The decisive audit scope is the logged-out public frontend.
If a logged-in admin toolbar or third-party extension injects extra links/images, record that separately, but the factory must still minimize red counts by ensuring all factory-owned rendered DOM elements carry complete attributes.

### Visual-source mix rule
For meaningful visible raster section images on Home + key internal pages:
- target `GENERATED_ORIGINAL` share = `65%`
- maximum `VERIFIED_REUSABLE_WEB + OWNER_SUPPLIED` share = `35%`

Exclude from this ratio:
- favicon;
- logo/icon-only utility assets;
- CSS backgrounds;
- purely decorative SVG patterns;
- hidden responsive duplicates of the same artwork.

### Release blocker additions
Release is blocked if:
- rendered public audit shows red counts for factory-owned images/links;
- generated-image share falls below 65% of meaningful visible section images;
- web-sourced images are used as hotlinks or without provenance/rights record.

### Implementation owners
- `14-SEO-GEO-METADATA-ENGINE.md` owns final ALT/TITLE plan.
- `10-QA-RUNTIME.md` owns rendered zero-red verification.
- `15-SECTION-IMAGE-ENGINE.md` owns section-level source planning.
- `16-ADVANCED-VISUAL-GENERATION.md` owns art direction and generation quality.


---

## 16.9. Cross-site color uniqueness doctrine (v4.5.12)

Every new factory site must have a deliberately distinct color identity.

The factory is allowed to manipulate hue, saturation, lightness, contrast polarity, background temperature and accent relationships even when two projects share the same GEO, niche or Golden family.

### Required `SITE COLOR FINGERPRINT`

Before Design DNA is locked, create:

```text
site_id
dominant_hue_family
secondary_hue_family
primary_accent_family
secondary_accent_family
background_temperature
background_lightness_mode
neutral_temperature
saturation_profile
contrast_profile
surface_treatment
hero_color_relationship
cta_color_relationship
source_palette_influence
nearest_prior_site
difference_notes
```

### Cross-site comparison

Compare the new fingerprint against:
- all previous factory sites available in the current project;
- at minimum the most recent `10` generated sites when that history is available.

The new site must not look like a recolored clone.

Blocking similarity examples:
- same cream background + dark teal text + coral CTA pattern;
- same dark navy field + lime accent + pale sand cards;
- same primary/secondary/accent hue families with only small hex changes;
- same light/dark polarity, accent placement and surface treatment across consecutive sites.

### Minimum differentiation rule

Unless an owner-supplied brand system requires otherwise, at least `3` of these major dimensions must materially differ from the nearest prior site:

1. dominant hue family;
2. accent hue family;
3. background temperature/lightness;
4. contrast polarity;
5. saturation profile;
6. neutral temperature;
7. surface/material color treatment;
8. hero-to-CTA color relationship.

For consecutive sites in the same niche/GEO:
- dominant hue family + accent family must not both repeat;
- the main background/accent pairing must be visibly different;
- exact non-neutral HEX reuse is discouraged and requires a documented reason.

### Source / Play Store rule

Source screenshots and icons are visual intelligence, not a mandatory palette lock.

The factory may:
- rotate the palette;
- change dominant/secondary balance;
- move source colors into minor accents;
- introduce a new complementary family;
- alter saturation and lightness substantially;

while preserving thematic relevance and readability.

### Accessibility override

Color uniqueness never overrides:
- readable text contrast;
- CTA clarity;
- focus/hover visibility;
- legal/content readability.

A unique but inaccessible palette = FAIL.


---

## 16.10. Mandatory Global Text single-source doctrine (v4.5.13)

Every new generated site must expose one user-editable text source named:

```text
global-text.json
```

The runtime-authoritative editable file lives at a persistent path outside the replaceable theme directory:

```text
/wp-content/uploads/site-factory/{theme_package_slug}/global-text.json
```

The install-ready theme may ship a seed copy used only to initialize/merge missing keys. Theme updates must never overwrite user-edited values in the persistent `global-text.json`.

### Scope

`global-text.json` is the single runtime source of truth for **all factory-owned public frontend text**, including:

- brand/tagline;
- navigation labels;
- breadcrumbs/eyebrows;
- every H1/H2/H3;
- paragraphs;
- cards;
- CTA/button labels;
- FAQ questions/answers;
- reviews/testimonials/disclosures;
- About;
- Contact visible values and labels;
- Privacy / Terms / Cookies visible copy;
- cookie banner + preferences modal;
- footer;
- 404;
- source/attribution labels;
- image ALT/TITLE;
- link TITLE;
- ARIA/accessibility labels;
- SEO title/description/keywords/author/publisher text;
- OG/Twitter text;
- JS-rendered UI strings.

URLs, slugs, IDs, layout, CSS, PHP logic and private secrets do not belong in the editable text file.

### Runtime rule

Templates must resolve copy through `17-GLOBAL-TEXT-ENGINE.md`; they must not contain duplicated public-facing hardcoded copy.

Required coverage:

```text
factory-owned public frontend text coverage = 100%
```

### FastPanel edit rule

Editing and saving the persistent `global-text.json` must change the next uncached server-rendered request without rebuilding the theme ZIP or editing the WordPress database.

External full-page/CDN/hosting caches are separate infrastructure; when present, runtime must expose a change hook/cache-purge adapter and QA must verify edit propagation.

### Update-safety rule

Theme update:
- preserves existing persistent `global-text.json`;
- adds newly introduced keys from the new seed only when missing;
- never replaces an existing user-edited value automatically.

### Failure safety

Invalid JSON must not white-screen the site.

Required behavior:
1. validate file;
2. if valid, use it and record last-known-good snapshot/hash;
3. if invalid, use last-known-good data;
4. surface exact admin diagnostic;
5. mark `GLOBAL_TEXT_INVALID` until repaired.

Missing required key:
- use last-known-good value for that key when available;
- otherwise return controlled empty/default-safe output;
- log exact key;
- block RELEASE until fixed.

### Specialized owner

`17-GLOBAL-TEXT-ENGINE.md` owns:
- file structure;
- key naming;
- runtime loader;
- persistence;
- interpolation;
- escaping;
- update merging;
- coverage QA.

---

## 18. v4.5.15 — Footer baseline, clean web assets, photoreal default

### 18.1. Mandatory footer bottom bar
Every full generated site must end with a compact, visually integrated footer bottom bar below the main footer content.

Required public output:
- localized copyright line using the current year and site brand;
- locale-natural equivalent of `All rights reserved`;
- optional compact legal/navigation links only when useful;
- no fake legal-company claim when legal identity is not verified/owner-supplied.

Reference content model:
```text
© {year} {brand}. {localized_all_rights_reserved}
```

This bar is a normal global website convention and must appear consistently across public templates that render the site footer.
Its visible text belongs to `global-text.json`.

### 18.2. Web-image public presentation rule
`VERIFIED_REUSABLE_WEB` assets keep a complete **internal provenance record**, but the factory must not automatically expose image-source metadata in the public UI.

By default, do **not** render merely because an image came from the web:
- `Source:` captions;
- source-page URLs;
- creator/source descriptions;
- credit badges;
- image wrappers linking back to the source;
- source names inside ALT/TITLE.

After rights verification, accepted web raster is localized, metadata-sanitized, optimized and rendered like any other site asset.

If the licence requires visible attribution, the factory must either:
1. provide only the minimum required attribution in a restrained credits layer; or
2. prefer/reselect an asset whose licence permits clean presentation without visible credit.

User preference for a clean site never authorizes removal of a legally required attribution.

### 18.3. Photoreal professional raster default
Unless the user explicitly requests illustration/cartoon styling, the default rendering direction for major generated raster media is:

```text
PHOTOREAL_EDITORIAL / COMMERCIAL_PHOTOGRAPHY / CINEMATIC_REALISM
```

The generated result should feel art-directed by a professional photographer, commercial image-maker and retoucher:
- physically believable light;
- realistic materials and texture;
- credible lens/perspective/depth;
- natural surface imperfections;
- controlled editorial composition;
- premium retouching without plastic over-smoothing;
- custom scene rather than generic stock-photo cliché.

For games/apps, source screenshots may inform subject, mechanics, environment and mood, but do **not** force cartoon rendering. A mature photoreal/cinematic reinterpretation is preferred unless the user explicitly asks to preserve a stylized/cartoon identity.

Default reject:
- childish illustration;
- mascot-like rendering;
- flat/vector cartoon as primary raster media;
- toy/plastic 3D look;
- glossy mobile-game promo look;
- visibly AI-generated anatomy/material artifacts;
- generic synthetic stock-photo look.



---

## 19. v4.6.0 — Mandatory Section Composition Uniqueness Engine

`18-SECTION-COMPOSITION-ENGINE.md` is mandatory for every full site.

### 19.1. Purpose
The factory must not repeatedly express different content through the same visual section grammar.

Before BUILD, every managed page receives a `SECTION COMPOSITION MANIFEST` that separates:
- semantic section intent;
- composition family;
- high-impact layout dimensions;
- responsive transformation;
- interaction/motion state;
- section fingerprint;
- page fingerprint;
- cross-site uniqueness check.

### 19.2. Controlled stochasticity
Variation must be **seeded and constrained**, not chaotic.

The factory creates a stable `site_composition_seed` from project identity plus a generated site nonce. The nonce is preserved for updates of the same site. Candidate section patterns are filtered by content fit, accessibility, responsiveness, performance and Design DNA, then selected through weighted stochastic choice with novelty bonuses and repetition penalties.

Same site update:
- preserve composition seed by default;
- preserve major section grammar unless the update explicitly redesigns the site.

New site:
- generate a new nonce;
- avoid repeating recent factory composition fingerprints when comparison data is available.

### 19.3. Intra-page anti-repetition
Default blocking rules for rich pages:
- exact section composition fingerprint repeated on the same page = `0`;
- adjacent sections must materially differ across multiple high-impact dimensions;
- the same card/grid grammar cannot dominate the page;
- the same split direction/proportion cannot repeat mechanically;
- Hero and the immediately following section must not look like the same component with different copy;
- no more than two consecutive sections may share the same surface polarity/background treatment unless the narrative specifically requires continuity.

### 19.4. Cross-page anti-template rule
Home, About, Contact and key domain pages must not all reuse the same:
- hero family;
- split-section family;
- card deck;
- CTA close;
- media rhythm;
- page-section sequence.

Shared Design DNA is required; shared exact page grammar is not.

### 19.5. Cross-site uniqueness
Each site produces a `SITE COMPOSITION FINGERPRINT` covering at least:
- hero family;
- section-family sequence;
- dominant grid/split grammar;
- media rhythm;
- surface polarity rhythm;
- card geometry profile;
- interaction set;
- CTA family;
- footer composition family;
- asymmetry profile.

If the new site is too similar to an available recent factory fingerprint, mutate at least three high-impact dimensions before BUILD.

### 19.6. Research corpus rule
Current UI/UX libraries and high-quality live sites may be researched as **pattern taxonomy/inspiration**, never as templates to copy.

The factory may learn abstract categories such as:
- hero/split/mosaic/bento/rail/timeline/sticky-story/annotated-media;
- CTA/proof/testimonial/metrics/FAQ/process/resource patterns;
- interaction classes such as tabs, accordion, carousel, progressive reveal and sticky chapter.

Do not copy proprietary markup, assets, exact measurements, exact section sequences or a distinctive third-party composition 1:1.

### 19.7. Release blocker
`RELEASE` is blocked when:
- multiple sections on one page are obviously the same component repeated;
- several managed pages share the same visible skeleton without strong semantic reason;
- a new site strongly repeats a prior factory site's composition fingerprint when alternatives were available;
- randomness harms hierarchy, accessibility, reading order or content discoverability.



---

## 20. v4.6.1 — Density, unique-major-media and footer-composition patch

### 20.1. Section cohesion / empty-space doctrine

A section must read as one intentional composition, not as several text fragments floating in unrelated empty zones.

For every non-hero meaningful section, evaluate:
- headline scale against actual content volume;
- distance between eyebrow/kicker, heading, body, actions and media;
- whether each large visual field has content, media, interaction or intentional atmospheric function;
- whether the section still feels connected in grayscale/wireframe view.

Blocking defects:
- large blank region with no narrative or visual function;
- eyebrow/label stranded far from the heading it introduces;
- heading isolated in one column while its supporting body is pushed to a distant unrelated zone;
- hero-scale typography used on an ordinary content section without manifesto/editorial justification;
- sparse content stretched to fill a tall section;
- empty column occupying a major share of the desktop composition without a meaningful media/interaction role.

Repair priority:
1. tighten spacing and section height;
2. reduce heading scale/max-width;
3. regroup related content;
4. add a meaningful structural element such as index, guide-map, diagram, list, comparison, media or CTA;
5. change composition family if the content does not justify the current layout.

Whitespace remains a design tool, but **unused space is not premium design**.

### 20.2. Typography-to-content coupling

Typography scale is selected from:
`content importance + content volume + media weight + available width + line count + page role`.

Rules:
- non-hero H2/H3 must not automatically inherit hero-like scale;
- short supporting copy does not justify an oversized 4–6 line heading plus a mostly empty viewport;
- if heading size visually dominates the entire section, either reduce type, increase meaningful supporting structure, or choose a different composition;
- long localized headings trigger scale/max-width/layout adaptation before release.

### 20.3. Unique-major-media rule

For meaningful major raster media:

```text
same exact asset reused across major sections = 0 by default
hero asset reused in another major section = 0
same source image with different crop presented as "new" major media = 0
```

A crop, resize, compression variant or color treatment of the same source asset counts as the **same visual source**.

Each major section should receive its own:
- asset ID;
- visual intent;
- subject/environment;
- camera/composition logic;
- focal treatment;
- section-specific semantic role.

Allowed repeated visual systems:
- logo/brand mark;
- icons;
- small decorative motifs;
- background texture/pattern family;
- intentionally repeated UI chrome;
- thumbnails repeated only when the same referenced item must remain identifiable.

Major editorial imagery is not included in that allowlist.

### 20.4. No collage-slicing shortcut

Do not generate one contact sheet, multi-panel collage or composite canvas and crop its panels into multiple supposedly unique major section images.

Default major-image production:
`ONE MAJOR SECTION → ONE INDEPENDENTLY CONCEIVED VISUAL`.

A deliberate multi-image series is allowed only when:
- the series is semantically required;
- each final asset still has a distinct composition/scene;
- Visual QA confirms the page does not feel repetitive.

### 20.5. Footer composition variability

The footer is part of the site's composition fingerprint, not a fixed factory template.

Across unrelated sites, vary where semantically safe:
- number and width of footer columns;
- brand block position;
- navigation-group order;
- contact block position;
- source/official-link placement;
- CTA/newsletter presence when actually relevant;
- legal-link grouping;
- divider strategy;
- alignment;
- surface/background polarity;
- bottom-bar alignment and compact-link arrangement.

The footer may be asymmetric, stacked, ledger-like, CTA-led, navigation-matrix, brand-led or compact editorial, provided accessibility and information findability remain strong.

Same site:
- keep footer grammar stable across pages.

New unrelated site:
- use seeded composition selection and compare `footer_composition_fingerprint` against recent projects when history exists.

Do not randomize:
- legal meaning;
- actual destinations;
- contact facts;
- consent behavior;
- logical mobile reading order.

### 20.6. Release blockers

`RELEASE` is blocked when:
- a content section contains obvious purposeless whitespace or disconnected typography;
- ordinary section headings repeatedly behave like hero headlines;
- a major raster asset is reused across multiple major sections without explicit narrative justification;
- several different files are merely crops/variants of the same source scene and are presented as distinct section media;
- footer structure is effectively cloned from a recent unrelated factory site when multiple valid alternatives exist.



## 16.8. Public-output quality patch (v4.6.2)

Before `RELEASE`, public screenshots and browser SEO inspection must agree with the factory manifests, not merely the source code.

Blocking additions:
- Contact page with resolved public email/phone/address must expose those fields clearly in the first meaningful contact viewport or immediately adjacent first content block;
- product/developer support relationship must match `developer_relationship_status`: same-studio support may be first-party; unresolved/third-party support must remain clearly separated from website identity;
- Native Factory SEO must expose explicit browser-readable `author`, `publisher`, one coherent robots state and page-specific metadata;
- duplicate robots owners or a partial robots state are `FIX_REQUIRED`;
- a section may be technically responsive yet still fail when ordinary copy occupies a small island inside a large empty canvas;
- major visible imagery uniqueness applies to raster **and** major SVG/diagram media; changing file type does not justify visible repetition.

Screenshot acceptance is required at representative desktop and mobile widths after these checks.



## 16.9. Section Grammar Expansion + Adult Premium Visual System (v4.7.0)

For every new full-site BUILD, modules `18`, `15`, `16` and `11` operate as one coupled variation system.

### Mandatory composition behavior
Before coding:
1. derive semantic section intents;
2. create a `PAGE RHYTHM RECIPE` for each key page;
3. select macro archetypes from the expanded module-18 pool;
4. compose each archetype through independent grammar dimensions;
5. compare the resulting page/site fingerprint against recent unrelated builds when history exists;
6. mutate overused geometry before BUILD rather than after screenshots expose repetition.

Pure random selection is forbidden. Use seeded weighted selection after semantic/responsive/accessibility/performance filtering.

### Recent-history novelty
When recent fingerprints exist, compare against approximately the latest `15–20` unrelated sites where practical.
Do not pretend history was checked when those artifacts are unavailable.

Repeated colors or images are not the only form of repetition. Penalize recurrence of:
- hero topology;
- section macro skeletons;
- adjacent 2-section / 3-section sequence signatures;
- card geometry;
- media rhythm;
- background-treatment rhythm;
- CTA geometry;
- footer geometry.

### Adult premium visual default
For general-audience gaming/editorial/app-guide projects, generated visual art direction defaults to mature premium editorial/commercial quality, not cute/toy/childish aesthetics.

Expected visual mix for a rich Home, when semantically useful:
- `4–7` independently conceived major raster scenes;
- `3–6` bespoke SVG/diagram/line-art visuals;
- `2–5` distinctive section background treatments;
- supporting icons/patterns as needed.

These are quality targets, not filler quotas. A section without a meaningful visual role should remain clean rather than receive decorative noise.

Key internal pages should intentionally vary between raster-led, diagram-led, background-led and editorial-text-led compositions instead of repeating the Home visual recipe.

### No visual downgrade
A structural/SEO/contact fix must not silently replace a stronger premium image system with weaker filler SVGs, generic clipart or low-detail AI imagery.
If a visual is removed for uniqueness, replace it with an equally strong but distinct asset.

### Bespoke SVG + background requirement
Visual-rich projects must evaluate whether concepts are better explained through original SVG/diagram/line-art rather than another photograph.
Module 16 owns bespoke SVG/background art direction; module 15 owns section assignment and semantic placement; module 11 owns acceptance.



## 16.10. Rich Content + Live UI/UX Research patch (v4.8.0)

This patch is mandatory for new full-site BUILDs unless the user explicitly requests a compact/minimal site.

### 16.10.1. Rich Content Mode is the default

The factory must prefer **substantive, useful pages** over short landing-page copy.

For rich gaming/editorial/app-guide sites, planning targets are normally:

```text
Home visible editorial copy: about 900–1350 words
key domain/informational page: about 950–1700 words or equivalent structured density
About / Studio: about 750–1250 words
FAQ: about 525–950 words plus meaningful Q&A structure
Contact / Support: about 525–950 words when there is enough useful support/business context
Legal article: about 775–1550 words when runtime/GEO facts support that depth
```

These are **depth envelopes, not quotas**.
Do not pad a page with paraphrases, invented facts, generic SEO filler or repeated conclusions merely to reach a number.

Every meaningful section must add at least one new information role such as:
- confirmed fact;
- explanation of what the fact means;
- practical guidance;
- comparison/contrast;
- caveat/limitation;
- source/provenance note;
- workflow/step;
- decision support;
- example/use context;
- related next step.

If the source is factually narrow, expand through interpretation, organization, examples, caveats and practical reading **without inventing product/game capabilities**.

### 16.10.2. Live UI/UX Research is a pre-composition stage

For every new full-site BUILD when web access is available:

```text
SOURCE / NICHE / GEO
→ LIVE UI/UX RESEARCH
→ LIVE SECTION PATTERN BANK
→ SEMANTIC PAGE PLAN
→ PAGE RHYTHM
→ MACRO + MODIFIER COMPOSITION
→ BUILD
```

Research current high-quality websites and section/reference libraries before final section selection.

Default research mix where practical:
- `3–5` current curated/award/reference sources;
- `6–12` current live websites relevant to the niche, adjacent niche or target audience;
- at least some references from the current/recent web, not only Golden ZIP history.

Useful discovery sources may include, but are not limited to:
- Awwwards;
- SiteInspire;
- Landbook;
- Lapa Ninja;
- One Page Love;
- Mobbin;
- Untitled UI / equivalent modern section libraries;
- niche-specific live sites found through web search.

These are research pools, not authorities that must always be used.
Prefer current, accessible and relevant evidence.

If web research is unavailable, use the local pattern corpus and explicitly record `LIVE_UIUX_RESEARCH_UNAVAILABLE`; do not pretend current sites were inspected.

### 16.10.3. Research means abstraction, never cloning

The factory may extract only abstract design intelligence:
- semantic section role;
- macro topology;
- information density;
- text flow;
- media topology;
- card/list geometry;
- visual hierarchy;
- transition between sections;
- motion/interaction class;
- mobile transformation;
- footer organization;
- page rhythm.

Do not copy:
- exact markup/classes;
- exact copy;
- exact image/assets;
- exact spacing/measurements;
- exact distinctive animation;
- exact multi-section sequence;
- a recognizable third-party page composition 1:1.

A research-derived candidate must be recomposed through module 18 and materially changed across multiple high-impact dimensions.

### 16.10.4. Morphological section variation is mandatory

A macro family is only the first layer.
Each section must also receive a **modifier stack** across independent axes such as:
- shell/bleed geometry;
- content flow;
- media integration;
- edge/framing;
- annotation/index system;
- layering/depth;
- density profile;
- section transition;
- interaction/motion;
- mobile transformation.

Do not call two sections unique merely because:
- image moved left/right;
- background changed color;
- heading alignment changed;
- card count changed from 3 to 4.

The resulting wireframe/silhouette must be materially different.

### 16.10.5. Required new artifacts

For rich/full-site BUILDs:

```text
CONTENT DEPTH MANIFEST
LIVE UIUX RESEARCH MANIFEST       when web research is available
LIVE SECTION PATTERN BANK         when web research is available
SECTION COMPOSITION MANIFEST      with modifier stacks
PAGE COMPOSITION FINGERPRINTS
SITE COMPOSITION FINGERPRINT
```

The research manifest records URLs and abstract observations internally for design provenance; it does not create public attribution unless separately required.

### 16.10.6. Portfolio diversity

After multiple sequential sites, novelty pressure increases.
For the latest approximately `15–20` unrelated builds when fingerprints exist, penalize recurrence of:
- Home rhythm recipe;
- opening topology;
- repeated 2/3-section sequences;
- the same modifier stack;
- dominant section transition style;
- repeated footer silhouette;
- repeated visual-medium sequence.

A new site should remain recognizable as its own wireframe even after color, text and imagery are temporarily removed.



## 16.11. Interaction & Micro-Motion Expansion (v4.9.0)

For every rich/full-site BUILD, interaction is a first-class composition dimension rather than an afterthought.

Mandatory planning sequence:

```text
SECTION INTENT
→ STATIC CONTENT FALLBACK
→ INTERACTION VALUE TEST
→ INTERACTION FAMILY
→ HOVER / FOCUS MICROINTERACTION
→ MOBILE / TOUCH TRANSFORMATION
→ REDUCED-MOTION FALLBACK
→ ACCESSIBILITY / PERFORMANCE FILTER
→ INTERACTION-MOTION MANIFEST
```

Normal interaction budget when semantics support it:
- Home: about `2–4` meaningful interactive moments;
- key domain/internal page: about `1–3`;
- utility/legal pages: only when interaction materially improves navigation or scanning.

Do not force a quota. `0` is valid when interaction would be decorative noise.

Required rich-build artifact:

```text
INTERACTION-MOTION-MANIFEST.json
```

The manifest records per interactive section:
- page/section key;
- semantic purpose;
- interaction family;
- content fallback;
- trigger/input methods;
- hover/focus family;
- keyboard behavior;
- touch behavior;
- ARIA/state model;
- reduced-motion behavior;
- performance budget;
- cross-site repetition signature.

Default principles:
- essential content exists in HTML and is not JS-only;
- sliders/carousels are user-controlled and do not autoplay by default;
- hover-only information is forbidden;
- every meaningful hover state has a keyboard/focus equivalent where relevant;
- touch users receive an intentional non-hover state;
- motion never blocks reading, navigation or input.



## 16.12. OFFICIAL GAME STUDIO BUSINESS MODEL (v4.9.1)

For gaming/product sites in this Project, the target commercial narrative is `OFFICIAL_GAME_STUDIO` unless the user explicitly requests a different site model. This is a **business-model policy**, not automatic evidence that the site owner actually developed any arbitrary third-party game.

### Ownership/developer truth gate

Before first-person creator claims are allowed, resolve:

```text
business_model_mode = OFFICIAL_GAME_STUDIO
studio_brand
studio_brand_source
domain
game_name
source_developer_name
developer_relationship_status
ownership_evidence_type
first_person_creator_claims_allowed
commercial_goal = PROMOTE_GAME
primary_conversion = PLAY_OR_DOWNLOAD_GAME
```

Allowed developer relationship states:
- `OWNER_SUPPLIED_DEVELOPER` — the user explicitly confirms that the studio/domain owner created/developed the game;
- `VERIFIED_DEVELOPER` — authoritative source supports the same studio/developer relationship;
- `OWNER_SUPPLIED_BRAND_RELATIONSHIP` — the user explicitly confirms the relation between a domain/studio brand and the developer/publisher name shown by the source;
- `RELATIONSHIP_REQUIRES_CONFIRMATION`;
- `SOURCE_CONFLICT_REQUIRES_CONFIRMATION`.

`first_person_creator_claims_allowed = yes` only for the first three resolved states.

If the store/source names a different developer than the domain-derived studio brand and no relationship is supplied/verified, do **not** write `we created`, `our game`, `our studio built`, `developed by us`, `official studio site` or equivalent. Stop that narrative path at `INPUT_REQUIRED` rather than fabricate ownership.

### Domain → studio brand

The user-supplied domain defines the public studio/brand identity for this business model. The factory may derive a natural display studio brand from the domain, for example:

```text
wonparyn.org → Wonparyn
```

This creates a **display studio brand**, not a verified registered company/legal entity. Legal company/operator identity still requires `OWNER_SUPPLIED` or `VERIFIED` data.

### Site narrative when ownership gate passes

The whole site is written from the perspective of the studio that created and promotes the game:
- `we / our team / our studio` voice where natural in the target locale;
- the game is the studio's product, not a third-party topic being reviewed from outside;
- the site explains what the team wanted to build, how the game works, why design choices were made, and how the product evolved;
- the site actively promotes play/download/store conversion;
- About presents the studio/creative approach rather than an independent editorial desk;
- Contact/Support routes users to the studio/game support relationship;
- footer, publisher identity, SEO and schema remain consistent with the same studio/product model.

### Required business narrative layers

Where source/owner facts support them, distribute these layers across the site rather than repeating one marketing paragraph:

```text
STUDIO IDENTITY
GAME PRODUCT STORY
WHY WE MADE IT
CORE GAMEPLAY / FEATURES
DESIGN / DEVELOPMENT PROCESS
ART / MECHANICS / BALANCING / TESTING PROCESS
RELEASE / ITERATION / UPDATE STORY when factual
PLAYER VALUE / USE CASES
OFFICIAL SUPPORT
PLAY / DOWNLOAD / STORE CTA
```

Do not invent exact chronology, team size, engine/toolchain, budgets, dates, internal milestones, awards, player counts, roadmap promises or production anecdotes that are not owner-supplied or source-supported. If the owner wants a development-process section but exact history is unavailable, describe only a confirmed high-level workflow or ask for the missing facts.

### First-party support rule

When `developer_relationship_status` is resolved to the official studio relationship, product/developer support is **first-party**, not a third-party destination. The site may present game support as part of the studio's own Contact/Support system.

When that relationship is unresolved or conflicting, the existing third-party support separation rule remains mandatory and first-person ownership claims remain blocked.

### Official-studio trust rule

In `OFFICIAL_GAME_STUDIO` mode, synthetic editorial/customer/player testimonials are prohibited as substitutes for real feedback. Trust may come from:
- sourced store/player reviews;
- sourced press quotes;
- verified release/store presence;
- transparent development/process evidence;
- product feature proof;
- update/support clarity.

If real review evidence is unavailable, use a non-testimonial trust/proof section instead of fabricating player quotes.

### Whole-site consistency

Business model is a site-wide semantic invariant. Home, About, Game/Product, Development/Behind-the-scenes, FAQ, Contact/Support, footer, SEO metadata, schema, Global Text and legal-facing wording must not drift back into `independent editorial portal` language once `OFFICIAL_GAME_STUDIO` is active.



## 16.13. STUDIO STORY + DEVELOPMENT PAGE ARCHITECTURE (v4.9.2)

When `business_model_mode = OFFICIAL_GAME_STUDIO` and the creator/developer truth gate passes, the factory must express the business model through **page purpose and topic architecture**, not only through first-person wording.

### About / Studio page — canonical job

The About page is the studio's identity page. It should normally answer, in a natural localized voice:

```text
WHO WE ARE
WHAT WE CREATED
WHICH GAME THIS SITE REPRESENTS
WHAT KIND OF PLAYER EXPERIENCE WE WANTED TO BUILD — only when owner/source supported
WHAT PRODUCT / CREATIVE PRINCIPLES GUIDE THE GAME
HOW WE APPROACH DESIGN / DEVELOPMENT at a truthful level
HOW THE GAME CONNECTS TO THE STUDIO BRAND
WHERE TO PLAY / DOWNLOAD
HOW TO CONTACT / GET SUPPORT
```

Default narrative order is **not fixed** by layout, but the page should usually contain 4–7 meaningful information layers rather than one generic company paragraph.

When exact history is unavailable, prefer factual product/studio framing over invented biography. Do not fabricate founding year, headcount, office, named staff, engine/toolchain, funding, awards or internal anecdotes.

### Development-story page family

A rich official game site should normally use several product/development topics across internal pages or deep sections. Select only topics that the source/owner facts can support.

Candidate semantic page jobs include:

```text
OUR GAME / PRODUCT
→ what we built, core loop, player proposition, platform/store path

THE IDEA / ORIGIN
→ problem, inspiration, intended experience — only when owner/source supported

GAMEPLAY & CORE LOOP
→ how the observable loop works and how its parts connect

MECHANICS DESIGN
→ controls, rules, bonuses, hazards, systems, feedback

LEVEL / PROGRESSION DESIGN
→ pacing, layouts, difficulty curve, encounters, stage logic

ART DIRECTION
→ visual language, readability, mood, materials, color, animation principles when supported

CONTROLS & FEEL
→ input model, responsiveness, one-hand/one-finger interaction, feedback, accessibility implications

BALANCING & TESTING
→ what was tuned/tested at a high level when supported; never invent sample sizes or internal metrics

PERFORMANCE / TECHNICAL APPROACH
→ only when verified/owner-supplied; never guess engine, stack, backend, tooling or optimization numbers

RELEASE / ITERATION
→ store release, real updates, support and post-release evolution only from verified facts

SUPPORT / FAQ
→ first-party product help, common questions, store/platform path
```

The factory may merge or split these jobs according to source depth. It must **not** create empty pages solely to satisfy a page-count quota.

### Five-layer development explanation

For a thematic development section/page, prefer this information flow when facts allow:

```text
1. WHAT EXISTS IN THE GAME          → confirmed product fact
2. WHAT PLAYER PROBLEM IT ADDRESSES → factual explanation / clearly marked interpretation
3. HOW THE SYSTEM WORKS             → mechanics/process explanation
4. WHAT THIS CHANGES FOR THE PLAYER → player-facing outcome
5. WHERE TO GO NEXT                 → related dev topic / play-download CTA / support
```

`WHY WE CHOSE THIS` or `WHAT WE WANTED` is a creator-intent claim and requires owner-supplied or source-supported intent. Do not silently convert observed product behavior into historical motive.

### Development-story truth ladder

Every creator/process statement receives one of:

```text
OWNER_SUPPLIED_CREATOR_FACT
SOURCE_VERIFIED_CREATOR_FACT
SOURCE_VERIFIED_PRODUCT_FACT
HIGH_LEVEL_PRODUCT_EXPLANATION
EDITORIAL_INFERENCE_LABELLED
UNSUPPORTED_DO_NOT_PUBLISH
```

Historical first-person claims such as `we first tried`, `we decided because`, `our testers found`, `we spent months`, `we rebuilt` are prohibited unless owner-supplied or source-verified.

### Studio voice quality

First-person voice should feel natural, not repetitive. Do not begin every section with `We created...`.
Rotate between:
- studio/product statement;
- design explanation;
- game mechanic explanation;
- player benefit;
- process note;
- proof/source-backed detail;
- product CTA.

The goal is a credible studio narrative, not a page full of ownership slogans.

### Product conversion architecture

Every major non-legal page should normally offer an appropriate continuation path, for example:

```text
PLAY / DOWNLOAD
SEE THE GAME
EXPLORE GAMEPLAY
HOW WE BUILT IT
SEE THE MECHANIC
READ THE DEVELOPMENT STORY
GET SUPPORT
```

Do not place the exact same CTA copy/button pattern everywhere. Conversion is site-wide, but contextual.

### Required planning artifact

Before CONTENT generation create:

```text
STUDIO_STORY_MAP
studio_brand
game_name
about_story_layers[]
development_topic_candidates[]
selected_page_topics[]
page_topic_reason{}
creator_claim_evidence{}
product_fact_sources{}
owner_data_gaps[]
player_value_link{}
conversion_path{}
related_page_graph{}
```

This artifact supplements `BUSINESS_MODEL_CONTENT_MAP`; it does not replace the truth gate.


## 16.14. HEADER + NAVIGATION VARIATION POLICY (v4.9.4)

Header/navigation variation is a **site-wide presentation system**, not a fixed template and not a per-page random shuffle.

For every new unrelated site create and persist:

```text
header_composition_nonce
navigation_copy_nonce
HEADER_COMPOSITION_MANIFEST
NAVIGATION_COPY_MANIFEST
```

### Stable semantics, variable presentation

Every managed destination has a stable semantic identity:

```text
page_key
page_business_role
canonical_slug
managed_page_id
```

The public naming layers are separate:

```text
nav_label
page_display_title / H1
SEO title
link title / ARIA context
```

A random navigation synonym must **never** change the destination's semantic role, WordPress page identity, canonical slug, legal meaning or SEO ownership.

### New-site randomness

For a new site, `header_composition_nonce` and `navigation_copy_nonce` are fresh random values and do not depend on memory of previous chats/sites.

Selection order:

```text
SEMANTIC ROLE
→ LOCALE-NATURAL ELIGIBLE LABEL POOL
→ AMBIGUITY / LENGTH / DUPLICATE FILTER
→ RANDOM LABEL DRAW
→ HEADER FAMILY ELIGIBILITY FILTER
→ RANDOM HEADER TOPOLOGY DRAW
→ LABEL-FIT / MOBILE / ACCESSIBILITY CHECK
→ REROLL IF NEEDED
→ PERSIST RESULT
```

Do not always choose `About / Game / FAQ / Contact` merely because they are the safest or shortest labels when multiple natural alternatives exist.

### Same-site persistence

An update to the same site keeps the selected header family and public navigation labels unless the user explicitly requests navigation/header regeneration.

Existing user edits in persistent Global Text outrank factory reselection.

### Header composition rule

The main header should remain recognizable and consistent across pages of one site, but its **site-level geometry** is randomly selected from the permanent header family bank after semantic/accessibility/responsive filtering.

Permitted variation includes:
- brand position;
- primary-nav position;
- split vs unified nav grouping;
- CTA presence/position;
- utility/meta rail presence/position;
- single-row vs multi-row structure;
- contained vs edge/full-width shell;
- overlay/solid page state when supported;
- divider/surface treatment;
- mobile transformation family.

Do not vary DOM order in a way that creates contradictory keyboard/screen-reader order merely to look different.

### Label diversity rule

Navigation copy uses role-specific permanent synonym families and locale-natural realization.

For common roles with a healthy language pool, target at least `6` semantically safe eligible variants before random draw; target `8+` where the locale supports it naturally.

If the pool is smaller, preserve meaning rather than invent awkward wording.

No two primary-nav destinations may use the same normalized visible label.

### Same-GEO lexical diversity rule

For multiple unrelated sites in the same locale/GEO, visible primary-navigation wording must not collapse to one habitual set such as `Início | Sobre | Jogo | FAQ | Contacto`.

For every new site derive and persist:

```text
navigation_lexical_profile
domain_lexical_salt = hash(normalized_domain + locale)
menu_lexical_fingerprint
```

Selection seed for each role should incorporate both the fresh site nonce and domain salt:

```text
role_label_seed = hash(navigation_copy_nonce + domain_lexical_salt + semantic_role)
```

The domain salt exists to decorrelate unrelated sites even when no previous-site memory/history is available. It does not replace the fresh random nonce and does not change page semantics.

When several same-locale sites are generated in one batch, perform a **without-replacement assignment** for common roles before individual site copy is locked. While natural candidates remain, avoid reusing the exact same label for `ABOUT_STUDIO`, `GAME_PRODUCT`, `DEVELOPMENT`, `CONTACT` and other high-frequency roles across the batch.

When prior same-locale navigation manifests are available, treat exact recent label reuse as a hard avoid when `>=4` clear alternatives remain, and reject an exact recent `menu_lexical_fingerprint`.

If history is unavailable, do not claim cross-site non-repetition was checked; rely on the permanent native-locale bank + fresh nonce + domain salt + whole-menu fingerprint.

### Naturalness over novelty

The goal is **quiet lexical variation**. Labels must feel like ordinary native navigation, not marketing slogans or thesaurus output.

Prefer:
- short established nouns;
- short natural action phrases;
- locally common studio/product vocabulary;
- clear destination meaning at a glance.

Reject:
- vague one-word labels whose destination is unclear;
- awkward literal translations;
- rare synonyms selected only to be different;
- several long phrase labels in one menu;
- labels that sound more dramatic than the page they open.



## 16.15. UNIVERSAL LOCALE NAVIGATION DIVERSITY POLICY (v4.9.5)

The navigation synonym system is universal across GEOs. The factory must never depend on a Portugal-only, English-only or manually curated single-language dictionary.

Required flow:

```text
GEO + SOURCE + LOCALE
→ RESOLVE REGIONAL LANGUAGE VARIANT
→ NAVIGATION_LOCALE_LEXICON
→ ROLE-SAFE NATIVE CANDIDATE POOLS
→ RANDOM / WITHOUT-REPLACEMENT ASSIGNMENT
→ WHOLE-MENU NATURALNESS + COLLISION QA
→ HEADER FIT QA
→ PERSIST
```

For every new unrelated site, fresh `navigation_copy_nonce` + `domain_lexical_salt` must be used. For same-locale batches, common-role labels are distributed without replacement until a healthy pool is exhausted.

The semantic page identity remains stable regardless of visible wording. `ABOUT_STUDIO` may surface as different native equivalents on different sites, but all variants resolve to the same role/page identity.

Do not use one canonical localized menu vocabulary for all sites in a GEO.

### Multilingual GEO rule
A country/region with several normal website languages does not authorize random language choice. Resolve `locale` from user/source/context before navigation generation.

<!-- BUNDLE-MODULE-END: 01-MASTER-SKILL-v4.5.md -->

---

<!-- BUNDLE-MODULE-START: 12-FACTORY-LEARNING.md -->

# LEGACY MODULE: 12-FACTORY-LEARNING.md

# FACTORY LEARNING & REGRESSION

**Version:** 4.5.0  
**Role:** фабрика не повторює знайдені баги

---

## 1. Principle

Не виправляти одну тему, якщо проблема класова.

Кожен реальний defect перетворюється на system knowledge.

---

## 2. Defect record

Для кожного:

- defect ID;
- screenshot/runtime evidence;
- symptom;
- root cause;
- affected layer;
- systemic fix;
- validator/QA gate;
- regression scenario;
- status.

---

## 3. Уже знайдені класи дефектів

### NAV-001 — stale menu leakage
**Symptom:** нова тема показує menu labels попереднього сайту.  
**Root cause:** залежність від старого WP Menu/location.  
**Rule:** default nav із current manifest + managed page IDs.

---

### PROVISION-001 — pages not created after in-place update
**Symptom:** header links існують, target pages не створилися.  
**Root cause:** provisioning залежав від `after_switch_theme`.  
**Rule:** first-request `init` bootstrap + self-heal + version verification.

---

### URL-001 — query mode used without need
**Symptom:** `?page_id=N` is used even though a cleaner mode is verified working.  
**Root cause:** fallback priority was not respected.  
**Rule:** verify and prefer clean → PATHINFO → query. Query mode is valid only when cleaner modes fail.

---

### PAGECTX-001 — wrong visible page context
**Symptom:** eyebrow/label показує brand/internal ID замість поточної сторінки.  
**Rule:** dynamic page-context integrity.

---

### LEGAL-001 — thin legal content
**Symptom:** Privacy/Terms/Cookies = 3 cards / кілька речень.  
**Rule:** full article generator + GEO/runtime profile.

---

### COOKIE-001 — ugly/generic banner
**Symptom:** generic black rectangle перекриває CTA.  
**Rule:** Design-DNA consent UI + viewport check.

---

### DESIGN-001 — cartoon default
**Symptom:** gaming автоматично отримав childish mascot art.  
**Rule:** Golden gaming family selection before assets.

---

### DESIGN-002 — abstract/cyber drift
**Symptom:** модель вигадала власний tech style замість орієнтації на accepted sites.  
**Rule:** Golden-first design calibration.

---

### DESIGN-003 — excessive empty space
**Symptom:** hero/sections виглядають пустими.  
**Rule:** visual density gate + first viewport screenshot review.

---

### CSS-001 — rigid px sizing
**Symptom:** fixed spacing/type/layout не гнучкі.  
**Rule:** numeric px forbidden; rem/clamp system.

---

## 4. Regression test rule

Кожен closed defect повинен мати сценарій, який можна повторити.

Наприклад PROVISION-001:

1. install old generated theme;
2. activate;
3. upload new version поверх active theme;
4. не deactivate;
5. open frontend;
6. assert all new managed pages exist.

---

## 5. Factory versioning

Не створювати безкінечні дублікати source rules.

Current Project skill-set `01–18` is authoritative; module-local version headers may differ.

Коли правило змінюється:
- оновити тільки відповідний MD;
- за потреби оновити MASTER;
- old contradictory MD прибрати із Sources.

---

## 6. Golden updates

Новий generated site не стає Golden автоматично.

У Golden corpus додавати тільки:
- після human acceptance;
- якщо дизайн справді розширює reference diversity;
- якщо runtime стабільний.

---

## 7. Batch uniqueness

Для batch:
- plan fingerprints before build;
- avoid same hero/nav/section/card/footer combination;
- Golden family можна повторювати;
- exact composition не повторювати.

Uniqueness dimensions:
- hero composition;
- section story arc;
- typography;
- media treatment;
- navigation pattern;
- catalog grammar;
- interaction;
- footer/finale.

---

## 8. Release learning

Після кожного реального WordPress install:
1. записати знайдені defects;
2. визначити class vs one-off;
3. class defect → global update;
4. rerun regression;
5. лише потім наступний production batch.

---

## 9. Never rationalize defects

Не пояснювати слабкий output словами:
- “це minimal”;
- “так і задумано”;
- “технічно все працює”

якщо user screenshot показує очевидну проблему.

Evidence from runtime і human acceptance має пріоритет.


---

### CONTACT-001 — placeholder-looking contact data
**Symptom:** footer/Contact показує `.example`, `000 000 000`, `Rua Exemplo` або інші obvious test values.  
**Root cause:** contact generator не мав synthetic-realism mode.  
**Rule:** `DOMAIN + GEO + TOPIC` must be resolved; generated fields use `SYNTHETIC_GEO_CONTACT`; factory-generated public email MUST be `{locale_natural_role}@DOMAIN`; phone/address follow GEO conventions and avoid obvious placeholders.

---

### CONTENT-001 — thin internal pages
**Symptom:** Home насичена, але domain/About/Contact майже порожні.  
**Rule:** 4–7 meaningful blocks + contextual visuals + related links на ключових сторінках.

---

### VISUAL-001 — insufficient visual recurrence
**Symptom:** hero має картинку, далі майже весь сайт текстовий.  
**Rule:** gaming/editorial target 10–18 assets, 4+ non-hero media moments, 2–4 SVG/background systems.


---

### INPUT-001 — missing domain
**Symptom:** SEO canonical/email/social metadata збираються з temporary host або placeholder domain.  
**Root cause:** DOMAIN не був blocking input.  
**Rule:** `DOMAIN + GEO + TOPIC/NICHE` mandatory before BUILD.

---

### CONTACT-002 — synthetic contact presented as verified legal identity
**Symptom:** generated address/phone shown as registered office, legal controller address або verified hotline.  
**Root cause:** presentation contact і legal identity були одним field class.  
**Rule:** `SYNTHETIC_GEO_CONTACT` окремо від `VERIFIED/OWNER_SUPPLIED`; legal/schema eligibility перевіряється окремо.

---

### VISUAL-002 — generic section imagery
**Symptom:** красиві картинки є, але не відповідають конкретним sections.  
**Root cause:** asset budget рахував кількість, а не semantic fit.  
**Rule:** `SECTION IMAGE MANIFEST` + section intent → subject → prompt → placement mapping.

---

### VISUAL-003 — low-quality generated imagery
**Symptom:** gibberish text, malformed objects, style drift, watermark, stock-like AI look.  
**Root cause:** generation завершувалась без dedicated image QA.  
**Rule:** `15-SECTION-IMAGE-ENGINE.md` + generated-image visual gate + regenerate loop.


---

### URL-002 — PATHINFO selected when clean mode works
**Symptom:** browser shows `/index.php/poradnik/` although `/poradnik/` is verified reachable.  
**Root cause:** fallback selected too early.  
**Systemic fix:** only select PATHINFO after real clean-mode failure.  
**Regression:** on a clean-capable host, assert final state remains `CLEAN_URL_PASS`.

---

### SEOHTML-001 — meaningful images missing ALT
**Symptom:** browser SEO audit reports images without ALT.  
**Root cause:** some shared templates/rendered WordPress markup emitted `<img>` without semantic alt.  
**Systemic fix:** image manifest → semantic alt helper → rendered DOM crawl → zero missing ALT for factory-owned meaningful images.

---

### SEOHTML-002 — images missing TITLE
**Symptom:** browser SEO audit reports most images without TITLE.  
**Root cause:** image semantic profile did not include audit-compatible title attribute.  
**Systemic fix:** every factory-owned meaningful `<img>` receives localized `title`; decorative visuals are moved to CSS/background or explicitly classified.

---

### SEOHTML-003 — links missing TITLE
**Symptom:** browser SEO audit reports factory-owned links without TITLE.  
**Root cause:** visible labels were descriptive, but audit compatibility profile did not generate title attributes.  
**Systemic fix:** link helper/manifest generates localized semantic `title` for internal, external and hash links; runtime count must be zero.

---

### URL-003 — clean slug visible but page returns 404
**Symptom:** `/melhorias/` or similar opens Not Found.  
**Rule:** runtime click-probe of all critical internal links before release.

### SEOHTML-004 — rendered IMG duplicates lost inherited ALT/TITLE
**Symptom:** audit still reports missing attributes on rendered image instances.  
**Rule:** rendered DOM audit, not only attachment/source audit.

### JS-001 — theme-owned console errors
**Symptom:** modal/nav/tabs/consent or theme scripts throw console errors.  
**Rule:** clean-browser console gate and blocking fail on theme-owned errors.

### LAYOUT-001 — oversized heading crushes section balance
**Symptom:** huge headline + tiny image + too much empty space.  
**Rule:** split-layout proportion gate with regenerate/reflow path.

### CONTACT-003 — generated mailbox is off-domain or unnatural
**Symptom:** generated contact email uses a freemail/foreign host, repeats the brand awkwardly, or looks technical/placeholder-like.  
**Rule:** factory-generated primary website email uses a short locale-natural role local-part on the exact site `DOMAIN`, e.g. `kontakt@domain.org`; explicit `OWNER_SUPPLIED` / `VERIFIED` email may override.  
**QA gate:** generated email host mismatch with `DOMAIN` = `FAIL`.  
**Regression:** build a site without owner email and reject `brand.guide@gmail.com`; require a domain mailbox such as `kontakt@domain.tld`.

### TRUST-001 — missing or invalid trust/proof layer
**Symptom:** site feels empty/low-trust or uses the wrong evidence type for its business model.  
**Rule:** every full site needs a trust/proof layer. Independent editorial mode may use disclosed `SYNTHETIC_EDITORIAL_REVIEW` where appropriate; `OFFICIAL_GAME_STUDIO` requires sourced reviews/press or non-testimonial product/development proof and forbids fabricated player/customer quotes.

### CONSENT-001 — cookie UI present but ugly / unbalanced / intrusive
**Symptom:** consent block looks like an afterthought.  
**Rule:** compact designed banner + settings modal + visual QA acceptance.

### IMGQUAL-001 — generated images blurry or artifacted
**Symptom:** visual looks low-quality or contains unwanted baked-in overlays.  
**Rule:** sharpness/clarity gate and mandatory regeneration.


---

### URL-004 — clean-looking links all return raw Apache 404
**Symptom:** `/guia/`, `/melhorias/`, `/faq/` all return server `Not Found`; WordPress 404 template is not reached.  
**Root cause:** factory trusted permalink configuration/capability heuristics instead of a real HTTP probe.  
**Rule:** clean → PATHINFO → query runtime probe; persist first verified mode; never emit unverified pretty links.

### PACKAGE-001 — update ZIP installed as second theme
**Symptom:** user uploads a "fixed" version, but active site still runs the old code.  
**Root cause:** new archive changed root directory from `theme-slug/` to `theme-slug-vX.Y.Z/`.  
**Rule:** theme root slug is immutable for the lifetime of one site; version only changes metadata/code.

### URL-005 — `get_permalink()` generated a 404 route
**Symptom:** page exists in WordPress, but helper returns `/slug/` that Apache cannot route.  
**Root cause:** helper returned `get_permalink()` before verified runtime mode was selected.  
**Rule:** selected URL mode owns link rendering; `get_permalink()` is not authoritative until that mode is verified.


### TYPE-001 — font selected before GEO research
**Symptom:** site uses a generic/trendy font that feels foreign to the locale or renders local diacritics poorly.  
**Root cause:** font family was selected before GEO/locale analysis.  
**Rule:** `GEO → web typography research → locale specimen → shortlist → visual comparison → final font selection`.

### TYPE-002 — heading looks good but body reading is tiring
**Symptom:** first viewport feels stylish, while article/legal/internal pages are uncomfortable to read.  
**Root cause:** selection optimized for display aesthetics only.  
**Rule:** body readability is an independent blocking gate; test several real localized paragraphs.

### TYPE-003 — locale glyphs fall back to another family
**Symptom:** accented characters or unsupported glyphs look visually inconsistent.  
**Root cause:** character coverage was not verified.  
**Rule:** verify locale-specific glyph coverage from authoritative/provider sources and rendered specimen before BUILD.


### IMGQUAL-002 — unintended white border/matte in published image
**Symptom:** a section image shows a thin white frame, collage divider, export margin or white halo that was not part of the design.  
**Root cause:** generated multi-panel output or downloaded source was cropped/exported without edge inspection.  
**Rule:** four-edge inspection + no unintended matte/gutter + repair/regenerate before publish.  
**Regression:** test cropped collage panels and alpha images on light/dark section backgrounds.

### IMGSRC-001 — factory uses only generated imagery even when real reusable imagery fits better
**Symptom:** site feels synthetic/repetitive and misses useful real-world visual context.  
**Root cause:** asset planning had one global source mode.  
**Rule:** choose source mode per section: generated, verified reusable web, owner supplied, SVG/CSS.

### IMGSRC-002 — publicly accessible image treated as automatically reusable
**Symptom:** external image was copied into production without a rights/provenance record.  
**Root cause:** public visibility was confused with reuse permission.  
**Rule:** non-generated external assets require a publishable rights state and provenance manifest.

### IMGMETA-001 — raw downloaded image shipped with unnecessary metadata
**Symptom:** production asset retains camera/location/private metadata or oversized embedded payloads.  
**Root cause:** source asset bypassed sanitization.  
**Rule:** normalize orientation → strip nonessential metadata → optimize/convert → verify. Required attribution remains recorded outside metadata.


### COLOR-001 — consecutive sites reuse the same color world
**Symptom:** two different sites feel visually related because both use the same dominant background, text and accent families.  
**Root cause:** factory reused a comfortable/default palette instead of comparing against prior projects.  
**Rule:** create `SITE COLOR FINGERPRINT` before Design DNA lock and compare against previous factory sites.  
**QA gate:** cross-site color uniqueness visual gate; at least 3 major fingerprint dimensions materially differ unless owner brand constraints apply.  
**Regression:** generate two consecutive gaming sites for the same GEO and assert that dominant hue family + accent family do not both repeat.

### COLOR-002 — HEX values changed but palette still looks the same
**Symptom:** colors are technically different, but the site still looks like the previous site's palette.  
**Root cause:** uniqueness was checked by exact HEX only rather than hue family, temperature, polarity and accent relationship.  
**Rule:** compare semantic palette roles and perceptual color relationships, not only raw codes.  
**Regression:** reject a candidate palette that preserves the same cream/dark-teal/coral role pattern with slightly shifted values.

### COLOR-003 — source screenshot locks the whole site palette
**Symptom:** multiple sites based on colorful apps converge on nearly identical website palettes because source colors were copied too literally.  
**Root cause:** source was treated as a palette mandate instead of visual intelligence.  
**Rule:** source palette may be rotated, reweighted, desaturated, darkened/lightened or moved to accents unless owner brand rules require fidelity.  
**Regression:** source-derived palette must still pass cross-site uniqueness before BUILD.


### TEXTSRC-001 — user must edit PHP/DB to change site wording
**Symptom:** changing one visible phrase requires template or WordPress editor changes.  
**Root cause:** copy is scattered across templates/database instead of one runtime source.  
**Rule:** all factory-owned public frontend text resolves from persistent `global-text.json`.  
**QA gate:** Global Text coverage = 100%; hardcoded public-copy scan = 0.  
**Regression:** change one hero key through filesystem and assert the frontend updates without rebuild/reprovision.

### TEXTSRC-002 — theme update destroys manual text edits
**Symptom:** user edits text in FastPanel, then a theme ZIP update restores factory wording.  
**Root cause:** editable text file lived only inside replaceable theme files.  
**Rule:** authoritative `global-text.json` lives under persistent uploads path; theme seed only merges missing keys.  
**Regression:** edit value → update same stable-root theme → assert edited value survives.

### TEXTSRC-003 — invalid JSON breaks production
**Symptom:** one comma/quote error causes fatal/blank site.  
**Root cause:** runtime parses editable file without last-known-good protection.  
**Rule:** validate + last-known-good fallback + admin diagnostic + self-recovery.  
**Regression:** intentionally corrupt JSON and assert public frontend still renders previous valid text.

### TEXTSRC-004 — text edit does not appear because content was copied into wp_post
**Symptom:** `global-text.json` changes but public page still shows old database body.  
**Root cause:** Global Text was used only at provisioning time.  
**Rule:** public page/head/component text is resolved at render time from Global Text.  
**Regression:** edit JSON after provisioning and assert next uncached request changes without DB sync.

### TEXTSRC-005 — manual copy edit breaks layout
**Symptom:** longer FastPanel text overlaps media/nav/buttons.  
**Root cause:** design was fitted to exact generated strings.  
**Rule:** Global Text edit resilience visual gate.  
**Regression:** lengthen representative heading/nav/CTA strings and rerun responsive QA.

---

### FOOTER-001 — site ends without conventional copyright bar
**Symptom:** footer contains navigation/cards but the page ends abruptly without the familiar copyright / rights-reserved baseline.  
**Root cause:** footer architecture covered links/contact but not the final global bottom bar.  
**Rule:** every full site gets a localized footer bottom bar: `© {year} {brand}. {all_rights_reserved}` from Global Text.  
**Regression:** render Home + internal + legal page and assert bottom bar presence and current-year interpolation.

### IMGSRC-003 — web image exposes unnecessary source caption/link
**Symptom:** selected reusable image is followed by a visible source description or link back to the image page even though the licence does not require public attribution.  
**Root cause:** internal provenance was incorrectly rendered as public content.  
**Rule:** provenance stays internal; public source caption/link defaults to none. Required legal attribution remains mandatory, otherwise prefer clean reusable assets.  
**Regression:** ingest attribution-free reusable image and assert no public source caption/link while provenance remains recorded.

### IMGSTYLE-001 — generated raster looks childish/cartoon/toy-like
**Symptom:** major hero/section visuals resemble children's illustrations, mascots, plastic 3D or cheap AI/game-promo art.  
**Root cause:** prompt only said `not cartoon` without defining a strong positive rendering target.  
**Rule:** default raster art direction = `PHOTOREAL_EDITORIAL / COMMERCIAL_PHOTOGRAPHY / CINEMATIC_REALISM`; illustration requires explicit justification.  
**Regression:** generate representative hero + 3 section visuals and reject any set that reads as cartoon/toy/flat illustration instead of professional custom image-making.



### LAYOUT-005 — repeated section skeleton across one page
**Symptom:** different sections look like the same component with only text/image swapped.  
**Root cause:** section intent was mapped to one comfortable split/card template.  
**Rule:** run `18-SECTION-COMPOSITION-ENGINE.md`; exact section composition fingerprint repeated on the same page = 0 by default.  
**QA gate:** adjacent-section distance + same-page fingerprint audit.  
**Regression:** generate a rich Home with 7+ sections and assert no exact composition fingerprint repeats.

### LAYOUT-002 — every site has the same homepage grammar
**Symptom:** different brands/topics still produce hero → cards → split → FAQ → CTA with visibly similar geometry.  
**Root cause:** Golden family was treated as a fixed section template instead of a maturity reference.  
**Rule:** store `SITE COMPOSITION FINGERPRINT`, compare to recent factory outputs when available, and mutate high-impact dimensions when similarity is too high.  
**Regression:** generate consecutive sites in the same niche and assert hero family + dominant section family + CTA family do not all repeat.

### LAYOUT-003 — randomization creates incoherent UX
**Symptom:** layouts are different but reading order, hierarchy or mobile behavior feels arbitrary.  
**Root cause:** pure random choice was used without semantic filtering.  
**Rule:** randomness applies only after content-fit/accessibility/responsive/performance filters; semantic intent always outranks novelty.  
**Regression:** candidate patterns that hide critical content, break reading order or require unsupported interaction must be excluded before stochastic selection.

### LAYOUT-004 — internal pages clone Home components
**Symptom:** About, guide and Contact reuse the same hero/split/card sequence as Home.  
**Root cause:** section components were selected globally instead of per page purpose.  
**Rule:** every managed page receives its own `PAGE COMPOSITION FINGERPRINT`; key pages must have distinct page grammar while preserving shared Design DNA.  
**Regression:** compare Home + two key internal pages and reject identical visible skeleton sequences.



---

### LAYOUT-006 — sparse section stretched into a giant empty composition
**Symptom:** eyebrow, large H2 and body copy sit far apart with a large unused field between them.  
**Root cause:** section family was selected for novelty without coupling typography and spacing to actual content volume.  
**Rule:** non-hero sections must pass section-cohesion and empty-space review; reduce type/spacing or change family when the content cannot support the canvas.  
**QA gate:** no purposeless major blank region; heading/body/label read as one composition in wireframe view.  
**Regression:** render a section with short copy at wide desktop and reject it when the text occupies isolated islands separated by unused space.

### IMGREUSE-001 — one generated collage becomes many "different" section images
**Symptom:** files have different crops but users perceive the same board/scene repeatedly across the site.  
**Root cause:** one composite/contact-sheet generation was sliced into multiple major assets.  
**Rule:** one major section receives one independently conceived major visual by default; crops/derivatives of one source count as one visual source.  
**QA gate:** major asset source IDs/hashes are unique by default and visual near-duplicate review passes.  
**Regression:** crop four quadrants from one composite image and assert the build rejects them as four unique major media assets.

### IMGREUSE-002 — exact major raster reused in multiple sections
**Symptom:** hero or section image reappears later as another content visual.  
**Root cause:** asset reuse was optimized for convenience instead of section specificity.  
**Rule:** exact major raster reuse across major sections = 0 by default; hero reuse = 0.  
**QA gate:** major raster render/source reuse count passes allowlist.  
**Regression:** intentionally assign one hero asset to a second major section and require FIX_REQUIRED.

### FOOTER-002 — every generated site ends with the same footer
**Symptom:** brand, nav, contact and legal columns appear in the same order and proportions across unrelated sites.  
**Root cause:** footer was treated as fixed utility markup outside the composition engine.  
**Rule:** footer receives its own seeded composition family/fingerprint; column order, widths, grouping, polarity and bottom-bar arrangement may vary while meaning/accessibility remain stable.  
**QA gate:** cross-site footer fingerprint comparison when history is available.  
**Regression:** create two unrelated sites with identical footer geometry and require at least two high-impact footer mutations.



### CONTACT-004 — resolved phone/address exist in data but are visually absent
**Symptom:** Contact looks incomplete even though email, phone and postal address exist in the Contact Profile.  
**Root cause:** fields were stored in JSON/runtime or footer only, while the visible Contact entry point showed generic copy.  
**Rule:** when public contact fields are resolved, Contact must surface email + phone + address together in the first meaningful contact viewport or its immediate first content block.  
**QA gate:** desktop + mobile screenshot confirms all resolved fields are readable; missing one resolved field = FIX_REQUIRED.  
**Regression:** provision a complete synthetic Contact Profile and reject a Contact page that visibly shows only email or only a generic CTA.

### CONTACT-005 — website/support relationship is ambiguous
**Symptom:** users cannot tell whether game support is first-party studio support or an unrelated developer destination.  
**Root cause:** support relationship was hard-coded as always third-party or always first-party.  
**Rule:** primary website mailbox uses locale-natural public-contact naming; support presentation follows `developer_relationship_status`. Verified same-studio support may be first-party; unresolved/third-party support must remain visibly separate.  
**QA gate:** support ownership labels must match the resolved studio/developer relationship.  
**Regression:** test both a verified same-studio case and a mismatched-source-developer case; require different support presentation.

### LAYOUT-007 — formally valid typography still creates an oversized empty section
**Symptom:** heading scale and padding pass CSS limits but the screenshot still shows large blank regions or disconnected text islands.  
**Root cause:** numeric type/spacing envelopes were checked without screenshot occupancy/cohesion review.  
**Rule:** content density is judged from rendered composition; sparse non-hero sections must reduce type/padding or change pattern family.  
**QA gate:** at 1440px-class desktop, purposeless dominant blank field or isolated label/title/body clusters = FIX_REQUIRED.  
**Regression:** render short copy in a wide section and reject it when empty canvas visually dominates the useful content.

### SEO-001 — Publisher exists in schema but browser audit reports missing
**Symptom:** JSON-LD has an Organization/publisher relationship while SEO tools still show `Publisher is missing`.  
**Root cause:** schema presence was treated as equivalent to browser-readable metadata.  
**Rule:** Native Factory SEO emits explicit publisher metadata in addition to coherent structured data.  
**QA gate:** browser SEO parity must resolve Author + Publisher as non-empty on indexable editorial pages.  
**Regression:** remove `<meta name="publisher">` while keeping Organization JSON-LD and require FAIL.

### SEO-002 — duplicate robots owners produce partial or contradictory state
**Symptom:** audit shows only `max-image-preview:large` or another subset although factory code outputs a fuller robots string.  
**Root cause:** WordPress core/plugin and factory both emitted robots metadata.  
**Rule:** one SEO owner controls robots; Native Factory SEO disables/adapts duplicate core/plugin output before emitting its coherent state.  
**QA gate:** exactly one public robots meta with expected complete directives.  
**Regression:** render core `wp_robots` plus factory robots and require FAIL.

### SEO-003 — metadata exists but descriptions are underdeveloped
**Symptom:** Description is technically present yet too short/generic to express page intent.  
**Root cause:** field-presence QA replaced content-quality QA.  
**Rule:** normal indexable content pages target approximately 135–160 natural characters; materially shorter copy needs page-specific justification.  
**QA gate:** key-page descriptions under about 120 characters are reviewed and normally rejected when intent can be expressed naturally.  
**Regression:** seed generic 50–90 character descriptions across key pages and require rewrite.

### IMGREUSE-003 — repeated major SVG/diagram across internal pages
**Symptom:** raster hashes are unique, but the same diagram/SVG is reused as a major visual on several pages.  
**Root cause:** uniqueness audit covered raster lineage only.  
**Rule:** major-visible uniqueness applies to raster, SVG and generated diagrams; repeated decorative systems remain exempt.  
**QA gate:** unexplained major asset ID/visual-signature reuse across unrelated sections/pages = FIX_REQUIRED.  
**Regression:** assign one major SVG to Guide, About and Terms and require replacement with page-specific visuals.



### LAYOUT-008 — comfortable-family gravity makes many sites look alike
**Symptom:** a large pattern pool exists, yet the factory repeatedly selects the same small subset of splits, card grids and centered statements.  
**Root cause:** candidate scoring rewards familiar high-fit patterns without sufficient recency/novelty penalty.  
**Rule:** module 18 applies family-recency, topology-recency and sequence-recency penalties before seeded weighted selection.  
**QA gate:** recent-site usage distribution and page fingerprint review.  
**Regression:** simulate 8+ unrelated sites and reject a run where the same small group dominates despite equally valid alternatives.

### LAYOUT-009 — different sections, same page rhythm
**Symptom:** individual section IDs differ but pages still read as hero → cards → split → FAQ → CTA.  
**Root cause:** sections were varied independently without a page-level rhythm grammar.  
**Rule:** every key page receives a `PAGE RHYTHM RECIPE` and 2-section/3-section sequence signatures are compared against recent pages/sites.  
**Regression:** reject a new Home whose macro sequence n-grams substantially reproduce a recent unrelated Home without semantic necessity.

### LAYOUT-010 — cosmetic modifiers masquerade as structural novelty
**Symptom:** alignment, color or image side changes, but wireframe geometry remains effectively identical.  
**Root cause:** novelty score overweights low-impact modifiers.  
**Rule:** macro skeleton/topology/media dominance count more than palette, copy alignment or minor card styling.  
**QA gate:** grayscale/wireframe comparison must show meaningful structural difference.  
**Regression:** flip image left/right and change surface color on an otherwise identical section; novelty must remain low.

### IMGSTYLE-002 — premium site receives cute/toy/childish generated scenes
**Symptom:** otherwise mature editorial site contains plastic 3D, mascot-like, toy/diorama or children's-book imagery.  
**Root cause:** image generation lacked an explicit adult-premium quality tier.  
**Rule:** general-audience visual-rich projects default to `ADULT_PREMIUM_EDITORIAL`; playful/child-oriented styling requires source/audience justification or explicit user direction.  
**Regression:** hero + representative section set must fail if major imagery reads as cheap game-ad CGI, childish illustration or toy photography.

### IMGSTYLE-003 — website/mockup generation is shipped as a section image
**Symptom:** generated asset contains an entire webpage, UI chrome, labels or fake marketing layout baked into the raster.  
**Root cause:** image-generation output was accepted because it looked polished, despite failing the requested scene role.  
**Rule:** major scene assets must be single-scene media unless the manifest explicitly requests a UI/device composition; webpage/mockup outputs are `REGENERATE`.  
**Regression:** generated website screenshot for a hero-scene request must be rejected.

### SVG-001 — bespoke visual opportunity replaced by generic icon/clipart
**Symptom:** process/economy/route/mechanics sections use a tiny generic icon where a useful diagram could explain the content.  
**Root cause:** SVG was treated as decoration rather than a first-class editorial medium.  
**Rule:** evaluate original diagram/line-art families for structured concepts; major SVG must have a semantic role and site-specific geometry.  
**Regression:** a complex upgrade/economy section with only generic icons fails the visual-depth review.

### SVG-002 — same major SVG grammar repeats across sites
**Symptom:** filenames differ but the same orbit, three-node flow or boxed diagram composition appears repeatedly.  
**Root cause:** SVG uniqueness tracked only exact files.  
**Rule:** major SVGs receive visual/topology signatures and recent-history penalties just like raster media.  
**Regression:** recoloring the same diagram topology does not count as a new major visual.

### BG-001 — every section uses flat solid fills
**Symptom:** layouts vary but the site still feels factory-made because sections alternate only plain light/dark surfaces.  
**Root cause:** backgrounds were not treated as an authored visual layer.  
**Rule:** visual-rich sites evaluate the Section Background Engine and use distinctive but restrained background treatments where they materially improve hierarchy/atmosphere.  
**Regression:** rich gaming/editorial Home with zero meaningful background treatment receives visual warning/fix unless Design DNA intentionally calls for strict minimalism.

### BG-002 — decorative background competes with content
**Symptom:** line art, texture or illustrated background hurts contrast, readability or mobile clarity.  
**Root cause:** background novelty was prioritized over content hierarchy.  
**Rule:** every background family declares contrast-safe zones, intensity, mobile simplification and reduced-motion behavior.  
**Regression:** background behind body copy failing readability or collapsing poorly on mobile = FAIL.

### VISMIX-001 — site relies on one visual medium everywhere
**Symptom:** every section is either another photo, another card grid or another generic SVG.  
**Root cause:** asset planning did not define a visual-medium rhythm.  
**Rule:** visual-rich sites create a `VISUAL MEDIUM RHYTHM` mixing raster, bespoke SVG/diagram, background illustration and clean text-led sections according to semantics.  
**Regression:** reject monotonous Home where all meaningful sections use the same visual medium despite valid alternatives.



## v4.5.0 regression additions — rich content + live section diversity

### CONTENT-006 — page technically complete but editorially thin
**Symptom:** page has several sections but only a few short sentences and feels like an expanded landing page.  
**Root cause:** section count was used as a proxy for information depth.  
**Rule:** use `CONTENT DEPTH MANIFEST`; require substantive information gain per section and page-type depth envelope.  
**Gate:** rich informational/domain pages that remain materially thin without source limitation justification = FIX_REQUIRED.

### CONTENT-007 — word-count padding / paraphrase loop
**Symptom:** content is longer but repeats the same idea with different wording.  
**Root cause:** word target treated as a quota.  
**Rule:** every meaningful section declares a distinct `information_role`; repeated semantic filler is removed.  
**Gate:** high semantic duplication or no new information across consecutive sections = FAIL.

### CONTENT-008 — invented feature used to make page longer
**Symptom:** extra depth introduces unsupported game/app/service capabilities.  
**Root cause:** source limitations were solved by fabrication.  
**Rule:** expand through explanation, examples, caveats, comparisons and practical guidance; never fabricate product facts.  
**Gate:** unsupported factual claim = FAIL.

### RESEARCH-001 — no current UI/UX research before composition
**Symptom:** factory keeps recycling its internal comfortable patterns after many sites.  
**Root cause:** composition engine is closed over its own history.  
**Rule:** when web is available, create `LIVE UIUX RESEARCH MANIFEST` before final page grammar.  
**Gate:** full rich BUILD with web access and no research artifact = FIX_REQUIRED.

### RESEARCH-002 — reference cloning
**Symptom:** new page is recognizably derived from one external site, including distinctive sequence/geometry.  
**Root cause:** research example was treated as a template.  
**Rule:** abstract traits only; recombine across independent dimensions and multiple references.  
**Gate:** recognizable 1:1 or near-1:1 reference composition = FAIL.

### LAYOUT-011 — modifier stack reuse
**Symptom:** macro IDs differ but shell, content flow, framing, density and transition remain effectively the same.  
**Root cause:** variation happened only at macro-family name level.  
**Rule:** every section records independent modifier stack; exact/near-exact stack recurrence is penalized.  
**Gate:** repeated modifier stack across adjacent/unrelated major sections without reason = FAIL.

### LAYOUT-012 — grayscale/wireframe clone
**Symptom:** sites appear different in color/imagery but become nearly identical when viewed as grayscale blocks.  
**Root cause:** cosmetic variation substituted for structural variation.  
**Rule:** compare page silhouette/wireframe fingerprint; mutate high-impact layout dimensions before release.  
**Gate:** visually obvious structural clone of recent unrelated site = FAIL.

### LAYOUT-013 — empty decorative stage
**Symptom:** a large bordered/colored visual panel has no meaningful content or media and reads as unfinished space.  
**Root cause:** a section family reserved a media/data slot that was never populated.  
**Rule:** every large stage must contain meaningful media/data/diagram/content, or the composition must collapse/reselect.  
**Gate:** large empty framed field without declared atmospheric function = FAIL.



### INTERACT-001 — decorative interaction with no information value
**Regression:** slider/tabs/accordion added only to make the site feel interactive.  
**Rule:** every interaction must improve discovery, comparison, sequencing, optional-detail access or media inspection.  
**Gate:** no clear semantic benefit = remove or redesign.

### INTERACT-002 — autoplay carousel steals control
**Regression:** carousel advances automatically and disrupts reading.  
**Rule:** autoplay is off by default; if exceptionally justified, pause/stop controls and reduced-motion handling are mandatory.  
**Gate:** uncontrolled autoplay = FAIL.

### INTERACT-003 — inaccessible tabs / slider controls
**Regression:** click-only tabs/carousel without keyboard, focus or ARIA state.  
**Rule:** use button semantics, visible focus, keyboard navigation and coherent ARIA/state ownership.  
**Gate:** inaccessible interaction = FAIL.

### INTERACT-004 — JS-only essential content
**Regression:** content is absent until JS creates it.  
**Rule:** essential copy/media/navigation must exist in readable HTML/static fallback.  
**Gate:** JS failure hides essential content = FAIL.

### INTERACT-005 — same interaction pattern dominates site
**Regression:** multiple pages repeat the same slider/cards/tabs geometry.  
**Rule:** interaction family and surrounding macro geometry participate in recent-history penalties and page fingerprints.  
**Gate:** interaction repetition makes page silhouettes recognizably templated = FIX_REQUIRED.

### INTERACT-006 — mobile interaction is desktop squeezed down
**Regression:** tabs/rails/sliders overflow or become unusable on touch.  
**Rule:** declare a mobile transformation such as snap rail, accordion, featured-list or static chapters.  
**Gate:** no intentional touch/mobile behavior = FAIL.

### HOVER-001 — hover-only information
**Regression:** important label/action appears only on mouse hover.  
**Rule:** information/action must remain discoverable for keyboard/touch users.  
**Gate:** hover is required to understand/use the component = FAIL.

### HOVER-002 — excessive hover motion
**Regression:** cards tilt/zoom/glow aggressively across most of the page.  
**Rule:** hover is restrained, hierarchy-aware and disabled/simplified for reduced motion/touch where needed.  
**Gate:** visual instability or reading distraction = FAIL.

### HOVER-003 — repeated generic lift-shadow effect
**Regression:** every card uses identical translateY + shadow hover across sites.  
**Rule:** choose hover/focus family by component role and penalize recent repeated signatures.  
**Gate:** generic hover signature dominates = FIX_REQUIRED.

### MOTION-001 — motion without reduced-motion fallback
**Regression:** reveal/parallax/progress animation ignores user preference.  
**Rule:** meaningful motion has a static or near-static `prefers-reduced-motion` behavior.  
**Gate:** missing fallback = FAIL.

### MOTION-002 — scroll-jacking or forced narrative
**Regression:** interaction captures scroll or blocks natural page navigation.  
**Rule:** sticky/progress effects enhance normal scrolling; they do not replace it.  
**Gate:** scroll-jacking = FAIL.



### LAYOUT-014 — different IDs still look like the same section
**Symptom:** Hero/sections have different family IDs but the visible wireframe is still the same split, card grid or centered stage.  
**Root cause:** diversity was measured by labels and soft novelty scores instead of hard structural distance.  
**Rule:** HARD DIVERSITY MODE is mandatory for new unrelated full-site BUILDs; near-identical structural signatures are one visual family regardless of ID.  
**Gate:** structural-distance threshold failure = reroll/mutate, not warning.  
**Regression:** give the selector 12 differently named split variants plus 8 materially different topologies; repeated split selection must be rejected.

### LAYOUT-015 — semantic rank #1 defeats randomness
**Symptom:** the same safe Hero/feature family keeps winning because it has the highest semantic score.  
**Root cause:** weighted ranking remained the final selector.  
**Rule:** scores establish eligibility; final choice is seeded random at topology-cluster level, then random within the eligible cluster.  
**Gate:** when >= 6 distant eligible candidates exist, deterministic top-1 selection is `FAIL`.  
**Regression:** run the same semantic brief with different site nonces and require materially different topology selections.

### LAYOUT-016 — cross-site Hero/Footer repetition
**Symptom:** unrelated sites repeatedly open and close with recognizably similar silhouettes.  
**Root cause:** recent-history penalty was soft.  
**Rule:** hard recent-role exclusion windows for Hero/Footer/CTA/FAQ/Process when alternatives exist.  
**Gate:** new Hero below required distance from recent available Heroes = reroll.  
**Regression:** attempt to reuse a recent Hero cluster while 4+ distant clusters are valid and require rejection.

### LAYOUT-017 — all mobile layouts collapse to one stack
**Symptom:** desktop pages differ, but 320–480px renders become the same text/image vertical sequence.  
**Root cause:** mobile was treated only as collapse behavior.  
**Rule:** mobile transformation participates in structural fingerprint and hard distance.  
**Gate:** repeated identical mobile transformation across most major sections without semantic need = `FIX_REQUIRED`.  
**Regression:** render a 7-section Home and require multiple intentional mobile transformation families with zero overflow.

### LAYOUT-018 — no distant candidate accepted as excuse for reuse
**Symptom:** selector falls back to a familiar layout when the pool has no sufficiently distant candidate.  
**Root cause:** no new-grammar escape hatch.  
**Rule:** synthesize/mutate a new grammar from compatible underused dimensions and rerun QA.  
**Gate:** `NO_DISTANT_CANDIDATE` may increase build time but may not silently lower the diversity threshold.  
**Regression:** constrain a role to similar candidates and require new-grammar generation instead of clone acceptance.



### LAYOUT-018 — Home is diverse but internal pages are cloned
**Symptom:** Home uses varied layouts, while About / Contact / Guide / FAQ repeat one shared visible skeleton with different text.  
**Root cause:** Hard Diversity was applied only to Home or page composition inherited a common renderer.  
**Rule:** every managed page receives an independent `page_composition_nonce`, random-first role-scoped layout selection, and cross-page silhouette comparison.  
**Gate:** repeated key-page skeleton or identical opening/sequence without semantic necessity = `FIX_REQUIRED`.  
**Regression:** generate Home + About + Contact + two domain pages and reject if internal pages remain recognizable as one template after neutralizing color/type/images.

### LAYOUT-019 — independent desktop pages collapse to one mobile template
**Symptom:** desktop pages differ, but mobile versions all become intro → cards → text → accordion → CTA.  
**Root cause:** one universal mobile collapse strategy is applied site-wide.  
**Rule:** every page records a mobile rhythm signature and chooses compatible mobile transformations per section/page grammar.  
**Gate:** cross-page mobile silhouettes that are materially identical despite available alternatives = `FIX_REQUIRED`.  
**Regression:** compare Home + About + Guide + Contact at 20rem–30rem; require distinct page rhythm while keeping horizontal overflow at zero.



### CONTACT-006 — generated public email host differs from site domain
**Symptom:** site domain is `example.org`, but generated Contact/footer/legal use `name@gmail.com`, `name@outlook.com` or another host.  
**Root cause:** legacy freemail fallback was allowed for synthetic contacts.  
**Rule:** when no explicit owner/verified email is supplied, factory-generated primary website email MUST use the exact canonical site `DOMAIN`: `{locale_natural_role}@{DOMAIN}`.  
**Gate:** `generated_email_host == DOMAIN` and `generated_email_localpart` is locale-natural/non-placeholder.  
**Regression:** for `DOMAIN=wonparyn.org`, reject generated `wonparyn.guide@gmail.com`; accept a role mailbox such as `kontakt@wonparyn.org` while keeping status `SYNTHETIC_GEO_CONTACT` until owner verification.



### BIZMODEL-001 — official studio site drifts into independent editorial portal
**Symptom:** Home markets the game, but About/FAQ/footer/SEO describe an independent guide/editorial project.  
**Root cause:** business model was treated as page copy instead of a site-wide invariant.  
**Rule:** `BUSINESS_MODEL_PROFILE` propagates to every public page, metadata surface and support route.  
**Gate:** mixed creator/editorial-owner voice = `FIX_REQUIRED`.  
**Regression:** render Home + About + Product + Contact + footer and require one coherent studio/product relationship.

### BIZMODEL-002 — fabricated `we created this game` ownership claim
**Symptom:** the site says `our game` even though the source names an unrelated developer and the owner never confirmed a relationship.  
**Root cause:** desired marketing persona was mistaken for factual ownership evidence.  
**Rule:** first-person creator claims require `OWNER_SUPPLIED_DEVELOPER`, `VERIFIED_DEVELOPER` or explicit owner-supplied brand relationship.  
**Gate:** unresolved/conflicting developer relation + creator claim = `FAIL`.  
**Regression:** source developer differs from domain brand; reject `we developed` until relationship confirmation is supplied.

### BIZMODEL-003 — domain brand is presented as a verified legal company
**Symptom:** domain-derived studio name is described as a registered company/operator without owner data.  
**Root cause:** display brand and legal identity were conflated.  
**Rule:** domain may define studio display brand; legal company identity remains `OWNER_SUPPLIED/VERIFIED` only.  
**Gate:** synthetic display brand used as legal entity = `FAIL`.

### BIZMODEL-004 — official studio site uses fabricated player testimonials
**Symptom:** synthetic editorial quotes appear as trust proof on the developer's own commercial site.  
**Root cause:** old mandatory-review rule ignored business model.  
**Rule:** `OFFICIAL_GAME_STUDIO` uses sourced reviews/press or non-testimonial product/development proof.  
**Gate:** synthetic player/customer testimonial in official-studio mode = `FAIL`.



### BIZMODEL-005 — About page says almost nothing about the studio/game relationship
**Symptom:** About is generic mission text and does not clearly explain who the studio is, what game it created, how the product relates to the brand, or where the visitor should go next.  
**Root cause:** About was treated as boilerplate trust copy rather than a core business page.  
**Rule:** official-studio About must cover studio identity + game relationship + truthful creative/product approach + product/support continuation.  
**Gate:** creator relationship is resolved but About lacks a clear game/studio connection = `FIX_REQUIRED`.  
**Regression:** generate an official-studio site and reject an About page that could belong to any unrelated company after removing the brand name.

### BIZMODEL-006 — development pages are generic game guides instead of creator-side topics
**Symptom:** internal pages explain gameplay only from the player's outside perspective and never express the product/development story.  
**Root cause:** old guide architecture survived after switching to `OFFICIAL_GAME_STUDIO`.  
**Rule:** key domain pages must receive explicit studio/product/development `page_business_role` and, when evidence permits, creator-side context.  
**Gate:** rich official-studio site with no meaningful development/process topic coverage = `FIX_REQUIRED`.  
**Regression:** compare Game, Mechanics, Development and About; require distinct creator/product jobs rather than four generic guides.

### BIZMODEL-007 — fabricated motivation or chronology is written as first-person history
**Symptom:** copy says `we wanted`, `we first tried`, `our testers found` or similar without owner/source evidence.  
**Root cause:** the model inferred creator intent from observed game features.  
**Rule:** creator motive/history uses the Development-story truth ladder; unsupported historical intent is omitted or explicitly requested from owner.  
**Gate:** `UNSUPPORTED_DO_NOT_PUBLISH` creator-history statement in public copy = `FAIL`.  
**Regression:** source confirms a mechanic but not why it was chosen; allow mechanic explanation, reject invented first-person motivation.


### NAV-001 — every site uses the same header geometry
**Symptom:** brand-left + nav-center/right + CTA-right repeats as the visible shell across unrelated sites.  
**Root cause:** header was treated as fixed utility chrome outside the composition engine.  
**Rule:** new sites select a header topology from the permanent header family bank using `header_composition_nonce` after accessibility/responsive filtering.  
**Gate:** healthy eligible pool + deterministic same family for different nonces = `FIX_REQUIRED`.  
**Regression:** evaluate several synthetic nonces against one site spec and require more than one eligible header family to be selected.

### NAV-002 — navigation labels always use canonical defaults
**Symptom:** every site shows the same `Home / About / Game / FAQ / Contact` wording even when natural alternatives exist.  
**Root cause:** semantic page role and visible nav label were conflated.  
**Rule:** stable `page_key` maps to a locale-aware synonym pool; visible label is randomly selected from the eligible pool and persisted.  
**Gate:** common-role eligible pool >= 4 but selector ignores nonce and always returns one default = `FAIL`.  
**Regression:** run multiple fixed nonces and assert label variation while destination IDs remain identical.

### NAV-003 — creative synonym changes page meaning
**Symptom:** an About page is labelled `News`, Support becomes `Contact`, or a process page receives a vague marketing phrase that does not identify its destination.  
**Root cause:** novelty outranked semantic clarity.  
**Rule:** randomization happens only inside the exact semantic-role pool after ambiguity filtering.  
**Gate:** `nav_label_semantic_match != PASS` = `FAIL`.  
**Regression:** inject an out-of-role candidate and assert it is filtered before random draw.

### NAV-004 — same-site update reshuffles the header or menu copy
**Symptom:** theme update unexpectedly changes `Our Studio` to `Who We Are` or moves the navigation to a different topology.  
**Root cause:** nonce/selection manifest was regenerated instead of persisted.  
**Rule:** same-site update preserves `header_composition_nonce`, `navigation_copy_nonce`, selected header family and existing Global Text labels unless explicit regeneration is requested.  
**Gate:** unchanged site + ordinary update + changed header/nav selection = `FAIL`.  
**Regression:** update the same theme package twice and compare the persisted manifests/labels.

### NAV-005 — nav label is used as slug/H1/SEO identity automatically
**Symptom:** changing `About` to `Our Studio` unexpectedly changes canonical URL, page ID, H1 or SEO title.  
**Root cause:** presentation label was reused as the machine/content identity.  
**Rule:** `nav_label`, `page_display_title`, `seo_title` and `canonical_slug` are separate fields.  
**Gate:** editing navigation copy changes canonical/page identity without an explicit migration = `FAIL`.  
**Regression:** change only `navigation.about` in Global Text and assert URL/page ID/SEO profile remain stable.

### NAV-006 — random labels collide or break the header
**Symptom:** two menu items share the same wording, labels wrap awkwardly, CTA overlaps, or mobile menu overflows.  
**Root cause:** random copy was selected without whole-menu fit validation.  
**Rule:** perform normalized-label collision + desktop/mobile fit checks after selection; reroll labels/header family before release.  
**Gate:** duplicate primary label, clipped label, header horizontal overflow or offscreen action = `FAIL`.  
**Regression:** test long locale-natural variants at representative widths and require a valid reroll/transform.


### NAV-007 — same-GEO sites reuse the same visible menu vocabulary
**Symptom:** five PT-PT sites have different layouts but all show nearly the same `Início / Sobre / Jogo / FAQ / Contacto` menu.  
**Root cause:** synonym support existed, but selection did not enforce lexical diversity across a same-locale batch/history.  
**Rule:** use native-locale banks, fresh nonce + domain lexical salt, batch without-replacement assignment, and recent same-GEO exclusions when manifests are available.  
**Gate:** healthy same-GEO batch with repeated complete menu set or avoidable repeated high-frequency role labels = `FIX_REQUIRED`.  
**Regression:** generate 5 PT-PT sites with overlapping roles; require distinct menu fingerprints and distribute common role labels without replacement while clear alternatives remain.

### NAV-008 — synonym variation becomes conspicuous or unclear
**Symptom:** menu technically differs but uses strange phrases, slogans or ambiguous words that make navigation feel generated.  
**Root cause:** novelty was optimized above native clarity.  
**Rule:** label candidates must pass locale-naturalness, destination-predictability and whole-menu tone checks before random selection.  
**Gate:** a native reader cannot reasonably predict the destination from the menu label = `FAIL`.  
**Regression:** reject vague/awkward labels even if they increase uniqueness; reroll from the clear native pool.



### NAV-009 — lexical diversity works only for one hardcoded GEO
**Symptom:** Portuguese sites vary menu wording, but another GEO falls back to the same canonical `About / Game / FAQ / Contact` equivalents on every site.  
**Root cause:** synonym diversity was implemented as a locale-specific dictionary instead of a universal resolver.  
**Rule:** every resolved locale receives a `NAVIGATION_LOCALE_LEXICON` generated from semantic concept families and regional naturalness rules.  
**Gate:** new non-PT test locale with healthy vocabulary must produce multiple eligible variants for common roles and use stochastic selection.  
**Regression:** run at least two distinct locales and verify both use locale-native randomized role labels.

### NAV-010 — multilingual GEO triggers arbitrary language selection
**Symptom:** a multilingual country gets a randomly chosen navigation language.  
**Root cause:** GEO was treated as equivalent to locale.  
**Rule:** resolve locale/regional language variant before lexical generation; ambiguous language state blocks BUILD or requires source/user resolution.  
**Gate:** unresolved multilingual GEO + generated nav copy = `FAIL`.

<!-- BUNDLE-MODULE-END: 12-FACTORY-LEARNING.md -->

---

---

<!-- BUNDLE-MODULE-START: 19-PRODUCTION-HYGIENE-IDENTITY.md -->

# LOGICAL MODULE: 19-PRODUCTION-HYGIENE-IDENTITY.md

# PRODUCTION HYGIENE & EDITORIAL IDENTITY

**Version:** 1.1.0  
**Role:** remove internal build leakage, preserve truthful owner-directed authorship, and enforce genuinely bespoke production identity across sites

---

## 1. Goal

Production output must read and behave like a finished site, not like a development artifact.

This module removes accidental implementation leakage and template fingerprints from the **public production surface** while preserving truthful ownership, legal integrity, update safety and QA observability.

It does **not** exist to falsify provenance, trick AI-detection systems, or claim that automated assistance was absent. Do not promise detector bypass or publish a false `human-only` claim.

---

## 2. Public leakage zero rule

Public HTML, visible copy, metadata, legal text, cookie UI, 404, JS-rendered strings and public asset annotations must not expose irrelevant internal implementation language such as:

- build/factory/debug labels;
- prompt text;
- model/provider names;
- internal QA notes;
- staging/test instructions;
- internal manifest paths;
- generator/debug HTML comments;
- temporary IDs or diagnostic tokens;
- development-only placeholder wording.

Exception: a disclosure is retained when it is factually or legally required for the actual site/runtime.

Release target:

```text
public_internal_implementation_leaks = 0
```

---

## 3. Production DOM rule

Do not emit development markers such as:

```html
<!-- generated-by: ... -->
<!-- factory-page: ... -->
<!-- prompt: ... -->
```

Runtime verification should prefer semantic page state already present for real functionality, for example:
- expected page ID/key resolved server-side;
- expected body class;
- expected H1/page context;
- private/admin diagnostic state.

Do not add a public fingerprint merely to make QA easier.

---

## 4. Internal compatibility exception

Legacy migration keys, old option names or internal filesystem paths may remain in server-side code **only when needed for backward-compatible upgrades** and when they are not rendered publicly.

Do not break an installed site simply to cosmetically rename a private migration identifier.

When a legacy marker can be safely retired after migration, migrate to a neutral site-specific identifier and remove the old stored value.

---

## 5. Owner-supplied editorial identity

When the user explicitly supplies a real editorial/owner identity, record it as:

```text
editorial_identity_name
editorial_identity_status = OWNER_SUPPLIED
editorial_role
publisher_brand
```

Allowed public uses when semantically true:
- `meta author`;
- Article `author` schema as `Person`;
- visible `Edited by` / `Redakcja` attribution;
- WordPress theme author field when the user owns/maintains the theme;
- About/editorial methodology contact.

Publisher normally remains the site/organization brand unless the user explicitly defines a different publisher.

Do not convert an owner-supplied name into unsupported credentials, employment history, certifications or a false `100% human-created` statement.

### 5.1. Human-directed authorship profile

When the owner states that they conceived, directed, configured, selected, edited or approved the site, record a separate editorial authorship profile:

```text
concept_owner_name
concept_owner_status = OWNER_SUPPLIED
editorial_director_name
editorial_director_status = OWNER_SUPPLIED
site_maintainer_name
site_maintainer_status = OWNER_SUPPLIED
public_credit_mode = OWNER_DIRECTED
```

These fields describe **human direction and responsibility**, not the absence of tooling.

Allowed public formulations when factually supplied by the owner and appropriate to the locale:
- `Koncepcja i redakcja: {owner_name}`;
- `Projekt i kierunek redakcyjny: {owner_name}`;
- `Opracowanie i publikacja: {owner_name}`;
- locale-natural equivalents of `Created and directed by {owner_name}`.

The site may therefore identify the real human who owns the concept/editorial direction even when tools assisted implementation.

### 5.2. Owner identity propagation

If `concept_owner_status = OWNER_SUPPLIED`, propagate the same identity consistently where semantically appropriate:
- `meta[name=author]` on editorial pages;
- Article/WebPage author schema when a Person author is appropriate;
- About / editorial-method block;
- optional footer credit line;
- theme metadata `Author` when the owner actually maintains/publishes the theme;
- Global Text editorial identity keys.

Do **not** silently convert editorial ownership into:
- legal company identity;
- registered office/controller identity;
- professional credentials;
- claim that every line of code/copy was manually typed without tools.

---

## 6. Genuine uniqueness contract

Uniqueness must come from actual project decisions, not cosmetic token swapping.

Before release, compare the current site with available recent factory projects across at least:
1. page architecture;
2. section-family sequence;
3. color fingerprint;
4. typography relationship;
5. hero composition;
6. card/component geometry;
7. visual-medium rhythm;
8. major asset signatures;
9. interaction pattern mix;
10. copy structure and CTA phrasing.

A recolored clone is a FAIL even if filenames, IDs and HEX values differ.

### 6.1. Authored-site fingerprint

For each new site create an internal `AUTHORED SITE FINGERPRINT`:

```text
site_id
concept_owner
voice_profile
lexicon_profile
sentence_rhythm_profile
information_architecture_signature
page_rhythm_signatures[]
color_fingerprint
type_relationship
hero_signature
footer_signature
interaction_signature
major_visual_signatures[]
nearest_prior_site
material_difference_notes[]
```

The goal is not to manipulate an external classifier. The goal is to ensure that a reviewer can see real project-specific editorial and design decisions rather than generic factory defaults.

Release should return to the relevant generation/design stage when too many high-impact dimensions are inherited from a recent unrelated site.

---

## 7. Copy fingerprint rule

Reject repeated factory phrasing such as identical:
- hero sentence architecture;
- section intros;
- CTA pairs;
- About methodology paragraphs;
- FAQ boilerplate;
- legal marketing-style filler.

Do not perform synonym spinning merely to defeat similarity or AI detectors. Rewrite only to improve clarity, locality, specificity, voice and project fit.

### 7.1. Editorial voice profile

Before long-form copy, define a site-specific voice profile:

```text
preferred_sentence_length_mix
preferred_paragraph_density
preferred_transition_style
preferred_technicality_level
preferred_first_person_policy
preferred_cta_tone
locale_specific_vocabulary
brand_specific_vocabulary
phrases_to_avoid
repeated_factory_phrases_to_avoid
```

QA compares Home + at least two internal pages for:
- repeated paragraph openings;
- repeated conclusion formulas;
- repeated CTA formulas;
- repeated FAQ answer structure;
- overuse of symmetrical three-item prose lists;
- generic filler that could belong to another site.

A human-directed site should have coherent editorial habits, but not mechanically identical sentence patterns everywhere.

---

## 8. Source-code hygiene

Install-ready production theme should not ship unnecessary:
- debug dumps;
- prompt files;
- generation logs;
- QA scratch output;
- temporary screenshots;
- contact sheets;
- source maps that expose private build paths when not required;
- internal research notes.

Required runtime code, update migrations, Global Text seed, and legitimate README/install notes are allowed.

### 8.1. Public-package residue scan

Static release scan must search the install-ready ZIP and rendered public HTML for accidental build residues such as:

```text
site factory
factory-page
generated-by
prompt:
model:
chatgpt
openai
claude
gemini
copilot
qa scratch
build note
todo generated
placeholder generated
```

Matches are classified, not blindly deleted:
- internal/debug residue controlled by the theme → remove;
- legitimate third-party/library licence text → keep;
- factual/legal disclosure that is actually required → keep;
- content that merely discusses one of these products/topics as subject matter → keep.

The scanner is a production-hygiene tool, not a provenance falsification tool.

---

## 9. Metadata hygiene

Public metadata must be intentional and coherent:
- one title owner;
- one canonical owner;
- one coherent robots state;
- truthful author/publisher;
- no accidental development generator comments/tags controlled by the theme;
- no stale theme/site identity from prior projects.

Removing unnecessary software-version generator metadata is allowed as production hygiene. It is not treated as a security guarantee.

---

## 10. Legal/content wording hygiene

Public Privacy / Terms / Cookies must describe the actual site and runtime, not the tooling that drafted or assembled the theme.

Do not write phrases such as `our factory generated...`, `the build system...`, or internal QA instructions into public policies unless that tooling itself materially processes user data and therefore requires disclosure.

Unknown legal facts remain unknown; hygiene never authorizes inventing operator identity, address, DPO, governing law or processing facts.

---

## 11. QA gate

Before RELEASE scan public rendered output and install ZIP separately.

### Public frontend
Assert:
```text
visible_internal_build_terms = 0
public_debug_comments = 0
stale_previous_project_identity = 0
truthful_author_publisher_state = PASS
owner_directed_credit_consistency = PASS when configured
accidental_generator_metadata = 0
```

When an OWNER_SUPPLIED concept/editorial owner exists, QA should verify that the public authorship fields name that person consistently where the content model calls for an individual author. It should not invent or require a `human-only` statement.

### Install ZIP
Assert:
```text
prompt_or_generation_logs = 0
qa_scratch_artifacts = 0
temporary_test_assets = 0
unrelated_previous_project_files = 0
```

### Uniqueness
Record:
```text
SITE IDENTITY FINGERPRINT
nearest_prior_site
materially_different_dimensions[]
repetition_risk
```

If the result still looks structurally copied from a previous project, return to Design/Composition/Content rather than renaming variables.

---

## 12. Non-deception invariant

Production cleanliness and originality are mandatory. False provenance is not.

Allowed:
- remove irrelevant internal build terminology from public output;
- attribute the site to a real owner/editor supplied by the user;
- produce distinct composition/copy/assets;
- remove debug/generator leakage controlled by the theme.

Not allowed by this module:
- claim a site was created without automated assistance when that is not established;
- fabricate a human team/persona;
- guarantee or optimize specifically for bypassing AI-authorship detectors;
- alter legal facts merely to look more human-authored.

<!-- BUNDLE-MODULE-END: 19-PRODUCTION-HYGIENE-IDENTITY.md -->



## 16.16. FOOTER CONTENT MINIMALISM + BUSINESS-MODEL COHERENCE POLICY (v4.9.6)

The footer is a **utility/navigation layer**, not a mini-About page, review disclaimer, methodology statement or second hero.

Default useful footer content may include only what helps the user finish or continue a task:
- brand/logo or compact brand name;
- primary/secondary navigation;
- legal links;
- concise contact/support destination;
- real social links when present;
- official game/store/play/download destination when relevant;
- compact copyright / rights-reserved bottom bar.

Optional descriptor copy is allowed only when it is short, useful, business-model coherent and non-duplicative. In `OFFICIAL_GAME_STUDIO`, the default is **no descriptive paragraph**. If a descriptor is genuinely useful, it should normally be one compact phrase such as a truthful localized equivalent of `Studio behind {Game}` or `Creators of {Game}` only when the developer-relationship gate allows that claim.

Do not render footer prose such as:
- `independent guide`, `independent review`, `editorial portal`, `independent Polish guide`;
- long source/methodology disclaimers;
- explanations like `facts from the official source`, `practical interpretations`, `boundary between advice and confirmed functionality`;
- repeated About/mission/product-story paragraphs;
- SEO-style descriptive filler;
- author/publisher/editorial-credit prose merely because the data exists elsewhere;
- a visible source citation paragraph when a simple functional store/product link is enough.

For official-studio sites, a store link such as `{Game} in Google Play` / locale equivalent is valid footer utility. Do not surround it with third-party review positioning.

Footer copy budget rule:
```text
functional links / labels = allowed
compact brand descriptor = optional
long descriptive paragraph = 0 by default
independent/editorial positioning in OFFICIAL_GAME_STUDIO = 0
repeated About/product narrative = 0
```

If removing prose leaves a visually weak footer, fix the **composition**, spacing, grouping, brand mark, contact/nav hierarchy or surface treatment. Do not refill the space with unnecessary text.


### FOOTER-003 — footer becomes a mini editorial disclaimer / independent-review block
**Symptom:** footer contains a paragraph such as `independent guide`, source methodology, review positioning or a repeated product explanation above otherwise useful links.  
**Root cause:** footer was treated as another content section instead of a utility layer.  
**Rule:** footer prose is optional and compact; `OFFICIAL_GAME_STUDIO` forbids independent-review/editorial positioning and defaults to no descriptive paragraph.  
**QA gate:** `footer_longform_prose_count = 0` by default and `official_studio_independent_footer_phrase_count = 0`.  
**Regression:** render an official-studio footer containing `Niezależny ... przewodnik` plus a Google Play link; remove the paragraph, retain the useful store link, navigation/legal/contact and bottom bar.


## 16.17. CLEAN GAMING / ZERO GAMBLING-ASSOCIATION POLICY (v4.9.7)

For this project family, ordinary game/app/studio sites operate in a clean product-gaming niche. When the source does not materially describe gambling, casino, betting, wagering or real-money-stake mechanics, the factory must not introduce those concepts anywhere in public output — including as denials or defensive disclaimers.

Required state for normal gaming builds:

```text
clean_gaming_mode = REQUIRED
source_gambling_relevance = NONE
public_gambling_semantic_mentions = 0
negative_gambling_disclaimers = 0
gambling_seo_terms = 0
```

### Public semantic exclusion

Do not generate localized equivalents of concepts such as:
- casino / online casino;
- gambling / games of chance in the wagering sense;
- betting / bets / sportsbook;
- wagering / stakes for money;
- slot-machine gambling;
- poker/betting positioning;
- real-money gaming / cash wagering;
- bookmaker / betting operator;
- gambling-risk or responsible-gambling disclaimers;
- `not a casino`, `not gambling`, `no betting`, `no real-money gambling` or equivalent denial language.

The prohibition applies to positive, neutral and **negative/denial** phrasing. A sentence saying the site is not related to gambling still creates an unwanted semantic association and is therefore prohibited when the source has no such relevance.

### Surface scope

Zero-association applies to every factory-controlled public textual surface, including:
- Home and all managed pages;
- About / Development / Game / Mechanics / FAQ / Support / Contact;
- header/navigation labels and breadcrumbs;
- footer and bottom bar;
- legal/cookie text unless an actual runtime/legal fact genuinely requires it;
- CTA and interaction copy;
- SEO title, description and meta keywords;
- Open Graph / social text;
- human-readable schema/entity strings;
- image ALT/TITLE and link TITLE;
- ARIA/accessibility copy;
- JS-rendered public messages;
- 404/empty states;
- factory-generated slugs or labels.

### Locale-aware exclusion, not substring matching

The scanner/content engine must resolve the prohibited **concept family** into the target locale/regional variant before generation and QA. Do not rely on one English keyword list.

Do not use naive substring matching that creates false positives. Words or mechanics such as `bonus`, `reward`, `score`, `random`, `chance`, `luck`, prize-like visual effects or collectible currency are not automatically gambling. Classification must depend on actual wagering/casino/real-money semantics.

### Source vertical conflict

Before BUILD, classify the authoritative source:

```text
SOURCE_VERTICAL_PROFILE
source_gambling_relevance = NONE | MATERIAL
clean_gaming_mode
source_vertical_conflict
```

For this project family:

```text
source_gambling_relevance = MATERIAL
→ SOURCE_VERTICAL_CONFLICT
→ INPUT_REQUIRED / STOP BEFORE PUBLIC COPY
```

Do not hide a real source conflict by describing a gambling product as ordinary clean gaming. Do not continue by adding `not gambling` disclaimers. Surface the conflict to the owner instead.

### No SEO/disclaimer contamination

Do not add casino/gambling/betting concepts:
- for negative-keyword coverage;
- for `people may wonder if...` FAQ filler;
- for legal caution where no such activity exists;
- for comparison content;
- for SEO keyword breadth;
- to reassure the user that the game is safe/non-gambling.

Absence is the correct output.

### GAMING-SEM-001 — irrelevant gambling denial leaks into clean game site
**Symptom:** a normal game site says `not a casino`, `not gambling`, `no betting` or a localized equivalent.  
**Root cause:** the generator tried to reassure users about a topic that was not present.  
**Rule:** when `source_gambling_relevance = NONE`, public gambling semantic mentions including denials = `0`.  
**Gate:** any such mention on a factory-controlled public surface = `FAIL`.  
**Regression:** generate an arcade/mobile game studio site and require zero casino/gambling/betting/wagering concept mentions across body, footer, FAQ, legal, SEO and Global Text.

### GAMING-SEM-002 — irrelevant gambling vocabulary added for SEO or legal filler
**Symptom:** casino/betting terms appear only in meta keywords, FAQ, legal disclaimers, ALT/TITLE or social metadata.  
**Root cause:** hidden/public-adjacent surfaces were excluded from content-policy QA.  
**Rule:** the zero-association policy covers rendered and metadata surfaces equally.  
**Gate:** unrelated prohibited semantic concept in any factory-owned metadata/text field = `FAIL`.

### GAMING-SEM-003 — authoritative source conflicts with clean-gaming project profile
**Symptom:** source materially describes wagering/casino/real-money mechanics, but the factory continues as an ordinary clean game studio site.  
**Root cause:** business-niche preference overrode source truth.  
**Rule:** stop at `SOURCE_VERTICAL_CONFLICT`; do not fabricate a clean-game description and do not solve it with denial disclaimers.  
**Gate:** material conflict unresolved before BUILD = `FAIL`.



## 16.18. HERO / FIRST-VIEWPORT STRUCTURAL DIVERSITY POLICY (v4.9.8)

A new site must not default to the recurring silhouette `large text block on the left + media on the right + two CTAs below`, even when that layout is technically valid.

Hero selection is a **separate high-impact diversity decision**. For every managed page that has a hero/intro stage, record:

```text
hero_family
hero_topology_cluster
hero_text_anchor
hero_copy_alignment
hero_media_topology
hero_media_dominance
hero_title_scale_tier
hero_eyebrow_position
hero_cta_position
hero_shell_mode
hero_mobile_transform
hero_signature
```

### Text-anchor family

Eligible hero text anchors include, when semantically/responsively valid:

```text
LEFT_EDGE
CENTERED
RIGHT_EDGE
TOP_CENTER
BOTTOM_EDGE
INSET_PANEL_LEFT
INSET_PANEL_RIGHT
OVERLAY_CENTER
OVERLAY_EDGE
MEDIA_FIRST_STACK
TEXT_FIRST_STACK
ASYMMETRIC_OFFSET
```

`LEFT_EDGE` is one option, not the default gravity.

For Home + at least three key internal pages, when healthy candidates exist:
- use at least `3` materially different hero text-anchor/topology families;
- exact hero-shell repetition across unrelated page roles = `0` by default;
- one left-anchored split family must not dominate the compared pages merely because it is safe;
- Home's hero renderer must never become the universal internal-page renderer.

### Cross-site hero anti-repeat

When recent comparable hero fingerprints are available, reject a new hero that preserves the same recognizable silhouette, even if colors, image, copy and border radius changed.

A new hero must materially vary across several of:
- text anchor/alignment;
- media position/topology;
- title width/scale tier;
- CTA placement;
- shell/bleed mode;
- overlay vs separated content;
- vertical rhythm;
- first-viewport media dominance.

If history is unavailable, use nonce-driven random selection across topology clusters and do not claim cross-site comparison PASS.

### Hero-title proportion rule

Large display type is an option, not a default identity.

At representative desktop width, reject when the H1:
- visually consumes most of the first viewport;
- becomes a 5–7-line wall mainly because of an oversized scale;
- pushes useful copy/CTA or media below the fold without a deliberate editorial reason;
- makes the media look secondary or ornamental;
- creates the same giant-left-headline silhouette repeatedly across sites/pages.

Prefer a moderate title tier first. Escalate to an oversized manifesto tier only when the page concept and media composition genuinely require it.

The fix order is:

```text
reduce title scale / max-inline-size
→ change line measure
→ rebalance copy depth
→ change text anchor
→ change hero family
→ reroll topology cluster
```

Do not solve every long headline by making it larger.


## 16.19. FOOTER CONTACT COMPLETENESS + BOTTOM-BAR MICROCOPY POLICY (v4.9.9)

For a full site using the standard factory Contact Profile, the footer contact zone must expose the resolved public contact set coherently:

```text
public_email
public_phone_display
public_postal_address
```

When those fields exist in the Contact Profile, silently omitting phone or address from the footer is a completeness defect.

The footer remains utility-first: contact values may be compact, but they must be present and readable. Synthetic status stays internal; public wording must not falsely call a synthetic phone/address verified, registered or official.

### Bottom-bar secondary phrase

The bottom bar may contain one short locale-natural microcopy phrase opposite or adjacent to the copyright line.

Recommended semantic families:
- `PRIVACY_RESPECT`;
- `SUPPORT_ORIENTATION`;
- `PRODUCT_ORIENTATION`;
- `BRAND_SERVICE_NOTE`.

Examples are locale calibration only, not universal defaults:
- pl-PL: `Szanujemy Twoją prywatność.` when coherent with the site's actual privacy/runtime model;
- another site may use a short support/product-oriented phrase instead.

Rules:
- normally `2–7` words or another equally compact locale-natural length;
- natural for the resolved GEO/locale;
- truthful and non-legalistic;
- no unsupported `secure / protected / guaranteed / safest` claims;
- no SEO filler;
- no duplicate About/mission prose;
- no unrelated disclaimer language.

A naked decorative arrow or unlabeled `back to top` control must not occupy this slot by default. A real back-to-top control is allowed only when intentionally designed as navigation, labeled accessibly and actually useful; it is not the default bottom-bar content.

The selected phrase is editable Global Text and may vary between unrelated sites.


## 16.20. MANDATORY FAVICON / SITE-ICON POLICY (v4.9.10)

Every full production build must ship a coherent favicon/site-icon solution before RELEASE.

Required outcome:

```text
brand_utility_icon_set = present
browser_favicon_resolves = yes
favicon_matches_current_site_brand = yes
stale_previous_site_icon = no
```

The factory must create or prepare an original compact brand mark suitable for tiny square display when the owner did not provide one.

Preferred local set:
- scalable favicon SVG when appropriate;
- small browser PNG fallback such as 32x32;
- Apple touch icon around 180x180;
- WordPress/site-icon compatible square asset around 192x192 and/or 512x512.

Runtime rule:
- if WordPress already has an intentional owner-supplied Site Icon, preserve/use it;
- otherwise the theme must provide its own local fallback icon links/assets;
- do not emit duplicate conflicting icon owners;
- favicon URLs should be cache-versioned on theme updates when the asset changes.

Missing favicon, broken icon URL, stale previous-project icon or unrelated generic placeholder icon = `FIX_REQUIRED`.

### HERO-DIV-001 — repeated giant-left hero silhouette
**Symptom:** unrelated sites/pages repeatedly open with oversized left H1 + right media.  
**Root cause:** semantic fit scoring allowed one safe split family to dominate hero selection.  
**Rule:** hero topology/text anchor is randomized from materially different clusters and checked independently from section diversity.  
**Regression:** compare Home + key internal pages and synthetic new-site nonces; require materially different hero anchors/topologies when healthy candidates exist.

### TYPE-HERO-001 — hero title overwhelms first viewport
**Symptom:** H1 occupies most of the first viewport and pushes media/supporting copy out of balance.  
**Rule:** moderate title tier is default; oversized tier requires explicit composition justification and screenshot PASS.

### FOOTER-004 — footer drops resolved phone/address or uses naked utility icon
**Symptom:** footer shows email but omits resolved phone/address, or bottom bar ends with an unlabeled arrow.  
**Rule:** render complete resolved contact set and use concise locale-natural microcopy or an intentional labeled utility control.

### ICON-001 — production site ships without favicon
**Symptom:** browser tab uses no icon, a WordPress default, or stale previous-site icon.  
**Rule:** mandatory brand utility icon set + runtime head verification before RELEASE.

---

## 16.19. PERSISTENT FACTORY STRUCTURAL MEMORY POLICY (v4.9.9)

Cross-site diversity history is persistent factory state, not optional conversational memory.

Canonical external store for this factory:

```text
STRUCTURAL_MEMORY_REPOSITORY = PingVinni/Landing
LAYOUT_BANK_ROOT = site-factory-layout-bank/
HISTORY_ROOT = site-factory-history/
HISTORY_INDEX = site-factory-history/index.json
SITE_HISTORY_PATH = site-factory-history/sites/{normalized-domain}.json
```

### Before every unrelated new-site BUILD

The factory must, when the repository connection is available:
1. read `site-factory-history/index.json`;
2. select recent sites, same-niche/GEO candidates when relevant, and nearest structural matches;
3. read detailed per-site fingerprint files for the comparison set;
4. feed those fingerprints into Hero, page rhythm, section, interaction, mobile, header, CTA and footer selection;
5. hard-exclude / reroll candidates that violate structural-distance or recent-use rules.

Do not claim cross-session history comparison when the repository could not be read.

### After every completed new-site BUILD

The factory must create exactly one canonical structural-memory file:

```text
site-factory-history/sites/{normalized-domain}.json
```

For a same-domain update, update that canonical file instead of creating a duplicate. Preserve a compact `revisions[]` record when the structural fingerprint materially changes.

The per-site file must record structural facts only, including at minimum:

```text
domain / GEO / locale / niche
build identity + structural schema version
Home hero topology / anchor / media topology / title tier
header family / cluster / signature
footer family / topology / signature
Home page rhythm
Home section archetype sequence
Home topology / text-anchor / media-topology sequences
Home bigram + trigram signatures
Home neutral silhouette fingerprint
key-page fingerprints
per-key-page section structural signatures
interaction profile
mobile transformation profile
site structural fingerprint
comparison summary
reroll / new-grammar counts
revisions[]
```

For each meaningful key-page section, prefer compact fields such as:

```text
page_key
section_key
semantic_role
archetype_id
topology_cluster
shell_mode
text_anchor
text_alignment
media_topology
media_dominance
card_or_list_geometry
surface_mode
edge_overlap_mode
density_mode
interaction_family
mobile_transform
section_fingerprint
```

Do **not** store:
- public page copy;
- prompts;
- credentials/secrets/tokens;
- private user data;
- unnecessary personal information;
- source assets themselves.

### Index update is mandatory

After the per-site file write, update:

```text
site-factory-history/index.json
```

The index must maintain enough recency/frequency state to support fast comparison, including where available:
- domain + date/version;
- niche/GEO/locale;
- site fingerprint;
- Hero/Footer archetype and topology counts;
- page rhythm frequency;
- section archetype/topology frequency;
- Home bigram/trigram frequency;
- most recent site list.

### Read-after-write verification

A write call alone is not PASS.

After writing the site file and index, re-read both from the repository default branch and verify:

```text
per_site_file_exists = yes
per_site_domain_matches = yes
site_fingerprint_matches_current_build = yes
history_index_contains_site = yes
history_index_frequency_update = coherent
```

Only then record:

```text
STRUCTURAL_MEMORY_WRITE_PASS
```

If the repository is unavailable or write permission fails:

```text
STRUCTURAL_MEMORY_WRITE_BLOCKED
cross_session_structural_memory_persisted = false
```

The theme/build artifact may still be produced, but the factory must not claim persistent cross-session anti-repeat PASS. `RELEASE PASS` requires either successful structural-memory persistence or an explicit owner waiver of the external-history requirement.

### Regression — LAYOUT-020 persistent memory silently missing

**Symptom:** a site is generated successfully but no per-site structural history file exists, so future sites cannot compare against it.  
**Root cause:** cross-site diversity lived only in transient chat/build artifacts.  
**Rule:** per-domain JSON + index update + read-after-write verification are mandatory after every full new-site build.  
**Gate:** missing/failed repository persistence without explicit owner waiver = `FIX_REQUIRED`.  
**Regression:** complete a synthetic BUILD, then assert canonical per-site file exists and is discoverable through the global history index before the next unrelated BUILD.



## 16.19. STUDIO-FIRST BUSINESS NARRATIVE POLICY (v4.9.9)

For this project family, a single-game promotional site should default to a **studio/product business narrative** when `business_model_mode = OFFICIAL_GAME_STUDIO` and the developer-relationship truth gate permits first-person creator claims.

The public site is not primarily a guide about somebody else's game. Its central commercial story is:

```text
STUDIO
→ OUR TEAM / CREATIVE APPROACH
→ OUR GAME / PRODUCT
→ WHAT WE SET OUT TO BUILD (only with creator-intent evidence)
→ DESIGN PROBLEMS / PRODUCT CONSTRAINTS
→ HOW THE GAME SYSTEMS WERE SHAPED
→ DEVELOPMENT / REFINEMENT
→ PLAYER-VISIBLE RESULT
→ PLAY / DOWNLOAD / SUPPORT
```

### Thematic-weight target

For a rich official studio site, the **majority of non-legal thematic depth** should normally come from studio/product/development content rather than generic player-guide copy.

Practical target when the source supports enough depth:

```text
studio / product / development / design narrative ≈ 60–80%
gameplay explanation / player guidance / FAQ      ≈ 20–40%
```

This is a narrative-balance target, not a word-count quota. Do not pad weak process claims merely to hit a percentage.

### Required business jobs

Across Home + key internal pages, cover distinct jobs such as:
- studio identity;
- game/product proposition;
- development story;
- mechanics/system design;
- level/progression design;
- controls/feel;
- art/visual direction;
- balancing/testing/refinement when supported;
- support/update relationship;
- play/download/store conversion.

Not every site needs every job, but a rich official-studio site must not collapse to `Home + How to Play + FAQ + Contact`.

### Team model

When the creator relationship is resolved, aggregate first-person language such as `our team`, `we built`, `we designed`, `we refined` is allowed at the level supported by evidence.

Do not invent:
- named employees;
- individual roles;
- team size;
- departments;
- office/studio location as workplace fact;
- founder biographies;
- staff quotes;
- internal responsibility assignments.

Those require owner-supplied or verified data.

### Development-situation model

The site should contain meaningful development tension, but must distinguish a **design problem** from an **invented historical anecdote**.

If the actual event is owner-supplied/source-verified, use:

```text
SITUATION / CHALLENGE
→ WHAT THE TEAM TRIED
→ DECISION
→ IMPLEMENTATION
→ RESULT / LEARNING
```

If exact internal history is unavailable, use the truth-safe product form:

```text
DESIGN PROBLEM / CONSTRAINT
→ SYSTEM REQUIREMENT
→ IMPLEMENTATION PRINCIPLE
→ PLAYER-VISIBLE OUTCOME
→ REFINEMENT / TEST CRITERIA at a high level
```

Do **not** convert an observable mechanic into a fake anecdote such as `we struggled for weeks`, `our testers complained`, `the first prototype failed`, or `we rebuilt the level three times` without evidence.

### Product promotion rule

Every major non-legal page should connect its story back to the product naturally. Use contextual first-party CTAs such as:
- play/download the game;
- see the game/product;
- explore a mechanic;
- see how we built a system;
- continue to the development story;
- get support.

The site promotes the game as the studio's product; conversion should be visible but not repetitive or spammy.

### Model-drift blockers

In resolved `OFFICIAL_GAME_STUDIO` mode, block:
- independent guide/review/editorial-portal framing;
- article-library-first architecture without product reason;
- anonymous outsider voice about the developer;
- generic `tips / guide / rankings` content dominating the site;
- About page focused on sourcing/editorial methodology;
- synthetic testimonials as studio trust;
- game description with almost no studio/development narrative;
- repeated `we created...` slogans without new information gain.


## 16.21. SEMANTIC VISUAL COUPLING + MICRO-VISUAL SYSTEM POLICY (v4.9.11)

For every new rich/site-factory BUILD, visual production is coupled to the actual section meaning. The factory must not place imagery merely because a layout contains an image slot.

### Mandatory semantic chain

For every meaningful non-legal section, resolve before asset creation:

```text
page_business_role
→ section_intent
→ section_heading_meaning
→ paragraph_cluster_meaning
→ factual/product entities present
→ player/studio/business message
→ visual_job
→ dedicated_asset_or_micro_visual
```

The final visual must support the **actual heading + paragraph cluster + section role**. A generic image that only matches the broad niche does not satisfy this rule.

### Dedicated visual rule

For rich gaming / official-studio sites:
- every major narrative section should receive its own dedicated major visual when a raster/illustrative scene can materially support the content;
- the same major image or near-duplicate composition must not be reused as the visual answer for unrelated sections;
- if a large image would be semantically weak, the section must use an original diagram, iconographic explainer, bespoke SVG, annotated micro-visual, or intentionally quieter typographic composition with supporting micro-elements;
- visual support follows content; the factory must not invent filler copy to justify an image.

A section is not considered visually complete merely because it has a background gradient, generic device mockup, repeated game-world scene, or decorative blob.

### Adult / premium default

Unless the source explicitly requires playful/cartoon treatment, generated major visuals should default to a mature, premium, editorial/commercial direction:
- controlled composition;
- believable depth/material/light;
- crisp detail;
- intentional crop/focal point;
- restrained color treatment consistent with the site Design DNA;
- no childish mascot energy, toy/plastic CGI, cheap mobile-ad look, generic fantasy filler, pseudo-3D badges or random neon.

### Site-specific micro-icon family

Every visual-rich site must define an original or purpose-built **MICRO-VISUAL SYSTEM**. It may include:
- feature/mechanic icons;
- development-stage symbols;
- process markers;
- support/contact icons;
- compact badges/chips where semantically useful;
- timeline nodes/connectors;
- list markers;
- section index marks;
- tiny diagrams/data glyphs;
- divider motifs and controlled micro-shapes.

The system is not decorative noise. Every icon/glyph must have a role, and repeated symbols must preserve the same meaning.

### Micro-visual manifest

Before BUILD record:

```text
MICRO_VISUAL_SYSTEM_MANIFEST
style_family
stroke_or_fill_strategy
corner_language
optical_weight
size_tiers[]
color_roles[]
icon_roles{}
section_assignments{}
repetition_policy
accessibility_policy
mobile_simplification
```

Default rich gaming/studio target when semantically useful: roughly `12–24` distinct small icons/glyphs across the site, not counting logo/favicon. This is a quality target, not a quota; do not create meaningless icons to hit a number.

### Hard blockers

`FIX_REQUIRED` when:
- a major section image does not correspond to the section's heading/paragraph meaning;
- one generic game image is reused as visual support for multiple unrelated topics;
- most sections use the same image composition family without narrative reason;
- important process/mechanic blocks are visually bare despite clear icon/diagram opportunities;
- random third-party/icon-library symbols create a mixed visual language;
- icons are added solely to fill empty space;
- icon semantics change from section to section;
- micro-elements reduce readability, focus clarity or touch usability.

### Regression — VISUAL-004 semantic mismatch

**Symptom:** section about balancing/testing displays the same generic world/game scene used for art direction and mechanics.  
**Rule:** each major section resolves a dedicated `visual_job` from heading + paragraph cluster; generic niche relevance is insufficient.  
**Gate:** `section_visual_semantic_match = FAIL` → replace/regenerate.

### Regression — VISUAL-005 visually empty micro-system

**Symptom:** site has large images but cards, process steps and compact information blocks feel bare/repetitive.  
**Rule:** use the site-specific micro-icon/micro-UI system where it improves scanning or semantic grouping.  
**Gate:** clear semantic icon opportunities with no designed micro-system across a rich site = `FIX_REQUIRED`.




## 16.22. COMPANY / TEAM / DEVELOPMENT-FIRST PAGE POLICY (v4.9.12)

This module is authoritative for new `OFFICIAL_GAME_STUDIO` gaming/product builds and supersedes earlier weaker page-order guidance when the creator/developer truth gate permits first-person studio claims.

### Business model first

The public site is primarily a **studio/business/product website**. The game is the product created and promoted by the studio; it is not the main editorial subject viewed from outside.

For every key non-legal page, narrative planning starts with:

```text
COMPANY / STUDIO
→ TEAM / COLLABORATION
→ CURRENT WORK / TASK / CHALLENGE
→ DESIGN / DEVELOPMENT PROCESS
→ REVIEW / ITERATION / QA
→ RESULT / PRODUCT DECISION
→ GAME / FEATURE / PLAYER EXPERIENCE
→ PLAY / DOWNLOAD / SUPPORT
```

The exact section order remains layout-diverse, but the semantic dominance is mandatory.

### Upper + middle page dominance

For Home, Product/Game, Development, Mechanics, Levels/Progression, Art/Visual Direction, About/Studio, FAQ and Contact/Support:

```text
first_viewport_business_story = REQUIRED
upper_half_team_or_process_sections >= 2
middle_page_team_or_process_presence = REQUIRED
lower_page_product/game explanation = REQUIRED when relevant
```

The first roughly `55–70%` of a rich page should normally be led by studio/team/work/process/design/review content.

The lower roughly `30–45%` may move more strongly into:
- game features;
- mechanics;
- progression;
- player experience;
- store/platform;
- support;
- play/download conversion.

This is a narrative architecture target, not permission to pad or fabricate internal history.

### Page opening rule

A key page should not normally open with:

```text
GAME FACT
→ GAME FACT
→ GAME FACT
```

It should instead open with a studio-owned reason for the page, for example:

```text
what our team is solving
what this discipline owns
what decision is being shaped
what quality target is being reviewed
what player-facing result the work should produce
```

Then the page may explain the concrete product/game system in the lower narrative layers.

### Team/work information roles

Add these information roles to `CONTENT DEPTH MANIFEST`:

```text
COMPANY_CONTEXT
TEAM_APPROACH
WORK_IN_PROGRESS
TASK_BREAKDOWN
DESIGN_DECISION
PROTOTYPE_OR_ITERATION
REVIEW_AND_QA
CROSS_DISCIPLINE_COLLABORATION
PRODUCT_OUTCOME
PLAYER_VISIBLE_RESULT
```

Do not repeat one generic `our team works hard` paragraph under different headings. Each section must add a different work/business job.

### 30% copy-density reduction override

For rich official-studio builds, reduce visible prose by approximately `30%` relative to the v4.9.12 high-density defaults while preserving distinct information roles and factual support.

Current planning envelopes:

```text
HOME
visible words: ~900–1350
meaningful sections: ~10–15

KEY DOMAIN / PRODUCT / DEVELOPMENT PAGE
visible words: ~950–1700
meaningful sections: ~7–11

ABOUT / STUDIO
visible words: ~750–1250
meaningful sections: ~6–9

FAQ
visible words: ~525–950
questions: commonly ~12–20 when useful

CONTACT / SUPPORT
visible words: ~525–950
meaningful sections: ~5–8
```

Legal text is **not** inflated by this multiplier. Legal remains driven by actual applicability/runtime facts.

The reduction must come from tighter sentences, fewer repeated explanations and less filler—not from deleting distinct information roles, factual support or useful decision context.

### Truth-gate behavior

The desired business model does not override factual ownership.

If the source developer differs from the domain/studio brand and the relationship is unresolved:

```text
OFFICIAL_GAME_STUDIO desired
+ relationship unresolved
→ INPUT_REQUIRED
```

Do **not** silently fall back to an outsider/guide model for the final production build unless the user explicitly selects that model.

Once the user explicitly confirms the creator/brand relationship, first-person studio voice may be used throughout according to the existing evidence rules.

### Team-image truth boundary

A generated collaboration/work scene may visually represent a **conceptual studio workflow**, but anonymous generated people must not be identified as named real employees or presented as documentary proof of the actual team.

If real staff identity/portrait claims are required, use owner-supplied or verified team media.

### Regression additions

`STUDIO-FIRST-002` — key page opens with generic product facts while the company/team/process model is absent from the first half = `FAIL`.

`CONTENT-DENSITY-001` — page materially exceeds the compact envelope without a documented information need, or reaches the target through repetition/filler = `FIX_REQUIRED`.

`MODEL-DRIFT-003` — unresolved developer relationship is silently converted into outsider/editorial copy instead of requesting confirmation = `FAIL`.



## 16.23. PAGE COMPOSITION DIVERSITY + NO-DEAD-SPACE DOCTRINE (v4.9.13)

This policy is mandatory for rich generated sites and is especially strict for `OFFICIAL_GAME_STUDIO`.

### Structural variety is a release requirement

Different copy inside the same repeated skeleton does **not** count as page diversity.

The factory must actively prevent repeated patterns such as:

```text
left heading + right paragraphs
→ 4 equal cards
→ left heading + right paragraphs
→ 4 equal cards
```

or:

```text
image left + copy right
→ image left + copy right
→ image left + copy right
```

within one page or across most key pages of one site.

### Mandatory section-family planning

Before rendering, every meaningful section receives:

```text
section_layout_family
section_topology_cluster
text_flow_mode
media_relationship
density_mode
interaction_family
background_family
mobile_transform
```

No page may be composed by repeatedly calling one generic section template with only swapped text.

### Same-page repetition limits

For a normal rich page:

```text
exact_layout_family_repeat = 0
same_topology_cluster_max_occurrences = 2
same_text_flow_mode_consecutive_repeat = 0
same_card_geometry_consecutive_repeat = 0
```

A second use of the same topology cluster is allowed only when:
- semantic need is materially different;
- media/text relationship changes;
- the resulting neutral silhouette is visibly different.

### Cross-page repetition limits

Across Home + key internal pages:
- one section family may not dominate the site;
- representative pages should use different opening, middle and closing grammars;
- repeating one `title-left / text-right` editorial pattern across multiple pages as the default = `FAIL`;
- repeating one `four-card grid` as the default explanation device = `FAIL`.

### No-dead-space invariant

Visible empty space is allowed only when it performs an intentional composition job.

Forbidden:
- a blank right half because media was omitted;
- a narrow copy column floating beside unused desktop width;
- reserved image geometry with no image;
- giant height created by fixed/min-height after content becomes shorter;
- empty decorative shell that contributes no hierarchy.

If a planned media asset is unavailable, the section must **reflow**, not preserve the empty slot.

Fallback order:

```text
REGENERATE / REPLACE SEMANTIC MEDIA
→ USE ANOTHER VALID MEDIA FORM
→ CHANGE TO FULL-WIDTH EDITORIAL COMPOSITION
→ ADD SEMANTIC DIAGRAM / LEDGER / CALLOUT
→ REDUCE SECTION SHELL
```

Never ship an empty media column.

### Full-width editorial fallback

When a section is text-heavy and no meaningful image is justified:

```text
content_width = FULL_USEFUL_WIDTH
heading_and_body_relationship = DELIBERATELY_COMPOSED
dead_secondary_column = 0
```

Eligible treatments include:
- full-width essay;
- wide editorial two-column text flow;
- centered manifesto + supporting paragraphs;
- staggered narrative;
- chapter ledger;
- pull-quote/fact rail when factual;
- process annotation;
- decision matrix;
- full-width body with small semantic markers.

### Text-growth requires visual-growth

When factory copy depth increases materially, visual density must be reconsidered.

For a rich studio page, if copy volume changes materially, recompute visual density. The compact-copy policy must never turn removed prose into new blank canvas.

Normal evaluation:

```text
for each ~300–450 visible words of rich non-legal narrative
→ evaluate one meaningful major/medium visual moment
```

This is not a hard quota. A strong full-width editorial passage may intentionally stay text-led, but a long page cannot become a sequence of empty text shells.

### Image wrapping and mixed composition

The design engine should support:
- text wrapping around an editorial image;
- floating image with caption;
- inset image inside an essay field;
- image between two narrative blocks;
- overlapping media + copy card;
- staggered image/text rhythm;
- gallery strip beside long-form narrative;
- top-image / body-below composition;
- asymmetrical image rail;
- image-led chapter break.

### Regression IDs

`LAYOUT-REP-001` — same section family repeated across a page without material structural change = `FAIL`.

`LAYOUT-REP-002` — same editorial left-heading/right-copy pattern dominates several key pages = `FAIL`.

`SPACE-001` — unused media column / visually dead half-section = `FAIL`.

`SPACE-002` — text remains artificially narrow although section has no semantic media = `FAIL`.

`MEDIA-DENSITY-001` — copy volume materially increased but page visual rhythm was not recalculated = `FIX_REQUIRED`.
---

## 16.24. FULL-WIDTH CANVAS + COMPACT COPY OVERRIDE (v4.9.14)

This patch supersedes earlier conflicting high-density copy targets and strengthens the no-dead-space doctrine after a regression where valid content was rendered inside a narrow left-side island while a large part of the desktop canvas remained unused.

### Compact-copy baseline

For normal rich builds, target roughly `30%` less visible prose than the v4.9.12 high-density profile:

```text
HOME                              ~900–1350 visible words
KEY DOMAIN / PRODUCT / DEVELOPMENT ~950–1700
ABOUT / STUDIO                    ~750–1250
FAQ                               ~750–1350 plus useful Q&A structure
CONTACT / SUPPORT                 ~525–950
LEGAL                             ~775–1550 when actual applicability supports it
```

These are envelopes, not quotas. Keep the same factual/information jobs where useful; compress by removing repetition, duplicate explanations, inflated intros, filler transitions and redundant CTA prose.

### Full useful width is the default composition contract

A full-width page section does not pass merely because its outer background is `100%` wide. The **meaningful composition** must use the available section canvas.

At desktop/laptop widths, for ordinary major non-hero sections:

```text
section_shell_inline_usage = FULL
major_section_canvas_coverage target >= 0.78
largest_unassigned_blank_region_ratio target <= 0.22
empty_grid_track_count = 0
reserved_media_slot_without_media = 0
```

The final screenshot remains authoritative. Numeric targets are diagnostics, not permission to ship an obviously half-empty section.

### One-sided blank-field blocker

`FAIL` when meaningful content/media is clustered into a narrow left or right island while a large opposite field has no declared role. Readable line length is not an excuse: a text measure may stay narrow, but the **section composition** must use the canvas through centered placement, multiple editorial columns, media, ledger/data, a meaningful rail, or another intentional structure.

### Mandatory auto-collapse

When an optional media/secondary column is absent:

```text
REMOVE EMPTY TRACK
→ RECOMPUTE GRID
→ EXPAND / RECENTER CONTENT COMPOSITION
→ RECHECK HEADING MEASURE
→ RECHECK SECTION HEIGHT
→ SCREENSHOT QA
```

Never preserve a `50/50` or similar split with one empty side.

### Compact copy must not create empty pages

The ~30% copy reduction does **not** permit taller padding, larger headings or extra blank fields to preserve the old section height. Re-run composition after copy compaction and give released space to media, hierarchy, useful interaction or a shorter section.

### Regression IDs

`WIDTH-001` — meaningful section uses only a narrow side of the available desktop canvas while the opposite side is functionally empty = `FAIL`.

`WIDTH-002` — outer section is full width but inner composition remains unnecessarily capped/narrow for the selected layout family = `FAIL`.

`REFLOW-001` — optional media disappears but its grid track/shell remains = `FAIL`.

`COPY-030` — generated rich-site copy ignores the compact ~30% reduction without a documented information need = `FIX_REQUIRED`.


---

## 16.25. RENDER-PROOF GEO / COMPOSITION / MEDIA OVERRIDE (v4.9.15)

This override exists because static manifests and self-declared composition metadata can pass while the installed site still has the wrong document locale, visibly empty desktop fields, repetitive rendered sections, or low-grade illustrative media. For full-site BUILD, **rendered evidence outranks manifest intent**.

### A. GEO + locale is a release invariant

Explicit user input such as `GEO = PL` and `locale = pl-PL` must resolve coherently across the final public document:

```text
requested_geo = PL
requested_locale = pl-PL
wordpress_locale = pl_PL
html_lang = pl-PL
og_locale = pl_PL
schema_inLanguage = pl-PL
content_language = Polish
```

A localized Polish site that renders `<html lang="en-GB">`, `en-US`, or another unrelated locale is `GEO-SEO-001 = FAIL` even when title/description copy is Polish.

For normal indexable public pages, emit one coherent explicit robots state equivalent to:

```text
index, follow, max-image-preview:large
```

Do not add obsolete `meta keywords` merely to satisfy legacy SEO analyzers; missing `keywords` is not itself a modern SEO failure.

### B. Browser render is mandatory for composition release

`STATIC_PASS` and manifest-based `COMPOSITION_SELF_CHECK` are no longer enough to declare a full BUILD ready.

A full BUILD must capture and inspect representative browser renders at minimum:

```text
mobile narrow
laptop / 1366-class
standard desktop / 1440–1600-class
wide desktop / 1920-class
```

If browser rendering is unavailable, the build artifact may be produced for debugging, but status must be:

```text
BROWSER_QA_BLOCKED
release_ready = false
```

Never use `RUNTIME_NOT_RUN` or static geometry claims as a substitute for visible composition acceptance.

### C. No narrow-island / headline-stack regression

For ordinary major desktop sections:
- meaningful content must visually occupy the useful canvas, not only the outer background;
- no large one-sided blank quadrant without an explicit visual role;
- standard H2/H3 should normally stay within `1–3` visual lines at desktop;
- `4+` heavy heading lines requires a manifesto/editorial exception and browser approval;
- multi-line section headings must not use compressed line-height that makes words appear stuck together;
- heading/body groups need obvious separation and shared alignment logic;
- section height must collapse after copy reduction instead of preserving old empty space.

### D. Rendered diversity, not label diversity

Different `archetype_id`, class names, colors or copy do **not** prove uniqueness.

Each major section must expose a rendered structural signature containing at least:

```text
dom_layout_signature
css_layout_signature
content_anchor_signature
media_geometry_signature
surface_geometry_signature
rendered_silhouette_signature
```

For rich pages with `6+` major sections, target at least `80%` materially distinct rendered silhouettes. Adjacent major sections that are near-identical in actual geometry must reroll even when their manifest IDs differ.

### E. Adult premium photography dominance

For commercial/gaming/product builds, major visual storytelling defaults to high-quality adult editorial / photorealistic imagery.

```text
major_photo_or_photoreal_visual_ratio >= 0.70
abstract_diagram_or_vector_major_visual_ratio <= 0.20
childlike_doodle_major_visual_count = 0
```

Original diagrams/SVGs are allowed as secondary explanatory support, utility graphics, icons or data visuals, but not as the default hero or dominant site-wide media language.

When source-owned photography/screenshot rights are unavailable, generate original photorealistic editorial imagery that is contextually truthful. Do not fabricate fake gameplay UI, fake awards, fake teams, fake offices or fake developer ownership.

### F. Blocking regressions

`GEO-SEO-001` — final HTML language/locale disagrees with requested locale = `FAIL`.

`RENDER-001` — no browser screenshot QA for a claimed full-site release = `FAIL`.

`SPACE-002` — major section contains a visually large unassigned side field or content island = `FAIL`.

`TYPE-STACK-001` — ordinary section heading becomes a 4+ line oversized/compressed word stack without explicit exception = `FAIL`.

`DIVERSITY-RENDER-001` — section IDs differ but rendered geometry remains materially repetitive = `FAIL`.

`MEDIA-ADULT-001` — abstract/vector/doodle visuals dominate a build that calls for adult premium photography = `FAIL`.
