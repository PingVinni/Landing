# 04 CONTENT LEGAL CONTACT

**Bundle format:** Source Bundle v1.5  
**Policy baseline:** Site Factory v4.9.14  
**Bundling rule:** logical module boundaries and aliases are preserved inside bundles. Source Bundle v1.5 applies the Site Factory v4.9.14 interaction, micro-motion, hover/focus and semantic interactive-section expansion while preserving v1.4 rich-content, live UI/UX research, morphological section variation, v1.3 adult-premium visuals and the 7-file Project Source architecture.

## Module aliases in this bundle

- `07-CONTENT-ENGINE.md` → this file, section `LEGACY MODULE: 07-CONTENT-ENGINE.md`
- `08-LEGAL-GEO-ENGINE.md` → this file, section `LEGACY MODULE: 08-LEGAL-GEO-ENGINE.md`
- `13-CONTACT-GEO-ENGINE.md` → this file, section `LEGACY MODULE: 13-CONTACT-GEO-ENGINE.md`

## Cross-reference rule

References inside logical module text to filenames such as `15-SECTION-IMAGE-ENGINE.md` remain valid **logical module IDs**. Resolve them against the module aliases declared across the loaded Source Bundles. `SOURCE-BUNDLE-MAP.md` is maintenance documentation only and is **not required** as a Project Source.

---

<!-- BUNDLE-MODULE-START: 07-CONTENT-ENGINE.md -->

# LEGACY MODULE: 07-CONTENT-ENGINE.md

# CONTENT ENGINE

**Version:** 4.5.0  
**Role:** rich thematic content, source-grounded expansion, SEO та information depth

---

## 1. Source-first

Контент про конкретний продукт/гру/сервіс базується на:
- наданому source URL;
- офіційних/public authoritative джерелах;
- фактах, які можна підтвердити.

Не вигадувати характеристики.

---

## 2. Content Bible

Перед copy створити:

- niche vocabulary;
- audience;
- GEO;
- locale;
- tone;
- preferred terminology;
- prohibited generic phrases;
- factual claims list;
- unknown facts;
- source attribution plan.

---

## 3. Natural localization

PT сайт — це не переклад англійського boilerplate.

Потрібні:
- природні формулювання;
- локальний spelling/variant;
- локалізовані labels;
- відповідний CTA tone;
- правильна пунктуація.

---

## 4. Full pages

### Depth target
Ключова content page зазвичай повинна мати:
- 4–7 meaningful sections;
- 700–1400 слів там, де формат справді потребує article depth;
- або еквівалентну інформаційну щільність через таблиці, catalog, steps, FAQ, examples;
- 1–3 meaningful visuals/media moments;
- contextual internal links.

Не роздувати текст заради лічильника слів: корисність важливіша за обсяг.



Domain page має бути корисною навіть без Home.

Типова informative page може включати:
- intro;
- explanation;
- examples;
- steps;
- comparison;
- caveats;
- related links;
- FAQ;
- source/reference CTA.

---

## 5. Catalog content

Якщо catalog доречний:

Кожен item має мати meaningful fields:
- title;
- category;
- short context;
- tags/attributes;
- related guide;
- optional filter data.

Не створювати “catalog” із трьох generic cards.

---

## 6. Cards

Картки використовуються для:
- discovery;
- comparison;
- categories;
- examples;
- highlights.

Картки не замінюють статтю.

Не використовувати один і той самий card component на всіх сторінках.

---

## 7. Interaction

Доречні:
- accordion;
- tabs;
- filters;
- category switcher;
- comparison controls;
- related-content switch;
- simple search/filter.

Interaction має давати користь.
Не додавати JS лише “щоб було інтерактивно”.

---

## 8. About

About content follows the active business model.

For `OFFICIAL_GAME_STUDIO` mode, About should present the studio/product relationship rather than independent-editorial language:
- studio mission / creative direction;
- what the team wanted to make;
- product philosophy;
- confirmed development approach;
- art/mechanics/testing principles where supported;
- real people/team only if owner-supplied or verified;
- game/store/support links;
- no invented founding story, staff size, office, credentials or production history.

For independent editorial mode, editorial approach/sourcing/independence may still be used.

---

## 9. Reviews / testimonials

Supported modes:

### Sourced reviews
- only when actually sourced/provided;
- preserve attribution accurately.

### Synthetic editorial reviews
When real reviews are unavailable, factory may generate `SYNTHETIC_EDITORIAL_REVIEW` cards:
- natural localized tone;
- short quote;
- non-verified name/initial presentation;
- visible section disclosure that examples are illustrative/editorial;
- no fake buyer status;
- no claim that quote came from a real customer;
- no fabricated aggregate rating, review count or usage statistics.

Do not use real-person photos/avatars for synthetic reviews.

---

## 10. Claims

Не вигадувати:
- awards;
- certifications;
- “best”;
- “#1”;
- exact user count;
- company address;
- legal registrations;
- security claims;
- performance numbers.

---

## 11. SEO

Кожна indexable page:
- distinct intent;
- distinct title;
- distinct meta description;
- contextually correct H1;
- internal links;
- canonical URL;
- meaningful body content.

Не робити keyword stuffing.

---

## 12. Homepage content density

Home:
- не повторює ті самі 2 речення в різних блоках;
- кожна section додає новий information layer;
- media і copy взаємопов’язані;
- final CTA логічно завершує story.

---

## 13. Content depth gate

FAIL якщо:
- required page = H1 + 1 paragraph;
- legal page = 3 marketing cards;
- однаковий generic copy повторюється;
- catalog не має реального domain structure;
- FAQ заповнений obvious filler;
- user benefit неясний.


---

## 14. Contact content integrity

Contact copy має чітко розрізняти:
- support продукту/гри;
- operator цього website;
- third-party destination.

Заборонено:
- приписувати сторонній support email власнику нашого сайту;
- вигадувати working mailbox;
- вигадувати номер телефону;
- вигадувати postal address для production.

Для staging можна використовувати demo contact pack, але він не повинен маскуватись як verified.

---

## 15. Trust / reviews by business model (v4.6 patch)

Every full site needs a meaningful trust/proof layer, but the evidence type follows the business model.

### `OFFICIAL_GAME_STUDIO`
Do **not** generate synthetic player/customer testimonials. Use, when available:
- sourced store/player reviews;
- sourced press quotes;
- verified store/release presence;
- transparent product/development evidence;
- feature/mechanic proof;
- update/support clarity.

If no real reviews exist, use a non-testimonial trust section rather than invented player quotes.

### Independent editorial mode
The existing disclosed `SYNTHETIC_EDITORIAL_REVIEW` mechanism may be used only when appropriate and clearly non-customer/non-verified.

## 16. Anti-thin-page rule

Page вважається недописаною, якщо це лише hero + 1 block.

Internal informative page повинна мати:
- intro/problem framing;
- structured main content;
- at least one supportive media block;
- summary/next-step/related-pages layer.

## 17. Contact copy realism

Contact page copy повинна виглядати як справжня editorial/support page:
- natural lead paragraph;
- what users can write about;
- expected reply window phrased naturally;
- email/phone/address in readable blocks;
- no test/demo wording.


---

## 18. Global Text content output (v4.3)

The Content Engine must output copy as a structured `GLOBAL TEXT CONTENT MAP`, not as scattered hardcoded PHP strings.

Every text unit receives a stable path.

Examples:

```text
site.brand
site.tagline
navigation.guide
pages.home.hero.eyebrow
pages.home.hero.title
pages.home.hero.body
pages.home.hero.cta_primary
pages.guide.sections.controls.heading
pages.guide.sections.controls.paragraphs
components.reviews.heading
components.reviews.items.0.quote
components.cookie.banner.body
footer.bottom_bar.copyright
errors.404.title
```

### Long-form content

Legal/editorial/article text should remain editable without embedding HTML in JSON.

Use structured arrays:

```text
heading
paragraphs[]
bullets[]
quote
cta_label
```

Markup remains in templates/components.

### Repeated entities

Centralize frequently repeated editable entities:

```text
entities.brand
entities.product_name
entities.country_name
entities.editorial_name
entities.support_email
```

Strings may reference safe placeholders such as:

```text
"Guia de {product_name} em português"
"© {year} {brand}"
```

Runtime interpolation must come from an explicit allowlisted context.

### Hardcoded-copy prohibition

Production templates/components/JS must not contain factory-authored visible prose/labels that should be editable.

Allowed hardcoded literals are technical-only:
- IDs;
- CSS classes;
- schema keys;
- machine state names;
- URLs/paths;
- developer diagnostics.

User-visible copy belongs in Global Text.



## 19. Rich Content Engine v2 (v4.4.0)

The default full-site output should read like a **complete editorial/information resource**, not a thin landing page with many decorative sections.

### 19.1. Page depth profiles

For rich gaming/editorial/app-guide sites, use these normal envelopes when the subject supports them:

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
visible words: ~525–950 plus meaningful question structure
questions: commonly ~12–20 when source/context supports them

CONTACT / SUPPORT
visible words: ~525–950
must combine company/team responsibility, support workflow, actual contact identity, preparation/privacy/source context

