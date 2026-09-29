# Creative Direction

Creative Direction is the graphic-design-first, brand-agnostic skill in this collection. It critiques existing work, develops distinct concepts from a brief, improves a sound direction, and teaches designers how to reason about their choices.

Use it for identities, editorial, campaigns, typography-led communication, packaging, presentations, and digital surfaces. It also translates graphic-design reasoning into interface, spatial, service, industrial, motion, data, and fashion work without treating those fields as surface styling.

## What changed in version 2.2

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

Version 2.1 added a deep editorial-cover branch built from longitudinal cover analysis. It does not prescribe an aesthetic. It teaches the assistant to direct the story's proposition, choose a truthful visual mechanism, manage first and second readings, and test a cover in its actual distribution system.

Version 2.2 establishes graphic design as the skill's center of gravity:

- a mandatory graphic-design spine for hierarchy, grids, composition, typography, imagery, color, graphic devices, material, systems, production, adaptation, and craft;
- graphic premises that connect an idea to a repeatable formal rule rather than a mood or style adjective;
- implementable recommendations that name the variable, action, intended effect, and success criterion;
- campaign-family, identity-system, copy-architecture, and stress-testing guidance;
- conditional Use / Performance and System diagnoses when the work extends beyond a single artifact;
- a cross-disciplinary translation framework that adds functional evidence without confusing visual direction with usability, engineering, architecture, garment construction, or service operations;
- expanded routing for presentations, motion, spatial design, products and furniture, services, fashion, and structural packaging.

## Package structure

```text
Creative-Direction.skill
└── creative-direction/
    ├── SKILL.md
    └── references/
        ├── critique.md
        ├── concept.md
        ├── cross-disciplinary.md
        ├── elevate.md
        ├── editorial-covers.md
        ├── graphic-design.md
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

For editorial work, it also distinguishes the subject from the specific claim or question the publication is placing on the cover.

### Communication

It examines hierarchy, comprehension in the actual viewing context, and audience and medium fit.

### Execution

For graphic work it examines composition, typography, imagery, color, graphic devices, system behavior, adaptation, production, and craft.

For interactive, spatial, service, and physical work, the diagnosis conditionally adds **Use / Performance**. Identities, campaigns, publications, families, and multi-touchpoint work conditionally add **System**. Unsupported dimensions are marked Not assessable rather than Weak.

Keeping these groups separate makes the response more diagnostic:

```text
Idea: Strong
Communication: Developing
Execution: Strong
Use / Performance: Not assessable
System: Developing
```

This indicates that the concept and craft should be preserved while hierarchy or comprehension is revised. A single average would conceal that distinction.

## Evidence model

Every material finding separates:

```text
Observation → Interpretation → Recommendation → Success criterion
```

The assistant states its assumptions and avoids claiming tested comprehension, accessibility, interaction quality, print readiness, licensing, exact measurements, or audience behavior without supporting evidence.

## Graphic-design spine

Every task reads the graphic-design reference. It directs:

- content and copy architecture;
- first, second, and third reads;
- composition, format, grids, counterspace, rhythm, edges, and controlled exceptions;
- typographic roles, hierarchy, spacing, line behavior, optical relationships, language support, and reproduction;
- photographic, illustrative, documentary, conceptual, atmospheric, and identity imagery;
- color as hierarchy, meaning, grouping, identity, navigation, material, and production;
- graphic devices, material language, authored imperfection, and craft;
- invariant assets, meaningful variables, adaptation rules, exceptions, governance, and system stress tests;
- relevant production and platform conditions without claiming unverified preflight readiness.

The skill asks for a **graphic premise**: the repeatable relationship among content and form that translates the idea. “Bold,” “clean,” “premium,” and “editorial” are moods, not premises.

## Concept Mode

Concepts begin from one shared strategy sentence:

```text
Communicate [message] to [audience] in [context] so they [response],
while respecting [constraints].
```

The skill produces three directions only when breadth is useful. The alternatives must differ in underlying idea or mechanism rather than merely typeface, color, or crop. Each direction includes its graphic premise; first encounter and reading or use sequence; content, composition, type, image, color and material logic; system behavior; asset needs; dependencies; failure mode; and a cheap test.

Directions are ranked using relevance, comprehension, distinctiveness, tone, truth, feasibility, and system fit.

Before developing directions, the assistant maps a broader decision space—literal evidence, human experience, system or structure, language, object, transformation, and metaphor—then removes mechanisms that would distort the message or tone.

## Medium-specific review

The package includes dedicated criteria for:

- posters, social graphics, and ads;
- identities;
- campaigns;
- editorial covers;
- editorial interiors and decks;
- websites and interfaces;
- data visualization;
- packaging;
- presentations and decks;
- motion, title, and broadcast work;
- spatial, retail, exhibition, and wayfinding systems;
- industrial products and furniture;
- services;
- fashion.

For UI, it considers task clarity, interaction hierarchy, affordance, state visibility, consistency, error handling, responsive behavior, and available accessibility evidence. A screenshot supports only the visible state; unseen interactions should not be invented.

For data visualization, necessary density is not treated as clutter. The review considers the analytical question, encoding integrity, comparisons, annotations, and uncertainty.

For adjacent fields, the skill preserves its graphic-design lens while adding the evidence the field requires. It will not infer a workflow from a hero screen, circulation from a render, comfort from a product beauty shot, service performance from a journey map, garment fit from campaign imagery, or manufacturing quality from a mockup.

## Editorial-cover direction

The editorial-cover reference begins with four lines:

```text
Topic → Claim → Tension → Cover move
```

This prevents a cover from merely illustrating a category such as housing, elections, health, or technology without expressing what the story actually says.

It then identifies the editorial act—such as witnessing, explaining, accusing, complicating, commemorating, celebrating, satirizing, humanizing, or archiving—and selects a visual mechanism that can perform that act truthfully. Supported mechanisms include documentary evidence, portraiture, objects, material transformation, visual metaphor, typography, diagrams, archives, illustration, satire, absence, and direct headline-image combinations.

The framework evaluates four cover jobs independently:

1. **Signal:** interrupt the surrounding field.
2. **Orient:** establish subject, stakes, or emotional register.
3. **Reward:** provide a consequential second reading.
4. **Entitle:** justify giving this story the publication's finite cover space.

It classifies image-language relationships as Anchor, Turn, Extend, Counterpoint, Redundant, or Dependent, then records the cover's immediate read, glance-level understanding, close read, and emotional residue.

Required checks can include:

- proposition and plausible-misread tests;
- thumbnail, distance, and five-second-recall tests;
- a covered-copy test and its image-hidden inverse;
- truth, provenance, dignity, and power review;
- neighbor and recent-issue sequence tests;
- physical trim, fold, binding, barcode, finish, and handling checks.

Distribution matters. A newspaper insert with a famous masthead can take identity risks that an unfamiliar newsstand title cannot. The skill therefore treats masthead obstruction, sparse cover lines, aggressive reduction, and social-feed performance as contextual decisions—not universal markers of sophistication.

The reference explicitly warns against copying another publication's masthead behavior, typography, palette, recurring format, or recognizable composition. It transfers editorial reasoning rather than trade dress.

## Default output

```text
CONTEXT
DIAGNOSIS
  Idea: Strong / Developing / Weak
  Communication: Strong / Developing / Weak
  Execution: Strong / Developing / Weak
  Use / Performance: Strong / Developing / Weak / Not assessable (when relevant)
  System: Strong / Developing / Weak / Not assessable (when relevant)
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
