# Loewy: beauty, taste, and the decision to ship

Loewy is a brand-agnostic visual critique skill. It evaluates whether a design is clear, restrained, well-proportioned, carefully made, emotionally persuasive, and appropriately balanced between novelty and familiarity. Its output is a first-impression diagnosis, an eight-part scorecard, a short narrative critique, seven ranked changes, and a SHIP / REFINE / REBUILD verdict.

The distinguishing concept is **MAYA: Most Advanced Yet Acceptable**. The skill asks whether the work is fresh enough to attract attention while remaining recognizable and credible to its intended audience.

This README analyzes [Loewy.skill](../../Loewy.skill), including its rubric, output rules, and known ambiguities. Illustrative calculations and prompts are documentation examples, not results of a live critique. Where this README recommends a convention for an undefined case, it labels that convention explicitly.

## Contents

- [Package contents](#package-contents)
- [What the skill does and does not do](#what-the-skill-does-and-does-not-do)
- [Setup and invocation](#setup-and-invocation)
- [The minimum useful context](#the-minimum-useful-context)
- [The doctrine behind the review](#the-doctrine-behind-the-review)
- [The review sequence](#the-review-sequence)
- [The eight scoring dimensions](#the-eight-scoring-dimensions)
- [Composite scores and verdict rules](#composite-scores-and-verdict-rules)
- [The seven moves](#the-seven-moves)
- [Required output format](#required-output-format)
- [Understanding MAYA](#understanding-maya)
- [Example prompts](#example-prompts)
- [Using the critique in an iteration](#using-the-critique-in-an-iteration)
- [Analysis: strengths and limitations](#analysis-strengths-and-limitations)
- [Known packaging issue](#known-packaging-issue)
- [Troubleshooting](#troubleshooting)
- [Comparison with the other skills](#comparison-with-the-other-skills)
- [Output checklist](#output-checklist)

## Package contents

The `.skill` file is a ZIP archive with one Markdown file:

```text
Loewy.skill
└── loewy/
    └── SKILL.md
```

The internal name is `loewy`. The instructions contain the persona, context questions, doctrine, review sequence, scorecard, output template, rules of engagement, and a short historical appendix.

There are no bundled scripts, design assets, image references, external integrations, or automatic scoring functions. The historical appendix is inside `SKILL.md`; there is no separate reference directory.

The current file also contains **two consecutive front-matter-style metadata blocks**. See [Known packaging issue](#known-packaging-issue) for the practical implications.

## What the skill does and does not do

Loewy is intended for logos, wordmarks, icons, posters, social graphics, ads, decks, websites, app screens, packaging, product forms, illustrations, data visualizations, and other compositions.

It is particularly useful for questions such as:

- Is this tasteful or merely polished?
- Is there too much decoration?
- Is the composition too safe or too strange for its audience?
- What should be removed before this ships?
- Is the current concept worth refining, or does it need rebuilding?
- Which strong choice must survive the next revision?

The skill explicitly excludes brand guideline enforcement, brand voice review, and copy correctness. It may flag a suspected issue in those areas and hand it back, but it is not a replacement for the relevant review.

Its release verdict concerns visual taste and effectiveness. It does not certify accessibility, functionality, legal clearance, factual accuracy, production readiness, or audience performance. A visually strong screen can still have broken interactions; a beautiful poster can still contain an incorrect date.

## Setup and invocation

Import [Loewy.skill](../../Loewy.skill) in a host that supports packaged skills. The repository does not supply installation tooling or verified compatibility information.

To inspect or extract it from the repository root:

```sh
unzip -l Loewy.skill
unzip Loewy.skill -d ./extracted
```

For a directory-based assistant, follow its installation procedure using the extracted `loewy/` folder. Extraction does not automatically register the skill.

A host-independent request is:

```text
Use the loewy skill to critique the attached design.
Follow its scorecard, seven moves, and final verdict format.
```

Some hosts may expose `/loewy` after installation. The slash command is not a program supplied by the archive, and its availability depends on the host.

The metadata contains triggers around beauty, taste, elegance, generic design, design QA, critique, and pre-export review. Automatic activation depends on how the host discovers and selects skills.

## The minimum useful context

The skill asks for just three kinds of context, using no more than one short clarification round when necessary:

| Context | Purpose |
| --- | --- |
| What is the artifact, and where will it appear? | Establishes medium, output size, viewing conditions, and screen versus print constraints. |
| Who is the audience, and what should they think, feel, or do immediately? | Establishes the intended emotional and communicative response. |
| What category or competitive set is familiar to that audience? | Calibrates how much novelty the design can support. |

If no artifact is supplied, the skill requests one or a description. If the user asks to proceed without more context, it says to state assumptions and judge the work rather than blocking on a perfect brief.

A visible image or render is preferable for detailed visual judgment. A description can support conceptual feedback but cannot establish whether the real file has clean edges, consistent kerning, or suitable contrast. A link is only useful if the host can access and render its contents; the skill itself supplies no browsing capability.

## The doctrine behind the review

Seven principles guide the critique:

1. **Beauty through function and simplification.** The appearance should express what the thing does, rather than conceal a weak structure with decoration.
2. **Simplicity as a deciding factor.** Remove what is unnecessary while preserving function and meaning.
3. **MAYA.** Balance the attraction of novelty with the trust of familiarity.
4. **Respect for attention.** Avoid making an already demanding experience harder to understand.
5. **Beauty as persuasive value.** Visual quality can contribute to desirability and confidence.
6. **Honesty of form.** Let the look serve the content instead of dressing it in an unrelated style.
7. **Educated intuition.** Use the rubric to organize judgment, without pretending the numbers replace the eye.

These are the skill's design beliefs, not experimentally verified outcomes of this package. For example, a claim that a change will increase sales would require evidence beyond a taste review.

## The review sequence

### Step 0: establish context

Identify the medium, audience response, and category expectations. Ask only for what is missing, or state assumptions if the user wants an immediate judgment.

### Step 1: the one-second test

Before detailed analysis, capture three impressions:

- What does the artifact read as?
- What emotional quality does it communicate?
- Where does attention go first, and is that the intended destination?

This is a first-impression heuristic. The package does not implement a timed exposure study or eye tracking. Its value is to keep the review from overlooking an unclear overall impression while becoming absorbed in detail.

### Step 2: score the eight dimensions

Assign 0–10 to each dimension, anchor the scores to visible evidence, calculate a composite, and identify the lowest dimension. The source reserves 9–10 for exceptional work and notes that most drafts are expected to fall around 4–7.

### Step 3: write the teardown

Produce two to four concise paragraphs covering the underlying problem, unearned decoration or complexity, MAYA placement, audience aspiration and anxiety, and any brave idea worth protecting.

Audience feelings are hypotheses inferred from the design and context. The review should not imply it has interviewed the audience unless that evidence is actually supplied.

### Step 4: prescribe seven moves

Give exactly seven concrete changes ranked by impact. Each includes the change, the principle, and the expected payoff. At least half must remove or simplify.

### Step 5: make the verdict useful

Choose SHIP, REFINE, or REBUILD, explain why in one line, identify the single most valuable change, and state what must not be disturbed.

## The eight scoring dimensions

| Dimension | What it measures | Weak evidence | Strong evidence |
| --- | --- | --- | --- |
| **Instant legibility** | Whether the primary form or message reads quickly. | The viewer must decode the composition. | The purpose is unmistakable at a glance. |
| **Simplicity / restraint** | Whether unnecessary elements remain. | Clutter and defensive additions. | Removing more would damage meaning or function. |
| **Hierarchy and focus** | Whether there is one thesis and a clear attention path. | Multiple elements compete equally. | Primary and supporting information resolve effortlessly. |
| **Honesty of form** | Whether the look expresses the content. | An unrelated style covers a weak core. | The visual form makes the argument itself. |
| **Proportion, spacing and rhythm** | Whether relationships are deliberately tuned. | Cramped, uneven, arbitrary spacing or ratios. | Deliberate rhythm and productive tension. |
| **Craft and finish** | Whether execution is resolved. | Misalignment, muddy details, obvious seams. | Consistent, precise visual execution. |
| **MAYA calibration** | Whether novelty fits category expectations. | Either derivative invisibility or alienating novelty. | A fresh but credible advance. |
| **Emotional tone / desire** | Whether the work creates the intended feeling. | Neutrality, generic tone, or an off-putting impression. | A compelling emotional signal relevant to the audience. |

The score bands within each dimension are:

| Score | Band |
| --- | --- |
| 0–3 | Fails |
| 4–6 | Competent |
| 7–8 | Good |
| 9–10 | Exceptional |

These dimension bands differ from the final verdict thresholds. A dimension of 6 can be “competent” while still contributing to an overall REBUILD result if the average is below 6.

Unlike Creative Direction, Loewy does not expressly allow omitting inapplicable dimensions. If evidence is insufficient, identify the limitation and any provisional judgment instead of presenting an unsupported score as an observation.

## Composite scores and verdict rules

The prescribed composite is the mean of all eight dimensions, displayed to one decimal place:

```text
Composite = sum of the eight scores / 8
```

The source uses approximate thresholds for SHIP and REFINE:

| Verdict | Packaged rule | Required interpretation |
| --- | --- | --- |
| **SHIP** | Composite approximately 8.0 or higher, with no dimension below 7. | Strong overall quality with no weaker dimension hidden by the average. |
| **REFINE** | Composite approximately 6.0–7.9. | The idea is sound; the top three changes should address the main weaknesses. |
| **REBUILD** | Composite below 6.0, **or any dimension at 3 or below**. | A fundamental weakness prevents a polish-only solution. |

The rules also allow the critic to explain a disagreement between the numbers and visual judgment. This is not permission to silently ignore the rubric; the reason should be explicit.

### Worked examples

These are invented score sets to explain the rules:

| Scores | Raw mean | Display | Result |
| --- | --- | --- | --- |
| 8, 8, 8, 8, 8, 8, 8, 8 | 8.0 | 8.0 | SHIP meets both the mean and minimum-score condition. |
| 7, 7, 7, 7, 7, 7, 7, 7 | 7.0 | 7.0 | REFINE. |
| 5, 5, 5, 5, 5, 5, 5, 5 | 5.0 | 5.0 | REBUILD because the mean is below 6. |
| 9, 9, 9, 9, 9, 9, 9, 3 | 8.25 | 8.3 | REBUILD because one dimension is 3, despite the high mean. |
| 9, 9, 9, 9, 9, 9, 9, 6 | 8.625 | 8.6 | Does not meet SHIP's minimum-score condition; see the gap below. |

The displayed examples use conventional half-up rounding. The package does not define how exact rounding ties must be handled, so an implementation should disclose its convention if it matters.

### An uncovered verdict case

An average above 8 with a lowest dimension of 4–6 is not fully classified by the written ranges: it fails the SHIP floor but is above the stated REFINE range and does not necessarily trigger REBUILD.

**Recommended interpretation, not an existing package rule:** use REFINE and explicitly identify the dimension preventing SHIP. This is consistent with requiring all dimensions to reach at least 7 before approval, but the source should ideally state the rule directly.

Similarly, apply verdict reasoning to the unrounded mean before displaying one decimal, or explain why an approximate boundary is being used. The package's approximate symbols mean these thresholds should not be presented as a rigorously specified automated classifier.

## The seven moves

Each move has three parts:

| Part | Function |
| --- | --- |
| **Move** | The exact edit to make. |
| **Principle** | The design doctrine it serves. |
| **Payoff** | The perceptual or communicative improvement expected. |

With seven moves, “at least half” means **at least four should remove or simplify**. Simplification can mean consolidating typographic roles, reducing competing colors, or eliminating a redundant treatment; it need not mean deleting essential information.

An illustrative move is:

```text
Remove the second outline around the headline — simplicity and restraint —
restores one clear dominant shape at thumbnail size.
```

A weak move is “make it cleaner,” because it does not identify an edit or explain the result.

The fixed count can encourage unnecessary recommendations on already resolved work. A useful review should distinguish essential fixes from minor refinements and avoid inventing faults merely to fill seven positions. The package still asks for exactly seven; it does not provide an exception for small artifacts.

## Required output format

The source specifies this shape:

```text
◤ LOEWY — BEAUTY & TASTE REVIEW ◢

ONE-SECOND VERDICT
<first impression>

SCORECARD
1. Instant legibility     x/10
2. Simplicity / restraint x/10
3. Hierarchy & focus      x/10
4. Honesty of form        x/10
5. Proportion & rhythm    x/10
6. Craft & finish         x/10
7. MAYA calibration       x/10
8. Emotional tone         x/10
COMPOSITE: x.x/10   ·   Weakest link: <dimension>

THE TEARDOWN
<2–4 paragraphs>

THE 7 MOVES (ranked)
1. <move> — <principle> — <payoff>
2. ...
3. ...
4. ...
5. ...
6. ...
7. ...

VERDICT: SHIP / REFINE / REBUILD — <rationale>
THE ONE THING: <highest-impact change>
DON'T TOUCH: <what should survive revision>
```

The first verdict is an immediate impression, while the final verdict is the considered decision. They serve different purposes and need not use identical wording.

## Understanding MAYA

MAYA requires context. An experimental cultural poster and an everyday payment interface face different expectations, even if both benefit from clarity and craft.

A practical way to read this dimension is to separate two questions:

1. What familiar cues make the artifact intelligible and credible in its category?
2. What distinct choice advances it beyond the expected template?

A hypothetical poster might preserve an easily read event title and conventional logistics while expressing the concept through an unexpected image. A hypothetical interface might preserve recognizable controls while using a distinctive but restrained visual hierarchy.

These examples illustrate the principle rather than prescribe a universal style. The source itself warns that “the audience is not ready” can become an excuse for excessive caution. It asks for the advanced edge of acceptability, not a retreat into the safest middle.

The appendix also warns against borrowing streamlined curves or other historical styling where they do not fit the content. Loewy's name should not become an instruction to make every design resemble a vehicle or a mid-century product.

## Example prompts

### Final poster review

```text
Use loewy to review the attached poster before export.
It will be printed at A2 and adapted for mobile social viewing.
The audience is the general public. The first impression should be
confident and welcoming, and the event name must read immediately.
The category is local cultural events.

Use the full output format. Give seven ranked moves, identify the
weakest dimension, and state what must remain unchanged.
```

### A critique with limited context

```text
Use loewy on this screenshot. Just judge it with the context available.
State your assumptions briefly and mark anything you cannot verify
from the image. Focus on hierarchy, restraint, proportion, and MAYA.
```

### Diagnose excessive novelty

```text
Use loewy to review this landing page for first-time customers.
The category is household maintenance services. People should feel
that booking is straightforward and the service is dependable.

Assess whether the unusual type and navigation feel distinctive or
unfamiliar enough to undermine confidence. Anchor the judgment to
visible evidence, and do not claim actual user-test results.
```

### Compare revisions

```text
Use loewy to review version B, with version A attached for comparison.
Keep the same audience and category assumptions. Use the full rubric
for B, then explain which changes improved or weakened the design.
Protect the strongest original idea and identify any new clutter.
```

## Using the critique in an iteration

Begin with the final verdict and weakest dimension, then read the teardown to understand the cause. Use THE ONE THING to choose the first edit. Read DON'T TOUCH before making changes so the revision does not erase the work's strongest choice.

For REFINE, the source points toward implementing the top three moves. For REBUILD, it should identify what to keep and what to restart; otherwise “rebuild” is too vague to guide production.

For SHIP, the remaining recommendations should not become an invitation to endlessly decorate the piece. The instructions explicitly value protecting resolved work from unnecessary changes.

When comparing revisions, keep the brief constant. A changed audience or category changes MAYA calibration, making score changes difficult to interpret. Scores are structured critical judgments, not objective measurements of improvement.

## Analysis: strengths and limitations

### Strengths

- **First impression comes before detail.** This helps prevent excellent craft from masking a weak overall read.
- **The minimum-score condition matters.** SHIP requires more than an attractive average.
- **Subtraction is operationalized.** The majority simplification requirement makes restraint actionable.
- **It protects successful choices.** DON'T TOUCH gives the next revision a boundary.
- **It treats novelty as contextual.** MAYA adds audience and category expectations to taste judgment.
- **It distinguishes the person from the work.** The rules explicitly reject contempt toward the maker.

### Limitations

- Numerical scores depend on the assistant; the package contains no scoring implementation or reproducibility mechanism.
- Some verdict edge cases and rounding behavior are undefined.
- Visual taste can be culturally and contextually variable, despite the persona's confidence.
- A static screenshot cannot substantiate functional, accessibility, print-production, or behavioral claims.
- The fixed seven-move count may exceed the useful number of changes for a small, strong artifact.
- The historical appendix lists works and quotations without a source bibliography. Verify attribution before quoting or publishing historical claims.
- A strong bias toward reduction must be balanced against required content and the needs of complex information.

The appendix acknowledges limits to commercial success as a design yardstick, including cultural, ethical, and experiential value. A review should preserve that nuance instead of equating desirability with sales performance.

## Known packaging issue

`loewy/SKILL.md` starts with a quoted `name` and `description` metadata block, followed by another front-matter-style block repeating those fields before the main heading.

This is redundant. A host may parse only the first block and treat the second as body text; other handling is host-specific. The package was inspected as text for this documentation, but its installation behavior has not been tested across assistants.

A reasonable maintenance fix would be to retain one canonical metadata block and remove the duplicate while preserving the instructional body. **This documentation change does not alter or repack the original archive.** Users comparing package hashes can therefore review the READMEs independently of a future packaging fix.

## Troubleshooting

| Problem | Likely cause | Useful correction |
| --- | --- | --- |
| An 8+ average gets SHIP despite a dimension of 6. | The minimum-score condition was overlooked. | Ask for the verdict to account for the below-7 dimension explicitly. |
| A score of 3 is hidden by stronger scores. | The rebuild override was missed. | Apply the any-dimension-at-or-below-3 rule. |
| MAYA feedback is generic. | No audience or category context. | Supply examples of what the audience already expects. |
| The critique adds more decoration. | The subtraction requirement was ignored. | Require at least four removing or simplifying moves. |
| The review rewrites the copy or enforces brand rules. | The skill has drifted from its scope. | Separate those tasks and keep this review about taste. |
| The critique sounds insulting. | Persona language has overridden the engagement rules. | Require evidence-based criticism of the artifact, never the maker. |
| The host displays duplicated metadata. | The packaged file contains two blocks. | Inspect the known issue; use the first block as the canonical metadata if maintaining a local copy. |

## Comparison with the other skills

Choose Loewy for a final taste judgment or a disciplined refinement review. Choose [Casey](../casey/README.md) for conceptual metaphor and typographic meaning. Choose [Creative Direction](../creative-direction/README.md) for three new concepts, adjustable critique intensity, or a three-move elevation pass.

The frameworks are complementary, but their scores and verdicts are not interchangeable. In particular, Creative Direction's SHIP intensity is not Loewy's SHIP verdict.

## Output checklist

A faithful Loewy review includes:

- The initial read, emotional impression, and attention destination.
- Eight evidence-based scores on the 0–10 scale.
- A correctly calculated mean and the weakest dimension.
- Two to four paragraphs of narrative diagnosis.
- Exactly seven ranked moves, each with a principle and payoff.
- At least four moves that remove or simplify.
- A verdict that respects the minimum dimension and rebuild override.
- An explanation for any rubric ambiguity or judgment-based departure.
- THE ONE THING and DON'T TOUCH.

---

[Back to repository overview](../../README.md)