LEGAL
visible words: commonly ~775–1550 per article when applicable
must reflect actual GEO/runtime, never filler or invented processing facts
```

Equivalent structured density through tables, definitions, steps, comparisons, taxonomies, diagrams or catalogs can replace some prose.

### 19.2. Information Gain rule

Every meaningful section receives an `information_role`.
Allowed roles include:
- `CONFIRMED_FACTS`;
- `EDITORIAL_EXPLANATION`;
- `PRACTICAL_GUIDANCE`;
- `COMPARISON`;
- `CAVEATS_LIMITATIONS`;
- `WORKFLOW_STEPS`;
- `TAXONOMY_CATALOG`;
- `SOURCE_PROVENANCE`;
- `DECISION_SUPPORT`;
- `FAQ_DIRECT_ANSWER`;
- `NEXT_STEP_NAVIGATION`.

Consecutive sections must not merely paraphrase the same role/content.

### 19.3. Four-layer source-grounded expansion

When facts are limited, expand in this order:

```text
1. CONFIRMED FACT
2. WHAT IT MEANS / WHY IT MATTERS
3. HOW TO USE / READ / APPROACH IT
4. CAVEAT / BOUNDARY / RELATED NEXT STEP
```

This produces depth without inventing capabilities.

Example:
A source says `local high scores`.
The site may explain:
- that the record remains local;
- how local scoring changes the user's comparison habit;
- a practical routine for tracking improvement;
- that this is not evidence of an online global leaderboard.

It may **not** invent cloud sync, global ranks or social competition.

### 19.4. Source expansion research

When extra factual depth is needed, prefer:
1. user-provided source URL;
2. official product/developer documentation/support pages;
3. authoritative platform/store documentation relevant to the feature;
4. other clearly authoritative public sources.

Do not use low-quality SEO copy as a factual authority merely to make pages longer.

### 19.5. CONTENT DEPTH MANIFEST

Before BUILD record per page:

```text
page_key
page_type
depth_tier
target_word_envelope
actual_or_planned_word_count
section_count
information_roles[]
confirmed_fact_count
editorial_explanation_count
practical_guidance_count
source_limitations[]
repetition_risk
```

### 19.6. Repetition prevention

Reject content when:
- two consecutive paragraphs express the same conclusion;
- several sections repeat the same source fact without adding interpretation;
- generic phrases such as "melhora a experiência" substitute for real explanation;
- CTA copy is used as content filler;
- the same intro paragraph structure is repeated across internal pages.

### 19.7. Long copy must stay scannable

More content requires better structure:
- descriptive subheads;
- short paragraphs mixed with deeper paragraphs;
- lists only where list semantics are real;
- tables/definition ledgers for comparison/data;
- pull quotes/fact rails only when they add hierarchy;
- contextual internal links;
- visual breaks approximately every few information clusters where useful.

Do not create a 1500-word wall of text to satisfy depth.



## 20. Interactive Content Semantics (v4.5.0)

Interaction may restructure content but must not dilute information depth.

Use:
- tabs when categories/states are parallel alternatives;
- accordion when details are optional or question-driven;
- slider/rail when peer items benefit from browsing but a long static grid would be worse;
- comparison switcher when the user is genuinely comparing modes/options;
- filters only when the collection is large enough to justify them;
- sticky chapters/progress when long-form navigation benefits.

Do not:
- hide the only important explanation behind arbitrary clicks;
- turn five normal paragraphs into five accordions merely to shorten the page;
- use a slider for unrelated content that should be visible together;
- repeat the same interaction structure across every internal page.

Each interactive section still receives an `information_role` and contributes to CONTENT DEPTH MANIFEST.



## 21. OFFICIAL GAME STUDIO CONTENT MODEL (v4.6.0)

When `business_model_mode = OFFICIAL_GAME_STUDIO` and the developer-relationship truth gate passes, the site's content must behave like the public site of the studio that created and promotes the game.

### 21.1 Voice
Use a natural first-person studio voice across marketing/editorial copy:
- `we created / we designed / our team / our game` equivalents are allowed only after the ownership/developer gate passes;
- avoid outsider phrases such as `the developer created`, `this guide reviews`, `independent editorial portal`, unless discussing an external source;
- product copy should feel like a creator explaining the product, not an affiliate site paraphrasing a store listing.

### 21.2 Core page jobs
A full gaming site should normally cover these jobs across distinct pages/sections:

```text
HOME            → studio + game proposition + strongest play/download CTA
GAME / PRODUCT  → gameplay, features, modes/mechanics, screenshots/visual explanation, store CTA
DEVELOPMENT     → concept → prototype → mechanics → art → balancing/testing → release/iteration, only where factual
ABOUT / STUDIO  → studio mission, creative/product philosophy, confirmed team/ownership facts
UPDATES         → real updates/releases only when source or owner data exists
FAQ             → game, compatibility, controls, support, purchase/download questions supported by facts
CONTACT/SUPPORT → first-party game/studio support when relationship is verified
LEGAL           → actual site/runtime/operator facts, never marketing fiction
```

Exact page count/order may vary through the composition engine; these are semantic jobs, not a fixed template.

### 21.3 Development-story truthfulness
Development/process content may explain confirmed stages such as:
- idea/problem the team wanted to solve;
- prototype/iteration;
- core mechanic design;
- level/progression design;
- art direction;
- balancing;
- QA/testing;
- release and post-release iteration.

Do not fabricate exact dates, internal anecdotes, employee roles, technology stack, budgets, milestone names, testing counts or roadmap commitments. If the source does not support a historical detail, either use an owner-supplied fact or omit it.

### 21.4 Promotional content
The site is allowed and expected to promote the game:
- repeat the official store/play destination contextually, not as spam;
- explain player value through factual gameplay/features;
- use product-led CTA language such as `Play`, `Download`, `Get the game`, `See gameplay`, `Discover how we built it`, localized to GEO;
- connect features to the team's design intent when that intent is owner-supplied or source-supported.

### 21.5 Business-model consistency map
Before BUILD produce:

```text
BUSINESS_MODEL_CONTENT_MAP
studio_brand
game_name
business_model_mode
developer_relationship_status
voice = FIRST_PERSON_STUDIO
commercial_goal = PROMOTE_GAME
primary_conversion
page_business_role{}
allowed_creator_claims{}
blocked_unsupported_claims{}
store_destination
support_relationship
```

Every major page must have a `page_business_role`; pages without a role are reviewed for filler or model drift.



## 22. STUDIO STORY & DEVELOPMENT CONTENT ARCHITECTURE (v4.6.1)

This module expands `OFFICIAL_GAME_STUDIO` from a voice rule into a page/topic system.

### 22.1 About / Studio content blueprint

When the relationship gate passes, About should be written as a first-party studio page rather than an editorial methodology page. Select 4–7 meaningful layers from:

```text
studio introduction
our game / product relationship
what the game is
why the product exists — only with creator-intent evidence
creative/product principles
how we approach mechanics / art / iteration at a supported level
what we learned / refined — only with evidence
how players can experience the game
support/contact path
```

Good About copy makes the studio/game relationship obvious within the first meaningful viewport or immediately following content block.

Do not force a fake corporate biography. A small independent studio may be described simply and credibly without invented headquarters, departments, staff biographies or founding milestones.

### 22.2 Development topic generator

Derive internal page topics from the actual game's strongest source-supported systems. Examples:

```text
source shows moving bricks
→ candidate page: how movement changes level rhythm / encounter design

source shows one-finger control
→ candidate page: controls & feel / input simplicity

source shows bonuses/modifiers
→ candidate page: mechanic interaction / power-up design

source shows changing layouts
→ candidate page: level variation / pacing / replay structure

