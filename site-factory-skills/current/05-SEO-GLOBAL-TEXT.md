# 05 SEO GLOBAL TEXT

**Bundle format:** Source Bundle v1.5  
**Policy baseline:** Site Factory v4.9.15  
**Bundling rule:** logical module boundaries and aliases are preserved inside bundles. Source Bundle v1.5 applies the Site Factory v4.9.14 interaction, micro-motion, hover/focus and semantic interactive-section expansion while preserving v1.4 rich-content, live UI/UX research, morphological section variation, v1.3 adult-premium visuals and the 7-file Project Source architecture.

## Module aliases in this bundle

- `14-SEO-GEO-METADATA-ENGINE.md` → this file, section `LEGACY MODULE: 14-SEO-GEO-METADATA-ENGINE.md`
- `17-GLOBAL-TEXT-ENGINE.md` → this file, section `LEGACY MODULE: 17-GLOBAL-TEXT-ENGINE.md`

## Cross-reference rule

References inside logical module text to filenames such as `15-SECTION-IMAGE-ENGINE.md` remain valid **logical module IDs**. Resolve them against the module aliases declared across the loaded Source Bundles. `SOURCE-BUNDLE-MAP.md` is maintenance documentation only and is **not required** as a Project Source.

---

<!-- BUNDLE-MODULE-START: 14-SEO-GEO-METADATA-ENGINE.md -->

# LEGACY MODULE: 14-SEO-GEO-METADATA-ENGINE.md

# SEO GEO METADATA ENGINE

**Version:** 4.5.1  
**Role:** повне SEO / GEO / metadata / social / structured-data наповнення кожної сторінки з rich-content intent separation  
**Scope:** Title, Description, Keywords, URL, Canonical, Robots, Author, Publisher, Lang, headings, images, links, social metadata, schema, sitemap, robots.txt  
**Authority:** цей модуль є спеціалізованим джерелом правил для SEO/meta. У разі конфлікту із загальними SEO-згадками в інших MD — цей файл має пріоритет.

---

## 1. Мета

Кожна indexable сторінка повинна мати завершений SEO profile, який відповідає:

`PAGE INTENT + TOPIC + ENTITY + GEO + LOCALE + SITE BRAND + RUNTIME`

Фабрика не повинна залишати поля на кшталт:

- `Keywords are missing`
- `Author is missing`
- `Publisher is missing`
- неправильний `Lang`
- generic title
- дубльований description
- canonical не на поточну сторінку
- неправильний robots state

---

## 2. SEO PAGE PROFILE

Перед рендером кожної indexable сторінки сформувати:

```text
page_key
page_type
page_intent
primary_topic
secondary_topics
primary_entity
geo
locale
language
brand
publisher_name
author_name
title
meta_description
meta_keywords
keyword_term_count
canonical_url
robots
og_title
og_description
og_image
og_locale
twitter_title
twitter_description
twitter_image
schema_types
breadcrumbs
internal_link_targets
external_sources
image_alt_plan
image_title_plan
link_title_plan
heading_plan
```

---

## 3. Page intent

Кожна сторінка має один primary intent.

Examples:

### Home
- brand discovery
- topic overview
- route to deeper pages

### Guide
- informational / educational

### Catalog
- discovery / comparison

### About
- trust / provenance

### Contact
- contact / support

### Legal
- compliance / policy

### FAQ
- direct question answering

Title, description, H1, schema та internal links повинні відображати саме цей intent.

---

## 4. GEO & locale profile

До SEO generation визначити:

```text
country
country_code
locale
language
regional_language_variant
currency_if_relevant
city_if_relevant
legal_geo
search_geo
```

Examples:

### Portugal
```text
country: Portugal
country_code: PT
locale: pt-PT
language: Portuguese
regional_language_variant: European Portuguese
```

### Brazil
```text
country: Brazil
country_code: BR
locale: pt-BR
language: Portuguese
regional_language_variant: Brazilian Portuguese
```

### Poland
```text
country: Poland
country_code: PL
locale: pl-PL
language: Polish
```

Не використовувати `en-US` на PT-сайті лише тому, що WordPress або сервер мають англійський default.

---

## 5. HTML lang — blocking rule

Фінальний DOM повинен мати правильний:

```html
<html lang="pt-PT">
```

для Portuguese Portugal.

QA перевіряє **реальний frontend DOM**, не лише WordPress settings.

Якщо WordPress site language не відповідає Site Manifest:
- factory має встановити correct frontend language output;
- або виправити site locale під час provisioning, якщо це безпечно для проекту;
- admin locale не повинен випадково визначати SEO locale production frontend.

Blocking:
- content PT + `lang="en-US"` = FAIL.

---

## 6. Title generation

### Ціль
Title повинен:
- чітко описувати сторінку;
- містити primary topic;
- бути у природній мові GEO;
- бути унікальним;
- за потреби містити brand.

### Default formulas

Home:
```text
{Primary Topic / Value Proposition} | {Brand}
```

Domain page:
```text
{Specific Page Topic} | {Brand}
```

Strong entity page:
```text
{Topic} em {Entity} | {Brand}
```

Local-service page:
```text
{Service} em {City/Region} | {Brand}
```

### Length envelope

Default target:
- приблизно 45–60 characters;
- не обрізати зміст лише заради цифри;
- важливі слова — ближче до початку;
- brand можна прибрати, якщо він робить title неприродно довгим.

### Example

Weak:
```text
Progressão
```

Better:
```text
Progressão no Chicken Safari Jump | Salto Selvagem
```

---

## 7. Meta description

### Ціль
Description має:
- пояснювати користь сторінки;
- містити topic/entity природно;
- відповідати GEO language;
- не повторювати title;
- мати page-specific CTA/context.

### Target
Зазвичай:
- 135–160 characters;
- допускається відхилення, якщо текст природніший.

### Example

```text
Descobre como antecipar plataformas, corrigir mais cedo e manter a leitura do ritmo à medida que Chicken Safari Jump acelera.
```

Не використовувати однаковий description на кількох сторінках.

---

## 8. Meta keywords

`meta keywords` — legacy/audit compatibility field, а не основний SEO signal.

У factory SEO mode поле є **обов’язковим для кожної indexable page** як audit/browser-tool compatibility layer.

Required envelope:
- **minimum 16 terms/phrases**;
- normal target `16–24`;
- тільки релевантні конкретній сторінці;
- локалізовані під GEO/locale;
- page-specific, а не однаковий site-wide список;
- природна суміш entity/topic/feature/intent/context terms;
- без stuffing і без десятків майже однакових exact-match варіацій.

Example PT:

```text
Chicken Safari Jump, guia Chicken Safari Jump, jogo arcade, progressão, plataformas, controlos, touch, tilt, ritmo, obstáculos, pontuação local, guia em português, jogo móvel, mecânicas, dicas de jogo, Portugal
```

Do not inflate to 30–50 terms merely to increase count. Relevance and page intent remain mandatory.

Blocking audit rule for indexable pages:

```text
meta_keyword_term_count >= 16
```

Count comma-separated semantic terms/phrases after trimming empty values.

---

## 9. URL / slug

Slug:
- semantic;
- localized;
- lowercase;
- hyphen-separated;
- без stop-word stuffing;
- без IDs;
- без dates, якщо content evergreen.

Preferred runtime URL:

```text
/progressao/
```

Verified compatibility modes:

```text
/index.php/progressao/
?page_id=123
```

SEO profile must use the **actual verified reachable runtime URL**.

Priority:

```text
verified /slug/
→ verified /index.php/slug/
→ verified ?page_id=ID
```

A cosmetically cleaner URL that returns server 404 is never valid SEO output.

---

## 10. Canonical

Canonical:
- self-referencing for normal indexable pages;
- absolute;
- same protocol/domain;
- points to the verified reachable page;
- no tracking params;
- exactly one canonical tag;
- follows the selected verified runtime mode.

Priority:

```text
verified /slug/
→ verified /index.php/slug/
→ verified ?page_id=ID
```

Root-clean remains preferred, but reachability is mandatory.

Blocking:
- canonical on Home for unrelated internal pages;
- canonical on a stale/broken/unverified route;
- canonical on an old domain;
- multiple canonical tags;
- canonical mode different from the selected working runtime mode.

---

## 11. Robots

Default indexable page:

```text
index,follow,max-image-preview:large,max-snippet:-1,max-video-preview:-1
```

Noindex only when justified:
- admin/internal utility;
- staging;
- duplicate archive;
- thin search result;
- intentionally non-public page.

Не ставити `noindex` на важливу domain page випадково.

---

## 12. Author

Author визначається за content model.

### Editorial site
Якщо немає реального індивідуального автора:

```text
Salto Selvagem Editorial
```

або інша реальна назва editorial brand/team.

Не вигадувати:
- ім'я людини;
- посаду;
- credentials.

### Individual author
Тільки якщо:
- owner supplied;
- verified;
- реально відповідає content.

Author має бути узгоджений із schema.

### 12.1. Owner-directed editorial author

If the user explicitly supplies a real owner/editor name and states that this person conceived, directs, edits or publishes the site, the SEO profile may use that person as the editorial author:

```text
author_name = {owner_supplied_name}
author_status = OWNER_SUPPLIED
author_type = Person
```

Use consistently in:
- `<meta name="author">`;
- Article/WebPage `author` when semantically appropriate;
- visible byline/editorial credit when the page design includes one;
- Global Text `seo.author` / editorial identity branch.

This is a claim of editorial authorship/direction, not a claim that no automated tools were used.

Do not fabricate credentials or professional titles.

---

## 13. Publisher

Publisher = бренд/організація, що публікує website content.

Приклад:

```text
Salto Selvagem
```

Publisher не обов'язково дорівнює legal company name.

### Structured data
Допускається:

```json
{
  "@type": "Organization",
  "name": "Salto Selvagem",
  "url": "https://example.pt/"
}
```

`legalName`, address, phone та інші legal/business fields додаються тільки якщо VERIFIED / OWNER_SUPPLIED.

Не вигадувати юридичну особу заради Publisher field.

---

## 14. H1

Кожна indexable page:
- рівно один primary H1;
- H1 відповідає intent;
- H1 не повинен бути просто brand, якщо сторінка про конкретну тему.

Example:

```text
Progressão no Chicken Safari Jump
```

Не дублювати H1 у logo/header.

---

## 15. H2 / H3 hierarchy

### H2
Використовувати для основних змістових блоків.

Typical domain page:
- приблизно 4–8 H2.

### H3
Використовувати для підтем усередині H2.

Не використовувати heading tags лише заради styling.

Заборонено:
- H1 → H4 без логіки;
- 20 H2 з одним реченням;
- card title як H2, якщо це не section heading.

---

## 16. Image SEO

Кожен meaningful image:

```text
filename
alt
width
height
loading
context
```

### Filename
Semantic:

```text
chicken-safari-jump-progressao.svg
```

а не:

```text
img123.svg
```

### Alt
Описує visual/function.

Good:
```text
Mapa editorial da progressão vertical no Chicken Safari Jump
```

Bad:
```text
Chicken Safari Jump jogo Portugal melhor guia download
```

Decorative background:
```html
alt=""
```

або CSS background.

---


## 16.1. Image TITLE audit compatibility

Для factory-owned meaningful `<img>` final HTML повинен містити:

```html
<img
  src="..."
  alt="..."
  title="..."
>
```

`title`:
- localized під GEO;
- короткий;
- semantic;
- без keyword stuffing;
- не копіює довгий ALT word-for-word, якщо можна дати коротшу назву.

Example:

```html
<img
  src="/assets/img/control-radius.svg"
  alt="Schemat łodzi i zasięgu automatycznego łowienia"
  title="Zasięg automatycznego łowienia"
>
```

### Decorative visuals

Для decorative assets:
- віддавати перевагу CSS background;
- не створювати `<img>` лише як decorative filler;
- якщо `<img>` необхідний, він повинен мати explicit semantic/decorative classification у manifest.

Strict factory audit target:

```text
meaningful images missing ALT = 0
meaningful images missing TITLE = 0
```

---

## 17. Image dimensions

Rendered `<img>` по можливості має explicit width/height або інший стабільний aspect-ratio strategy для зменшення layout shift.

SVG:
- коректний `viewBox`;
- predictable aspect ratio.

Hero/social images:
- мати окрему social rendition, коли це потрібно.

---

## 18. Social metadata

Кожна важлива indexable page повинна мати:

```text
og:type
og:title
og:description
og:url
og:image
og:locale
og:site_name
```

### Default
Article-like domain page:

```html
<meta property="og:type" content="article">
```

Home:

```html
<meta property="og:type" content="website">
```

### PT example

```text
og:locale = pt_PT
```

Note:
HTML `lang` використовує `pt-PT`, Open Graph locale — `pt_PT`.

---

## 19. Twitter / X cards

Default:

```text
twitter:card = summary_large_image
twitter:title
twitter:description
twitter:image
```

Не вигадувати `twitter:site` handle, якщо його немає.

---

## 20. Social image

Default social asset:
- 1.91:1 ratio;
- орієнтовно 1200×630 equivalent;
- без дрібного тексту;
- brand/topic readable;
- page-specific where useful.

Не використовувати випадкову hero crop, якщо вона погано читається в social preview.

---

## 21. Structured data ownership

Schema повинна відповідати **видимому content**.

Base graph:

```text
WebSite
Organization
WebPage
BreadcrumbList
```

Content page:
```text
Article
```
або
```text
WebPage
```

залежно від фактичного format.

FAQ:
```text
FAQPage
```

тільки якщо FAQ питання/відповіді реально видимі на сторінці.

Contact:
```text
ContactPage
```

About:
```text
AboutPage
```

---

## 22. Organization schema

Safe fields:
- name;
- URL;
- logo;
- brand.

Conditional:
- email;
- telephone;
- address.

Contact fields додаються в schema тільки якщо:
- `VERIFIED`
- або `OWNER_SUPPLIED`.

`SYNTHETIC_GEO_CONTACT` data **не повинні потрапляти в production Organization/LocalBusiness contact fields** unless they become `OWNER_SUPPLIED` or `VERIFIED`.

---

## 23. BreadcrumbList

Internal page:

```text
Home > Section/Page
```

Deep architecture:

```text
Home > Library > Progression Guide
```

Breadcrumb schema та visible breadcrumb повинні збігатися.

---

## 24. GEO relevance

GEO keywords додаються лише коли вони реально впливають на intent.

### Informational game guide PT
Natural:
- "guia em português"
- "Portugal" у About/Contact/legal/contextual copy

Unnatural:
- вставляти "Portugal" у кожен H2;
- "Chicken Safari Jump Lisboa Porto Portugal" без search intent.

### Local business
GEO важливіший:
- city;
- region;
- service area;
- local phone/address;
- LocalBusiness schema, якщо business факти VERIFIED.

---

## 25. GEO keyword tiers

### Tier A — mandatory locale signals
- language;
- locale;
- country/legal GEO;
- correct spelling/variant.

### Tier B — contextual GEO
- country name;
- city/region, якщо page intent local.

### Tier C — forbidden stuffing
- список міст без content relevance;
- GEO repeated в every heading;
- fake service areas.

---

## 26. Internal linking

Кожна domain page:
- 3–8 contextual internal links;
- link to parent/related topic;
- link to at least one deeper/adjacent resource;
- no broken links;
- descriptive anchor text.

Bad:
```text
click here
```

Better:
```text
ver o guia de controlos
```

---


## 26.1. Link TITLE audit compatibility

Для factory-owned `<a>` final DOM повинен мати localized `title`.

Examples:

