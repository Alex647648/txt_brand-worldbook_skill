# txt_brand-worldbook_skill

A private review repo for a master skill that turns abstract brand positioning into a structured **brand worldbook / visual guideline / multi-page brand deck**.

This skill is designed for tasks such as:
- brand worldbuilding
- brand visual systems
- multi-page visual manuals
- art direction decks
- future-facing brand proposals
- structured prompt generation for multi-image brand presentations

It is **not** a single-image poster prompt skill and **not** a generic branding copy skill. Its job is to help produce a coherent brand universe with clear page roles, consistent visual grammar, and reusable prompt outputs.

---

## What this skill does

The skill helps Claude transform a loose branding request into a complete system that includes:

1. **Brand abstraction**
   - clarify the brand essence
   - identify the core tension pairs
   - define audience, product, and positioning

2. **Visual grammar definition**
   - color system
   - shape language
   - typography mood
   - layout rhythm
   - image treatment
   - material / texture language

3. **Page-structured worldbook generation**
   - 6-page / 8-page / 10-page / 12-page structures
   - clear page-by-page responsibilities
   - prompt-ready outputs for each page

4. **Consistency control**
   - maintain one brand universe across all pages
   - keep visual language coherent across touchpoints
   - avoid style drift between product / packaging / photography / digital / retail

5. **Flexible delivery formats**
   - one-shot master prompt
   - paged prompts
   - design brief
   - bilingual Chinese + English output

---

## Best use cases

Use this skill when the user wants things like:

- “Make me a brand worldbook”
- “Create a multi-page visual system for this brand”
- “Turn this brand idea into a visual guideline deck”
- “I need a future-facing brand proposal with strong art direction”
- “Help me build a brand universe for a consumer tech / luxury / lifestyle / editorial / system brand”
- “Generate prompts for a full brand manual, not just one image”

Especially useful for:
- consumer tech brands
- lifestyle brands
- fashion-tech brands
- cultural / editorial brands
- system / software / protocol brands
- luxury object or accessories brands
- future mobility / speculative product brands

---

## What it should NOT be used for

This skill is usually the wrong tool if the user only wants:

- a single poster prompt
- one logo idea
- naming only
- tagline / slogan only
- one product render without brand system thinking
- narrative storyboards or ad film scripts

---

## Core design philosophy

This skill is built around four high-level mechanisms:

### 1. Tension Pair Engine
Strong brands usually live between two poles, not one flat adjective.

Examples:
- playful ↔ premium
- future ↔ human
- sacred ↔ decadent
- natural ↔ refined
- precise ↔ serene

The skill begins by defining this tension before generating visuals.

### 2. Visual Grammar Table
Instead of vague words like “premium”, “young”, or “futuristic”, the skill translates brand positioning into concrete visual controls:
- colors
- forms
- typography
- layout
- image treatment
- texture
- material cues

### 3. Page Responsibility Locking
Each page must first answer:

> This page exists to show ______.

This prevents every page from becoming the same moodboard with different objects.

### 4. Stable-vs-Variable Ratio
The skill treats brand systems as a balance between:

**Stable elements**
- core worldbuilding
- main color logic
- shape grammar
- typographic tone
- overall art direction

**Variable elements**
- composition
- scene
- touchpoint
- density
- object category
- visual application

This is how it aims to produce outputs that feel coherent without becoming repetitive.

---

## Repository structure

```text
txt_brand-worldbook_skill/
├── README.md
├── SKILL.md
└── references/
    ├── foundations.md
    ├── page-structures.md
    ├── style-branches.md
    ├── consistency-rules.md
    └── output-formats.md
```

### File roles

#### `SKILL.md`
The main entrypoint.
Contains:
- trigger conditions
- overall workflow
- input slots
- advanced mechanisms
- default operating principles
- guidance on when to read supporting references

#### `references/foundations.md`
How to abstract a brand before designing anything.
Focuses on:
- brand essence
- positioning
- tension pairs
- visual abstraction logic

#### `references/page-structures.md`
Defines the supported page systems:
- 6-page
- 8-page
- 10-page
- 12-page

Each structure explains page roles and when to use it.

#### `references/style-branches.md`
Contains the current style branches used to route the skill into different visual directions.

Current built-in branches:
- playful-future-consumer-tech
- luxury-creative-tech
- editorial-fashion-tech
- brutalist-digital-system
- soft-tactile-lifestyle

#### `references/consistency-rules.md`
Explains how to keep outputs from drifting into unrelated sub-brands.

#### `references/output-formats.md`
Defines supported output modes and how they should be structured.

---

## How to use the skill

## Step 1 — Provide the right kind of input

The skill works best when the user provides some combination of:
- brand name
- category / industry
- product or service type
- target audience
- price level
- desired tone
- reference mood
- key touchpoints
- preferred number of pages
- desired output format

You do **not** need every field, but the more clearly the brand tension and touchpoints are described, the better the result.

### Recommended input fields

- **Brand name**
- **Industry / category**
- **Product / service type**
- **Audience**
- **Price positioning**
- **3–5 keywords**
- **1–2 tension pairs** (optional but very helpful)
- **Priority touchpoints**
- **Page count**
- **Output type**

---

## Step 2 — Choose a page count

