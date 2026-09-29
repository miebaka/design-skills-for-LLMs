# Design Skills for LLMs

Three open-source, platform-agnostic instruction packages that help designers critique work, develop concepts, refine visual taste, and learn the reasoning behind stronger design decisions.

## Skills

| Skill | Primary role | Detailed guide | Package |
| --- | --- | --- | --- |
| **Casey** | Concept, metaphor, typographic meaning, and structural clarity. | [Read the guide](skills/casey/README.md) | [Download](skills/casey/Casey.skill) |
| **Creative Direction** | Broad critique, concept generation, elevation, and cross-medium direction. | [Read the guide](skills/creative-direction/README.md) | [Download](skills/creative-direction/Creative-Direction.skill) |
| **Loewy** | Taste, restraint, form, MAYA calibration, and release judgment. | [Read the guide](skills/loewy/README.md) | [Download](skills/loewy/Loewy.skill) |

## Choose the right skill

- Use **Casey** when the central problem is what the design means and how its visual idea emerges from the subject.
- Use **Creative Direction** when you need the broadest diagnosis, several new directions, or a prioritized improvement pass.
- Use **Loewy** when you need a final judgment about clarity, form, taste, and whether the work should ship.

The metadata intentionally separates these roles so a generic design request does not need to invoke all three.

## Version 2.1 principles

The collection now prioritizes teaching and evidence over theatrical criticism.

Every skill:

- distinguishes visible observation from interpretation;
- turns recommendations into testable success criteria;
- states assumptions and confidence when evidence is incomplete;
- adapts its judgment to the medium and design stage;
- avoids treating numerical scores as objective measurements;
- distinguishes design taste from usability, accessibility, brand, copy, legal, and production checks;
- supports revision comparison;
- includes a Learning Mode for junior designers;
- keeps its core entry file concise and loads detailed references only when relevant.

Creative Direction 2.1 adds a dedicated editorial-cover framework. It separates a story's topic from its proposition, directs the relationship between image and language, evaluates immediate and delayed readings, and adds truth, dignity, provenance, identity, sequence, thumbnail, neighbor, and physical-object checks. The framework draws lessons from editorial-cover practice without copying any publication's trade dress.

The goal is not to let AI declare what good taste is. It is to make visual reasoning explicit enough that a designer can question it, test it, and eventually use it independently.

## Package structure

```text
skills/
├── casey/
│   ├── Casey.skill
│   └── README.md
├── creative-direction/
│   ├── Creative-Direction.skill
│   └── README.md
└── loewy/
    ├── Loewy.skill
    └── README.md
```

Each `.skill` file is a ZIP archive containing `SKILL.md` and relevant references. It contains instructions rather than executable software. Import support, automatic invocation, and slash commands depend on the AI host.

## Evidence and scope

A visible artifact or clear brief, audience, intended message, medium, dimensions, design stage, and constraints produce the strongest review. A static screenshot supports visible composition judgments but cannot prove accessibility, interaction quality, print readiness, licensing, or actual audience behavior.

These skills should not manufacture certainty. When a specialist review is needed, they identify it instead of stretching a taste framework beyond its evidence.

## Suggested learning workflow

1. Ask the junior designer to state the intended idea and focal point.
2. Run the appropriate skill in Learning Mode.
3. Compare the designer's reasoning with the review's visible evidence.
4. Change one variable in the next version.
5. Re-evaluate using the same success criterion.
6. Record the reusable principle rather than only the final score or verdict.

## Example

```text
Use Creative Direction in Learning Mode to review this mobile screen.
First ask me to identify its message, focal point, and weakest decision.
Then compare my reasoning with visible evidence. Give me one principle,
one bounded exercise, and a success criterion for the next version.
Do not infer interaction states that are not shown.
```

## License and historical material

The repository currently has no license file. The packages reference historical designers and works as interpretive context. Verify quotations, dates, and attribution before reusing them in published historical or academic material.
