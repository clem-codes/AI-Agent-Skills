# SKILL: Financial Times (FT) Visual Vocabulary Framework for Data Visualisation

## Purpose

Use the Financial Times Visual Vocabulary as a reference framework for selecting visual forms for data visualisation.

The FT Visual Vocabulary was created by the Financial Times Visual Journalism Team to help designers and journalists select appropriate visual symbology and improve chart literacy. It is intended to help people recognise opportunities to use visualisations effectively alongside words, rather than to provide an exhaustive course in chart construction.

The framework is organised around nine broad analytical categories:

1. Deviation
2. Correlation
3. Ranking
4. Distribution
5. Change over Time
6. Part-to-Whole
7. Magnitude
8. Spatial
9. Flow

The categories describe analytical purposes rather than mutually exclusive chart classes. Some visual forms occur in more than one category because they can answer different analytical questions.

---

# 1. Source-Faithful FT Categories

## 1.1 Deviation

### FT purpose

Emphasise variations (+/-) from a fixed reference point.

The reference point is typically zero, but can also be:

- a target
- a long-term average
- another meaningful baseline

Deviation can also express sentiment such as positive / neutral / negative.

### FT examples

- Trade surplus / deficit
- Climate change

### FT visual forms

- Diverging bar
- Diverging stacked bar
- Spine chart
- Surplus/deficit filled line

### FT-specific guidance

**Diverging bar**
- A standard bar chart capable of handling positive and negative magnitude values.

**Diverging stacked bar**
- Particularly useful for survey responses involving sentiment such as disagree / neutral / agree.

**Spine chart**
- Splits a single value into two contrasting components, such as male/female.

**Surplus/deficit filled line**
- Uses shaded area to show a balance against a baseline or between two series.

---

# 1.2 Correlation

### FT purpose

Show the relationship between two or more variables.

Be mindful that readers may interpret a displayed relationship as causal unless the visualisation or accompanying text makes the nature of the relationship clear.

### FT examples

- Inflation and unemployment
- Income and life expectancy

### FT visual forms

- Scatterplot
- Line + Column
- Connected scatterplot
- Bubble
- XY heatmap

### FT-specific guidance

**Scatterplot**
- Standard method for showing the relationship between two continuous variables, each represented by its own axis.

**Line + Column**
- Shows the relationship between an amount represented by columns and a rate represented by a line.

**Connected scatterplot**
- Usually shows how the relationship between two variables changes over time.

**Bubble**
- Similar to a scatterplot but adds a third variable through circle size.

**XY heatmap**
- Shows patterns between two categories of data.
- Useful for patterns but less effective for showing fine differences in amounts.

---

# 1.3 Ranking

### FT purpose

Use when an item's position in an ordered list is more important than its absolute or relative value.

Points of particular interest may be highlighted.

### FT examples

- Wealth
- Deprivation
- League tables
- Constituency election results

### FT visual forms

- Ordered bar
- Ordered column
- Ordered proportional symbol
- Dot strip plot
- Slope
- Lollipop chart

### FT-specific guidance

**Ordered bar / ordered column**
- Standard bars or columns sorted into order make rank easy to see.

**Ordered proportional symbol**
- Useful when there are large variations between values or fine differences are not important.

**Dot strip plot**
- Space-efficient method of laying out ranks across multiple categories.

**Slope**
- Useful for showing how ranks have changed over time or vary between categories.

**Lollipop**
- Draws attention to the data value while also communicating rank and value.

---

# 1.4 Distribution

### FT purpose

Show values in a dataset and how often they occur.

The shape or skew of the distribution can highlight lack of uniformity or equality.

### FT examples

- Income distribution
- Population age/sex distribution

### FT visual forms

- Histogram
- Boxplot
- Violin plot
- Population pyramid
- Dot strip plot
- Dot plot
- Barcode plot
- Cumulative curve

### FT-specific guidance

**Histogram**
- Standard method for showing a statistical distribution.
- Small gaps between columns help emphasise the shape.

**Boxplot**
- Summarises distributions using the median and range.

**Violin plot**
- Similar to a boxplot but useful for more complex distributions that cannot be adequately summarised by a simple average.

**Population pyramid**
- Shows age and sex population breakdowns using back-to-back histograms.

**Dot strip plot**
- Shows individual values in a distribution.
- Can become problematic when many observations share the same value.

**Dot plot**
- Can show change or range (minimum/maximum) across multiple categories.

**Barcode plot**
- Displays all observations and works particularly well when individual values need highlighting.

**Cumulative curve**
- Shows distributional inequality using cumulative frequency against a measured variable.

---

# 1.5 Change Over Time

### FT purpose

Give emphasis to changing trends.

