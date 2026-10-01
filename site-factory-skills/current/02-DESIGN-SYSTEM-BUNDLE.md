# 02 DESIGN SYSTEM BUNDLE

**Bundle format:** Source Bundle v1.5  
**Policy baseline:** Site Factory v4.9.15  
**Bundling rule:** logical module boundaries and aliases are preserved inside bundles. Source Bundle v1.5 applies the Site Factory v4.9.14 interaction, micro-motion, hover/focus and semantic interactive-section expansion while preserving v1.4 rich-content, live UI/UX research, morphological section variation, v1.3 adult-premium visuals and the 7-file Project Source architecture.

## Module aliases in this bundle

- `02-GOLDEN-DESIGN-DNA.md` → this file, section `LEGACY MODULE: 02-GOLDEN-DESIGN-DNA.md`
- `03-DESIGN-SYSTEM.md` → this file, section `LEGACY MODULE: 03-DESIGN-SYSTEM.md`
- `18-SECTION-COMPOSITION-ENGINE.md` → this file, section `LOGICAL MODULE: 18-SECTION-COMPOSITION-ENGINE.md`

## Cross-reference rule

References inside logical module text to filenames such as `15-SECTION-IMAGE-ENGINE.md` remain valid **logical module IDs**. Resolve them against the module aliases declared across the loaded Source Bundles. `SOURCE-BUNDLE-MAP.md` is maintenance documentation only and is **not required** as a Project Source.

---

<!-- BUNDLE-MODULE-START: 02-GOLDEN-DESIGN-DNA.md -->

# LEGACY MODULE: 02-GOLDEN-DESIGN-DNA.md

# GOLDEN DESIGN DNA

**Version:** 4.3  
**Role:** дизайн-калібрування за 7 прийнятими користувачем WordPress-сайтами

---

## 1. Основний принцип

Golden Sites — це **quality bar**, а не шаблони.

Дозволено запозичувати:
- рівень щільності;
- ритм секцій;
- тип hero;
- баланс media/content;
- способи структурування catalog/services/guides;
- принципи typography;
- trust/finale patterns;
- responsive maturity.

Заборонено копіювати:
- markup;
- exact section order;
- тексти;
- brand identity;
- унікальні assets;
- exact palette;
- exact card geometry.

---

## 2. Прямий аудит Golden Sites

### Alverena Gaming Store
Observed homepage:
1. hero
2. categories
3. highlights
4. benefits
5. bestseller
6. brand strip
7. guide banner
8. testimonials
9. newsletter

Observed media assets: приблизно **82**.

**DNA:** image-led gaming commerce/editorial, висока visual density, багатий каталог, сильний hero/media layer.

---

### Aveluno
Observed homepage:
1. hero
2. fleet
3. how it works
4. delivery
5. occasions
6. enquiry

Observed media assets: приблизно **20**.

**DNA:** premium service/editorial, strong media sections, restrained typography, повний service journey.

---

### Coravelle
Observed homepage:
1. sanctuary hero
2. slow care
3. ritual menu
4. visit journey
5. quiet gift
6. booking suite

Observed media assets: приблизно **13**.

**DNA:** organic luxury, editorial serif, slow narrative, alternating media/copy.

---

### Elvarino
Observed homepage:
1. hero
2. services
3. story
4. process
5. team
6. reviews
7. contact

Observed media assets: приблизно **9**.

**DNA:** complete service narrative, process/team/reviews, clear conversion path.

---

### Lumecora
Observed homepage:
1. media hero
2. why
3. showcase
4. process
5. library
6. client signals
7. coverage
8. newsletter
9. final call

Observed media assets: приблизно **16**.

**DNA:** immersive gaming/VR showcase, strong visual media, proof + library + trust.

---

### Meravino
Observed homepage:
1. hero
2. proof
3. category deck
4. editor picks
5. club invite
6. choice guide
7. reading shelf
8. testimonials
9. finale

Observed media assets: приблизно **32**.

**DNA:** content-rich gaming editorial/commerce, media cards, proof, reading content, mature visual rhythm.

---

### Velmoria
Observed homepage:
1. hero
2. featured
3. games
4. schedule
5. how to participate
6. contact

Observed media assets: приблизно **14**.

**DNA:** gaming/event architecture, functional hierarchy, clear domain sections.

---

## 3. Golden families

### A. Gaming Commerce / Editorial
Primary references:
- Alverena
- Meravino

Use when:
- gaming catalogs;
- guides;
- collections;
- editorial gaming portals;
- game discovery.

Traits:
- visual hero;
- category decks;
- media cards;
- editor picks;
- guides;
- proof/trust;
- final CTA/newsletter.

---

### B. Immersive Gaming / Showcase
Primary references:
- Lumecora
- Velmoria

Use when:
- one game;
- VR;
- events;
- showcases;
- gaming experiences;
- campaign-like content hubs.

Traits:
- stronger scene/media layer;
- showcase;
- feature panels;
- process/how to participate;
- proof/trust;
- coverage/finale.

---

### C. Premium Service
Primary references:
- Aveluno
- Elvarino

Use when:
- services;
- premium local businesses;
- consultations;
- delivery;
- studios.

---

### D. Organic Editorial Luxury
Primary:
- Coravelle

Use when:
- wellness;
- beauty;
- hospitality;
- slow living;
- premium experiences.

---

## 4. Gaming rule

При замовленні Gaming фабрика **не винаходить cyber/minimal style автоматично**.

Спочатку відповісти:

1. Чи більше підходить Alverena/Meravino?
2. Чи більше підходить Lumecora/Velmoria?
3. Який рівень imagery має вихідна гра?
4. Чи є source brand навмисно cartoon/playful?

Тільки після цього створювати власний Design DNA.

---

## 5. Homepage completeness

Нормальна Golden-quality homepage зазвичай має приблизно **6–9 meaningful sections**.

Не треба механічно робити 9 секцій, але заборонено видавати за повний сайт:

`header → giant hero → 3 cards → footer`

якщо ніша дозволяє значно багатший experience.

---

## 6. Visual density

Для gaming нормальна ціль:

- 5+ meaningful media moments як абсолютний мінімум;
- зазвичай 7–12 visual assets;
- hero — не єдиний сильний visual;
- хоча б 2–3 non-hero sections мають meaningful media.

---

## 7. Section grammar

За homepage повинні зустрічатися різні композиції:

- hero split / media background;
- proof/metrics strip;
- category/catalog deck;
- editorial media split;
- showcase;
- guide/process;
- media rows;
- reading shelf;
- trust/social proof;
- FAQ;
- final CTA.

Не більше двох послідовних секцій з однаковою grid-граматикою.

---

## 8. Типографіка

Golden-like typography:
- брендова;
- читабельна;
- масштабована;
- не перетворює hero на плакат без контенту.

Default hero H1 не повинен займати майже весь viewport.

Large type допускається, але має:
- працювати з media;
- залишати supporting copy;
- показувати CTA;
- швидко приводити до наступної секції.

---

## 9. Anti-patterns

Blocking:
- пустий hero на великому фоні;
- одна абстрактна SVG як увесь visual identity;
- випадковий cyber look без зв’язку з Golden family;
- cartoon mascot як gaming default;
- лише картки без сильного media layer;
- надмірний all-caps;
- over-minimalism, який прибирає корисний контент;
- дизайн, який неможливо прив’язати до жодної Golden family.

---

## 10. Design Manifest requirement

Перед coding записати:

- `golden_primary_reference`
- `golden_secondary_reference`
- `borrowed_principles`
- `non_copying_changes`
- `hero_media_strategy`
- `visual_asset_budget`
- `homepage_section_plan`
- `type_scale`
- `density_profile`
- `responsive_transformation`
- `trust_pattern`
- `final_cta_pattern`

Без цього BUILD не починається.


---

## 11. GEO-first typography override (v4.1)

Golden Sites define typography **maturity, hierarchy and composition**, not the exact family for every GEO.

Before borrowing a typography direction:
1. resolve GEO + locale;
2. run internet-based GEO typography research;
3. verify target-language glyph coverage;
4. test real localized copy;
5. then adapt the Golden family.

Allowed to borrow:
- serif vs sans mood;
- editorial contrast;
- hierarchy;
- density;
- headline/body relationship.

Do not blindly copy exact font families/pairings/tracking when local-language readability or GEO fit is weaker.


---

## 12. Golden color independence (v4.2)

Golden Sites define:
- color maturity;
- contrast discipline;
- accent restraint;
- section hierarchy;
- palette sophistication.

They do **not** define the exact color family of a new site.

### Forbidden reuse pattern

Do not repeatedly derive multiple new projects from the same Golden palette fingerprint.

Even when two projects use the same Golden family, the new project must establish an independent color identity.

### Allowed transformation

From a Golden reference the factory may preserve:
- number of palette roles;
- contrast logic;
- warm/cool balance discipline;
- accent frequency;
- surface hierarchy.

But it should change, where appropriate:
- dominant hue family;
- supporting hue family;
- accent family;
- neutral temperature;
- light/dark mode;
- saturation profile.

### Same-family diversity

Two `Gaming Commerce / Editorial` sites may share composition maturity while having completely different color worlds.

Golden family match therefore does not justify repeated:
- teal + cream;
- coral + sand;
- navy + lime;
- purple + cyan;
or any other recurring factory default.



---

## 13. Golden section-grammar independence (v4.3)

Golden Sites define production maturity, density, pacing and composition quality. They do **not** define a fixed section skeleton for new sites.

For every new project:
- borrow principles, not exact section geometry;
- do not preserve the exact Home section sequence of a Golden site;
- do not repeatedly select the same hero + split + card + CTA combination merely because it passed before;
- send semantic section intents to `18-SECTION-COMPOSITION-ENGINE.md` for project-specific composition.

A site can belong to the same Golden family while using a materially different section grammar.


<!-- BUNDLE-MODULE-END: 02-GOLDEN-DESIGN-DNA.md -->

---

<!-- BUNDLE-MODULE-START: 03-DESIGN-SYSTEM.md -->

# LEGACY MODULE: 03-DESIGN-SYSTEM.md

# DESIGN SYSTEM — REM / FLUID / RESPONSIVE

**Version:** 4.5.3  
**Role:** глобальна CSS/layout система

---

## 1. Numeric px заборонений

Production CSS фабрики **не використовує numeric `px`**.

Замість:

`1px` → `0.0625rem`  
`16px` → `1rem`  
`24px` → `1.5rem`  
`1400px` → `87.5rem`

Blocking QA:
- будь-який numeric `px` token у generated production CSS = FAIL.

---

## 2. Дозволені одиниці

### Typography / spacing / radius
- `rem`

### Component-relative
- `em`

### Layout
- `%`
- `fr`
- `minmax()`
- `auto`

### Fluid
- `clamp()`
- контрольований `vw`
- `svh` / `dvh`, якщо справді потрібно

### Breakpoints
- `rem` або `em`

---

## 3. Root tokens

Рекомендована структура:

```css
:root {
  --container: 88rem;
  --gutter: clamp(1.25rem, 4vw, 4rem);

  --space-1: 0.5rem;
  --space-2: 0.75rem;
  --space-3: 1rem;
  --space-4: 1.5rem;
  --space-5: 2rem;
  --space-6: 3rem;
  --space-7: 4.5rem;
  --space-8: 6rem;

  --radius-sm: 0.5rem;
  --radius-md: 1rem;
  --radius-lg: 1.5rem;

  --hairline: 0.0625rem;
}
```

Точні значення змінюються через Design DNA.

---

## 4. Container

Default:

```css
.shell {
  inline-size: min(
    calc(100% - (2 * var(--gutter))),
    var(--container)
  );
  margin-inline: auto;
}
```

Не задавати desktop container жорстким px.

---

## 5. Fluid type scale

Default envelope is semantic, not one universal display scale:

- body: `1rem`
- small: `0.75rem–0.875rem`
- lead: `1.125rem–1.35rem`
- H3: `1.4rem–2.25rem`
- ordinary non-hero H2: usually about `1.9rem–3.25rem`; deliberate display H2 may reach about `4.25rem` only when composition supports it
- Home hero H1: usually about `3.5rem–4.25rem`
- internal-page hero H1: usually about `2.75rem–3.75rem`; utility/legal intros normally use the lower end
- `MANIFESTO_EXCEPTION`: may exceed the normal Home envelope only with explicit Design DNA justification + first-viewport screenshot PASS; it is not a default H1 scale and must not create a `5+` line wall or push supporting copy/media out of the first viewport

Reference fluid examples:

```css
.hero--home h1 {
  font-size: clamp(2.75rem, 4.4vw, 4.25rem);
}

.hero--internal h1 {
  font-size: clamp(2.25rem, 3.5vw, 3.75rem);
}
```

Hero-specific rules in sections 20 and 56 are authoritative for first-viewport sizing. A generic type token must never override the lower role-specific envelope. Going larger requires explicit `MANIFESTO_EXCEPTION` evidence and visual QA, not only a large available viewport.

---

## 6. Spacing

Не використовувати випадкові десятки різних відступів.

Використовувати систему:

```css
.section {
  padding-block: clamp(4rem, 7vw, 7rem);
}
```

Hero:
- зазвичай `4rem–7rem` vertical padding;
- content-driven height;
- не fixed desktop height.

---

## 7. Hero rule

Заборонено:
- hero із fixed `min-height` лише для заповнення екрану;
- H1, який забирає більшість першого viewport;
- величезні пусті поля для створення "premium feel".

Hero має містити:
- eyebrow/kicker, якщо доречно;
- H1;
- supporting copy;
- CTA;
- meaningful visual/media;
- зрозумілий перехід до наступного content moment.

---

## 8. Grid

Використовувати:

```css
grid-template-columns:
  minmax(0, 1fr)
  minmax(0, 1fr);
```

або:

```css
repeat(auto-fit, minmax(min(100%, 18rem), 1fr))
```

Заборонено layout, що залежить від випадкової фіксованої ширини картки.

---

## 9. Responsive transformation

Mobile — не "desktop, стиснутий донизу".

При переході:
- змінювати порядок media/copy;
- скорочувати decorative layers;
- перебудовувати cards;
- змінювати navigation;
- адаптувати typography;
- змінювати padding rhythm;
- забезпечувати touch targets.

---

## 10. Breakpoints

Приклад:

```css
@media (max-width: 64rem) { ... }
@media (max-width: 48rem) { ... }
@media (max-width: 30rem) { ... }
```

Точна сітка залежить від контенту, а не від конкретних пристроїв.

---

## 11. Empty-space gate

Whitespace — дизайн-інструмент, але не заміна контенту.

FAIL якщо:
- приблизно третина першого desktop viewport — беззмістовний фон;
- media/copy виглядають як маленькі острови у великій пустоті;
- наступний meaningful content момент надто далеко без композиційної причини.

---

## 12. CSS QA

Перед release:
- numeric px = 0;
- horizontal overflow = 0;
- layout працює при збільшеному тексті;
- images мають flexible sizing;
- long labels не ламають nav/cards;
- reduced-motion підтримується для значної анімації;
- mobile nav не перекриває viewport.

---

## 13. Split-section proportion rule (v4.1 patch)

Editorial split sections повинні мати відчутний visual balance.

Target envelope:
- text zone: `42%–58%`;
- media zone: `42%–58%`;
- heading max width: приблизно `8–12` слів на рядок;
- section gap: `clamp(1.5rem, 3vw, 4rem)`;
- media block min visual weight: не менше ніж ~`38%` visible section value на desktop.

Якщо title/heading занадто довгий, система повинна:
1. зменшити heading max-width;
2. зменшити upper font bound через `clamp()`;
3. перенести part of supporting copy в body/eyebrow;
4. вирівняти image ratio.

## 14. Image/frame rule

У split layouts не дозволяється:
- tiny image next to dominant headline;
- oversized empty beige zones;
- image card із випадковим baked-in label, якщо label повинен жити в HTML;
- нечіткий / over-smoothed visual.


---

## 15. Wide-screen typography guard

At `120rem–160rem` viewport widths, split-section headings must not scale indefinitely.

Default split-section heading envelope:
- H2 max about `3.75rem–4.25rem`;
- usually no more than `4–5` visual lines;
- clamp upper bound stays fixed on ultrawide screens.

Run screenshot QA at approximately `90rem`, `120rem` and `160rem` viewport widths for visual-rich builds.


---

## 16. GEO typography selection engine (v4.2)

### 16.1. Research comes before font-family

Typography is selected **after** GEO + locale are known.

