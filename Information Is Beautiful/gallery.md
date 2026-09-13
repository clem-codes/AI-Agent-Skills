# Gallery of studied examples

Real, published Information Is Beautiful graphics, analysed in detail. This is a starter set covering four of the eight patterns in the main pattern library. When a task needs a pattern not covered here (flow diagrams, matrices, networks, small multiples), research a genuine example from informationisbeautiful.net's visualisation archive before designing, and add an entry below in the same format. Don't invent a hypothetical entry; the value of this library is that every entry was actually built, published, and in most cases publicly argued over.

---

## The Billion Dollar-o-Gram (2009, updated 2013)

**Pattern:** Proportional shapes

**The question being answered:** Big numbers reported in the news, a war costing $726bn, a company worth $227bn, a debt of $200bn, are individually almost meaningless. What do they actually mean next to each other?

**The central insight:** Once placed on the same page at the same honest scale, some figures reported by the media as enormous turn out to be small next to others, and some quietly enormous figures (the value of the global illegal drugs trade, for instance) rarely get reported as news at all.

**The data type:** Point-in-time monetary figures scraped from major news outlets (The New York Times, The Guardian, the BBC), each independently sourced and dated, covering government budgets, corporate valuations, debts, fines, and personal fortunes.

**Visual encoding:** Area-proportional blocks, arranged treemap-style, each sized to represent one dollar figure.

**Use of scale:** A single linear area scale across the entire graphic, so any two blocks can be compared directly by eye. No axis is drawn; relative size does all the comparative work.

**Composition:** Blocks are loosely grouped by theme (spending, earning, losing, giving, fighting, hustling) rather than strictly ranked, encouraging the eye to wander and compare rather than read top to bottom.

**Colour system:** Colour is tied to category of transaction (for example, purple for fighting-related spend, red for giving), so a viewer can visually scan for one type of behaviour across the whole graphic.

**Annotations:** Every block is labelled directly with its figure and a short description; nothing requires a separate legend to read an individual value.

**Why the design works:** It converts an abstraction, a number with nine zeroes, into a directly comparable physical quantity. A single glance delivers both a specific fact and that fact's place in a landscape of other facts, which a list or a bar chart of the same length would not do nearly as fast.