```html
<a href="/ulepszenia/" title="Otwórz poradnik ulepszeń">Ulepszenia</a>
<a href="#prawa" title="Przejdź do sekcji Prawa użytkownika">Prawa</a>
```

Rules:
- visible anchor text залишається descriptive;
- `title` уточнює destination/action;
- не keyword-stuff;
- не використовувати generic `Link`, `Kliknij tutaj`, `Read more` без context.

Runtime target:

```text
factory links missing TITLE = 0
```

---

## 27. External links

External link:
- тільки коли додає factual/source value;
- meaningful anchor;
- HTTPS;
- `rel="noopener noreferrer"` if opening new context;
- source distinction clear.

Не додавати external links лише заради link count.

---

## 28. Author / Publisher visible trust

Для editorial sites бажано мати visible trust block:

```text
Publicado por Salto Selvagem Editorial
Atualizado em {date}
Fonte factual principal: {source}
```

Якщо дата не підтримується реально — не генерувати fake "updated today".

---

## 29. SEO ownership mode

На сайті повинен бути один SEO owner.

### Mode A — Native Factory SEO
Theme/site factory генерує:
- title;
- meta description;
- canonical;
- robots;
- social;
- schema.

### Mode B — SEO plugin
Якщо активний Yoast / Rank Math / AIOSEO / SEOPress або інший SEO plugin:
- не дублювати canonical/meta/schema;
- factory використовує adapter або plugin-owned metadata flow;
- якщо adapter не підтримується — release блокується, поки не визначено ownership.

Blocking:
- два canonical;
- два conflicting meta descriptions;
- два Organization schema graphs із різними даними.

---

## 30. WordPress title runtime

Final `<title>` перевіряється в browser DOM.

Не достатньо мати WordPress page title.

Expected:
```text
Progressão no Chicken Safari Jump | Salto Selvagem
```

а не:
```text
Progressão – domain.org
```

якщо Page SEO Profile задає інший optimized title.

---

## 31. WordPress language runtime

Final source:
```html
<html lang="pt-PT">
```

Не покладатися лише на:
```text
Content-Language
```

або page copy.

---

## 32. Meta description runtime

У `<head>` рівно один:

```html
<meta name="description" content="...">
```

Description має збігатися з Page SEO Profile.

---

## 33. Robots runtime

У `<head>` рівно один coherent robots state.

Example:

```html
<meta name="robots" content="index,follow,max-image-preview:large,max-snippet:-1,max-video-preview:-1">
```

---

## 34. Sitemap

Production indexable site:
- XML sitemap доступний;
- містить canonical indexable pages;
- не містить staging/test pages;
- використовує URLs тільки з selected verified runtime mode;
- не містить old managed pages;
- legal pages можуть бути включені, якщо indexable за Site Manifest.

Factory може використовувати WordPress core sitemap або SEO-plugin sitemap, але не генерувати конфліктні дублікати без причини.

---

## 35. robots.txt

Production:
- не блокувати CSS/JS/images, потрібні для rendering;
- sitemap reference;
- не блокувати весь site випадково.

Staging:
- noindex/password strategy визначається deployment profile.

---

## 36. Favicon / site icon

Production site має:
- site icon / favicon that actually resolves in final public `<head>`;
- consistent current-site brand mark;
- valid MIME/decode;
- adequate square resolution/renditions;
- no stale previous-project icon;
- theme fallback when WordPress Site Icon is not configured.

Це не ranking field, але входить у quality/identity QA.

---

## 37. Page-specific uniqueness

Для кожної indexable page повинні бути унікальні:

- title;
- description;
- H1;
- primary intent;
- canonical;
- OG title/description;
- internal-link pattern.

Не генерувати один SEO template, де змінюється лише одне слово.

---

## 38. Keyword map

До BUILD створити keyword/intent map:

| Page | Primary topic | Secondary topics | GEO modifier | Intent |
|---|---|---|---|---|
| Home | Chicken Safari Jump guide | controls, safari, progression | PT / Portuguese | overview |
| Guide | Chicken Safari Jump guide | route, platforms | Portuguese | informational |
| Controls | touch vs tilt | input, sensitivity | Portuguese | informational |
| Progression | progression | speed, anticipation | Portuguese | informational |
| Contact | site contact | app support | Portugal | navigational |

Одна primary topic не повинна без потреби конкурувати на 5 сторінках.

---

## 39. SEO copy anti-patterns

FAIL:
- keyword stuffing;
- city stuffing;
- exact same title pattern на всіх сторінках;
- fake "best", "#1", "official";
- title unrelated to H1;
- description unrelated to page;
- English meta on PT content;
- author/publisher invented;
- brand repeated 4–5 times у title/description;
- meta keywords generated як spam list.

---

## 40. GEO language quality

SEO text має використовувати regional language.

PT-PT examples:
- `contacto`
- `utilização`
- `ficheiro`
- `telemóvel`, якщо доречно

Не змішувати системно pt-BR та pt-PT без причини.

---

## 41. SEO audit blocking gates

Release FAIL якщо на indexable page:

- title missing;
- meta description missing;
- canonical missing;
- canonical wrong;
- robots contradictory;
- H1 count ≠ 1;
- final DOM lang wrong;
- author missing у editorial profile;
- publisher missing;
- duplicate title/description у key pages;
- social title/description missing;
- OG locale wrong;
- important images missing alt;
- factory-owned meaningful images missing title;
- factory-owned links missing title;
- broken internal links;
- sitemap missing/broken у production;
- SEO ownership conflict.

---

## 42. Runtime SEO crawl

Для кожної managed page збирати:

```text
HTTP status
final URL
title
description
keywords
keyword_term_count
canonical
robots
author
publisher
lang
H1 count
H2 count
H3 count
image count
images missing alt
images missing title
internal link count
broken link count
links missing title
og:title
og:description
og:image
og:locale
twitter:card
schema types
sitemap presence
```

Потім порівняти із Site Manifest / SEO Page Profile.

---

## 43. Quality targets for the audit shown by SEO browser tools

Для нормальної content page очікувати приблизно:

```text
Title: meaningful + unique
Description: meaningful + unique
Keywords: 16–24 page-specific terms/phrases for audit compatibility
URL: semantic slug
Canonical: exact final URL
Robots: index/follow unless intentionally otherwise
Author: editorial brand or verified person
Publisher: site brand/organization
Lang: exact GEO locale
H1: 1
H2: 4–8 typical
H3: as structurally needed
Images: enough for page format; meaningful IMG ALT/TITLE complete
Links: contextual, working, useful; factory-owned A TITLE complete
```

Не оптимізувати сайт під цифри самого audit tool, якщо це погіршує content quality.

---

## 44. Example — Progressão / Portugal

```text
PAGE
Progressão

PRIMARY TOPIC
progressão no Chicken Safari Jump

GEO
Portugal

LOCALE
pt-PT

TITLE
Progressão no Chicken Safari Jump | Salto Selvagem

DESCRIPTION
Descobre como antecipar plataformas, corrigir mais cedo e manter a leitura do ritmo à medida que Chicken Safari Jump acelera.

KEYWORDS
Chicken Safari Jump, progressão, plataformas, jogo arcade, guia PT, touch, tilt

URL
https://example.pt/progressao/

CANONICAL
https://example.pt/progressao/

ROBOTS
index,follow,max-image-preview:large,max-snippet:-1,max-video-preview:-1

AUTHOR
Salto Selvagem Editorial

PUBLISHER
Salto Selvagem

LANG
pt-PT

H1
Progressão no Chicken Safari Jump

H2
5–7 thematic sections

OG LOCALE
pt_PT
```

---

## 45. Release state

SEO state:

```text
SEO_PROFILE_PLANNED
SEO_STATIC_PASS
SEO_RUNTIME_PASS
SEO_RELEASE
```

Final production site не отримує `SEO_RELEASE`, поки browser/runtime crawl не підтвердить фактичні rendered fields.

---

## 46. Factory learning

Кожен SEO defect:

```text
SEO DEFECT
→ ROOT CAUSE
→ SEO RULE
→ RUNTIME CHECK
→ REGRESSION CASE
```

Known regression examples:
- PT site rendered `lang=en-US`;
- page title залишився WordPress default;
- Author / Publisher missing;
- canonical pointed to a broken/unverified URL or did not match the selected runtime mode;
- duplicate meta descriptions;
- social metadata missing;
- SEO plugin + theme generated duplicate canonical/schema.

Ці класи дефектів не повинні повторюватись.

---

## 47. Rendered audit zero-miss rule (v4.4 patch)

Quality target values are not aspirational — they are release blockers.

Required final state:
- missing meaningful image ALT = `0`;
- missing meaningful image TITLE = `0`;
- missing factory-owned link TITLE = `0`;
- missing Author = `0` for pages/types where factory owns it;
- missing Publisher = `0` where factory owns it;
- missing Keywords = `0` in factory SEO mode;
- indexable page keyword term count `< 16` = `FAIL`;
- duplicated site-wide keyword list on unrelated page intents = `FIX_REQUIRED`.

## 48. Attachment inheritance rule

If WordPress generates multiple rendered image instances/sizes, all meaningful visible instances must inherit a localized semantic alt/title plan from the source asset.

Hash-like filenames or transformed versions are not an excuse for missing attributes.

## 49. Link title generation patch

Factory must centralize link title generation for:
- header nav links;
- footer links;
- CTA links;
- card links;
- legal links.

The goal is audit compatibility **without** spam.


---

## 50. Canonical follows verified reachable mode

Canonical must point to the URL that actually resolves to the intended managed page on the target host.

Priority:

```text
verified /slug/
→ verified /index.php/slug/
→ verified ?page_id=ID
```

Never emit a root-clean canonical if that route returns raw server 404.

If compatibility mode is selected:
- OG URL follows the same canonical;
- sitemap uses the same reachable page URL;
- internal link plan uses the same mode;
- no mixed clean/broken URL graph.

Preferred SEO state remains root-clean, but reachability is mandatory.

---

## v4.5.11 patch — complete image/link title coverage

### 1. Final image attribute generation
For every meaningful visible image generate localized final values:
```text
final_alt
final_image_title
```

These must be attached to every rendered image instance, not only the source asset record.

### 2. Final link title generation
For every factory-owned link generate:
```text
final_link_title
```

This includes:
- internal nav;
- buttons/CTAs;
- image wrappers;
- attribution/source links;
- footer/legal links;
- skip links.

### 3. Filename blindness rule
Never use a hash-like filename as the semantic source for ALT or TITLE.
If the rendered asset filename looks like a hash, semantic metadata still comes from page + section + subject context.

### 4. Title-writing style
Image TITLE:
- short;
- human-readable;
- localized;
- section-aware.

Link TITLE:
- action-oriented;
- human-readable;
- localized;
- destination-aware.

### 5. Release target reiteration
Required final public rendered state:
```text
meaningful images missing ALT = 0
meaningful images missing TITLE = 0
factory-owned links missing TITLE = 0
```


---

## 51. SEO text resolves from Global Text (v4.4.8)

All factory-owned textual SEO fields must be represented in `global-text.json`.

Recommended keys:

```text
seo.pages.home.title
seo.pages.home.description
seo.pages.home.keywords
seo.pages.guide.title
seo.pages.guide.description
seo.author
seo.publisher
seo.og.*
seo.twitter.*
images.{asset_id}.alt
images.{asset_id}.title
links.{link_key}.title
accessibility.*
```

Canonical URLs, robots directives, schema types and structural IDs remain machine/runtime data, but any visible/human-readable textual values used by them should resolve from Global Text.

### Single-source rule

Do not generate one ALT/TITLE in the image manifest and a second unrelated literal in the template.

Image/Link engines provide semantic intent; SEO finalizes localized text into Global Text; runtime consumes that same key.

### SEO edit behavior

Editing a valid SEO text key in `global-text.json` must update the corresponding server-rendered head/attribute on the next uncached request without rebuilding the theme.

### Safety

SEO output still passes:
- escaping;
- length/quality review;
- locale;
- uniqueness;
- no keyword stuffing.

Global editability does not waive SEO QA.



## 44. Browser SEO parity patch (v4.4.9)

Native Factory SEO must satisfy both semantic structured data and common browser SEO field inspection.

### Explicit Author / Publisher
On indexable editorial pages emit browser-readable metadata for:
```html
<meta name="author" content="…">
<meta name="publisher" content="…">
```
while keeping JSON-LD publisher/Organization coherent.

Schema alone is not sufficient when browser inspection reports Publisher missing.

### Single robots owner
Exactly one system owns the final robots meta.

In Native Factory SEO mode:
- disable/adapt duplicate WordPress core or plugin robots output;
- emit exactly one coherent robots state;
- normal public indexable target remains:
  `index,follow,max-image-preview:large,max-snippet:-1,max-video-preview:-1`;
- 404/non-index states remain page-specific.

A partial directive shown because another robots tag won precedence is FAIL.

### Description quality
For normal indexable content pages:
- natural target remains about `135–160` characters;
- descriptions materially below about `120` characters require a real page-format reason;
- Home, Guide, Contact, About and key domain pages should not use generic one-sentence stubs when richer accurate intent is available.

### Title quality
For standard indexable pages, roughly `45–60` characters is a useful default target where natural. Short legal/utility titles may be justified, but key domain pages should communicate the actual topic/entity rather than only a generic label.

### Browser parity QA
Record from final DOM:
```text
author
publisher
robots_tag_count
robots_value
description_length
title_length
```
Field presence in source templates or JSON-LD does not substitute for this rendered check.



## 45. Rich-content SEO separation (v4.5.0)

Increased page depth must not create keyword cannibalization or repetitive SEO copy.

For every deep page:
- retain one clear primary intent;
- map secondary topics to supporting sections;
- avoid repeating the Home's entire topic set on every internal page;
- ensure internal anchors reflect the specific destination topic;
- do not increase keyword frequency merely because body copy is longer;
- keep title/description concise even when the page body is extensive.

`CONTENT DEPTH MANIFEST` and `SEO PAGE PROFILE` must agree on the page's primary intent.



## 46. OFFICIAL GAME STUDIO SEO / ENTITY MODEL (v4.5.1)

When `business_model_mode = OFFICIAL_GAME_STUDIO` and the developer relationship is owner-supplied/verified, SEO/entity output must represent a coherent `Studio → Game` relationship rather than an independent editorial publisher.

### Required entity profile

```text
studio_brand
studio_brand_source
game_name
business_model_mode
developer_relationship_status
site_publisher = studio_brand
product_creator_claim_allowed
official_store_url
```

The domain-derived studio brand is a public brand identity, not automatically a registered legal company. Do not add unsupported legal suffixes, address, founding date, employee count or corporate registration data.

### Metadata direction
When creator claims are allowed, page titles/descriptions may naturally express relationships such as:
- `{Game} by {Studio}`;
- `Discover {Game}, created by {Studio}`;
- `How we designed {mechanic} in {Game}`;
- `{Studio} — creators of {Game}`.

Do not use `official`, `created by us`, `our game`, or equivalent creator wording when `developer_relationship_status` is unresolved/conflicting.

### Author / Publisher
For official studio/product pages:
- Publisher should normally be the studio/site brand;
- Author may be the studio team/brand or an owner-supplied person where semantically appropriate;
- do not default to `{Brand} Editorial` merely because older editorial templates used that convention.

### Structured data
Where supported by the chosen schema graph, represent the studio/organization and game/application as separate entities and connect creator/developer/publisher relationships only when the relationship is owner-supplied or verified.

Never manufacture:
- legal company registration;
- founding date;
- employee count;
- headquarters;
- awards;
- aggregateRating/reviewCount;
- release/update facts not supported by source/owner data.