source shows boss-like creatures
→ candidate page: encounter design / escalation
```

This mapping may explain the **observable design** without inventing historical motive. `Why we chose it` requires creator-intent evidence.

### 22.3 Thematic page content recipe

Each development/product page should normally combine several of these blocks:

```text
CREATOR / PRODUCT OPENING
CONFIRMED GAME FACTS
SYSTEM OR MECHANIC BREAKDOWN
DESIGN CONSEQUENCE
PLAYER EXPERIENCE / BENEFIT
PROCESS OR ITERATION NOTE — only when supported
VISUAL / DIAGRAM EXPLANATION
RELATED DEVELOPMENT TOPIC
PLAY / DOWNLOAD / SUPPORT CTA
```

Do not make every page use the same order or headings. Composition remains independently randomized by the section engine.

### 22.4 Distinguish product fact from creator intent

Allowed without extra creator-history evidence:
- describe what the game contains;
- explain how mechanics interact;
- explain what a player experiences;
- compare states/modes that are visibly/source supported;
- explain practical controls/progression.

Requires owner/source evidence:
- why the team chose a mechanic;
- what inspired the game;
- first prototype story;
- what testers said;
- what the team changed after testing;
- internal production sequence;
- toolchain/engine;
- staff responsibilities;
- schedule/budget/milestones.

### 22.5 Page-role diversity

A rich official-studio site should avoid making all internal pages into `guide` pages. Prefer a mix such as:

```text
PRODUCT STORY
MECHANIC DEEP DIVE
DEVELOPMENT / MAKING-OF
LEVEL / PROGRESSION DESIGN
ART / VISUAL DIRECTION
CONTROLS / FEEL
SUPPORT / FAQ
ABOUT / STUDIO
```

Exact mix follows source depth. If only 3–4 strong topics are supported, build fewer stronger pages rather than filler.

### 22.6 Conversion without repetition

Every page can contribute to promotion, but the CTA should match the page:
- mechanics page → `Try the mechanic in the game` / locale equivalent;
- development page → `See the finished game`;
- About → `Discover our game`;
- controls page → `Play and feel the controls`;
- support → `Get help` plus store/product path;
- FAQ → answer first, conversion second.

### 22.7 Global Text branches

Recommended content keys:

```text
entities.studio_brand
entities.game_name
business_model.mode
business_model.voice
pages.about.studio_intro
pages.about.game_relationship
pages.about.product_principles
pages.about.development_approach
pages.development.*
pages.mechanics.*
pages.progression.*
pages.art_direction.*
pages.controls.*
cta.play_download
cta.see_game
cta.how_we_built_it
cta.support
```

Only create branches for pages actually present in the manifest.


## 23. NAVIGATION COPY + PAGE-NAMING ENGINE (v4.6.3)

This engine varies **how known page roles are named publicly** without changing what those pages are.

### 23.1. Naming layers

Keep these fields independent:

```text
page_key                 = stable machine identity
page_business_role       = stable semantic/business job
nav_label                = short randomized locale-natural menu label
page_display_title       = visible page title/H1 family
seo_title                = SEO-owned title
canonical_slug           = stable URL identity
```

`nav_label` is the main target of synonym randomization. `page_display_title` may also vary within its own role-safe title family, but it is not forced to equal the menu label.

### 23.2. Permanent semantic synonym bank

The bank below is a **semantic concept bank**. For non-English sites, generate natural localized equivalents for the target locale, then filter awkward/literal translations before random selection.

```text
HOME
Home | Start | Welcome | Overview | Discover | Start Here | Studio Home | Main | Explore | Welcome to {Studio}

ABOUT_STUDIO
About Us | Our Studio | Who We Are | Studio | Our Story | Meet the Studio | Behind the Studio | Our Approach | Studio & Game | About {Studio} | Inside the Studio | The People Behind the Game*

GAME_PRODUCT
Our Game | The Game | Game | Discover the Game | Explore {Game} | Meet {Game} | Play {Game} | About the Game | Game Overview | The Experience | Inside {Game} | {Game}

DEVELOPMENT
Development | How We Built It | Making the Game | Behind the Build | From Idea to Game | Development Story | Building {Game} | The Making Of | Our Process | Inside Development | Design & Development | How It Came Together

MECHANICS
Mechanics | Game Mechanics | Core Mechanics | Game Systems | How It Works | Gameplay Systems | Systems & Rules | Inside the Mechanics | Mechanics Explained | Core Systems

PROGRESSION_LEVELS
Progression | Level Design | Levels & Progression | Game Flow | Pacing & Challenge | Progression Design | Level Rhythm | Difficulty & Flow | Building the Challenge | How Levels Evolve

CONTROLS_FEEL
Controls | How to Play | Controls & Feel | Game Feel | Input & Feel | Playing {Game} | Control Design | Interaction | Touch & Control | How It Feels

ART_VISUAL
Art Direction | Visual Direction | Art & Style | Visual Design | The Look of {Game} | Game Art | Visual World | Style & Atmosphere | Art Behind the Game | Look & Feel

FAQ
FAQ | Questions & Answers | Common Questions | Your Questions | What to Know | Help & Answers | Quick Answers | Questions | Need to Know | Player Questions

SUPPORT
Support | Game Support | Player Support | Help Center | Get Help | Need Help? | Support Center | Help & Support | Assistance | Technical Help

CONTACT
Contact | Contact Us | Get in Touch | Reach Us | Write to Us | Talk to Us | Studio Contact | Send a Message | Connect with Us | Contact the Studio

UPDATES
Updates | Game Updates | What's New | News | Latest | Release Notes | Changelog | New & Updated | Development Updates | Latest from the Studio

PLAY_STORE
Play | Download | Get the Game | Play Now | Download {Game} | Get {Game} | Visit Store | Play {Game} | Try the Game | Get Started
```

`*` Team/people wording is eligible only when the site can truthfully support a team/person relationship.

The bank may expand over time. Do not shrink it to one canonical word per role.

### 23.2a. Example curated locale pack — PT-PT (non-authoritative example)

Portugal (`pt-PT`) is shown only as one **example locale pack**. It is not a special-case requirement and must never be treated as the only locale with lexical variation. Every resolved target locale must receive an equivalent native-quality candidate pool through the universal locale resolver in section 23.9. The list is deliberately conservative: variation should be noticeable across sites only when compared side-by-side, not conspicuous inside one site.

```text
HOME
Início | Página inicial | Começar | Entrada | Visão geral

ABOUT_STUDIO
Sobre nós | O estúdio | O nosso estúdio | Quem somos | A nossa história | Conhece o estúdio | Por dentro do estúdio | Estúdio e jogo | Sobre {Studio} | A nossa abordagem

GAME_PRODUCT
O jogo | O nosso jogo | {Game} | Conhece {Game} | Descobre {Game} | Explora {Game} | Sobre o jogo | A experiência | Por dentro de {Game} | Jogar {Game}

DEVELOPMENT
Desenvolvimento | Criação do jogo | Como fizemos {Game} | Como criámos o jogo | Nos bastidores | O processo | Processo de desenvolvimento | Do conceito ao jogo | Por dentro do desenvolvimento | Como nasceu {Game}*

MECHANICS
Mecânicas | Mecânicas do jogo | Sistemas de jogo | Como funciona | Jogabilidade | Sistemas e regras | Núcleo do jogo | Por dentro das mecânicas | Regras do jogo | Sistemas principais

PROGRESSION_LEVELS
Progressão | Níveis | Níveis e progressão | Design de níveis | Ritmo e desafio | Progressão do jogo | Estrutura dos níveis | Fluxo do jogo | Desafio e progressão | Evolução dos níveis

CONTROLS_FEEL
Controlos | Como jogar | Controlos e resposta | Jogabilidade | Resposta do jogo | Interação e controlos | Controlo do jogo | Jogar {Game} | Comandos | Controlos do jogo

ART_VISUAL
Direção artística | Arte e estilo | Identidade visual | Visual do jogo | Estilo visual | Arte de {Game} | Mundo visual | Estilo e atmosfera | Design visual | Por trás do visual

FAQ
Perguntas frequentes | Perguntas e respostas | Dúvidas frequentes | Dúvidas | Respostas rápidas | Ajuda e respostas | Perguntas dos jogadores | Perguntas comuns | O que saber | Centro de respostas

SUPPORT
Apoio | Apoio ao jogador | Ajuda | Centro de ajuda | Suporte | Assistência | Apoio técnico | Ajuda com o jogo | Precisas de ajuda? | Apoio e ajuda

CONTACT
Contacto | Contacte-nos | Fale connosco | Escreva-nos | Entrar em contacto | Falar com o estúdio | Contactar o estúdio | Enviar mensagem | Contacto do estúdio | Fala connosco

UPDATES
Novidades | Atualizações | Notícias | O que há de novo | Notas de versão | Novidades do jogo | Atualizações do jogo | Últimas novidades | Mudanças recentes | Diário de desenvolvimento*