These can range from short intra-day movements to extended series covering decades or centuries.

The chosen time period should provide suitable context for the reader.

### FT examples

- Share-price movements
- Economic time series

### FT visual forms

- Line
- Column
- Line + Column
- Stock price
- Slope
- Area chart
- Fan chart (projection)
- Connected scatterplot
- Calendar heatmap
- Priestley timeline
- Circle timeline
- Seismogram

### FT-specific guidance

**Line**
- Standard way to show a changing time series.
- If data are irregular, markers can represent individual observations.

**Column**
- Works well for change over time, generally with only one series.

**Line + Column**
- Shows the relationship over time between an amount and a rate.

**Stock price**
- Focuses on day-to-day activity, including opening/closing and high/low values.

**Slope**
- Useful when changing data can be simplified to two or three points without losing an important part of the story.

**Area chart**
- Useful for changes to a total.
- Changes in individual components can be difficult to see.

**Fan chart**
- Shows uncertainty in future projections, usually increasing further into the projection period.

**Connected scatterplot**
- Shows changing data for two variables when there is a relatively clear pattern of progression.

**Calendar heatmap**
- Shows temporal patterns across daily, weekly or monthly observations at the expense of precise quantitative comparison.

**Priestley timeline**
- Useful when date and duration are important elements of the data.

**Circle timeline**
- Shows discrete values of varying size across multiple categories.

**Seismogram**
- An alternative to a circle timeline for series with large variations.

---

# 1.6 Part-to-Whole

### FT purpose

Show how a single entity is broken down into its component elements.

If the reader is solely interested in the size of the components, consider a magnitude-type visualisation instead.

### FT examples

- Fiscal budgets
- Company structures
- National election results

### FT visual forms

- Stacked column
- Proportional stacked bar
- Pie
- Donut
- Treemap
- Voronoi
- Arc
- Gridplot
- Venn
- Waterfall

### FT-specific guidance

**Stacked column**
- Simple way to show part-to-whole relationships.
- Can become difficult to read with many components.

**Proportional stacked bar**
- Shows size and proportion simultaneously when the data are not too complicated.

**Pie**
- Common way of showing part-to-whole.
- Precise comparison of segment sizes is difficult.

**Donut**
- Similar to a pie chart.
- The centre can provide space for additional information such as the total.

**Treemap**
- Intended for hierarchical part-to-whole relationships.
- Can become difficult to read with many small segments.

**Voronoi**
- Turns points into areas, where each area is associated with its nearest central point.

**Arc**
- A hemicycle, often used to visualise political results in parliaments.

**Gridplot**
- Useful for percentage information.
- Works particularly well with whole-number percentages and multiple layouts.

**Venn**
- Generally intended for schematic representation.

**Waterfall**
- Useful for part-to-whole relationships where some components are negative.

---

# 1.7 Magnitude

### FT purpose

Show size comparisons.

Magnitude can be:

- Relative — the reader primarily needs to see which is larger.
- Absolute — the reader needs to see fine differences.

These visualisations usually show a counted number such as:

- barrels
- dollars
- people

rather than a calculated rate or percentage.

### FT examples

- Commodity production
- Market capitalisation

### FT visual forms

- Column
- Bar
- Paired column
- Paired bar
- Proportional stacked bar
- Proportional symbol
- Isotype (pictogram)
- Lollipop chart
- Radar chart
- Parallel coordinates

### FT-specific guidance

**Column**
- Standard method for comparing size.
- The FT specifies that the axis must start at zero.

**Bar**
- Standard size comparison.
- Particularly useful when the data are not time series and category labels are long.

**Paired column**
- Allows multiple series.
- Can become difficult with more than two series.

**Paired bar**
- Equivalent comparison form when horizontal orientation is preferable.

**Proportional stacked bar**
- Shows size and proportion simultaneously when the data are not too complicated.

**Proportional symbol**
- Useful when values vary substantially or fine differences are not important.

**Isotype / pictogram**
- Can be effective in some situations.
- Should be used with whole numbers rather than fractional pictorial units.

**Lollipop**
- Draws attention to the value more than a standard bar or column.
- Does not necessarily have to start at zero, although zero is preferable.

**Radar chart**
- Compact way to show values across multiple variables.
- Variables should be organised in a meaningful order.

**Parallel coordinates**
- Alternative to radar charts.
- Variable arrangement is important and highlighting values is often useful.

---

# 1.8 Spatial

### FT purpose

Use when precise locations or geographical patterns in the data are more important to the reader than anything else.

### FT examples

- Locator maps
- Population density
- Natural resource locations
- Natural disaster risk/impact
- Catchment areas
- Variation in election results

