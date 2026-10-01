# Site Factory patch — Full-width canvas + compact copy

**Release candidate:** `full-width-canvas-compact-copy-v4`  
**Policy target:** Site Factory v4.9.14  
**Date:** 2026-10-02

## Why this patch exists

A recent build passed earlier composition checks while still rendering major desktop sections as narrow content islands with large functionally empty fields. The existing “no dead space” language was therefore not strict enough at render/QA level.

This patch also replaces the v4.9.12 “+50% content depth” bias with a **~30% visible-prose reduction** while preserving distinct information jobs, factual support and useful structure.

## Precedence

Until this candidate is merged into the seven canonical Project Source bundles, the rules in this file are the authoritative candidate override for the items below. They supersede contradictory older high-density word envelopes and any rule that permits a split/grid track to remain empty.

## 1. Compact-copy baseline — 0.70 density

Normal rich-site visible-copy targets:

```text
HOME                               ~900–1350 visible words
KEY DOMAIN / PRODUCT / DEVELOPMENT ~950–1700
ABOUT / STUDIO                     ~750–1250
FAQ                                ~750–1350 plus meaningful Q&A structure
CONTACT / SUPPORT                  ~525–950
LEGAL                              ~775–1550 when actually applicable
```

These are envelopes, not quotas.

### Cut first

- repeated thesis statements;
- duplicated benefit language;
- long intros repeated later;
- filler transitions;
- generic team/culture slogans;
- repeated source facts without added interpretation;
- CTA prose used as content filler.

### Preserve

- confirmed facts;
- materially distinct explanations;
- workflow/process logic;
- caveats and boundaries;
- practical guidance;
- source/provenance context where needed;
- page-specific next steps.

A lower word count may pass when page jobs are complete. Never add filler to reach a minimum.

## 2. Full useful width is a composition requirement

A section does **not** pass because its background or outer wrapper is `100%` wide. The meaningful composition must use the available desktop canvas.

For ordinary major non-hero sections:

```text
section_shell_inline_usage = FULL
major_section_canvas_coverage target >= 0.78
largest_unassigned_blank_region_ratio target <= 0.22
empty_grid_track_count = 0
reserved_media_slot_without_media = 0
one_sided_blank_field = false
```

Screenshot perception remains final authority.

Readable text measure is separate from section width: body text may remain ~60–75ch, but the section must use its useful width through media, editorial columns, ledger/data, side notes, a centered field, a rail, or another intentional composition.

## 3. Mandatory adaptive reflow

When optional media/secondary content is absent:

```text
REMOVE EMPTY TRACK
→ RECOMPUTE GRID
→ EXPAND / RECENTER MEANINGFUL COMPOSITION
→ RECHECK HEADING MEASURE
→ RECHECK SECTION HEIGHT
→ SCREENSHOT QA
```

Forbidden:
- preserving a 50/50 split with one empty half;
- empty `figure` or grid child used as geometry;
- reserved media wrapper with no asset;
- old min-height/padding retained only to keep the former section height;
- small shared max-width applied to an entire major section instead of only readable text.

## 4. Copy compaction must not become whitespace

After the ~30% copy reduction:
- recompute section height;
- do not enlarge H2/H1 just to refill space;
- do not add padding to retain previous height;
- re-evaluate image size/placement;
- tighten section rhythm where useful;
- use newly available room for stronger media/hierarchy only when semantically justified.

Shorter copy should create a tighter and cleaner composition, not a smaller island in the same oversized frame.

## 5. Bundle application map

### 01-CORE-GOVERNANCE.md
- bump policy/master target to v4.9.14;
- replace the v4.9.12 “+50%” prose-growth bias with `COMPACT_070`;
- add the full-useful-width contract;
- add `WIDTH-001`, `WIDTH-002`, `REFLOW-001`, `COPY-030`.

### 02-DESIGN-SYSTEM-BUNDLE.md
- separate readable text measure from section-canvas usage;
- require full useful shell for major sections;
- add coverage/blank-region diagnostics;
- require no-media track collapse;
- add text-only full-width alternatives.

### 03-SITE-WORDPRESS-RUNTIME.md
Per major section record:
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
Runtime must collapse empty tracks before final HTML/CSS.

### 04-CONTENT-LEGAL-CONTACT.md
- use the 0.70 density envelopes above;
- preserve information roles while removing repetition/filler;
- expose `visible_word_estimate` before composition lock.

### 05-SEO-GLOBAL-TEXT.md
SEO metadata rules remain intact. The 30% reduction applies to visible page prose, not to shortening title/meta fields below their SEO intent/quality requirements.

### 06-VISUAL-ENGINE.md
- recalculate media rhythm after copy compaction;
- normal key-page planning envelope: ~950–1700 visible words;
- useful visual pacing reference: roughly one meaningful visual moment per ~300–450 visible words where semantics support it;
- never convert reduced copy into larger empty shells.

### 07-QA-RELEASE.md
Add a blocking full-width/copy-density gate using the thresholds above and screenshot review at laptop, normal desktop and wide desktop widths.

## 6. Regression gates

### WIDTH-001 — one-sided empty field
Major section content sits in a narrow side island while the opposite field has no declared function.  
**Result:** FAIL.

### WIDTH-002 — false full-width
Outer section is full width but an unnecessarily narrow inner wrapper caps the whole major composition.  
**Result:** FAIL.

### REFLOW-001 — empty track survives
Optional media/secondary content disappears but its grid/flex track or reserved shell remains.  
**Result:** FAIL.

### COPY-030 — compact-copy regression
Rich page materially exceeds the compact envelope without documented information need, or reaches length through repetition/filler.  
**Result:** FIX_REQUIRED.

## 7. Mandatory reflow test

At least one representative section must be tested with optional media unavailable:

1. remove/disable optional asset;
2. render;
3. require the media track to disappear;
4. require content width/alignment to recompute;
5. require section height to shrink/recompose;
6. require no one-sided blank field.

## 8. Final screenshot question

Before composition/release PASS:

> If the screenshot is viewed without reading the copy, does each major section use the available page width as an intentional composition rather than a small block floating in empty space?

If **no** → `FIX_REQUIRED`.
