# Casey: concept-led creative direction

Casey is a design critique and creative direction skill built around the relationship between **American visual metaphor and Swiss structural discipline**. Its central question is whether a design compresses a meaningful idea into a compelling image or typographic gesture, then gives that idea a precise visual structure.

Use it when a piece looks orderly but says little, when a concept is clever but poorly organized, or when you want an identity, poster, or campaign to emerge from its subject rather than an imported style.

This README analyzes the instructions and reference material inside [Casey.skill](../../Casey.skill). It documents the packaged behavior; it does not introduce new requirements into the skill. Prompt examples and practical interpretations below are documentation examples, not results from a live evaluation.

## Contents

- [What is included](#what-is-included)
- [What Casey is designed to do](#what-casey-is-designed-to-do)
- [Setup and invocation](#setup-and-invocation)
- [Preparing a useful brief](#preparing-a-useful-brief)
- [The two-culture framework](#the-two-culture-framework)
- [The seven tests](#the-seven-tests)
- [The design process](#the-design-process)
- [The four operating modes](#the-four-operating-modes)
- [The recommendation contract](#the-recommendation-contract)
- [Example prompts](#example-prompts)
- [Reading and using the output](#reading-and-using-the-output)
- [Reference material and attribution](#reference-material-and-attribution)
- [Strengths, limitations, and ambiguities](#strengths-limitations-and-ambiguities)
- [Troubleshooting](#troubleshooting)
- [Choosing between the three skills](#choosing-between-the-three-skills)
- [Review checklist](#review-checklist)

## What is included

The downloadable `.skill` file is a ZIP archive with this structure:

```text
Casey.skill
└── casey/
    ├── SKILL.md
    └── references/
        └── casey-biography-and-works.md
```

| Item | Purpose |
| --- | --- |
| `casey/SKILL.md` | Persona, evaluation framework, seven-step process, four modes, recommendation format, and tone instructions. |
| `casey/references/casey-biography-and-works.md` | Biography, influences, work catalog, poster analyses, quotations, and a bibliography. |

The internal skill name is `casey`. The package contains Markdown instructions, not executable software. There are no bundled scripts, fonts, images, design templates, or integrations. Its historical examples are text descriptions; it does not include reproductions of the posters.

## What Casey is designed to do

The skill takes the role of an exacting creative director inspired by Jacqueline Casey's practice. It evaluates whether the idea and its construction support each other. It can critique existing work, develop alternative concepts, interrogate a brand's visual proposition, or assess the coherence of a design system.

Good applications include:

- Posters and event identities that need a memorable central idea.
- Campaign concepts that currently depend on generic photography and a headline.
- Typography that delivers information but contributes no meaning.
- Brand identities with consistent execution but little distinctive conceptual content.
- Systems in which colors, grids, and components need a stronger reason for existing.
- Reviews where specific historical precedents would make a recommendation easier to understand.

The skill is especially distinctive when language itself can become the image: letterforms, word relationships, negative space, and typographic manipulation can carry the proposition.

It is less complete as a standalone tool for usability research, accessibility certification, copy verification, print preflight, or implementation. It may identify a visible problem in those areas, but it does not supply a dedicated testing procedure for them.

## Setup and invocation

### Use the packaged skill

Download [Casey.skill](../../Casey.skill) and import it through a host that supports this package format. Installation controls, automatic discovery, and slash-command support depend on the host. The repository does not provide an installer or a compatibility matrix.

### Inspect or install the extracted instructions

If your assistant uses directory-based skills, extract the package and follow that assistant's documented installation procedure. Preserve the `references` directory alongside `SKILL.md`; the main instructions refer to it by a relative path.

To inspect locally from the repository root:

```sh
unzip -l Casey.skill
unzip Casey.skill -d ./extracted
```

This produces `./extracted/casey/`. Extraction alone does not register the skill with an assistant. Choose a new destination if you already have an extracted copy you want to preserve.

### Ask for the skill explicitly

A portable request is:

```text
Use the casey skill in Critique Mode to review the attached poster.
Run all seven tests and give the seven structured recommendations.
```

If the host supports named slash commands, it may expose `/casey`. That command is host-dependent, not an executable included in this repository.

The metadata also lists natural-language triggers around design critique, creative direction, brand identity, poster design, typography, visual metaphor, layout review, campaigns, art direction, and CCO review. Whether those phrases automatically activate the skill depends on the assistant.

## Preparing a useful brief

The process begins with immersion in the subject. Supplying the underlying communication problem will produce more useful advice than requesting a stylistic reaction alone.

| Input | Why it matters | Example |
| --- | --- | --- |
| Artifact or brief | Gives the critique a concrete object or the direction a concrete problem. | Poster screenshot, identity presentation, campaign brief. |
| Single intended message | Establishes what must be compressed. | “The workshop makes difficult research understandable.” |
| Audience | Calibrates wit, knowledge, and the amount of interpretation the image can require. | First-year students with no specialist background. |
| Medium and size | Establishes viewing distance and information limits. | A3 print plus a mobile social adaptation. |
| Required information | Prevents reduction from removing essential content. | Title, date, location, organizer, registration route. |
| Brand constraints | Separates legitimate constraints from arbitrary stylistic habits. | Existing wordmark and licensed type family. |
| Stage of work | Distinguishes an exploratory idea from an almost finished artifact. | Early concept or final layout. |
| Production constraints | Keeps prescriptions feasible. | Two-color print, no new photography, one-day turnaround. |

If the assistant can only access a written description, it can discuss the concept and proposed structure. It should not present exact kerning, image quality, or alignment judgments as observed facts. Attach a visible render for those judgments.

## The two-culture framework

Casey combines two complementary requirements:

| Side | What it contributes | Failure when isolated |
| --- | --- | --- |
| American visual metaphor | Wit, emotional resonance, narrative, a meaningful conceptual association. | An interesting idea with confused execution. |
| Swiss structural discipline | Grid, proportion, hierarchy, reduction, rational placement. | An orderly composition with little communicative life. |

The practical implication is that a cleaner layout is not automatically a stronger design. The framework asks whether the order clarifies an idea worth communicating. Conversely, a clever image does not excuse weak hierarchy or careless typography.

## The seven tests

All seven are part of the core framework. In Critique Mode, the skill explicitly requires a verdict for each. It does not define numerical scores, weights, or a composite rating.

| Test | What it examines | Useful evidence | Typical corrective direction |
| --- | --- | --- | --- |
| **Stop** | Whether the work earns attention among competing messages. | Dominant form, unusual relationship, confident typographic presence. | Establish one arresting gesture and reduce competitors. |
| **Compression** | Whether the proposition can become one image or typographic act. | A concise relationship between subject and visual. | Replace several literal illustrations with one coherent metaphor. |
| **Duality** | Whether immediate impact and a second layer of meaning coexist. | A form that reads quickly and rewards closer attention. | Develop a meaningful secondary reading without obscuring the first. |
| **Appropriateness** | Whether the solution belongs to this subject. | A visual choice traceable to the brief rather than a fashionable treatment. | Rebuild the concept from a subject-specific fact or relationship. |
| **Humor** | Whether there is intelligent wit or conceptual pleasure. | A satisfying discovery, pun, or unexpected connection. | Look for insight rather than adding a literal joke. |
| **Reduction** | Whether each element earns its place. | Clear hierarchy and necessary supporting information. | Remove redundant graphics, competing messages, and unused treatments. |
| **Proportion** | Whether relationships feel measured and humane. | Deliberate scale, spacing, alignment, and visual rhythm. | Tune the relationships within a consistent structural framework. |

The Humor Test is about conceptual intelligence, not a demand to make every subject funny. For solemn or sensitive material, a forced joke could conflict with Appropriateness. The package does not provide a formal rule for resolving that tension; a useful review should explain it in context.

## The design process

The skill specifies seven steps for a design challenge:

1. **Deep subject immersion.** Understand the subject's core truth and the audience's feelings, fears, and aspirations. The objective is to find material for the idea before choosing its appearance.
2. **Essence extraction.** Reduce the proposition to a sentence, then to an image, then consider whether typography alone could express it.
3. **Metaphor search.** Find the conceptual connection that makes the subject visible. This is the thinking stage that prevents defaulting to decoration.
4. **Grid and structure.** Build the rational framework and justify placement. The grid supports the idea instead of becoming an arbitrary overlay.
5. **Typographic integration.** Make type work as both information and image. Typeface, scale, placement, and manipulation should contribute to meaning.
6. **Reduction.** Remove elements that do not carry necessary information or strengthen the idea.
7. **Bulletin Board Test.** Reconsider the result among competing messages. A successful isolated composition can still disappear in its intended environment.

These are reasoning instructions. The package does not perform an actual timed attention study, automatically assemble a comparison board, or generate a finished layout. Those actions require the host's tools and an explicit production task.

## The four operating modes

### Critique Mode

Use this for an existing design, identity, or set of visual materials.

The required sequence is:

1. Give explicit verdicts against all seven tests.
2. Diagnose the primary failure type.
3. Identify what to keep, discard, and reinvent.
4. Give seven specific recommendations in the prescribed format.

The listed failure types are perception, trust, hierarchy, metaphor, coherence, reduction, and signal-to-noise problems. Naming a dominant failure is useful because it separates the cause from its symptoms. For example, changing font weight may not fix a concept that communicates the wrong proposition.

### Direction Mode

Use this when developing new creative direction from a brief.

The skill calls for the full seven-step process and **three conceptual directions**. Each direction must include:

- A visual metaphor.
- A typographic approach.
- Color logic based on meaning.
- Compositional structure.
- A Casey precedent.

It then recommends one direction and defends the choice through the seven tests. Three colorways of the same idea would not provide the conceptual breadth this mode is intended to produce.

Unlike Critique Mode, this mode does not explicitly require seven recommendations after the three concepts.

### Interrogation Mode

Use this to examine a business or brand through its visual proposition before committing to execution.

The questions examine the central metaphor, attention, typographic meaning, hidden audience anxieties and aspirations, social meaning, structural logic, and removable elements. The output concludes with seven high-leverage creative recommendations.

A useful application is diagnosing why an identity feels replaceable even though its individual components are competently designed.

### System Mode

Use this when evaluating or developing a design system.

The specified areas are typography, meaningful color, grid logic, consistency across touchpoints, the balance of metaphor and structure, and reduction at the element level.

The package does not define a fixed System Mode response template, token schema, component inventory, or numerical scorecard. A practical request can supply the desired deliverable—for example, an audit grouped by typography, color, layout, and components—without implying that format is built in.

## The recommendation contract

The skill gives a specific structure for recommendations:

```text
Recommendation [N]: [Title]

The Casey Diagnosis:
The specific perceptual, visual, or conceptual failure.

The Reframe:
The underlying problem rather than its surface symptom.

The Prescription:
The concrete change to make.

The Precedent:
A relevant Casey or analogous Swiss/International Style example.

The Danger of Ignoring This:
The communication cost in this context.
```

Each field serves a different purpose. The diagnosis points to evidence; the reframe identifies the cause; the prescription turns the critique into an action; the precedent explains the design principle; the final field explains why the change matters.

Specificity should be grounded in the supplied artifact. A typeface recommendation can be useful, but an exact size should take account of actual dimensions. Historical precedents should explain a relationship or technique rather than encourage copying a famous composition.

## Example prompts

### Critique an event poster

```text
Use casey in Critique Mode on the attached poster.

Audience: undergraduate students outside the department.
Message: this public lecture makes an intimidating topic accessible.
Placement: campus noticeboards and a mobile social feed.
Required content: title, speaker, date, location, and registration URL.
Constraints: keep the organizer logo and use our licensed type family.

Run all seven tests explicitly. Identify the primary failure, explain
what to keep/discard/reinvent, and provide seven structured recommendations.
```

### Develop three directions

```text
Use casey in Direction Mode.

Brief: create a poster concept for a community repair workshop.
The central message is that repairing an object extends its story.
The audience is local residents, including beginners.
The format is an A3 two-color print. No commissioned photography.

Develop three genuinely different metaphors, including typographic
approach, color logic, structure, and a relevant precedent. Recommend
one using the seven tests. Describe concepts; no finished artwork is required.
```

### Interrogate an identity

```text
Use casey in Interrogation Mode to examine this identity presentation.
The organization helps researchers explain their work to the public.
It currently looks like a generic technology consultancy.

Find the visual proposition the identity should compress. Examine
its typography, social meaning, audience aspiration, and structural
logic. Finish with seven concrete creative recommendations.
```

### Review a system across touchpoints

```text
Use casey in System Mode on these six examples from the same brand.
Assess type hierarchy, color meaning, grid logic, component consistency,
and the balance between conceptual wit and structural discipline.

Separate system-wide causes from isolated execution errors. Explain
which recurring elements are necessary and which can be removed.
```

## Reading and using the output

Treat the primary diagnosis as the first decision. If the core metaphor is wrong, rebuilding the idea comes before spacing adjustments. If the metaphor is strong and the structure is weak, protect the concept while revising hierarchy and proportions.

For an iteration, provide the original and revised artifact and ask which test verdicts changed. This comparison method is a practical recommendation; the skill does not include persistent version tracking.

Do not treat confident language as evidence of audience performance. The skill's attention, trust, and emotional readings are critical judgments that can guide a revision. Real audience response requires observation or testing outside the package.

## Reference material and attribution

The included reference document contains seven sections: biography, influences, notable works, detailed poster analyses, quotes, legacy, and sources. It supplies examples such as *Goya: The Disasters of War*, *Russia, USA Peace*, *Body Language*, and *Intimate Architecture* to support the skill's conceptual vocabulary.

Its bibliography links to MIT, RIT, Eye Magazine, and other sources. Those are reference leads embedded in the package, not a set of sources independently verified by this README. Verify dates, quotations, authorship, and specific interpretations before reusing them in published scholarship or a historical claim.

The persona is an interpretation of a designer's approach, not an endorsement or a representation that the historical designer is speaking. The README deliberately focuses on what the package instructs rather than repeating its biographical claims as newly established facts.

## Strengths, limitations, and ambiguities

### Where the design is strong

- **A distinctive analytical lens.** It tests conceptual content and formal discipline together rather than treating visual cleanliness as sufficient.
- **Actionable recommendation structure.** The five fields encourage a connection between evidence, cause, intervention, precedent, and consequence.
- **Multiple stages of usefulness.** The four modes support work before, during, and after concept development.
- **Bundled depth.** The reference file gives the assistant material for more specific precedents without requiring it to invent examples.

### Where judgment is still required

- **No numerical calibration.** There is no defined scoring scale or release threshold. A numerical rating would be an addition by the assistant or user.
- **Uneven output specificity.** Critique and Direction are tightly specified; System Mode is comparatively open-ended.
- **An exact recommendation count.** Seven recommendations can be more than a small artifact needs. The assistant should distinguish major issues from minor opportunities instead of manufacturing equally severe problems.
- **A strong stylistic prior.** Reduction, few typefaces, grids, and typographic metaphor dominate. Other visual traditions may serve a brief better; the Appropriateness Test is an important counterweight.
- **Tone can become theatrical.** The language favors forceful critique. Its useful purpose is precision about the work, not contempt for its maker.
- **References are not visual proof.** Textual poster descriptions cannot substitute for examining the original work when historical accuracy matters.
- **No built-in production capability.** Concrete direction does not itself create editable assets, validate fonts, or inspect output files.

## Troubleshooting

| Problem | Likely cause | Better next request |
| --- | --- | --- |
| Feedback is mostly about style. | The subject and intended message are missing. | Supply the proposition and ask for Appropriateness and Compression first. |
| The review is long but not actionable. | Prescriptions are not tied to visible elements. | Request exact element-level changes in each Prescription field. |
| Every direction resembles a Swiss poster. | The historical lens has become a visual template. | Ask why each concept belongs to this brief and whether another execution would communicate better. |
| The assistant invents a precedent. | The reference file is unavailable or unused. | Provide the complete package and request a traceable reference from its catalog. |
| Important information is removed. | Reduction has overridden communication requirements. | Identify mandatory copy and require it to remain readable. |
| The system review lacks structure. | System Mode has no fixed template. | Specify the sections and touchpoints you want compared. |

## Choosing between the three skills

Choose **Casey** when the main question is “What is the idea, and how can the visual compress it?” Choose [Creative Direction](../creative-direction/README.md) for a broad scored critique, three visual concepts, or a short set of improvement moves. Choose [Loewy](../loewy/README.md) when the central concern is taste, restraint, proportion, and how advanced the design should feel for its audience.

When combining them, run one primary review at a time. Their recommendation counts and output formats differ; combining all requirements into a single response can obscure the decision you need to make.

## Review checklist

A faithful Casey critique should have:

- Explicit coverage of all seven tests.
- A clear primary diagnosis grounded in the supplied work.
- An explanation of what to preserve, discard, and reinvent.
- Seven recommendations using all five required fields.
- Prescriptions that respect the brief and production constraints.
- Relevant precedents rather than decorative name-dropping.
- A connection between the conceptual idea and the structural choices.

For Direction Mode, instead check for three complete concepts and a defended recommendation. For System Mode, check all six specified areas rather than expecting an undocumented numerical score.

---

[Back to repository overview](../../README.md)
