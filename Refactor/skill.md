# Refactor

Perform behaviour-preserving refactoring with disciplined, incremental verification.

Be concise. Report only what affects a decision, risk or verification.

## Inputs

Establish these from the request before starting. If the goal, scope or execution mode is missing, ask. For the rest, discover what you can from the repository and state what you found.

- Goal: the concrete outcome the refactoring must achieve
- In scope: paths
- Out of scope: paths, layers, modules
- Constraints: contracts, performance budgets, deadlines
- Verification commands: build, tests, full suite, lint, type check; note slow or flaky suites
- Execution mode: plan-only | approval-required | execute (default: approval-required)
- Git: may create commits, yes or no (default: no)

## Execution modes

- plan-only: inspect and produce the plan; never modify files.
- approval-required: inspect, produce the plan, then wait for explicit approval. On approval, execute the approved plan as written. If the working tree or baseline has changed since planning, re-baseline first.
- execute: inspect, plan and execute without an additional approval gate.

## Non-negotiables

- Preserve externally observable behaviour by default. Documented and demonstrably relied-upon behaviour is part of the compatibility contract. Undocumented behaviour is a risk to investigate, not automatically a contract.
- No unrelated work. Changes outside the stated scope are allowed only when necessary to achieve the goal and explicitly identified in the plan.
- Do not add, remove, upgrade or downgrade dependencies, or regenerate lockfiles, without approval.
- Treat pre-existing user changes as immutable. Never overwrite, revert, reformat, stash or discard them. If they overlap planned changes, ask first.
- Do not remove code solely because static analysis finds no references. Check reflection, DI, configuration, plugins, dynamic loading and public exports.
- Do not edit generated output when a supported source of truth exists. Follow the repository's generation workflow.
- Do not touch vendored code, build outputs or existing migrations unless authorised.
- Never fabricate test results, coverage or metrics.
- If the goal cannot be materially advanced within scope at acceptable risk, make no structural change and explain why in the report.

## Design principles

1. Refactor for the stated goal. Leave code nobody needs to change alone.
2. Reduce complexity, not line count.
3. Prefer duplication to the wrong abstraction. Extract shared code only when the commonality is genuine.
4. Introduce patterns only when a specific problem calls for them.
5. Keep structural changes separate from behaviour changes.
6. Prefer mechanical, semantics-preserving transformations that tooling can verify.
7. Prefer small, independently reversible changes.

## Workflow

### Phase 1: Baseline

- Check git status and record pre-existing changes.
- Map the compatibility surface: exported APIs, CLI flags and exit codes, HTTP routes, events and message formats, configuration and environment variables, database schemas, serialised formats, plugin interfaces, reflection names, and operational logs or metrics.
- Run available verification and record the baseline.
- Separate pre-existing failures and known flaky or environmental failures from later regressions.
- Identify test gaps relevant to the intended changes.

### Phase 2: Assess

- Define acceptance criteria that directly test the goal.
- Identify only design problems that materially prevent those criteria.
- Group symptoms of the same underlying problem.
- For each finding give evidence and the smallest useful intervention.
- Do not optimise for an acceptance metric by introducing disproportionate complexity, indirection or hidden coupling.

### Phase 3: Plan

Produce an ordered list of small, independently reviewable steps. For each step state:

- change
- affected files
- risk
- compatibility concerns
- verification level

Where coverage is insufficient, propose characterisation tests first. For each such test, state whether the captured behaviour is contractual, relied upon, or preserved because its status is unknown.

In plan-only or approval-required mode, stop here.

### Phase 4: Execute

For each step:

- Make one coherent change.
- Run the smallest sufficient verification set.
- Run the full suite at sensible checkpoints and before finishing.
- If a failure is caused by the step, fix it only when the fix is directly required and mechanical. Otherwise revert the step and rethink it.
- If a failure predates the change or is environmental, record it.
- Never silently work around a regression.
- Keep each step independently reviewable and reversible.
- If commits are authorised, create one commit per coherent step.
- If execution shows the plan needs to change materially (new files, new risks, a different approach): in approval-required mode, stop and present the revised plan before continuing; in execute mode, continue and record the deviation and its reason in the report.

### Phase 5: Report

- For every acceptance criterion: met, partly met or not met, with evidence.
- What changed and why.
- What deliberately did not change.
- Verification results compared with baseline.
- Bugs found but not fixed.
- Residual risks and worthwhile follow-ups.

## When to ask vs proceed

Stop and ask when:

- a public contract may change;
- scope is ambiguous;
- existing user changes would be affected;
- a behaviour change appears necessary;
- a dependency change is needed;
- available verification is insufficient to establish reasonable confidence in behavioural preservation.

Otherwise proceed, stating assumptions that materially affect scope, behaviour or risk.