PLAY_STORE
Jogar | Jogar agora | Transferir | Obter o jogo | Ver na loja | Abrir na loja | Visitar a loja | Experimentar o jogo | Jogar {Game} | Obter {Game}
```

`*` Historical/process wording is eligible only when the corresponding content/evidence gate permits it.

Do not force an explicit `HOME` menu item when the linked brand/logo already provides an obvious Home destination; omitting it is itself a valid header/navigation variation.

### 23.2b. Lexical profile + same-GEO distribution

Before role-level draws, randomly select a subtle `navigation_lexical_profile` such as:

```text
DIRECT_SHORT
STUDIO_LED
EDITORIAL_CLEAR
PRODUCT_LED
EXPLORATORY_LIGHT
ACTION_LIGHT
```

The profile is a **soft eligibility/tone filter**, not a reason to make every label follow the same grammatical pattern. Whole-menu naturalness is more important than profile purity.

For each role, seed the candidate permutation with:

```text
navigation_copy_nonce + normalized_domain + locale + semantic_role
```

This makes separate domains naturally decorrelate even without access to prior-site memory.

If `N` sites of the same locale are being generated together, build a cross-site assignment matrix first:
- common-role exact labels are allocated without replacement while clear candidates remain;
- exact whole-menu fingerprints may not repeat;
- when each relevant role has `>=6` valid candidates, no pair should normally share more than `50%` of visible primary-nav labels;
- if a role has only a small clear pool, allow repetition rather than inventing unnatural language.

When history exists, avoid the exact label used for the same role by the latest `3` same-locale unrelated sites when `>=4` alternatives remain. Avoid exact whole-menu fingerprint matches against the latest `10` same-locale sites.

### 23.3. Locale realization

For each present page role:
1. start from the permanent semantic concepts;
2. produce natural target-locale equivalents;
3. remove literal/unnatural translations;
4. remove labels that imply unsupported facts (`team`, `official`, `news`, `release notes`, etc.);
5. remove candidates that are too ambiguous by themselves in the current menu;
6. remove normalized duplicates across primary destinations;
7. check length against eligible header families;
8. retain a healthy eligible pool;
9. choose by seeded random draw using `navigation_copy_nonce`.

For common roles, aim for:

```text
eligible_locale_variants >= 6 normally
eligible_locale_variants >= 8 when naturally available
```

If natural language only supports fewer good choices, semantic clarity wins over quota.

### 23.4. Random means random after eligibility

Do not rank one conventional word as automatic winner.

Correct:

```text
ROLE-SAFE POOL
→ locale/meaning/fit filters
→ eligible variants
→ seeded random draw
```

Incorrect:

```text
score every synonym
→ always choose highest score (`About`, `Contact`, `FAQ`)
```

### 23.5. Whole-menu anti-collision

After all labels are selected, validate the menu as one set.

Blocking:
- two primary destinations share the same normalized label;
- two labels are so similar that destination meaning is unclear;
- a label describes a different page role;
- every site falls back to the same canonical set despite healthy pools;
- long labels create header/mobile overflow.

If blocked, reroll only the affected role(s) first; reroll the header family when the copy set itself is strong.

### 23.6. Page display-title variation

The visible H1/page title may use a richer role-safe family than the nav label.

Example relationship:

```text
page_key: about
nav_label: Our Studio
page_display_title: Meet the studio behind {Game}
seo_title: About {Studio} and {Game} | {Studio}
canonical_slug: /about/   (or the already selected stable localized slug)
```

The values serve different jobs and need not be identical.

### 23.7. Persistence / user edits

Record:

```text
NAVIGATION_COPY_MANIFEST
navigation_copy_nonce
navigation_lexical_profile
domain_lexical_salt
menu_lexical_fingerprint
cross_site_lexical_history_available
batch_same_locale_site_count
page_key
semantic_role
eligible_candidate_count
selected_nav_label
selected_label_family
compact_variant_optional
rejected_candidates_with_reason[]
```

The selected visible values are stored in Global Text. Manual user edits persist through updates and are not overwritten by reseeding.

### 23.8. Legal labels

Legal navigation uses a **constrained clarity-first pool** rather than aggressive synonym variation. `Privacy`, `Terms`, `Cookies` (localized equivalents) may vary only among clearly equivalent legal labels such as `Privacy Policy` vs `Privacy` where jurisdiction/context permits.

Novelty never outranks legal clarity.



## 23.9. UNIVERSAL GEO / LOCALE NAVIGATION LEXICON RESOLVER (v4.6.4)

Navigation lexical diversity is mandatory for **every GEO and resolved locale**, not only Portugal or English-language sites.

### 23.9.1 Input resolution

Before navigation-copy generation resolve:

```text
geo
country_code
locale
language
regional_language_variant
script
site_business_model
semantic_navigation_roles[]
```

`GEO` does not by itself authorize guessing a language when the market is multilingual. If the source/input does not establish the intended locale, resolve it before BUILD.

Examples of valid distinctions include:
- `pt-PT` vs `pt-BR`;
- `en-GB` vs `en-US` vs `en-CA`;
- `fr-FR` vs `fr-CA`;
- `de-DE` vs `de-AT` vs `de-CH`;
- regional vocabulary/spelling differences in any other supported locale.

### 23.9.2 Universal locale-pack construction

For each semantic role, build a target-locale candidate pool from **meaning first, wording second**:

```text
STABLE SEMANTIC ROLE
→ PERMANENT CONCEPT FAMILY
→ TARGET LOCALE REALIZATION
→ REGIONAL NATURALNESS FILTER
→ BUSINESS-MODEL TRUTH FILTER
→ AMBIGUITY FILTER
→ MENU-COLLISION FILTER
→ HEADER-FIT FILTER
→ ELIGIBLE NATIVE LABEL POOL
```

The English concept bank is a semantic seed, not a translation template. Literal translation is prohibited when a native site would use a different phrase.

When web research is available and the locale is unfamiliar or ambiguous, inspect current native-language website navigation patterns from the target market to calibrate ordinary wording. Extract common linguistic patterns only; do not copy a brand's exact navigation set.

When web research is unavailable, generate multiple native candidates from language competence, then run a self-audit for grammar, register, regional spelling, clarity and role match. Record the research limitation instead of falling back to English defaults.

### 23.9.3 Candidate-depth requirement

For common non-legal roles such as About, Product/Game, Development, FAQ/Help and Contact:

```text
target eligible native variants >= 8
minimum healthy pool >= 6 when language permits naturally
```

For roles whose language naturally has fewer concise labels, preserve clarity and record `LEXICON_POOL_CONSTRAINED`; do not invent awkward pseudo-synonyms to hit a quota.

Legal labels remain clarity-first and are exempt from aggressive lexical variation.

### 23.9.4 New-site randomization independent of memory

Every new site receives:

```text
navigation_copy_nonce = fresh random
domain_lexical_salt = HASH(normalized_domain + locale)
locale_lexical_lane = HASH(domain_lexical_salt + navigation_copy_nonce)
```

For each semantic role:

```text
role_seed = HASH(locale_lexical_lane + semantic_role)
→ seeded permutation of eligible native candidates
→ choose first candidate that passes whole-menu anti-collision
```

This makes unrelated domains in the same market naturally decorrelate even when prior-site memory is unavailable. It reduces accidental repetition but does not pretend an infinite finite-language vocabulary exists.

### 23.9.5 Batch anti-repeat — hard distribution

When multiple sites are generated together for the same resolved locale, assign common-role labels **without replacement** until that role's healthy pool is exhausted.

For a batch of `N` sites:

```text
FOR EACH semantic_role:
  build native eligible pool
  seeded shuffle by batch nonce
  distribute different labels to sites 1..N
  only reuse after all eligible labels have been consumed
