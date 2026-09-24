---
name: dataviz-fundamentals
description: Use when choosing, building, critiquing or fixing a static chart, map or table, applying the principles of Wilke's Fundamentals of Data Visualization.
---

# Data visualisation fundamentals

Wilke-derived working heuristics for static figures. Source: Claus O. Wilke, *Fundamentals of Data Visualization* (O'Reilly, 2019), https://clauswilke.com/dataviz/, CC BY-NC-ND 4.0. All paraphrased.

**Provenance.** The pipeline (section 1) and critique format (section 9) are this skill's own. Sections 2 to 8 synthesise Wilke's guidance with operational heuristics; claims marked *(own)* are explicitly this skill's.

**Tiers.** Every rule carries one. **H** hard: breaking it creates a materially false or ambiguous representation; always fix unless the breach is only superficial. **D** default: depart only with a stated reason. **J** judgement: weigh audience, data and message; say why.

**Scope and precedence.** Static figures. For dashboards or interactive pages, apply this skill to each view; interaction design (hover, filtering, animation, responsive layout) is out of scope. If a brand palette, design system or another chart skill is active, its colours and styling win; this skill still governs chart choice, encoding honesty, colour *roles* (section 4) and critique.

---

## 1. Pipeline

Run once when building. When reviewing, run it on the existing figure. Address every material "no" with either a fix or an explicit reason for accepting the trade-off.

| Step | Do | Check |
|---|---|---|
| 1. Finding | State it in one sentence. None means exploring: make rough plots. | Is there a single point? |
| 2. Reader task | Name it: compare, locate, estimate, recognise a pattern, follow change. One message can imply several tasks. | Is the task explicit? |
| 3. Channel | Put that task on the strongest channel. Standard perception ranking *(own)*: position on a shared axis, then length, then angle or area, then colour. Demote other variables to colour, size, shape or panels. | Is the key comparison on a common axis? |
| 4. Faithfulness | Apply section 2. A perceptually strong but unfaithful encoding is still wrong. | Could a reasonable reader draw a materially wrong conclusion? |
| 5. Alternatives *(own)* | If the choice is ambiguous, build two options and compare them (section 1a); keep the one that makes step 2 faster and more accurate. | Was a real alternative considered? |
| 6. Hierarchy *(own)* | Finding first, structure second, context third; grids and metadata recede. Use accent colour and annotation. | Is the pattern visible within seconds? |
| 7. Labels and claims | Section 6. | Are axes titled with units? Does the title claim no more than the data support? |
| 8. Colour | Section 4. | Does every colour do a job, and survive CVD and greyscale checks? |
| 9. Final size | Check at real output size (section 1a). | Is text legible and balanced with the marks? |

### 1a. Checks without eyes *(own)*

Visual checks must actually run. Never claim a check you did not perform; if a check was impossible, say so in the output.

| Check | If you can render and view images | If you cannot |
|---|---|---|
| Compare alternatives (step 5) | Render both, view them, pick one and say why | Describe both encodings and reason from step 3's ranking |
| Final size (step 9) | Export at the real output width and view it | Compute: text height should be at least about 2% of figure width at output size; flag if smaller |
| CVD (step 8) | Simulate deuteranopia, protanopia and tritanopia (e.g. Python `colorspacious` or `daltonlens`) and view results | Confirm no pair of categories differs only in red against green, and that redundant coding exists where colour carries meaning |
| Greyscale (step 8) | Convert to greyscale and view | Compute relative luminance of each colour; categories that must be told apart should differ clearly |

**Critique style.** Follow the format in section 9. Wilke's labels help: *wrong* (misrepresents data), *bad* (correct but hard to read or misleading), *ugly* (readable but aesthetically poor). The boundaries are fluid; they are diagnostic words, not scores.

---

## 2. Faithful encoding

| Rule | Tier |
|---|---|
| Scales are consistent and unambiguous: the same data value always gets the same visual value, and the reader can tell what a visual value represents. Binning and rounding are fine when the grouping is explicit. | H |
| A filled shape read as a magnitude must be proportional to it. Bars encoding amounts on a linear axis start at zero so their lengths stay proportional to the values. | H |
| Shading under a line needs a zero baseline. | D |
| Points and unfilled lines may use a zoomed axis; do not exaggerate small changes. | J |
| To show small differences, show them directly rather than making the reader subtract two large values. | D |
| On a log axis, prefer dots or other position marks; avoid bars unless their meaning is made explicit. | J |
| Stack only when totals mean something; never stack medians or averages. | H |
| Never double-count overlapping categories in a chart that implies a whole. | H |
| Density curves must not extend into impossible values; they can also show structure sparse data do not support. | H |
| Excessive jitter misplaces data. | H |
| Small multiples share axes; if they cannot, say so in the caption. | D |
| Moving an inset region is fine; rescaling it misleads. | H |
| No decorative 3D (tilted pies, 3D bars). | D |
| 3D position scales only for interactive views or genuine 3D objects. | D |

**Axes.**
- Different units: aspect ratio is a choice; do not inflate change (J). Same units: square grid (D).
- Log scales when multiplicative structure is the point or values span magnitudes (J). Label in original units, never an unlabelled "log(x)" (D). Zero cannot appear. For ratios, 1 means no change.
- Square-root scales allow zero but steps lack constant meaning (J). Polar coordinates suit cyclic data (J).
- Map projections: equal-area when sizes are compared (D).

**Variables by meaning, not type.** Counts usually sit on continuous axes (D). Ordered categories (months, age bands, ratings) keep their natural order and are never sorted by value (H). Unordered categories sort by value (D). Numeric labels (postcodes, IDs) are categories (H).

---

## 3. Task to representation

Prefer the representation that lets the reader make the required comparison in the fewest perceptual steps. The table gives starting points (J), not a lookup.

| Reader must... | Start with | Avoid |
|---|---|---|
| Compare amounts | Bars sorted by value if categories are unordered, in natural order if ordered; dots if zero is irrelevant; horizontal bars for long labels | Rotated labels; alphabetical order |
| Compare across two groupings | Small multiples; grouped bars, key comparison on position | Many legend colours |
| See one distribution | Histogram or density at several bin widths or bandwidths; ECDF or q-q for skew or precision | One default setting |
| Compare few distributions | Transparent densities; each group against the total; back-to-back for two | Stacked or overlapping histograms |
| Compare many distributions | Boxplots, violins (enough data), sina or jittered points, ridgelines | Mean with error bars as spread |
| See parts of a whole | Pie for few parts or simple fractions; side-by-side bars to compare parts; stacked bars over many sets or time | Pies of similar slices or across conditions |
| See nested parts | Mosaic (crossed variables), treemap (hierarchy), parallel sets (3+ variables); print counts on areas | Double-counting |
| Relate two quantities | Scatter, with a fitted form if the trend is the point | Important variable on bubble size |
| Relate many quantities | Scatter matrix; correlogram (size by abs(r)); PCA with loadings and scores | 3D scatter |
| Compare pairs | Scatter with x = y line; slopegraph for few cases | Grid without reference line |
| Follow change | Line graph, directly labelled; two aligned line charts for two responses | Unconnected dots; unmarked connected scatter |
| Locate in space | Choropleth of rates or other normalised, comparable values, 4 to 6 colour bins; cartogram or equal tiles when area misleads | Raw totals over unequal regions |

**Trends.**
- Smoothers (moving average, LOESS, splines) change with settings, especially at the edges: try several (D).
- Prefer forms with meaningful parameters (D). Linearise to test: exponential growth is straight on a log y axis, power laws on log-log.
- If theory implies multiplicative structure, consider fitting on the transformed scale; check residuals (J).

**Overplotting.** Transparency plus slight jitter for moderate overlap (D). 2D hex bins or contours for large data (D). Colour-coded contours only for two or three well-separated groups; otherwise panels (D).

---

## 4. Colour

| Job | Scale | Rule | Tier |
|---|---|---|---|
| Distinguish unordered groups | Qualitative | Distinct, equal weight, no implied order | D |
| Represent values | Sequential | Lightness changes steadily one way; natural gradients (dark blue to light yellow) | H |
| Show deviation from a meaningful midpoint | Diverging | Balanced sides, light centre; use when deviation is the point | J |
| Highlight | Accent | Grey base, few strong accents | D |

- Three to five categories are generally easy to distinguish; around eight is already hard. Beyond that, label directly, group, or re-encode (D).
- No decorative colour; no large saturated areas (D). No rainbow scales for values (H).
- Do not rely on red against green alone (D). Pairs differing in more than one perceptual channel are more robust. Thin lines and small marks weaken every colour difference.
- Redundant coding (shape for points, direct labels for lines) when colour alone may fail; skip it where colour clearly works (J). Avoid dashed lines as a second code (D).

**Okabe-Ito palette** (designed for colour-vision deficiency). Default qualitative palette when no brand palette applies (D). Qualitative use only, never as a sequential or diverging scale (H).

```
OKABE_ITO = ["#E69F00", "#56B4E9", "#009E73", "#F0E442",
             "#0072B2", "#D55E00", "#CC79A7", "#000000"]
# orange, sky blue, bluish green, yellow, blue, vermilion, reddish purple, black
```

Application *(own)* (D): assign colours to categories consistently and keep each category's colour fixed across every figure in a set. Never cycle past eight; re-encode instead. Avoid yellow for text or thin lines on white; keep it for fills. Use black or grey for reference lines or an "other" group. A safe palette is not proof: still run the CVD check in section 1a.

---

## 5. Uncertainty

| Question | Show |
|---|---|
| How spread out are observations? | The distribution or raw points |
| How precise is an estimate? | Interval, or sampling or posterior distribution |
| Do two estimates differ? | The difference with its interval |
| How uncertain is a fitted curve? | Band, or sampled alternative curves |
| What might happen (lay audience)? | Frequency framing; quantile dot plot with few dots (about 10 to 20 *(own)*) |

- Label every error bar and band: SD, SE, or which interval (H).
- SD is spread among observations; SE is the precision of an estimate. For a mean, a 95% interval is roughly two SE either side, as an approximation.
- Frequentist intervals describe a procedure's long-run coverage; Wilke links them to rejecting a null. Bayesian credible intervals locate the parameter given model, prior and data.
- Do not judge significance from overlapping bars; plot the difference (D).
- Point plus error bars summarises an estimate, not a distribution (D).
- Readers treat interval ends as hard limits; graded intervals counter this at the cost of clutter (J).
- Animated outcomes: quick cuts, representative frames (D).

---

## 6. Labels, titles, layout

- **Title:** one clear primary title, placed inside a standalone graphic or in the document's caption, as the format dictates (D). State the point, never beyond the evidence; "associated with" is not "causes" *(own)* (H).
- Captions sit below figures and above tables (D). Include the data source (D).
- Title axes and legends with variable and units; omit only when self-evident (D).
- Prefer direct labels where they spare legend-matching; if a legend stays, order it like the data (D). Integrate a colour key into the axis when one variable drives both (D).
- Compound figures: discreet panel letters, aligned axes, one visual language across panels (D).
- Declutter without stripping context: light grids perpendicular to the key variable; a single reference line or x = y diagonal often beats a grid (J).
- Filled shapes and solid points, not outlines (D).
- Default software text is usually too small; check it (section 1a) (D).
- **Tables:** no vertical rules or rules between rows; text left, numbers right with consistent decimals; headers aligned with their columns (D).

---

## 7. Sets of figures

- One figure, one point (D). Build up to complex figures via a simpler one (D).
- Order the set as a story or lead with the conclusion (J).
- Keep the visual language constant but vary chart types between sections (D).

---

## 8. Delivery

Production defaults, not perception rules (D): vector (PDF, SVG) for print, PNG for screens, never JPEG; script figures; keep styling in a shared theme separate from content.

---

## 9. Critique format *(own)*

When reviewing a figure, answer in this shape:

1. **Verdict:** one sentence. Is the finding clear and the encoding faithful?
2. **Issues, ranked:** at most five, H first, then by impact on the reader. For each: the problem, the consequence for the reader, the tier, and the smallest fix.
3. **Checks run:** list the section 1a checks performed and any you could not perform.
4. **Keep:** what already works, in one line, so fixes do not break it.

When building, state the finding, the reader task and the chosen channel in one line each before the code, then run the checks.

---

## 10. Examples

- **Small income differences, author wants drama:** bars must start at zero (H). If change is the story, plot change from a base year.
- **Five near-equal market shares over three years:** pies and stacked bars defeat comparison; use side-by-side bars or one panel per firm.
- **Monthly sales, bars sorted tallest first:** wrong for an ordered category. Restore calendar order (H); highlight the peak month with an accent colour instead.
- **Correlation titled "X causes Y":** fix the title to state an association unless the design supports causation (H).