Mandatory web research:
- inspect `5–10` current high-quality sites relevant to the target GEO where practical;
- include at least two locally authoritative/editorial/cultural references when available;
- inspect official/provider font documentation for language/script coverage;
- note recurring local tendencies: serif/sans preference, x-height, contrast, density, display usage.

Research provides direction, not permission to clone a local publication.

### 16.2. Locale specimen

Test candidates with actual target-language text.

For `pt-PT`, specimen should include forms such as:

```text
ação, informação, utilização, português, coração,
próximo, melhorias, experiência, ligação, conteúdo
```

Equivalent locale-specific specimen is mandatory for every GEO.

Check:
- accents/diacritics;
- punctuation;
- uppercase;
- numerals;
- currency when relevant;
- long navigation labels;
- multi-line H1/H2;
- body paragraphs.

### 16.3. Candidate comparison

Shortlist usually `3–5` candidates/pairings.

Evaluate:
- body readability;
- heading personality;
- visual comfort at real sizes;
- locale character quality;
- spacing/rhythm;
- niche/brand compatibility;
- weight/italic range;
- fallback behavior;
- performance/delivery risk.

### 16.4. Type-family count

Default:
- `1` body family;
- optional `1` display/headline family;
- optional system monospace only when functional.

Avoid decorative font piles.

### 16.5. Delivery

Record the font delivery mode and a robust fallback stack.

Do not make the site depend on an unavailable font binary.

If remote font delivery is used:
- declare it in runtime/third-party manifest;
- account for legal/privacy implications when applicable;
- ensure the layout remains usable if the provider fails.

### 16.6. Final selection gate

A font may be selected only when:

```text
glyph coverage = PASS
body readability = PASS
headline composition = PASS
GEO fit = PASS
niche/design fit = PASS
fallback = PASS
delivery/license status = PASS
```

"Looks fashionable" alone is not enough.


---

## 17. Site Color System + cross-project uniqueness (v4.3)

Each site must define semantic color tokens from a project-specific palette:

```text
--color-bg
--color-bg-alt
--color-surface
--color-surface-strong
--color-text
--color-text-muted
--color-primary
--color-primary-strong
--color-secondary
--color-accent
--color-border
--color-focus
--color-success
--color-warning
--color-danger
```

The exact token names may vary, but the system must be semantic rather than scattered raw HEX values.

### Palette construction

Build the palette from:
- topic / source visual intelligence;
- GEO visual context where relevant;
- Golden maturity;
- typography;
- image art direction;
- cross-site uniqueness requirement.

### Anti-template rule

Do not maintain a hidden default palette that repeatedly produces the same visual world.

Before finalizing tokens:
1. generate a candidate palette;
2. create `SITE COLOR FINGERPRINT`;
3. compare it with previous factory sites;
4. if too similar, deliberately mutate hue families / temperature / polarity / accent relationship;
5. re-check contrast;
6. only then lock tokens.

### Color manipulation freedom

The factory may freely manipulate source colors unless:
- owner-supplied brand rules constrain them;
- a factual product identity requires a recognizable color;
- accessibility/readability would be harmed.

### Contrast gate

All final combinations must remain readable in real components:
- body text on main background;
- headings;
- navigation;
- buttons;
- cards;
- cookie UI;
- legal content;
- focus/hover states.

Distinctiveness is not achieved by sacrificing usability.



---

## 18. Composition-system compatibility (v4.4)

`18-SECTION-COMPOSITION-ENGINE.md` may vary section geometry aggressively, but every selected pattern must still obey this Design System.

Required invariants:
- no numeric `px` in production CSS;
- semantic source order remains understandable without CSS;
- grid/flex structures use resilient `minmax()`, `%`, `fr`, `auto`, `clamp()` and intrinsic sizing;
- visual overlap never clips critical copy at text zoom;
- asymmetry collapses intentionally on mobile;
- sticky/rail/mosaic patterns have a static readable fallback;
- interaction is progressive enhancement, not a prerequisite for access to essential content;
- unusual layout does not justify horizontal page overflow.

Composition novelty is subordinate to usability.



---

## 19. Content-density + typography coupling (v4.5)

The section canvas must be earned by its content/media.

### Non-hero heading envelope
Default non-hero H2 target:
- usually about `2.25rem–3.75rem`;
- larger only for a deliberate manifesto/editorial statement with enough supporting structure;
- ordinary explanatory sections should not visually compete with the page H1.

At wide desktop:
- prefer roughly `2–4` visual lines for a normal H2;
- if a heading reaches `4+` heavy lines and dominates the section, reduce scale/max-width or restructure;
- a sparse section with one short paragraph should not receive hero-scale typography merely to fill space.

### Cohesion distances
Eyebrow → heading → lead/body → CTA/media should form a readable spatial group.

Do not create:
- orphaned eyebrow in a distant column;
- body copy pushed to the opposite corner without a connector;
- a large empty middle field with no media, navigation, annotation or atmospheric purpose.

### Empty-space functional test
At representative desktop widths, every large empty region must answer at least one:
- does it protect a meaningful focal image?
- does it create a deliberate editorial pause between dense regions?
- does it host an interaction/annotation/diagram?
- does it materially improve hierarchy/readability?

If none apply, tighten or recompose.

### Text expansion
After tightening, long localized copy must still pass the existing Global Text resilience test.



## 20. Rendered density acceptance (v4.5.1)

Typography envelopes are defaults, not permission to fill space with type.

Recommended rendered defaults unless Design DNA justifies otherwise:
- Home hero H1 should usually remain within about `3.5rem–4.25rem`; larger manifesto sizing requires explicit first-viewport justification;
- internal page hero H1 should usually remain within about `2.75rem–3.75rem`; utility/legal intros should normally be smaller;
- ordinary non-hero H2 usually about `1.9rem–3.25rem`;
- sparse utility/contact sections should prefer the lower half of those ranges.

At a representative `~90rem / 1440px-class` desktop screenshot:
- label + heading + lead/body should read as one spatial cluster;
- a blank region that visually dominates roughly one third or more of the section needs a declared role (media, navigation, annotation, atmospheric focal area);
- an unused second grid column is not a design feature; remove it, fill it, or change pattern family;
- padding/min-height must not make a short section feel like a full-screen poster;
- Contact/utility page introductions should be compact unless meaningful media truly supports a wider canvas.

If screenshot perception conflicts with numeric CSS limits, screenshot perception wins and the section returns to FIX LOOP.



## 21. Hover / focus / pointer interaction system (v4.5.2)

Interactive surfaces must define states intentionally:

```text
default
hover when pointer supports hover
focus-visible
active/pressed
disabled when applicable
selected/current when applicable
```

Rules:
- hover cannot be the only way to discover essential content or action;
- `:focus-visible` must be at least as clear as hover;
- on touch/coarse pointers, hover transforms that can stick or obscure content are disabled/simplified;
- avoid applying the same translate-up + shadow treatment to every component;
- transform scale should be subtle enough to avoid layout collision;
- image zoom stays clipped inside intentional media frames;
- motion durations/easing come from a small project token set;
- reduced-motion users receive near-static state transitions.

<!-- BUNDLE-MODULE-END: 03-DESIGN-SYSTEM.md -->

---

<!-- BUNDLE-MODULE-START: 18-SECTION-COMPOSITION-ENGINE.md -->

# LOGICAL MODULE: 18-SECTION-COMPOSITION-ENGINE.md

# SECTION COMPOSITION ENGINE — VARIATION / UI-UX GRAMMAR / ANTI-REPETITION

**Version:** 2.2.0  
**Role:** generate semantically correct but maximally varied page sections through live UI/UX pattern harvesting, morphological modifiers and anti-repetition  
**Status:** Mandatory for full-site BUILD  
**Research model:** abstract pattern taxonomy learned from current UI/UX libraries and high-quality live sites; never copy proprietary components 1:1

---

## 1. Mission

The factory must create sites that feel designed for the specific project rather than assembled from the same recurring section templates.

Goal:

```text
SEMANTIC INTENT
→ VALID PATTERN CANDIDATES
→ SEEDED WEIGHTED VARIATION
→ ANTI-REPETITION FILTER
→ RESPONSIVE / A11Y CHECK
→ SECTION COMPOSITION MANIFEST
→ BUILD
→ COMPOSITION QA
```

Variation is intentional and reproducible. Pure random layout chaos is forbidden.

---

## 2. Inspiration corpus — taxonomy only

When web research is available, the factory may study current libraries/showcases such as:
- Relume-style component taxonomies and layout/element/interaction filtering;
- Untitled UI-style variant-rich marketing section categories;
- Flowbase-style section + interaction/tag catalogues;
- Landbook-style curated section categories, industries and styles;
- Mobbin-style real-product UI elements and user-flow pattern analysis;
- niche-specific current live websites relevant to the project GEO/topic.

These sources are **research inputs**, not source code or templates.

Allowed extraction:
- abstract section role;
- layout family name;
- interaction class;
- density idea;
- content-to-media relationship;
- responsive behavior concept;
- high-level composition principle.

Forbidden extraction:
- exact markup/classes;
- copied screenshots/assets;
- proprietary component code;
- exact pixel/rem measurements from a reference;
- distinctive layout copied 1:1;
- exact page section sequence copied from one reference.

---

## 3. Research refresh

For a new full-site project, when web access is available:
1. inspect at least `2` current section/pattern libraries or showcase sources;
2. inspect `3–8` niche-relevant live examples where practical;
3. collect abstract candidate patterns relevant to the actual page intents;
4. discard patterns that conflict with accessibility, content depth or project Design DNA;
5. do not import external markup/assets into the theme merely because a pattern was observed.

For multi-site batches, rotate research sources and pattern families so the whole batch does not converge on one trend.

---

## 4. Semantic intent comes first

Each section starts with `section_intent`, not with a visual template.

Examples:
- introduce topic;
- explain mechanic;
- compare options;
- show progression;
- expose resources;
- prove trust;
- answer objections;
- guide next action;
- contact/support;
- legal/informational long form.

The engine chooses among patterns that can express that intent honestly.

Do not use novelty to hide information or force unsuitable UI.

---

## 5. Site composition seed

Before section selection create:

```text
site_composition_seed
site_composition_nonce
```

Reference model:

```text
seed = HASH(domain + geo + topic + site_composition_nonce)
```

Rules:
- new site → generate a new nonce;
- same-site update → preserve existing nonce by default;
- explicit redesign → may rotate nonce and record that choice;
- seed is internal build metadata, not public content.

The seed makes stochastic choices reproducible inside the same project while allowing different sites to diverge.

---

## 6. Section Composition Manifest

Every meaningful section records:

```text
page_key
section_key
section_intent
content_shape
priority
pattern_family
pattern_variant
composition_axis
content_alignment
media_mode
media_position
media_ratio
container_mode
grid_signature
card_geometry
surface_mode
background_mode
edge_mode
overlap_mode
density_mode
type_alignment
interaction_mode
motion_mode
desktop_behavior
mobile_transformation
accessibility_constraints
performance_constraints
section_seed
section_fingerprint
selection_score
selection_rationale
```

Optional:
- sticky behavior;
- rail behavior;
- comparison mode;
- progressive-reveal mode;
- visual anchor/focal region;
- overflow strategy;
- related source/reference taxonomy label.

---

## 7. Pattern family pool

Pattern labels are **abstract grammars**, not fixed templates. The pool is extensible.

### 7.1 Hero / opening families
- `H01_EDITORIAL_SPLIT`
- `H02_ASYMMETRIC_MEDIA_SPLIT`
- `H03_FULL_BLEED_MEDIA_STAGE`
- `H04_FRAMED_CINEMATIC_STAGE`
- `H05_MOSAIC_COLLAGE_HERO`
- `H06_TEXT_FIRST_FLOATING_MEDIA`
- `H07_POSTER_WITH_PROOF_LAYER`
- `H08_CENTERED_STATEMENT_WITH_MEDIA_RAIL`
- `H09_SIDEWAYS_EDITORIAL_HERO`
- `H10_LAYERED_DEPTH_HERO`

### 7.2 Editorial / feature / narrative families
- `C01_ALTERNATING_EDITORIAL_SPLIT`
- `C02_OFFSET_ASYMMETRIC_SPLIT`
- `C03_BENTO_INFORMATION_FIELD`
- `C04_STAGGERED_MEDIA_MOSAIC`
- `C05_SPOTLIGHT_WITH_SATELLITES`
- `C06_STICKY_CHAPTER_STORY`
- `C07_EDITORIAL_TWO_COLUMN_WITH_ASIDE`
- `C08_MEDIA_RAIL_WITH_COPY_ANCHOR`
- `C09_SERPENTINE_MEDIA_STORY`
- `C10_ANNOTATED_VISUAL`
- `C11_STACKED_BANDS`
- `C12_CENTERED_MANIFESTO_WITH_NOTES`
- `C13_OVERLAP_MEDIA_LEDGER`
- `C14_INSET_PANEL_WITH_EDGE_MEDIA`
- `C15_TEXT_GRID_WITH_ONE_DOMINANT_VISUAL`
- `C16_CHAPTER_INDEX_WITH_CONTENT_STAGE`

### 7.3 Discovery / catalogue / resource families
- `D01_ASYMMETRIC_CARD_DECK`
- `D02_EDITORIAL_INDEX`
- `D03_HORIZONTAL_MEDIA_SHELF`
- `D04_SPOTLIGHT_PLUS_GRID`
- `D05_CATEGORY_LEDGER`
- `D06_COMPARISON_DECK`
- `D07_STAGGERED_RESOURCE_LIST`
- `D08_FILTERABLE_GRID_WHEN_USEFUL`
- `D09_NUMBERED_CONTENT_DIRECTORY`
- `D10_FEATURED_ITEM_PLUS_RAIL`

### 7.4 Process / explanation / data families
- `P01_NUMBERED_RUNWAY`
- `P02_ALTERNATING_TIMELINE`
- `P03_VERTICAL_STEPPER`
- `P04_HORIZONTAL_STAGE_TRACK`
- `P05_TABBED_WALKTHROUGH`
- `P06_ACCORDION_EXPLAINER`
- `P07_ANNOTATED_DIAGRAM`
- `P08_COMPARISON_MATRIX`
- `P09_BEFORE_AFTER_OR_STATE_COMPARE`
- `P10_PROGRESSIVE_STICKY_STORY`

### 7.5 Proof / trust families
- `T01_QUOTE_MEDIA_SPLIT`
- `T02_TESTIMONIAL_MOSAIC`
- `T03_METRICS_PLUS_PROOF`
- `T04_TRUST_STRIP_WITH_CONTEXT`
- `T05_CASE_STUDY_SPOTLIGHT`
- `T06_REVIEW_RAIL`
- `T07_EDITORIAL_QUOTES_WITH_ONE_FEATURED`
- `T08_METHOD_PROOF_LEDGER`

### 7.6 CTA / closing families
- `A01_FULL_WIDTH_MEDIA_CTA`
- `A02_CONTAINED_SPLIT_CTA`
- `A03_TYPOGRAPHIC_STATEMENT_CTA`
- `A04_INLINE_ACTION_RIBBON`
- `A05_DUAL_ACTION_STAGE`
- `A06_EDITORIAL_CLOSE_WITH_RELATED_LINKS`
- `A07_FLOATING_PANEL_OVER_MEDIA`
- `A08_QUIET_MINIMAL_CLOSE`

### 7.7 Long-form / legal / utility families
- `L01_ARTICLE_WITH_STICKY_TOC`
- `L02_ARTICLE_WITH_INLINE_SUMMARY`
- `L03_CHAPTERED_LONGFORM`
- `L04_FAQ_LEDGER`
- `L05_CONTACT_SPLIT_WITH_SUPPORT_MAP`
- `L06_CONTACT_DIRECTORY_WITH_CONTEXT`
- `L07_RESOURCE_ARTICLE_WITH_ASIDES`

Not every project needs every family.

---

## 8. Independent variation dimensions

Pattern family alone is not enough. Build the final composition by varying high-impact dimensions.

### Structure
- one-column;
- two-column;
- asymmetric 2-column;
- 3-column editorial;
- nested grid;
- bento/mosaic;
- rail;
- timeline/stepper;
- sticky chapter;
- full-bleed stage.

### Container
- full bleed;
- wide contained;
- standard shell;
- narrow editorial;
- edge-to-edge media + contained copy;
- inset framed stage.

### Alignment / direction
- left-led;
- right-led;
- centered;
- alternating;
- mirrored;
- top-aligned;
- baseline-aligned;
- deliberately offset.

### Media behavior
- dominant media;
- supporting media;
- background media;
- inset media;
- multi-image collage;
- image rail;
- annotated image;
- media absent when copy/data is stronger.