```

Whole-menu fingerprints must also differ. If two sites still look lexically too similar, reroll the overlapping roles with the largest available pools.

Default batch target when pools allow:

```text
exact same role-label reuse before pool exhaustion = 0
identical full primary-menu fingerprint = 0
pairwise primary-menu exact-label overlap <= 0.50 normally
```

### 23.9.6 Cross-session/history-aware enhancement

When prior manifests for the same locale are available:
- hard-exclude the exact same label used for the same common role by the most recent unrelated sites while `>=4` alternatives remain;
- reject identical full-menu fingerprints against recent unrelated sites;
- prefer underused native candidates without making the vocabulary strange.

History improves diversity but is **not required** for baseline operation.

### 23.9.7 Quiet-naturalness rule

Variation should feel ordinary to a native visitor. Reject labels that are:
- clever but unclear;
- poetic where navigation needs directness;
- literal translations that sound foreign;
- grammatically wrong for the regional variant;
- excessively long merely to be unique;
- misleading about page content;
- dependent on unsupported facts such as `team`, `official`, `news`, `release notes`, `studio` when those claims are unavailable.

The target is **different vocabulary across sites, not conspicuous vocabulary inside a site**.

### 23.9.8 Required locale lexicon artifact

Before selection record:

```text
NAVIGATION_LOCALE_LEXICON
geo
locale
regional_language_variant
semantic_role
concept_candidates[]
native_candidates[]
rejected_unnatural[]
rejected_ambiguous[]
rejected_truth_conflicts[]
eligible_candidates[]
lexicon_source_mode = CURATED_PACK | LIVE_CALIBRATED | MODEL_NATIVE_FALLBACK
lexicon_pool_status = HEALTHY | CONSTRAINED
```

The final `NAVIGATION_COPY_MANIFEST` references this artifact.

<!-- BUNDLE-MODULE-END: 07-CONTENT-ENGINE.md -->

---

<!-- BUNDLE-MODULE-START: 08-LEGAL-GEO-ENGINE.md -->

# LEGACY MODULE: 08-LEGAL-GEO-ENGINE.md

# LEGAL GEO ENGINE

**Version:** 4.4  
**Role:** Privacy / Terms / Cookies відповідно до GEO і runtime

---

## 1. Головний принцип

Legal text не є статичним шаблоном.

Він генерується з:

`GEO + locale + site type + runtime feature manifest + owner data`

---

## 2. Перед генерацією

Зібрати runtime facts:

- contact forms;
- accounts;
- comments;
- newsletter;
- analytics;
- ads;
- affiliate systems;
- embeds;
- video;
- maps;
- payments;
- e-commerce;
- cookies;
- localStorage;
- external APIs;
- hosting/logs;
- age/audience;
- data fields;
- processors/vendors.

---

## 3. GEO research

Для кожного production site:
- визначити target jurisdiction;
- перевірити актуальні authoritative legal/regulator sources;
- сформувати legal requirements profile;
- лише після цього draft legal pages.

Не покладатися на старий static legal knowledge, якщо питання залежить від чинних вимог.

---

## 4. Contact / owner data state

Кожне contact field має статус:
- `VERIFIED`
- `OWNER_SUPPLIED`
- `SYNTHETIC_GEO_CONTACT`
- `REQUIRES_OWNER_DATA`

Legal pages можуть використовувати тільки `VERIFIED` або `OWNER_SUPPLIED` як підтверджені legal identity facts.

`SYNTHETIC_GEO_CONTACT` може бути використаний як public presentation/contact profile, якщо це явно обраний режим фабрики, але ніколи не повинен перетворюватися на claim про:
- registered office;
- verified controller address;
- legal company registration;
- підтверджену working hotline;
- реальне місце діяльності.

У legal article synthetic contact може бути згаданий лише як website public contact channel, а не як підтверджена юридична ідентичність.

## 5. Unknown owner data

Ніколи не вигадувати як **verified legal facts**:
- company/operator legal name;
- registered/legal address;
- DPO;
- registration number;
- processor;
- retention period;
- governing law details.

Використовувати internal state:

`REQUIRES_OWNER_DATA`

Перед фінальним production release такі поля повинні бути:
- заповнені власником;
- або сторінка чітко пояснює, що інформація ще не надана, якщо сайт тестовий.

---

## 6. Privacy Policy

Повна article structure, відповідно до applicability:

- scope / last updated;
- controller/operator;
- categories of data;
- data sources;
- purposes;
- legal bases;
- recipients/processors;
- transfers;
- retention;
- security;
- rights;
- withdrawal/objection;
- complaint/supervisory authority;
- children/audience;
- third-party links/services;
- changes.

Не всі секції однаково застосовні до всіх сайтів.
Текст має відображати фактичний runtime.

---

## 7. Cookie Policy

Включити:
- що таке cookies / local storage;
- exact technologies;
- keys/categories where useful;
- purpose;
- first/third party;
- duration;
- necessary/optional;
- consent model;
- withdrawal/change preferences;
- browser controls;
- third parties;
- updates.

---

## 8. Terms

Адаптувати до site type:

- nature/scope;
- acceptance/use;
- audience/eligibility if needed;
- informational nature;
- IP/trademarks;
- acceptable use;
- external services;
- disclaimers appropriate to niche;
- changes;
- operator/contact;
- jurisdiction wording only when supported.

---

## 9. Cookie/consent UX

### Якщо лише necessary storage
Не робити fake “Accept cookies” marketing consent.

Можна:
- compact informational notice;
- link to Cookie Policy;
- dismiss state.

### Якщо є optional trackers
Потрібні:
- correct consent flow;
- optional tech inactive before required consent;
- manage/withdraw preferences;
- legal/runtime synchronization.

---

## 10. Legal presentation

Legal pages не виглядають як marketing cards.

Використовувати:
- article width;
- readable body;
- TOC;
- H2/H3;
- lists;
- tables;
- anchors;
- last updated;
- print-friendly structure.

---

## 11. Legal ↔ Runtime QA

BLOCK RELEASE якщо:
- runtime має analytics, legal каже “немає analytics”;
- third-party embed не disclosed;
- Cookie Policy описує неіснуючий tracker;
- consent активує optional storage до consent;
- mandatory legal page відсутня;
- footer link broken;
- legal page thin/incomplete.

---

## 12. Legal integrity

Factory генерує informative draft на базі актуального profile.

Для production use:
- не називати текст “юридично гарантовано правильним”;
- owner review потрібен, коли цього вимагає ризик/бізнес-контекст;
- невідомі факти не домислюються.


---

## 13. Contact consistency gate

BLOCK RELEASE якщо:
- Privacy показує один email, а Contact інший;
- phone/address у footer не збігаються з Contact;
- `SYNTHETIC_GEO_CONTACT` використаний як registered/legal identity;
- synthetic address названа registered office/controller address;
- controller legal identity вигадана;
- public email/phone/address зазначені як working без owner confirmation або verification.

---

## 14. Full legal-article depth (v4.3 patch)

Legal pages не можуть бути thin summaries.

Privacy / Terms / Cookie pages повинні бути:
- fully written;
- localized to GEO/language;
- structurally sectioned with headings/lists;
- adapted to actual site model (informational/game guide/editorial/store/etc.);
- linked in footer and consent UI.

## 15. Cookie UX requirement

Site повинен мати:
- compact cookie banner/bar that does not destroy the hero;
- secondary button/link to open preferences/settings modal;
- localized short explanation;
- links to Privacy Policy and Cookie Policy.

### Necessary-only runtime
If the site uses only necessary storage:
- primary action is acknowledgement/dismiss (`OK`, `Entendi`, locale equivalent), **not fake marketing consent**;
- settings modal still exists and shows the necessary category as always enabled;
- no invented analytics/marketing toggles.

### Optional trackers runtime
If optional categories actually exist:
- primary accept action may be shown;
- reject non-essential action is present;
- preferences modal exposes only real categories;
- optional tech stays inactive until required consent.

Cookie settings modal must always open/close cleanly and persist the user's choice where appropriate.


---

## 18. Legal copy in Global Text (v4.4)

Privacy, Terms and Cookies public copy must be stored in the persistent `global-text.json`.

Recommended structure:

```text
legal.privacy.title
legal.privacy.intro
legal.privacy.sections[]
legal.terms.title
legal.terms.sections[]
legal.cookies.title
legal.cookies.sections[]
```

Each section should be structured with text-only fields:

```text
id
heading
paragraphs[]
bullets[]
```

The template supplies HTML semantics.

### Runtime/legal separation

Legal logic/state remains outside Global Text:
- actual cookie/runtime inventory;
- consent category booleans;
- verified/synthetic status;
- schema eligibility;
- URLs/slugs.

But all **visible wording** describing those facts is resolved from Global Text.

### Safety

A manual text edit must not silently change factual runtime behavior. If legal copy claims a technology or processing activity that the runtime manifest does not support, legal QA must flag the mismatch.

<!-- BUNDLE-MODULE-END: 08-LEGAL-GEO-ENGINE.md -->

---

<!-- BUNDLE-MODULE-START: 13-CONTACT-GEO-ENGINE.md -->

# LEGACY MODULE: 13-CONTACT-GEO-ENGINE.md

# CONTACT GEO ENGINE

**Version:** 4.3.5  
**Role:** mandatory site-domain public email mode, synthetic GEO phone/address, operator-contact consistency

---

## 1. Мета

Кожен сайт повинен мати повноцінний contact profile, адаптований до:

```text
DOMAIN + GEO + TOPIC/NICHE + BRAND
```

Контакти не повинні виглядати як test placeholders.

Водночас фабрика повинна знати, що згенерований реалістичний contact ≠ verified legal identity.

---

## 2. Mandatory input

До contact generation повинні бути **resolved**:

```text
DOMAIN
GEO
TOPIC / NICHE
```

User obligation:
```text
SOURCE URL
GEO / TYPE
DOMAIN
```

`TOPIC / NICHE` factory derives from SOURCE URL when the source clearly establishes the subject. Ask the user only when the source is ambiguous.

Optional:
- brand name;
- real owner email;
- real phone;
- real address;
- legal operator/company identity.

Якщо DOMAIN або GEO відсутні:
`CONTACT_INPUT_REQUIRED → STOP BEFORE BUILD`.

---

## 3. Contact Profile

Створити до BUILD:

```text
brand_name
domain
geo
locale

public_email
public_email_status

public_phone_display
public_phone_e164
public_phone_status
phone_interaction_state

postal_address
postal_address_status

legal_operator_name
legal_operator_status
legal_address
legal_address_status

source
generation_notes
```

---

## 4. Status model

Допустимі field states:

- `VERIFIED`
- `OWNER_SUPPLIED`
- `SYNTHETIC_GEO_CONTACT`
- `REQUIRES_OWNER_DATA`

### VERIFIED
Підтверджено authoritative/public source.

### OWNER_SUPPLIED
Надано користувачем як його власні дані.

### SYNTHETIC_GEO_CONTACT
Згенеровано фабрикою:
- виглядає природно;
- відповідає GEO;
- не є obvious placeholder;
- не вважається доказом, що mailbox/phone/address реально працює або належить оператору.

### REQUIRES_OWNER_DATA
Потрібно для юридичного/операційного use, але немає достатніх даних.

---

## 5. Public email engine — domain mailbox contract

### 5.1 Priority

```text
VERIFIED / OWNER_SUPPLIED explicit email
→ SYNTHETIC_DOMAIN_MAILBOX on exact site DOMAIN
```

For factory-generated contact identity, user-supplied `DOMAIN` is authoritative for the public email host as well as site identity, canonical URLs, links, sitemap and publisher identity.

### 5.2 Generated domain mailbox

If no owner email is supplied, generate:

```text
{locale_natural_role}@{DOMAIN}
```

Before construction, normalize `DOMAIN` to the canonical hostname only:
- lowercase;
- no `http://` / `https://`;
- no path, query or fragment;
- no port;
- no trailing slash.

Do not invent a different mail host and do not add/remove a leading `www.` unless canonical site identity explicitly uses that hostname.

Examples:
```text
kontakt@wonparyn.org
redakcja@wonparyn.org
hello@domain.org
```

Local-part should normally be one short public role word suitable for the target locale/site role. Prefer clear contact/editorial nouns over brand repetition.

Avoid:
- random hashes;
- `test`, `demo`, `example`;
- campaign/build identifiers;
- duplicated brand strings such as `brand.guide@brand.tld` when a simple public role works;
- generated Gmail/Outlook/other off-domain primary website mailbox.