### Search intent
Page-specific keyword sets remain mandatory under factory SEO mode, but they should support the commercial/product model:
- game name + studio;
- gameplay/mechanics;
- official download/play intent where truthful;
- development/process topics;
- support/FAQ intent;
- platform/store context.

Avoid affiliate/review phrasing that contradicts first-party studio ownership.



## 47. STUDIO STORY PAGE SEO + ENTITY INTENT (v4.5.2)

For `OFFICIAL_GAME_STUDIO`, page SEO must reflect each creator/product job rather than reuse a generic game-guide pattern.

### About / Studio intent
When creator relationship is resolved, valid directions include localized equivalents of:

```text
{Studio} — the studio behind {Game}
About {Studio} and {Game}
Meet the team/studio behind {Game} — only if team wording is truthful
How {Studio} approaches {Game}
```

Avoid `independent guide`, `editorial portal`, `review site` language in this mode.

### Development-page intents
Potential page intents, only when the page exists and evidence supports the wording:

```text
How we built {Game}
Designing {mechanic} in {Game}
How {mechanic} works in {Game}
Level and progression design in {Game}
Controls and feel in {Game}
Art direction of {Game}
Testing and balancing {Game}
```

`How we built`, `we designed`, `our process` require the creator relationship plus claim-level evidence appropriate to the actual sentence.

### Entity continuity
Across Home/About/Development/Product pages:
- `studio_brand` remains the same publisher/site organization;
- `game_name` remains the same product entity;
- each page has a distinct primary intent;
- internal links form a creator/product knowledge graph, not a set of isolated SEO landing pages.

Recommended internal-link graph:

```text
ABOUT → GAME / DEVELOPMENT
GAME → MECHANICS / CONTROLS / PLAY
DEVELOPMENT → GAME / MECHANICS / ART / PLAY
MECHANICS → DEVELOPMENT / GAME / PLAY
FAQ/SUPPORT → GAME / STORE / CONTACT
```

### Keyword direction
Maintain the global 16–24 relevant term target, but vary by page role:
- studio/about terms;
- game/product terms;
- mechanic/system terms;
- development/process terms;
- support/platform terms.

Do not repeat the same `game + studio + download` keyword list on every page.


## 48. NAVIGATION LABELS ARE PRESENTATION, NOT SEO IDENTITY (v4.5.3)

Randomized navigation/page-display naming must not destabilize SEO or URLs.

For every managed page keep separate:

```text
nav_label
page_display_title
seo_title
meta_description
canonical_slug
page_key
```

Rules:
- `nav_label` may be a short synonym such as `Our Studio`;
- H1 may be a longer natural page title;
- SEO title remains intent/entity optimized;
- canonical/slug remains stable unless an explicit migration is requested;
- breadcrumb label may follow the page display-title family or a dedicated concise breadcrumb value, but must remain semantically consistent;
- changing only a navigation Global Text key never triggers an automatic canonical/slug rewrite.

SEO QA checks the destination/page intent, not whether the menu uses the canonical word `About`, `Game`, `FAQ` or `Contact`.

<!-- BUNDLE-MODULE-END: 14-SEO-GEO-METADATA-ENGINE.md -->

---

<!-- BUNDLE-MODULE-START: 17-GLOBAL-TEXT-ENGINE.md -->

# LEGACY MODULE: 17-GLOBAL-TEXT-ENGINE.md

# GLOBAL TEXT ENGINE

**Version:** 1.2.0  
**Role:** one persistent editable source for all factory-owned public frontend text
**Authoritative file:** `global-text.json`

---

## 1. Goal

Every generated site must let the user edit public wording from one filesystem file without rebuilding the theme and without editing WordPress page content manually.

The editable runtime file is:

```text
/wp-content/uploads/site-factory/{theme_package_slug}/global-text.json
```

This path is intentionally outside the replaceable theme directory so WordPress theme updates do not erase user edits.

---

## 2. Runtime source of truth

After first provisioning:

```text
PERSISTENT global-text.json
→ GLOBAL TEXT LOADER
→ PHP TEMPLATES / HEAD / ATTRIBUTES / JS UI STRINGS
→ RENDERED SITE
```

The theme may ship a seed/default tree only for:
- first initialization;
- introducing newly required keys after an update.

The seed is **not** authoritative once the persistent file exists.

---

## 3. What belongs in Global Text

All factory-owned public frontend text:

### Site / identity
- brand display name;
- tagline;
- editorial label;
- source disclosure wording.

### Navigation
- menu labels;
- breadcrumbs;
- eyebrow labels;
- skip-link label.

### Pages
- H1/H2/H3;
- paragraphs;
- lists;
- cards;
- tables' human-readable labels/cells when content copy;
- CTA/button labels;
- FAQ;
- reviews/testimonials;
- disclosures.

### Contact
- public display email;
- phone display;
- address lines;
- visible contact labels/copy.

### Legal
- Privacy;
- Terms;
- Cookies;
- consent banner;
- preference modal;
- visible legal notices.

### SEO / semantics
- title;
- meta description;
- meta keywords;
- author/publisher text;
- OG/Twitter text;
- image ALT;
- image TITLE;
- link TITLE;
- ARIA labels;
- JS-rendered messages.

### Global UI
- footer;
- 404;
- empty states;
- accordions/tabs labels;
- form labels/messages when forms exist.

---

## 4. What does NOT belong

Do not use Global Text as a generic config dump.

Keep these in manifests/runtime code:
- URLs and canonical slugs;
- WordPress page IDs;
- permalink mode;
- CSS classes/tokens;
- asset file paths;
- PHP callbacks;
- JS selectors;
- schema property/type names;
- booleans and permissions;
- secrets/passwords/API keys;
- private/internal diagnostics.

Public email/phone/address may be editable text values, but verification/status remains in Contact Profile.

---

## 5. File structure

Use a predictable hierarchy.

Reference shape:

```json
{
  "_schema_version": "1.0",
  "entities": {
    "brand": "Pankowers",
    "product_name": "Scream Go Stickman",
    "country_name": "Portugal"
  },
  "site": {
    "tagline": "Guia independente em português"
  },
  "navigation": {
    "_location": "Header and mobile navigation",
    "home": "Início",
    "guide": "Guia",
    "about": "Sobre",
    "contact": "Contacto"
  },
  "pages": {
    "home": {
      "_location": "Homepage",
      "hero": {
        "_location": "Home > Hero",
        "eyebrow": "GUIA PT",
        "title": "Controla o salto com a tua voz",
        "body": "Aprende a dosear som, ritmo e timing.",
        "cta_primary": "Começar pelo guia"
      },
      "sections": {
        "controls": {
          "_location": "Home > Controls section",
          "heading": "A voz funciona como comando",
          "paragraphs": [
            "Um som mais baixo ajuda a avançar.",
            "Um impulso mais forte desencadeia o salto."
          ]
        }
      }
    }
  },
  "components": {
    "reviews": {},
    "cookie": {}
  },
  "contact": {},
  "legal": {
    "privacy": {},
    "terms": {},
    "cookies": {}
  },
  "footer": {},
  "errors": {
    "404": {}
  },
  "seo": {
    "pages": {}
  },
  "images": {},
  "links": {},
  "accessibility": {}
}
```

Reserved keys beginning with `_` are editor metadata and never render.

---

## 6. Key naming

Use stable semantic dot paths.

Good:

```text
pages.home.hero.title
pages.guide.sections.controls.heading
components.cookie.banner.accept
legal.privacy.sections.data.heading
images.home_hero.alt
links.header.guide.title
```

Bad:

```text
text1
block_12
heading_new
final_copy_2
```

Keys survive wording changes.

---

## 7. Text-only data model

The file should contain text and text collections, not presentation markup.

Preferred:

```json
{
  "heading": "Como funciona",
  "paragraphs": [
    "Primeiro parágrafo.",
    "Segundo parágrafo."
  ],
  "bullets": [
    "Primeiro ponto",
    "Segundo ponto"
  ]
}
```

Avoid raw HTML in editable strings.

