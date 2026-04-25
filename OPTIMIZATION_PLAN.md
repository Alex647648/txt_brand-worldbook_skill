# Optimization Plan for `txt_brand-worldbook_skill`

This document captures the **recommended v2 optimization plan** for the current skill architecture.

Important: as of this revision, these are **analysis-backed recommendations only**. The skill itself has **not** been modified yet. This document exists so the current version can be reviewed together with the proposed next-step improvements.

---

## Current assessment

The current version of `txt_brand-worldbook_skill` is a strong **v1 architecture draft**.

It already has the right backbone:
- tension pair engine
- visual grammar table
- page responsibility locking
- consistency awareness

However, it is still closer to a **methodology skeleton** than a mature, production-stable brand operating system.

The main opportunities are not cosmetic rewrites, but **structural upgrades**.

---

## Main optimization directions

### 1. Expand the style branch system
The current branch set is too small for the range of brand types already tested.

Current branches:
- playful-future-consumer-tech
- luxury-creative-tech
- editorial-fashion-tech
- brutalist-digital-system
- soft-tactile-lifestyle

Recommended additions:
- contemporary-eastern-lifestyle
- sacred-maximalist-accessories
- future-aerospace-mobility
- quiet-cultural-editorial-luxury
- editorial-luxury-objects
- speculative-premium-industrial

**Why this matters:**
Without enough branches, the skill will keep forcing unrelated brands into the closest available style bucket.

---

### 2. Upgrade `style-branches.md` into a routing document
Right now it behaves more like a style description sheet than a real routing system.

Each branch should eventually include:
- suitable industries / brand types
- common trigger keywords
- core tension pairs
- typical visual signals
- priority touchpoints
- nearby confusing branches
- what it should NOT be mistaken for
- anti-patterns

**Why this matters:**
The skill needs to route deliberately, not guess loosely.

---

### 3. Add a brand archetype / object-type layer
The current flow is roughly:

`brand input → style branch → page output`

This skips a useful middle layer:

`brand input → brand archetype → style branch → page output`

Recommended archetypes:
- object-led
- interface-led
- editorial-led
- ritual-led
- space-led
- mobility-led
- collectible-led
- system-led

**Why this matters:**
This helps the skill distinguish whether it is designing around objects, systems, spaces, rituals, mobility, or interfaces before it chooses a style branch.

---

### 4. Add anti-pattern / failure-mode documentation
The current skill has many positive instructions, but too little explicit protection against common failure modes.

Recommended new file:
- `references/anti-patterns.md`

Suggested coverage:
- cheap toy-tech visual drift
- generic “guochao” template drift
- cosplay-goth / low-end dark ornament drift
- blue startup tech template drift
- cinematic concept-art drift instead of brand-system output
- over-moodboarded but structurally weak output

**Why this matters:**
High-end outputs need both positive direction and negative constraints.

---

### 5. Tighten output format templates
The current output format document explains the available modes, but does not strongly define their minimum required structure.

Recommended improvements:

#### For paged prompts
Require:
- page title
- purpose sentence (`This page exists to show...`)
- visual objective
- touchpoint focus
- prompt
- keep
- avoid

#### For design briefs
Require:
- brand one-liner
- tension pairs
- audience
- visual grammar
- priority touchpoints
- recommended structure
- risks to avoid
- output direction

#### For bilingual mode
Require:
- Chinese strategy overview
- Chinese visual grammar summary
- Chinese page logic
- English prompt output

**Why this matters:**
Without stronger output schemas, results will stay structurally inconsistent.

---

### 6. Add examples and evals
The skill currently explains *how* to think, but it still lacks a formal example and testing layer.

Recommended additions:
- `examples/`
- `evals/evals.json`

Suggested example sets:
- playful future AI hardware
- brutalist digital system brand
- contemporary Eastern lifestyle brand
- sacred maximalist jewelry brand
- future aerospace mobility brand

Each example could include:
- `input.md`
- `expected-output.md`
- `notes.md`

**Why this matters:**
This upgrades the repo from “written framework” to “trainable and reviewable system”.

---

## Recommended priority order

### P0 — highest priority
1. Expand branch coverage
2. Rework branch routing logic
3. Add brand archetype layer

### P1 — next most valuable
4. Add anti-pattern documentation
5. Tighten output schemas
6. Add examples
7. Add eval prompts

### P2 — later refinement
8. Add more specialized touchpoint weighting rules
9. Add per-page writing density guidance
10. Optimize description triggering with formal trigger evals

---

## Proposed file-level changes for v2

### Existing files to update later
- `SKILL.md`
- `references/foundations.md`
- `references/page-structures.md`
- `references/style-branches.md`
- `references/consistency-rules.md`
- `references/output-formats.md`

### New files / dirs recommended later
- `references/anti-patterns.md`
- `references/brand-archetypes.md`
- `examples/`
- `evals/evals.json`

---

## Suggested v2 execution sequence

### Round 1
- add brand archetypes
- expand style branches
- rewrite branch routing logic

### Round 2
- add anti-patterns
- add examples
- tighten output structures

### Round 3
- add evals
- test routing on real prompts
- then optimize triggering description and edge-case handling

---

## Bottom-line conclusion

This skill does **not** need to be rewritten from scratch.

It already has the right foundation.

What it needs is to evolve from:

> a strong brand-worldbook methodology draft

into:

> a routeable, testable, anti-drift brand operating system

That means the next major gains will come from **structure, routing, constraints, and examples**, not from polishing the prose alone.