The generated mailbox may be displayed as the website's public contact channel, but its status remains `SYNTHETIC_GEO_CONTACT` until the owner confirms provisioning/deliverability.

### 5.3 Explicit owner/verified override

An exact email supplied by the owner or verified from an authoritative source may use another host if that is the actual contact the owner wants published. Do not rewrite owner-supplied contact data merely to satisfy the generated-mailbox convention.

### 5.4 Status

Generated domain mailbox:
`SYNTHETIC_GEO_CONTACT`.

Owner-provided:
`OWNER_SUPPLIED`.

Verified public source:
`VERIFIED`.

Never claim synthetic mailbox deliverability.

---

## 6. Synthetic phone engine

Якщо owner не надав phone, фабрика **генерує реалістичний GEO phone**, а не `000 000 000`.

### 6.1 GEO profile

Визначити:
- country calling code;
- national number length;
- geographic/mobile patterns;
- common human display grouping;
- E.164 representation;
- forbidden emergency/service/premium ranges.

### 6.2 Number generation

Phone повинен:
- мати natural digit distribution;
- не використовувати obvious sequences:
  - `000000`
  - `111111`
  - `123456`
  - `987654`
- не використовувати emergency/service numbers;
- не копіювати phone із unrelated business/source.

Priority:
1. documented fictional/reserved test range, якщо GEO його має;
2. otherwise plausible synthetic number;
3. exact-string web/search collision check, якщо доступний;
4. conflict → regenerate.

Search absence не перетворює number на VERIFIED.

### 6.3 Display

Example format:
```text
+351 21 845 67 32
```

Internal:
```text
+351218456732
```

### 6.4 Interaction

Default:
```text
status: SYNTHETIC_GEO_CONTACT
phone_interaction_state: DISPLAY_ONLY
```

`tel:` за замовчуванням активний лише для:
- `VERIFIED`
- `OWNER_SUPPLIED`

Synthetic phone не називати:
- official hotline;
- verified support;
- customer service number.

---

## 7. Synthetic address engine

Якщо owner address не надано, фабрика створює **natural-looking GEO address**.

### 7.1 Address profile

Визначити:
- street naming convention;
- building-number position;
- postal code format;
- locality/city;
- region/state rules;
- country display format.

### 7.2 Street generation

Street name:
- природний для мови/GEO;
- може походити з neutral geographic/editorial vocabulary;
- не використовує слова `Example`, `Exemplo`, `Test`, `Demo`;
- не копіює відому адресу source product/developer;
- не приписує real third-party business нашому сайту.

Building number:
- natural;
- non-zero;
- не очевидний placeholder.

Postal code:
- syntactically valid для GEO;
- не `00000` / `0000-000`.

### 7.3 Collision reduction

Якщо web/search доступний:
- exact address search;
- якщо exact address явно належить реальній company/residence/entity → regenerate;
- не використовувати real map pin для synthetic address.

Search absence не означає verified physical existence.

### 7.4 Status

```text
postal_address_status: SYNTHETIC_GEO_CONTACT
```

Synthetic address можна використовувати як normal-looking public website contact presentation, якщо user обрав synthetic mode.

Але його не називати:
- registered office;
- headquarters;
- verified shop/office;
- legal controller address.

---

## 8. Brand / operator display name

Якщо brand не наданий:
- derive from domain/topic;
- назва повинна бути природною;
- не копіювати third-party developer/product owner;
- status може бути `SYNTHETIC_GEO_CONTACT` для display brand.

Legal company/operator identity:
- тільки `OWNER_SUPPLIED` або `VERIFIED`;
- інакше `REQUIRES_OWNER_DATA`.

---

## 9. Operator vs product/developer support

Relationship depends on the active business model and verified/owner-supplied developer relationship.

### `OFFICIAL_GAME_STUDIO` with resolved developer relationship
Game/product support is first-party studio support. The website Contact/Support system may represent the same studio/game relationship. Verified source support channels may be linked or integrated as official product support when they belong to the same confirmed entity/brand relationship.

### Unresolved / independent / third-party relationship
Keep strict separation between:
- website public Contact Profile;
- third-party developer/app/product support from the source.

Не можна:
- merge a third-party developer email into the website identity when relationship is not resolved;
- переносити unrelated third-party phone/address у наш footer;
- використовувати third-party company як legal operator сайту without owner-supplied/verified legal identity;
- claim `our game` merely because the website links to official support.

---

## 10. Placement

### Contact page
Повний блок:
- public email according to Contact Profile mode;
- GEO phone;
- GEO address;
- contact scope;
- operator/product support distinction;
- privacy/legal links.

### Footer
Короткий consistent summary.

### Header/topbar
За Design DNA.

### Legal
Тільки fields, дозволені `08-LEGAL-GEO-ENGINE.md`.

### SEO/Schema
Тільки fields, дозволені `14-SEO-GEO-METADATA-ENGINE.md`.

---

## 11. Presentation quality

Visible contact block не повинен виглядати як debug/staging data.

Blocking visual patterns:
```text
contact@example.com
contact@site.example
+351 210 000 000
+1 555 000 0000
Rua Exemplo
Example Street
Test Address
```

For a factory-generated primary website email, host mismatch with the exact site `DOMAIN` is a blocking error. Explicit `OWNER_SUPPLIED` / `VERIFIED` email may use another host when that is the actual supplied contact.

---

## 12. GEO consistency

Для одного сайту:
- phone country code = GEO;
- display grouping = GEO convention;
- address format = GEO;
- postal code syntax = GEO;
- email local-part / presentation = locale-natural;
- legal jurisdiction не суперечить GEO;
- Contact/footer/meta мають один contact profile.

---

## 13. QA gate

BLOCK якщо:
- DOMAIN не наданий;
- `.example` присутній;
- obvious placeholder phone/address;
- synthetic status загублений у manifest;
- synthetic contact названий VERIFIED;
- third-party support виданий за website operator;
- Contact/footer не збігаються;
- `mailto:`/`tel:` interaction не відповідає status.

---

## 14. Release modes

### VERIFIED RELEASE
Контактні fields підтверджені або owner-supplied.

### SYNTHETIC CONTACT RELEASE
Сайт може мати production-looking public contact block, згенерований під GEO/brand/site context.

У manifest:
```text
contact_mode: SYNTHETIC_GEO_CONTACT
```

Це не перетворює synthetic data на legal/verified identity.

### LEGAL IDENTITY REQUIRED
Якщо конкретний site/business/legal context вимагає реальну operator identity:
`REQUIRES_OWNER_DATA` блокує legal production completion.

---

## 15. Regression rule

Ніколи більше не генерувати visual placeholders:
- `.example`
- `000...`
- `Example Street`
- `Rua Exemplo`

Замість цього:
`DOMAIN + GEO + TOPIC → SYNTHETIC_GEO_CONTACT`.

---

## 16. Synthetic public email mode — domain-first

If no owner email is supplied, the primary website email MUST be generated on the exact site `DOMAIN` using a short locale-natural role local-part:

```text
{role}@{DOMAIN}
```

Freemail hosts are not used for the factory-generated primary website identity. Synthetic domain email is never treated as verified identity or guaranteed-working mailbox.


## 17. Contact realism patch

Synthetic contact block повинен виглядати як реальний public contact package:
- natural email;
- plausible GEO phone;
- plausible GEO address;
- locale-consistent label language.

Поля повинні бути узгоджені між header, footer, contact page, legal pages і schema.


---

## 18. Contact visible-text handoff to Global Text (v4.3.3)

All public contact wording and editable display values must be exposed through Global Text keys.

Examples:

```text
contact.heading
contact.intro
contact.public_email
contact.phone_display
contact.address_lines[]
contact.support_scope
contact.privacy_note
contact.operator_label
contact.official_app_support_label
```

Machine/status fields remain in Contact Profile:
- VERIFIED / OWNER_SUPPLIED / SYNTHETIC_GEO_CONTACT;
- normalized interaction state;
- schema/legal eligibility.

### Derived actions

When safe/allowed:
- `mailto:` may be derived from `contact.public_email`;
- `tel:` may be derived from normalized phone logic.

Do not hardcode a visible email/phone/address in templates separately from Global Text.

A Global Text edit must not automatically upgrade synthetic contact status to verified.



## 19. Public contact naturalness + visibility patch (v4.3.5)

For a synthetic public website mailbox used as the primary Contact identity:
- the only factory-generated primary shape is `{locale_natural_role}@{DOMAIN}`;
- choose one concise, locale-natural public role such as `kontakt`, `redakcja`, `contact`, `hello` or `info` when appropriate;
- do not use provider-host patterns, brand-repeating local-parts, technical aliases, campaign/build identifiers or generated off-domain hosts as the primary mailbox;
- the site-domain syntax does not prove the mailbox is provisioned or deliverable; state remains `SYNTHETIC_GEO_CONTACT` until owner confirmation/verification.

There are exactly two primary-email source modes:
1. explicit `OWNER_SUPPLIED` / `VERIFIED` email, preserved as supplied;
2. otherwise factory-generated `{locale_natural_role}@{DOMAIN}`.

No freemail/off-domain fallback mode exists for factory generation.

