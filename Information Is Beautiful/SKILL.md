---
name: information-is-beautiful
description: >
  Create concept-driven, editorial-quality data visualisations and
  infographics inspired by the principles of Information Is Beautiful
  and David McCandless. Use when turning data, research, ideas, or
  written reports into compelling visual explanations, charts,
  diagrams, interactive graphics, or polished infographic assets.
---

# Information Is Beautiful: Concept-Driven Data Visualisation

## Mission

Transform complex information into visual explanations that are:

- Accurate.
- Interesting.
- Insightful.
- Beautiful.
- Useful.
- Memorable.

Do not merely decorate a dataset. Discover what is worth communicating,
then design the clearest and most engaging way to communicate it.

The guiding framework is:

1. Information — What is true, relevant, and meaningful?
2. Function — What must the audience understand or do?
3. Visual form — What visual language makes the information clear and appealing?
4. Story — What is the central insight, narrative, or question?

A successful graphic balances all four.

## Operating principles

### 1. Begin with the concept, not the chart

Before selecting a visualisation, answer:

- What is the subject?
- What is the interesting question?
- What is surprising, important, beautiful, absurd, or revealing?
- What should the viewer understand after looking at the graphic?
- Who is the audience?
- What decision, feeling, or action should the graphic support?

Write a one-sentence concept:

> This graphic reveals [insight] by showing [relationship] so that
> [audience] understands [meaning].

If the concept is weak, improve the question before designing.

### 2. Find the story inside the data

Explore the dataset for:

- Contrasts.
- Trends.
- Outliers.
- Rankings.
- Clusters.
- Proportions.
- Changes over time.
- Unexpected relationships.
- Scale differences.
- Human relevance.
- Counterintuitive findings.

Look for a meaningful pattern, not just the most visually convenient pattern.

Generate several possible stories before committing to one.

For each candidate story, record:

- The claim.
- The evidence.
- The intended audience.
- Why it matters.
- The most suitable visual form.

Do not manufacture a narrative that the data does not support.

### 3. Research and curate information

Treat research as part of design.

- Prefer primary sources and authoritative datasets.
- Identify the date, population, units, methodology, and limitations.
- Check definitions before comparing values.
- Verify surprising findings.
- Record sources and provenance.
- Distinguish facts, calculations, estimates, assumptions, and interpretations.
- Remove irrelevant data that does not support the story.
- Preserve uncertainty where it affects meaning.

Do not use visual polish to conceal weak evidence.

### 4. Choose the visual form conceptually

Do not default to a bar chart.

Explore multiple possible representations:

- Timeline.
- Flow diagram.
- Network.
- Matrix.
- Treemap.
- Proportional shapes.
- Connected scatterplot.
- Small multiples.
- Map.
- Radial or circular structure.
- Annotated chart.
- Comparison graphic.
- Pictorial or metaphorical visualisation.
- Interactive exploration.

Select the form that best expresses the concept.

Use familiar chart forms when they communicate more clearly.
Use unusual forms only when they provide a genuine conceptual or
communication advantage.

Every visual decision must have a reason.

### 5. Design for comprehension

The viewer should understand the main point without needing a
technical manual.

Prioritise:

- A clear headline.
- An obvious visual hierarchy.
- Meaningful labels.
- Direct annotations.
- Useful comparisons.
- Consistent scales.
- Readable typography.
- Sufficient contrast.
- Logical grouping.
- A clear entry point.
- A concise explanation of the insight.

Use annotations to explain what matters, not to repeat every data point.

Avoid:

- Decorative complexity.
- Excessive legends.
- Unexplained symbols.
- Ambiguous colour scales.
- Unnecessary axes.
- Dense labels that obscure the graphic.
- Visual effects that imply unsupported precision.
- A title that merely names the dataset.

### 6. Make the graphic beautiful with purpose

Beauty should reinforce understanding.

Aim for:

- Strong composition.
- Deliberate spacing.
- A coherent visual system.
- Carefully chosen typography.
- Restrained, meaningful colour.
- Balanced density.
- Clear focal points.
- Distinctive but appropriate visual metaphors.
- A polished editorial finish.

Use colour to encode categories, emphasis, sequence, or meaning.
Do not add colour simply to make the graphic look lively.

Use visual repetition to establish rhythm and structure.

Make the graphic feel designed, not like a default chart exported
from a spreadsheet.

### 7. Use scale and comparison intelligently

Large numbers are difficult to understand in isolation.

Whenever appropriate:

- Compare quantities using a common scale.
- Use relatable reference points.
- Show proportions and ratios.
- Translate abstract magnitudes into meaningful comparisons.
- Explain the denominator.
- Make differences visible without exaggerating them.
- Preserve the distinction between absolute and relative values.

Do not use misleading area, volume, perspective, or distorted shapes
to create a dramatic effect.

If using circles, icons, or pictograms to represent quantities,
ensure the encoding is understandable and reasonably proportional.
Explain any non-obvious encoding.

### 8. Build a visual grammar

Before producing the final graphic, define:

- Canvas dimensions and aspect ratio.
- Layout and reading order.
- Grid and alignment.
- Typography hierarchy.
- Colour palette.
- Data encoding.
- Annotation style.
- Iconography.
- Background and surface treatment.
- Source and footnote treatment.

Use a small, consistent set of visual rules.

The graphic should have a recognisable visual voice without becoming
a rigid template.

### 9. Work through sketches and alternatives

Do not jump directly to the finished design.

Produce at least three rough concepts where the problem warrants it.

For each concept, consider:

- What is the visual metaphor?
- What does the viewer see first?
- How does the eye move through the graphic?
- What is the central comparison?
- What is gained or lost by this representation?
- Can the graphic be understood quickly?
- Does the design still work without decorative elements?

Choose the strongest concept based on communication, not personal
attachment to an attractive idea.

### 10. Select tools based on the output

Choose the simplest tool that can achieve the required quality.

- Use Python for data cleaning, statistical analysis, validation,
  repeatable calculations, and exploratory plotting.
- Use SVG for precise diagrams, custom shapes, and editorial
  illustrations.
- Use HTML, CSS, and JavaScript for interactive graphics.
- Use D3 or another suitable visualisation library for custom
  interactive data-driven graphics.
- Use a charting library for standard charts when it provides the
  necessary control.
- Use image-generation tools only for decorative or illustrative
  artwork, not for precise numerical encodings.
- Use design software or vector tooling when the final composition
  requires detailed art direction.

Separate data processing from visual styling so that the graphic
can be updated without redoing the analysis.

## The production workflow

### Phase 1: Brief

Create a short creative brief containing:

- Topic.
- Audience.
- Core question.
- Main insight.
- Desired action or takeaway.
- Format.
- Constraints.
- Available data.
- Source requirements.

### Phase 2: Research

Collect and verify the evidence.

Create a data dictionary and source register.

Identify gaps, uncertainties, inconsistent definitions, and
potentially misleading comparisons.

### Phase 3: Concept generation

Generate several candidate stories and visual metaphors.

Write a one-sentence concept for each.

Rank them according to:

- Insight strength.
- Relevance.
- Visual potential.
- Comprehension.
- Accuracy.
- Originality.
- Feasibility.

### Phase 4: Data preparation

Clean and validate the data.

Document:

- Transformations.
- Calculations.
- Filters.
- Aggregations.
- Missing values.
- Assumptions.
- Units.
- Normalisations.

Keep the raw data separate from derived data.

### Phase 5: Visual prototyping

Create rough visual prototypes.

Test different:

- Encodings.
- Layouts.
- Scales.
- Annotation systems.
- Colour schemes.
- Levels of detail.

Do not spend excessive time polishing a weak concept.

### Phase 6: Design and execution

Build the selected graphic.

Prioritise the main story, visual hierarchy, and readability.

Add detail only when it improves understanding or exploration.

### Phase 7: Validation

Check:

- Every number.
- Every label.
- Every unit.
- Every source.
- Every calculation.
- Every visual encoding.
- Every comparison.
- Every legend.
- Every annotation.
- Accessibility and colour contrast.
- Mobile or small-format readability, where relevant.

Confirm that the visual does not imply a stronger conclusion
than the evidence supports.

### Phase 8: Editorial refinement

Ask:

- Is the main insight immediately apparent?
- Is the headline compelling and accurate?
- Does the graphic reward closer inspection?
- Is anything unnecessary?
- Is anything confusing?
- Does the visual form add meaning?
- Is the design distinctive without becoming distracting?
- Would a reader remember the insight tomorrow?

Revise until the graphic communicates with clarity and character.

## Output requirements

When asked to create a visualisation, return:

1. A concise concept statement.
2. The intended audience and takeaway.
3. The data and source assumptions.
4. The selected visual form and rationale.
5. The visual design specification.
6. The implementation or finished graphic.
7. A validation summary.
8. Source notes and limitations.

When the user requests only the finished graphic, keep the explanation
brief but still ensure the graphic is accurate and well-founded.

## Quality checklist

Before delivery, verify:

- [ ] The graphic has one clear central idea.
- [ ] The data is accurate and appropriately sourced.
- [ ] The visual form fits the concept.
- [ ] The main insight is easy to find.
- [ ] The encoding is understandable.
- [ ] The scale and comparisons are honest.
- [ ] The typography is readable.
- [ ] Colour has a purpose.
- [ ] The composition has a clear hierarchy.
- [ ] The graphic is attractive without unnecessary decoration.
- [ ] Annotations add insight.
- [ ] Uncertainty and limitations are visible where necessary.
- [ ] The graphic works at its intended display size.
- [ ] The final result is useful, insightful, and memorable.

## Style boundaries

Aim for the qualities associated with Information Is Beautiful:

- Concept-led.
- Editorial.
- Curious.
- Insightful.
- Clear.
- Visually inventive.
- Data-informed.
- Human-centred.
- Playful when appropriate.
- Beautiful through purposeful design.

Do not copy specific copyrighted graphics, illustrations, or layouts.
Learn from the underlying principles and create original work.

Do not confuse decorative complexity with sophistication.

Do not sacrifice truth, clarity, or usability for aesthetic effect.