Templates own:
- `<h2>`;
- `<p>`;
- `<ul>`;
- links/components;
- layout.

This keeps the file safe and easy to edit in FastPanel.

---

## 8. Entity interpolation

To avoid repeating global entities, support explicit placeholders.

Example:

```json
{
  "entities": {
    "brand": "Pankowers",
    "product_name": "Scream Go Stickman"
  },
  "pages": {
    "guide": {
      "hero": {
        "title": "Guia de {product_name}"
      }
    }
  },
  "footer": {
    "copyright": "© {year} {brand}"
  }
}
```

Allowed placeholder values come from an allowlisted interpolation context.

Unknown placeholder:
- log;
- preserve visibly in diagnostic mode or resolve safely;
- fail QA.

Never evaluate PHP/code from JSON.

---

## 9. Runtime loader requirements

Implement equivalent behavior to:

```text
global_text_load()
global_text(path, vars = {})
global_text_array(path)
global_text_attr(path)
```

### Load once per request

Use a static in-request parsed tree.

### Detect edits

Track:
- `filemtime`;
- content hash.

On valid change:
- parse;
- validate;
- update last-known-good snapshot/hash;
- invalidate relevant factory caches;
- fire `factory_global_text_changed`.

### UTF-8

File must be UTF-8 without unsafe binary content.

---

## 10. Context-aware escaping

Global Text is editable input and must be escaped at output.

Use equivalent context handling:

```text
text node    → esc_html
attribute    → esc_attr
textarea     → esc_textarea
URL target   → not sourced from Global Text by default
structured   → JSON encode safely
```

Do not output raw editable HTML by default.

---

## 11. Persistent initialization and update merge

### First install

If persistent file does not exist:

```text
theme seed
→ validate
→ create persistent global-text.json
→ store schema version/hash
```

### Theme update

If persistent file exists:

```text
new seed
+
existing persistent tree
→ recursive missing-key merge
→ existing user values win
→ validate
→ save only when new keys were added
```

Never overwrite an existing key value automatically.

### Removed/deprecated keys

Do not automatically delete user data.

Mark deprecated keys in schema/state and ignore them if no longer rendered.

---

## 12. Last-known-good resilience

Maintain:

```text
last_good_hash
last_good_data
last_good_timestamp
```

If current JSON cannot parse:

```text
GLOBAL_TEXT_INVALID
→ render last-known-good
→ admin notice with exact parse error
→ no public fatal
```

If no last-known-good exists:
- use validated theme seed;
- report blocking diagnostic.

---

## 13. Missing-key behavior

Required-key schema is generated with the site.

If key is missing:
1. look for that key in last-known-good;
2. if available, use previous value + log warning;
3. otherwise use controlled safe empty/default;
4. record `GLOBAL_TEXT_MISSING_KEY:{path}`;
5. block RELEASE.

Explicit empty string is different from missing key and may intentionally render blank when the component allows it.

---

## 14. WordPress page model

WordPress managed pages provide:
- page identity;
- status;
- slug;
- routing;
- page key.

They must not be the only runtime copy source.

Public component/body text resolves from Global Text.

If the factory synchronizes `post_title` for admin convenience, that sync is secondary and must not become authoritative over Global Text.

---

## 15. JavaScript UI text

Do not hardcode factory UI strings inside JS.

Pass required text subset server-side:

```text
global-text.json
→ PHP loader
→ JSON-encoded JS config
→ modal/menu/consent interactions
```

Examples:
- cookie button labels;
- modal labels;
- validation messages;
- accessibility announcements.

---

## 16. SEO / image / link integration

One semantic value must not fork into multiple conflicting literals.

Flow:

```text
CONTENT / IMAGE / SEO INTENT
→ finalized localized Global Text key
→ rendered DOM/head
→ runtime crawl
```

Examples:

```text
images.home_hero.alt
images.home_hero.title
links.header.guide.title
seo.pages.home.title
seo.pages.home.description
```

---

## 17. Contact integration

Editable display values:

```text
contact.public_email
contact.phone_display
contact.address_lines
```

Status and verification remain outside Global Text.

A text edit:
- changes display;
- does not automatically grant `VERIFIED` status;
- does not make a synthetic contact legally authoritative.

When interaction is allowed:
- `mailto:` derives from the editable email;
- `tel:` derives via normalization rules.

---

## 18. FastPanel workflow

The user should be able to:

```text
FastPanel
→ File Manager
→ wp-content
→ uploads
→ site-factory
→ {theme_package_slug}
→ global-text.json
→ edit
→ save
→ refresh site
```

No ZIP rebuild.
No PHP edit.
No page-builder edit.
No DB edit.

The theme should expose this path in an admin diagnostic/help panel.

---

## 19. Cache behavior

On a normal uncached WordPress request, valid saved changes should appear immediately.

When external full-page caching exists:
- factory change hook should purge supported caches when possible;
- QA must verify;
- do not promise instant appearance through a cache layer the theme cannot control.

Never disable all caching globally just to implement Global Text.

---

## 20. Static hardcoded-copy audit

Before release scan:
- PHP templates;
- component renderers;
- JS UI source.

Factory-authored public text literal = FAIL unless specifically allowlisted as technical/debug data.

Target:

```text
HARDCODED_EDITABLE_PUBLIC_TEXT = 0
```

---

## 21. Runtime coverage audit

Crawler maps rendered text-bearing elements to expected source roles.

Minimum checks:
- header;
- mobile nav;
- Home;
- every managed page;
- footer;
- legal;
- cookie UI;
- reviews;
- contact;
- 404;
- SEO head;
- image alt/title;
- link title;
- JS modal labels.

Target:

```text
GLOBAL_TEXT_REQUIRED_KEYS_PRESENT = 100%
```

---

## 22. Visual edit-resilience audit

Test longer replacements for:
- H1;
- H2;
- CTA;
- navigation;
- FAQ;
- legal paragraphs.

The design must remain usable/responsive.

---

## 23. Security rules

`global-text.json` contains public copy only.

Never store:
- credentials;
- API keys;
- private customer data;
- secret tokens;
- admin-only confidential notes.

Even if the file is directly web-readable, it must contain nothing more sensitive than text already intended for public site output.

---

## 24. Release gate

`GLOBAL_TEXT_PASS` requires:

```text
persistent file exists
JSON parses
schema version valid
required keys complete
hardcoded editable frontend text = 0
FastPanel edit propagation = PASS
theme-update preservation = PASS
invalid-JSON fallback = PASS
SEO/image/link semantic integration = PASS
responsive long-text test = PASS
```

Otherwise:

```text
FIX_REQUIRED
```

---

## 25. Footer bottom-bar text contract (v1.0.2)

Every full site seed must include editable footer bottom-bar strings.

Recommended structure:
```json
{
  "footer": {
    "bottom_bar": {
      "copyright": "© {year} {brand}.",
      "rights_reserved": "All rights reserved."
    }
  }
}
```

Both values are localized to the target locale.
The renderer may combine them into one compact visual line.

Rules:
- `{year}` resolves from the current runtime year;
- `{brand}` resolves from the allowlisted brand entity;
- wording must not invent a legal company/operator;
- manual user edits remain preserved by the normal persistent merge rules.

Image provenance/source URLs do **not** belong in public Global Text merely because an image was sourced from the web. They stay in the internal asset/provenance manifest unless visible licence attribution is required.



## 18. Rich long-form storage contract (v4.5.0)

Expanded content remains fully editable through the persistent Global Text tree.

For long informational pages prefer structured branches:

```text
pages.{page}.hero
pages.{page}.sections.{section_key}.heading
pages.{page}.sections.{section_key}.lead
pages.{page}.sections.{section_key}.paragraphs[]
pages.{page}.sections.{section_key}.items[]
pages.{page}.sections.{section_key}.definitions[]
pages.{page}.sections.{section_key}.notes[]
```

Do not move hundreds of words back into hardcoded PHP because the page became deeper.
Templates own structure; Global Text owns factory-authored visible wording.