Visibility contract:
- when email, phone and address are resolved, all three must appear visibly on Contact;
- `DISPLAY_ONLY` phone is still visibly rendered as text, just without an active `tel:` action;
- synthetic postal address is visibly labelled/presented as public presentation contact, never as registered office;
- official product support follows the resolved relationship: same-studio support may be integrated into first-party Support; unresolved/third-party support is shown separately and must never masquerade as the site's own operator identity.

<!-- BUNDLE-MODULE-END: 13-CONTACT-GEO-ENGINE.md -->

---



## 24. FOOTER COPY POLICY — UTILITY FIRST (v4.6.5)

The Content Engine does **not** treat the footer as an additional editorial section.

### Default footer copy model
Prefer short labels and destinations:
```text
BRAND
PRIMARY / SECONDARY NAV
CONTACT / SUPPORT
OFFICIAL GAME / STORE DESTINATION
LEGAL
COPYRIGHT / RIGHTS
```

A prose descriptor is optional, not required. Default descriptor paragraph count is `0`.

### OFFICIAL_GAME_STUDIO
Forbidden footer wording includes localized equivalents of:
- independent guide / independent review;
- editorial portal / editorial project;
- `facts from the official source` methodology statements;
- advice-vs-confirmed-feature explanations;
- source-provenance paragraphs;
- repeated `we created the game` story already covered by Home/About/Development.

The footer may still contain a concise direct product/store link, for example `{Game} in Google Play`, `{Game} in the App Store`, `Play {Game}` or another truthful localized equivalent. This is a functional destination, not a review/source disclaimer.

### Compact descriptor exception
A single short phrase may be used only when all are true:
- it improves orientation;
- it is natural in the resolved locale;
- it is consistent with the business model;
- it does not duplicate nearby navigation or About copy;
- it fits without becoming a sentence/paragraph block;
- any creator claim passes the ownership/developer truth gate.

If no phrase meets those conditions, omit the descriptor entirely.


## 25. CLEAN GAMING CONTENT + LEGAL SEMANTIC EXCLUSION (v4.6.6)

When `clean_gaming_mode = REQUIRED` and `source_gambling_relevance = NONE`, content generation must treat casino/gambling/betting semantics as **out-of-scope concepts**, not as disclaimer topics.

### Content rule

Do not mention or compare the game/site to:
- casinos;
- gambling products;
- betting or bookmakers;
- wagering or real-money stakes;
- slot/poker gambling products;
- responsible-gambling frameworks.

This includes reassurance language such as `this is not gambling`, `we are not a casino`, `there are no bets`, `no real money is involved` or localized equivalents. If the topic is absent from the product, silence is more accurate than denial.

Normal game mechanics must remain described on their own terms. Features such as scores, bonuses, random variation, rewards, progression, collectibles or difficulty changes must **not** be reframed using casino/betting vocabulary unless the authoritative source materially requires that interpretation.

### FAQ rule

Do not invent questions such as:
- `Is this gambling?`
- `Is this a casino game?`
- `Can I bet real money?`
- locale equivalents of those questions.

A FAQ answers real product/support questions; it does not introduce irrelevant risky verticals.

### Legal rule

Privacy, Terms and Cookies describe the actual site/runtime. They must not contain speculative clauses about:
- gambling;
- casino operations;
- wagering;
- betting;
- responsible gambling;
- real-money gaming;

when those activities are absent.

Do not add such language merely as a broad legal disclaimer or template precaution. Unknown/unrelated verticals are omitted rather than denied.

### Source conflict handoff

If authoritative source evidence materially indicates gambling/casino/betting/wagering/real-money stakes while the project is configured as clean gaming:

```text
SOURCE_VERTICAL_CONFLICT
→ STOP CONTENT GENERATION
→ INPUT_REQUIRED
```

Do not rewrite, euphemize or conceal the conflicting source facts.



## 26. FOOTER BOTTOM-BAR UTILITY MICROCOPY RESOLVER (v4.6.7)

When the footer composition has a secondary bottom-bar text slot, generate one **short useful locale-native phrase** instead of decorative filler.

Input:

```text
GEO
locale
business_model_mode
site_topic
privacy_runtime_profile
support_profile
brand_tone
```

Eligible semantic families:
- `PRIVACY_RESPECT` — only when wording is compatible with the actual privacy/runtime model;
- `SUPPORT_ORIENTATION` — short orientation toward help/contact;
- `PRODUCT_ORIENTATION` — concise product/game context;
- `BRAND_SERVICE_NOTE` — restrained service/quality-of-information note that does not make unverifiable claims.

Constraints:
- natural regional language;
- usually one short sentence or phrase;
- no security guarantees;
- no `your data is fully protected`, `100% secure`, certification or compliance claims unless actually verified and necessary;
- no legal boilerplate;
- no independent-review/editorial positioning in `OFFICIAL_GAME_STUDIO`;
- no duplicated About/mission paragraph;
- no SEO keywords stuffed into the phrase.

Example calibration for `pl-PL`:
`Szanujemy Twoją prywatność.` may be used when the site's actual privacy/runtime behavior supports that statement.

Do not reuse one exact phrase across every site/GEO as a factory signature. Generate/select from a locale-natural role-safe pool.

Expose the chosen value through:

```text
footer.bottom_bar.utility_phrase
```

If no useful truthful phrase is available, omit the second text slot rather than insert an icon or filler.


## 25. STUDIO-FIRST BUSINESS COPY ENGINE (v4.6.6)

For `OFFICIAL_GAME_STUDIO`, copy generation starts from a business story, not from an SEO article outline.

### 25.1 Content Bible additions

Before copy, record:

```text
studio_brand
game_name
business_model_mode
developer_relationship_status
studio_voice_person = FIRST_PERSON_PLURAL when allowed
commercial_goal = PROMOTE_GAME
primary_conversion = PLAY_OR_DOWNLOAD_GAME
core_product_promise[]
source_confirmed_game_systems[]
studio_story_topics[]
development_story_topics[]
creator_intent_evidence[]
team_fact_state
actual_development_events[]
design_problem_candidates[]
unsupported_history_blacklist[]
```

### 25.2 First-party copy hierarchy

Prioritize these content classes:

```text
1. STUDIO / PRODUCT IDENTITY
2. PRODUCT PROPOSITION
3. DEVELOPMENT / DESIGN WORK
4. MECHANICS / LEVEL / ART / CONTROLS EXPLANATION
5. PLAYER-VISIBLE OUTCOME
6. PRODUCT PROOF / SUPPORT
7. PLAY / DOWNLOAD CONVERSION
8. PLAYER GUIDANCE / FAQ where useful
```

A generic guide/article voice is lower priority and should not dominate a first-party studio site.

### 25.3 Development narrative units

Build rich process copy from reusable truth-safe units:

#### A. Verified development event
Use only with owner/source evidence:
```text
context
challenge/event
team response
decision/implementation
result/learning
```

#### B. Design challenge explanation
May be derived from confirmed product behavior without pretending to be a historical event:
```text
design problem or constraint
what the system needs to achieve
implementation principle
how the mechanic/level/control expresses it
player-visible outcome
what is evaluated/refined at a high level
```

#### C. System deep dive
```text
system purpose
inputs/rules
state changes
feedback/readability
interaction with other systems
player consequence
related development topic
```

#### D. Production-stage explanation
When exact chronology is not known, present a **development framework**, not fake history:
```text
concept definition
core-loop prototyping
system integration
content/level construction
art/readability pass
balancing/testing
release/support
```

Wording must avoid asserting that these exact stages happened in this exact order unless evidence supports it.

### 25.4 Team voice

When first-person creator claims are allowed:
- `our team` / locale equivalent is allowed as an aggregate studio voice;
- describe shared product/design work without inventing individuals;
- use phrases like `our approach`, `we focus on`, `we designed the system to...` only when the claim is supported by owner/source evidence or clearly framed as a current product principle;
- named people, job titles, departments, quotes, team size and responsibility maps require owner-supplied/verified facts.

Do not generate fake employee profiles to make the site feel like a company.

### 25.5 Page copy blueprints

#### Home
Mix:
- studio/product opening;
- concise game explanation;
- development/design spotlight;
- one or two system deep dives;
- studio/team approach;
- proof/support;
- play/download conversion.

#### Game / Product
Focus on:
- what the game is;
- core loop;
- modes/features/platform;
- player experience;
- how product systems connect;
- store/play CTA.

#### Development
Focus on:
- high-level creation story;
- design challenges;
- systems built/refined;
- process stages supported by evidence;
- testing/refinement principles;
- links to mechanic/level/art pages;
- finished product CTA.

#### Mechanics / Levels / Controls / Art
Each page should explain a **different part of the work** and connect technical/product choices to the player's experience.

#### About / Studio
Focus on:
- studio identity;
- game relationship;
- creative/product principles;
- aggregate team approach;
- support/contact;
- product continuation.

### 25.6 Promotion without ad-copy spam

Product promotion is expected, but avoid every paragraph becoming a sales pitch. A healthy rhythm is:

```text
EXPLAIN WORK
→ SHOW PRODUCT RESULT
→ CONNECT TO PLAYER VALUE
→ CTA AT NATURAL DECISION POINT
```

Use multiple contextual CTA phrasings across pages; do not repeat one button sentence everywhere.

### 25.7 Business-model drift blacklist

