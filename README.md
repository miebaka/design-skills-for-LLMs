# Design Skills for LLMs

Three instruction packages for AI-assisted design critique and creative direction. Each provides a different way to judge visual work, explain what is wrong, and decide what to do next.

## Skill documentation

Each guide covers installation considerations, inputs, the complete framework, operating modes, output requirements, example prompts, practical usage, and an analysis of strengths and limitations.

| Skill | Best question to bring | Main output | Detailed guide | Package |
| --- | --- | --- | --- | --- |
| **Casey** | What idea should this design compress, and how should type and structure express it? | Seven qualitative tests; four modes; structured recommendations or three concepts. | [Casey README](docs/casey/README.md) | [Casey.skill](Casey.skill) |
| **Creative Direction** | How good is this, what could it look like, or how do I improve it quickly? | CRITIQUE, CONCEPT, or ELEVATE; stage-sensitive intensity. | [Creative Direction README](docs/creative-direction/README.md) | [Creative-Direction.skill](Creative-Direction.skill) |
| **Loewy** | Is this tasteful, appropriately distinctive, and visually ready? | Eight scores, seven ranked moves, and SHIP / REFINE / REBUILD. | [Loewy README](docs/loewy/README.md) | [Loewy.skill](Loewy.skill) |

## Choose a starting point

- Start with **Casey** when the missing ingredient is a subject-specific idea, visual metaphor, or typographic wit.
- Start with **Creative Direction** for a broad critique, three different directions from a brief, or three focused improvement moves.
- Start with **Loewy** for beauty, restraint, proportion, craft, and the balance between unfamiliarity and convention.

For a longer project, use one primary framework at each stage. You might develop a concept with Casey, review its execution with Creative Direction, and use Loewy for a final taste pass. That sequence is a suggested workflow, not a requirement or an automated pipeline.

## How the packages work

Each `.skill` file is a ZIP archive containing Markdown instructions. These are prompts and reference material for a compatible assistant, not standalone applications. Import support, directory installation, automatic activation, and slash commands depend on the host.

```text
Casey.skill
├── casey/SKILL.md
└── casey/references/casey-biography-and-works.md

Creative-Direction.skill
└── creative-direction/SKILL.md

Loewy.skill
└── loewy/SKILL.md
```

No package bundles scripts, fonts, images, or design application integrations. Casey includes a textual reference document; the other two keep their reference descriptions within the main instructions.

For inspection, run `unzip -l` with the relevant package filename. Each guide includes an extraction example. Preserve the internal directory structure, particularly Casey's relative reference path.

Once the host has loaded a skill, a request can be as direct as:

```text
Use the creative-direction skill in CRITIQUE mode at BUILD intensity.
Review the attached poster for a mobile audience. The primary message
is the workshop topic, followed by the registration action. Keep all
required event details. Give specific, prioritized changes.
```

## What to provide

A visible artifact or a clear brief, the audience, intended message, placement, dimensions, and constraints make the reviews more useful. Include current brand guidance where relevant. A written description supports conceptual feedback but does not let an assistant verify the actual file's visual finish.

These skills do not create access to a linked file, install a design tool, conduct audience research, or establish production readiness. Their recommendations depend on the evidence and capabilities available to the assistant.

## Important distinctions

| Detail | Casey | Creative Direction | Loewy |
| --- | --- | --- | --- |
| Core framework | Seven qualitative tests. | Eight applicable critique dimensions. | Eight required rubric dimensions. |
| Numerical scale | None specified. | 1–10 for applicable dimensions. | 0–10 for eight dimensions. |
| Final verdicts | No fixed verdict vocabulary. | EXCEPTIONAL / SOLID / MEDIOCRE / WEAK. | SHIP / REFINE / REBUILD. |
| Concept generation | Three directions in Direction Mode. | Three concepts in CONCEPT mode. | No dedicated concept mode. |
| Recommendation count | Seven in Critique and Interrogation. | One primary move in CRITIQUE; three in ELEVATE. | Seven, at least four removing or simplifying. |
| Tone adjustment | Forceful, specific persona; no level setting. | EXPLORE / BUILD / SHIP intensity. | Blunt critique with explicit respect for the maker. |
| External context | Subject and audience; bundled historical reference. | Current brand guidance and campaign examples when relevant. | Audience and category context for MAYA. |

Do not compare scores directly across frameworks. In Creative Direction, SHIP names an intensity level; in Loewy, it names a verdict.

## Findings from the documentation review

- **Casey:** the most developed conceptual lens, with an included reference document. It has no numerical scoring system and leaves System Mode's response format relatively open.
- **Creative Direction:** the broadest workflow coverage. Its referenced historical “archive” is not included; brand context comes from materials supplied for the task. Weighting, rounding, and Critical severity are not fully specified.
- **Loewy:** the clearest taste-review template and minimum-score gate. Its main file duplicates its metadata, and a high average with a lowest dimension of 4–6 is not fully covered by the written verdict ranges.

The individual guides explain these findings and distinguish source requirements from recommended interpretations. The packages use brand-agnostic instructions. Creative Direction uses supplied brand context without requiring brand-specific companion skills.

## Documentation scope

The guides were initially written from every Markdown file contained in the three packages at repository commit `7c65eaa0d0feb703f24005b5f75775b7a8933c24` of [miebaka/design-skills-for-LLMs](https://github.com/miebaka/design-skills-for-LLMs).

Creative Direction and its documentation were subsequently updated to make the instructions brand-agnostic.

This was a source-content review, not a cross-platform installation test or live evaluation of model output. Historical examples and quotations are documented as package content; they have not been independently fact-checked here. Practical examples are illustrative.

The repository snapshot contains no license file. These READMEs do not establish new licensing terms for the packages or any third-party historical material they reference.