### Surface
- flat continuous background;
- contrast band;
- elevated panel;
- transparent/overlay;
- outlined frame;
- tinted surface;
- image-backed surface.

### Card geometry
- no cards;
- open editorial blocks;
- outlined cards;
- soft cards;
- edge cards;
- asymmetric spans;
- featured card + satellites;
- list rows.

### Edge / overlap
- clean contained;
- media bleed;
- controlled overlap;
- cropped edge;
- floating panel;
- interlocking sections.

### Density
- compact;
- balanced;
- spacious;
- dense editorial;
- mixed-density within one section.

### Interaction
- static;
- accordion;
- tabs;
- carousel/rail;
- filter;
- lightbox;
- sticky progress;
- progressive reveal.

### Motion
- none;
- subtle entrance;
- media parallax-lite;
- marquee only when content supports it;
- progress-linked reveal;
- hover/focus microinteraction.

Motion is optional and must respect reduced motion.

---

## 9. Candidate filtering

Before random selection, remove any candidate that fails one of these:

```text
semantic_fit
content_volume_fit
media_availability
responsive_fit
accessibility_fit
performance_fit
Design_DNA_fit
legal/content_integrity
```

Examples:
- do not use tabs if important content would be hidden unnecessarily;
- do not use carousel for essential sequential reading by default;
- do not use sticky scrollytelling if the same content cannot remain readable without JS/sticky support;
- do not use a photo-led layout when no valid meaningful image exists;
- do not use a data matrix when the content is narrative prose.

---

## 10. Weighted stochastic selection

For remaining candidates calculate an internal score.

Reference weighting:

```text
semantic/content fit        30%
novelty within page         20%
cross-site novelty          15%
Golden/Design-DNA fit       10%
responsive robustness       10%
accessibility robustness    10%
performance cost             5%
```

Then:
1. eliminate blockers;
2. apply repetition penalties;
3. apply novelty bonuses;
4. take a weighted seeded sample from the strongest candidates rather than always choosing rank #1;
5. record why the selected pattern was valid.

This creates variation without sacrificing quality.

---

## 11. Section fingerprint

Each section receives a normalized signature such as:

```text
pattern_family
composition_axis
media_mode
media_position
container_mode
grid_signature
card_geometry
surface_mode
edge_mode
density_mode
interaction_mode
motion_mode
```

Micro details such as a slightly different radius or small color change do **not** count as meaningful uniqueness by themselves.

---

## 12. Intra-page anti-repetition

Default rules for Home and rich internal pages:

```text
exact section fingerprint repeats = 0
same pattern_family repeats = max 1 by default
same card geometry dominance = max 2 sections
adjacent high-impact similarity = reject when too close
```

Exceptions are allowed for genuine functional repetition such as:
- repeated article chapters;
- table rows;
- FAQ items;
- catalog items inside one intentional system.

But the **outer section grammar** still should vary around those repeated inner items.

### Adjacent section distance
Adjacent meaningful sections should differ in at least `4` high-impact dimensions from section 11 where practical.

At minimum inspect:
- structure;
- media role/position;
- alignment;
- surface/background;
- density;
- card geometry;
- interaction;
- edge/overlap behavior.

Hero + section 2 receives the strictest comparison.

---

## 13. Page grammar fingerprint

For each managed page store:

```text
page_key
hero_or_intro_family
section_family_sequence
dominant_structure_family
media_rhythm
surface_rhythm
interaction_set
closing_pattern
page_composition_fingerprint
```

Key pages must not all share the same visible skeleton.

Examples of unacceptable factory repetition:
- every page begins with the same left-copy/right-image split;
- every page uses three equal cards as section 2;
- every page ends with the same rounded CTA panel;
- every internal page is `hero → 3 cards → text split → FAQ`.

---

## 14. Cross-site Site Composition Fingerprint

Each released site produces:

```text
site_composition_seed
hero_family
home_section_sequence_signature
dominant_pattern_families
asymmetry_profile
media_rhythm
surface_polarity_rhythm
card_geometry_profile
interaction_profile
motion_profile
cta_family
footer_composition_family
```

Recommended artifact:

```text
site-composition-fingerprint.json
```

Keep it outside the install-ready theme ZIP unless requested. It may live in build/QA artifacts.

---

## 15. Cross-site similarity gate

When recent factory fingerprints are available, compare the candidate against at least the most recent `8–12` sites where practical.

Reference weighted similarity dimensions:

```text
hero family                 18%
section sequence            18%
dominant layout families    15%
media rhythm                12%
surface polarity            10%
CTA + footer family          9%
card geometry                8%
interaction + motion         5%
asymmetry profile            5%
```

If similarity exceeds approximately `0.68` to a recent unrelated project:
- do not merely change colors;
- mutate at least `3` high-impact dimensions;
- rerun semantic/responsive/a11y checks;
- recompute fingerprint.

Owner brand constraints may justify similarity, but the reason must be recorded.

If prior fingerprints are unavailable, use the site seed, Golden-family diversity rules and strong intra-project anti-repetition. Never pretend cross-site history was checked when it was not available.

---

## 16. Mutation operators

When composition is too similar, use high-impact mutation operators:
- change hero family;
- switch split → mosaic/bento/rail/editorial index;
- mirror reading direction only when semantic order remains correct;
- change media dominance/support role;
- change contained ↔ full-bleed relationship;
- change grid span hierarchy;
- remove card shell in favor of open editorial blocks;
- change surface polarity rhythm;
- replace grid with rail/timeline/ledger;
- change CTA family;
- change testimonial/proof family;
- change section order inside a semantically safe reorder group;
- change interaction class where useful;
- change mobile transformation strategy.

Low-impact cosmetic mutations alone do not satisfy cross-site uniqueness.

---

## 17. Section-order variation

Section **geometry** is broadly variable. Section **order** is only partially variable.

Keep strong journey invariants:
- clear opening/hero first;
- critical explanation before dependent detail;
- proof near the claim it supports;
- final CTA/next step after enough context;
- legal/utility content remains structurally predictable.

Safe reorder groups may include peer-level sections such as:
- features vs progression;
- resources vs tips;
- proof vs methodology;
when dependency is absent.

Do not randomize user journey blindly.

---

## 18. Card anti-factory rule

Cards are one tool, not the default answer.

A rich page fails if most sections are variations of:

```text
heading
→ 3 equal cards
→ heading
→ 3 equal cards
→ heading
→ 3 equal cards
```

Before using a card grid ask whether the content would be stronger as:
- editorial index;
- feature spotlight;
- media rail;
- comparison matrix;
- timeline;
- annotated image;
- ledger/list;
- split story;
- sticky chapter;
- asymmetric mosaic.

---

## 19. Interaction diversity without gimmicks

Interaction may increase distinction, but only when it improves use.

Good uses:
- tabs for alternate states/categories;
- accordion for optional details/FAQ;
- horizontal rail for browseable peers;
- filter for sufficiently large collections;
- sticky chapter for long narrative explanation;
- lightbox for inspectable media.

Avoid:
- scroll-jacking;
- autoplay motion that steals control;
- hidden essential content;
- interaction with no informational benefit;
- heavy JS where static composition is sufficient.

---

## 20. Mobile transformation diversity

Do not make every desktop layout collapse to the identical vertical stack.

Depending on pattern, mobile may use:
- reordered media/copy;
- horizontal scroll rail;
- compact accordion;
- featured item + list;
- reduced mosaic;
- single-column timeline;
- sticky behavior disabled;
- background media converted to inline media;
- secondary visuals hidden only when truly decorative.

Essential content must remain accessible.

---

## 21. Visual Engine handoff

For every section pass to `15-SECTION-IMAGE-ENGINE.md`:

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

Image composition should fit the selected section grammar rather than forcing the section back into a generic image-left/text-right split.

---

## 22. Global Text resilience

Section composition must tolerate editable copy.

Test representative text expansion before PASS:
- heading +25–40%;
- body +20–30%;
- longer CTA;
- longer localized labels.

Novel layout is not acceptable if it only works for one exact generated string length.

---

## 23. Accessibility / semantics

Required:
- logical DOM reading order;
- visible focus states;
- keyboard access to interactive components;
- reduced-motion handling;
- no content dependency on hover only;
- no visual reordering that creates a contradictory assistive-tech order;
- controls use correct semantics/ARIA state when needed.

Asymmetry does not justify semantic disorder.

---

## 24. Performance guard

High-variation UI must remain efficient.

Do not create uniqueness by:
- loading large JS frameworks for one effect;
- embedding multiple autoplay videos;
- using huge offscreen raster assets;
- adding complex animation to every section;
- creating dozens of DOM layers only for decoration.

Prefer CSS/grid/flex and progressive enhancement.

---

## 25. Composition QA state

State model:

```text
COMPOSITION_PLANNED
COMPOSITION_STATIC_PASS
COMPOSITION_VISUAL_PASS
COMPOSITION_RELEASE
```

`COMPOSITION_STATIC_PASS` requires:
- manifest exists;
- every meaningful section has a fingerprint;
- no unexplained exact fingerprint duplicates;
- candidate pattern is semantically valid;
- responsive fallback is defined;
- accessibility constraints are recorded.

`COMPOSITION_VISUAL_PASS` additionally requires screenshot/browser review.

---

## 26. Visual acceptance questions

Before PASS ask:
1. Can I distinguish adjacent sections at a glance without reading the text?
2. Does each section geometry help its content rather than merely decorate it?
3. Do Home and key internal pages have different visible grammar?
4. Would this site still look different from the previous factory site if both were rendered in grayscale?
5. Is variation coming from composition, not only color/images?
6. Does mobile still feel intentionally designed?

If several answers are `no` → `FIX_REQUIRED`.

---

## 27. Release rule

A full site may not reach `RELEASE` until:

```text
SECTION COMPOSITION MANIFEST = complete
same-page exact composition repeats = 0 by default
adjacent repetition gate = PASS
key-page grammar differentiation = PASS
cross-site fingerprint check = PASS when history available
responsive composition = PASS
accessibility composition = PASS
visual screenshot review = PASS
```

The target is **controlled variety with coherent Design DNA**.


---

## 28. Section density and cohesion scoring (v1.1.0)

`content_volume_fit` must include a density/cohesion score, not only whether the words technically fit.

For each candidate, inspect:
- headline visual mass;
- body visual mass;
- media/interaction mass;
- intentional negative space;
- distance between related text nodes;
- total section height at representative widths.

Penalize candidates when:
- content occupies isolated islands in a large section;
- headline mass is disproportionate to body/media;
- more whitespace is created by grid placement than by deliberate editorial intent;
- the section needs artificial `min-height`/padding to look complete.

A candidate with worse novelty but materially better cohesion should win.

### Density modes are not fixed heights
`spacious` means generous readable rhythm, not an empty viewport.
Do not use `spacious` as permission to create unused columns or giant gaps.

---

## 29. Footer Composition Engine (v1.1.0)

Footer composition is selected by module 18 and stored as part of the site fingerprint.

### Footer semantic zones
Possible zones:
- brand/identity;
- optional compact brand/product descriptor (often omitted);
- primary navigation;
- domain/resource navigation;
- legal;
- contact;
- official/source destination;
- optional real newsletter/CTA;
- social only when real;
- bottom bar.

The semantic zones remain accurate; their **geometry and order may vary**.

### Footer family pool
Abstract families:
- `F01_BRAND_LED_ASYMMETRIC_LEDGER`
- `F02_NAVIGATION_MATRIX`
- `F03_CONTACT_LED_SPLIT`
- `F04_CTA_LED_FOOTER_STAGE`
- `F05_STACKED_EDITORIAL_FOOTER`
- `F06_COMPACT_MULTIROW_DIRECTORY`
- `F07_WIDE_BRAND_WITH_SIDE_INDEX`
- `F08_DUAL_BAND_FOOTER`
- `F09_MINIMAL_EDITORIAL_WITH_LEGAL_RAIL`
- `F10_RESOURCE_HEAVY_FOOTER`

These are grammars, not fixed templates.

### Footer independent dimensions
Vary where valid:
- `column_count`: 1–5;
- `column_ratio_signature`;
- brand position: left / center / right / full-width top;
- nav grouping: combined / separated / matrix / rows;
- contact position;
- legal position;
- source/official CTA position;
- CTA presence/absence;
- divider mode;
- surface polarity;
- text alignment;
- bottom-bar layout: left-right / centered / compact multi-item / split.

### Footer fingerprint
Record:

```text
footer_family
column_count
column_ratio_signature
brand_zone_position
nav_group_sequence
contact_zone_position
legal_zone_position
source_cta_position
cta_mode
surface_mode
divider_mode
bottom_bar_signature
mobile_zone_order
footer_composition_fingerprint
```

### Cross-site footer anti-repeat
When recent site fingerprints exist:
- identical footer fingerprint on unrelated consecutive sites = reject;
- same family may repeat only when at least `3` high-impact footer dimensions materially change;
- if the nearest recent footer is visually too similar, mutate at least `2` of:
  - family;
  - column ratios/count;
  - brand position;
  - nav grouping/order;
  - contact/legal placement;
  - surface polarity;
  - bottom-bar signature.

### Mobile
Mobile footer order must be intentional and easy to scan.
Do not use CSS visual reordering that contradicts DOM/assistive-technology order.

---

## 30. Major-image uniqueness handoff (v1.1.0)

Composition planning must mark every major media slot with:

```text
major_media_unique_required: yes/no
visual_role_id
reuse_allowlist_reason_if_any
```

Default for hero + major editorial/content sections:

```text
major_media_unique_required = yes
```

A repeated asset cannot be hidden by changing:
- crop;
- aspect ratio;
- filter;
- overlay;
- compression;
- filename.

Those remain one visual source.

When module 18 selects several image-led sections, it must ensure their media slots also differ in visual role:
- establishing scene;
- overhead/diagrammatic;
- close detail;
- human/action;
- device/object;
- environment;
- annotated board/data;
- atmospheric close.

Do not ask the Visual Engine for five variants of the same scene.



---

## 31. Extended Macro Archetype Library (v2.0.0)

The original families in section 7 remain valid stable IDs. This v2 library adds **165 additional macro archetypes** rather than replacing them.
Together with the existing pool, the engine now has a substantially broader grammar surface.

These IDs define **macro skeletons only**. They are not finished components and must still be composed through the independent dimensions in sections 8 and 32.

### 31.1 Hero / opening additions
- `H11_ASYMMETRIC_EDITORIAL_CANVAS`
- `H12_MEDIA_TRIPTYCH_OPENING`
- `H13_VERTICAL_TITLE_WITH_SIDE_STAGE`
- `H14_PANORAMIC_BAND_HERO`
- `H15_DEVICE_OR_OBJECT_PEDESTAL`
- `H16_TYPOGRAPHIC_LEFT_RAIL_HERO`
- `H17_OFFSET_FRAME_WITH_FLOATING_PROOF`
- `H18_FULL_BLEED_WITH_INSET_COPY_CARD`
- `H19_DUAL_MEDIA_DIAGONAL_HERO`
- `H20_EDITORIAL_COVER_GRID`
- `H21_STACKED_MEDIA_WINDOW_HERO`
- `H22_EDGE_TO_EDGE_OBJECT_STAGE`
- `H23_QUIET_LUXURY_INTRO`
- `H24_KINETIC_ROUTE_HERO`

### 31.17 Editorial / narrative additions
- `C17_ASYMMETRIC_CHAPTER_PAIRS`
- `C18_FLOATING_ASIDE_COLUMNS`
- `C19_EDITORIAL_STAIRS`
- `C20_MEDIA_WINDOW_WITH_FACT_LEDGER`
- `C21_VERTICAL_STORY_RAIL`
- `C22_OFFSET_QUOTE_AND_MEDIA`
- `C23_THREE_ZONE_NARRATIVE`
- `C24_TEXTURE_BAND_WITH_CONTENT_ISLAND`
- `C25_ANNOTATED_OBJECT_STAGE`
- `C26_SPREAD_LAYOUT_EDITORIAL`
- `C27_DOMINANT_MEDIA_WITH_MARGIN_NOTES`
- `C28_NESTED_EDITORIAL_GRID`
- `C29_EDGE_CAPTION_STORY`
- `C30_SPLIT_WITH_VERTICAL_INDEX`
- `C31_STACKED_FEATURE_CHAPTERS`
- `C32_SIDE_LEDGER_WITH_FLOATING_MEDIA`
- `C33_CENTER_SPINE_STORY`
- `C34_ASYMMETRIC_PULLQUOTE_FIELD`
- `C35_EDITORIAL_DIPTYCH`
- `C36_CROSS_AXIS_MEDIA_COPY`
- `C37_TALL_MEDIA_WITH_SHORT_NOTES`
- `C38_INSET_STORY_WITH_OUTER_CAPTION`
- `C39_OPEN_GRID_WITH_EMPHASIS_CELL`
- `C40_SERIES_OF_VARIABLE_WIDTH_BANDS`