### 6-page
For quick exploration.

### 8-page
Default recommended format.
Best for a standard brand worldbook.

### 10-page
Better when product, packaging, photography, and retail all need separate treatment.

### 12-page
For large brand universes or pitch-grade worldbuilding.

---

## Step 3 — Choose an output mode

### A. One-shot master prompt
Best for fast image-model exploration.

### B. Paged prompts
Best when generating each spread/page separately.

### C. Design brief
Best for handing off to a designer or creative team.

### D. Bilingual output
Best when strategy is discussed in Chinese but prompt execution happens in English.

---

## Input examples

### Example 1 — Playful future consumer tech

```text
Help me create an 8-page brand worldbook for an AI hardware brand called ANYPLAY.
It makes collectible AI devices for young creators.
The feeling should be playful but premium, futuristic but approachable, colorful but controlled.
Please include product obsession, packaging, editorial photography, retail imagination, and app/social touchpoints.
Output: Chinese overview + English paged prompts.
```

### Example 2 — Contemporary Eastern lifestyle

```text
Help me build a 10-page brand worldbook for a contemporary Chinese lifestyle brand called 山隐之间.
The brand focuses on fragrance, tea objects, home rituals, seasonal gift boxes, and quiet retail spaces.
The tone should feel contemporary Eastern, natural, restrained, poetic, tactile, and refined.
Please include materials, typography rhythm, packaging, scent storytelling, photography, and retail imagination.
Output: Chinese overview + English paged prompts.
```

### Example 3 — Future mobility / space brand

```text
Create a 12-page brand worldbook for AURELIA VECTOR, a premium orbital mobility brand.
The tone should feel Apple-like, aerospace-grade, serene, precise, luxurious but restrained.
Please include industrial design language, interface systems, cabin experience, service layer, retail experience center, and campaign direction.
Output: Chinese overview + English paged prompts.
```

---

## Expected output structure

The skill typically produces outputs in this order:

### 1. One-sentence brand definition
Example:
> AURELIA VECTOR is a future mobility brand living between orbital precision and serene post-automotive luxury.

### 2. Tension pairs
Example:
- precise ↔ serene
- futuristic ↔ trustworthy
- luxurious ↔ restrained

### 3. Visual grammar table
Example categories:
- primary colors
- accent colors
- shape language
- typography mood
- layout rhythm
- image treatment
- texture / material language

### 4. Priority touchpoints
Example:
- product obsession
- packaging exploration
- editorial photography
- retail environment
- digital application

### 5. Structured page system
Each page gets:
- a title
- a purpose statement
- a prompt or brief

---

## Output examples

### Output mode: Chinese overview + English paged prompts

Typical shape:

```text
一、中文概述
- 品牌一句话定义
- 张力对
- 总锚点
- 视觉语法表
- 触点重点

二、英文分页 prompts
- Page 1 — Cover
- Page 2 — Brand Essence
- Page 3 — Color System
- ...
```

### Output mode: Design brief

Typical shape:

```text
- Project summary
- Brand tension pair
- Visual language
- Priority touchpoints
- Recommended structure
- Risks to avoid
```

---

## Style branch behavior

The skill should not use one visual language for everything.
It is expected to route differently depending on the brand.

### Example routing logic
- playful AI device brand → `playful-future-consumer-tech`
- quiet tactile wellness brand → `soft-tactile-lifestyle`
- fashion-technology accessory brand → `editorial-fashion-tech`
- infrastructure / software / system brand → `brutalist-digital-system`
- premium hardware / refined future product → `luxury-creative-tech`

Future versions may add more branches, such as:
- contemporary-eastern-lifestyle
- sacred-maximalist-accessories
- future-aerospace-mobility

---

## Quality bar

A successful output should:

1. clearly define the brand world in one sentence
2. identify real tension pairs
3. convert abstract taste into visual grammar
4. assign distinct responsibilities to each page
5. cover the right touchpoints
6. feel like one coherent brand universe
7. remain directly usable for prompting or creative collaboration

---

## Common failure modes

The skill is failing if it does any of the following:

- repeats the same “premium / futuristic / creative” language without grounding it visually
- makes every page feel like the cover page
- drifts into unrelated aesthetics from one page to another
- confuses worldbuilding with moodboard clutter
- ignores touchpoints like packaging, retail, or interface when they matter
- produces a brand deck that feels like multiple brands stitched together

---

## Review checklist

When reviewing outputs from this skill, ask:

- Did it define the tension pair first?
- Did it produce a usable visual grammar table?
- Did every page have a clear role?
- Did it choose the right visual branch?
- Did the whole output feel like one brand world?
- Could a designer or image model actually use this directly?

---

## Current status

This repository contains the **initial full draft** of the skill architecture, including:
- main skill entry
- supporting references
- page systems
- style branches
- consistency rules
- output modes

It is intended for review and iteration.

### Important note
The skill itself is **still on the current v1 draft**.
A structured optimization proposal has been documented, but **has not been applied to the skill yet**.

See:
- `OPTIMIZATION_PLAN.md`

Current recommended next-step improvements include:
- example outputs
- eval prompts
- anti-pattern examples
- more specialized style branches
- stronger branch routing logic
- stronger per-page writing templates
- a brand archetype layer before style routing