For resolved official studio sites, reject public wording equivalent to:
- independent guide/review;
- editorial portal about the game;
- `according to the developer` when speaking about ourselves;
- `we reviewed the game`;
- generic buyer-guide language;
- article-library framing as the site's main identity;
- synthetic player voices presented as trust.


## 27. CONTENT → VISUAL SEMANTIC BRIEF HANDOFF (v4.6.8)

Content generation must describe what the visual needs to communicate before the Visual Engine chooses/generates an asset.

For every meaningful non-legal section, append to the section content plan:

```text
section_heading_meaning
paragraph_cluster_summary
key_entities[]
key_action_or_state
studio_or_player_value
visualizable_concept
visual_job
visual_must_show[]
visual_must_not_imply[]
micro_icon_opportunities[]
small_diagram_opportunity
```

### Visual brief quality

A valid `visual_job` is specific enough that a reviewer can explain why the image belongs beside this copy.

Weak:
```text
game image
studio image
nice development visual
```

Strong:
```text
show the relationship between rising challenge, checkpoints and heat-management pressure without inventing UI or unseen mechanics
```

### Paragraph-cluster rule

Visuals attach to coherent paragraph clusters, not to arbitrary word count. Several paragraphs that explain one idea may share one dedicated visual. A new section/topic with materially different meaning requires a new visual answer or a deliberately different micro-visual/diagram treatment.

### Icon opportunity rule

When content contains 3+ parallel concepts, stages, mechanics, support methods or facts, evaluate whether a small icon family or diagram improves scanning. Do not automatically convert every bullet into an icon.

### Truth boundary

The visual brief must not request imagery that fabricates:
- real team members;
- real office/studio facilities;
- documentary prototypes;
- tools/engine/code screens;
- historical events;
- unreleased game content;
- verified awards/reviews/metrics

unless owner/source evidence supports them.




## 28. TEAM / COMPANY / WORKFLOW CONTENT ENGINE (v4.6.9)

This module is authoritative for rich `OFFICIAL_GAME_STUDIO` builds after the creator/developer truth gate passes.

### 28.1 Core editorial premise

The site tells the story of a company building a product.

The dominant subject is not:

```text
WHAT THE GAME HAS
```

It is:

```text
WHO WE ARE
→ WHAT OUR TEAM IS RESPONSIBLE FOR
→ WHAT PROBLEM / TASK WE ARE WORKING ON
→ HOW WE APPROACH IT
→ HOW WE REVIEW / REFINE IT
→ WHAT RESULT APPEARS IN THE GAME
```

### 28.2 Mandatory page opening content

For every key non-legal page, the first two meaningful content clusters must include at least two distinct roles from:

```text
COMPANY_CONTEXT
TEAM_APPROACH
TASK_BREAKDOWN
DESIGN_DECISION
WORK_IN_PROGRESS
CROSS_DISCIPLINE_COLLABORATION
```

A page that begins with only a store-listing paraphrase is not valid for this branch.

### 28.3 Mandatory middle content

The middle of the page must include at least one distinct work/process role:

```text
PROTOTYPE_OR_ITERATION
REVIEW_AND_QA
DESIGN_DECISION
IMPLEMENTATION_PRINCIPLE
HANDOFF_BETWEEN_DISCIPLINES
PRODUCT_OUTCOME
```

### 28.4 Lower product explanation

Game/product detail belongs lower in the page and should be voiced as a result of the studio's work.

Prefer creator framing such as:
- what we wanted this system to achieve;
- how we shaped the player-facing result;
- what we review when tuning this mechanic;
- what a level needs to communicate;
- how visual hierarchy supports decisions;
- how the final product expresses the design goal.

Historical cause claims still require evidence.

### 28.5 Business-story content matrix

Across the site, distribute distinct material from:

```text
COMPANY
- what the studio exists to build
- product focus
- quality principles
- how disciplines collaborate

TEAM
- aggregate team responsibility
- design / art / level / QA / support disciplines
- review and handoff logic
- collective decision-making principles

WORK
- active task definition
- constraints
- acceptance criteria
- trade-offs
- review checkpoints

DEVELOPMENT
- concept framing
- system design
- prototyping at a truthful level
- iteration logic
- implementation principle
- QA / balancing / readability review
- release readiness

PRODUCT
- game loop
- mechanics
- levels
- visuals
- player experience
- support
- play/download
```

### 28.6 Team details boundary

Allowed after relationship confirmation:
- `our team`;
- `we design`;
- `we review`;
- `we refine`;
- `we test`;
- `we build`;
- aggregate discipline references.

Requires owner/source evidence:
- named employees;
- exact job titles attached to real people;
- headcount;
- office location as workplace fact;
- biographies;
- personal quotes;
- exact internal chronology;
- exact tools/engine;
- exact sprint/task history;
- exact test numbers.

When those facts are unavailable, write about the work model and design logic, not invented biographies.

### 28.7 Compact information method — ~30% less visible prose

Current word envelopes are approximately `0.70×` the v4.9.12 high-density defaults. Preserve information gain while removing repetition, long connective prose and duplicated marketing explanation.

Add depth through:

```text
problem definition
decision criteria
trade-off explanation
workflow step
review condition
failure mode to avoid
player-visible consequence
cross-discipline dependency
quality check
related next step
```

Do not add depth through:
- repeating the hero thesis;
- generic culture slogans;
- fake agile/sprint jargon;
- invented meetings;
- invented user-test quotes;
- unsupported development drama.

### 28.8 Recommended per-page narrative jobs

`HOME`
company → team → current product mission → work/process → product result → game → conversion.

`GAME / PRODUCT`
product team → product goals → feature prioritization/review → game loop/features → store.

`DEVELOPMENT`
team workflow → task/challenge → iteration → review/QA → finished product.

`MECHANICS`
systems discipline → mechanic problem → tuning criteria → test/review → player-facing mechanic.

`LEVELS`
level-design discipline → level brief → progression planning → balance/readability review → level experience.

`ABOUT / STUDIO`
company identity → team model → disciplines → decision flow → quality principles → product relationship.

`FAQ`
first group about studio/work/process; second group about game/product/support.

`CONTACT`
communication ownership → support workflow → what information helps → channels → privacy/legal.

### 28.9 Content-depth failure

If a key official-studio page has:
- fewer than two team/company/process roles in the opening half;
- no work/process role in the middle;
- only game facts and CTA;
- old pre-v4.6.9 word depth without an explicit source limitation;

then mark `CONTENT_MODEL_FIX_REQUIRED`.



## 29. CONTENT-TO-COMPOSITION DEPTH HANDOFF (v4.7.0)

Copy depth must inform visual/composition planning.

### Section depth metadata

For each meaningful section append:

```text
visible_word_estimate
paragraph_count
subtopic_count
visual_support_need
visual_support_reason
eligible_visual_forms[]
text_only_rationale_if_any
```

### Visual support need

A section with several distinct subtopics should not automatically become a card grid.

Evaluate:
- photo/documentary-style conceptual scene;
- diagram;
- annotated workflow;
- comparison;
- timeline;
- editorial inset image;
- image wrap;
- gallery;
- full-width essay.

### Text-only sections

Text-only is valid when:
- the narrative is strong enough;
- full width is intentionally used;
- there is no semantic media worth adding;
- nearby sections already supply sufficient visual rhythm.

Text-only is **not** valid when it merely reflects an unfilled image slot.

### Copy expansion handoff

When page copy increases:
- re-run section break planning;
- re-run media opportunity planning;
- re-run page rhythm planning.

Do not append more paragraphs into the old layout without recomposition.

### Cross-section anti-repeat

Content planning should vary rhetorical structure too.

Do not repeatedly generate:

```text
claim
→ two paragraphs
→ four bullets
```

for most sections.

Mix:
- narrative;
- problem/decision/result;
- comparison;
- process;
- Q&A;
- evidence ledger;
- discipline deep dive;
- annotated example;
- concise manifesto;
- product outcome.
---

## 30. COMPACT COPY POLICY — 0.70 DENSITY (v4.7.1)

The content engine now targets approximately `70%` of the visible prose used by the v4.9.12 high-density profile while preserving useful information roles.

### Current envelopes

```text
HOME                              ~900–1350 visible words
KEY DOMAIN / PRODUCT / DEVELOPMENT ~950–1700
ABOUT / STUDIO                    ~750–1250
FAQ                               ~750–1350 plus meaningful Q&A structure
CONTACT / SUPPORT                 ~525–950
LEGAL                             ~775–1550 when applicable
```

### What to cut first

Reduce:
- repeated thesis statements;
- long introductory framing that is restated later;
- duplicate benefit language;
- generic team/culture slogans;
- filler transitions between sections;
- multiple paragraphs that explain the same consequence;
- CTA prose masquerading as information.

Preserve:
- confirmed facts;
- materially distinct explanations;
- process/workflow logic;
- caveats and boundaries;
- practical user guidance;
- source/provenance context where needed;
- page-specific next steps.

Do not replace removed prose with extra generic cards, bullet padding or FAQ filler merely to maintain visual height.

### Handoff to composition

After copy compaction, every section must expose its new `visible_word_estimate` before layout lock. Composition must reflow to the new volume and may not retain empty geometry sized for the previous longer copy.