### FT visual forms

- Basic choropleth
- Proportional symbol
- Flow map
- Contour map
- Equalised cartogram
- Scaled cartogram
- Dot density
- Heat map

### FT-specific guidance

**Basic choropleth**
- Standard approach to putting data on a map.
- Should use rates rather than totals and an appropriate base geography.

**Proportional symbol**
- Use for totals rather than rates.
- Small differences may be difficult to see.

**Flow map**
- Shows unambiguous movement across a map.

**Contour map**
- Shows areas of equal value.
- Deviation colour schemes can show positive and negative values.

**Equalised cartogram**
- Converts geographic units into regular, equally sized shapes.
- Useful where each voting region or spatial unit should have equal visual weight.

**Scaled cartogram**
- Stretches or shrinks areas according to a specified value.

**Dot density**
- Shows locations of individual events or locations.
- Patterns should be explicitly annotated where necessary.

**Heat map**
- Uses grid-based data values mapped to an intensity colour scale.
- Similar to a choropleth but not constrained to administrative or political units.

---

# 1.9 Flow

### FT purpose

Show volumes or intensity of movement between two or more states or conditions.

Flows can represent:

- logical sequences
- geographical movement
- movement of funds
- trade
- migrants
- lawsuits
- information
- relationships

### FT visual forms

- Sankey
- Waterfall
- Chord
- Network

### FT-specific guidance

**Sankey / river plot**
- Shows changes in flows from one condition to at least one other.
- Particularly useful for tracing eventual outcomes through complex processes.

**Waterfall**
- Shows sequencing through a flow process, typically budgets.
- Can include positive and negative components.

**Chord**
- Shows two-way flows in a matrix and can illustrate net winners.

**Network**
- Shows the strength and interconnectedness of relationships of varying types.

---

# 2. Important Classification Rules

The FT taxonomy contains deliberate overlap.

Do not force a visual form into one category when the FT source places it in more than one.

Examples:

- **Line + Column** appears under both Correlation and Change over Time.
- **Connected scatterplot** appears under Correlation and Change over Time.
- **Slope** appears under Ranking and Change over Time.
- **Proportional stacked bar** appears under Part-to-Whole and Magnitude.
- **Waterfall** appears under Part-to-Whole and Flow.
- **Flow map** appears under Spatial.
- Some visual forms can naturally answer more than one analytical question even where the FT list places them in only one category.

The category should therefore be interpreted as the **primary analytical purpose in the particular use case**, not as an exclusive classification.

---

# 3. Agent Selection Layer

The following is an agent-oriented extension of the FT taxonomy. It is **decision logic added to this skill**, not additional FT taxonomy.

## Step 1 — Identify the reader's question

Determine what the reader primarily needs to understand:

- Difference from a reference
- Relationship between variables
- Position in a ranking
- Distribution
- Change over time
- Composition
- Magnitude
- Geographic pattern
- Movement or relationships

If the question is ambiguous and the ambiguity would materially change the recommendation, ask for clarification.

Otherwise state the assumption being made.

---

## Step 2 — Identify the data structure

Inspect:

- Quantitative variables
- Categorical variables
- Ordinal variables
- Dates/times
- Geographic identifiers
- Origins/destinations
- Hierarchies
- Groups/subgroups
- Positive/negative values
- Totals/components
- Uncertainty/forecasts
- Number of observations
- Number of categories
- Number of series

Do not select a chart merely because a particular field exists.

Examples:

- Dates do not automatically imply a line chart.
- Countries do not automatically imply a map.
- Percentages do not automatically imply a pie chart.
- Two quantitative variables do not automatically imply a scatterplot.

---

## Step 3 — Identify primary and secondary analytical purposes

Assign:

- One primary FT category where possible.
- Secondary categories where they materially affect the visualisation.

If two analytical purposes are equally important, prefer a form that can communicate both without introducing unnecessary complexity.

---

## Step 4 — Generate candidates

Select 2–4 plausible visual forms from the FT vocabulary.

Do not return the entire category as a list of possibilities.

---

## Step 5 — Apply constraints

Consider:

- Number of observations
- Number of categories
- Number of series
- Need for precise comparison
- Long category labels
- Overplotting
- Positive/negative values
- Time granularity
- Geographic structure
- Hierarchy
- Uncertainty
- Accessibility
- Audience familiarity

---

## Step 6 — Select the primary visualisation

Choose the visual form that best supports the reader's primary analytical task.

Prefer the simplest suitable form when competing options communicate the information equally well.

---

## Step 7 — Explain the visual encoding

Explain what the reader is expected to compare:

- Position
- Length
- Area
- Angle
- Colour
- Connection
- Spatial position
- Temporal progression

