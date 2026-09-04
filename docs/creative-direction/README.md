# Creative Direction: critique, concept, and elevation

Creative Direction is a general-purpose art direction skill for evaluating existing visual work, developing three different concepts from a brief, and identifying focused changes that improve an adequate design. It combines an eight-dimension critique with adjustable intensity and a strong preference for clear ideas, deliberate typography, and specific prescriptions.

Its three modes answer different questions:

| Mode | Question |
| --- | --- |
| **CRITIQUE** | How good is this, what works, and what is holding it back? |
| **CONCEPT** | What are three substantially different ways to communicate this brief? |
| **ELEVATE** | What are the three highest-impact changes to the existing direction? |

This README analyzes [Creative-Direction.skill](../../Creative-Direction.skill). It describes the packaged instructions, including their gaps and dependencies. Example prompts and implementation advice are documentation additions, not proof of tested assistant behavior.

## Contents

- [Package contents and scope](#package-contents-and-scope)
- [Setup and invocation](#setup-and-invocation)
- [Choose the mode](#choose-the-mode)
- [Choose the intensity](#choose-the-intensity)
- [Inputs and preparation](#inputs-and-preparation)
- [CRITIQUE: the eight dimensions](#critique-the-eight-dimensions)
- [Scoring and verdicts](#scoring-and-verdicts)
- [CRITIQUE output](#critique-output)
- [CONCEPT workflow and output](#concept-workflow-and-output)
- [The twelve concept techniques](#the-twelve-concept-techniques)
- [ELEVATE workflow and output](#elevate-workflow-and-output)
- [Principles shared by all modes](#principles-shared-by-all-modes)
- [Brand context and dependencies](#brand-context-and-dependencies)
- [Example prompts](#example-prompts)
- [Analysis: strengths and limitations](#analysis-strengths-and-limitations)
- [Troubleshooting and quality checks](#troubleshooting-and-quality-checks)
- [How it differs from Casey and Loewy](#how-it-differs-from-casey-and-loewy)

## Package contents and scope

The `.skill` download is a ZIP archive containing a single file:

```text
Creative-Direction.skill
└── creative-direction/
    └── SKILL.md
```

The internal name is `creative-direction`. There are no scripts, image assets, templates, standalone reference files, scoring utilities, or design application integrations in the package.

The skill adopts an experienced creative director persona and draws on design traditions and historical examples. That persona is an instruction for the assistant's style of reasoning; it is not a credential or a guarantee of expertise.

It supports brand identity, advertising, editorial work, corporate communications, and other visual artifacts. It explicitly separates its role from brand compliance and asset generation. A strong review can tell you what to change, but the package does not itself create a Figma file, generate an image, export artwork, or certify a production file.

## Setup and invocation

Import [Creative-Direction.skill](../../Creative-Direction.skill) in a host that supports packaged skills. The exact controls and supported format must be established from your host; the repository does not include an installer or a list of verified platforms.

For directory-based use, inspect and extract it from the repository root:

```sh
unzip -l Creative-Direction.skill
unzip Creative-Direction.skill -d ./extracted
```

The resulting folder is `./extracted/creative-direction/`. Follow the host's own instructions for registering that folder. Extraction alone does not activate it.

An explicit request is the clearest way to select the framework:

```text
Use the creative-direction skill in CRITIQUE mode at BUILD intensity
on the attached draft.
```

Natural-language triggers in the metadata include requests to review a design, generate ideas, art-direct something, explain what is missing, or improve work that feels flat. Automatic matching and any `/creative-direction` command depend on the host.

## Choose the mode

| Situation | Recommended mode | Main deliverable |
| --- | --- | --- |
| You have a draft and need a diagnosis. | CRITIQUE | Scores, verdict, strengths, ranked issues, one key change. |
| You have a brief and need a direction. | CONCEPT | Three distinct concepts with rationale and a recommendation. |
| You have an established direction that needs a push. | ELEVATE | Three concrete changes ranked by impact. |

The instructions say to infer the mode when the request makes it clear and ask when it does not. You can avoid ambiguity by naming the mode explicitly.

A useful sequence is CONCEPT for the initial brief, CRITIQUE after a draft exists, and ELEVATE for a focused improvement pass. This sequence is a suggested workflow; the package does not require all three modes to run together.

## Choose the intensity

Intensity changes the critique's stance according to the maturity of the work. It is separate from the operating mode.

| Level | Name | Intended stage | Behavior |
| --- | --- | --- | --- |
| 1 | **EXPLORE** | Sketches, mood boards, early ideas. | Encouraging but specific; looks for promising potential. |
| 2 | **BUILD** | Working drafts and mid-process reviews. | Constructive, prioritized, concrete. |
| 3 | **SHIP** | Final review before publishing or printing. | Demanding; the instructions prohibit shipping with a Critical issue. |

If unspecified, the skill infers intensity from the context: a finished social graphic suggests SHIP, a rough sketch suggests EXPLORE, and an in-progress check suggests BUILD. If still uncertain, it asks which stage applies.

**SHIP here is an intensity setting, not a scored verdict.** The scored verdicts are EXCEPTIONAL, SOLID, MEDIOCRE, and WEAK. This distinction matters when comparing it with Loewy, where SHIP is a final verdict.

The package mentions “Critical” issues but does not define a formal severity taxonomy. If a release decision depends on severity, ask the assistant to name the specific blocking issue and why it prevents release rather than relying on the label alone.

## Inputs and preparation

For critique or elevation, provide a visible artifact and enough context to understand its purpose. A screenshot supports visual assessment; a written description supports a more limited conceptual review.

For concept development, the skill explicitly asks for:

1. The single message.
2. The audience and its context.
3. The placement or channel.
4. The format and dimensions.
5. The brand and any available guidelines.
6. The production method, such as digital, print, or video.

Additional useful constraints include required text, asset availability, licensed fonts, deadlines, and what can be changed. These prevent a precise-sounding prescription from being impractical.

For multi-page work, identify whether the task concerns a single page or consistency across the full sequence. For an iteration, attach both versions and label them clearly. Version comparison is useful, but persistent revision history is not a packaged feature.

## CRITIQUE: the eight dimensions

The skill scores only dimensions relevant to the artifact. A typography-only poster need not receive an invented image-quality score.

| Dimension | Core question | What the skill examines |
| --- | --- | --- |
| **Concept strength** | Is there an idea worth expressing? | Clarity, relevance, memorability, and whether the idea does more than a stock template. |
| **Composition and spatial intelligence** | Does the arrangement guide attention intentionally? | Eye path, negative space, grid logic, placement, and compositional tension. |
| **Typography** | Does type actively contribute to the design? | Hierarchy, headline function, face choice, spacing, alignment, and type as a visual element. |
| **Color strategy** | Is there a purposeful palette? | Dominant/supporting/accent roles, meaning, contrast, distinctiveness. |
| **Image/illustration quality** | Is imagery doing conceptual work? | Composition, lighting, stylistic relevance, purposeful art direction, and avoidance of generic filler. |
| **Craft and finish** | Has the execution been resolved? | Edges, alignment, spacing, text problems, artifacts, and suitability for the intended scale. |
| **Originality and surprise** | Does the work have a distinctive point of view? | Unexpected choices, ownability, and whether a competitor's logo could be substituted. |
| **Communication effectiveness** | Does the audience understand the intended message quickly? | First impression, information order, and clarity without explanation. |

Several checks are design heuristics rather than measured procedures. The two-second eye path and 1.5-second impression are prompts for attention analysis, not instrumented user tests. The 60/30/10 color rule is a suggested palette check with room for deliberate exceptions, not a mandatory pixel ratio.

Likewise, a screenshot cannot establish actual print resolution, bleed, font embedding, or exact measured contrast. The assistant can flag suspected issues but needs the appropriate files or tools to verify them.

## Scoring and verdicts

Each applicable dimension receives a score from **1 to 10**.

| Average | Verdict | Interpretation in the package |
| --- | --- | --- |
| 8–10 | **EXCEPTIONAL** | Portfolio-worthy work. |
| 6–7.9 | **SOLID** | Professional and competent, but not yet memorable. |
| 4–5.9 | **MEDIOCRE** | Significant concept, composition, or craft issues. |
| 1–3.9 | **WEAK** | Fundamental problems requiring a major rethink. |

The table refers to an average, but the package does not specify weighting or rounding. A transparent practical convention is an equal-weight mean of the applicable dimensions, with the included dimensions named. That convention should be disclosed if the result is near a boundary.

For example, seven applicable scores of `8, 7, 8, 7, 8, 6, 8` total 52. Their mean is approximately `7.43`, which falls in SOLID. The omitted image dimension should be labeled not applicable, not scored zero. This is an illustrative calculation, not a review of an actual design.

Avoid rounding a sub-8 average upward and silently classifying it as EXCEPTIONAL. The source does not settle every decimal boundary; showing the calculation is more useful than implying false precision.

A high average is also not a complete release gate. At SHIP intensity the instructions still prohibit Critical issues, even though the average-based table uses encouraging language for EXCEPTIONAL work. Keep the quality verdict and any blocking issue explicit.

## CRITIQUE output

The required shape contains these sections:

```text
MODE: CRITIQUE | Intensity: [EXPLORE/BUILD/SHIP]

VERDICT: [EXCEPTIONAL / SOLID / MEDIOCRE / WEAK]

SCORES:
[Applicable dimension]: [Score]/10 — [Specific assessment]

WHAT WORKS:
[One to three specific strengths]

WHAT DOESN'T:
[Issues ranked by severity]

THE MOVE:
[The single most impactful concrete change]
```

The key discipline is prioritization. A list of observations becomes useful direction when it identifies the change that most improves the outcome. “Increase contrast” is incomplete unless the review identifies which elements should separate and how.

The strength section also matters: it identifies what should survive revision rather than inviting indiscriminate redesign.

## CONCEPT workflow and output

CONCEPT first clarifies the brief, then generates **three different ideas**, and finally ranks them. Merely changing colors, fonts, or crops around one underlying idea does not satisfy the intended conceptual diversity.

Each concept includes:

```text
CONCEPT [A/B/C]: [Distinctive name]

THE IDEA:
[One-sentence proposition]

VISUAL DIRECTION:
- Composition
- Typography
- Color
- Imagery
- Texture/material, if relevant

REFERENCE LINEAGE:
[Relevant design tradition or precedent and its purpose]

WHY THIS WORKS:
[Connection to this message, audience, and medium]

RISK:
[The direction's likely failure mode]
```

After all three, the assistant recommends one and explains why. The risk field is valuable: it prevents a concept from being presented as universally effective and shows what execution must get right.

Specific hex values are appropriate when the brand palette is supplied or known. When it is not, the instructions allow color logic rather than invented brand specifications.

The output is written direction. Any image generation, mockup creation, or editable design production requires separate tooling and authorization appropriate to that task.

## The twelve concept techniques

The package offers a repertoire to avoid defaulting to a photograph plus a headline. These are optional techniques, not twelve steps to execute on every project.

| Technique | Mechanism | Best fit |
| --- | --- | --- |
| Type as hero | Letterforms, a headline, or numerals become the image. | A strong verbal message with visual potential. |
| Monumental scale | One element becomes unexpectedly large. | Attention and impact through size relationships. |
| Object portrait | A single rendered or photographed object carries meaning. | Symbolism, aspiration, elegance. |
| Atmospheric photography | Environment and mood tell the story. | Emotion, narrative, gravitas. |
| Systematic grid | A coherent structure organizes multiple elements. | Collections, variety, scope. |
| Surrealist juxtaposition | An unexpected relationship creates metaphor. | Surprise and conceptual depth. |
| Diagrammatic beauty | Systems or flows become the visual subject. | Networks, processes, technical relationships. |
| Material texture | Surface and material carry the experience. | Craft, tactility, perceived quality. |
| Collage/montage | Multiple images form a larger composition. | Multiplicity or transformation. |
| Color field | Flat color establishes the dominant presence. | Brand recognition and direct impact. |
| Negative space drama | Absence amplifies what remains. | Confidence, sophistication, emphasis. |
| Paper-cut/silhouette | Shapes create form and depth without photography. | Warmth, handcraft, constrained illustration budgets. |

The source associates these techniques with historical corporate design examples. It repeatedly mentions an “archive,” but no separate archive, image collection, or source bibliography is included. The examples should be treated as internal reference descriptions until the original works are consulted.

## ELEVATE workflow and output

ELEVATE uses the eight dimensions to diagnose the existing direction, then looks for its strongest achievable version. It focuses on six possible kinds of intervention:

- **Scale shift:** change the relative size of elements.
- **Subtraction:** remove unnecessary content or decoration.
- **Concept injection:** introduce the missing central idea.
- **Material upgrade:** improve imagery, type, color, or execution quality.
- **Tension introduction:** break an overly predictable relationship deliberately.
- **Spatial reorganization:** rearrange the right elements into a better composition.

The output requires **three moves ranked by impact**, each concrete enough to execute in 15 minutes or less:

```text
MODE: ELEVATE

CURRENT STATE:
[One-sentence assessment]

THE CEILING:
[The best version of the current direction]

MOVE 1 (Highest impact):
[Concrete action]

MOVE 2:
[Concrete action]

MOVE 3:
[Concrete action]

WHY THESE MOVES:
[Principles and expected improvement]
```

The 15-minute constraint is a prescription target, not a reliable time estimate for every user or tool. New photography, custom illustration, or licensing a typeface may exceed it. If those are essential, the output should distinguish a larger dependency from a genuinely quick edit.

Although the diagnosis uses the same dimensions as CRITIQUE, the ELEVATE template does not require a full displayed scorecard.

## Principles shared by all modes

The ten principles prioritize one clear idea, restraint, typography as design, meaningful color, fast communication, concept before polish, competitive distinctiveness, thoughtful use of history, durability of judgment, and specificity.

They help resolve common traps: polishing an empty layout, mistaking many elements for richness, or borrowing an aesthetic without understanding its purpose. They are assertive creative heuristics, not universal laws. Information-dense work can still be excellent; a recurring series can have a legitimate template; a complex story may need several coordinated messages across multiple pages.

Apply the principles at the appropriate unit. “One idea per piece” can mean one governing thesis across a deck, rather than deleting every supporting fact.

## Brand context and dependencies

The skill applies the same creative framework to every brand, organization, and independent project. It uses the current task's supplied or verified guidelines rather than assuming a particular palette, visual metaphor, production style, or companion skill.

Its brand-context checks ask whether:

- The organization has a specific reason to communicate this message.
- The idea is relevant to the audience and purpose.
- The work is coherent with supplied examples from the broader campaign or system.
- The execution respects current constraints without confusing compliance with creative quality.

The repository does not include private brand assets or a universal brand rulebook. Supply current guidelines and comparison work when those judgments matter. If no brand system applies, use the brief, audience, medium, and production constraints as the basis for the review.

Formal brand compliance and asset generation remain separate tasks. The skill does not require a named companion skill, and it does not create access to design files or production tools.

## Example prompts

### Review a working draft

```text
Use creative-direction in CRITIQUE mode at BUILD intensity.
Review the attached event announcement for a mobile audience.

Goal: make the event topic clear, then drive registration.
Keep: logo, date, speaker names, and registration address.
Evaluate applicable dimensions only. Give a verdict, specific strengths,
ranked problems, and one highest-impact change.
```

### Generate three concepts

```text
Use creative-direction in CONCEPT mode.

Message: a public library gives people room to explore unfamiliar ideas.
Audience: local adults who do not currently use the library.
Placement: bus shelter posters.
Format: portrait; the headline must read at a distance.
Brand: use the attached guidelines.
Production: print, with an illustration budget but no photo shoot.

Develop three different ideas with composition, type, color, imagery,
reference lineage, rationale, and risk. Rank them and choose one.
```

### Request a focused improvement pass

```text
Use creative-direction in ELEVATE mode on this draft.
Keep the central concept and the approved copy. I have 45 minutes.
Give three ranked changes that can each be executed in about 15 minutes
using the existing assets. Explain the best achievable version.
```

### Apply supplied brand context

```text
Use creative-direction in CRITIQUE mode at SHIP intensity.
I have attached the organization's current brand guidance and recent
campaign examples. Assess the message's relevance and the design's
coherence using those materials. Distinguish creative quality from
formal brand compliance, and identify any missing evidence.
```

## Analysis: strengths and limitations

The clearest strength is the separation of diagnosis, ideation, and refinement. The user can ask for the decision they need instead of receiving the same lengthy critique at every stage. Adjustable intensity makes the framework less likely to treat a rough sketch as a failed final piece.

The concepts include risks and an explicit recommendation, which makes them more useful than a list of equally praised directions. ELEVATE adds a practical constraint by limiting the output to three focused moves.

Important limitations remain:

| Limitation | Consequence |
| --- | --- |
| No executable scoring or validation logic. | Arithmetic and format compliance depend on the assistant. |
| No defined weighting or rounding policy. | Borderline verdicts should explain their calculation. |
| Critical severity is undefined. | Release blockers need specific evidence and rationale. |
| No bundled historical archive. | Precedents and factual claims need verification before publication. |
| Brand guidelines and campaign examples are external inputs. | Brand-specific conclusions require supplied, current references. |
| Static visual evidence may be incomplete. | Print quality, interaction behavior, and accessibility cannot be fully established from a screenshot. |
| Strong preference for reduction and novelty. | Apply context so useful density or coherent repetition is not mistaken for failure. |

## Troubleshooting and quality checks

| Symptom | Correction |
| --- | --- |
| Three concepts look like the same layout. | Ask for different underlying ideas before discussing visual treatments. |
| Feedback is too severe for a sketch. | Specify EXPLORE and explain what has intentionally not been resolved. |
| Scores include irrelevant dimensions. | Ask for the applicable subset and an explicit denominator. |
| Advice cannot fit the deadline. | State asset and time constraints; request feasible ELEVATE moves. |
| The output says “on brand” without seeing guidelines. | Supply the guidelines or mark that conclusion unverified. |
| An excellent average hides a blocker. | Ask for the blocking issue separately from the quality verdict. |
| Recommendations are vague. | Request the exact element, edit, and intended effect. |

A faithful CRITIQUE includes applicable scores, the correct verdict family, one to three strengths, ranked issues, and THE MOVE. A faithful CONCEPT includes three distinct complete concepts and a preferred direction. A faithful ELEVATE includes the current state, ceiling, exactly three ranked moves, and their rationale.

## How it differs from Casey and Loewy

Use Creative Direction as the broad everyday framework. Use [Casey](../casey/README.md) when the task needs deeper investigation of visual metaphor, typographic wit, and subject-specific conceptual compression. Use [Loewy](../loewy/README.md) when taste, proportion, simplification, and the balance between familiarity and novelty are the main concern.

Do not compare scores as if they came from a shared instrument. Creative Direction uses applicable dimensions scored 1–10; Loewy specifies eight dimensions scored 0–10; Casey defines qualitative tests without a numerical scale.

---

[Back to repository overview](../../README.md)