**Where the design could mislead:** People systematically underjudge how much bigger one area is than another, so two blocks that look "about twice the size" can represent a much larger real ratio. It also puts flows (a year's revenue) and stocks (a total accumulated debt) on the same scale; visually equal size can imply an economic comparability the two figures don't actually share.

**How to apply the underlying idea:** Any brief with a list of large, hard-to-compare quantities (budgets, market capitalisations, casualty figures, energy consumption) is a candidate for proportional shapes, but only when every value shares a genuinely comparable unit and time frame, and only when the area is computed by area, never by linear side length or radius.

---

## Mountains Out of Molehills (2007, interactive 2015)

**Pattern:** Timelines

**The question being answered:** Does the intensity of media coverage of a "scare story" track the real-world harm it caused?

**The central insight:** Some panics (Y2K, killer wasps, autism linked to vaccines) generated huge coverage against low or zero linked deaths, while the shape of coverage over time often tracked the news calendar rather than risk: violent video game coverage, for instance, spiked every April and November, tied to game release dates and the anniversary of a school shooting, not to any change in actual danger.

**The data type:** Counts of news mentions per scare-story category over time (sourced from Google News Timeline), cross-referenced against worldwide death tolls attributed to each topic.

**Visual encoding:** An overlapping area chart where each "mountain range" is one scare story and height represents intensity of media coverage.

**Use of scale:** A shared time axis running from 2000 onward. Height encodes number of stories, not deaths; the death toll is given separately, as a per-topic annotation, deliberately kept out of the shape itself.

**Composition:** The mountains sit side by side like a skyline, coloured by topic, which makes repeating patterns, like the twin peaks in video-game coverage, visible at a glance.

**Colour system:** One consistent hue per scare topic throughout, functioning as an in-place legend rather than a separate key.

**Annotations:** Rolling over a peak reveals the actual headline and the real death count for that story, anchoring the shape to a checkable fact.

**Why the design works:** The mountain metaphor literalises the idiom "making a mountain out of a molehill", so the insight is legible from the silhouette alone, before a single word is read.

**Where the design could mislead:** Because height encodes volume of coverage rather than actual risk, a careless reading could take a tall peak as "this was genuinely dangerous". The chart's argument depends entirely on the annotation doing the work of separating coverage from harm; without it, the shape alone could be read the wrong way round.

**How to apply the underlying idea:** Any brief about the gap between perceived risk and actual risk, hype cycles, or attention versus outcome suits a timeline built as a landscape rather than a line graph, provided the two measures being contrasted stay visually distinct rather than merging into a single misleading shape.

---

## Snake Oil? Scientific Evidence for Health Supplements (2010, revised repeatedly since)

**Pattern:** Annotated charts (a "balloon race": part scatter plot, part matrix of supplement against condition)

**The question being answered:** Of the hundreds of supplements marketed for health, which are actually backed by clinical evidence, and which are folklore?

**The central insight:** Evidence strength, not popularity or marketing spend, separates a small number of genuinely supported uses (green tea for cholesterol, for example) from the majority of supplement claims, which sit near the bottom of the evidence scale regardless of how widely they're sold.

**The data type:** Ordinal evidence-grade ratings distilled from clinical literature (Cochrane systematic reviews, PubMed, Examine.com), covering roughly 200 supplements against roughly 200 specific health conditions.

**Visual encoding:** A "balloon race": bubbles float at a height that encodes strength of evidence, with a horizontal "worth it" threshold line, and are grouped and coloured by supplement type.

**Use of scale:** Explicitly ordinal, not linear. Height bands correspond to evidence categories (strong, conflicting, no evidence) rather than a precise statistic, and this is disclosed rather than presented as continuous data.

**Composition:** Many small bubbles scattered across a wide canvas, filterable by health condition, so one underlying chart answers many different specific questions depending on what a viewer filters for.

**Colour system:** Colour distinguishes broad supplement categories (vitamins, herbs, minerals, compounds), so related clusters are visible even before filtering.

**Annotations:** Each bubble names the specific condition it addresses and links to the primary study behind its rating, since a single supplement is often well-evidenced for one condition and worthless for another.

**Why the design works:** It compresses a large, genuinely contested literature into one clear visual verdict per condition, while keeping the underlying evidence one click away, so the graphic invites scrutiny of itself rather than asserting unquestionable authority.

**Where the design could mislead:** Converting nuanced, sometimes conflicting clinical literature into a single ordinal height necessarily discards caveats; a bubble sitting high can still rest on a small or dated study. The Information Is Beautiful team has revised this dataset's ratings multiple times in response to challenges and new evidence, which is itself a sign of how much interpretive judgement the format has to compress.

**How to apply the underlying idea:** Any brief comparing many small entities on a single quality axis (safety ratings, policy effectiveness, marketing claims against evidence) suits a balloon race or annotated scatter, provided the ordinal nature of the underlying score is stated honestly rather than dressed up as precise measurement.

---

## Left vs Right: The Political Spectrum (2009, revised 2011)

**Pattern:** Radial structures (a concept-map, described by its own creator as a "rosette")

**The question being answered:** What actually distinguishes a "left" and a "right" political worldview across a wide range of issues?

**The central insight:** Rather than a single left-right dial, a wide set of concepts (attitudes to tax, tradition, equality, family) cluster into two loose, mirrored bundles fanning out from a shared centre, showing this is a spectrum of many correlated but distinct beliefs rather than one measurable axis.

**The data type:** Not measured data at all. Qualitative concepts and commonly held associations, synthesised by the authors from political theory and commentary.

**Visual encoding:** A radial "rosette" or concept-map, two mirrored fans of labelled petals branching outward from a central spine.

**Use of scale:** None in the numeric sense. Position along a petal and clustering of petals communicate closeness of association, not a measured quantity.

**Composition:** Strict left-right symmetry down the centre reinforces the two-sides framing, while petal length groups related ideas together within each side.

**Colour system:** One colour per side, red or blue, deliberately reversed between the US version and the world or UK version, since the same two colours map to opposite political sides in different countries.

**Annotations:** Short concept labels alone carry the entire explanation; there is no supporting paragraph of text.

**Why the design works:** The flower or rosette form makes an abstract, contested classification feel organic and navigable rather than dogmatic, inviting a viewer to travel across it and compare, rather than absorb a single fixed number.

**Where the design could mislead:** This is authorial synthesis presented in the visual language of data. Its own creator has said the original version subtly favoured the left through his own unconscious bias in wording, and had to revise it after public criticism from readers on the right. A radial concept-map borrows the visual authority of a "data visualisation" while actually encoding editorial judgement, which makes it the pattern in this library most likely to smuggle unstated opinion in as if it were measured fact.

**How to apply the underlying idea:** Use a radial or concept-map structure when the brief concerns relationships between many qualitative ideas rather than a measured quantity (mapping a debate, a taxonomy of related concepts, a set of overlapping values), but state plainly that the placement reflects editorial synthesis, and get an outside read on the wording for bias before treating it as finished, exactly as this example eventually needed.
