---
name: product-ui-design
description: Use when designing or building the interface of a product, tool, dashboard, web app, personal site or small browser game, where the main challenge is its identity, composition and usability rather than chart design. Use instead of the built-in frontend-design skill for this work. Requires a stated visual thesis before any code and rejects generic AI-generated aesthetics.
---

# Product UI design

Design the interface as a product, not a collection of components. The aim is an interface that looks as if it was designed for this product, its users and their work, not one that could belong to any product.

Chart selection, visual encoding and statistical representation are covered by the `dataviz-fundamentals` skill. Apply it to any charts. Do not repeat its rules here.

## 1. Establish the context first

**With a codebase.** Inspect it before writing any code: framework and build system, routing, styling approach and design tokens, existing components and layouts, fonts and brand assets, charting libraries, data-fetching and state patterns, and the test, lint, typecheck and build commands. Search the codebase for these. Do not assume. Existing conventions and any established design system take precedence unless there is a specific reason to depart from them.

**Without a codebase** (a single-file HTML app, an artifact or a prototype). State the delivery constraints before designing:
- whether the output must be a single file
- whether it must work offline
- which external sources are permitted (CDNs, font hosts)
- target devices and input (mouse, keyboard, touch, a tablet held by a child)
- how state persists
- any size limit

These constraints govern every later decision.

**When to ask.** If there is no existing product, no brand and no stated audience, ask the user one question about who will use the interface and for what, then choose a direction. In all other cases, decide yourself.

## 2. State a visual thesis before writing code

This is a hard requirement. Before any implementation, write the visual thesis into the response in two or three sentences. It must cover:
- what the product is
- who uses it, and how often
- what they are doing (monitoring, analysing, operating, configuring, reporting, playing)
- the intended character
- what it must deliberately not look like

Derive the thesis from the domain, the brand and the available assets, not from taste. It then governs typography, spacing, surfaces, colour, density, navigation and composition.

Generic, and therefore useless:
> A clean, modern dashboard with a professional look and intuitive navigation.

Specific enough to design from:
> An on-call handover board for a small operations team, read at shift change on a wall screen and on laptops. It should feel like a well-kept logbook: high contrast, typographic and dense, with status carried by position and label before colour. It should not look like a marketing dashboard or a chat app.

If the thesis has to change during the build, say so and restate it.

## 3. Reject the generic starting point

Do not reach for these by default:
- a left sidebar with top navigation
- a page title and subtitle over four KPI cards
- large rounded cards everywhere
- a pale grey background
- Inter, Roboto or a system font chosen by default
- purple or blue gradient accents
- soft shadows on everything
- pill-shaped controls
- identical card grids
- a generic "Analytics" heading
- oversized empty space
- every section boxed in a bordered rectangle

None of these is forbidden. They are forbidden only as unexamined defaults.

Test: *would this interface still look plausible if the logo and content were swapped for those of five unrelated SaaS products?* If so, identify which decisions are generic and change them.

## 4. Compose before choosing components

Decide what the user must notice first, what they must understand next, what they may investigate, what they may act on, and what can stay peripheral. Compose the page around those relationships. Only then choose components.

Structures to consider include asymmetric editorial layouts, dense operational workspaces, split views, persistent contextual rails, tables beside contextual summaries, expandable investigation areas, command-oriented interfaces and vertically flowing reports. Do not force every page into a regular grid.

Establish hierarchy with scale, position, typography, contrast, density and whitespace before adding containers, colour or shadows. The most important element on the page should be obvious without reading every label.

## 5. Typography within the delivery constraints

Use the existing fonts if there are any. If there are none, choose deliberately. Pairings worth considering include an editorial serif with a restrained sans, a technical grotesk with a monospace, a humanist sans, or a condensed display face with a neutral text face. The choice must serve the product, not show off.

Respect the constraints from section 1. In an offline or single-file app, a web font must be embedded, which costs file size, or it will fail to load. Subset it, or use a single weight. A carefully set system font stack is a legitimate, deliberate choice when the constraints rule out anything else. Give it a proper scale, weights, line height and tracking.

For numbers, use tabular numerals, align decimals and choose the precision deliberately. Use monospace where it signals technical or data context.

## 6. A small token system

Define semantic tokens for page background, surface, raised surface, divider, primary, secondary and muted text, accent, selected, success, warning, critical and information. Use them consistently.

Colour establishes hierarchy, grouping, state and identity. It is not decoration. Not everything needs a card: group content with whitespace, alignment, dividers, background shifts and shared edges before reaching for another rounded container.

## 7. Behaviour

- **States:** design the loading, empty and error states. Distinguish empty, zero, unavailable and failed-to-load from one another. Empty and error states say what happened and what the user can do next.
- **Data:** test with content that stresses the layout: long labels, extreme numbers, a single row, no rows, missing values.
- **Interaction:** use progressive disclosure, and keyboard shortcuts where they help the task. Never put essential information behind hover. Use motion only to show cause and effect, and respect the user's reduced-motion setting.
- **Responsive:** recompose the layout for smaller widths rather than shrinking it, deciding per element. Do not turn a useful table into a stack of cards to avoid horizontal scrolling.
- **Accessibility:** meet WCAG 2.2 AA unless the project sets another standard. Never show status by colour alone.

## 8. Keep the debug states reviewable

Use a small, explicit mechanism for forcing each state, such as `?debugState=loading|empty|error`. Do not build a fake backend to produce them.

Do not delete this mechanism before handing over, because the human review in section 10 depends on it.
- **Where the project has a dev mode,** gate the mechanism behind it (for example, the build tool's development flag).
- **In a single-file app,** a query-parameter check that only changes the displayed state may stay in the file. Document it in a comment at the top of the file.

Remove only the scaffolding that the review does not need.

## 9. Respect the technical architecture

Before adding a dependency, check whether an existing one already does the job. Do not add any of the following:
- a new UI framework for one component
- a second charting library
- a new state-management system for one page
- a large dependency to solve a small styling problem

Do not make unrelated refactors. Without a codebase, every external dependency must satisfy the constraints set in section 1.

## 10. Verify, and say exactly what was verified

If browser or visual tooling is available, render the page at desktop, tablet and phone width (about 390px), with realistic data and each debug state. Fix what you find and check again.

If visual tooling is not available, run whatever checks exist: typecheck, lint, tests and build. For a single file with no toolchain, check the structure and the script for errors.

Never claim to have seen something you could not see. Report one of the following:

`VISUALLY VERIFIED`: only when you actually inspected the rendered page.

`STRUCTURALLY VERIFIED: VISUAL REVIEW REQUIRED`: in every other case. Follow it with exact review steps, for example:

```text
STRUCTURALLY VERIFIED: VISUAL REVIEW REQUIRED

1. Run: npm run dev
2. Open: http://localhost:5173/board?debugState=loading
3. Check: layout and loading state at desktop width
4. Open: http://localhost:5173/board?debugState=empty
5. Check: empty-state message and next action
6. Repeat both at about 390px width
```

For a single-file app, the steps are the file name plus query parameters (for example, open `board.html?debugState=error` in a browser).

Never invent a URL, port, route or command. If you cannot determine one from the codebase, say what you know and what the human needs to find out.

## Final check

Before finishing, confirm all of the following:
- The thesis was stated before any code, and the result matches it.
- The result would not pass for a generic SaaS dashboard.
- The primary task is obvious at a glance.
- Every debug state named in the review steps still works.
- The verification claim is honest.

> Design the most appropriate interface for this product, these users, this information and these constraints. The product should decide the interface; components, frameworks and trends should serve that decision.
