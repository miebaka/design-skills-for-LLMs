# Loewy

Loewy provides a final visual-taste and refinement review. It evaluates clarity, form, restraint, emotional tone, craft, and MAYA—Most Advanced Yet Acceptable—before recommending SHIP, REFINE, or REBUILD.

The skill is inspired by Raymond Loewy's emphasis on function and simplification. It does not impersonate him or present subjective judgments as his personal verdict.

## What changed in version 2

The original skill used eight 0–10 scores and a one-decimal average. That created false precision, contained an uncovered verdict case, and allowed subjective emotional judgments to look as measurable as visible alignment problems. It also treated a one-second impression as universally decisive and required exactly seven changes, at least four of which had to subtract.

Version 2:

- removes duplicated YAML frontmatter;
- replaces the “sacred” one-second test with Glance, Scan, and Study layers;
- groups criteria under Clarity, Form, and Taste;
- uses evidence-based rating bands instead of default numerical averages;
- adds confidence to material judgments;
- resolves verdict rules without arithmetic gaps;
- bases REBUILD on the nature of the failure rather than one low score;
- replaces seven mandatory changes with Must Fix, Should Improve, and Optional Refinement;
- retains subtraction as a useful prior without punishing necessary complexity;
- adds medium-specific calibration and Learning Mode;
- moves historical guidance into an optional reference.

## Package structure

```text
Loewy.skill
└── loewy/
    ├── SKILL.md
    └── references/
        ├── learning.md
        ├── loewy-principles.md
        └── media.md
```

## Three viewing layers

| Layer | Question |
| --- | --- |
| **Glance** | What silhouette, primary message, or emotional signal registers immediately? |
| **Scan** | Does the hierarchy reveal the intended relationships and supporting information? |
| **Study** | Does detail, rhythm, craft, and secondary meaning reward sustained attention or use? |

The relevant balance depends on the medium. A safety sign must succeed primarily at a glance. A report, interface, or data visualization may reveal necessary information through scanning and study.

## Diagnostic groups

### Clarity

- Legibility in context.
- Hierarchy and focus.
- Honesty between form, content, and function.

### Form

- Proportion, spacing, and rhythm.
- Craft and finish.
- Necessary complexity versus unearned clutter.

### Taste

- Restraint and coherence.
- Emotional tone for the intended audience.
- MAYA calibration.

Each criterion receives one of five bands:

| Band | Meaning |
| --- | --- |
| **Exceptional** | Resolved and unusually strong. |
| **Strong** | Clearly effective with no material weakness. |
| **Developing** | A sound basis with a meaningful issue. |
| **Weak** | Materially impairs the result. |
| **Critical** | Breaks comprehension, function, or the central idea. |

Developing, Weak, and Critical ratings require evidence and a confidence level. Numerical scores are available only when requested and must be explained as summaries of judgment rather than measurements.

## MAYA analysis

The skill identifies:

1. Familiar category cues that preserve recognition or trust.
2. The choice that advances beyond the expected pattern.
3. Whether that novelty serves function, expression, or fashion alone.
4. The evidence available for its audience judgment.

MAYA should not excuse timid work. It also should not demand novelty where conventional patterns reduce errors or make an experience easier to use.

## Verdict rules

- **SHIP:** every essential criterion is Strong or Exceptional, no blocker remains, and further changes are optional.
- **REFINE:** the central idea is sound, but one or more material criteria remain Developing or Weak.
- **REBUILD:** the concept, functional structure, or communication model is fundamentally wrong.

Craft weakness alone does not automatically require rebuilding. No average can conceal a blocking issue.

## Priority changes

Recommendations use only the tiers that contain real findings:

- **Must fix:** changes required to alter the verdict or prevent failure.
- **Should improve:** changes that materially strengthen the work.
- **Optional refinement:** defensible enhancements that are not disguised faults.

Subtraction is recommended when it removes unearned complexity. It is not used to erase information, affordances, cultural character, or richness the artifact needs. The output also identifies what should remain untouched.

## Evidence model

Each material recommendation follows:

```text
Observation → Interpretation → Move → Success criterion
```

The assistant states evidence limitations. A screenshot does not establish actual user behavior, accessibility, print quality, interaction behavior, licensing, commercial outcomes, or unseen states.

## Default output

```text
CONTEXT AND CONFIDENCE
VIEWING READ
  Glance
  Scan
  Study
DIAGNOSIS
  Clarity
  Form
  Taste
MAYA POSITION
PRIORITY CHANGES
VERDICT
THE ONE THING
KEEP
```

If the work should ship, the skill says so and avoids inventing improvements.

## Learning and comparison

Learning Mode asks the designer what registers first, what can be removed without loss, what complexity is necessary, and which choice is familiar or new. It compares their evidence with the review, explains one principle, and sets a one-variable exercise.

When comparing revisions, it reports what improved or regressed at Glance, Scan, and Study, and whether the previous priority issue was resolved. Bands remain secondary to evidence.

## Example prompt

```text
Use Loewy in Learning Mode to compare versions A and B of this landing page.

Audience: people encountering the service for the first time.
Goal: communicate trust and make the primary action immediately clear.
Category: professional services.
Evidence: desktop screenshots only.

Assess Glance, Scan, and Study; separate Clarity, Form, and Taste;
explain MAYA using category evidence; and identify whether the earlier
hierarchy problem was resolved. Do not infer mobile or interaction behavior.
```

## Medium calibration

The package contains criteria for posters and social graphics, identities, editorial and decks, websites and UI, data visualization, packaging and products, and wayfinding and safety. “Timeless” is not assumed to be every brief's goal; current, temporary, subcultural, or deliberately abrasive work may be appropriate.

## Historical reference

The optional reference summarizes principles and commonly associated works. It cautions against copying streamlined styling, equating commercial success with all design value, or using MAYA to defend conservatism. Historical details and quotations should be verified before publication.

## Installation

Import [Loewy.skill](Loewy.skill) into a compatible host. The package contains Markdown instructions, not executable software. Platform support and invocation behavior vary.

To inspect it:

```sh
unzip -l Loewy.skill
```

---

[Back to repository overview](../../README.md)
