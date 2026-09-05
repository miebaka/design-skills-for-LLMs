# Creative Direction

Creative Direction is the broad, brand-agnostic skill in this collection. It critiques existing work, develops distinct concepts from a brief, improves a sound direction, and teaches junior designers how to reason about their choices.

Use it when the task spans the idea, communication, and execution of graphic, identity, editorial, campaign, presentation, web, interface, data-visualization, or packaging work.

## What changed in version 2

The original rubric averaged eight unlike dimensions into one score. That could hide the difference between a strong idea with rough execution and polished work with no meaningful idea. Its universal heuristics also favored posters and reduction even when the medium required density or familiar interaction patterns.

Version 2:

- evaluates Idea, Communication, and Execution separately;
- uses Strong, Developing, and Weak diagnoses by default;
- makes numerical scores optional;
- adds Blocking, Major, Minor, and Optional severity;
- defines what can block a Ship-stage review;
- requires visible evidence and confidence limits;
- adds success criteria to recommendations;
- adds medium-specific branches, including UI and data visualization;
- adds effort labels to Elevate Mode;
- adds a stopping rule so resolved work can ship;
- adds Learning Mode for junior designers;
- separates substantial modes into references for lower context use.

## Package structure

```text
Creative-Direction.skill
└── creative-direction/
    ├── SKILL.md
    └── references/
        ├── critique.md
        ├── concept.md
        ├── elevate.md
        ├── learning.md
        └── media.md
```

## Modes

| Mode | Use it for | Output |
| --- | --- | --- |
| **Critique** | Diagnosing an existing artifact. | Three-part diagnosis, evidence, severity, up to three actions, and what to keep. |
| **Concept** | Developing directions from a brief. | Different conceptual mechanisms, feasibility, risk, testing, ranking, and a recommendation. |
| **Elevate** | Improving a sound existing direction. | Its achievable ceiling and up to three changes labeled Quick, Moderate, or Substantial. |
| **Learning** | Developing independent judgment. | Guided diagnosis, one principle, one-variable exercise, and revision review. |

## Design-stage calibration

- **Explore:** look for potential and open decisions; do not punish unfinished craft.
- **Build:** identify the few decisions preventing coherence.
- **Ship:** distinguish release blockers from optional improvement.

A Blocking issue prevents comprehension, intended use, or responsible release. A Major issue materially weakens the idea. A Minor issue affects finish. An Optional change is a legitimate alternative rather than a hidden defect.

Ship is a stage, not a numerical verdict. The skill no longer treats the possibility of another improvement as proof that the current work cannot ship.

## Diagnostic model

### Idea

The skill examines relevance to the brief, clarity of the governing idea, and distinctiveness.

### Communication

It examines hierarchy, comprehension in the actual viewing context, and audience and medium fit.

### Execution

It examines composition, typography, color, imagery when applicable, and craft.

Keeping these groups separate makes the response more diagnostic:

```text
Idea: Strong
Communication: Developing
Execution: Strong
```

This indicates that the concept and craft should be preserved while hierarchy or comprehension is revised. A single average would conceal that distinction.

## Evidence model

Every material finding separates:

```text
Observation → Interpretation → Recommendation → Success criterion
```

The assistant states its assumptions and avoids claiming tested comprehension, accessibility, interaction quality, print readiness, licensing, exact measurements, or audience behavior without supporting evidence.

## Concept Mode

Concepts begin from one shared strategy sentence:

```text
Communicate [message] to [audience] in [context] so they [response],
while respecting [constraints].
```

The skill produces three directions only when breadth is useful. The alternatives must differ in underlying idea or mechanism rather than merely typeface, color, or crop. Each direction includes its immediate and deeper read, visual logic, relationship to the brief, asset needs, effort, dependencies, failure mode, and a cheap test.

Directions are ranked using relevance, comprehension, distinctiveness, feasibility, and system fit.

## Medium-specific review

The package includes dedicated criteria for:

- posters, social graphics, and ads;
- identities;
- campaigns;
- editorial work and decks;
- websites and interfaces;
- data visualization;
- packaging.

For UI, it considers task clarity, interaction hierarchy, affordance, state visibility, consistency, error handling, responsive behavior, and available accessibility evidence. A screenshot supports only the visible state; unseen interactions should not be invented.

For data visualization, necessary density is not treated as clutter. The review considers the analytical question, encoding integrity, comparisons, annotations, and uncertainty.

## Default output

```text
CONTEXT
DIAGNOSIS
  Idea: Strong / Developing / Weak
  Communication: Strong / Developing / Weak
  Execution: Strong / Developing / Weak
EVIDENCE
PRIORITIES
  Blocking / Major / Minor / Optional
NEXT VERSION
KEEP
TEACHING NOTE
```

Up to three next actions are provided by default, each with a success criterion. The response should stop when the work meets the brief and no material problem remains.

## Example prompt

```text
Use Creative Direction in Critique Mode at Build stage.
Review these two mobile onboarding screens.

Audience: first-time users.
Goal: make the next action obvious and reduce uncertainty.
Evidence available: static screens only.

Diagnose Idea, Communication, and Execution separately. Do not infer
unseen interaction states. Classify findings by severity and give no more
than three priority actions, each with a success criterion.
```

## Brand context

The skill uses only supplied or verified current guidelines. It can assess whether a message is specific to an organization and whether work coheres with supplied campaign examples, but creative quality remains separate from formal brand compliance.

## Installation

Import [Creative-Direction.skill](Creative-Direction.skill) into a compatible host. The package consists of Markdown instructions; installation and invocation behavior depend on the host.

To inspect it:

```sh
unzip -l Creative-Direction.skill
```

---

[Back to repository overview](../../README.md)