### 31.43 Media / showcase additions
- `M01_PANORAMIC_SHOWCASE`
- `M02_DUAL_FRAME_SHOWCASE`
- `M03_ASYMMETRIC_GALLERY_WALL`
- `M04_HORIZONTAL_FILMSTRIP`
- `M05_VERTICAL_FILMSTRIP`
- `M06_FLOATING_MEDIA_CARDS`
- `M07_EDGE_TO_EDGE_IMAGE_WITH_NOTES`
- `M08_MOSAIC_WITH_ONE_HERO_TILE`
- `M09_LAYERED_MEDIA_STACK`
- `M10_SCROLL_SNAP_MEDIA_RAIL`
- `M11_MEDIA_PAIR_WITH_CENTER_NOTE`
- `M12_CROPPED_PORTRAIT_RHYTHM`
- `M13_LANDSCAPE_DIPTYCH`
- `M14_THUMBNAIL_INDEX_WITH_STAGE`
- `M15_SPOTLIGHT_CAROUSEL_STATIC_FALLBACK`
- `M16_ANNOTATED_MEDIA_BOARD`
- `M17_FULL_BLEED_WITH_FLOATING_CAPTIONS`
- `M18_MEDIA_LADDER`
- `M19_OVERLAPPING_FRAME_PAIR`
- `M20_EDITORIAL_CONTACT_SHEET_ORIGINAL_ASSETS_ONLY`
- `M21_MEDIA_STRIPE_SEQUENCE`
- `M22_WIDE_NARROW_WIDE_SEQUENCE`
- `M23_OBJECT_DETAIL_GALLERY`
- `M24_MIXED_RATIO_MEDIA_SHELF`

### 31.69 Discovery / directory additions
- `D11_MAGAZINE_CONTENT_INDEX`
- `D12_ASYMMETRIC_DIRECTORY`
- `D13_FEATURED_PLUS_TWO_RAILS`
- `D14_STACKED_RESOURCE_LEDGER`
- `D15_MASONRY_EDITORIAL_CATALOG`
- `D16_CATEGORY_TABS_WITH_FEATURE_STAGE`
- `D17_ALPHABET_OR_TAG_INDEX`
- `D18_COMPACT_LIST_WITH_PREVIEW`
- `D19_SPLIT_DIRECTORY_WITH_COUNTS`
- `D20_CURATED_THREE_TIER_SHELF`
- `D21_FEATURED_ROW_WITH_MICRO_LIST`
- `D22_RESOURCE_MAP`
- `D23_CONTENT_TABLE_WITH_VISUAL_CALLOUT`
- `D24_MULTI_COLUMN_READING_LIST`
- `D25_SPOTLIGHT_CATALOG_WITH_SIDE_FILTER`
- `D26_RANKED_EDITORIAL_LIST`

### 31.87 Process / data / mechanics additions
- `P11_RADIAL_PROCESS_MAP`
- `P12_LOOP_DIAGRAM_WITH_STEPS`
- `P13_SWIMLANE_PROCESS`
- `P14_VERTICAL_METRIC_RUNWAY`
- `P15_INPUT_OUTPUT_FLOW`
- `P16_BRANCHING_DECISION_PATH`
- `P17_STAGE_CARDS_WITH_CONNECTORS`
- `P18_DIAGONAL_PROGRESS_PATH`
- `P19_CENTERLINE_MILESTONES`
- `P20_STICKY_DIAGRAM_WITH_SCROLLING_NOTES`
- `P21_PROCESS_TABLE_WITH_HIGHLIGHTS`
- `P22_BEFORE_DURING_AFTER_BANDS`
- `P23_STATE_MACHINE_EXPLAINER`
- `P24_ORBITAL_ECONOMY_LOOP`
- `P25_UPGRADE_TREE`
- `P26_CAUSE_EFFECT_LEDGER`
- `P27_STEP_GRID_WITH_DOMINANT_STAGE`
- `P28_PROGRESS_CURVE_WITH_ANNOTATIONS`

### 31.107 Proof / trust additions
- `T09_PROOF_TIMELINE`
- `T10_REVIEW_SPOTLIGHT_WITH_SIDE_QUOTES`
- `T11_METHOD_AND_SOURCE_PANEL`
- `T12_TRUST_BADGES_WITH_CONTEXT_NOT_LOGOS`
- `T13_EVIDENCE_LEDGER`
- `T14_QUOTE_WALL_WITH_ONE_LONGFORM`
- `T15_SOURCE_TRANSPARENCY_STAGE`
- `T16_REVIEW_INDEX`
- `T17_PROOF_BANDS`
- `T18_EDITORIAL_METHOD_SPLIT`
- `T19_FACT_CHECK_RAIL`
- `T20_TRUST_SUMMARY_WITH_LINKS`

### 31.121 FAQ additions
- `Q01_TWO_COLUMN_FAQ_LEDGER`
- `Q02_FAQ_WITH_TOPIC_INDEX`
- `Q03_FAQ_STICKY_CATEGORY_RAIL`
- `Q04_FAQ_SPLIT_BY_INTENT`
- `Q05_FAQ_CARDS_WITH_EXPANDERS`
- `Q06_FAQ_EDITORIAL_ARTICLE`
- `Q07_FAQ_WITH_SOURCE_NOTES`
- `Q08_FAQ_COMPACT_DENSE_LIST`
- `Q09_FAQ_FEATURED_QUESTION_STAGE`
- `Q10_FAQ_TIMELINE`
- `Q11_FAQ_TABS_WITH_STATIC_FALLBACK`
- `Q12_FAQ_SIDE_NOTES`

### 31.135 Contact additions
- `K01_CONTACT_DIRECTORY_GRID`
- `K02_CONTACT_IDENTITY_STAGE`
- `K03_CONTACT_DETAILS_WITH_EDITORIAL_ASIDE`
- `K04_CONTACT_LEDGER_WITH_SUPPORT_SPLIT`
- `K05_CONTACT_COMPACT_THREE_FIELD_BAR`
- `K06_CONTACT_CARDLESS_COLUMNS`
- `K07_CONTACT_WITH_SOURCE_SUPPORT_RAIL`
- `K08_CONTACT_STACKED_BANDS`
- `K09_CONTACT_BRAND_AND_CHANNELS`
- `K10_CONTACT_CENTERED_DETAILS_WITH_SIDE_LINKS`
- `K11_CONTACT_ASYMMETRIC_DIRECTORY`
- `K12_CONTACT_MINIMAL_DETAILS_PLUS_LEGAL`

### 31.149 CTA / closing additions
- `A09_CTA_MEDIA_DIPTYCH`
- `A10_CTA_EDGE_BAND`
- `A11_CTA_CENTER_STAGE_WITH_SIDE_LINKS`
- `A12_CTA_RESOURCE_NEXT_STEPS`
- `A13_CTA_OBJECT_PEDESTAL`
- `A14_CTA_DARK_LIGHT_SPLIT`
- `A15_CTA_SHORT_FORM_LEDGER`
- `A16_CTA_STICKY_BOTTOM_STAGE_STATIC_FALLBACK`
- `A17_CTA_IMAGE_RAIL_WITH_ACTION`
- `A18_CTA_EDITORIAL_EPILOGUE`

### 31.161 Long-form / About / legal additions
- `L08_ARTICLE_WITH_MARGIN_GLOSSARY`
- `L09_ARTICLE_WITH_CHAPTER_NAV`
- `L10_LEGAL_TWO_COLUMN_READING_FRAME`
- `L11_LEGAL_SUMMARY_PLUS_ARTICLE`
- `L12_RESOURCE_LONGFORM_WITH_MEDIA_BREAKS`
- `L13_ABOUT_EDITORIAL_MANIFEST`
- `L14_ABOUT_METHOD_AND_SOURCE`
- `L15_UTILITY_DIRECTORY_PAGE`
- `L16_LEGAL_INDEX_WITH_STICKY_SECTION_SUMMARY`

### 31.172 Footer additions
- `F11_BRAND_BANNER_OVER_DIRECTORY`
- `F12_ASYMMETRIC_TWO_TIER_DIRECTORY`
- `F13_CENTERED_BRAND_WITH_SIDE_COLUMNS`
- `F14_CONTACT_STRIP_OVER_NAV_GRID`
- `F15_RESOURCE_COLUMNS_WITH_BRAND_RAIL`
- `F16_LEGAL_RAIL_OVER_WIDE_NAV`
- `F17_BRAND_PANEL_PLUS_COMPACT_MATRIX`
- `F18_THREE_BAND_EDITORIAL_FOOTER`
- `F19_MINIMAL_TOP_BRAND_BOTTOM_DIRECTORY`
- `F20_CTA_AND_DIRECTORY_SPLIT`
- `F21_OFFSET_CONTACT_AND_LEGAL`
- `F22_MAGAZINE_MASTHEAD_FOOTER`
- `F23_WIDE_SOURCE_STAGE_WITH_NAV`
- `F24_COMPACT_INDEX_WITH_BRAND_SIGNATURE`


## 32. Hierarchical Layout Grammar

Do not choose a section as one fixed template. Compose it through layers:

```text
SEMANTIC INTENT
→ MACRO ARCHETYPE
→ GRID TOPOLOGY
→ CONTAINER TOPOLOGY
→ CONTENT ANCHOR
→ MEDIA TOPOLOGY
→ MEDIA DOMINANCE
→ SURFACE / BACKGROUND FAMILY
→ EDGE / OVERLAP MODE
→ CARD / LIST GEOMETRY
→ DENSITY
→ INTERACTION
→ MOTION
→ MOBILE TRANSFORMATION
→ ACCESSIBILITY / PERFORMANCE FILTER
```

### Grid topology pool
- mono-column editorial;
- balanced split;
- 40/60 or 60/40 split;
- 33/67 or 67/33 split;
- three-zone editorial;
- nested grid;
- stepped/stair grid;
- radial/orbit diagram field;
- center-spine;
- rail + stage;
- sticky rail + flowing content;
- mosaic/bento;
- layered overlap;
- edge-to-edge stage;
- ledger/table/list;
- timeline/runway;
- serpentine/alternating path.

### Content anchor pool
- top-left;
- top-center;
- center-left;
- center;
- side rail;
- bottom-left;
- bottom band;
- floating inset;
- margin note system;
- split anchors.

### Media topology pool
- no major media;
- one dominant stage;
- two unequal frames;
- diptych;
- triptych;
- mosaic;
- rail/shelf;
- background media;
- object/detail macro;
- annotated diagram;
- SVG line-art field;
- media + thumbnail index;
- edge crop;
- floating frame;
- alternating media chapters.

A change in only alignment, color or image side is **not sufficient structural novelty** when the macro wireframe remains the same.

## 33. Page Rhythm Recipe Engine

Before choosing section families for each key page, select or derive a `PAGE RHYTHM RECIPE`.
The recipe controls alternation of density, media dominance, surface polarity and interaction intensity.

Reference recipes:

1. `R01_IMMERSIVE_COMPACT_EDITORIAL_DATA_MEDIA_QUIET_CLOSE`
2. `R02_EDITORIAL_INDEX_WIDE_MEDIA_DENSE_GRID_STORY_PROOF_CLOSE`
3. `R03_PRODUCT_STAGE_DIRECTORY_TIMELINE_FULL_BLEED_LEDGER_FAQ_CTA`
4. `R04_QUIET_OPEN_DATA_RAIL_MEDIA_STORY_DIRECTORY_MINIMAL_CLOSE`
5. `R05_MEDIA_OPEN_COMPACT_PROOF_EDITORIAL_MOSAIC_PROCESS_CTA`
6. `R06_OBJECT_STAGE_INDEX_DIAGRAM_STORY_MEDIA_RAIL_FAQ_CLOSE`
7. `R07_TEXT_FIRST_MEDIA_BREAK_LEDGER_STICKY_STORY_PROOF_CLOSE`
8. `R08_PANORAMIC_OPEN_COMPACT_LIST_PROCESS_MEDIA_DIPTYCH_CTA`
9. `R09_ASYMMETRIC_OPEN_RESOURCE_INDEX_MEDIA_RUNWAY_TRUST_CLOSE`
10. `R10_CENTERED_OPEN_EDGE_MEDIA_EDITORIAL_GRID_DATA_FAQ_EPILOGUE`
11. `R11_STAGE_PROOF_DIRECTORY_STICKY_DIAGRAM_MEDIA_SHELF_CTA`
12. `R12_COVER_OPEN_LIST_MOSAIC_PROCESS_QUOTE_WALL_RESOURCE_CLOSE`
13. `R13_SPLIT_OPEN_COMPACT_METRICS_CHAPTERS_DIAGRAM_DIRECTORY_CTA`
14. `R14_QUIET_INTRO_EDITORIAL_STAIRS_MEDIA_STAGE_LEDGER_FAQ_CLOSE`
15. `R15_OBJECT_OPEN_THREE_ZONE_STORY_INDEX_PROCESS_MEDIA_CLOSE`
16. `R16_MEDIA_TRIPTYCH_PROOF_RAIL_EDITORIAL_RUNWAY_DIRECTORY_CTA`
17. `R17_TYPOGRAPHIC_OPEN_MEDIA_WINDOW_FACT_LEDGER_GALLERY_FAQ_CLOSE`
18. `R18_FRAME_OPEN_COMPACT_BANDS_ANNOTATED_MEDIA_RESOURCE_PROOF_CTA`
19. `R19_SIDEWAYS_OPEN_INDEX_STICKY_NOTES_MEDIA_LEDGER_CLOSE`
20. `R20_DEPTH_OPEN_METRICS_DIAGRAM_MIXED_MEDIA_REVIEW_EPILOGUE`
21. `R21_MINIMAL_OPEN_DIRECTORY_MEDIA_BREAK_ARTICLE_PROOF_CLOSE`
22. `R22_STAGE_OPEN_TIMELINE_CATEGORY_SHELF_METHOD_FAQ_CTA`
23. `R23_EDITORIAL_COVER_COMPACT_PROCESS_MOSAIC_TRUST_RESOURCE_CLOSE`
24. `R24_MEDIA_OPEN_LEDGER_SERPENTINE_STORY_DATA_QUIET_CLOSE`

The semantic page manifest may reorder only sections marked `can_reorder_with_peers=yes`.
A rhythm recipe never overrides content logic.

## 34. Recent-History Diversity Memory

When fingerprint history is available, compare against approximately the latest `15–20` unrelated sites.
Track recency/frequency for:
- macro family;
- hero family;
- macro topology;
- Home sequence;
- adjacent 2-section signature;
- adjacent 3-section signature;
- media rhythm;
- background rhythm;
- card geometry;
- CTA family;
- footer family.

Suggested scoring additions:

```text
family_recency_penalty
macro_topology_recency_penalty
sequence_bigram_penalty
sequence_trigram_penalty
recent_hero_penalty
recent_footer_penalty
rare_valid_family_bonus
underused_topology_bonus
```

Rules:
- a hero family used on the immediately preceding unrelated site receives a strong penalty unless clearly best for semantics;
- repeated Home 3-section subsequences receive a strong penalty;
- changing only palette/type/images does not clear a structural penalty;
- do not invent cross-site history if fingerprints are unavailable.

## 35. Portfolio / Batch Diversity Mode

When building several sites in a batch or sequential run, plan them as a portfolio rather than independent isolated pages.

Before locking each new Home:
1. inspect recent fingerprints;
2. reserve different hero topology where practical;
3. reserve different dominant macro structures;
4. vary page rhythm recipe;
5. vary footer family;
6. vary visual-medium rhythm;
7. run similarity check;
8. mutate until below threshold.

This is especially important after `5+` sites in the same GEO/niche family.

## 36. Structural Diversity Targets

For a rich Home with `7+` meaningful sections:
- unique macro family ratio should normally be `>= 0.80`;
- repeated macro family requires semantic justification;
- no exact section fingerprint repeat;
- avoid more than two sections dominated by the same card/list geometry;
- avoid a run of three sections with the same primary topology;
- adjacent sections should usually differ in at least four high-impact dimensions;
- Home wireframe should remain distinguishable from recent unrelated sites with colors/images removed.

## 37. Background Composition Handoff