## 21.1. Editorial identity keys

When owner-directed identity is configured, keep public credit text editable in Global Text:

```text
entities.editorial_owner
site.editorial_credit
seo.author
pages.about.editorial_identity.heading
pages.about.editorial_identity.body
footer.editorial_credit  # opt-in only when the active business model truly needs visible footer credit
```

Status (`OWNER_SUPPLIED`, verification state, legal-identity eligibility) remains outside Global Text.

---

## 22. Interactive UI text ownership (v1.2.0)

All factory-authored visible interaction strings belong in `global-text.json`, including:
- slider previous/next labels;
- slide position/status text when visible or announced;
- tab labels;
- accordion headings and optional expand/collapse wording;
- filter/sort labels;
- comparison switcher labels;
- lightbox close/next/previous labels;
- accessible instructions/status messages.

ARIA-only labels are still public user-facing text and therefore use Global Text rather than hardcoded English literals.



## 23. Official Game Studio business-model keys (v1.3.0)

When `OFFICIAL_GAME_STUDIO` is active, keep the complete public creator/product narrative editable through Global Text. Recommended keys include:

```text
entities.studio_brand
entities.game_name
business_model.mode
business_model.studio_tagline
business_model.game_value_proposition
business_model.creator_voice_label
pages.home.product_story.*
pages.game.*
pages.development.*
pages.about.studio_story.*
pages.about.creation_philosophy.*
pages.support.*
cta.play_game
cta.download_game
cta.visit_store
cta.see_how_we_built_it
seo.publisher
seo.author
footer.studio_product_line  # optional compact phrase; omit by default
```

Machine truth fields such as `developer_relationship_status`, ownership evidence, schema eligibility and legal operator status remain outside Global Text. Editing copy must not silently upgrade an unresolved relationship into verified ownership.


## 24. Navigation copy persistence + role mapping (v1.4.0)

Selected randomized navigation wording is public editable copy and therefore lives in persistent Global Text.

Recommended keys:

```text
navigation.home
navigation.about
navigation.game
navigation.development
navigation.mechanics
navigation.progression
navigation.controls
navigation.art
navigation.faq
navigation.support
navigation.contact
navigation.updates
navigation.play_store
```

Only keys for pages/actions actually present in the Site Manifest are required.

Optional compact variants when explicitly planned:

```text
navigation_compact.{page_key}
```

Machine selection metadata does **not** belong in Global Text. Keep these in the Navigation Copy Manifest/site state:

```text
navigation_copy_nonce
semantic_role
candidate_pool
selected_family
rejection_reasons
```

### Update behavior

If `global-text.json` already contains a valid user-edited navigation value, theme update must preserve it even when the factory seed contains a different randomly selected default.

### Example

```text
navigation.about = "Our Studio"
pages.about.hero.title = "Meet the studio behind {game_name}"
seo.pages.about.title = "About {studio_brand} and {game_name}"
```

These three strings may differ intentionally while resolving to the same stable page identity.


## 18. Navigation lexical-variation persistence (v1.2.1)

Navigation labels are editable public text, but their **initial factory selection** comes from the locale-aware Navigation Copy Engine.

Store selected labels under stable semantic keys, for example:

```text
navigation.home
navigation.about_studio
navigation.game_product
navigation.development
navigation.mechanics
navigation.faq
navigation.support
navigation.contact
```

The key names remain stable even when the visible values differ between sites. The values are generated in the site's resolved locale; PT-PT below is only an example, not a special case:

```text
navigation.about_studio = "Sobre nós" | "O estúdio" | "Quem somos" | "A nossa história"
navigation.development = "Desenvolvimento" | "Nos bastidores" | "Criação do jogo" | "O processo"
navigation.contact = "Contacto" | "Fale connosco" | "Escreva-nos" | "Contactar o estúdio"
```

Do not infer page identity from the rendered label. Runtime linking uses stable page keys/IDs.

Same-site updates preserve existing values. New-site selection must not overwrite manual Global Text edits and must not canonicalize all same-locale sites to one default vocabulary.



## 19. Universal locale navigation text contract (v1.2.2)

`navigation.*` values are initialized from `NAVIGATION_LOCALE_LEXICON` for the resolved locale of the current site.

Global Text stores only the chosen human-readable values. Machine metadata such as locale pools, rejected candidates, nonces and lexical fingerprints remains outside `global-text.json`.

Required invariant:

```text
resolved navigation locale == site content locale
navigation values = native/regional wording for that locale
page identity != inferred from visible label
```

Do not seed English fallback labels merely because a locale does not have a prewritten curated pack. The Content Engine must synthesize and validate a native pool first.

Same-site manual edits still win over future factory seeds.

<!-- BUNDLE-MODULE-END: 17-GLOBAL-TEXT-ENGINE.md -->

---



## 20. Footer Global Text minimalism contract (v1.2.3)

Global Text may store optional footer descriptor/credit keys, but **presence of a key does not require rendering it**. Footer rendering follows the active footer content policy.

Recommended minimal branch:
```text
footer.navigation.*
footer.contact.*          when present
footer.store_link.*       when present
footer.legal.*
footer.bottom_bar.copyright
footer.bottom_bar.rights_reserved
```

Optional only:
```text
footer.descriptor
footer.editorial_credit
footer.studio_product_line
```

For `OFFICIAL_GAME_STUDIO` default seed:
```text
footer.descriptor = omitted
footer.editorial_credit = omitted
footer.studio_product_line = omitted unless a short useful creator/product phrase is deliberately selected
```

Never seed an independent-guide/review/editorial disclaimer into an official-studio footer. SEO/source methodology belongs in the appropriate page/head/internal manifest, not as filler footer prose.


## 21. CLEAN GAMING SEO + GLOBAL TEXT EXCLUSION CONTRACT (v1.2.4)

When `clean_gaming_mode = REQUIRED` and authoritative source relevance to gambling is `NONE`, all factory-owned SEO and Global Text must remain semantically free of gambling/casino/betting associations.

Required public state:

```text
seo_gambling_concept_mentions = 0
meta_keyword_gambling_terms = 0
social_gambling_concept_mentions = 0
schema_human_text_gambling_mentions = 0
global_text_gambling_concept_mentions = 0
negative_gambling_disclaimers = 0
```

### Covered fields

Audit at minimum:
- `seo.pages.*.title`;
- `seo.pages.*.description`;
- `seo.pages.*.keywords`;
- `seo.og.*`;
- `seo.twitter.*`;
- author/publisher-adjacent visible text;
- navigation/breadcrumb/CTA copy;
- page headings/body/FAQ;
- footer branches;
- legal/cookie branches;
- images `alt` / `title`;
- links `title`;
- accessibility/ARIA strings;
- errors/404;
- human-readable schema values.

### No negative SEO targeting

Do not add casino/gambling/betting/wagering terms as:
- negative-comparison keywords;
- `not casino` / `not gambling` search phrases;
- FAQ-search capture;
- semantic keyword expansion;
- social-description reassurance;
- ALT/TITLE context filler.

The correct SEO strategy for an unrelated concept is **zero semantic targeting**.

### Universal locale handling

Generate a `CLEAN_NICHE_EXCLUSION_LEXICON` from the prohibited semantic concept family in the resolved locale/regional variant. It is a QA/generation artifact, not public copy and does not belong in `global-text.json`.

The lexicon must include natural local equivalents and inflections where practical, while avoiding naive substring rules and false positives. Generic game words such as bonus/reward/score/random/chance are not prohibited merely because they can also occur in gambling contexts.

### Existing persistent Global Text

A theme update must not silently overwrite a genuine user-edited value merely to satisfy this gate. If an existing persistent user value introduces a prohibited unrelated concept, flag the exact key as `CLEAN_NICHE_PUBLIC_TEXT_CONFLICT` for owner correction. Factory-seeded legacy values that are provably unedited may be migrated/removed through the normal versioned migration path.