Do not add visual dimensions simply because the chart permits them.

---

## Step 8 — State important limitations

Where relevant, warn about:

- Correlation versus causation
- Difficulty comparing segments in stacked charts
- Difficulty comparing angles/areas precisely
- Overplotting
- Dual-axis interpretation
- Geographic-area distortion
- Raw counts versus rates on maps
- Uncertainty in projections
- Excessive categories or series

---

# 4. General Decision Principles

These principles are **agent guidance**, not claims that every item is part of the FT taxonomy itself.

### 4.1 Start with the question

Do not start with:

> “What chart can I make from this dataset?”

Start with:

> “What does the reader need to understand?”

### 4.2 Data structure constrains; analytical purpose selects

The presence of time, geography, categories or multiple variables does not independently determine the chart.

### 4.3 Prefer appropriate visual encodings

When precise comparison matters, favour visual encodings that make comparison straightforward.

### 4.4 Do not overcomplicate

Additional variables, dimensions and specialised chart forms should only be introduced when they materially improve the answer.

### 4.5 Distinguish magnitude from ranking

Ask:

> Is the important thing the size of the values, or their position in an ordered list?

### 4.6 Distinguish composition from component comparison

If the question is:

> What makes up the whole?

consider Part-to-Whole.

If the question is:

> Which component is largest?

consider Magnitude or Ranking.

### 4.7 Distinguish geographic data from spatial questions

A geographic identifier does not automatically make a map appropriate.

Use Spatial when geographic location or geographic pattern is itself important.

### 4.8 Distinguish temporal data from temporal questions

A date column does not automatically make a time-series chart appropriate.

Use Change over Time when temporal progression is part of the analytical story.

---

# 5. Common Failure Modes

The agent should screen candidate visualisations for obvious problems.

### Overplotting

Too many observations or series make individual marks difficult to distinguish.

### Excessive categories

Too many categories can make a chart difficult to scan or label.

### Long labels

Horizontal bars may be preferable when category names are long.

### Dual axes

Use cautiously. Different scales can encourage misleading visual comparisons.

### Stacked comparisons

Stacked charts are useful for composition but can make precise comparison of individual components difficult.

### Area-based comparisons

Area is generally less precise for quantitative comparison than position or length.

### Colour dependence

Do not make essential information inaccessible to people who cannot distinguish the chosen colours.

### Geographic distortion

Maps can give visual prominence to large areas even when geographic area is not the quantity of interest.

### Unclear baselines

For magnitude bar/column charts, preserve the meaningful zero baseline.

### Excessive decoration

Do not introduce visual elements that do not help answer the analytical question.

---

# 6. Accessibility and Communication

Consider:

- Colour accessibility
- Contrast
- Direct labelling
- Legible annotations
- Text alternatives
- Small-screen readability
- Clear units
- Clear scales
- Audience familiarity

Do not assume that a sophisticated chart is better simply because it encodes more information.

---

# 7. Recommendation Format

When recommending a visualisation, use:

### Primary recommendation

**[Chart type]**

Explain why it best addresses the reader's primary analytical task.

### FT category

**[Primary category]**

Add a secondary category when relevant.

### Alternatives

- **[Chart type]** — when it would be preferable.
- **[Chart type]** — important trade-off.

### Design considerations

Mention only the constraints relevant to this particular visualisation, such as:

- Ordering
- Baseline
- Scale
- Units
- Labels
- Number of series
- Colour
- Uncertainty
- Geographic normalisation
- Overplotting

---

# 8. Compact Decision Procedure

```text
1. What does the reader need to understand?

   Deviation
   Correlation
   Ranking
   Distribution
   Change over Time
   Part-to-Whole
   Magnitude
   Spatial
   Flow

2. What does the data allow?

   Variables
   Types
   Time
   Geography
   Categories
   Hierarchy
   Flows
   Uncertainty
   Positive/negative values

3. Which FT visual forms fit the analytical task?

   Generate 2–4 candidates.

4. Which candidates fail because of the data or presentation constraints?

   Eliminate them.

5. Which remaining form makes the required comparison clearest?

   Recommend it.

6. What is the reader actually comparing?

   Position
   Length
   Area
   Angle
   Colour
   Connection
   Spatial position
   Time/progression

7. What caveat matters?

   State it.
```

---

# 9. Core Rule

The skill should ultimately implement this sequence:

**Reader question → Analytical purpose → Data structure → FT candidate forms → Constraints → Visual encoding → Primary recommendation**

Do not implement:

**Dataset → familiar chart type.**

The FT Visual Vocabulary is a vocabulary for recognising and selecting visual forms, not a rule that each data type has one predetermined chart.