Each meaningful section records:

```text
background_family
background_asset_id_if_any
background_intensity
background_contrast_zone
background_motion_mode
background_mobile_simplification
```

Module 18 chooses whether a section needs a distinctive background role; modules 15/16 create the actual asset.
Do not place an illustrated background behind every section. Background rhythm must include intentional quiet/rest sections.

## 38. Footer pool expansion

The footer family pool now includes the original `F01–F10` plus `F11–F24` from section 31.
The absolute bottom layer is separate from the main footer geometry.

Supported bottom-layer signatures include:
- copyright-only centered;
- copyright-only left;
- copyright left + tiny status right when semantically required;
- compact split metadata;
- legal links above + copyright-only absolute bottom.

When `copyright-only absolute bottom` is selected, legal links/disclaimers must live in the layer above.

## 39. Section Library Usage Audit

For every release record:

```text
available_macro_family_count
eligible_family_count_per_section
selected_family_count
recent_family_usage_summary
page_rhythm_recipe
sequence_bigram_signature
sequence_trigram_signature
structural_diversity_ratio
```

If a large library exists but selection repeatedly collapses to a tiny subset, treat that as a factory defect rather than acceptable randomness.



## 40. Live UI/UX Section Research Engine (v2.1.0)

Module 18 now performs a **current-web research pass** before locking compositions when web access is available.

### 40.1. Research sample

Default target where practical:

```text
curated / award / pattern sources: 3–5
live niche / adjacent-niche websites: 6–12
recent factory fingerprints: approximately 15–20 when available
```

Possible discovery pools include Awwwards, SiteInspire, Landbook, Lapa Ninja, One Page Love, Mobbin, Untitled UI and current niche-specific live sites discovered through search.
Do not hard-code any one provider as mandatory.

For interaction-rich projects, when current references allow it, inspect at least `2` examples with meaningful tabs/rails/sliders/sticky/reveal/microinteraction behavior and record the abstract interaction pattern rather than copying implementation.

### 40.2. LIVE UIUX RESEARCH MANIFEST

For every inspected reference record internally:

```text
reference_id
url
source_type: award_gallery | section_library | live_site
retrieved_or_observed_date
niche_relevance
page_type
observed_section_role
macro_topology
content_flow
media_topology
density_profile
surface_or_background_logic
transition_to_next_section
interaction_or_motion_class
mobile_behavior_if_observable
abstract_takeaway
copy_prohibited: yes
asset_reuse_prohibited: yes unless separately licensed
```

Do not store copied proprietary markup or large verbatim text.

### 40.3. LIVE SECTION PATTERN BANK

Convert research observations into temporary abstract candidates:

```text
LRP01 ... LRPN
```

Each live-research pattern must be expressed only as a grammar recipe, for example:

```text
semantic_fit
macro_topology
content_anchor
media_mode
density
transition
modifier_compatibility
mobile_transformation
```

A temporary LRP pattern is not a template. It enters the same semantic/accessibility/performance filters as permanent families.

### 40.4. Anti-clone recombination rule

A research-derived section should normally combine traits from:
- at least two independent reference observations; or
- one observation plus multiple internal grammar dimensions.

Before acceptance, materially mutate at least `4` high-impact dimensions relative to the closest single external reference when those dimensions are observable.

Examples of high-impact mutation:
- macro topology;
- shell/bleed behavior;
- content anchor;
- media topology;
- section height/density;
- foreground/background relationship;
- card/list geometry;
- transition;
- mobile transformation.

Do not reproduce more than two adjacent recognizable sections from one reference site's sequence.

## 41. Morphological Modifier Library

Macro family selection alone is insufficient. Every meaningful section receives a modifier stack chosen from compatible axes.

### 41.1. Shell / canvas modifiers
- `SH01_CONTAINED_NARROW`
- `SH02_CONTAINED_WIDE`
- `SH03_EDGE_TO_EDGE`
- `SH04_ONE_SIDE_BLEED_LEFT`
- `SH05_ONE_SIDE_BLEED_RIGHT`
- `SH06_INSET_ISLAND`
- `SH07_NESTED_SHELLS`
- `SH08_OFFSET_CANVAS`
- `SH09_FULL_WIDTH_WITH_INNER_RAIL`
- `SH10_CENTERED_STAGE_WITH_MARGIN_FIELD`
- `SH11_OVERFLOWING_MEDIA_SHELL`
- `SH12_ASYMMETRIC_GUTTER_SHELL`

### 41.2. Content-flow modifiers
- `CF01_LINEAR_EDITORIAL`
- `CF02_STAGGERED_COLUMNS`
- `CF03_CENTER_SPINE`
- `CF04_SIDE_RAIL_WITH_CHAPTERS`
- `CF05_TOP_HEAVY_THEN_SPREAD`
- `CF06_BOTTOM_ANCHORED_COPY`
- `CF07_ZIGZAG_READING_PATH`
- `CF08_SERPENTINE_FLOW`
- `CF09_INDEX_THEN_EXPANSION`
- `CF10_LEDGER_FLOW`
- `CF11_MARGIN_NOTE_FLOW`
- `CF12_FLOATING_ASIDES`
- `CF13_CHAPTER_BANDS`
- `CF14_DIAGONAL_READING_PATH`
- `CF15_DENSE_TO_QUIET_FLOW`
- `CF16_QUIET_TO_DENSE_FLOW`

### 41.3. Media-integration modifiers
- `MI01_MEDIA_BACKGROUND`
- `MI02_MEDIA_EDGE_CROP`
- `MI03_MEDIA_INSET_WINDOW`
- `MI04_MEDIA_FLOATING_FRAME`
- `MI05_MEDIA_MULTI_RATIO_SHELF`
- `MI06_MEDIA_ANNOTATED_STAGE`
- `MI07_MEDIA_THUMBNAIL_TO_STAGE`
- `MI08_MEDIA_VERTICAL_RUNWAY`
- `MI09_MEDIA_HORIZONTAL_RAIL`
- `MI10_MEDIA_OVERLAP_COPY`
- `MI11_MEDIA_BETWEEN_COPY_COLUMNS`
- `MI12_MEDIA_OBJECT_PEDESTAL`
- `MI13_MEDIA_DIPTYCH_UNEQUAL`
- `MI14_MEDIA_TRIPTYCH_VARIABLE`
- `MI15_MEDIA_GHOSTED_BACKPLATE`
- `MI16_NO_MAJOR_MEDIA_DATA_LED`

### 41.4. Edge / framing modifiers
- `EF01_FRAMELESS`
- `EF02_HAIRLINE_FRAME`
- `EF03_HEAVY_TOP_RULE`
- `EF04_SIDE_RULE`
- `EF05_ROUNDED_ISLAND`
- `EF06_SQUARE_EDITORIAL_FRAME`
- `EF07_CUT_CORNER_FRAME`
- `EF08_OPEN_FRAME_TWO_EDGES`
- `EF09_LAYERED_BORDER`
- `EF10_SOFT_SHADOW_FLOAT`
- `EF11_INSET_BORDER_FIELD`
- `EF12_DIVIDER_DRIVEN`

### 41.5. Annotation / index modifiers
- `AN01_NONE`
- `AN02_NUMERIC_INDEX`
- `AN03_ROMAN_CHAPTERS`
- `AN04_MARGIN_LABELS`
- `AN05_COORDINATE_LABELS`
- `AN06_INLINE_FACT_TAGS`
- `AN07_CALLOUT_LEADERS`
- `AN08_SIDE_GLOSSARY`
- `AN09_PROGRESS_MARKERS`
- `AN10_SOURCE_NOTES`

### 41.6. Layering / depth modifiers
- `LY01_FLAT`
- `LY02_TWO_PLANE`
- `LY03_THREE_PLANE`
- `LY04_MEDIA_BEHIND_COPY`
- `LY05_COPY_OVER_MEDIA_SAFE_ZONE`
- `LY06_FOREGROUND_OBJECT_OVERFLOW`
- `LY07_FLOATING_ANNOTATION_LAYER`
- `LY08_GHOSTED_BACKGROUND_DIAGRAM`
- `LY09_NESTED_SURFACE_DEPTH`
- `LY10_PARALLAX_OPTIONAL_STATIC_FALLBACK`

### 41.7. Density/rhythm modifiers
- `DR01_COMPACT`
- `DR02_STANDARD`
- `DR03_SPACIOUS_EARNED`
- `DR04_DENSE_LEDGER`
- `DR05_COMPACT_TOP_SPACIOUS_BOTTOM`
- `DR06_SPACIOUS_TOP_DENSE_BOTTOM`
- `DR07_ALTERNATING_DENSITY`
- `DR08_MEDIA_DENSE_COPY_LIGHT`
- `DR09_COPY_DENSE_MEDIA_LIGHT`
- `DR10_MICRO_MACRO_CONTRAST`

### 41.8. Section-transition modifiers
- `ST01_HARD_CUT`
- `ST02_COLOR_POLARITY_FLIP`
- `ST03_OVERLAPPING_EDGE`
- `ST04_MEDIA_BRIDGE`
- `ST05_DIAGONAL_VISUAL_HANDOFF`
- `ST06_CONTINUOUS_GRID_HANDOFF`
- `ST07_FADE_TO_QUIET`
- `ST08_QUIET_TO_STAGE`
- `ST09_RULE_OR_LEDGER_HANDOFF`
- `ST10_SHARED_BACKGROUND_MORPH`
- `ST11_OBJECT_CONTINUATION`
- `ST12_SPACING_COMPRESSION_HANDOFF`

### 41.9. Mobile transformation modifiers
- `MT01_STACK_TEXT_FIRST`
- `MT02_STACK_MEDIA_FIRST`
- `MT03_RAIL_TO_SNAP`
- `MT04_MOSAIC_TO_FEATURED_LIST`
- `MT05_STICKY_TO_STATIC_CHAPTERS`
- `MT06_OVERLAP_TO_SEPARATE_BLOCKS`
- `MT07_SIDE_RAIL_TO_TOP_INDEX`
- `MT08_TABLE_TO_CARDS`
- `MT09_DIPTYCH_TO_HORIZONTAL_SCROLL`
- `MT10_FLOATING_ASIDES_TO_INLINE_NOTES`
- `MT11_BACKGROUND_ART_TO_RESTRAINED_CROP`
- `MT12_MULTI_ZONE_TO_PRIORITY_STACK`

Total v2.1 modifier IDs in this library: `110`.

## 42. Modifier selection rules

For each meaningful rich section:
- choose one compatible macro archetype;
- choose normally `4–7` meaningful modifiers from distinct axes;
- do not force modifiers that do not improve the semantic section;
- preserve accessibility and source order.

Default anti-repeat:
- exact modifier stack repeated on the same rich page = `0`;
- adjacent sections should normally share no more than `2` high-impact modifier axes;
- same semantic section across consecutive unrelated sites receives a penalty if macro + modifier stack is too similar;
- selection receives `underused_modifier_bonus` and `recent_modifier_penalty` when history exists.

## 43. Page silhouette / wireframe diversity

Before BUILD lock and again at Visual QA, compare the page as a simplified silhouette:
- hide colors;
- ignore brand typeface;
- reduce imagery to neutral blocks;
- compare section heights, dominant axes, media slots, card/list fields, transitions and footer silhouette.

If a new unrelated site's Home remains obviously recognizable as a recent factory wireframe, change at least `5` high-impact structural dimensions before release.

Cosmetic changes never satisfy this gate.

## 44. Research freshness and relevance

Live research should prefer:
- recently published/updated design references;
- current live sites;
- niche-relevant or audience-relevant examples;
- high-quality sources with clear page/section visibility.

Old references may still contribute timeless structural ideas, but a new BUILD should not claim "current UI/UX research" if the inspected corpus is stale.

The research manifest must distinguish:
```text
CURRENT_REFERENCE
EVERGREEN_REFERENCE
UNAVAILABLE_OR_BLOCKED
```

## 45. Dynamic pattern-bank release artifact

For full-site builds with web research available, export:

```text
LIVE-UIUX-RESEARCH-MANIFEST.json
LIVE-SECTION-PATTERN-BANK.json
```

These are QA/build artifacts, not part of the public WordPress theme unless explicitly requested.



## 46. Interaction Pattern Library v1

Interaction is selected after semantic/content fit and before final visual lock. It is part of the section fingerprint.

### Slider / rail families
- `IP01_SNAP_CARD_RAIL`
- `IP02_FEATURED_STAGE_WITH_THUMB_RAIL`
- `IP03_MEDIA_STORY_SLIDER`
- `IP04_COMPARISON_BEFORE_AFTER_SLIDER`
- `IP05_QUOTE_OR_PROOF_RAIL`
- `IP06_CHAPTER_CAROUSEL_WITH_PROGRESS`
- `IP07_CATEGORY_PEEK_RAIL`
- `IP08_VERTICAL_SLIDE_DECK_DESKTOP_STACK_MOBILE`

### Tabs / switcher families
- `IP09_CONTENT_TABS_UNDERLINE`
- `IP10_SEGMENTED_STATE_SWITCHER`
- `IP11_MEDIA_TABS_STAGE`
- `IP12_COMPARISON_MODE_SWITCHER`
- `IP13_CATEGORY_TAB_DIRECTORY`
- `IP14_TIMELINE_PHASE_SWITCHER`
- `IP15_DEVICE_OR_CONTEXT_SWITCHER`

### Accordion / reveal families
- `IP16_EDITORIAL_ACCORDION`
- `IP17_SPLIT_ACCORDION_WITH_MEDIA`
- `IP18_NUMBERED_DISCLOSURE_LEDGER`
- `IP19_FAQ_GROUPED_DISCLOSURE`
- `IP20_PROGRESSIVE_DETAIL_REVEAL`
- `IP21_MOBILE_ACCORDION_DESKTOP_OPEN_CHAPTERS`

### Sticky / scroll-linked families
- `IP22_STICKY_CHAPTER_RAIL`
- `IP23_STICKY_MEDIA_STATE_CHANGE`
- `IP24_PROGRESS_LEDGER_WITH_SCROLL_MARKER`
- `IP25_SCROLL_SNAP_CHAPTERS_OPTIONAL`
- `IP26_STICKY_COMPARISON_STAGE`

### Filter / comparison / utility families
- `IP27_FILTERABLE_CATALOG`
- `IP28_TAG_FILTER_RAIL`
- `IP29_COMPARISON_MATRIX_SWITCHER`
- `IP30_SORTABLE_FACT_LEDGER_LIGHTWEIGHT`
- `IP31_RELATED_CONTENT_SWITCHER`

### Media inspection families
- `IP32_IMAGE_LIGHTBOX_GALLERY`
- `IP33_ANNOTATED_MEDIA_HOTSPOTS`
- `IP34_ZOOMABLE_DIAGRAM_INSPECTION`
- `IP35_AUDIO_OR_WAVEFORM_PREVIEW_WHEN_REAL`
- `IP36_VIDEO_OR_MOTION_POSTER_PLAY_WHEN_REAL`

Total interaction families: `36`.

## 47. Hover / Focus Microinteraction Library

Hover is a secondary enhancement. The same semantic affordance must remain available through `:focus-visible` and touch-safe states where relevant.

- `HV01_BORDER_TRACE`
- `HV02_UNDERLINE_SLIDE`
- `HV03_MEDIA_ZOOM_SUBTLE`
- `HV04_MEDIA_PAN_SUBTLE`
- `HV05_SURFACE_LIFT_LOW`
- `HV06_SURFACE_INVERT`
- `HV07_ACCENT_EDGE_REVEAL`
- `HV08_ICON_TRANSLATE`
- `HV09_ICON_ROTATE_MICRO`
- `HV10_METADATA_REVEAL_INLINE`
- `HV11_BACKGROUND_TINT_SHIFT`
- `HV12_TEXT_ACCENT_SHIFT`
- `HV13_IMAGE_DESAT_TO_COLOR`
- `HV14_IMAGE_COLOR_TO_TINT`
- `HV15_SOFT_GLOW_LOCAL`
- `HV16_DEPTH_PARALLAX_POINTER_LITE`
- `HV17_MASK_WIPE_MEDIA`
- `HV18_SPLIT_PANEL_EXPAND`
- `HV19_NUMBER_OR_INDEX_EMPHASIS`
- `HV20_CURSOR_FOLLOW_ACCENT_LITE`
- `HV21_CARD_INTERNAL_REBALANCE`
- `HV22_LINK_ARROW_REVEAL`
- `HV23_RULE_LENGTHEN`
- `HV24_NONE_STATIC_CONFIDENT`

Total hover/focus families: `24`.

