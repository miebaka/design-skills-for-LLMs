# Casey

Casey develops and critiques visual concepts through subject-specific metaphor, typographic meaning, and disciplined structure. It is designed for posters, campaigns, identities, and expressive communication where the central question is: **what should this design mean, and how should its form express that meaning?**

The skill is inspired by Jacqueline Casey's combination of American visual metaphor and Swiss structural discipline. It does not impersonate her or present an AI judgment as her personal view.

## What changed in version 2

The original package required seven tests and seven elaborate recommendations in most critiques. That structure could produce repetition, elevate cleverness over clarity, and encourage the assistant to manufacture findings. Version 2:

- separates observation, interpretation, prescription, and success criteria;
- uses only relevant tests instead of forcing every artifact through all of them;
- treats wit, duality, and ambiguity as optional rather than universal requirements;
- adds confidence and evidence limits;
- adds medium-specific calibration;
- adds Learning Mode for junior designers;
- replaces fixed recommendation counts with prioritized decisions;
- treats accessibility, usability, and production checks as separate disciplines;
- uses historical references only when they clarify a principle.

## Package structure

```text
Casey.skill
└── casey/
    ├── SKILL.md
    └── references/
        ├── critique.md
        ├── direction.md
        ├── learning.md
        ├── media.md
        └── casey-biography-and-works.md
```

`SKILL.md` is a concise router and shared framework. Mode-specific detail is loaded only when relevant. The biography and works reference remains available for historical context but is no longer part of every review.

## Core framework

The skill works through four stages:

1. **Subject truth:** state the proposition in one sentence and identify what makes the subject specific.
2. **Conceptual compression:** find the smallest visual or typographic relationship that carries the proposition.
3. **Formal construction:** test hierarchy, typography, grid, color, imagery, proportion, and reduction as support for the idea.
4. **Viewing conditions:** distinguish what must register immediately from what may unfold through attention.

Its available tests are Attention, Compression, Appropriateness, Metaphor Quality, Depth, Structural Clarity, Reduction, and Proportion. The assistant selects those that fit the artifact and medium.

Metaphor Quality now asks whether the relationship is understandable, specific, culturally responsible, useful, and capable of surviving without a paragraph of explanation. Humor is not mandatory. Direct communication may be the correct answer for functional or sensitive work.

## Modes

### Critique

Compares the intended message with what the artifact currently communicates, diagnoses the underlying cause, and prioritizes only material changes. Findings distinguish conceptual failures from craft symptoms.

### Direction

Begins with a strategy sentence and produces meaningfully different concepts when alternatives would help. Directions can be metaphor-led, information-led, or experience-led. Each includes production needs, risk, and a cheap test—not just visual styling.

### Interrogation

Clarifies the visual proposition of a brand, organization, or campaign before execution. It focuses on subject truth, audience, relevance, and ownability.

### System

Tests whether type, color, imagery, grid, and components express a coherent proposition across touchpoints. It uses criteria appropriate to the relevant medium.

### Learning

Helps a junior designer name the intended idea and focal point, compare their reasoning with visible evidence, learn one principle, make a bounded revision, and evaluate the result using the same criterion.

## Evidence model

Every major finding follows this sequence:

```text
Observation → Interpretation → Prescription → Success criterion
```

Example:

```text
Observation: The event title and sponsor block occupy similar visual weight.
Interpretation: The eye has two competing entry points, weakening the concept.
Prescription: Reduce and separate the sponsor block while preserving required marks.
Success criterion: At intended viewing size, the event title registers before sponsorship.
```

The skill must state assumptions and confidence when the artifact or context is incomplete. A screenshot cannot verify print resolution, accessibility, interaction behavior, licensing, or actual audience response.

## Default output

```text
CORE IDEA
EVIDENCE
CONCEPT VERDICT
STRUCTURAL VERDICT
PRIORITY CHANGES
LESSON
```

The default verdict vocabulary is Clear, Promising, Generic, or Contradictory. Recommendations remain proportional to the work. When concept, structure, and typography all need attention, the skill prioritizes one decision in each area.

## Example prompt

```text
Use Casey in Learning Mode to review this poster.

Message: the public lecture makes climate research understandable.
Audience: non-specialists seeing the poster on campus and mobile.
Required content: title, speaker, date, location, and registration URL.
Stage: working draft.

First ask me to identify the idea and focal point. Then compare my answer
with visible evidence, diagnose the concept and structure, and give me one
bounded exercise for the next version.
```

## Appropriate and inappropriate use

Casey is strongest when expressive meaning, metaphor, or typography is central. It can contribute to interfaces, dashboards, dense reports, safety communication, and wayfinding, but it should not dominate them. In those contexts, task completion, accessibility, necessary complexity, direct comprehension, and error cost may matter more than wit or ambiguity.

Historical examples should explain a principle rather than become templates. Verify quotations, dates, and attribution before publishing historical claims.

## Installation

Import [Casey.skill](Casey.skill) into a compatible host. The archive contains Markdown instructions rather than executable software. Host support, automatic invocation, and slash commands vary by platform.

To inspect it:

```sh
unzip -l Casey.skill
```

---

[Back to repository overview](../../README.md)