## 22. FOOTER UTILITY PHRASE + FAVICON TEXT/HEAD CONTRACT (v1.2.5)

### Footer utility phrase

Global Text reserves:

```text
footer.bottom_bar.utility_phrase
```

Rules:
- optional value, rendered only when the selected footer composition uses the slot;
- short and locale-natural;
- may differ across unrelated sites;
- manual edits persist through theme updates;
- absence is valid and must collapse cleanly;
- an icon/arrow is not a text fallback.

### Favicon/site-icon ownership

Favicon asset paths remain runtime/asset data, not editable Global Text. Human-readable accessibility/brand text associated with icon controls, if any, remains in Global Text.

SEO/head audit profile records:

```text
favicon_owner = WORDPRESS_SITE_ICON | THEME_FALLBACK
favicon_url
favicon_http_status
favicon_mime
favicon_decode_status
favicon_brand_match
apple_touch_icon_url when used
```

Do not count a declared asset in source code as PASS; verify the final public head and reachable asset.


## 48. STUDIO-FIRST GLOBAL TEXT + SEARCH INTENT MODEL (v4.5.3)

For `OFFICIAL_GAME_STUDIO`, Global Text and SEO must expose the same first-party business model as visible content.

### Global Text content tree

Recommended semantic branches:

```text
site.studio
site.product
pages.home
pages.game
pages.development
pages.mechanics
pages.levels
pages.controls
pages.art
pages.testing
pages.about_studio
pages.support
pages.contact
components.development_story
components.design_challenge
components.product_proof
components.play_download
```

Only create branches for pages/components that actually exist.

### Page-intent ownership

Use first-party search intents such as:
- `{Game} by {Studio}`;
- `{Studio} game development`;
- `how we built/designed {Game}` only when creator/evidence gates permit;
- `{Game} mechanics / level design / controls / art direction`;
- `{Game} support`;
- `{Game} download / play / store`.

Avoid first-party sites targeting outsider-intent language such as `independent review`, `best guide`, `our review of {Game}` or affiliate-like comparison phrasing unless the active business model genuinely requires it.

### Metadata narrative distribution

Do not use the same `creators of {Game}` sentence on every page. Each page title/description should represent its distinct business job:
- Studio/About → identity and product relationship;
- Development → creation/refinement work;
- Mechanics/Levels/Controls/Art → specific design discipline;
- Game → product proposition/player experience;
- Support → help/platform context;
- Home → studio + game + primary conversion.

### Truth-safe historical SEO

`How we built`, `how we created`, `our development story`, `behind the scenes` require the resolved creator relationship and sentence-level evidence consistent with the Content Engine. Do not use historical first-person metadata to bypass content truth rules.


## 49. SEMANTIC IMAGE + MICRO-VISUAL METADATA CONTRACT (v4.5.4)

Image metadata is derived from the same section semantic brief that produced the visual.

For every meaningful image, final ALT/TITLE generation consumes:

```text
page_key
section_key
section_heading_meaning
paragraph_cluster_summary
visual_job
semantic_subject
visible_action_or_state
```

### Relevance rule

ALT/TITLE must describe what the visual actually shows **in the context of that section**. Do not fall back to generic strings such as:
- `{Game} image`;
- `game development image`;
- `gaming visual`;
- `studio illustration`.

If the image was regenerated/replaced and its subject changed materially, its ALT/TITLE must be regenerated from the new final asset + section context.

### Micro-icon accessibility text

For decorative micro-icons:
```text
accessible_text = none / aria-hidden as appropriate
```

For semantic icons paired with visible labels, do not duplicate the label unnecessarily to assistive tech.

For icon-only interactive controls:
```text
accessible_name = required localized Global Text key
```

Suggested keys:

```text
images.{asset_id}.alt
images.{asset_id}.title
accessibility.icons.{icon_id}.label
components.{component_key}.badges.{badge_key}.label
```

No icon asset filename or internal ID may leak as public ALT/TITLE/ARIA text.




## 50. STUDIO / TEAM / PROCESS SEO + GLOBAL TEXT PRIORITY (v4.5.5)

For `OFFICIAL_GAME_STUDIO`, SEO and Global Text must reflect the same company/team/development-first page model as visible copy.

### 50.1 Primary topic hierarchy

For Home and key domain pages, page topics should usually resolve in this order:

```text
STUDIO / COMPANY
→ TEAM / DEVELOPMENT DISCIPLINE
→ PAGE-SPECIFIC WORK / PROCESS
→ PRODUCT / GAME SYSTEM
→ PLAYER RESULT / STORE / SUPPORT
```

Do not make every page's metadata a gameplay summary.

### 50.2 Recommended Global Text branches

```text
pages.{page}.company_context
pages.{page}.team_role
pages.{page}.task_or_challenge
pages.{page}.process
pages.{page}.review_qa
pages.{page}.decision
pages.{page}.product_outcome
pages.{page}.game_detail
pages.{page}.cta
```

Long-form business copy continues to use structured paragraphs/items arrays.

### 50.3 Search-intent examples

When the relationship truth gate passes, valid first-party intent families include:
- `{Studio} — studio behind {Game}`;
- `{Studio} game development`;
- `{Game} development process`;
- `{Game} mechanics design`;
- `{Game} level design`;
- `{Game} visual direction`;
- `{Game} testing and balancing`;
- `{Studio} team and development approach`;
- `{Game} support / download`.

Avoid keyword stuffing the exact phrase `our team` into every metadata field.

### 50.4 Image metadata

Team/workflow hero imagery should use semantic ALT/TITLE based on its role, for example:
- game design review;
- level design planning;
- studio collaboration;
- QA/balance review;
- art-direction work session.

Do not write ALT text that claims anonymous generated people are named/real staff members.

### 50.5 Persistent migration

A factory update may add new studio/process Global Text branches and migrate unedited legacy factory defaults.

Manual edits remain authoritative and are not overwritten merely because the content model changed.



## 51. COMPOSITION-SUPPORT TEXT METADATA (v4.5.6)

Global Text should support composition diversity without hardcoding layout copy into templates.

Recommended optional keys:

```text
pages.{page}.sections.{section}.caption
pages.{page}.sections.{section}.kicker
pages.{page}.sections.{section}.side_note
pages.{page}.sections.{section}.pull_quote
pages.{page}.sections.{section}.fact_labels[]
pages.{page}.sections.{section}.chapter_label
pages.{page}.sections.{section}.image_caption
```

Rules:
- captions must describe useful context, not filler;
- pull quotes must come from actual page copy or owner/source facts, not invented testimonials;
- side notes should add information, not duplicate adjacent paragraphs;
- changing layout family must not require hardcoded PHP text;
- optional composition-support text may be absent without leaving blank DOM slots.

If a layout changes during anti-repeat reroll, Global Text remains the public-copy authority.


---

## 41. GEO / LOCALE SEO HARD GATE (v4.8.1)

SEO locale must be verified from the **final public HTML**, not inferred from Polish copy or internal manifests.

For a PL / Polish build require coherence across:

```text
input.geo = PL
input.locale = pl-PL
<html lang> = pl-PL
OpenGraph locale = pl_PL
schema inLanguage = pl-PL
visible primary language = Polish
canonical host = requested domain
```

Any unrelated language code such as `en-GB` or `en-US` on the public document is `SEO-GEO-001 = FAIL`.

### Required release probe

Fetch rendered Home plus one internal page and assert:
- exactly one canonical per page;
- canonical uses the requested production host;
- final `<html lang>` matches the requested locale;
- OG locale matches the same language/region;
- schema `inLanguage` matches;
- title/description are localized and page-specific;
- normal public pages have a coherent explicit index/follow robots state.

### Meta keywords

Do **not** add `meta name="keywords"` solely because a legacy analyzer reports “keywords missing”. Modern search engines do not require this tag; factory SEO quality is judged through title, description, content, canonical, robots, language, structured data and crawlability instead.