Do not use the same hover family for every card/link. `HV24_NONE_STATIC_CONFIDENT` is intentionally valid.

## 48. Interaction selection + diversity rules

For Home when content supports interaction:
- normal target `2–4` meaningful interactive sections;
- normally use at least `2` different interaction classes when more than one interactive moment exists;
- no single interaction family should dominate the page;
- `accordion` does not satisfy all interaction diversity by itself.

For key internal pages:
- normal target `1–3` meaningful interactive moments;
- page grammar determines whether tabs, reveal, rail, sticky or static is more appropriate.

Interaction contributes to:
- section fingerprint;
- page composition fingerprint;
- site interaction profile;
- recent-history similarity penalty.

Pure interaction randomization is forbidden. First pass: semantic fit. Second pass: accessibility/performance. Third pass: seeded weighted diversity.

## 49. Slider / carousel contract

Default:
- user-controlled;
- previous/next buttons when more than one viewport of content exists;
- keyboard operable;
- touch/swipe or CSS scroll-snap where appropriate;
- visible position/progress cue when useful;
- no essential information hidden only in inaccessible offscreen state;
- autoplay = off by default;
- infinite looping only when it does not confuse focus/order and has a strong reason.

Prefer CSS scroll-snap/vanilla JS before heavy dependencies.

## 50. Tabs / accordion contract

Tabs:
- tablist/tab/button semantics where JS tabs are used;
- arrow-key behavior where applicable;
- `aria-selected`, focus handling and panel relationships coherent;
- all panel content exists in DOM;
- mobile may transform to accordion/stack when tabs become cramped.

Accordion:
- native `details/summary` is preferred when it fits;
- otherwise button + `aria-expanded` + controlled region;
- FAQ answers remain crawlable/readable in HTML;
- do not collapse every long page section merely to make it look compact.

## 51. Motion intensity profiles

- `MO01_NONE`
- `MO02_MICRO_ONLY`
- `MO03_SUBTLE_REVEAL`
- `MO04_MEDIA_MOTION_LITE`
- `MO05_PROGRESS_LINKED_LITE`
- `MO06_INTERACTIVE_STAGE_CONTROLLED`

Normal rich editorial default is usually `MO02–MO04`, not constant motion.

Never use motion to hide loading delays, force scroll, or make basic reading dependent on animation.



## 52. HARD DIVERSITY MODE — random-from-distant-pool (v3.1.0)

This mode is **ON by default for every new unrelated full-site BUILD**.
Same-site updates keep the existing composition seed and are exempt unless an explicit redesign is requested.

### 52.1. Goal

The factory must not merely choose a different layout ID. It must choose a section whose **visible silhouette is materially different** from nearby sections and recent unrelated sites.

For common roles such as Hero, Feature, Process, Proof, FAQ, CTA, Gallery, Contact and Footer, selection is intentionally slower when needed:

```text
ROLE POOL
→ SEMANTIC / CONTENT / MEDIA FILTER
→ HARD VISUAL-DISTANCE FILTER
→ TOPOLOGY-CLUSTER RANDOM DRAW
→ ARCHETYPE RANDOM DRAW
→ MODIFIER RANDOM DRAW
→ IMPLEMENTATION BLUEPRINT
→ NEUTRAL WIREFRAME CHECK
→ REROLL / MUTATE IF TOO SIMILAR
```

Quality filters happen first. **Similarity is then a blocker, not merely a soft penalty.**

### 52.2. Structural signature required for every candidate

Every permanent or live-research layout candidate must resolve to a normalized structural signature:

```text
topology_cluster
primary_axis
shell_or_bleed_mode
content_anchor
content_flow
media_topology
media_dominance
card_or_list_geometry
layering_depth
overlap_mode
surface_polarity_role
density_profile
transition_family
interaction_family
mobile_transformation
```

Two IDs with near-identical signatures are treated as the same visual family for diversity purposes.
Renaming classes, swapping image left/right, recoloring, changing radius or changing copy does not create a new family.

### 52.3. Topology clusters

At minimum classify layouts into broad visual clusters such as:

```text
TC01_SPLIT_EDITORIAL
TC02_FULL_BLEED_STAGE
TC03_FRAMED_STAGE
TC04_MOSAIC_BENTO
TC05_LEDGER_INDEX
TC06_RAIL_FILMSTRIP
TC07_STICKY_CHAPTER
TC08_CENTERED_STATEMENT
TC09_OBJECT_PEDESTAL
TC10_TIMELINE_PROCESS
TC11_DATA_MATRIX
TC12_EDITORIAL_SPREAD
TC13_LAYERED_OVERLAP
TC14_ASYMMETRIC_CANVAS
TC15_GALLERY_WALL
TC16_HORIZONTAL_FLOW
TC17_STACKED_BANDS
TC18_ANNOTATED_MEDIA
TC19_DIRECTORY_RESOURCE
TC20_QUIET_TEXT_LED
```

The library may add more clusters. The purpose is to prevent 30 differently named layouts from collapsing into one split/card silhouette.

### 52.4. Hard structural distance

Use a normalized structural-distance score `0.00–1.00` based on high-impact dimensions, not pixels or colors.
Suggested weighting:

```text
topology cluster         0.22
shell / bleed            0.12
content anchor / flow    0.12
media topology           0.14
media dominance          0.08
card/list geometry       0.08
layering / overlap       0.08
density / transition     0.06
interaction              0.04
mobile transformation    0.06
```

Default minimums for new unrelated sites:

```text
adjacent major sections on one page          >= 0.62
same-role sections on one site               >= 0.66
new Hero vs each of last 8 available Heroes >= 0.72
new Footer vs each of last 6 available       >= 0.68
Home silhouette vs recent unrelated Home     >= 0.68
key internal page vs sibling page silhouette >= 0.58
```

If history is unavailable, enforce the same-page and same-site gates and record that cross-site comparison was unavailable.

### 52.5. Uniform cluster randomness after quality filtering

In HARD DIVERSITY MODE, section 10's weighted scoring is used to establish **eligibility**, not to force the highest-ranked familiar pattern.

After blockers and minimum-quality checks:
1. remove every candidate below the required structural-distance threshold;
2. group remaining candidates by `topology_cluster`;
3. exclude recently used clusters for the same semantic role when enough alternatives exist;
4. choose one eligible topology cluster by **seeded random draw with approximately equal cluster probability**;
5. choose one archetype inside that cluster by seeded random draw;
6. choose compatible modifier axes by seeded random draw while enforcing modifier-distance gates;
7. build the actual implementation blueprint;
8. run the wireframe check;
9. reroll if the rendered/derived silhouette is still too close.

This prevents semantic score from repeatedly selecting the same safe split/card family.

### 52.6. Recent-role exclusion windows

When recent fingerprints exist and sufficient alternatives remain:

```text
Hero topology cluster: hard exclude last 5 unrelated sites
Hero exact macro family: hard exclude last 10 unrelated sites
Footer topology cluster: hard exclude last 4 unrelated sites
Footer exact family: hard exclude last 8 unrelated sites
FAQ exact family: hard exclude last 4 unrelated sites
CTA exact family: hard exclude last 5 unrelated sites
Process / Feature exact family: hard exclude last 4 unrelated sites
```

If exclusion leaves fewer than `4` valid candidates, relax the oldest exclusion first — never the current-site similarity gates.

### 52.7. Same-page visual separation

For rich pages:
- adjacent major sections may not share the same `topology_cluster` by default;
- the same dominant topology may appear at most twice on a page and never consecutively unless semantics require it;
- two split-derived sections are not considered different merely because left/right is mirrored;
- two card sections require materially different shell, hierarchy and topology or one must be replaced;
- Hero and section 2 must use different topology clusters;
- final CTA must not reuse the Hero's visible stage geometry.

For Home with `7+` meaningful sections, target:

```text
unique_topology_cluster_count >= 6
unique_macro_family_ratio >= 0.85
adjacent_distance_failures = 0
```

### 52.8. Reroll-before-accept rule

A selected layout is provisional until the implementation blueprint and neutral wireframe are checked.

If similarity fails:

```text
REROLL_1: choose another archetype from a different eligible cluster
REROLL_2: choose another cluster
REROLL_3: mutate high-impact shell/media/content-flow dimensions
REROLL_4: synthesize a new grammar from underused compatible dimensions
```

Do not accept a familiar layout merely because repeated rerolls take longer.

### 52.9. New-grammar escape hatch

If no permanent archetype can satisfy semantic quality + hard distance:
- create a new abstract grammar from the existing modifier dimensions;
- assign a temporary/new family ID;
- verify accessibility/mobile behavior;
- add it to the internal pattern bank only after QA.

`NO_DISTANT_CANDIDATE` is a reason to create/mutate a layout, not a reason to reuse a similar one.

### 52.10. Mobile must also be different

Diversity is checked at desktop **and mobile silhouette level**.
Do not let all desktop layouts collapse into `text → image → text` stacks.

Where semantics permit, rotate among:
- text-first stack;
- media-first stack;
- featured item + compact list;
- snap rail;
- reduced mosaic;
- chapter/index stack;
- timeline;
- inline annotated media;
- table-to-cards;
- quiet editorial stack;
- background-to-inline-media conversion.

Mobile uniqueness never overrides source order, accessibility or `horizontal overflow = 0`.

### 52.11. Hard diversity build artifact

Every full new site records:

```text
HARD_DIVERSITY_REPORT
mode = ON
role_candidate_counts{}
role_excluded_recent_families{}
selected_topology_clusters{}
selected_macro_families{}
pairwise_adjacent_distances[]
hero_recent_distances[]
footer_recent_distances[]
home_recent_silhouette_distance
reroll_count
new_grammar_count
cross_site_history_available
```

Missing report for a new full-site BUILD = `FIX_REQUIRED`.



## 53. ALL-PAGES RANDOM COMPOSITION MODE (v3.2)

Hard Diversity applies to **every managed public page**, not only Home.

### 53.1. Independent page composition seed

For every managed page create and persist:

```text
page_composition_nonce
page_composition_seed = HASH(site_composition_seed + page_key + page_composition_nonce)
```

Rules:
- new site → every managed page receives its own new page nonce;
- same-site update → preserve the existing page nonce by default;
- newly added page → generate a new page nonce only for that page;
- explicit redesign → page nonce may rotate and the redesign is recorded;
- Home's selected layouts must never become the default renderer for internal pages.

The page nonce is internal build metadata and is not public content.

### 53.2. Scope

This mode applies to the content composition of at least:
- Home;
- About;
- Contact;
- Guide / How-to / Mechanics;
- FAQ / Resources;
- category / catalog / library / comparison pages;
- editorial/domain pages;
- Privacy;
- Terms;
- Cookies;
- 404;
- any other factory-managed public page.

Site-wide global navigation and the same-site footer may remain structurally stable across pages because consistency is useful there. Their **page handoff and surrounding section geometry** may still vary when valid.

### 53.3. Random-first page construction

For each page:

```text
SEMANTIC PAGE PLAN
→ PAGE-SPECIFIC NONCE
→ PAGE RHYTHM CANDIDATE POOL
→ RANDOM VALID RHYTHM FAMILY
→ FOR EACH SECTION:
   ROLE-SCOPED LAYOUT POOL
   → HARD FILTER
   → TOPOLOGY CLUSTERS
   → RANDOM CLUSTER
   → RANDOM DISTANT LAYOUT
   → RANDOM COMPATIBLE MODIFIER STACK
→ PAGE WIREFRAME
→ INTRA-PAGE DISTANCE CHECK
→ CROSS-PAGE SILHOUETTE CHECK
→ REROLL / MUTATE IF TOO SIMILAR
```

Do not create internal pages by copying Home and replacing copy/assets.
Do not create several internal pages through one shared visible skeleton merely because their semantic section names differ.

### 53.4. Cross-page hard exclusion inside one site

For Home + key internal pages:
- the exact opening/hero macro family must not repeat by default;
- the same opening topology cluster should not repeat while other valid clusters exist;
- identical 2-section and 3-section macro sequences across key pages = `0` by default;
- the same dominant content topology must not control all key pages;
- identical closing CTA geometry on all key pages = reject when alternatives exist;
- the same `hero → equal cards → split → FAQ → CTA` skeleton on multiple pages = `FAIL`;
- mirroring image left/right does not clear a cross-page similarity failure.

### 53.5. Page-level diversity targets

For a key page with `4+` meaningful sections:

```text
unique_topology_cluster_ratio >= 0.75 normally
exact_section_fingerprint_repeat = 0
adjacent_structural_distance_failures = 0
```

For a rich key page with `6+` meaningful sections:

```text
unique_topology_cluster_ratio >= 0.80 normally
```

For Home with `7+`, the stricter Hard Diversity target remains in force.

These are quality targets after semantic filtering. If content genuinely supports only a narrower family, record the constraint rather than forcing nonsense.

### 53.6. Internal page opening diversity

Every important internal page receives an intentional opening selected from its own eligible opening pool.
Examples include:
- compact editorial cover;
- side-index opening;
- media-led opening;
- annotated object opening;
- chapter-led opening;
- panoramic band;
- quiet text-led introduction;
- split only when randomly selected from a valid distant pool;
- directory/index opening;
- fact-led ledger opening.

Do not make every internal page a reduced Home hero.

### 53.7. Legal and utility pages

Legal correctness/readability outrank novelty, but legal pages still must not be three cloned article shells.
Randomly select among **legal-safe** grammars such as:
- article + sticky TOC;
- article + side index;
- narrow editorial article + top chapter rail;
- two-zone article with contextual notes;
- chapter bands with compact legal navigation;
- intro ledger + long-form article;
- quiet full-width reading column with margin metadata.

Privacy, Terms and Cookies may share typography and legal navigation, but should not have identical full-page silhouettes by default when multiple safe grammars are available.

### 53.8. Contact / About / FAQ specialization

The engine must use role-appropriate pools instead of a generic internal-page template.

Examples:
- Contact: contact-led split, directory board, communication ledger, support stage, compact card/list hybrid, editorial contact index;
- About: narrative chapters, manifesto + proof, timeline, editorial spread, methodology ledger, media story;
- FAQ: side-index accordion, chapter FAQ, searchable question directory when justified, split FAQ, grouped questions, progressive disclosure;
- Guide: annotated media, chapter rail, process timeline, comparison board, sticky story, editorial ledger.

Selection inside the valid role pool remains random-first.

### 53.9. Cross-page silhouette distance

Before BUILD lock and again in Visual QA, compare neutral silhouettes among:
- Home;
- About;
- Contact;
- at least two key domain pages;
- FAQ/resources when present;
- representative legal pages.

If two unrelated-purpose pages remain recognizably the same template after colors/type/images are neutralized, reroll or mutate one of them.

Default internal threshold for key-page pairs:

```text
page_silhouette_distance >= 0.62
```

Legal/utility pairs may use a lower threshold when readability constraints reduce the pool, but exact page-shell duplication remains a failure unless explicitly justified.

### 53.10. Mobile page diversity

Cross-page diversity must survive mobile transformation.
Do not allow every page to become the same:

```text
small intro
→ stacked cards
→ text
→ accordion
→ CTA
```

Each page records its mobile rhythm and transformation family. Different desktop grammars should preserve meaningful differences on mobile while remaining readable and overflow-free.

### 53.11. Expanded Hard Diversity report

`HARD_DIVERSITY_REPORT` now also records:

```text
page_composition_nonces{}
page_rhythm_families{}
page_topology_cluster_sets{}
page_unique_topology_ratios{}
page_pair_silhouette_distances{}
repeated_cross_page_sequence_count
repeated_cross_page_opening_count
per_page_reroll_counts{}
per_page_new_grammar_counts{}
mobile_page_rhythm_signatures{}
```

For a full site, missing per-page diversity data = `FIX_REQUIRED`.


## 54. HEADER COMPOSITION + NAVIGATION PRESENTATION ENGINE (v3.3.1)

The header is part of the composition system. A large section library is not sufficient if every site begins with the same logo/menu/CTA geometry.

### 54.1. Required site-level state

For each new site create:

```text
header_composition_nonce
navigation_copy_nonce
navigation_lexical_profile
menu_lexical_fingerprint
HEADER_COMPOSITION_MANIFEST
NAVIGATION_COPY_MANIFEST
```

The header topology is **global to the site** and normally remains stable across managed pages. Individual pages may use compatible states such as transparent-over-hero vs solid-on-scroll, but they do not randomly relocate the whole navigation on every page.

### 54.2. Permanent header family bank

These are structural grammars, not pixel templates:

```text
HDR01_BRAND_LEFT_NAV_CENTER_ACTION_RIGHT
HDR02_BRAND_LEFT_NAV_RIGHT_COMPACT_ACTION
HDR03_ACTION_LEFT_NAV_CENTER_BRAND_RIGHT
HDR04_CENTER_BRAND_SPLIT_NAV_LEFT_RIGHT
HDR05_CENTER_BRAND_NAV_BAND_BELOW
HDR06_BRAND_TOP_LEFT_NAV_SECOND_ROW
HDR07_BRAND_TOP_CENTER_NAV_SECOND_ROW
HDR08_UTILITY_TOP_MAIN_NAV_BELOW
HDR09_NAV_TOP_BRAND_ACTION_SECOND_ROW
HDR10_ASYMMETRIC_BRAND_BLOCK_NAV_RAIL
HDR11_INSET_ISLAND_HEADER
HDR12_FULL_BLEED_BAR_INNER_NAV
HDR13_OFFSET_CONTAINER_HEADER
HDR14_BRAND_PANEL_LEFT_NAV_FIELD_RIGHT
HDR15_NAV_LEDGER_WITH_BRAND_ANCHOR
HDR16_COMPACT_WORDMARK_NAV_NO_PRIMARY_CTA
HDR17_CTA_LED_HEADER_NAV_LEFT
HDR18_NAV_LEFT_BRAND_CENTER_ACTION_RIGHT
HDR19_BRAND_LEFT_NAV_WITH_RULE_DIVIDERS
HDR20_BRAND_LEFT_NAV_PILLS_ACTION_END
HDR21_MINIMAL_BRAND_KEY_LINKS_PLUS_MENU_TRIGGER
HDR22_FLOATING_CAPSULE_OVER_HERO
HDR23_TRANSPARENT_HERO_HEADER_TO_SOLID_STATE
HDR24_SPLIT_POLARITY_BRAND_NAV_HEADER
HDR25_SIDE_INDEX_ACCENT_WITH_MAIN_NAV
HDR26_BRAND_META_TOP_NAV_SECOND_LINE
HDR27_LARGE_WORDMARK_ROW_COMPACT_NAV_ROW
HDR28_EDITORIAL_MASTHEAD_WITH_NAV_BAND
HDR29_UTILITY_ACTION_RAIL_PLUS_PRIMARY_NAV
HDR30_CENTER_NAV_BRAND_LEFT_NO_ACTION
HDR31_NAV_LEFT_ACTION_CENTER_BRAND_RIGHT
HDR32_DUAL_GROUP_NAV_WITH_CENTER_BRAND
```

A family is eligible only when the actual number of links, brand length, CTA requirement, locale label lengths, viewport range and accessibility model fit it.

### 54.3. Header topology clusters

Group families before random draw so superficial variants do not dominate probability:

```text
HC01_SINGLE_ROW_BALANCED
HC02_SINGLE_ROW_ASYMMETRIC
HC03_CENTER_BRAND_SPLIT_NAV
HC04_TWO_ROW_MASTHEAD
HC05_UTILITY_PLUS_PRIMARY
HC06_INSET_FLOATING_ISLAND
HC07_OVERLAY_HERO_HEADER
HC08_EDITORIAL_MASTHEAD_BAND
HC09_BRAND_PANEL_PLUS_NAV_FIELD
HC10_MINIMAL_TRIGGER_HYBRID
HC11_DUAL_GROUP_NAV
HC12_POLARITY_SPLIT_HEADER
```

Selection uses approximately equal eligible-cluster probability, then a random family inside the selected cluster.

### 54.4. Structural signature

Record at minimum:

```text
header_family
header_cluster
shell_mode
row_count
brand_zone_position
primary_nav_zone_position
nav_grouping_mode
primary_action_position
utility_zone_position
text_alignment_mode
surface_mode
hero_overlay_state
mobile_header_family
mobile_menu_opening_mode
```

Changing only color, border radius, icon or gap does not count as a new header family.

### 54.5. Random selection pipeline

```text
ACTUAL NAV DESTINATIONS
→ ACTUAL SELECTED NAV LABEL LENGTHS
→ SEMANTIC / ACCESSIBILITY FILTER
→ WIDTH / RESPONSIVE FIT FILTER
→ ELIGIBLE HEADER CLUSTERS
→ RANDOM CLUSTER DRAW USING header_composition_nonce
→ RANDOM FAMILY DRAW
→ MOBILE TRANSFORMATION DRAW
→ WHOLE-HEADER FIT CHECK
→ REROLL IF CLIPPED / CROWDED / TOO SIMILAR
→ PERSIST
```

Do not use semantic score as a hidden top-1 selector after the candidate pool is healthy. Scores establish eligibility; random draw chooses among valid structures.

### 54.6. Mobile header transformation bank

```text
MHD01_BRAND_LEFT_MENU_RIGHT
MHD02_MENU_LEFT_BRAND_CENTER
MHD03_BRAND_LEFT_COMPACT_ACTION_MENU
MHD04_TWO_ROW_BRAND_THEN_CONTROLS
MHD05_UTILITY_STRIP_PLUS_MAIN_ROW
MHD06_FLOATING_COMPACT_ISLAND
MHD07_CENTER_BRAND_ACTIONS_EDGES
MHD08_BRAND_TOP_NAV_DRAWER_TRIGGER_BELOW
MHD09_COMPACT_WORDMARK_MENU_WITH_INLINE_CTA
MHD10_DUAL_ACTION_ROW_TO_DRAWER
MHD11_OVERLAY_TO_SOLID_COMPACT_ROW
MHD12_EDITORIAL_MASTHEAD_TO_COMPACT_TRIGGER
```

Mobile variation must preserve:
- visible menu trigger;
- keyboard/focus usability;
- minimum touch target quality;
- coherent DOM/source order;
- no horizontal page overflow;
- no offscreen CTA/brand;
- safe long-label wrapping inside the opened menu.

### 54.7. Label-fit feedback loop

Header layout and navigation copy are independent random dimensions but must be validated together.

If a natural selected label makes a header family invalid:
1. try another compatible label from the **same semantic role**;
2. if the label pool should remain intact, try another header family/cluster;
3. use a compact semantic label variant only when explicitly recorded;
4. never silently replace all labels with generic defaults simply to save the chosen header.

### 54.8. Anti-template and persistence

For a new site, fresh nonce-based selection is sufficient even when no prior-site history exists.
When recent header fingerprints are available, they may additionally penalize/reject near-identical unrelated-site headers, but cross-site memory is optional enhancement, not a dependency.

Same-site update behavior:

```text
existing HEADER_COMPOSITION_MANIFEST → preserve
existing navigation Global Text values → preserve
existing nonces → preserve
```

Only explicit `REGENERATE_HEADER` / `REGENERATE_NAVIGATION_COPY` may intentionally reseed these dimensions.

### 54.9. Required manifest

```text
HEADER_COMPOSITION_MANIFEST
header_composition_nonce
eligible_header_clusters[]
eligible_header_families[]
selected_header_cluster
selected_header_family
header_signature
mobile_header_family
reroll_count
fit_rejection_reasons[]
```

The corresponding `NAVIGATION_COPY_MANIFEST` is owned by the Content/Architecture layers and consumed here for real label lengths.


### 54.10. Lexical diversity is a header-fit input, not a reason to canonicalize copy

The header engine consumes the actual selected locale-natural labels. If a varied label set does not fit one header family, prefer this repair order:

```text
1. try compact synonym for only the affected role
2. choose another eligible header family
3. choose another mobile header transformation
4. reduce nonessential utility/CTA occupancy
5. reroll the affected label from the same semantic pool
```

Do **not** normalize every site back to the shortest canonical labels merely to make one comfortable header template fit.

When a same-locale batch provides multiple `menu_lexical_fingerprint` values, header composition may vary independently; lexical diversity does not require visually loud header treatment.



### 54.11. Universal locale lexicon handoff (v3.3.2)

Header composition must consume `NAVIGATION_LOCALE_LEXICON` for the site's resolved locale. No header family may assume English or PT label lengths.

Eligibility must use actual candidate measurements/scripts, including:
- long Germanic compounds;
- Romance multi-word labels;
- non-Latin scripts;
- locale-specific capitalization/word spacing;
- diacritics and glyph widths;
- right-to-left direction when the selected locale requires it and the broader factory supports that locale.

When a new locale's labels are longer than the current header candidate can support, change label/family through the normal fit loop rather than reverting to English or one global canonical word set.

`header_composition_nonce` and `navigation_copy_nonce` remain independent; locale fit constrains eligibility but does not remove random selection from healthy pools.

<!-- BUNDLE-MODULE-END: 18-SECTION-COMPOSITION-ENGINE.md -->

---


## 55. FOOTER CONTENT-DENSITY / UTILITY-FIRST HANDOFF (v3.3.3)

Footer composition diversity does not require footer copy density. The footer engine must be able to produce a complete, premium footer with **zero descriptive paragraph**.

Composition should create richness through:
- grouping and hierarchy;
- brand placement;
- nav matrix / rails / bands;
- contact/support placement;
- official store CTA placement;
- legal grouping;
- dividers, surfaces and bottom-bar geometry.

Do not add prose simply to balance a column. If the optional descriptor is absent, collapse/rebalance the corresponding zone instead of leaving an empty text slot.

For `OFFICIAL_GAME_STUDIO`, any descriptor candidate containing independent-guide/review/editorial positioning is ineligible. A concise truthful creator/product phrase may be used only when useful and claim-safe.



## 56. HERO COMPOSITION DIVERSITY + TITLE-SCALE CONTROL (v3.4.0)

Hero diversity is evaluated independently from general section diversity because the first viewport has disproportionate perceptual weight.

### 56.1. Hero topology clusters

Group hero candidates before random selection so left-split variants do not dominate by count:

```text
HV01_CENTERED_STAGE
HV02_LEFT_TEXT_RIGHT_MEDIA_SPLIT
HV03_RIGHT_TEXT_LEFT_MEDIA_SPLIT
HV04_MEDIA_FIRST_FULL_BLEED_OVERLAY
HV05_TOP_CENTER_MEDIA_BELOW
HV06_MEDIA_ABOVE_TEXT_BELOW
HV07_INSET_TEXT_PANEL_ON_MEDIA
HV08_ASYMMETRIC_OFFSET_STAGE
HV09_SIDE_RAIL_WITH_MAIN_STAGE
HV10_STACKED_EDITORIAL_LEDGER
HV11_BOTTOM_ANCHORED_TEXT_ON_MEDIA
HV12_DUAL_FIELD_TEXT_MEDIA_BAND
```

Selection pipeline:

```text
PAGE INTENT
→ HERO ROLE-SAFE CANDIDATES
→ GROUP BY HERO TOPOLOGY CLUSTER
→ RANDOM ELIGIBLE CLUSTER
→ RANDOM FAMILY INSIDE CLUSTER
→ COPY/MEDIA FIT
→ FIRST-VIEWPORT BALANCE
→ CROSS-PAGE/CROSS-SITE SILHOUETTE CHECK
→ REROLL / MUTATE
```

Do not score every candidate globally and repeatedly choose one comfortable left-split family.

### 56.2. Independent positioning dimensions

Record and vary:

```text
hero_text_anchor
hero_text_alignment
hero_eyebrow_anchor
hero_lead_alignment
hero_cta_alignment
hero_media_anchor
hero_media_dominance
hero_shell_mode
hero_vertical_alignment
hero_title_scale_tier
```

A centered H1 does not require every supporting paragraph/button to be centered; compositions may use controlled mixed alignment when the reading order remains obvious.

### 56.3. Intra-site hero diversity

For Home + key internal pages, when valid pools allow:
- at least `3` distinct hero topology clusters across the representative set;
- exact `hero_signature` repeat = `0` for unrelated page roles;
- all compared pages text-left = `FAIL` unless a documented brand system requires it;
- a shared helper may coordinate semantics, but it must dispatch to materially different hero-family renderers rather than output one DOM/layout skeleton everywhere.

### 56.4. Title scale tiers

Use explicit tiers instead of one aggressive fluid scale:

```text
COMPACT
STANDARD
DISPLAY
MANIFESTO_EXCEPTION
```

Default selection:
- most Home heroes → `STANDARD` or `DISPLAY`;
- most internal heroes → `COMPACT` or `STANDARD`;
- `MANIFESTO_EXCEPTION` requires enough supporting composition/media and a screenshot reason.

At representative desktop width, a normal hero should usually keep the H1 to roughly `2–4` visual lines. `5+` heavy lines combined with large scale is a reroll/resize signal, not an achievement.

The H1 should not visually occupy the majority of the first viewport. If it does, reduce scale/measure or change family before reducing useful content.

### 56.5. First-viewport balance fingerprint

Record:

```text
h1_line_count
h1_visual_height_ratio
text_block_width_ratio
media_visible_in_first_viewport
primary_cta_visible_in_first_viewport
hero_text_anchor
hero_media_topology
```

Use screenshot perception as final authority; numeric envelopes do not excuse a poster-like result.


## 57. FOOTER CONTACT + BOTTOM-BAR MICROCOPY COMPOSITION HANDOFF (v3.4.1)

When Contact Profile contains email, phone and postal address, footer family eligibility must provide enough space to render all three without creating a dense paragraph.

Possible treatments include:
- compact stacked contact rail;
- two-line contact ledger;
- split email/phone + address row;
- dedicated contact column;
- contact band above the bottom bar.

Do not hide resolved contact data merely to preserve a chosen footer geometry; choose another footer family or rebalance the grid.

Bottom-bar composition may include:

```text
copyright / rights
+
optional footer.utility_phrase
```

The microcopy may be left/right, centered as a second item, or integrated into a compact multi-item bar.

Do not place a naked arrow/icon at the far edge as decorative filler. An icon-only action is eligible only when it is a genuine accessible control with a clear accessible name and useful interaction.


## 58. PERSISTENT LAYOUT DNA BANK + CROSS-SITE MEMORY HANDOFF (v3.5.0)

The Section Composition Engine consumes the external persistent Layout DNA Bank and structural history when available.

Canonical repository state for this factory:

```text
PingVinni/Landing
site-factory-layout-bank/index.json
site-factory-layout-bank/axes.json
site-factory-layout-bank/compatibility-and-diversity-rules.json
site-factory-layout-bank/archetypes/*.json
site-factory-history/index.json
site-factory-history/sites/{normalized-domain}.json
```

### 58.1. Bank usage before selection

For every unrelated new site:

```text
LOAD LAYOUT BANK
→ LOAD HISTORY INDEX
→ CHOOSE RECENT / SAME-NICHE / NEAREST STRUCTURAL COMPARISON SET
→ LOAD THEIR PER-SITE JSON FILES
→ BUILD RECENCY + FREQUENCY EXCLUSION MAP
→ FILTER SEMANTICALLY VALID ARCHETYPES
→ EXCLUDE TOO-RECENT / TOO-SIMILAR STRUCTURES
→ RANDOM DRAW FROM DISTANT UNDERUSED TOPOLOGY CLUSTERS
→ COMPOSE THROUGH INDEPENDENT AXES
→ NEUTRAL SILHOUETTE CHECK
→ REROLL / MUTATE / SYNTHESIZE
```

The external bank extends the permanent in-bundle family library; it does not waive accessibility, semantic fit, content truth, responsive behavior or the existing Hard Diversity thresholds.

### 58.2. Persistent section-level fingerprint output

After final composition lock, emit a compact structural record for every meaningful section of Home and key internal pages:

```text
page_key
section_key
semantic_role
archetype_id
topology_cluster
grid_topology
shell_mode
content_anchor
text_alignment
copy_flow
text_measure
media_topology
media_dominance
card_or_list_geometry
surface_mode
edge_overlap_mode
density_mode
transition_family
cta_position
annotation_family
interaction_family
motion_family
mobile_transform
section_fingerprint
```

This is the data source for the canonical per-site repository JSON.

### 58.3. Page and site memory output

Record per key page:

```text
opening_archetype
page_rhythm_recipe
section_archetype_sequence
topology_sequence
content_anchor_sequence
media_topology_sequence
surface_sequence
interaction_sequence
mobile_transform_sequence
bigram_signature
trigram_signature
neutral_silhouette_hash
page_composition_fingerprint
```

Record at site level:

```text
hero signature
header signature
footer signature
Home silhouette
key-page silhouettes
interaction profile
mobile profile
site structural fingerprint
nearest prior structural matches
comparison distances
reroll count
new grammar count
```

### 58.4. History-aware uniqueness is not cosmetic

When history exists, the selector must compare normalized structural dimensions. These changes alone do not clear a repeat:
- left/right mirror;
- color/palette change;
- new font;
- new image;
- radius/gap change;
- renamed component classes.

The bank should prefer underused **topology + anchor + media relationship + rhythm** combinations, not merely underused IDs.

### 58.5. Same-domain update rule

A same-site maintenance update normally preserves its established composition DNA. If an explicit redesign materially changes the structure:
- recompute page/site fingerprints;
- update the same canonical per-domain JSON;
- append a compact structural revision entry;
- never create a second history identity for the same normalized domain merely because the theme version changed.



## 59. STUDIO DEVELOPMENT SEMANTIC ROLE HANDOFF (v3.6.0)

The composition engine must recognize first-party studio/development content as distinct semantic jobs rather than forcing them into generic `feature`, `cards`, or `guide` sections.

Additional semantic roles:

```text
STUDIO_IDENTITY
PRODUCT_PROPOSITION
DEVELOPMENT_OVERVIEW
DESIGN_CHALLENGE
IMPLEMENTATION_PRINCIPLE
MECHANICS_DESIGN
LEVEL_PROGRESSION_DESIGN
CONTROLS_FEEL
ART_DIRECTION
BALANCING_TESTING
TEAM_APPROACH
ITERATION_RELEASE
PLAYER_OUTCOME
PRODUCT_PROOF
PLAY_DOWNLOAD_CONVERSION
SUPPORT_RELATIONSHIP
```

These roles may map to any semantically valid Layout DNA archetype. Do not hardcode `process = numbered cards` or `team = portrait grid`.

### Content-shape diversity

Studio/development storytelling should rotate among structures such as:
- challenge → response → outcome;
- annotated system diagram;
- sticky development chapters;
- prototype/state comparison when factual assets exist;
- process runway/timeline only when chronology is supported;
- design-principle ledger;
- media + technical explanation;
- level/progression map;
- mechanic relationship matrix;
- team-principles spread without invented staff cards;
- product proof stage;
- contextual play/download close.

### Historical-truth filter

A timeline or `before/after` pattern is eligible only when the copy/assets contain a factual sequence. If only a high-level product explanation is available, choose a non-chronological design/process composition.

### Anti-template rule

A rich official-studio site should not render every development topic as:

```text
H2 + paragraph + 3 cards + image
```

The studio story must participate in the same cross-site Layout DNA memory and hard-distance gates as all other major sections.


## 60. ICONOGRAPHY + MICRO-UI COMPOSITION SYSTEM (v3.7.0)

Micro visuals are part of Design DNA, not an afterthought.

### 60.1. Site-level icon language

Before components are implemented, define one coherent icon language:

```text
icon_style_family
stroke_weight_or_fill_mode
optical_grid
corner_character
terminal_shape
negative_space_character
primary_icon_size
secondary_icon_size
micro_icon_size
icon_surface_mode
icon_accent_mode
```

Do not mix unrelated outline, filled, 3D, emoji and stock-icon languages on one site.

### 60.2. Size and placement tiers

Use semantic tiers rather than arbitrary sizes:
- `MICRO` — inline status/list/support markers;
- `COMPACT` — card/feature/process icon;
- `FEATURE` — iconographic explainer focal point;
- `DIAGRAM` — multi-node system/process visual.

Exact dimensions are Design-DNA driven and remain fluid/rem-based. Icons must never become mini-heroes that overpower copy.

### 60.3. Where micro visuals may improve composition

Eligible uses include:
- feature rows;
- mechanic/property groups;
- development stages;
- process sequences;
- support/contact methods;
- fact ledgers;
- section indexes;
- CTA qualifiers;
- timeline/progression nodes;
- small comparison cues;
- compact badges only when they communicate a real state/category.

### 60.4. Small decorative systems

Allowed supporting elements:
- short rule segments;
- branded dots/nodes;
- corner ticks;
- coordinate/index marks;
- subtle line connectors;
- sectional counters;
- small geometric anchors derived from brand/visual DNA.

They must support rhythm/hierarchy. Random stars, sparks, floating shapes or excessive pseudo-tech HUD decoration are not a substitute for composition.

### 60.5. Semantic icon rule

One symbol = one meaning within a site. If a glyph represents `testing`, it must not later represent `download` or `difficulty`.

When an icon accompanies text:
- the visible text remains understandable without the icon;
- decorative icons are hidden from assistive tech where appropriate;
- interactive icon-only controls require an accessible localized name and adequate target size;
- icons must survive light/dark/surface variants.

### 60.6. Card and process enrichment

Do not solve visual richness by wrapping every item in a card. Micro-visuals may enrich open editorial layouts, ledgers, timelines, side rails and process diagrams without creating repetitive card grids.

If several peer items require icons, prefer a coherent site-specific set rather than reusing one generic symbol for all items.

### 60.7. Mobile transformation

On small screens:
- simplify nonessential ornament;
- preserve semantic icons;
- keep labels readable;
- collapse complex connectors into a clear linear relationship;
- never let micro-decor cause horizontal overflow or tiny tap targets.

### 60.8. Micro-UI diversity handoff

The Section Composition Engine may vary how the micro-system appears by section — rail, ledger, stage, inline markers, diagram, index — while preserving one coherent icon language. Visual diversity comes from composition, not from changing icon style randomly.




## 61. STUDIO-BUSINESS PAGE COMPOSITION PRIORITY (v3.8.0)

For `OFFICIAL_GAME_STUDIO`, section composition must make the business model visible before the visitor reaches product-detail content.

### 61.1 Narrative zones

Each key non-legal page resolves three semantic zones:

```text
ZONE_A_OPENING
ZONE_B_WORKING_MIDDLE
ZONE_C_PRODUCT_OUTCOME
```

Default meaning:

```text
ZONE_A_OPENING
= studio/team/task/challenge

ZONE_B_WORKING_MIDDLE
= collaboration/process/design decision/prototype/review/QA

ZONE_C_PRODUCT_OUTCOME
= feature/mechanic/level/player result/store/support
```

Layout randomization remains active inside each zone. Do not turn this into one fixed page template.

### 61.2 Opening layout families

Create/choose from structurally diverse studio/business openings such as:
- team/work scene with offset editorial copy;
- worktable / review-room stage;
- task-led editorial spread;
- process rail + large working-scene media;
- studio manifesto with documentary-style visual field;
- design-review canvas;
- production board / decision ledger;
- collaboration scene with narrow side narrative;
- full-bleed work scene with inset business statement;
- two-stage opening: company statement → active task.

Avoid reducing all business pages to `people photo left + copy right`.

### 61.3 Working-middle families

The middle of each key page should normally include one or more:
- task ledger;
- decision matrix;
- process chapters;
- review checklist;
- iteration comparison;
- QA/testing board;
- cross-discipline handoff;
- art/UX review spread;
- level design workbench;
- release readiness board;
- challenge → decision → outcome story.

Cards are optional, not the default.

### 61.4 Business copy prominence

Do not let a large hero image visually erase the studio narrative.

Hero copy should normally contain:
- studio/company context;
- page-specific team responsibility;
- a work/process proposition;
- one clear continuation.

Generic slogans without business meaning are weak candidates.

### 61.5 Text-dense premium layouts

Because the current compact-copy policy carries roughly `30%` less visible prose than the v4.9.12 high-density profile, layouts must use the released space for stronger media, wider composition and cleaner grouping rather than blank canvas:
- 55–75 character body measures where practical;
- multi-paragraph editorial blocks;
- chapter navigation;
- ledgers/side notes;
- pull facts only when factual;
- process annotations;
- visual breaks without fragmenting every paragraph into cards.

Avoid giant empty fields that make the richer text look sparse.

### 61.6 Cross-page diversity

Although the company/team/process story is present on every key page, each page must express a different work discipline.

Examples:
- Game/Product → product definition / feature prioritization;
- Development → production workflow / iteration;
- Mechanics → systems design / tuning;
- Levels → level-design workflow / progression review;
- Art → visual-language review;
- About → studio principles / collaboration;
- FAQ → how the team works + product questions;
- Contact → support ownership / communication workflow.

Repeating the same team-photo + three-process-cards composition across pages = `FAIL`.



## 62. SECTION FAMILY DIVERSITY + HARMONY ENGINE (v3.9.0)

The composition engine must select from a broad family library, not one reusable split/card template.

### 62.1 Required section-family library

Maintain at least these structurally distinct families:

```text
EDITORIAL_FULL_WIDTH_ESSAY
EDITORIAL_TWO_COLUMN_TEXT
EDITORIAL_CENTERED_MANIFESTO
EDITORIAL_ASYMMETRIC_ESSAY
EDITORIAL_STAGGERED_NARRATIVE
MEDIA_LEFT_TEXT_RIGHT
MEDIA_RIGHT_TEXT_LEFT
MEDIA_TOP_TEXT_BELOW
TEXT_OVER_MEDIA_PANEL
MEDIA_STRIP_WITH_NARRATIVE
COLLAGE_WITH_EDITORIAL_COPY
OVERLAP_MEDIA_COPY
INSET_MEDIA_IN_ESSAY
SPLIT_GALLERY_COMPACT_COPY
FLOATING_MEDIA_WITH_CAPTION
PROCESS_TIMELINE
PROCESS_CHAPTER_RUNWAY
WORKFLOW_BOARD
TEAM_ROLE_LEDGER
MILESTONE_RAIL
CASE_STUDY
PROBLEM_SOLUTION
DECISION_MATRIX
QA_TESTING_BOARD
PRODUCTION_PHASES
CONCEPT_TO_RELEASE
ANNOTATED_WORKBENCH
METRIC_BAND
FACT_LEDGER
CHAPTER_INDEX
FULL_WIDTH_CTA
MEDIA_LED_CTA
```

The library may grow beyond these.

### 62.2 Selection rule

For each page:

```text
semantic_role
→ eligible layout families
→ exclude same-page used exact families
→ exclude recent consecutive topology
→ compare cross-page frequency
→ choose distant valid family
→ verify content/media fit
→ verify no dead space
→ lock section
```

### 62.3 Same-page rhythm

A rich page should usually alternate composition rhythm.

Examples:

```text
media-led
→ editorial
→ structured process
→ photo narrative
→ full-width text
→ matrix
→ product media
```

Avoid:

```text
split
→ split
→ cards
→ split
→ cards
```

even when each section has different wording.

### 62.4 Harmony rules

Harmony is evaluated through:
- visual weight;
- column occupancy;
- text measure;
- media scale;
- vertical density;
- transition into next section;
- alignment continuity;
- whitespace purpose.

A section is not harmonious merely because its grid is mathematically valid.

### 62.5 Missing-media adaptive reflow

Each media-capable section must declare:

```text
media_required
media_optional
no_media_fallback_family
```

If `media_required = true` and no valid asset exists:
`FIX_REQUIRED`.

If `media_optional = true` and no asset exists:
renderer must switch to `no_media_fallback_family`.

The fallback may not preserve a blank media track.

### 62.6 Long-copy composition

For long-form sections:
- use more of the container width;
- permit multiple paragraph columns only when reading order is clear;
- use internal subheads/notes/figures to prevent wall-of-text fatigue;
- add real visual anchors where semantically justified;
- never squeeze long copy into a narrow half-column just to preserve a template.

### 62.7 Image-wrap composition

Desktop families may allow editorial wrap where:
- media occupies approximately one-third to one-half of the local text field;
- paragraph flow remains readable;
- image caption/alt remains semantic;
- mobile collapses to media-before or media-between text;
- no awkward orphaned lines or micro-columns occur.

### 62.8 Per-page uniqueness target

For a normal rich internal page with 7–11 sections:
- target at least `5` materially distinct section families;
- no exact family repeated;
- no more than `2` sections from the same broad topology cluster;
- at least `1` section should differ strongly from neighboring sections in both media relationship and text flow.

For Home with 10–15 sections:
- target at least `7` materially distinct families;
- at least `4` broad topology clusters.

These are quality targets with blocking fallback when the page visibly clones itself.

### 62.9 Cross-page page grammar

Each key page receives a distinct page grammar fingerprint.

Do not let:
- Product,
- Development,
- Mechanics,
- Levels,
- Studio

all use the same sequence of:

```text
hero split
→ statement
→ cards
→ workflow
→ matrix
→ product
→ CTA
```

even when the semantic labels differ.

A page grammar is a composition artifact, not a content label.
---

## 63. FULL-WIDTH CANVAS UTILIZATION ENGINE (v3.10.0)

The design system must distinguish **readable text measure** from **section canvas usage**. A paragraph can remain `60–75ch` while the overall section still occupies the useful desktop width.

### 63.1 Section shell rule

Major sections use the full available shell by default:

```text
outer_section_inline_size = 100%
inner_shell = full useful container width
unassigned desktop grid tracks = 0
```

Do not apply a small shared `max-inline-size` to an entire major section merely because the body copy itself needs a readable measure.

### 63.2 Canvas-coverage diagnostics

For ordinary major non-hero desktop sections record:

```text
available_canvas_width
meaningful_content_span
major_section_canvas_coverage
largest_unassigned_blank_region_ratio
empty_track_count
```

Default review targets:

```text
major_section_canvas_coverage >= 0.78
largest_unassigned_blank_region_ratio <= 0.22
empty_track_count = 0
```

Exceptions are allowed only for explicitly selected families such as a centered statement or intentionally quiet text-led composition, and they still must not create a one-sided unfinished field.

### 63.3 No-media collapse

A split family is invalid after its second side becomes empty. The renderer must switch family or collapse the track:

```css
.section-grid {
  inline-size: 100%;
}

.section-grid[data-media="none"] {
  grid-template-columns: minmax(0, 1fr);
}
```

The exact selectors vary by project. The invariant is mandatory and production CSS still follows the no-numeric-`px` rule.

### 63.4 Text-only full-width treatments

When no semantic media is justified, prefer one of:
- wide editorial spread with readable nested measures;
- two-column editorial body;
- centered reading measure inside a full-width statement field;
- chapter/ledger composition;
- definition or decision matrix;
- staggered subtopic columns;
- full-width text with semantic side notes.

Do not leave a dead media half just to preserve visual symmetry.

### 63.5 Copy compaction coupling

After the ~30% copy reduction:
- reduce section height when appropriate;
- do not inflate H2 size to refill space;
- do not increase padding to preserve former height;
- re-evaluate media size and placement;
- re-run canvas-coverage diagnostics.

Shorter copy should produce a tighter, wider, cleaner composition—not a smaller island inside the same large frame.


---

## 64. RENDERED COMPOSITION PROOF + TEXT BREATHING (v3.11.0)

This section supersedes any interpretation that manifest-level diversity or nominal full-width shells are sufficient.

### 64.1 Effective occupied canvas

At browser runtime record for each major section:

```text
section_viewport_width
meaningful_union_bbox_width
meaningful_union_bbox_height
occupied_width_ratio
largest_blank_side_ratio
heading_visual_line_count
heading_body_gap_ratio
```

Default desktop acceptance for ordinary sections:

```text
occupied_width_ratio >= 0.74
largest_blank_side_ratio <= 0.26
heading_visual_line_count <= 3
```

A section may intentionally use quiet space only when the chosen family declares that space as part of the composition and the screenshot reads as finished rather than missing content.

### 64.2 Text breathing

For normal editorial sections:
- multi-line H2 line-height should normally read around `1.0–1.12`, not poster-tight stacking;
- paragraph measure remains readable, but body copy must not be squeezed into a tiny island;
- heading → lead/body separation must be visually obvious;
- paragraph groups need consistent vertical rhythm;
- when heading and body sit on different grid axes, align them deliberately rather than leaving the body stranded halfway across the canvas.

If the heading visually becomes a vertical stack of isolated words, first increase measure / reduce size / change family before accepting it.

### 64.3 Render-family diversity gate

Every major section records both planned family and **rendered family**.

Rendered-family signature includes:
- number and proportion of columns/tracks;
- text anchor and vertical anchor;
- media position/dominance;
- card/list topology;
- surface boundary shape;
- overlap/layering;
- primary visual mass position;
- mobile transformation.

Rules for a rich page:
- distinct rendered-family ratio `>= 0.80` where `6+` major sections exist;
- no adjacent near-duplicate rendered family;
- one generic renderer may not masquerade as many families through class renaming;
- a repeated card grid may appear only when semantically necessary and must not dominate the page rhythm;
- Home and each key internal page need materially different first three major-section silhouettes.

### 64.4 Browser evidence

Diversity and whitespace decisions are finalized from screenshots, not from layout IDs. If screenshots contradict the manifest, the manifest is wrong and must be repaired.
